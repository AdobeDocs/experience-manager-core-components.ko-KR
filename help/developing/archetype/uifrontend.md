---
title: AEM Project Archetype 프론트엔드 빌드
description: AEM 기반 애플리케이션용 프로젝트 템플릿
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 99132b49-bd06-4ac2-9348-12c0dfdfe8b2
source-git-commit: 2ac16b15718128feefbe903e92f276b16fe96f69
workflow-type: tm+mt
source-wordcount: '1618'
ht-degree: 99%

---

# AEM Project Archetype의 ui.frontend 모듈 {#uifrontend-module}

AEM Project Archetype에는 Webpack 기반의 전용 프론트엔드 빌드 메커니즘(선택 사항)이 포함됩니다. 이에 ui.frontend 모듈은 JavaScript 및 CSS가 포함된 모든 프로젝트 프론트엔드 리소스의 중앙 위치가 됩니다. 이 유용하고 유연한 기능을 최대한 활용하려면 프론트엔드 개발이 AEM 프로젝트에 얼마나 적합한지 이해하는 것이 중요합니다.

## AEM 프로젝트 및 프론트엔드 개발 {#aem-and-front-end-development}

간단히 정리하면 AEM 프로젝트는 별도로 구성된 2개의 부분이 서로 관련된 것으로 생각할 수 있습니다.

* AEM 논리를 유도하고 Java 라이브러리, OSGi 서비스 등을 생성하는 백엔드 개발
* 결과 웹 프레젠테이션 및 비헤이비어를 유도하고 JavaScript 및 CSS 라이브러리를 생성하는 프론트엔드 개발

이 두 가지 개발 프로세스가 프로젝트의 서로 다른 부분에 중점을 두기 때문에 백엔드 및 프론트엔드 개발이 동시에 발생할 수 있습니다.

![프론트엔드 워크플로 다이어그램](/help/assets/front-end-flow.png)

결과적으로 모든 프로젝트는 이들 두 가지 개발 역량(예: 백엔드 및 프론트엔드)의 출력을 사용해야 합니다.

`npm run dev`가 실행되면 ui.frontend 모듈에 보관된 JavaScript 및 CSS 파일을 수집하고, 축소된 두 개의 클라이언트 라이브러리나 ClientLib(`clientlib-site` 및 `clientlib-dependencies`라고 함)을 생성하고 ui.apps 모듈에 저장하는 프론트엔드 빌드 프로세스가 시작됩니다. AEM에 ClientLib을 배포할 수 있고 이를 통해 클라이언트측 코드를 저장소에 저장할 수 있습니다.

`mvn clean install -PautoInstallPackage`를 사용하여 전체 AEM Project Archetype을 실행하면 ClientLib이 포함된 모든 프로젝트 아티팩트가 AEM 인스턴스로 푸시됩니다.

>[!TIP]
>
>[AEM 개발 설명서](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html)에서 AEM의 ClientLib 처리 방법, [ClientLib 포함](/help/developing/including-clientlibs.md) 방법에 대해 자세히 살펴보거나 [ui.frontend 모듈의 ClientLib 사용 방법을 참조하십시오.](#clientlib-generation)

## ClientLib 개요 {#clientlibs}

[AEM ClientLib](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html)으로 프론트엔드 모듈을 사용할 수 있습니다. NPM 빌드 스크립트가 실행되면 앱이 빌드되고, aem-clientlib-generator 패키지가 결과 빌드 출력을 요청하면 ClientLib으로 변환됩니다.

ClientLib은 다음 파일과 디렉터리로 구성됩니다.

* `css/`: HTML로 요청될 수 있는 CSS 파일
* `css.txt`: 파일이 병합될 수 있도록 AEM에 지시하고 `css/` 파일 이름을 알려 줍니다.
* `js/`: HTML로 요청될 수 있는 JavaScript 파일
* `js.txt` 파일이 병합될 수 있도록 AEM에 지시하고 `js/` 파일 이름을 알려 줍니다.
* `resources/`: 소스 맵, 비-진입점 코드 청크(코드 분할이 원인), 정적 에셋(예: 아이콘) 등

## 가능한 프론트엔드 개발 워크플로 {#possible-workflows}

프론트엔드 빌드 모듈은 유용하고 매우 유연한 도구이지만 사용 방법에 대해서는 특별한 의견을 제시하지 않습니다. 다음은 사용량에 대한 2가지 *가능한* 사례이지만 개별 프로젝트는 다른 사용 모델을 보여 줄 수 있습니다.

### Webpack 정적 개발 서버 사용 {#using-webpack}

ui.frontend 모듈 내 AEM 웹 페이지의 정적 출력 기반으로 Webpack을 사용하여 스타일링하고 개발할 수 있습니다.

1. 페이지 미리보기 모드를 사용하거나 URL로 `wcmmode=disabled`를 전달하면서 AEM의 페이지 미리보기
1. 페이지 소스를 보고 ui.frontend 모듈 내 정적 HTML로 저장합니다.
1. [Webpack 시작](#webpack-dev-server) 후 필수 JavaScript와 CSS 스타일링 및 생성을 시작합니다.
1. `npm run dev`를 실행하여 ClientLib을 생성합니다.

이 흐름에서 AEM 개발자는 단계 1, 2를 수행하고, 정적 HTML을 AEM HTML 출력에 따라 개발한 프론트엔드 개발자에게 전달할 수 있습니다.

>[!TIP]
>
>페이지 수준이 아닌 구성 요소 수준에서 작업할 수 있도록 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_kr)를 활용하여 각 구성 요소의 마크업 출력 샘플을 캡처할 수 있습니다.

### 스토리북 사용 {#using-storybook}

[스토리북](https://storybook.js.org)을 사용하여 보다 작은 단위의 프론트엔드 개발을 수행할 수 있습니다. 스토리북이 AEM Project Archetype에 포함되지 않지만 ui.frontend 모듈에 설치하여 스토리북 아티팩트를 저장할 수 있습니다. AEM에서 테스트할 준비가 되면 C`npm run dev`를 실행하여 ClientLib으로 배포할 수 있습니다.

>[!NOTE]
>
>[스토리북](https://storybook.js.org)은 AEM Project Archetype에 포함되지 않습니다. 스토리북 사용을 선택한 경우 별도로 설치해야 합니다.

### 마크업 확인 {#determining-markup}

프로젝트에 어떤 프론트엔드 개발 워크플로를 구현하든지 백엔드 개발자와 프론트엔드 개발자는 먼저 마크업에 동의해야 합니다. 일반적으로 AEM은 핵심 구성 요소에서 제공하는 마크업을 정의합니다. [단, 필요한 경우 이를 사용자 정의할 수 있습니다](/help/developing/customizing.md#customizing-the-markup).

## ui.frontend 모듈 {#ui-frontend-module}

AEM Project Archetype에는 다음 기능과 함께 Webpack 기반의 전용 프론트엔드 빌드 메커니즘(선택 사항)이 포함됩니다.

* 전체 TypeScript, ES6 및 ES5 지원(해당되는 Webpack 래퍼 포함)
* TypeScript 및 JavaScript 린팅, TSLint 규칙 세트 사용
* ES5 출력, 레거시 브라우저 지원의 경우
* 글로빙
   * 아무 곳에 가져오기를 추가할 필요가 없습니다.
   * 이제 JS 및 CSS 파일을 각 구성 요소에 추가할 수 있습니다.
      * 모범 사례는 `/clientlib/js`, `/clientlib/css` 또는 `/clientlib/scss` 아래에 있습니다.
   * 모든 것이 Webpack을 통해 실행되기 때문에 `.content.xml` 또는 `js.txt`/`css.txt` 파일을 필요로 하지 않습니다.
   * 글로버는 `/component/` 폴더 아래의 모든 JS 파일을 가져옵니다.
      * Webpack에서 CSS/SCSS 파일은 JS 파일을 통해 내부 결속될 수 있습니다.
      * 파일은 `sites.js`와 `vendors.js`의 두 진입점을 통해 가져옵니다.
   * AEM에서 사용하는 유일한 파일은 출력 파일로 `/clientlib-site`의 `site.js` 및 `site.css`와 `/clientlib-dependencies`의 `dependencies.js` 및 `dependencies.css`입니다.
* 청크
   * 메인(사이트 js/css)
   * 공급업체(종속성 js/css)
* 전체 Sass/Scss 지원(Sass는 Webpack을 통해 CSS에 컴파일됨)
* AEM 로컬 인스턴스에 내장된 프록시가 있는 정적 Webpack 개발 서버

>[!NOTE]
>
>ui.frontend에 대한 기술 정보를 보려면 [GitHub 설명서](https://github.com/adobe/aem-project-archetype/blob/master/src/main/archetype/ui.frontend.general/README.md)를 참조하십시오.

## 설치 {#installation}

1. [NodeJS](https://nodejs.org/en/download/)(v10+)를 전체적으로 설치합니다. npm을 설치할 수도 있습니다.
1. 프로젝트의 ui.frontend로 이동하고 `npm install`를 실행합니다.

>[!NOTE]
>
>옵션 `-DoptionIncludeFrontendModule=y`로 [Archetype을 실행](overview.md)하면 ui.frontend 폴더가 채워집니다.

## 사용량 {#usage}

다음 npm 스크립트는 프론트엔드 워크플로로 연결됩니다.

* `npm run dev` - 전체 빌드에서 JS 최적화는 비활성화되고(트리 셰이킹 등), 소스 맵은 활성화되고 CSS 최적화는 비활성화됩니다.
* `npm run prod` - 전체 빌드에서 JS 최적화는 활성화되고(트리 셰이킹 등), 소스 맵은 비활성화되고 CSS 최적화는 활성화됩니다.
* `npm run start`- AEM의 종속성을 최소화하는 로컬 개발을 위해 정적 Webpack 개발 서버를 시작합니다.

## 출력 {#output}

ui.frontend 모듈은 `ui.frontend/src` 폴더 아래의 코드를 컴파일하고 컴파일된 CSS 및 JS와 `ui.frontend/dist`로 지정된 폴더 아래의 모든 리소스를 출력합니다.

* **사이트** - `dist/`clientlib-site 폴더에 레이아웃 종속 이미지와 글꼴에 대한 `site.js`, `site.css` 및 `resources/`폴더가 생성됩니다.
* **종속성** - `dist/clientlib-dependencies`폴더에 `dependencies.js` 및 `dependencies.css`가 생성됩니다.

### JavaScript {#javascript}

* 최적화 - 제작 빌드의 경우 사용 중이거나 호출되지 않은 모든 JS는 제거됩니다.

### CSS {#css}

* 자동 접두사 사용 - 접두사 플러그인을 통해 모든 CSS를 실행하고, 접두사 사용이 필요한 속성에는 해당 접두사를 자동으로 추가합니다.
* 최적화 - 개시하는 경우 다음 기본 규칙에 따라 CSS를 표준화하는 Optimizer(cssnano)를 통해 모든 CSS를 실행합니다.
   * 브라우저 호환성과 압축을 유지하면서 CSS 계산 표현식을 줄이고 동일한 길이, 시간 및 각도 값을 변환합니다. 기본적으로 길이 값은 변환되지 않습니다.
   * 규칙, 선택기 및 선언 관련 댓글을 지웁니다.
   * 규칙과 선언에서 복제된 규칙을 제거합니다.
      * 정확한 복제본을 제작하는 경우에만 작동합니다.
   * 출력에 영향을 주지 않기 때문에 비어있는 규칙, 빈 선택기가 포함된 미디어 쿼리와 규칙을 제거합니다.
   * 선택기에 의한 인접 규칙과 겹치는 속성/값 쌍을 병합합니다.
   * 단일 @charset가 CSS 파일에만 존재하는지, 그리고 파일이 문서 맨 위로 이동하는지 확인합니다.
   * 결과 출력이 유사하면 CSS 초기 키워드를 실제 값으로 바꿉니다.
   * SVGO로 인라인 SVG 정의를 압축합니다.
* 정리 - 온디맨드로 생성된 CSS, JS 및 맵 파일을 지우는 명시적 정리 작업이 포함됩니다.
* 소스 매핑 - 개발 빌드만 해당

>[!NOTE]
>
>프론트엔드 빌드 옵션은 일반 구성 파일을 공유하는 개발-제작 전용 Webpack 구성 파일을 활용합니다. 이렇게 하면 개발 및 제작 설정 값을 개별적으로 수정할 수 있습니다.

### 클라이언트 라이브러리 생성 {#clientlib-generation}

ui.frontend 모듈 빌드 프로세스는 [aem-clientlib-generator](https://www.npmjs.com/package/aem-clientlib-generator) 플러그인을 활용하여 컴파일된 CSS, JS 및 리소스를 ui.apps 모듈로 이전할 수 있습니다. `clientlib.config.js`에서 aem-clientlib-generator 구성을 정의합니다. 다음 클라이언트 라이브러리가 생성됩니다.

* **clientlib-site** - `ui.apps/src/main/content/jcr_root/apps/<app>/clientlibs/clientlib-site`
* **clientlib-dependencies** - `ui.apps/src/main/content/jcr_root/apps/<app>/clientlibs/clientlib-dependencies`

### 페이지에 클라이언트 라이브러리 포함 {#clientlib-inclusion}

`clientlib-site` 및 `clientlib-dependencies` 범주는 [페이지 정책 구성](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/components-templates/templates.html#template-definitions)을 통해 기본 템플릿의 일부로 페이지에 포함됩니다. 정책을 조회하려면 **콘텐츠 페이지 템플릿 > 페이지 정보 > 페이지 정책**&#x200B;을 편집합니다.

다음과 같이 사이트 페이지에 클라이언트 라이브러리가 마지막으로 포함됩니다.

```html
<HTML>
    <head>
        <link rel="stylesheet" href="clientlib-base.css" type="text/css">
        <script type="text/javascript" src="clientlib-dependencies.js"></script>
        <link rel="stylesheet" href="clientlib-dependencies.css" type="text/css">
        <link rel="stylesheet" href="clientlib-site.css" type="text/css">
    </head>
    <body>
        ....
        <script type="text/javascript" src="clientlib-site.js"></script>
        <script type="text/javascript" src="clientlib-base.js"></script>
    </body>
</HTML>
```

페이지 정책 업데이트 및/또는 각 클라이언트 라이브러리에 대한 범주 및 엠베디드 속성 수정을 통해 상기 포함된 내용을 수정할 수 있습니다.

### 정적 Webpack 개발 서버 {#webpack-dev-server}

ui.frontend 모듈에는 AEM 외부서 라이브로 프론트엔드 개발을 빠르게 다시 로드할 수 있는 webpack-dev-server가 포함됩니다. 설정은 html-webpack-plugin을 활용하여 ui.frontend 모듈에서 컴파일된 CSS 및 JS를 정적 HTML 템플릿에 자동으로 주입할 수 있습니다.

#### 중요 파일 {#important-files}

* `ui.frontend/webpack.dev.js`
   * 이 중요 파일은 webpack-dev-server를 위한 구성을 포함하고 사용할 HTML 템플릿을 지정합니다.
   * 또한 localhost:4502에서 실행 중인 AEM 인스턴스에 대한 프록시 구성을 포함합니다.
* `ui.frontend/src/main/webpack/static/index.html`
   * 이는 서버가 실행할 수 있는 정적 HTML입니다.
   * 이를 통해 개발자는 CSS/JS를 변경하고 마크업에 즉시 반영되었는지 확인할 수 있습니다.
   * 이 파일에 배치된 마크업이 AEM 구성 요소에서 생성한 마크업을 반영한다고 가정해 봅니다.
   * 이 파일의 마크업은 AEM 구성 요소 마크업과 자동으로 동기화되지 않습니다.
   * 이 파일에는 핵심 구성 요소 CSS 및 반응형 그리드 CSS 등 AEM에 저장된 클라이언트 라이브러리에 대한 참조가 포함됩니다.
   * Webpack 개발 서버는 AEM 인스턴스를 실행하는 로컬에서 `ui.frontend/webpack.dev.js`의 구성에 따라 해당 CSS/JS가 포함된 프록시로 설정됩니다.

#### 사용 {#using-webpack-server}

1. 프로젝트 루트에서 명령 `mvn -PautoInstallSinglePackage clean install`를 실행하여 `localhost:4502`에서 실행 중에 AEM 인스턴스에 전체 프로젝트를 설치합니다.
1. `ui.frontend` 폴더 내부로 이동합니다.
1. 다음 명령 `npm run start`를 실행하여 Webpack 개발 서버를 시작합니다. 시작되면 브라우저(`localhost:8080` 또는 다음 사용 가능한 포트)를 여십시오.

이제 CSS, JS, SCSS, 및 TS 파일을 수정하고, Webpack 개발 서버에 바로 반영되는 변경 사항을 확인할 수 있습니다.

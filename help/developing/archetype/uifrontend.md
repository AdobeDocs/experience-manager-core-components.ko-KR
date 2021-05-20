---
title: AEM Project Archetype 프런트 엔드 빌드
description: AEM 기반 응용 프로그램용 프로젝트 템플릿
feature: 핵심 구성 요소, AEM 프로젝트 원형
role: Architect, Developer, Administrator
exl-id: 99132b49-bd06-4ac2-9348-12c0dfdfe8b2
source-git-commit: 8ff36ca143af9496f988b1ca65475497181def1d
workflow-type: tm+mt
source-wordcount: '1625'
ht-degree: 0%

---

# AEM 프로젝트 원형 {#uifrontend-module}의 ui.frontend 모듈

AEM 프로젝트 원형 에는 웹 팩을 기반으로 하는 선택적 전용 프런트 엔드 빌드 메커니즘이 포함되어 있습니다. 따라서 ui.frontend 모듈은 JavaScript 및 CSS 파일을 비롯한 모든 프로젝트의 프런트 엔드 리소스의 중앙 위치가 됩니다. 이 유용하고 유연한 기능을 최대한 활용하려면 프런트 엔드 개발이 AEM 프로젝트에 어떻게 적합한지 이해하는 것이 중요합니다.

## AEM 프로젝트 및 프런트 엔드 개발 {#aem-and-front-end-development}

매우 단순화된 용어로 AEM 프로젝트는 두 개의 서로 다른 관련 부분으로 구성됩니다.

* AEM의 논리를 구동하고 Java 라이브러리, OSGi 서비스 등을 생산하는 백엔드 개발
* 결과 웹 사이트의 프레젠테이션 및 동작을 유도하고 JavaScript 및 CSS 라이브러리를 생성하는 프런트 엔드 개발

이 두 개발 프로세스는 프로젝트의 서로 다른 부분에 초점을 맞추기 때문에 백엔드 및 프런트 엔드 개발이 동시에 진행될 수 있습니다.

![프런트엔드 워크플로우 다이어그램](/help/assets/front-end-flow.png)

그러나 결과 프로젝트는 백엔드 및 프런트엔드 모두에서 이러한 개발 작업의 결과물을 사용해야 합니다.

`npm run dev`을 실행하면 ui.frontend 모듈에 저장된 JavaScript 및 CSS 파일을 수집하는 프런트 엔드 빌드 프로세스가 시작되고, 축소된 클라이언트 라이브러리 또는 `clientlib-site` 및 `clientlib-dependencies`라는 두 개를 생성하여 ui.apps 모듈에 전달합니다. ClientLibs는 AEM에 배포할 수 있으며 리포지토리에 클라이언트측 코드를 저장할 수 있도록 해줍니다.

전체 AEM 프로젝트 원형이 `mvn clean install -PautoInstallPackage`을 사용하여 실행되면 ClientLibs를 포함하는 모든 프로젝트 아티팩트가 AEM 인스턴스에 푸시됩니다.

>[!TIP]
>
>AEM이 [AEM 개발 설명서](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html)에서 ClientLibs를 처리하는 방법, [Include](/help/developing/including-clientlibs.md)하는 방법 또는 ui.frontend 모듈에서 ClientLibs를 사용하는 방법에 대해 자세히 알아보십시오.](#clientlib-generation)[

## ClientLibs 개요 {#clientlibs}

프런트 엔드 모듈은 [AEM ClientLib](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html)을(를) 사용하여 사용할 수 있습니다. NPM 빌드 스크립트를 실행할 때 앱이 빌드되고 aem-clientlib-generator 패키지가 결과 빌드 출력을 가져와 ClientLib로 변환합니다.

ClientLib은 다음 파일과 디렉터리로 구성됩니다.

* `css/`:HTML에서 요청할 수 있는 CSS 파일
* `css.txt`:병합할 수  `css/` 있도록 AEM에 파일의 순서와 이름을 알려줍니다
* `js/`:HTML에서 요청할 수 있는 JavaScript 파일
* `js.txt` 병합할 수  `js/` 있도록 AEM에 파일의 순서와 이름을 알려줍니다
* `resources/`:소스 맵, 비시작 지점 코드 청크(코드 분할에 의한), 정적 자산(예: 아이콘) 등은

## 가능한 프런트 엔드 개발 워크플로우 {#possible-workflows}

프런트 엔드 빌드 모듈은 유용하고 매우 유연한 도구이지만 사용 방법에 대해 특별한 의견이 없습니다. 다음은 *가능한* 사용법에 대한 두 가지 예입니다. 그러나 개별 프로젝트에 다른 사용 모델이 필요할 수도 있습니다.

### Webpack 정적 개발 서버 사용 {#using-webpack}

웹 팩을 사용하면 ui.frontend 모듈 내의 AEM 웹 페이지의 정적 출력을 기반으로 스타일을 지정하고 개발할 수 있습니다.

1. 페이지 미리 보기 모드를 사용하거나 URL에서 `wcmmode=disabled`으로 전달하는 AEM의 미리 보기 페이지
1. ui.frontend 모듈 내에서 페이지 소스를 보고 정적 HTML로 저장
1. [웹 ](#webpack-dev-server) 패키지를 시작하고 필요한 JavaScript 및 CSS를 스타일링 및 생성하기 시작합니다
1. `npm run dev`을 실행하여 ClientLibs를 생성합니다.

이 플로우에서 AEM 개발자는 1단계와 2단계를 수행하고 AEM HTML 출력을 기반으로 개발하는 프런트 엔드 개발자에게 정적 HTML을 전달할 수 있습니다.

>[!TIP]
>
>또한 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library)를 활용하여 페이지 수준이 아닌 구성 요소 수준에서 작동하도록 각 구성 요소의 마크업 출력 샘플을 캡처할 수 있습니다.

### 스토리북 사용 {#using-storybook}

[Storybook](https://storybook.js.org)을 사용하여 보다 원자적 프런트 엔드 개발을 수행할 수 있습니다. Storybook은 AEM Project Archetype에 포함되지 않지만, 이를 설치하고 ui.frontend 모듈 내에 Storybook 아티팩트를 저장할 수 있습니다. AEM 내에서 테스트할 준비가 되면 `npm run dev` 을 실행하여 ClientLibs로 배포할 수 있습니다.

>[!NOTE]
>
>[](https://storybook.js.org) Storybookis는 AEM Project Archetype에 포함되어 있지 않습니다. 사용하도록 선택한 경우 별도로 설치해야 합니다.

### 마크업 {#determining-markup} 확인

프로젝트를 위해 구현하려는 프런트 엔드 개발 워크플로우에서 백엔드 개발자와 프런트 엔드 개발자는 마크업에 먼저 동의해야 합니다. 일반적으로 AEM은 핵심 구성 요소에서 제공하는 마크업을 정의합니다. [그러나 필요한 경우 사용자 지정할 수 있습니다](/help/developing/customizing.md#customizing-the-markup).

## ui.frontend 모듈 {#ui-frontend-module}

AEM Project Archetype에는 다음 기능이 포함된 웹 팩을 기반으로 하는 선택적 전용 프런트 엔드 빌드 메커니즘이 포함되어 있습니다.

* 전체 TypeScript, ES6 및 ES5 지원(적용 가능한 웹 팩 래퍼 포함)
* TSLint 규칙 세트를 사용하여 TypeScript 및 JavaScript 연결
* 레거시 브라우저 지원을 위한 ES5 출력
* Globbing
   * 어디에나 가져오기를 추가할 필요가 없습니다.
   * 이제 모든 JS 및 CSS 파일을 각 구성 요소에 추가할 수 있습니다.
      * 가장 좋은 방법은 `/clientlib/js`, `/clientlib/css` 또는 `/clientlib/scss` 아래에 있습니다
   * 모든 파일이 웹 팩을 통해 실행되므로 `.content.xml` 또는 `js.txt`/`css.txt` 파일이 필요하지 않습니다.
   * 글로버는 `/component/` 폴더 아래에 있는 모든 JS 파일을 가져옵니다.
      * 웹 팩을 사용하면 CSS/SCSS 파일을 JS 파일을 통해 에 체인으로 연결할 수 있습니다.
      * 두 시작 지점 `sites.js` 및 `vendors.js`을 통해 가져옵니다.
   * AEM에서 소비한 유일한 파일은 `/clientlib-site`의 출력 파일 `site.js` 및 `site.css`뿐만 아니라 `/clientlib-dependencies`의 `dependencies.js` 및 `dependencies.css`입니다
* 청크
   * 기본(사이트 js/css)
   * 공급업체(종속성 js/css)
* 전체 Sass/Scs 지원(Sass는 웹 팩을 통해 CSS에 컴파일됨)
* AEM의 로컬 인스턴스에 프록시가 내장된 정적 웹 팩 개발 서버

>[!NOTE]
>
>ui.frontend 모듈에 대한 기술적인 정보는 GitHub](https://github.com/adobe/aem-project-archetype/blob/master/src/main/archetype/ui.frontend.general/README.md)의 [설명서를 참조하십시오.

## 설치 {#installation}

1. 전역적으로 [NodeJS](https://nodejs.org/en/download/)(v10+)를 설치합니다. npm도 설치됩니다.
1. 프로젝트에서 ui.frontend로 이동하고 `npm install` 을 실행합니다.

>[!NOTE]
>
>ui.frontend 폴더를 채우려면 `-DoptionIncludeFrontendModule=y` 옵션과 함께 [원형](overview.md)을 실행해야 합니다.

## 사용량 {#usage}

다음 npm 스크립트는 프런트 엔드 워크플로우를 구동합니다.

* `npm run dev` - JS 최적화를 사용하지 않는 전체 빌드(트리 흔들기 등)와 소스 맵 활성화와 CSS 최적화를 사용할 수 없습니다.
* `npm run prod` - JS 최적화가 활성화된 전체 빌드(트리 흔들기 등), 소스 맵이 비활성화되고 CSS 최적화가 활성화되었습니다.
* `npm run start` - AEM에 대한 최소한의 종속성으로 로컬 개발을 위한 정적 웹 팩 개발 서버를 시작합니다.

## 출력 {#output}

ui.frontend 모듈은 `ui.frontend/src` 폴더 아래의 코드를 컴파일하여 컴파일된 CSS 및 JS와 `ui.frontend/dist` 폴더 아래에 있는 모든 리소스를 출력합니다.

* **사이트**  -  `site.js`  `site.css` 및  `resources/` 레이아웃 종속 이미지 및 글꼴용 폴더가 clientlib- `dist/`site 폴더에 생성됩니다.
* **종속성**  -  `dependencies.js` 및 `dependencies.css` 는 폴더에  `dist/clientlib-dependencies` 만들어집니다.

### JavaScript {#javascript}

* 최적화 - 프로덕션 빌드의 경우 사용되거나 호출되지 않는 모든 JS가 제거됩니다.

### CSS {#css}

* 자동 수정 - 모든 CSS는 사전 수정을 통해 실행되며 사전 수정이 필요한 모든 속성은 자동으로 CSS에 추가됩니다.
* 최적화 - 포스트에서 모든 CSS는 다음 기본 규칙에 따라 표준화하는 최적화 프로그램(cssnano)을 통해 실행됩니다.
   * 가능한 모든 위치에서 CSS 계산 표현식을 줄임으로써 브라우저 호환성과 압축을 모두 보장합니다
등가 길이, 시간 및 각도 값 간에 변환합니다. 기본적으로 길이 값은 변환되지 않습니다.
   * 규칙, 선택기 및 선언의 주석 제거
   * 중복된 규칙, at-rules 및 선언 제거
      * 이는 정확한 중복에만 작동합니다.
   * 출력에 영향을 주지 않으므로 빈 규칙, 미디어 쿼리 및 규칙이 비어 있는 선택기를 제거합니다
   * 선택기와 겹치는 속성/값 쌍으로 인접 규칙을 병합합니다
   * CSS 파일에 단일 @charset만 있고 문서 맨 위로 이동되도록 합니다
   * 결과 출력이 더 작은 경우 CSS 초기 키워드를 실제 값으로 바꿉니다
   * SVGO를 사용하여 인라인 SVG 정의 압축
* 정리 - 생성된 CSS, JS 및 Map 파일을 주문형 지우기에 대한 명시적 정리 작업을 포함합니다.
* 소스 매핑 - 개발 빌드만

>[!NOTE]
>
>프런트 엔드 빌드 옵션은 일반적인 구성 파일을 공유하는 개발 전용 및 제품 전용 웹 팩 구성 파일을 사용합니다. 이렇게 하면 개발 및 프로덕션 설정을 독립적으로 수정할 수 있습니다.

### 클라이언트 라이브러리 생성 {#clientlib-generation}

ui.frontend 모듈 빌드 프로세스는 [aem-clientlib-generator](https://www.npmjs.com/package/aem-clientlib-generator) 플러그인을 사용하여 컴파일된 CSS, JS 및 모든 리소스를 ui.apps 모듈로 이동합니다. aem-clientlib-generator 구성은 `clientlib.config.js`에 정의되어 있습니다. 다음 클라이언트 라이브러리가 생성됩니다.

* **clientlib-site**  -  `ui.apps/src/main/content/jcr_root/apps/<app>/clientlibs/clientlib-site`
* **clientlib-dependencies**  -  `ui.apps/src/main/content/jcr_root/apps/<app>/clientlibs/clientlib-dependencies`

### 페이지에 클라이언트 라이브러리 포함 {#clientlib-inclusion}

`clientlib-site` 및  `clientlib-dependencies` 카테고리는 기본 템플릿의 일부로  [페이지 정책 ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/components-templates/templates.html#template-definitions) 구성을 통해 페이지에 포함됩니다. 정책을 보려면 **컨텐츠 페이지 템플릿 > 페이지 정보 > 페이지 정책**&#x200B;을 편집하십시오.

사이트 페이지에 클라이언트 라이브러리를 최종 포함하는 방법은 다음과 같습니다.

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

위의 포함 사항은 물론 페이지 정책을 업데이트하거나 각 클라이언트 라이브러리의 카테고리 및 포함 속성을 수정하여 수정할 수 있습니다.

### 정적 웹 팩 개발 서버 {#webpack-dev-server}

ui.frontend 모듈에 포함된 는 AEM 외부의 빠른 프런트 엔드 개발을 위해 라이브 재로드를 제공하는 웹 팩-개발 서버입니다. 이 설정은 html-webpack-plugin을 활용하여 ui.frontend 모듈에서 컴파일된 CSS 및 JS를 정적 HTML 템플릿에 자동으로 주입합니다.

#### 중요 파일 {#important-files}

* `ui.frontend/webpack.dev.js`
   * 여기에는 웹 팩-개발-서비스에 대한 구성이 포함되어 있으며, 사용할 html 템플릿을 가리킵니다.
   * 로컬 호스트:4502에서 실행되는 AEM 인스턴스에 대한 프록시 구성도 포함되어 있습니다.
* `ui.frontend/src/main/webpack/static/index.html`
   * 서버가 실행되는 정적 HTML입니다.
   * 이렇게 하면 개발자는 CSS/JS를 변경하고 이를 마크업에 즉시 반영하도록 할 수 있습니다.
   * 이 파일에 배치된 마크업이 AEM 구성 요소에 의해 생성된 마크업을 정확하게 반영한다고 가정합니다.
   * 이 파일의 마크업은 AEM 구성 요소 마크업을 사용하여 자동으로 동기화되지 않습니다.
   * 이 파일에는 코어 구성 요소 CSS 및 응답형 그리드 CSS와 같이 AEM에 저장된 클라이언트 라이브러리에 대한 참조도 포함되어 있습니다.
   * 웹 팩 개발 서버는 이러한 CSS/JS를 `ui.frontend/webpack.dev.js`에 있는 구성에 따라 실행 중인 로컬 AEM 인스턴스에서 프록시하도록 설정되어 있습니다.

#### 사용 {#using-webpack-server}

1. 프로젝트의 루트 내에서 `mvn -PautoInstallSinglePackage clean install` 명령을 실행하여 전체 프로젝트를 `localhost:4502`에서 실행되는 AEM 인스턴스에 설치합니다.
1. `ui.frontend` 폴더 내부를 탐색합니다.
1. 다음 명령 `npm run start`을 실행하여 웹 팩 개발 서버를 시작합니다. 시작되면 브라우저(`localhost:8080` 또는 사용 가능한 다음 포트)를 열어야 합니다.

이제 CSS, JS, SCSS 및 TS 파일을 수정하고 웹 팩 개발 서버에 즉시 반영되는 변경 사항을 확인할 수 있습니다.

---
title: AEM 프로젝트 원형 프런트 엔드 구축
description: AEM 기반 응용 프로그램용 프로젝트 템플릿
feature: 핵심 구성 요소, AEM 프로젝트 원형
role: 건축가, 개발자, 관리자
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '1628'
ht-degree: 0%

---


# AEM 프로젝트 원형형의 ui.frontend 모듈 {#uifrontend-module}

AEM Project Tranype에는 Webpack을 기반으로 하는 선택적 전용 프런트 엔드 빌드 메커니즘이 포함되어 있습니다. 따라서 ui.frontend 모듈은 JavaScript 및 CSS 파일을 비롯한 모든 프로젝트의 프런트 엔드 리소스에 대한 중앙 위치가 됩니다. 이 유용하고 유연한 기능을 최대한 활용하려면 프런트 엔드 개발이 AEM 프로젝트에 어떻게 적합한지 이해하는 것이 중요합니다.

## AEM 프로젝트 및 프런트 엔드 개발 {#aem-and-front-end-development}

매우 간단하게 말하면 AEM 프로젝트는 서로 다르지만 관련 두 부분으로 구성된 것으로 간주될 수 있습니다.

* AEM의 논리를 지원하고 Java 라이브러리, OSGi 서비스 등을 생산하는 백엔드 개발
* 결과 웹 사이트의 표시 및 동작을 유도하고 JavaScript 및 CSS 라이브러리를 생성하는 프런트 엔드 개발

이러한 두 개발 프로세스는 프로젝트의 서로 다른 부분에 중점을 두기 때문에 백엔드 및 프런트엔드 개발이 동시에 발생할 수 있습니다.

![프런트 엔드 워크플로우 다이어그램](/help/assets/front-end-flow.png)

그러나 결과로 발생하는 모든 프로젝트는 이러한 개발 노력(즉, 백엔드 및 프런트 엔드 모두)의 출력을 모두 사용해야 합니다.

`npm run dev`을(를) 실행하면 ui.frontend 모듈에 저장된 JavaScript 및 CSS 파일을 수집하는 프런트 엔드 빌드 프로세스가 시작되고 `clientlib-site` 및 `clientlib-dependencies`라는 두 개의 미니화된 클라이언트 라이브러리 또는 ClientLibs를 생성하여 ui.apps 모듈에 저장합니다. ClientLibs는 AEM에 배포할 수 있으며 이를 통해 클라이언트측 코드를 저장소에 저장할 수 있습니다.

전체 AEM 프로젝트 원형이 `mvn clean install -PautoInstallPackage`을 사용하여 실행되면 ClientLibs를 비롯한 모든 프로젝트 아티팩트가 AEM 인스턴스로 푸시됩니다.

>[!TIP]
>
>AEM이 [AEM 개발 설명서](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html)에서 ClientLibs를 처리하는 방법, [include them](/help/developing/including-clientlibs.md) 또는 ui.frontend 모듈에서 ui를 사용하는 방법에 대해 자세히 알아보십시오.](#clientlib-generation)[

## ClientLibs 개요 {#clientlibs}

프런트 엔드 모듈은 [AEM ClientLib](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html)를 사용하여 사용할 수 있습니다. NPM 빌드 스크립트를 실행할 때 앱이 빌드되고 aem-clientlib-generator 패키지가 결과 빌드 출력을 가져와서 이러한 ClientLib로 변환합니다.

ClientLib는 다음 파일 및 디렉터리로 구성됩니다.

* `css/`:HTML에서 요청할 수 있는 CSS 파일
* `css.txt`:병합할 수 있도록 파일의 순서와  `css/` 이름을 AEM에 알려줍니다.
* `js/`:HTML에서 요청할 수 있는 JavaScript 파일
* `js.txt` 병합할 수 있도록 파일의 순서와  `js/` 이름을 AEM에 알려줍니다.
* `resources/`:소스 맵, 비시작 지점 코드 청크(코드 분할에 의해 발생됨), 정적 자산(예: 아이콘) 등

## 가능한 프런트 엔드 개발 워크플로 {#possible-workflows}

프런트 엔드 빌드 모듈은 유용하고 매우 유연한 도구이지만 사용 방법에 대해서는 특별한 의견을 내놓지 않습니다. 다음은 *가능한* 사용량의 두 가지 예입니다. 그러나 개별 프로젝트에 다른 사용 모델이 필요할 수 있습니다.

### Webpack 정적 개발 서버 사용 {#using-webpack}

Webpack을 사용하면 ui.frontend 모듈 내의 AEM 웹 페이지의 정적 출력을 기반으로 스타일을 지정하고 개발할 수 있습니다.

1. 페이지 미리 보기 모드를 사용하거나 URL에서 `wcmmode=disabled`으로 전달하여 AEM에서 페이지 미리 보기
1. 페이지 소스를 보고 ui.frontend 모듈 내에서 정적 HTML로 저장
1. [웹 ](#webpack-dev-server) 패키징을 시작하고 필요한 JavaScript 및 CSS를 생성하고 스타일링을 시작합니다.
1. `npm run dev`을(를) 실행하여 ClientLibs를 생성합니다.

이 과정에서 AEM 개발자는 1단계와 2단계를 수행하고 정적인 HTML을 AEM HTML 출력을 기반으로 개발하는 프런트 엔드 개발자에게 전달할 수 있습니다.

>[!TIP]
>
>또한 페이지 수준이 아닌 구성 요소 수준에서 작업할 수 있도록 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library)를 사용하여 각 구성 요소의 마크업 출력 샘플을 캡처할 수도 있습니다.

### 스토리북 사용 {#using-storybook}

[스토리북](https://storybook.js.org)을 사용하여 원자적 프런트 엔드 개발을 더 수행할 수 있습니다. Storybook은 AEM Project Tranype에 포함되지 않지만 ui.frontend 모듈 내에 Storybook 객체를 설치하고 저장할 수 있습니다. AEM 내에서 테스트할 준비가 되면 `npm run dev`을(를) 실행하여 ClientLibs로 배포할 수 있습니다.

>[!NOTE]
>
>[스토리북](https://storybook.js.org) 은 AEM 프로젝트 원형에 포함되지 않습니다. 사용하려는 경우 별도로 설치해야 합니다.

### 마크업 {#determining-markup} 결정

프로젝트를 위해 구현하려는 프런트 엔드 개발 워크플로우에서 백엔드 개발자와 프런트 엔드 개발자는 마크업에 먼저 동의해야 합니다. 일반적으로 AEM은 마크업을 정의하며, 이 마크업은 핵심 구성 요소에서 제공합니다. [하지만 필요한 경우 이 값을 사용자 지정할 수 있습니다](/help/developing/customizing.md#customizing-the-markup).

## ui.frontend 모듈 {#ui-frontend-module}

AEM Project Tranype에는 다음 기능이 포함된 Webpack을 기반으로 하는 선택적 전용 프런트 엔드 빌드 메커니즘이 포함되어 있습니다.

* 전체 TypeScript, ES6 및 ES5 지원(해당 웹 팩 래퍼 포함)
* TSLint 규칙 세트를 사용한 TypeScript 및 JavaScript 린팅
* 기존 브라우저 지원을 위한 ES5 출력
* Globbing
   * 어디에서나 가져오기 추가 필요 없음
   * 이제 모든 JS 및 CSS 파일을 각 구성 요소에 추가할 수 있습니다.
      * 우수 사례는 `/clientlib/js`, `/clientlib/css` 또는 `/clientlib/scss` 아래에 있습니다.
   * 모든 것이 웹 팩을 통해 실행되므로 `.content.xml` 또는 `js.txt`/`css.txt` 파일이 필요하지 않습니다.
   * 이 글로버는 `/component/` 폴더 아래의 모든 JS 파일을 가져옵니다.
      * Webpack을 사용하면 CSS/SCSS 파일을 JS 파일을 통해 체인으로 연결할 수 있습니다.
      * 두 시작 지점인 `sites.js` 및 `vendors.js`을 통해 가져옵니다.
   * AEM에서 사용하는 유일한 파일은 `/clientlib-site`의 출력 파일 `site.js` 및 `site.css`, `dependencies.js` 및 `/clientlib-dependencies`의 `dependencies.css`입니다.
* 청크
   * 기본(사이트 js/css)
   * 공급업체(종속성 js/css)
* 전체 Sass/Scss 지원(Sass는 Webpack을 통해 CSS로 컴파일됨)
* AEM의 로컬 인스턴스에 내장된 프록시가 포함된 정적 웹 팩 개발 서버

>[!NOTE]
>
>ui.frontend 모듈에 대한 자세한 기술 정보는 GitHub](https://github.com/adobe/aem-project-archetype/blob/master/src/main/archetype/ui.frontend.general/README.md)에 대한 [설명서를 참조하십시오.

## 설치 {#installation}

1. 전역적으로 [NodeJS](https://nodejs.org/en/download/)(v10+)를 설치합니다. npm도 설치됩니다.
1. 프로젝트에서 ui.frontend로 이동하고 `npm install`을(를) 실행합니다.

>[!NOTE]
>
>ui.frontend 폴더를 채우려면 `-DoptionIncludeFrontendModule=y` 옵션과 함께 [의 원형 유형](overview.md)을 실행해야 합니다.

## 사용량 {#usage}

다음 npm 스크립트는 프런트 엔드 작업 흐름을 주도합니다.

* `npm run dev` - JS 최적화를 사용하지 않도록 설정(트리 흔들기 등) 및 소스 맵 활성화 및 CSS 최적화를 비활성화하여 전체 빌드를 구성할 수 있습니다.
* `npm run prod` - JS 최적화가 활성화된 상태에서 전체 빌드(트리 흔들기 등), 소스 맵 비활성화 및 CSS 최적화가 활성화된 경우
* `npm run start` - AEM에 대한 의존성을 최소화하면서 로컬 개발을 위한 정적 웹 팩 개발 서버를 시작합니다.

## 출력 {#output}

ui.frontend 모듈은 `ui.frontend/src` 폴더 아래의 코드를 컴파일하고 컴파일된 CSS 및 JS와 `ui.frontend/dist` 폴더 아래의 모든 리소스를 출력합니다.

* **사이트** -  `site.js` `site.css` 및 레이아웃 종속 이미지 및  `resources/` 글꼴을 위한 폴더가 clientlib- `dist/`site 폴더에 생성됩니다.
* **종속성**   `dependencies.js` - 폴더 `dependencies.css` 에  `dist/clientlib-dependencies` 만들어집니다.

### JavaScript {#javascript}

* 최적화 - 프로덕션 빌드의 경우 사용 중이거나 호출되지 않는 모든 JS가 제거됩니다.

### CSS {#css}

* 자동 수정 - 모든 CSS는 사전 수정을 통해 실행되며 접두사가 필요한 모든 속성은 자동으로 CSS에 추가됩니다.
* 최적화 - 이후 모든 CSS는 다음과 같은 기본 규칙에 따라 표준화하는 최적기(csnano)를 통해 실행됩니다.
   * 가능하면 CSS 계산 표현식을 줄여 브라우저 호환성 및 압축을 보장합니다.
동일한 길이, 시간 및 각도 값 간을 변환합니다. 기본적으로 길이 값은 변환되지 않습니다.
   * 규칙 내 및 주변 댓글, 선택기 및 선언 제거
   * 중복된 규칙, at-rules 및 선언을 제거합니다.
      * 이 기능은 정확히 중복된 부분에만 작동합니다.
   * 출력에 영향을 주지 않으므로 빈 선택기가 있는 빈 규칙, 미디어 쿼리 및 규칙을 제거합니다.
   * 선택기와 겹쳐진 속성/값 쌍을 사용하여 인접한 규칙을 병합합니다.
   * CSS 파일에 단일 @charset만 있고 문서 맨 위로 이동하도록 합니다.
   * 결과 출력이 작으면 CSS 초기 키워드를 실제 값으로 바꿉니다.
   * SVGO를 사용하여 인라인 SVG 정의 압축
* 정리 - 생성된 CSS, JS 및 Map 파일을 On-Demand로 정리하기 위한 명시적 정리 작업을 포함합니다.
* 소스 매핑 - 개발 빌드만

>[!NOTE]
>
>프런트 엔드 빌드 옵션은 일반 구성 파일을 공유하는 개발 전용 및 제품 전용 웹 팩 구성 파일을 사용합니다. 이렇게 하면 개발 및 제작 설정을 개별적으로 수정할 수 있습니다.

### 클라이언트 라이브러리 생성 {#clientlib-generation}

ui.frontend 모듈 빌드 프로세스는 [aem-clientlib-generator](https://www.npmjs.com/package/aem-clientlib-generator) 플러그인을 사용하여 컴파일된 CSS, JS 및 모든 리소스를 ui.apps 모듈로 이동합니다. aem-clientlib-generator 구성이 `clientlib.config.js`에 정의되어 있습니다. 다음 클라이언트 라이브러리가 생성됩니다.

* **clientlib-site** -  `ui.apps/src/main/content/jcr_root/apps/<app>/clientlibs/clientlib-site`
* **clientlib-dependencies** -  `ui.apps/src/main/content/jcr_root/apps/<app>/clientlibs/clientlib-dependencies`

### {#clientlib-inclusion} 페이지에 클라이언트 라이브러리 포함

`clientlib-site` 및  `clientlib-dependencies` 카테고리는 기본 템플릿의 일부로  [페이지 정책 ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/components-templates/templates.html#template-definitions) 구성을 통해 페이지에 포함됩니다. 정책을 보려면 **컨텐트 페이지 템플릿 > 페이지 정보 > 페이지 정책**&#x200B;을 편집합니다.

사이트 페이지에 클라이언트 라이브러리를 최종 포함시키는 작업은 다음과 같습니다.

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

위의 포함은 페이지 정책을 업데이트하고 해당 클라이언트 라이브러리의 카테고리와 포함 속성을 수정하여 수정할 수도 있습니다.

### 정적 웹 팩 개발 서버 {#webpack-dev-server}

ui.frontend 모듈에 포함된 이 모듈은 AEM 외부의 신속한 프런트 엔드 개발을 위해 라이브 리로딩을 제공하는 webpack-dev-server입니다. 이 설정은 html-webpack-plugin을 활용하여 ui.frontend 모듈에서 컴파일된 CSS 및 JS를 정적 HTML 템플릿으로 자동 주입합니다.

#### 중요 파일 {#important-files}

* `ui.frontend/webpack.dev.js`
   * 여기에는 webpack-dev-serve에 대한 구성이 포함되어 있으며 사용할 html 템플릿을 가리킵니다.
   * 또한 localhost:4502에서 실행되는 AEM 인스턴스에 대한 프록시 구성이 포함되어 있습니다.
* `ui.frontend/src/main/webpack/static/index.html`
   * 서버가 실행할 정적 HTML입니다.
   * 이를 통해 개발자는 CSS/JS를 변경하고 마크업에 즉시 반영되는 내용을 볼 수 있습니다.
   * 이 파일에 배치된 마크업은 AEM 구성 요소에서 생성된 마크업을 정확하게 반영한다고 가정합니다.
   * 이 파일의 마크업은 AEM 구성 요소 마크업과 자동으로 동기화되지 않습니다.
   * 또한 이 파일에는 핵심 구성 요소 CSS 및 응답형 격자 CSS와 같이 AEM에 저장된 클라이언트 라이브러리에 대한 참조가 포함되어 있습니다.
   * 웹 팩 개발 서버는 `ui.frontend/webpack.dev.js`에 있는 구성을 기반으로, 로컬 실행 AEM 인스턴스에서 이러한 CSS/JS를 포함하는 프록시로 설정됩니다.

#### 사용 {#using-webpack-server}

1. 프로젝트의 루트 내에서 `mvn -PautoInstallSinglePackage clean install` 명령을 실행하여 전체 프로젝트를 `localhost:4502`에서 실행되는 AEM 인스턴스에 설치합니다.
1. `ui.frontend` 폴더 안으로 이동합니다.
1. 다음 명령 `npm run start`을 실행하여 웹팩 개발 서버를 시작합니다. 시작한 후에는 브라우저(`localhost:8080` 또는 사용 가능한 다음 포트)를 열어야 합니다.

이제 CSS, JS, SCSS 및 TS 파일을 수정할 수 있으며 웹 팩 개발 서버에 즉시 반영된 변경 사항을 확인할 수 있습니다.

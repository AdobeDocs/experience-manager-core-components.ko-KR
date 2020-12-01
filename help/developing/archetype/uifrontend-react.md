---
title: 반응형 SPA을 위한 프런트 엔드 빌드
description: 반응형 기반의 SPA 프로젝트를 위한 프런트 엔드 구축 프로세스에 대한 설명
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---


# 반응형 SPA {#frontend-react}에 대한 프런트 엔드 빌드

이 문서에서는 원형 유형을 사용하여 React 프레임워크에 따라 단일 페이지 애플리케이션(SPA)을 만들 때 생성된 프로젝트의 세부 사항에 대해 설명합니다. 즉, `frontendModule` 옵션을 `react`로 설정하면

## 개요 {#overview}

이 프로젝트는 [create-react-app](https://github.com/facebook/create-react-app)과(와) 부트스트래드가 설정되었습니다.

이 응용 프로그램은 사이트의 AEM 모델을 사용하도록 빌드되었습니다. 이 구성 요소는 [@adobe/cq-response-editable-components](https://www.npmjs.com/package/@adobe/cq-react-editable-components) 패키지의 헬퍼 구성 요소를 사용하여 레이아웃을 자동으로 생성합니다.

## 스크립트 {#scripts}

프로젝트 디렉토리에서 다음 명령을 실행할 수 있습니다.

### npm 시작 {#npm-start}

```
npm start
```

이 명령은 http://localhost:4502에서 실행되는 로컬 AEM 인스턴스에서 JSON 모델을 프록싱하여 개발 모드에서 앱을 실행합니다. 따라서 프로젝트 루트에서 최소 한 번(프로젝트 루트의 `mvn clean install -PautoInstallPackage`)에 전체 프로젝트가 AEM에 배포되었다고 가정합니다.

[ui.frontend](uifrontend.md) 디렉터리에서 `npm start`을(를) 실행하면 앱이 브라우저에서 자동으로 열립니다(경로 `http://localhost:3000/content/<appId>/<country>/<language>/home.html`). 편집을 하면 페이지가 다시 로드됩니다.

CORS와 관련된 오류가 발생하는 경우 다음과 같이 AEM을 구성할 수 있습니다.

1. 구성 관리자(http://localhost:4502/system/console/configMgr)으로 이동합니다.
1. &quot;Adobe Granite Cross-Origin Resource Sharing Policy&quot;의 구성을 엽니다.
1. 다음과 같은 추가 값을 사용하여 새 구성을 만듭니다.
   * 허용된 출처:http://localhost:3000
   * 지원되는 헤더:인증
   * 허용되는 메서드:OPTIONS

### npm 테스트 {#npm-test}

```
npm test
```

이 명령은 대화형 감시 모드에서 테스트 러너를 시작합니다. 자세한 내용은 테스트 실행](https://facebook.github.io/create-react-app/docs/running-tests)에 대한 [반응형 설명서를 참조하십시오.

### npm 실행 빌드 {#npm-run-build}

```
npm run build
```

이 명령은 제작 앱을 빌드 폴더에 빌드합니다. 프로덕션 모드에서 반응하고 최상의 성능을 위해 빌드를 최적화합니다. 자세한 내용은 [배포](https://facebook.github.io/create-react-app/docs/deployment)에 대한 반응형 설명서를 참조하십시오.

또한 AEM ClientLib는 [aem-clientlib-generator](https://github.com/wcm-io-frontend/aem-clientlib-generator) 패키지를 사용하여 앱에서 생성됩니다.

## 브라우저 지원 {#browser-support}

기본적으로 이 프로젝트는 대상 브라우저를 식별하는 [Browserslist](https://github.com/browserslist/browserslist)의 기본값 옵션을 사용합니다. 또한 이전 브라우저(예: Internet Explorer 11)를 지원하기 위한 최신 언어 기능을 위한 다각형이 포함되어 있습니다. 이러한 브라우저를 지원하지 않는 경우 다채우기 종속성 및 가져오기를 제거할 수 있습니다.

## 코드 분할 {#code-splitting}

React 앱은 기본적으로 [코드 분할](https://webpack.js.org/guides/code-splitting)을 사용하도록 구성되어 있습니다. 프로덕션용 앱을 빌드할 때 코드는 다음과 같이 여러 청크로 출력됩니다.

```
$ ls build/static/js
2.5b77f553.chunk.js
2.5b77f553.chunk.js.map
main.cff1a559.chunk.js
main.cff1a559.chunk.js.map
runtime~main.a8a9905a.js
runtime~main.a8a9905a.js.map
```

청크가 필요한 경우에만 청크를 로드하면 앱 성능이 크게 향상될 수 있습니다.

이 기능이 AEM에서 작동하려면 앱이 AEM에서 생성된 HTML에서 요청해야 하는 JS 및 CSS 파일을 식별할 수 있어야 합니다. 이것은 asset-manifest.json 파일의 &quot;entrypoints&quot; 키를 사용하여 구현할 수 있습니다. 이 파일은 clientlib.config.js에서 구문 분석되며 entrypoint 파일만 ClientLib에 번들로 포함됩니다. 나머지 파일은 ClientLib의 리소스 디렉토리에 배치되며 동적으로 요청되므로 실제로 필요할 때만 로드됩니다.

프로젝트 원형에서 AEM ClientLibs를 사용하는 방법에 대한 자세한 내용은 일반 [ui.frontend 모듈 설명서](uifrontend.md#clientlibs)를 참조하십시오.

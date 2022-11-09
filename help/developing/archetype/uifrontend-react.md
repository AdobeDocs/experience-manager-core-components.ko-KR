---
title: React SPA의 프론트엔드 빌드
description: React 기반 SPA 프로젝트의 프론트엔드 빌드 프로세스에 대한 설명
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: dd8ef13a-9686-47a9-b6af-e486ff10c4d8
source-git-commit: 0eea0cd65063c739e5b405b0380b73962a858e48
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 99%

---

# React SPA의 프론트엔드 빌드 {#frontend-react}

이 문서에서는 Archetype을 통해 React 프레임워크 기반의 단일 페이지 애플리케이션(SPA)을 생성하는 과정에서 제작된 프로젝트의 세부 사항에 대해 설명합니다. 예: `frontendModule` 옵션을 `react`으로 설정하는 경우.

## 개요 {#overview}

이 프로젝트는 [create-react-app](https://github.com/facebook/create-react-app)을 통해 Bootstrap으로 제작되었습니다.

이 애플리케이션은 사이트의 AEM 모델을 사용하도록 제작되었습니다. [@adobe/cq-react-editable-components](https://www.npmjs.com/package/@adobe/aem-react-editable-components)의 Helper 구성 요소를 사용하여 레이아웃을 자동으로 생성합니다.

## 스크립트 {#scripts}

프로젝트 디렉터리에서 다음 명령을 실행할 수 있습니다.

### npm 시작 {#npm-start}

```shell
npm start
```

이 명령은 http://localhost:4502에서 실행 중인 로컬 AEM 인스턴스의 JSON 모델을 프록싱하면서 개발 모드에서 앱을 실행합니다. 전체 프로젝트가 AEM에 최소 한 번이라도 배포되었다고 가정됩니다(프로젝트 루트의 `mvn clean install -PautoInstallPackage`).

[ui.frontend](uifrontend.md) 디렉터리에서 `npm start` 시작을 실행하면 브라우저에서 앱이 자동으로 열립니다(경로 `http://localhost:3000/content/<appId>/<country>/<language>/home.html`). 편집하는 경우 페이지가 다시 로드됩니다.

CORS 관련 오류가 발생하면 다음과 같이 AEM을 구성할 수 있습니다.

1. 구성 매니저로 이동합니다(http://localhost:4502/system/console/configMgr).
1. “Adobe Granite 원본 간 리소스 공유 정책“에 대한 구성을 엽니다.
1. 다음 추가 값을 사용하여 새 구성을 만듭니다.
   * 허용된 원본: http://localhost:3000
   * 머리글 지원: 승인
   * 허용된 방법: 옵션

### npm 테스트 {#npm-test}

```shell
npm test
```

이 명령은 대화형 관찰 모드에서 테스트 실행기를 실행합니다. 자세한 내용은 [테스트 실행에 대한 React 설명서](https://facebook.github.io/create-react-app/docs/running-tests)를 참조하십시오.

### npm 실행 빌드 {#npm-run-build}

```shell
npm run build
```

이 명령은 빌드 폴더에 제작용 앱을 빌드합니다. 제작 모드에서 React를 번들로 제공하고 최고의 성능을 제공하기 위해 빌드를 최적화합니다. 자세한 내용은 [배포에 대한 React 설명서](https://facebook.github.io/create-react-app/docs/deployment)를 참조하십시오.

또한, [aem-clientlib-generator](https://github.com/wcm-io-frontend/aem-clientlib-generator) 패키지를 통해 앱에서 AEM ClientLib을 생성합니다.

## 브라우저 지원 {#browser-support}

기본적으로 이 프로젝트는 [브라우저 목록](https://github.com/browserslist/browserslist)의 기본 옵션을 사용하여 대상 브라우저를 식별합니다. 또한, 기존 브라우저(예: Internet Explorer 11)를 지원하는 최신 언어 기능의 폴리필이 포함됩니다. 해당 브라우저 지원이 요구 사항이 아닌 경우 폴리필 종속성과 가져오기를 제거할 수 있습니다.

## 코드 분할 {#code-splitting}

React 앱을 구성하여 [코드 분할](https://webpack.js.org/guides/code-splitting)을 기본 사용합니다. 앱을 제작용으로 빌드하는 경우 코드를 몇 가지 청크로 출력합니다.

```shell
$ ls build/static/js
2.5b77f553.chunk.js
2.5b77f553.chunk.js.map
main.cff1a559.chunk.js
main.cff1a559.chunk.js.map
runtime~main.a8a9905a.js
runtime~main.a8a9905a.js.map
```

청크가 필요한 경우에만 로드하면 앱 성능이 크게 개선될 수 있습니다.

이 기능이 AEM에서 작동하는 경우 앱은 AEM에서 생성한 HTML로부터 요청한 JS 및 CSS 파일을 식별할 수 있습니다. asset-manifest.json 파일의 “진입점“ 키를 사용하여 이를 수행할 수 있습니다. 파일은 clientlib.config.js에서 구문 분석되면 진입점만 ClientLib으로 번들됩니다. 나머지 파일을 ClientLib의 리소스 디렉터리에 배치하면 자동 요청될 수 있으므로 실제 필요한 경우에만 로드할 수 있습니다.

Project Archetype에서 AEM ClientLib을 사용하는 방법에 대한 자세한 내용은 일반 [ui.frontend 모듈 설명서](uifrontend.md#clientlibs)를 참조하십시오.

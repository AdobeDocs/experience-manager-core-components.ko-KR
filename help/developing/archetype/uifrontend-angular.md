---
title: Angular SPA를 위한 프런트 엔드 빌드
description: Angular-based SPA 프로젝트를 위한 프런트 엔드 구축 프로세스에 대한 설명
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Angular SPA를 위한 프런트 엔드 빌드 {#frontend-angular}

이 문서에서는 Angular 프레임워크를 기반으로 하는 단일 페이지 애플리케이션(SPA)을 만들 때 생성된 프로젝트의 세부 사항에 대해 설명합니다. 예를 들어 `frontendModule` 옵션을 로 설정할 `angular`때

## 개요 {#overview}

이 프로젝트는 Angular CLI와 함께 [부트스트되었습니다](https://github.com/angular/angular-cli).

이 애플리케이션은 사이트의 AEM 모델을 사용하도록 빌드되었습니다. 이 구성 요소는 [@adobe/cq-angular-editable-components](https://www.npmjs.com/package/@adobe/cq-angular-editable-components) 패키지의 도우미 구성 요소를 사용하여 레이아웃을 자동으로 생성합니다.

## 스크립트 {#scripts}

프로젝트 디렉토리에서 다음 명령을 실행할 수 있습니다.

### npm 시작 {#npm-start}

```
npm start
```

이 명령은 http://localhost:4502에서 실행 중인 로컬 AEM 인스턴스에서 JSON 모델을 프록시하여 개발 모드에서 앱을 실행합니다. 이 경우 프로젝트 루트에서 전체 프로젝트가 최소 한 번(`mvn clean install -PautoInstallPackage` AEM에 배포)이 되었다고 가정합니다.

ui.frontend 디렉토리에서 npm 시작을 실행하면 앱이 브라우저에서 자동으로 열립니다(http://localhost:4200/content/${appId}/${country}/${language}/home.html). 편집을 하면 페이지가 다시 로드됩니다.

CORS와 관련된 오류가 발생하는 경우 다음과 같이 AEM을 구성할 수 있습니다.

1. 구성 관리자(http://localhost:4502/system/console/configMgr)로 이동합니다.
1. &quot;Adobe Granite Cross-Origin Resource Sharing Policy&quot;의 구성을 엽니다.
1. 다음과 같은 추가 값을 사용하여 새 구성을 만듭니다.
   * 허용된 출처:http://localhost:4200
   * 지원되는 헤더:인증
   * 허용되는 방법:옵션

### npm 테스트 {#npm-test}

```
npm test
```

이 명령은 Karma test 주자를 시작합니다. 자세한 [내용은 테스트](https://angular.io/guide/testing) 실행에 대한 Angular 설명서를 참조하십시오.

### npm run test:debug {#npm-run-test-debug}

```
npm run test:debug
```

이 명령은 대화형 감시 모드에서 Karma test 러너를 시작합니다.

### npm 실행 빌드 {#npm-run-build}

```
npm run build
```

이 명령은 제작 응용 프로그램을 빌드 폴더에 빌드합니다. 프로덕션 모드에서 각진 번들로 번들하고 최상의 성능을 위해 빌드를 최적화합니다. 자세한 [내용은 배포에](https://angular.io/guide/deployment) 대한 각 설명서를 참조하십시오.

또한 AEM ClientLib는 [aem-clientlib-generator](https://github.com/wcm-io-frontend/aem-clientlib-generator) 패키지를 사용하여 앱에서 생성됩니다.

프로젝트 원형에서 AEM ClientLibs를 사용하는 방법에 대한 자세한 내용은 일반 [ui.frontend 모듈 설명서를](uifrontend.md#clientlibs) 참조하십시오.

## 브라우저 지원 {#browser-support}

기본적으로 이 프로젝트는 Browserslist [의](https://github.com/browserslist/browserslist)기본값 옵션을 사용하여 대상 브라우저를 식별합니다. 또한 이전 브라우저(예: Internet Explorer 11)를 지원하기 위한 최신 언어 기능을 위한 다각형이 포함되어 있습니다. 이러한 브라우저를 지원하지 않는 경우 polyfill 종속성 및 가져오기를 제거할 수 있습니다.

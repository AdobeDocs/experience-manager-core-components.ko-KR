---
title: Angular SPA의 프론트엔드 빌드
description: Angular 기반 SPA 프로젝트의 프론트엔드 빌드 프로세스에 대한 설명
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 5726e29d-081c-42bb-bf4e-2852043b21d6
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: ht
source-wordcount: '404'
ht-degree: 100%

---

# Angular SPA의 프론트엔드 빌드 {#frontend-angular}

이 문서에서는 Archetype을 통해 Angular 프레임워크 기반의 단일 페이지 애플리케이션(SPA)을 생성하는 과정에서 제작된 프로젝트의 세부 사항에 대해 설명합니다. 예: `frontendModule` 옵션을 `angular`으로 설정하는 경우.

## 개요 {#overview}

이 프로젝트는 [Angular CLI](https://github.com/angular/angular-cli)를 통해 Bootstrap으로 제작되었습니다.

이 애플리케이션은 사이트의 AEM 모델을 사용하도록 제작되었습니다. [@adobe/cq-angular-editable-components](https://www.npmjs.com/package/@adobe/cq-angular-editable-components)의 Helper 구성 요소를 사용하여 레이아웃을 자동으로 생성합니다.

## 스크립트 {#scripts}

프로젝트 디렉터리에서 다음 명령을 실행할 수 있습니다.

### npm 시작 {#npm-start}

```
npm start
```

이 명령은 http://localhost:4502에서 실행 중인 로컬 AEM 인스턴스의 JSON 모델을 프록싱하면서 개발 모드에서 앱을 실행합니다. 전체 프로젝트가 AEM에 최소 한 번이라도 배포되었다고 가정됩니다(프로젝트 루트의 `mvn clean install -PautoInstallPackage`).

ui.frontend 디렉터리에서 npm 시작을 실행하면 브라우저에서 앱이 자동으로 열립니다(경로 http://localhost:4200/content/${appId}/${country}/${language}/home.html). 편집하는 경우 페이지가 다시 로드됩니다.

CORS 관련 오류가 발생하면 다음과 같이 AEM을 구성할 수 있습니다.

1. 구성 매니저로 이동합니다(http://localhost:4502/system/console/configMgr).
1. “Adobe Granite 원본 간 리소스 공유 정책“에 대한 구성을 엽니다.
1. 다음 추가 값을 사용하여 새 구성을 만듭니다.
   * 허용된 원본: http://localhost:4200
   * 머리글 지원: 승인
   * 허용된 방법: 옵션

### npm 테스트 {#npm-test}

```shell
npm test
```

이 명령은 Karma 테스트 실행기를 실행합니다. 자세한 내용은 [테스트 실행에 대한 Angular 설명서](https://angular.io/guide/testing)를 참조하십시오.

### npm 실행 테스트: 디버그 {#npm-run-test-debug}

```shell
npm run test:debug
```

이 명령은 대화형 관찰 모드에서 Karma 테스트 실행기를 실행합니다.

### npm 실행 빌드 {#npm-run-build}

```shell
npm run build
```

이 명령은 빌드 폴더에 제작용 앱을 빌드합니다. 제작 모드에서 Angular를 번들로 제공하고 최고의 성능을 제공하기 위해 빌드를 최적화합니다. 자세한 내용은 [배포에 대한 Angular 설명서](https://angular.io/guide/deployment)를 참조하십시오.

또한, [aem-clientlib-generator](https://github.com/wcm-io-frontend/aem-clientlib-generator) 패키지를 통해 앱에서 AEM ClientLib을 생성합니다.

Project Archetype에서 AEM ClientLib을 사용하는 방법에 대한 자세한 내용은 일반 [ui.frontend 모듈 설명서](uifrontend.md#clientlibs)를 참조하십시오.

## 브라우저 지원 {#browser-support}

기본적으로 이 프로젝트는 [브라우저 목록](https://github.com/browserslist/browserslist)의 기본 옵션을 사용하여 대상 브라우저를 식별합니다. 또한, 기존 브라우저(예: Internet Explorer 11)를 지원하는 최신 언어 기능의 폴리필이 포함됩니다. 해당 브라우저 지원이 요구 사항이 아닌 경우 폴리필 종속성과 가져오기를 제거할 수 있습니다.

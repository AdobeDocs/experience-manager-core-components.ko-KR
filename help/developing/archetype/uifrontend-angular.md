---
title: angular SPA용 프런트 엔드 빌드
description: angular 기반의 SPA 프로젝트를 위한 프런트 엔드 구축 프로세스에 대한 설명
feature: 핵심 구성 요소, AEM 프로젝트 원형
role: 건축가, 개발자, 관리자
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---


# angular SPA용 프런트 엔드 빌드 {#frontend-angular}

이 문서에서는 Angular 프레임워크을 기반으로 단일 페이지 애플리케이션(SPA)을 만들 때 생성된 프로젝트의 세부 사항을 설명합니다. 즉, `frontendModule` 옵션을 `angular`로 설정한 경우입니다.

## 개요 {#overview}

이 프로젝트는 [Angular CLI](https://github.com/angular/angular-cli)로 부트스트랩되었습니다.

이 응용 프로그램은 사이트의 AEM 모델을 사용하도록 빌드되었습니다. 이 구성 요소는 [@adobe/cq-angular-editable-components](https://www.npmjs.com/package/@adobe/cq-angular-editable-components) 패키지의 헬퍼 구성 요소를 사용하여 레이아웃을 자동으로 생성합니다.

## 스크립트 {#scripts}

프로젝트 디렉토리에서 다음 명령을 실행할 수 있습니다.

### npm 시작 {#npm-start}

```
npm start
```

이 명령은 http://localhost:4502에서 실행되는 로컬 AEM 인스턴스에서 JSON 모델을 프록싱하여 개발 모드에서 앱을 실행합니다. 여기서는 전체 프로젝트가 적어도 한 번(프로젝트 루트의 `mvn clean install -PautoInstallPackage`)에 배포되었다고 가정합니다.

ui.frontend 디렉토리에서 npm을 실행한 후 앱이 브라우저에서 자동으로 열립니다(http://localhost:4200/content/${appId}/${country}/${language}/home.html). 편집하는 경우 페이지가 다시 로드됩니다.

CORS와 관련된 오류가 발생하는 경우 다음과 같이 AEM을 구성할 수 있습니다.

1. 구성 관리자(http://localhost:4502/system/console/configMgr)으로 이동합니다.
1. &quot;Adobe Granite Cross-Origin Resource Sharing Policy&quot;의 구성을 엽니다.
1. 다음 추가 값을 사용하여 새 구성을 만듭니다.
   * 허용된 원본:http://localhost:4200
   * 지원되는 머리글:인증
   * 허용되는 메서드:OPTIONS

### npm 테스트 {#npm-test}

```shell
npm test
```

이 명령은 카르마 테스트 주자를 실행합니다. 자세한 내용은 테스트 실행](https://angular.io/guide/testing)에 대한 [Angular 설명서를 참조하십시오.

### npm 실행 테스트:debug {#npm-run-test-debug}

```shell
npm run test:debug
```

이 명령은 대화형 감시 모드에서 카르마 테스트 주자를 시작합니다.

### npm 실행 빌드 {#npm-run-build}

```shell
npm run build
```

이 명령은 제작 앱을 빌드 폴더에 빌드합니다. 프로덕션 모드에서 Angular을 번들로 처리하고 최상의 성능을 위해 빌드를 최적화합니다. 자세한 내용은 배포](https://angular.io/guide/deployment)에 대한 [Angular 설명서를 참조하십시오.

또한 AEM ClientLib는 [aem-clientlib-generator](https://github.com/wcm-io-frontend/aem-clientlib-generator) 패키지를 사용하여 앱에서 생성됩니다.

프로젝트 원형에서 AEM ClientLibs를 사용하는 방법에 대한 자세한 내용은 일반 [ui.frontend 모듈 설명서](uifrontend.md#clientlibs) 를 참조하십시오.

## 브라우저 지원 {#browser-support}

기본적으로 이 프로젝트는 대상 브라우저를 식별하기 위해 [Browserslist](https://github.com/browserslist/browserslist) 기본값 옵션을 사용합니다. 또한 이전 브라우저(예: Internet Explorer 11)를 지원하기 위해 최신 언어 기능을 위한 다각형이 포함되어 있습니다. 이러한 브라우저를 지원할 필요가 없는 경우 다채우기 종속성 및 가져오기를 제거할 수 있습니다.

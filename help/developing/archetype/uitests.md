---
title: ui.tests AEM 프로젝트 원형형의 모듈
description: AEM 프로젝트 전형 JUnit 테스트를 사용하는 방법
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# ui.tests AEM 프로젝트 원형형의 모듈 {#uitests-module}

프로젝트에 포함된 세 가지 수준의 테스트가 있습니다.

## 단위 테스트 {#unit-tests}

코어 모듈의 [](core.md) 유닛 테스트는 번들에 포함된 코드의 클래식 단위 테스트를 보여줍니다. 테스트하려면 다음을 실행합니다.

```
mvn clean test
```

## 통합 테스트 {#integration-tests}

서버측 통합 테스트를 사용하면 AEM 환경에서 단위 관련 테스트를 실행할 수 있습니다(예: AEM 서버에서). 테스트하려면 다음을 실행합니다.

```
mvn clean verify -PintegrationTests
```

## 클라이언트측 테스트 {#client-side-tests}

이 `client-side Hobbes.js` 테스트는 브라우저 측 동작을 확인하는 JavaScript 기반 브라우저 측 테스트입니다.

테스트하려면 브라우저에서 테스트할 AEM 페이지를 볼 때 왼쪽 패널을 열어 **개발자 모드에서** 페이지를 열고 테스트 **탭으로** 전환하여 생성된 **MyName 테스트를** 찾아실행합니다.

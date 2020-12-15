---
title: ui.AEM 프로젝트 원형 모듈의 테스트
description: AEM 프로젝트 원형 테스트 사용 방법
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---


# ui.테스트 AEM 프로젝트 원형의 모듈 {#uitests-module}

프로젝트에 포함된 3가지 테스트 수준은 다음과 같습니다.

## 단위 테스트 {#unit-tests}

[핵심 모듈](core.md)의 단위 테스트는 번들에 포함된 코드의 클래식 단위 테스트를 보여줍니다. 테스트하려면 다음을 실행합니다.

```
mvn clean test
```

## 통합 테스트 {#integration-tests}

서버측 통합 테스트를 통해 AEM 환경에서 단위 유사한 테스트를 실행할 수 있습니다(예: AEM 서버). 테스트하려면 다음을 실행합니다.

```
mvn clean verify -PintegrationTests
```

## 클라이언트측 테스트 {#client-side-tests}

`client-side Hobbes.js` 테스트는 브라우저 측 동작을 확인하는 JavaScript 기반 브라우저 측 테스트입니다.

테스트하려면 브라우저에서 테스트할 AEM 페이지를 볼 때 왼쪽 패널을 열어 **테스트** 탭으로 전환하여 **개발자 모드**&#x200B;에서 페이지를 열고 생성된 **MyName 테스트**&#x200B;를 찾아 실행합니다.

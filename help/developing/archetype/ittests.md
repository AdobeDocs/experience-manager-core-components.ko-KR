---
title: it.AEM 프로젝트 원형의 테스트 모듈
description: AEM 프로젝트 원형 통합 테스트를 사용하는 방법
translation-type: tm+mt
source-git-commit: 9d737b31efc8c346775ea5296f7599295af07cf1
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 0%

---


# it.tests Module of the AEM Project Tranype {#ittests-module}

프로젝트에 포함된 3가지 테스트 수준은 다음과 같습니다.

* [단위 테스트](core.md#unit-tests)
* 통합 테스트
* [UI 테스트](uitests.md)

이 문서에서는 it.tests 모듈의 일부로 사용할 수 있는 통합 테스트에 대해 설명합니다.

## 통합 테스트 실행 {#running-tests}

서버측 통합 테스트를 통해 AEM 환경에서 단위 유사한 테스트를 실행할 수 있습니다(예: AEM 서버). 테스트하려면 다음을 실행합니다.

```
mvn clean verify -PintegrationTests
```

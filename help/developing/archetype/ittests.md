---
title: AEM Project Archetype의 it.tests 모듈
description: AEM Project Archetype 통합 테스트를 사용하는 방법
feature: 핵심 구성 요소, AEM 프로젝트 원형
role: Architect, Developer, Administrator
exl-id: 0abc0265-3a3f-4323-97e6-3af0c62299ef
source-git-commit: 8ff36ca143af9496f988b1ca65475497181def1d
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# AEM Project Archetype {#ittests-module}의 it.tests 모듈입니다.

프로젝트에 포함된 세 가지 수준의 테스트가 있습니다.

* [단위 테스트](core.md#unit-tests)
* 통합 테스트
* [UI 테스트](uitests.md)

이 문서에서는 it.tests 모듈의 일부로 사용할 수 있는 통합 테스트를 설명합니다.

## 통합 테스트 실행 {#running-tests}

서버측 통합 테스트를 사용하면 장치 유사한 테스트를 AEM 환경, 즉 AEM 서버에서 실행할 수 있습니다. 테스트하려면 다음을 실행합니다.

```
mvn clean verify -PintegrationTests
```

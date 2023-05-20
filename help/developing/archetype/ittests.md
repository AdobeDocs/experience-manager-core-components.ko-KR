---
title: AEM Project Archetype의 it.tests 모듈
description: AEM Project Archetype 통합 테스트 사용법
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 0abc0265-3a3f-4323-97e6-3af0c62299ef
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 100%

---

# AEM Project Archetype의 it.tests 모듈 {#ittests-module}

세 가지 수준의 테스트가 프로젝트에 포함되어 있습니다.

* [단위 테스트](core.md#unit-tests)
* 통합 테스트
* [UI 테스트](uitests.md)

이 문서에서는 it.tests 모듈의 일부로 사용 가능한 통합 테스트에 대해 설명합니다.

## 통합 테스트 실행 {#running-tests}

서버측 통합 테스트를 통해 AEM 환경(AEM 서버)에서 유사 단위 테스트를 실행할 수 있습니다. 테스트를 하려면 다음을 실행합니다.

```
mvn clean verify -PintegrationTests
```

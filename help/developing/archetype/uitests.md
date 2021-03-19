---
title: ui.AEM 프로젝트 원형 모듈의 테스트
description: AEM 프로젝트 원형 UI 테스트를 사용하는 방법
feature: 핵심 구성 요소, AEM 프로젝트 원형
role: 건축가, 개발자, 관리자
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---


# ui.테스트 AEM 프로젝트 원형의 모듈 {#uitests-module}

프로젝트에 포함된 3가지 테스트 수준은 다음과 같습니다.

* [단위 테스트](core.md#unit-tests)
* [통합 테스트](ittests.md)
* UI 테스트

이 문서에서는 ui.tests 모듈의 일부로 사용할 수 있는 UI 테스트에 대해 설명합니다.

## UI 테스트 실행 {#running-tests}

테스트하려면 다음을 실행합니다.

```shell
mvn verify -Pui-tests-local-execution
```

실행 후에는 `target/reports` 폴더에서 보고서 및 로그를 사용할 수 있습니다.

## 추가 옵션 {#additional-options}

UI 테스트는 로컬 브라우저에 대한 헤드리스 테스트를 비롯하여 Docker 이미지로 실행할 수 있는 등 여러 옵션을 사용하여 실행할 수 있습니다. 자세한 내용은 ui.tests 모듈](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/ui.tests)의 [README.md 파일을 참조하십시오.

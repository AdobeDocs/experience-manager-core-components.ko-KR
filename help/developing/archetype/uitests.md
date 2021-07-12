---
title: AEM Project Archetype의 ui.tests 모듈
description: AEM Project Archetype UI 테스트를 사용하는 방법
feature: 핵심 구성 요소, AEM 프로젝트 원형
role: Architect, Developer, Admin
exl-id: eb3c9b34-f10e-410f-bcf3-34f94f124c7c
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---

# AEM Project Archetype의 ui.tests 모듈 {#uitests-module}

프로젝트에 포함된 세 가지 수준의 테스트가 있습니다.

* [단위 테스트](core.md#unit-tests)
* [통합 테스트](ittests.md)
* UI 테스트

이 문서에서는 ui.tests 모듈의 일부로 사용할 수 있는 UI 테스트를 설명합니다.

## UI 테스트 실행 {#running-tests}

테스트하려면 다음을 실행합니다.

```shell
mvn verify -Pui-tests-local-execution
```

실행 후에는 `target/reports` 폴더에서 보고서 및 로그를 사용할 수 있습니다.

## 추가 옵션 {#additional-options}

UI 테스트는 로컬 브라우저에 대한 헤드리스 테스트 및 Docker 이미지처럼 여러 가지 옵션을 사용하여 실행할 수 있습니다. 자세한 내용은 ui.tests 모듈](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/ui.tests)의 [README.md 파일을 참조하십시오.

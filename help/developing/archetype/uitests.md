---
title: AEM Project Archetype의 ui.tests 모듈
description: AEM Project Archetype UI 테스트 사용법
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: eb3c9b34-f10e-410f-bcf3-34f94f124c7c
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: ht
source-wordcount: '112'
ht-degree: 100%

---

# AEM Project Archetype의 ui.tests 모듈 {#uitests-module}

세 가지 수준의 테스트가 프로젝트에 포함되어 있습니다.

* [단위 테스트](core.md#unit-tests)
* [통합 테스트](ittests.md)
* UI 테스트

이 문서에서는 ui.tests 모듈의 일부로 사용 가능한 UI 테스트에 대해 설명합니다.

## UI 테스트 실행 {#running-tests}

테스트를 하려면 다음을 실행합니다.

```shell
mvn verify -Pui-tests-local-execution
```

실행 후 `target/reports` 폴더에서 보고서와 로그를 사용할 수 있습니다.

## 추가적인 옵션 {#additional-options}

로컬 브라우저에 대한 헤드리스 테스트를 포함하여 다양한 여러 옵션과 도커 이미지로 UI 테스트를 실행할 수 있습니다. 자세한 내용은 [ui.test의 README.md 파일](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/ui.tests)을 참조하십시오.

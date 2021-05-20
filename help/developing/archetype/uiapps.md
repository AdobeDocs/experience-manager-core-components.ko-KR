---
title: AEM Project Archetype의 ui.apps 모듈
description: AEM Project Archetype의 ui.apps 모듈
feature: 핵심 구성 요소, AEM 프로젝트 원형
role: Architect, Developer, Administrator
exl-id: fc63a19a-3253-44ee-96e2-bb5544c2235b
source-git-commit: 8ff36ca143af9496f988b1ca65475497181def1d
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 0%

---

# AEM 프로젝트 원형 {#uiapps-module}의 ui.apps 모듈

ui.apps maven 모듈(`<src-directory>/<project>/ui.apps`)에는 `/apps` 아래의 사이트에 필요한 모든 렌더링 코드가 포함되어 있습니다. 여기에는 [clientlibs라는 AEM 형식으로 저장될 CSS/JS가 포함됩니다.](uifrontend.md#clientlibs) 여기에는 동적 HTML 렌더링을 위한 HTL 스크립트도 포함됩니다. ui.apps 모듈을 JCR의 구조에 대한 맵으로 생각할 수 있지만 파일 시스템에 저장하고 소스 제어에 커밋할 수 있는 형식으로 생각할 수 있습니다.

Apache Jackrabbit FileVault 패키지 플러그인은 ui.apps 모듈의 컨텐츠를 AEM에 배포할 수 있는 AEM 패키지로 컴파일하는 데 사용됩니다. 플러그인의 전역 구성은 상위 pom.xml에 정의됩니다.

## 상위 POM {#parent-pom}

[상위 POM](/help/developing/archetype/using.md#parent-pom) (`<src>/<project>/pom.xml`)에는  `<plugin>` 프로젝트에 사용되는 플러그인에 대한 다양한 구성을 정의하는 섹션이 포함되어 있습니다. 여기에는 Jackrabbit FileVault 패키지 플러그인에 대한 `filterSource`에 대한 구성이 포함됩니다. `filterSource` 은 패키지에 포함된 jcr 경로를 정의하는 데 사용되는 `filter.xml` 파일의 위치를 가리킵니다.

Jackrabbit FileVault 패키지 플러그인 외에 패키지를 AEM에 푸시하는 데 사용되는 컨텐츠 패키지 플러그인의 정의입니다. `aem.host`, `aem.port`, `vault.user` 및 `vault.password`에 대한 변수가 동일한 상위 POM에 정의된 전역 속성에 해당하는 변수가 사용됩니다.

## ui.apps/pom.xml {#uiapps-pom}

ui.apps pom(`<src>/<project>/ui.apps/pom.xml`)은 `filevault-package-maven-plugin`에 대한 `embedded` 태그를 제공합니다. `embedded` 태그에는 ui.apps 패키지의 일부로 컴파일된 코어 번들과 해당 번들이 설치될 위치가 포함됩니다.

core.wcm.components.all 및 core.wcm.components.example 패키지가 하위 패키지로 포함되어 있습니다. 이렇게 하면 매번 WKND 코드와 함께 코어 구성 요소 패키지가 배포됩니다.

core.wcm.components.all 및 core.wcm.components.example은 종속성 목록에 종속성으로 포함됩니다. 그러나 가장 좋은 방법으로서, 종속성 버전은 여기에서 생략되고 [상위 pom 파일](/help/developing/archetype/using.md#core-components)에서 관리됩니다.

## filter.xml {#filter}

ui.apps 모듈용 `filter.xml` 파일은 `<src>/<project>/ui.apps/src/main/content/META-INF/vault/filter.xml`에 있으며 ui.apps 패키지와 함께 포함 및 설치되는 경로가 포함되어 있습니다.

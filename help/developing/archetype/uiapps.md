---
title: ui.AEM 프로젝트 원형 모듈의
description: ui.AEM 프로젝트 원형 모듈의
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Administrator
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 0%

---


# ui.apps 모듈 AEM 프로젝트 원형 {#uiapps-module}

ui.apps maven 모듈(`<src-directory>/<project>/ui.apps`)에는 `/apps` 아래 사이트에 필요한 모든 렌더링 코드가 포함되어 있습니다. 여기에는 [clientlibs라는 AEM 형식으로 저장되는 CSS/JS가 포함됩니다.](uifrontend.md#clientlibs) 동적 HTML 렌더링을 위한 HTML 스크립트도 포함되어 있습니다. ui.apps 모듈을 JCR의 구조에 대한 맵으로 생각할 수 있지만 파일 시스템에 저장되고 소스 제어에 커밋할 수 있는 형식으로 생각하면 됩니다.

Apache Jackrabbit FileVault 패키지 플러그인은 ui.apps 모듈의 컨텐츠를 AEM에 배포할 수 있는 AEM 패키지로 컴파일하는 데 사용됩니다. 플러그인의 전역 구성은 상위 pom.xml에 정의됩니다.

## 상위 POM {#parent-pom}

[상위 POM](/help/developing/archetype/using.md#parent-pom) (`<src>/<project>/pom.xml`)에는 프로젝트에 사용된 플러그인에 대한 다양한 구성을 정의하는  `<plugin>` 섹션이 포함되어 있습니다. 여기에는 Jackrabbit FileVault 패키지 플러그인에 대한 `filterSource`의 구성이 포함됩니다. `filterSource`은 패키지에 포함된 jcr 경로를 정의하는 데 사용되는 `filter.xml` 파일의 위치를 가리킵니다.

Jackrabbit FileVault Package Plugin 외에도 패키지를 AEM에 푸시하는 데 사용되는 Content Package Plugin의 정의입니다. `aem.host`, `aem.port`, `vault.user` 및 `vault.password`에 대한 변수는 동일한 상위 POM에 정의된 전역 속성에 해당하는 데 사용됩니다.

## ui.apps/pom.xml {#uiapps-pom}

ui.apps pom(`<src>/<project>/ui.apps/pom.xml`)은 `filevault-package-maven-plugin`에 대한 `embedded` 태그를 제공합니다. `embedded` 태그에는 ui.apps 패키지의 일부로 컴파일된 코어 번들과 해당 번들 구성 요소가 설치될 위치가 포함됩니다.

core.wcm.components.all 및 core.wcm.components.examples 패키지가 하위 패키지로 포함되어 있습니다. 이렇게 하면 매번 WKND 코드와 함께 핵심 구성 요소 패키지가 배포됩니다.

core.wcm.components.all 및 core.wcm.components.examples는 종속성 목록에 종속성으로 포함됩니다. 그러나 종속성 버전은 여기에서 생략되고 [상위 양식 파일](/help/developing/archetype/using.md#core-components)에서 관리됩니다.

## filter.xml {#filter}

ui.apps 모듈의 `filter.xml` 파일은 `<src>/<project>/ui.apps/src/main/content/META-INF/vault/filter.xml`에 있으며 ui.apps 패키지에 포함되어 설치할 경로를 포함합니다.

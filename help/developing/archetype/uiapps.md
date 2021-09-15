---
title: AEM Project Archetype의 ui.apps 모듈
description: AEM Project Archetype의 ui.apps 모듈
feature: 핵심 구성 요소, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: fc63a19a-3253-44ee-96e2-bb5544c2235b
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: ht
source-wordcount: '340'
ht-degree: 100%

---

# AEM Project Archetype의 ui.apps 모듈 {#uiapps-module}

ui.apps Maven 모듈(`<src-directory>/<project>/ui.apps`)에는 `/apps` 아래 사이트에 필요한 모든 렌더링 코드가 포함됩니다. [clientlib이라는 AEM 포맷으로 저장되는 CSS/JS가 여기에 포함됩니다.](uifrontend.md#clientlibs) 동적 HTML 렌더링에 HTL 스크립트가 포함됩니다. ui.apps 모듈은 JCR의 구조에 대한 맵으로 간주될 수 있지만 파일 시스템에 저장되고 소스 제어 전용인 포맷으로 간주될 수도 있습니다.

Apache Jackrabbit FileVault 패키지 플러그인을 통해 ui.apps 모듈 콘텐츠를 AEM에 배포할 수 있는 AEM 패키지로 컴파일합니다. 상위 pom.xml에서 플러그에 대한 전역 구성을 정의합니다.

## 상위 POM {#parent-pom}

[상위 POM](/help/developing/archetype/using.md#parent-pom)(`<src>/<project>/pom.xml`)에는 프로젝트에 사용되는 플러그에 대한 여러 구성을 정의하는 `<plugin>` 섹션이 포함됩니다. Jackrabbit FileVault 패키지 플러그의 `filterSource`에 대한 구성이 여기에 포함됩니다. `filterSource`는 패키지에 포함된 jcr 경로 정의에 사용되는 `filter.xml` 파일의 위치를 지정합니다.

Apache Jackrabbit FileVault 패키지 플러그 외에도 패키지를 AEM에 푸시하는 콘텐츠 패키지 플러그에 대한 정의가 있습니다. 동일한 상위 POM에 정의된 전역 속성에 해당되는 `aem.host`, `aem.port`, `vault.user` 및 `vault.password`에 대한 변형이 사용됩니다.

## ui.apps/pom.xml {#uiapps-pom}

ui.apps pom(`<src>/<project>/ui.apps/pom.xml`)은 `filevault-package-maven-plugin`에 `embedded` 태그를 제공합니다. `embedded` 태그에는 ui.apps 패키지로 컴파일된 핵심 번들과 설치 위치가 포함됩니다.

하위 패키지로 core.wcm.components.all과 core.wcm.components.examples 패키지가 포함됩니다. 매번 WKND 코드와 함께 핵심 구성 요소 패키지가 배포됩니다.

종속성 목록에서 종속성으로 core.wcm.components.all과 core.wcm.components.examples 패키지가 포함됩니다. 단, [상위 pom 파일](/help/developing/archetype/using.md#core-components)에서는 종속성에 대한 버전을 생략하고 관리하는 것이 좋습니다.

## filter.xml {#filter}

ui.apps 모듈에 대한 `filter.xml` 파일은 `<src>/<project>/ui.apps/src/main/content/META-INF/vault/filter.xml`에서 찾을 수 있고 해당 파일에는 ui.apps 패키지와 함께 포함 및 설치될 경로가 있습니다.

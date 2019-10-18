---
title: ui.apps AEM 프로젝트 원형형의 모듈
seo-title: ui.apps AEM 프로젝트 원형형의 모듈
description: ui.apps AEM 프로젝트 원형형의 모듈
seo-description: ui.apps AEM 프로젝트 원형형의 모듈
contentOwner: 보허트
content-type: 참조
topic-tags: 핵심 구성 요소
translation-type: tm+mt
source-git-commit: 683b4f4705c226275439a408423cbf1b23bea66f

---


# ui.apps AEM 프로젝트 원형형의 모듈 {#uiapps-module}

ui.apps maven 모듈(`<src-directory>/<project>/ui.apps`)에는 아래 사이트에 필요한 모든 렌더링 코드가 포함되어 `/apps`있습니다. 여기에는 clientlibs라는 AEM 형식으로 저장되는 CSS/JS가 포함됩니다. 동적 HTML 렌더링을 위한 HTL 스크립트도 포함되어 있습니다. ui.apps 모듈은 JCR의 구조에 대한 맵으로 생각할 수 있지만 파일 시스템에 저장되고 소스 제어에 커밋될 수 있는 형식으로 생각할 수 있습니다.

Apache Jackrabbit FileVault 패키지 플러그인은 ui.apps 모듈의 콘텐츠를 AEM에 배포할 수 있는 AEM 패키지로 컴파일하는 데 사용됩니다. 플러그인의 전역 구성은 상위 pom.xml에 정의됩니다.

## 상위 POM {#parent-pom}

[상위 POM](overview.md#parent-pom) (`<src>/<project>/pom.xml`)에는 프로젝트에 사용된 플러그인의 다양한 구성을 정의하는 `<plugin>` 섹션이 포함되어 있습니다. 여기에는 Jackrabbit FileVault 패키지 플러그인에 `filterSource` 대한 구성이 포함됩니다. 패키지에 포함된 jcr 경로를 정의하는 데 사용되는 `filterSource` `filter.xml` 파일의 위치를 가리킵니다.

Jackrabbit FileVault 패키지 플러그인 외에도 패키지를 AEM에 푸시하는 데 사용되는 컨텐츠 패키지 플러그인의 정의입니다. 동일한 상위 POM에 정의된 전역 속성에 해당하는 `aem.host`, `aem.port`, `vault.user`및 `vault.password` 에 대한 변수가 사용됩니다.

## ui.apps/pom.xml {#uiapps-pom}

ui.apps pom(`<src>/<project>/ui.apps/pom.xml`)은 에 대한 `embedded` 태그를 `filevault-package-maven-plugin`제공합니다. 이 `embedded` 태그에는 ui.apps 패키지의 일부로 컴파일된 코어 번들과 해당 번들 제품이 설치되는 위치가 포함됩니다.

core.wcm.components.all 및 core.wcm.components.examples 패키지가 하위 패키지로 포함되어 있습니다. 이렇게 하면 매번 WKND 코드와 함께 코어 구성 요소 패키지가 배포됩니다.

core.wcm.components.all 및 core.wcm.components.examples는 종속성 목록에 종속성으로 포함됩니다. 그러나 종속성 버전은 여기에서 생략되고 [상위 양식 파일에서](overview.md#core-components)관리됩니다.

## filter.xml {#filter}

ui.apps 모듈에 대한 `filter.xml` 파일은 에 `<src>/<project>/ui.apps/src/main/content/META-INF/vault/filter.xml` 있으며 ui.apps 패키지에 포함되어 설치될 경로를 포함합니다.

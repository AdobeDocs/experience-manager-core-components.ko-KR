---
title: ui.AEM 프로젝트 원형 모듈의
description: ui.AEM 프로젝트 원형 모듈의
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Administrator
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---


# ui.AEM 프로젝트 원형 모듈의 {#uicontent-module}

ui.content maven 모듈(`<src-directory>/<project>/ui.content`)에는 `/content` 및 `/conf` 아래에 있는 기준 컨텐츠 및 구성이 포함되어 있습니다. ui.content는 ui.apps와 같이 AEM 패키지로 컴파일됩니다. 주요 차이점은 ui.content에 저장된 노드를 AEM 인스턴스에서 직접 수정할 수 있다는 것입니다. 페이지, DAM 자산 및 편집 가능한 템플릿이 포함되어 있습니다. ui.content 모듈을 사용하여 깔끔한 인스턴스에 대한 샘플 컨텐츠를 저장하거나 소스 제어에서 관리할 일부 기준 구성을 만들 수 있습니다.

## filter.xml {#filter}

ui.content 모듈에 대한 `filter.xml` 파일은 `<src>/<project>/ui.content/src/main/content/META-INF/vault/filter.xml`에 있으며 ui.content 패키지에 포함되어 설치할 경로를 포함합니다. 경로에 `mode="merge"` 속성이 추가되었음을 확인합니다. 이렇게 하면 코드 배포로 배포된 구성이 AEM 인스턴스에서 직접 제작한 컨텐츠 또는 구성을 자동으로 재정의하지 않습니다.

## ui.content/pom.xml

ui.apps 모듈과 같은 ui.content 모듈은 FileVault 패키지 플러그인을 사용합니다. 그러나 ui.content 포럼(`<src>/<project>/ui.content/pom.xml`)에는 `acHandling`이라는 추가 구성 속성이 포함되며 `merge_preserve`로 설정됩니다. 이 구성 요소는 ui.content 모듈에 템플릿을 편집할 수 있는 사람을 결정하는 권한인 ACL(액세스 제어 목록)이 포함되어 있기 때문에 포함됩니다. 이러한 ACL을 AEM으로 가져오려면 `acHandling` 속성이 필요합니다.

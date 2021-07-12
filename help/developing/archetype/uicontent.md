---
title: AEM 프로젝트 원형 중 ui.content 모듈
description: AEM 프로젝트 원형 중 ui.content 모듈
feature: 핵심 구성 요소, AEM 프로젝트 원형
role: Architect, Developer, Admin
exl-id: af019cd8-c733-4b53-bb57-321dd9451178
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# AEM 프로젝트 원형 중 ui.content 모듈 {#uicontent-module}

ui.content maven 모듈(`<src-directory>/<project>/ui.content`)은 `/content` 및 `/conf` 아래에 있는 기본 컨텐츠 및 구성을 포함합니다. ui.content는 ui.apps와 마찬가지로 AEM 패키지에 컴파일됩니다. 주요 차이점은 ui.content에 저장된 노드를 AEM 인스턴스에서 직접 수정할 수 있다는 것입니다. 여기에는 페이지, DAM 자산 및 편집 가능한 템플릿이 포함됩니다. ui.content 모듈은 깨끗한 인스턴스에 대한 샘플 컨텐츠를 저장하거나 소스 제어에서 관리할 일부 기준 구성을 만드는 데 사용할 수 있습니다.

## filter.xml {#filter}

ui.content 모듈용 `filter.xml` 파일은 `<src>/<project>/ui.content/src/main/content/META-INF/vault/filter.xml`에 있으며 ui.content 패키지와 함께 포함 및 설치되는 경로를 포함합니다. `mode="merge"` 속성이 경로에 추가되었음을 확인합니다. 따라서 코드 배포와 함께 배포된 구성이 AEM 인스턴스에서 직접 작성된 컨텐츠 또는 구성을 자동으로 재정의하지 않습니다.

## ui.content/pom.xml

ui.apps 모듈과 같은 ui.content 모듈은 FileVault 패키지 플러그인을 사용합니다. 그러나 ui.content pom(`<src>/<project>/ui.content/pom.xml`)에는 `acHandling`, `merge_preserve`로 설정된 추가 구성 속성이 포함되어 있습니다. 이 구성 요소는 ui.content 모듈에 템플릿을 편집할 수 있는 사용자를 결정하는 사용 권한인 ACL(액세스 제어 목록)이 포함되어 있기 때문입니다. 이러한 ACL을 AEM으로 가져오려면 `acHandling` 속성이 필요합니다.

---
title: AEM Project Archetype의 ui.content 모듈
description: AEM Project Archetype의 ui.content 모듈
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: af019cd8-c733-4b53-bb57-321dd9451178
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 100%

---

# AEM Project Archetype의 ui.content 모듈 {#uicontent-module}

ui.content maven 모듈(`<src-directory>/<project>/ui.content`)에는 `/content`와 `/conf`아래의 기준 콘텐츠 및 구성이 포함됩니다. ui.content는 ui.apps과 동일하게 AEM 패키지로 컴파일됩니다. ui.content에 저장된 노드를 AEM 인스턴스에서 바로 수정할 수 있다는 것이 중요한 차이점입니다. 페이지, DAM 에셋 및 편집 가능한 템플릿이 여기에 포함됩니다. ui.content 모듈을 사용하여 클린 인스턴스의 샘플 콘텐츠를 저장하거나 소스 제어 기능에서 관리하는 기준 구성을 생성할 수 있습니다.

## filter.xml {#filter}

ui.content 모듈에 대한 `filter.xml` 파일은 `<src>/<project>/ui.content/src/main/content/META-INF/vault/filter.xml`에서 찾을 수 있고 해당 파일에는 ui.content 패키지와 함께 포함 및 설치될 경로가 있습니다. `mode="merge"` 속성이 경로에 추가됩니다. 이로써 코드 배포로 구성이 배포되면 AEM 인스턴스에 바로 작성된 콘텐츠나 구성을 자동으로 오버라이드합니다.

## ui.content/pom.xml

ui.apps 모듈과 같이 ui.content 모듈은 FileVault 패키지 플러그인을 사용합니다. 하지만 ui.content pom(`<src>/<project>/ui.content/pom.xml`)에는 `merge_preserve`로 설정된 `acHandling`라는 구성 속성이 추가로 포함됩니다. 속성이 포함되는 이유는 ui.content 모듈에 템플릿을 누가 편집할 것인지 결정하는 권한인 액세스 제어 목록(ACL)이 있기 때문입니다. 이 ACL을 AEM으로 가져오려면 `acHandling` 속성이 필수입니다.

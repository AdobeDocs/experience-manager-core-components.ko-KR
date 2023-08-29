---
title: 핵심 구성 요소를 통해 성공으로 가는 경로
description: 프로젝트를 구현할 때 핵심 구성 요소로 성공하는 방법은?
role: Architect, Developer, Admin, User
exl-id: 1ea8cd1c-8435-4ded-82dc-5a7896c53e0c
source-git-commit: b1d38310a3f05e2dd2a68de1574a278bac2c78e7
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 92%

---


# 핵심 구성 요소를 통해 성공으로 가는 경로 {#paths-to-success}

핵심 구성 요소는 강력하고 유연하며 사용 및 맞춤화가 매우 간편합니다. 이 문서에 명시된 몇 군데 주요 가이드라인에 따라 핵심 구성 요소를 사용하면 프로젝트를 성공적으로 완료할 수 있습니다.

## 성공으로 가는 두 가지 경로 {#two-paths}

기본적인 두 가지 방법으로 핵심 구성 요소를 구현할 수 있습니다. 이렇게 하면 성공적인 성과를 얻을 수 있지만 프로젝트별로 자체 절충안을 고려해야 합니다.

1. 핵심 구성 요소에 대한 디자인을 매핑하고 핵심 구성 요소에서 제공하는 HTML를 사용합니다. 또는
1. 이미 정의된 HTML 표준을 준수하는 경우 추가 역량이 필요하고 핵심 구성 요소의 모든 혜택을 다운로드할 수 없습니다.

## 구성 요소 구현 시 발생하는 공통된 문제 {#common-pitfalls}

핵심 구성 요소로 프로젝트가 실패한 경우 발생하는 공통된 문제는 다음과 같습니다.

* **디자인 완료** - 완료된 디자인이 C 레벨로 인정되어 개발 팀에 인도되면 무결점 기반 기술로 완벽하게 구현될 수 있습니다.
* **전사적인 HTML 스타일 가이드** - 구성 요소는 하향식 방식으로 스타일을 적용하면서 해당 스타일 가이드를 독단적으로 따르는 경우가 너무 많습니다.

두 사례에서 구성 요소에 적용되는 요구 사항이 너무 엄격하고 제한적이라는 이유로 핵심 구성 요소나 즉시 사용 가능한 구성 요소가 해당 요구 사항을 준수할 수 없기 때문에 대량의 맞춤형 구성 요소가 개발되었습니다.

## 조기 시작 {#start-early}

프로젝트의 구현 단계에서 핵심 구성 요소만 고려하지 않고 와이어프레이밍 및 디자인 단계에서 핵심 구성 요소를 조기 시작합니다.

### 구성 요소 라이브러리 사용 {#component-library}

이미 디자인 단계에서 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_kr)를 참조하십시오. 핵심 구성 요소는 강력하고 유연한 도구로서 시작점부터 여러분의 여정에 도움을 줄 수 있습니다. 핵심 구성 요소로 달성할 수 없는 실제 비즈니스 요구가 있다면 맞춤형 구성 요소를 추가하기만 하면 됩니다.

### Adobe XD용 UI 키트 사용 {#ui-kit}

맞춤형 구성 요소에 대한 필요성이 입증되면 즉시 Adobe XD용 UI 키트 활용 [여기서 다운로드할 수 있습니다.](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/AEM-CoreComponents-UI-Kit.xd) 따라서 디자이너는 핵심 구성 요소를 빌딩 블록으로 사용하여 와이어프레임 및 디자인 빌드를 시작할 수 있습니다.

## 강력한 기능에 주목하십시오. {#powerful-features}

AEM 및 핵심 구성 요소는 매우 강력하고 섬세한 기능을 갖추고 있습니다. 디자이너는 특정 기능에 대한 잠재성을 바로 파악할 수는 없습니다.

### 콘텐츠 조각 {#content-fragments}

변형(채널별로 가능)과 함께 [콘텐츠 조각](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/content-fragments.html)을 사용하여 채널 중립적인 콘텐츠를 만들 수 있습니다. 그런 다음 콘텐츠 페이지를 작성할 때 이러한 조각과 해당 변형을 사용할 수 있습니다.

업데이트된 JSON Exporter와 함께 구조화된 콘텐츠 조각을 사용하여 AEM 페이지 이외의 채널에 콘텐츠 서비스를 통해 AEM 콘텐츠를 제공할 수도 있습니다.

### 경험 조각 템플릿 {#experience-fragment-templates}

작성자가 페이지의 일부(경험 조각)를 재사용하려는 경우 경험 조각을 사용할 수 있습니다. [경험 조각](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/experience-fragments.html)이 없으면 작성자는 해당 조각을 복사하여 붙여넣어야 합니다. 이러한 복사/붙여넣기 경험을 생성하고 유지 관리하는 데는 시간이 오래 걸리고 사용자 오류가 발생합니다. 경험 조각은 복사/붙여넣기가 필요하지 않습니다.

### 임베디드 구성 요소 {#embed-component}

[임베디드 구성 요소](/help/components/embed.md)를 통해 YouTube 비디오 콘텐츠 등 외부 소스를 간단히 내포하고, 프로젝트에 맞는 콘텐츠를 수용하여 확장성을 높일 수 있습니다.

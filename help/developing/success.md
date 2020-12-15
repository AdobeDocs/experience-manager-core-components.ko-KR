---
title: 핵심 구성 요소를 사용한 성공 경로
description: 핵심 구성 요소로 프로젝트를 구현할 때 성공하는 방법
translation-type: tm+mt
source-git-commit: c338428a681f652d17bb972fb6a2abf216a338c3
workflow-type: tm+mt
source-wordcount: '570'
ht-degree: 14%

---


# 핵심 구성 요소 {#paths-to-success} 사용 성공 경로

핵심 구성 요소는 강력하고, 유연하며, 사용하기 쉽고, 사용자 정의할 수 있습니다. 이 문서에 설명된 몇 가지 주요 지침을 따르면 핵심 구성 요소가 있는 프로젝트가 성공했는지 확인합니다.

## 두 개의 성공 경로 {#two-paths}

핵심 구성 요소를 구현하는 두 가지 기본 접근 방식이 있습니다. 이 방법은 성공으로 이어질 수 있지만 프로젝트별로 고려해야 하는 자체 균등한 기준을 가지고 있습니다.

1. 디자인을 핵심 구성 요소에 매핑하고 디자인에서 제공하는 HTML을 가져옵니다. 또는
1. 이미 정의된 HTML 표준을 준수해야 하는 경우 핵심 구성 요소의 이점을 모두 활용하지는 않고 더 많은 노력이 필요합니다.

## 구성 요소 구현의 일반적인 함선 {#common-pitfalls}

핵심 구성 요소로 프로젝트가 성공하지 못할 수 있는 두 가지 일반적인 문제는 다음과 같습니다.

* **완료된 디자인**  - C 레벨 승인 시 기본 기술에 대한 걱정 없이 픽셀 하나까지 완벽하게 구현되도록 개발 팀에 전달할 수 있습니다.
* **회사 전체 HTML 스타일 가이드**  - 이러한 안내선을 너무 자주 따라하려면 위쪽 아래쪽 원근에서 스타일을 적용하는 구성 요소가 도그적으로 수행해야 합니다.

두 경우 모두 구성 요소에 대한 요구 사항이 매우 엄격하고 구체적이어서 핵심 구성 요소나 즉시 사용 가능한 구성 요소가 해당 구성 요소를 따르도록 하는 것이 어려우므로 사용자 지정 구성 요소를 대량으로 개발할 수 있습니다.

## 시작 날짜 {#start-early}

프로젝트의 구현 단계에서 핵심 구성 요소를 고려하기만 하는 것이 아니라 와이어프레임 및 디자인 단계 동안 이미 핵심 구성 요소로 시작합니다.

### 구성 요소 라이브러리 사용 {#component-library}

디자인 단계에서 이미 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library)를 참조합니다. 핵심 구성 요소는 강력하고 유연하므로 시작점으로 전환할 수 있습니다. 핵심 구성 요소로 실현할 수 없는 실제 비즈니스 요구 사항이 있는 경우에만 사용자 지정 구성 요소를 추가합니다.

### Adobe XD {#ui-kit}용 UI 키트 사용

사용자 지정 구성 요소에 대한 필요성이 증명되면 디자이너가 핵심 구성 요소로 와이어프레임과 디자인을 빌드할 수 있도록 Adobe XD](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/assets/overview/AEM_UI-kit_Wireframe.xd)용 [UI 키트를 활용하십시오.

## 강력한 기능 {#powerful-features} 간과하지 마십시오.

AEM 및 핵심 구성 요소의 기능은 매우 강력할 수 있지만 매우 미세하고 특정 기능에 대한 가능성은 디자이너에게는 즉시 나타나지 않을 수 있습니다.

### 콘텐츠 조각 {#content-fragments}

[컨텐츠 ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/content-fragments.html) 조각은 채널 중립적인 컨텐츠(채널별 관련)와 변형을 함께 만들 수 있도록 도와줍니다. 그런 다음 컨텐츠 페이지를 작성할 때 이러한 조각과 해당 변형을 사용할 수 있습니다.

업데이트된 JSON Exporter와 함께 구조화된 컨텐츠 조각을 사용하여 AEM 페이지 이외의 채널에 컨텐츠 서비스를 통해 AEM 컨텐츠를 제공할 수도 있습니다.

### 경험 조각 템플릿 {#experience-fragment-templates}

작성자가 페이지의 일부(경험 조각)를 재사용하려는 경우 경험 조각을 사용할 수 있습니다. [경험 조각 없이 작성자는 해당 조각을 복사하여 붙여넣어야 합니다. ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/experience-fragments.html) 이러한 복사/붙여넣기 경험을 생성하고 유지 관리하는 데는 시간이 오래 걸리고 사용자 오류가 발생합니다. 경험 조각은 복사/붙여넣기가 필요하지 않습니다.

### 포함 구성 요소 {#embed-component}

[포함 구성 ](/help/components/embed.md) 요소는 YouTube 비디오 컨텐츠와 같은 외부 리소스를 간단히 포함할 수 있을 뿐만 아니라 프로젝트의 요구 사항에 맞는 컨텐츠를 수용할 수 있도록 확장할 수 있습니다.
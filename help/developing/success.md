---
title: 핵심 구성 요소를 사용하여 성공으로 가는 경로
description: 핵심 구성 요소로 프로젝트를 구현할 때 성공하는 방법
role: Architect, Developer, Administrator, Business Practitioner
exl-id: 1ea8cd1c-8435-4ded-82dc-5a7896c53e0c
source-git-commit: 056c5bc15ac9e669c3bf6d5da7f060d6eef02608
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 14%

---

# 코어 구성 요소 {#paths-to-success}를 사용하여 성공에 이르는 경로

핵심 구성 요소는 강력하고 유연하며 사용이 편리하고 사용자 지정할 수 있습니다. 이 문서에 설명된 몇 가지 주요 지침을 따르면 핵심 구성 요소를 사용하는 프로젝트가 성공했는지 확인합니다.

## 두 개의 성공 경로 {#two-paths}

핵심 구성 요소를 구현하는 두 가지 기본 접근 방법이 있는데, 이 접근 방식은 성공으로 이어질 수 있지만 프로젝트별로 고려해야 하는 자체 단점을 갖습니다.

1. 디자인을 핵심 구성 요소에 매핑하고 제공된 HTML로 가져옵니다. 또는
1. 이미 정의된 HTML 표준을 준수해야 하는 경우 더 많은 노력이 필요하며 핵심 구성 요소의 이점을 모두 얻을 수는 없습니다.

## 구성 요소 구현의 공통 함정 {#common-pitfalls}

핵심 구성 요소로 프로젝트가 성공하지 못하는 일반적인 두 가지 문제는 다음과 같습니다.

* **최종 설계**  - C 레벨에서 승인될 수도 있으며, 기본 기술에 대한 걱정 없이 픽셀-퍼펙트를 구현하도록 개발 팀에 전달됩니다.
* **회사 전체의 HTML 스타일 가이드**  - 이러한 안내서는 하향식 관점에서 스타일을 적용하는 구성 요소를 통해 도그적으로 따라야 합니다.

두 경우 모두 핵심 구성 요소에 대한 요구 사항이 매우 엄격하고 구체적이므로 핵심 구성 요소나 바로 사용 가능한 구성 요소가 이러한 구성 요소를 준수하도록 하는 것이 매우 어렵습니다. 따라서 사용자 지정 구성 요소가 대량으로 개발됩니다.

## {#start-early} 일찍 시작

프로젝트의 구현 단계에서 핵심 구성 요소를 고려하지 않고, 와이어프레임 및 디자인 단계 동안 이미 핵심 구성 요소로 시작합니다.

### 구성 요소 라이브러리 {#component-library} 사용

디자인 단계에서 이미 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library)를 참조합니다. 핵심 구성 요소는 강력하고 유연하며 시작 지점으로 이동할 수 있습니다. 핵심 구성 요소로 합리적으로 달성할 수 없는 실제 비즈니스 요구가 있는 경우에만 사용자 지정 구성 요소를 추가합니다.

### Adobe XD용 UI 키트 {#ui-kit} 사용

사용자 지정 구성 요소가 필요한 것으로 증명되는 즉시 Adobe XD](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/AEM-CoreComponents-UI-Kit.xd)용 [UI 키트 를 활용하여 디자이너가 코어 구성 요소를 구성 요소로 사용하여 와이어프레임과 디자인을 작성할 수 있습니다.

## 강력한 기능 {#powerful-features} 을 간과하지 마십시오.

AEM 및 핵심 구성 요소의 기능은 매우 강력할 수 있지만, 특정 기능에 대한 가능성은 설계자에게 즉시 나타나지 않을 수 있습니다.

### 콘텐츠 조각 {#content-fragments}

[컨텐츠 ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/content-fragments.html) 조각은 (채널별 포함) 변형과 함께 채널 중립적인 컨텐츠를 만들 수 있습니다. 그런 다음 컨텐츠 페이지를 작성할 때 이러한 조각과 해당 변형을 사용할 수 있습니다.

업데이트된 JSON Exporter와 함께 구조화된 컨텐츠 조각을 사용하여 AEM 페이지 이외의 채널에 컨텐츠 서비스를 통해 AEM 컨텐츠를 제공할 수도 있습니다.

### 경험 조각 템플릿 {#experience-fragment-templates}

작성자가 페이지의 일부(경험 조각)를 재사용하려는 경우 경험 조각을 사용할 수 있습니다. [경험 조각이 없으면 작성자는 해당 조각을 복사하여 붙여넣어야 합니다. ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/experience-fragments.html) 이러한 복사/붙여넣기 경험을 생성하고 유지 관리하는 데는 시간이 오래 걸리고 사용자 오류가 발생합니다. 경험 조각은 복사/붙여넣기가 필요하지 않습니다.

### 포함 구성 요소 {#embed-component}

[포함 구성 ](/help/components/embed.md) 요소는 YouTube 비디오 컨텐츠와 같은 외부 리소스를 간단하게 포함할 수 있을 뿐만 아니라 프로젝트 요구 사항에 맞는 컨텐츠를 수용할 수 있도록 확장 가능합니다.

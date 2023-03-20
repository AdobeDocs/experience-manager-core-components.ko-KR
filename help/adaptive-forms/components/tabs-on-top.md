---
title: 응용 Forms 코어 구성 요소 - 맨 위의 탭
description: 상단 코어 구성 요소에서 응용 Forms 탭 사용 또는 사용자 지정
role: Architect, Developer, Admin, User
source-git-commit: d2a6108f17f6e0c6b91bec84893d64a8bd48effd
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 16%

---


# 상단 탭 {#tabs-on-top-adaptive-forms-core-component}

적응형 양식의 탭-상 레이아웃은 양식의 관련 필드 및 섹션을 별도의 탭으로 구성하고 그룹화하는 방법입니다. 각 탭은 일반적으로 양식 맨 위에 있는 탭 레이블로 표시되며 특정 양식 필드 및 섹션 세트를 포함합니다. 이 레이아웃을 사용하면 양식의 여러 섹션을 쉽게 탐색하고 액세스할 수 있으므로 사용자에게 더 친숙하고 부담을 덜 수 있습니다. 일반적으로 양식에서 많은 필드와 섹션이 포함되어 있을 때 사용되며 이 필드를 더 작고 관리하기 쉬운 청크로 나누어야 합니다. 또한 탭 을 사용하면 키보드 단축키를 사용하여 양식을 탐색할 수 있으므로 장애가 있는 사용자가 양식에 쉽게 액세스할 수 있으므로 접근성을 향상시킬 수 있습니다.

**예**

![](/help/adaptive-forms/assets/tabs.png)

## 사용 {#reasons-to-use-tab-on-the-top-layout}

적응형 양식의 맨 위 레이아웃에 있는 탭을 사용해야 하는 몇 가지 이유가 있습니다.

* **조직**: 탭을 사용하여 양식의 여러 섹션을 개별 범주로 구성할 수 있으므로 사용자가 필요한 정보를 쉽게 탐색하고 찾을 수 있습니다.

* **공간 보존**: 탭은 한 번에 양식의 한 섹션만 표시되도록 하여 페이지의 공간을 절약하는 데 도움이 될 수 있습니다.

* **향상된 사용자 경험**: 탭은 양식을 시각적으로 더 호소력 있고 쉽게 사용할 수 있도록 하여 사용자 경험을 향상시킬 수 있습니다.

* **모바일 친화적**: 탭 기능을 사용하면 스크롤을 줄이고 필드 간을 쉽게 전환할 수 있으므로 보다 모바일 친화적으로 양식을 만들 수 있습니다.

간단히 말해, 탭은 양식을 보다 체계적이고, 공간을 효율적으로 하며, 사용자에게 친숙하고, 액세스할 수 있도록 만들 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

적응형 Forms 아코디언 코어 구성 요소는 Cloud Service용 코어 구성 요소 2.0.4 및 AEM 6.5.16.0 Forms 용 코어 구성 요소 1.1.12의 일부로 2023년 2월에 출시되었습니다. 다음은 지원되는 모든 버전, AEM 호환성 및 해당 설명서 링크를 보여주는 표입니다.

| 구성 요소 버전 | AEM as a Cloud Service | AEM 6.5.16.0 Forms 이상 |
|---|---|---|
| v1 | 호환 가능 <br>[2.0.4](/help/adaptive-forms/version.md) 및 이후 릴리스 | 호환 가능<br>[릴리스 1.1.12](/help/adaptive-forms/version.md) 2.0.0보다 작음 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/adaptive-forms/version.md) 문서를 참조하십시오.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## 기술 세부 정보 {#technical-details}

적응형 양식 최상위 탭 핵심 구성 요소에 대한 최신 정보는 [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/tabsontop/v1/tabsontop)의 기술 설명서에서 확인할 수 있습니다. 핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 확인하십시오.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자에서 방문자의 최상위 경험 탭을 쉽게 사용자 지정할 수 있습니다. 또한 원활한 사용자 경험을 위해 상단 옵션에 탭을 쉽게 정의할 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

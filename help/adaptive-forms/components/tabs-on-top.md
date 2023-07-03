---
title: 적응형 양식 핵심 구성 요소 - 상단 탭
description: 적응형 양식 상단 탭 핵심 구성 요소를 사용 또는 사용자 정의합니다.
role: Architect, Developer, Admin, User
source-git-commit: 7888cfa0f1358ce8018fc1e3cc3b19eb66a82b9d
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 94%

---


# 상단 탭 {#tabs-on-top-adaptive-forms-core-component}

적응형 양식의 상단 탭 레이아웃은 양식의 관련 필드 및 섹션을 별도의 탭으로 구성하고 그룹화하는 방법입니다. 각 탭은 일반적으로 양식 상단에 있는 탭 레이블에 표시되고, 특정 양식 필드 및 섹션 집합을 포함합니다. 이 레이아웃을 통해 사용자는 쉽게 서로 다른 양식의 섹션을 탐색하고 액세스하여 양식을 보다 사용자 친화적이고 더 편리하게 사용할 수 있습니다. 일반적으로 필드와 섹션이 많은 양식에 사용되므로 양식을 더 작고 관리하기 쉬운 청크로 분리해야 합니다. 사용자가 키보드 단축키를 사용하여 양식을 탐색하는 경우 탭은 접근성을 개선하여 장애가 있는 사용자가 보다 쉽게 양식에 액세스할 수 있도록 해 줍니다.

**예**

![](/help/adaptive-forms/assets/tabs.png)

## 사용 {#reasons-to-use-tab-on-the-top-layout}

적응형 양식에서 상단 탭 레이아웃을 사용하는 데에는 다음과 같은 몇 가지 이유가 있습니다.

* **구성**: 탭을 통해 서로 다른 양식의 섹션을 별도의 범주로 구성하여 사용자가 원하는 정보를 쉽게 탐색하고 살펴볼 수 있습니다.

* **공간 절약**: 탭을 사용하여 한 번에 양식의 한 섹션만 표시하여 페이지 공간을 절약할 수 있습니다.

* **사용자 경험 개선**: 탭을 통해 양식을 시각적으로 더 매력적이고 사용하기 쉽게 만들어 사용자 경험을 개선할 수 있습니다.

* **모바일 친화적 양식**: 탭을 통해 스크롤 횟수를 줄이고 필드 간 전환을 쉽게 만들어 양식을 모바일 친화적으로 만듭니다.

즉, 탭을 사용하여 구성과 공간이 보다 효율적이고, 사용자 친화적인 접근성 높은 양식을 만들 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

적응형 양식 아코디언 핵심 구성 요소는 Cloud Service의 핵심 구성 요소 2.0.4 및 AEM 6.5.16.0 Forms 이상의 핵심 구성 요소 1.1.12 일부로 2023년 2월에 릴리스되었습니다. 다음 표에서는 지원되는 모든 버전, AEM 호환성 및 해당 문서에 대한 링크를 보여 줍니다.

| 구성 요소 버전 | AEM as a Cloud Service | AEM 6.5.16.0 Forms 이상 |
|---|---|---|
| v1 | 호환 가능 <br>[2.0.4](/help/adaptive-forms/version.md) 및 이후 릴리스 | <br>[릴리스 1.1.12](/help/adaptive-forms/version.md) 이상과 호환합니다(2.0.0 이전 버전). |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/adaptive-forms/version.md) 문서를 참조하십시오.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## 기술 세부 정보 {#technical-details}

적응형 양식 최상위 탭 핵심 구성 요소에 대한 최신 정보는 [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/tabsontop/v1/tabsontop)의 기술 설명서에서 확인할 수 있습니다. 핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 확인하십시오.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자를 사용하여 방문자를 위한 상단 탭 경험을 손쉽게 사용자 정의할 수 있습니다. 상단 탭 옵션을 간편하게 정의하여 원활한 사용자 경험을 제공할 수도 있습니다.

## 관련 문서 {#related-article}

* [AEM Sites 페이지 또는 경험 조각에서 적응형 양식 만들기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html)

* [독립 실행형 적응형 양식 만들기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

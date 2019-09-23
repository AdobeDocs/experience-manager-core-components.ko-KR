---
title: 탐색 구성 요소
seo-title: 탐색 구성 요소
description: 'null'
seo-description: 탐색 구성 요소를 사용하면 글로벌화된 사이트 구조를 쉽게 탐색할 수 있습니다.
uuid: 616c03fb-39b3-402a-b990-f56c87bc6df4
content-type: 참조
topic-tags: authoring
products: SG_EXPERIENCEMANAGER/CORCOMPONENTS-new
discoiquuid: da8d67d7-b65e-4041-bc0e-e998f24a68f9
disttype: dist5
gnavtheme: 밝음
groupsectionnavitems: 아니오
hidemerchandisingbar: 상속
hidepromocomponent: 상속
modalsize: 426x240
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c4e86960ec271464661193f6409cd93d1b9ec51b

---


# 탐색 구성 요소{#navigation-component}

탐색 구성 요소를 사용하면 글로벌화된 사이트 구조를 쉽게 탐색할 수 있습니다.

## 사용량 {#usage}

탐색 구성 요소에는 사이트 사용자가 사이트 구조를 쉽게 탐색할 수 있도록 페이지 트리가 나열됩니다.

탐색 구성 요소는 사이트의 글로벌라이제이션 사이트 구조를 자동으로 감지하고 현지화된 페이지에 [자동으로 적용할 수 있습니다.](#localized-site-strucutre) 또한 [그림자 리디렉션 페이지를](#shadow-structure) 사용하여 기본 컨텐츠 구조가 아닌 다른 구조를 표시하여 임의의 사이트 구조를 지원할 수 있습니다.

컨텐츠 작성자는 [편집 대화](#edit-dialog) 상자를 사용하여 탐색 심도와 함께 탐색 루트 페이지를 정의할 수 있습니다. 템플릿 작성자는 [디자인 대화 상자를](#design-dialog) 사용하여 탐색 루트 및 깊이의 기본값을 정의할 수 있습니다.

## 현지화된 사이트 구조 지원 {#localized-site-structure}

웹 사이트는 여러 지역에 대해 여러 언어로 제공되는 경우가 많습니다. 일반적으로 현지화된 각 페이지에는 페이지 템플릿의 일부로 포함된 탐색 요소가 포함됩니다. 탐색 구성 요소를 사용하면 사이트의 모든 페이지에 대한 템플릿에 한 번 배치할 수 있으며, 그러면 글로벌화된 사이트 구조를 기반으로 로컬라이즈된 개별 페이지에 대해 자동으로 적용됩니다.

* 탐색 구성 요소의 현지화 기능에 대한 예는 아래 [섹션을 참조하십시오](#example-localiatzion).
* 핵심 구성 요소의 현지화 기능이 함께 작동하는 방법에 대한 예는 핵심 구성 요소 [페이지의](localization.md)현지화 기능을 참조하십시오.

### 예 {#example-localization}

귀하의 컨텐츠는 다음과 같은 모습이라고 가정해 보겠습니다.

```
/content
+-- we-retail
   +-- language-masters
      +-- de
         \-- experience
            \-- arctic-surfing-in-lofoten
      +-- en
         \-- experience
            \-- arctic-surfing-in-lofoten
      +-- es
      +-- fr
      \-- it
   +-- us
      +-- en
         \-- experience
            \-- arctic-surfing-in-lofoten
      \-- es
   \-- ch
      +-- de
         \-- experience
            \-- arctic-surfing-in-lofoten
      +-- fr
      \-- it
+-- wknd-events
\-- wknd-shop
```

사이트 We.Retail의 경우 페이지 템플릿에 탐색 구성 요소를 머리글의 일부로 배치할 수 있습니다. 템플릿의 일부로 구성 요소의 탐색 **루트가** 해당 사이트에 대한 마스터 컨텐츠가 시작되는 `/content/we-retail/language-masters/en` 곳이기 때문에 구성 요소의 탐색 루트를 설정할 수 있습니다. 또한 구성 요소에서 전체 컨텐츠 **트리를** 표시하지 않고 처음 두 개 수준이 개요로 제공되도록 하기 `2` 때문에 탐색 구조 깊이를 설정할 수도 있습니다.

탐색 **루트** 값을 사용하면 탐색 구성 요소는 탐색 시작 후 `/content/we-retail/language-masters/en` 사이트의 구조를 두 수준 아래로 반복(탐색 구조 깊이 값으로 정의됨)하여 탐색 옵션을 생성할 수 **있음을** 알 수 있습니다.

사용자가 보고 있는 현지화된 페이지에 관계없이 탐색 구성 요소는 현재 페이지의 위치를 알고 루트로 역행하고 해당 페이지로 이동하여 해당 현지화된 페이지를 찾을 수 있습니다.

따라서 방문자가 보고 `/content/ch/de/experience/arctic-surfing-in-lofoten`있는 경우 구성 요소는 탐색 구조를 생성하도록 알고 `/content/we-retail/language-masters/de`있습니다. 마찬가지로 방문자가 보고 `/content/us/en/experience/arctic-surfing-in-lofoten`있는 경우 구성 요소는 탐색 구조를 생성하도록 알고 `/content/we-retail/language-masters/en`있습니다.

## 그림자 사이트 구조 지원 {#shadow-structure}

경우에 따라 실제 사이트 구조와 다른 방문자에 대한 탐색 메뉴를 만들어야 합니다. 판촉 행사에서는 컨텐츠 목록을 다시 정렬하여 메뉴의 특정 컨텐츠를 강조 표시해야 합니다. 다른 컨텐츠 페이지로 간단히 리디렉션되는 그림자 페이지를 사용하여 탐색 구성 요소는 필요한 임의 탐색 구조를 생성할 수 있습니다.

이를 위해서는 다음을 수행해야 합니다.

1. 원하는 사이트 구조를 나타내는 결합 페이지로 섀도 페이지를 만듭니다. 이를 종종 그림자 사이트 구조라고 합니다.
1. 이러한 **페이지의 페이지 속성에** 있는 리디렉션 값을 설정하여 실제 컨텐츠 페이지를 가리킵니다.
1. 그림자 **페이지의 페이지** 속성에서 탐색에 숨기기 옵션을 설정합니다.
1. 내비게이션 **구성** 요소의 탐색 루트 값을 새 그림자 사이트 구조의 루트를 가리키도록 설정합니다.

그러면 탐색 구성 요소가 그림자 사이트 구조에 따라 메뉴를 렌더링합니다. 구성 요소로 렌더링된 링크는 그림자 페이지 자체가 아니라 그림자 페이지가 리디렉션되는 실제 컨텐츠 페이지에 대한 링크입니다. 또한 구성 요소는 실제 페이지의 이름을 표시하고, 탐색을 섀도 페이지를 기반으로 하는 경우에도 활성 페이지를 올바르게 강조 표시합니다. 탐색 구성 요소는 그림자 페이지를 방문자에게 완전히 투명하게 만듭니다.

>[!NOTE]
>그림자 페이지를 사용하면 내비게이션 옵션을 보다 유연하게 사용할 수 있지만 이 구조의 기본 설정은 완전히 수동적입니다. 실제 사이트 컨텐츠를 다시 배열하거나 컨텐츠를 추가/제거하는 경우 필요에 따라 그림자 구조를 수동으로 업데이트해야 합니다.

>[!NOTE]
>그림자 사이트 구조를 렌더링할 때 탐색 논리로 인해 그림자 페이지만 반복됩니다. 로직은 리디렉션 대상의 구조를 반복하지 않습니다.

## 버전 및 호환성 {#version-and-compatibility}

탐색 구성 요소의 현재 버전은 v1이며, 이 버전은 2018년 1월 핵심 구성 요소 릴리스 2.0.0과 함께 도입되었으며 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소 버전이 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 핵심 구성 요소 [버전을 참조하십시오](versions.md).

## 샘플 구성 요소 출력 {#sample-component-output}

탐색 구성 요소뿐만 아니라 구성 옵션의 예와 HTML 및 JSON 출력을 보려면 구성 요소 [라이브러리를 참조하십시오](http://opensource.adobe.com/aem-core-wcm-components/library/navigation.html).

## 기술 정보 {#technical-details}

탐색 구성 요소에 대한 최신 기술 문서는 GitHub에서 [찾을 수 있습니다](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/navigation/v1/navigation).

핵심 구성 요소 개발에 대한 자세한 내용은 핵심 구성 요소 개발자 [설명서를](developing.md)참조하십시오.

>[!NOTE]
>
>핵심 구성 요소 릴리스 2.1.0부터 탐색 구성 요소는 [schema.org microdata](https://schema.org)를 지원합니다.

## Edit Dialog {#edit-dialog}

편집 대화 상자에서 컨텐츠 작성자는 탐색 루트 페이지와 탐색 구조의 심도를 정의할 수 있습니다.

### 속성 탭 {#properties-tab}

![](assets/screen-shot-2019-08-29-12.23.45.png)

* **탐색**&#x200B;루트탐색 트리를 생성하는 데 사용되는 루트 페이지입니다.
* **탐색 루트**&#x200B;제외 결과 트리에서 탐색 루트를 제외하고 하위 항목만 포함합니다.
* **모든 하위 페이지**&#x200B;수집탐색 루트의 하위 항목인 모든 페이지를 수집합니다.
* **탐색**&#x200B;구조 깊이탐색 루트에 대해 구성 요소가 표시해야 하는 탐색 트리 아래의 수준 수를 정의합니다(모든 하위 페이지 **** 수집을 선택하지 않은 경우에만 사용 가능).

### 액세스 가능성 탭 {#accessibility-tab}

![](assets/screen-shot-2019-08-29-12.23.53.png)

액세스 **가능성** 탭에서 구성 요소에 대한 ARIA 액세스 [가능](https://www.w3.org/WAI/standards-guidelines/aria/) 레이블에 대한 값을 설정할 수 있습니다.

* **레이블** - 구성 요소에 대한 ARIA 레이블 속성의 값

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 사용하여 컨텐츠 작성자에게 제공되는 탐색 루트 페이지 및 탐색 깊이의 기본값을 설정할 수 있습니다.

### 속성 탭 {#properties-tab-design}

![](assets/screen_shot_2018-04-03at112357.png)

* **탐색**&#x200B;루트탐색 구조의 루트 페이지의 기본값으로, 컨텐츠 작성자가 페이지에 구성 요소를 추가할 때 탐색 트리를 생성하고 기본값으로 설정됩니다.
* **탐색 루트**&#x200B;제외결과 트리에서 탐색 루트를 제외하는 옵션의 기본값입니다.
* **모든 하위 페이지**&#x200B;수집옵션 기본값은 탐색 루트의 하위 페이지인 모든 페이지를 수집합니다.
* **탐색**&#x200B;구조 깊이탐색 구조 깊이의 기본값.

### 스타일 탭 {#styles-tab}

탐색 구성 요소는 AEM 스타일 [시스템을 지원합니다](authoring.md#component-styling).

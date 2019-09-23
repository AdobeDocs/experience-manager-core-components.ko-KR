---
title: Language Navigation Component
seo-title: Language Navigation Component
description: 'null'
seo-description: 언어 탐색 구성 요소는 방문자가 다른 로케일에서 동일한 페이지로 이동할 수 있도록 사이트에 대한 언어/국가 탐색을 제공합니다.
uuid: ce736458-9cdf-4bc2-b90f-9c5a62fe1ca0
content-type: 참조
topic-tags: authoring
products: SG_EXPERIENCEMANAGER/CORCOMPONENTS-new
discoiquuid: 8f232eb0-65d5-4075-8668-75f136682c8
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


# Language Navigation Component{#language-navigation-component}

언어 탐색 구성 요소는 방문자가 다른 로케일에서 동일한 페이지로 이동할 수 있도록 사이트에 대한 언어/국가 탐색을 제공합니다.

## 사용량 {#usage}

웹 사이트는 여러 지역에 대해 여러 언어로 제공되는 경우가 많습니다. 언어 탐색 구성 요소를 사용하면 방문자가 동일한 페이지를 다른 언어/로케일로 볼 수 있습니다. 스위스 독일어 버전의 웹 사이트에서 독자가 있는 경우 동일한 페이지의 미국 영어 버전으로 손쉽게 전환할 수 있습니다. 언어 탐색 구성 요소는 사이트 언어 구조를 파악하고 해당 페이지를 자동으로 찾습니다.

* 언어 탐색 구성 요소의 현지화 기능에 대한 예는 아래 [섹션을 참조하십시오](#example).
* 다른 핵심 구성 요소의 현지화 기능이 함께 작동하는 방법의 예는 핵심 구성 요소 [페이지의](localization.md)현지화 기능을 참조하십시오.

[ [편집] 대화 상자를](#edit-dialog) 사용하면 전역 사이트 탐색 루트의 정의뿐만 아니라 탐색이 가야 하는 구조의 깊이를 정의할 수 있습니다. 템플릿 작성자는 [디자인 대화](#design-dialog)상자를 사용하여 동일한 옵션에 대한 기본값을 설정할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

언어 탐색 구성 요소의 현재 버전은 v1이며, 이 버전은 2018년 1월 핵심 구성 요소 릴리스 2.0.0과 함께 도입되었으며 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소 버전이 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 핵심 구성 요소 [버전을 참조하십시오](versions.md).

## 샘플 구성 요소 출력 {#sample-component-output}

언어 탐색 구성 요소뿐만 아니라 구성 옵션의 예와 HTML 및 JSON 출력을 보려면 구성 요소 [라이브러리를 참조하십시오](http://opensource.adobe.com/aem-core-wcm-components/library/language-navigation/language-structure/us/en/language-navigation.html).

## 기술 정보 {#technical-details}

언어 탐색 구성 요소에 대한 최신 기술 문서는 GitHub에서 [찾을 수 있습니다](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/languagenavigation/v1/languagenavigation).

핵심 구성 요소 개발에 대한 자세한 내용은 핵심 구성 요소 개발자 [설명서를](developing.md)참조하십시오.

## 디자인 대화 상자 {#design-dialog}

편집 대화 상자에서는 전역 사이트 탐색 루트의 정의뿐만 아니라 탐색이 가야 하는 구조 깊이를 정의할 수 있습니다.

일반적으로 이러한 구성은 페이지 템플릿 수준에서 수행해야 합니다. 하지만 [편집 대화 상자를](#edit-dialog)통해 페이지 수준에서 변경할 수 있습니다.

### 속성 탭 {#properties-tab}

![](assets/screen_shot_2018-01-12at133642.png)

* **탐색 루트**
   * 여기에서 사이트 언어 탐색을 시작해야 합니다.
   * The language structure of the site begins on the next level below this root.
* **언어 구조 깊이**
   * This is how many levels of the content tree below the Navigation Root represent the language structure of the site. **** Examples:
      * `1` typically means that you only have the choice of language.
      * `2` typcially means that you have a choice of language and country.
      * `3` typically means that you have a choice of langauge, country, and region.

#### 예 {#example}

Let's say that your content looks something like this:

```
/content
+-- we-retail
   +-- language-masters
   +-- us
      +-- en
      \-- es
   \-- ch
      +-- de
      +-- fr
      \-- it
+-- wknd-events
\-- wknd-shop
```

For the site We.Retail, you would probably want to place the Language Navigation component on a page template as part of the header. Once part of the template, you can set the Navigation Root of the component to  since that is where your localized content for that site begins. ****`/content/we-retail` You would also want to set the Language Structure Depth to be  since your structure is of two levels (country then laguage).****`2`

With the Navigation Root value, the Language Component knows that after  that that the navigation begins and it can generate language navigation options by recognizing the next two levels in the content tree as the site's language navigation structure (as defined by the Language Structure Depth value).****`/content/we-retail`****

No matter what page a user is viewing, the Language Navigation component is able find the corresponding page in another language, by knowing the location of the current page and working backwards to the root, and then forwards to the corresponding page.

### Styles Tab {#styles-tab}

언어 탐색 구성 요소는 AEM Style [System을 지원합니다](authoring.md#component-styling).

## Edit Dialog {#edit-dialog}

일반적으로 언어 탐색 구성 요소는 사이트의 페이지 템플릿에만 추가하고 구성해야 합니다. 하지만 개별 컨텐츠 페이지에 언어 탐색 구성 요소를 추가해야 하는 경우 편집 대화 상자를 사용하면 컨텐츠 작성자가 [디자인 대화](#design-dialog)상자에 설명된 것과 동일한 값을 구성할 수 있습니다.

![](assets/screen_shot_2018-01-12at133353.png)

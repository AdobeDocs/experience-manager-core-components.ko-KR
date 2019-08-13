---
title: 언어 탐색 구성 요소
seo-title: 언어 탐색 구성 요소
description: 'null'
seo-description: 언어 탐색 구성 요소는 방문자가 다른 로케일에서 동일한 페이지로 이동할 수 있도록 사이트에 대한 언어/국가 탐색을 제공합니다.
uuid: CE 736458-9 CDF -4 BC 2-B 90 F -9 C 5 A 62 FE 1 CA 0
content-type: 참조
topic-tags: 저작
products: sg_ Experiencemanager/Corecomponents-new
discoiquuid: 8 F 232 EB 0-65 D 5-4075-8668-75 F 1366882 C 8
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
source-git-commit: 8a34ecc432e489b8dc025aeda29d8eba9c788861

---


# Language Navigation Component{#language-navigation-component}

언어 탐색 구성 요소는 방문자가 다른 로케일에서 동일한 페이지로 이동할 수 있도록 사이트에 대한 언어/국가 탐색을 제공합니다.

## 사용량 {#usage}

웹 사이트는 지역마다 여러 언어로 제공됩니다. 언어 탐색 구성 요소를 사용하면 방문자가 다른 언어/로케일로 동일한 페이지를 볼 수 있습니다. 따라서 스위스 독일어 버전의 웹 사이트에서 독자인 경우 동일한 페이지의 미국 영어 버전으로 손쉽게 전환할 수 있습니다. 언어 탐색 구성 요소는 사이트 언어 모음을 이해하는 데 사용되며 해당 페이지를 자동 검색합니다.

[편집 대화 상자에서는](#edit-dialog) 전역 사이트 탐색 루트에 대한 정의와 탐색이 이동하는 구조에 깊이를 허용할 수 있습니다. 템플릿 작성자는 [디자인 대화 상자를](#design-dialog)사용하여 동일한 옵션에 대한 기본값을 설정할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

언어 탐색 구성 요소의 현재 버전은 2018 년 1 월에 핵심 구성 요소의 릴리스 2.0.0에서 처음 소개된 v 1 이며, 이 문서에서는 설명합니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서에 대한 링크를 제공합니다.

| 구성 요소 버전 | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 문서 [코어 구성 요소 버전을 참조하십시오](versions.md).

## 샘플 구성 요소 출력 {#sample-component-output}

언어 내비게이션 구성 요소를 경험하고 HTML 및 JSON 출력과 같은 구성 옵션의 예를 보려면 [구성 요소 라이브러리를 참조하십시오](http://opensource.adobe.com/aem-core-wcm-components/library/language-navigation/language-structure/us/en/language-navigation.html).

## 기술 세부 정보 {#technical-details}

언어 내비게이션 구성 요소에 [대한 최신 기술 설명서는 Github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/languagenavigation/v1/languagenavigation)에서 찾을 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서를](developing.md)참조하십시오.

## 디자인 대화 상자 {#design-dialog}

편집 대화 상자에서는 전역 사이트 탐색 루트에 대한 정의와 탐색이 이동하는 구조에 깊이를 허용할 수 있습니다.

일반적으로 이러한 구성은 페이지 템플릿 LEVE 에서만 수행해야 합니다. 그러나 [편집 대화 상자를 통해 페이지 수준에서 변경할](#edit-dialog)수 있습니다.

### 속성 탭 {#properties-tab}

![](assets/screen_shot_2018-01-12at133642.png)

* **탐색 루트**
   * 이 위치에서 사이트의 언어 탐색이 시작됩니다.
   * 사이트의 언어 구조는 이 루트 아래의 다음 수준에서 시작됩니다.
* **언어 구조 깊이**
   * **탐색 루트 아래의 컨텐츠 트리 수준이 사이트의 언어 구조를** 나타내는 횟수입니다. 예:
      * `1` 일반적으로 사용자는 언어만 선택할 수 있습니다.
      * `2` 언어적으로는 귀하가 언어와 국가를 선택할 수 있음을 의미합니다.
      * `3` 일반적으로 사용자는 Langauge, 국가 및 지역을 선택할 수 있습니다.

#### 예 {#example}

컨텐츠가 다음과 같이 표시됩니다.

```
/content
+-- we-retail
   +-- language-masters
   +-- us
      +-- en
      \-- es
   +-- ch
      +-- de
      +-- fr
      +-- it
+-- wknd-events
\-- wknd-shop
```

We. Retail 사이트인 경우, 페이지 템플릿에 언어 탐색 구성 요소를 헤더의 일부로 배치할 수 있습니다. 템플릿의 일부가 되면 해당 사이트의 **현지화된** 컨텐츠가 시작되는 `/content/we-retail` 곳이기 때문에 구성 요소의 탐색 루트를 설정할 수 있습니다. 구조가 두 수준 (국가 간 뒤섞기) 이기 때문에 **언어 구조 깊이를** `2` 설정할 수도 있습니다.

**탐색 루트** 값을 사용할 경우 언어 구성 요소는 `/content/we-retail` 탐색이 시작되고 다음 2 개의 수준을 사이트의 언어 탐색 구조로 인식하여 언어 탐색 옵션을 생성할 수 있습니다 **(언어 구조 깊이** 값으로 정의된 대로).

사용자가 보고 있는 페이지에 관계없이 언어 탐색 구성 요소는 현재 페이지의 위치를 알고, 루트로 돌아가서 해당 페이지로 이동하여 다른 언어로 해당 페이지를 찾을 수 있습니다.

### 스타일 탭 {#styles-tab}

언어 탐색 구성 요소는 AEM [스타일 시스템을 지원합니다](authoring.md#component-styling).

## Edit Dialog {#edit-dialog}

일반적으로 Langauge 내비게이션 구성 요소는 사이트의 페이지 템플릿에 추가하고 구성해야 합니다. 그러나 언어 내비게이션 구성 요소를 개별 컨텐츠 페이지에 추가해야 하는 경우 컨텐츠 작성자는 컨텐츠 작성자가 [디자인 대화 상자에 설명된 것과 동일한 값을 구성할](#design-dialog)수 있습니다.

![](assets/screen_shot_2018-01-12at133353.png)

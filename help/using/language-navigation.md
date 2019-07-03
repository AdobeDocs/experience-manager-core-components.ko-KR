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
source-git-commit: eef608fb06001485aa2c2c0b574af412ed7f15a4

---


# Language Navigation Component{#language-navigation-component}

언어 탐색 구성 요소는 방문자가 다른 로케일에서 동일한 페이지로 이동할 수 있도록 사이트에 대한 언어/국가 탐색을 제공합니다.

## 사용량 {#usage}

종종 웹 사이트는 지역마다 여러 언어로 제공됩니다. 언어 탐색 구성 요소를 사용하면 방문자가 다른 언어/로케일로 동일한 페이지를 볼 수 있습니다.

[편집 대화 상자에서는](#edit-dialog) 전역 사이트 탐색 루트에 대한 정의와 탐색이 이동하는 구조에 깊이를 허용할 수 있습니다. Using the [design dialog](#design-dialog), the template author can set the default values for the same options.

## Version and Compatibility {#version-and-compatibility}

언어 탐색 구성 요소의 현재 버전은 2018 년 1 월에 핵심 구성 요소의 릴리스 2.0.0에서 처음 소개된 v 1 이며, 이 문서에서는 설명합니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서에 대한 링크를 제공합니다.

| 구성 요소 버전 | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |


For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

To experience the Language Navigation Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/language-navigation/language-structure/us/en/language-navigation.html).

## Technical Details {#technical-details}

The latest technical documentation about the Language Navigation Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/languagenavigation/v1/languagenavigation).

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md).

## Edit Dialog {#edit-dialog}

편집 대화 상자에서는 전역 사이트 탐색 루트에 대한 정의와 탐색이 이동하는 구조에 깊이를 허용할 수 있습니다.

![](assets/screen_shot_2018-01-12at133353.png)

* **탐색 루트는**
탐색 구조의 루트 페이지를 정의합니다.
   * Use the **Open Selection Dialog** button to easily navigate the content structure and select the root.
* **탐색 루트를 기준으로 한 글로벌 언어 구조의 언어 구조 깊이**
깊이입니다.

## Design Dialog {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 사용하여 편집 대화 상자에서 사용할 수 있는 동일한 옵션에 대한 기본값을 설정할 수 있습니다.

### Properties Tab {#properties-tab}

![](assets/screen_shot_2018-01-12at133642.png)

* **컨텐츠 작성자가 컨텐츠 페이지에 언어 전환기 구성 요소를 배치할 때 탐색 루트의 탐색 루트**
기본값
* **컨텐츠 작성자가 컨텐츠 페이지에 언어 전환기 구성 요소를 배치할 때 언어 구조 깊이의 언어 구조 깊이**
기본값

### Styles Tab {#styles-tab}

The Language Navigation Component supports the AEM [Style System](authoring.md#component-styling).
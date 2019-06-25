---
title: 탐색 구성 요소
seo-title: 탐색 구성 요소
description: 'null'
seo-description: 탐색 구성 요소를 사용하면 글로벌라이제이션 사이트 구조를 쉽게 탐색할 수 있습니다.
uuid: 616 c 03 fb -39 b 3-402 a-b 990-f 56 c 87 bc 6 df 4
content-type: 참조
topic-tags: 저작
products: sg_ Experiencemanager/Corecomponents-new
discoiquuid: da 8 d 67 d 7-b 65 e -4041-bc 0 e-e 998 f 24 a 68 f 9
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
source-git-commit: c58826c133eb112b305fa4facbe2a81e577eb896

---


# Navigation Component{#navigation-component}

탐색 구성 요소를 사용하면 글로벌라이제이션 사이트 구조를 쉽게 탐색할 수 있습니다.

## 사용량 {#usage}

탐색 구성 요소는 블루프린트 Live Copy, 언어 마스터의 언어 사본 또는 간단한 페이지 트리에서 구축할 수 있는 모든 탐색 계층을 허용합니다. 페이지 사용자는 사이트 구조를 쉽게 탐색할 수 있습니다.

The [edit dialog](#edit-dialog) allows the content author to define the navigation root page along with the depth of navigation. The [design dialog](#design-dialog) allows the template author to define default values for the navigation root and depth.

## Version and Compatibility {#version-and-compatibility}

탐색 구성 요소의 현재 버전은 2018 년 1 월에 핵심 구성 요소의 릴리스 2.0.0에서 처음 소개된 v 1 이며, 이 문서에서는 설명합니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서에 대한 링크를 제공합니다.

| 구성 요소 버전 | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |


For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

To experience the Navigation Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/navigation.html).

## Technical Details {#technical-details}

The latest technical documentation about the Navigation Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/navigation/v1/navigation).

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md.

>[!NOTE]
>
>As of Core Components release 2.1.0, the Navigation Component supports [schema.org microdata](https://schema.org).

## Edit Dialog {#edit-dialog}

편집 대화 상자에서 컨텐츠 작성자는 탐색을 위한 루트 페이지와 탐색 구조의 깊이를 정의할 수 있습니다.

![](assets/screen_shot_2018-04-03at112055.png)

* **탐색 루트**
탐색 트리를 생성하는 데 사용되는 루트 페이지입니다.
* **제외 탐색 루트**
결과 트리에서 탐색 루트를 제외시키고 그 하위 항목을 포함합니다.
* **모든 하위 페이지**
수집 탐색 루트의 하위 항목인 모든 페이지를 수집합니다.
* **탐색 구조 깊이는**
탐색 트리에서 구성 요소가 얼마나 많이 표시되어야 하는지를 정의합니다 (모든 하위 페이지를 **수집하지 않은 경우에만** 사용 가능).

## Design Dialog {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 사용하여 컨텐츠 작성자에게 표시되는 탐색 루트 페이지 및 탐색 깊이에 대한 기본값을 설정할 수 있습니다.

### Properties Tab {#properties-tab}

![](assets/screen_shot_2018-04-03at112357.png)

* **탐색 루트에는**
탐색 트리를 생성하는 데 사용할 탐색 구조의 기본값, 컨텐츠 작성자가 구성 요소를 페이지에 추가할 때 기본값이 지정됩니다.
* **제외 탐색 루트**
결과 트리에서 탐색 루트를 제외하는 옵션의 기본값입니다.
* **탐색 루트의 하위 항목인 모든 페이지를 수집하는 옵션의**기본값을 모든 하위 페이지에
수집합니다.
* **탐색 구조 깊이탐색**
구조 깊이의 기본값입니다.

### Styles Tab {#styles-tab}

The Navigation Component supports the AEM [Style System](authoring.md#component-styling).
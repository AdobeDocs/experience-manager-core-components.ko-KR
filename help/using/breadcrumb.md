---
title: 탐색 표시 구성 요소
seo-title: 탐색 표시 구성 요소
description: 'null'
seo-description: 핵심 구성 요소 탐색 표시 구성 요소는 컨텐츠 계층 구조에서 페이지 위치를 기반으로 링크의 탐색 표시를 빌드하는 탐색 구성 요소입니다.
uuid: 13 e 858 d 5-24 ad -4144-adc 4-0 fa 1 ffd 257 c 1
contentOwner: 사용자
content-type: 참조
topic-tags: 저작
products: sg_ Experiencemanager/Corecomponents-new
discoiquuid: ECD 237 DF -08 B 8-4 DEB -9881-66 A 1 F 0 D 65 EF 3
modalsize: 426x240
translation-type: tm+mt
source-git-commit: c58826c133eb112b305fa4facbe2a81e577eb896

---


# Breadcrumb Component{#breadcrumb-component}

핵심 구성 요소 탐색 표시 구성 요소는 컨텐츠 계층 구조에서 페이지 위치를 기반으로 링크의 탐색 표시를 빌드하는 탐색 구성 요소입니다.

## 사용량 {#usage}

탐색 표시 구성 요소는 사이트 계층 구조 내에서 현재 페이지의 위치를 표시하므로 페이지 방문자가 현재 위치에서 페이지 계층을 탐색할 수 있습니다. 페이지 머리글이나 바닥글에 통합되는 경우가 많습니다.

Available options, such as the default navigation level and the ability to show the current page or hidden pages, can be defined by the template author in the [design dialog](#design-dialog). The content editor can then choose if hidden pages should be shown or not and the actual navigation level for the component in the [edit dialog](#edit-dialog).

## Version and Compatibility {#version-and-compatibility}

Breadcrumb 구성 요소의 현재 버전은 2018 년 1 월에 핵심 구성 요소의 릴리스 2.0.0에 도입된 v 2 이며, 이 문서에서는 설명합니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서에 대한 링크를 제공합니다.

| 구성 요소 버전 | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | 호환 가능 | 호환 가능 | 호환 가능 |
| [v1](breadcrumb-v1.md) | 호환 가능 | 호환 가능 | 호환 가능 |

For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

To experience the Breadcrumb Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/breadcrumb.html).

>[!NOTE]
>
>As of Core Components release 2.1.0, the Breadcrumb Component supports [schema.org microdata](https://schema.org/BreadcrumbList).

## Technical Details {#technical-details}

The latest technical documentation about the Breadcrumb Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb).

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md).

## Edit Dialog {#edit-dialog}

컨텐츠 작성자는 편집 대화 상자를 사용하여 탐색 표시 시 숨겨진 페이지와 활성 페이지를 표시하지 않을 수 있습니다.

![](assets/screen_shot_2018-01-12at124250.png)

* **탐색 시작 수준** - 계층에서 탐색 표시 구성 요소가 현재 페이지로 이동하기 시작해야 합니다. 예를 들어 We. Retail에서 다음을 수행합니다.

   * 0 starts at `/content`

   * 1 starts at `/content/we-retail`
   * 2 starts at `/content/we-retail/<country>`

* **숨겨진 탐색 항목 표시** - 탐색 표시에 숨김으로 표시된 페이지 표시 (기본적으로 표시되지 않음)
* **현재 페이지 숨기기**- 탐색 표시를 통해 현재 페이지를 표시하지 않습니다 (기본적으로 표시).

## Design Dialog {#design-dialog}

템플릿 작성자는 [디자인] 대화 상자를 사용하여 탐색 표시 시 숨겨진 페이지와 활성 페이지를 표시하지 않고 표시해야 하는 계층 구조의 깊이를 지정할 수 있습니다.

### Main Tab {#main-tab}

![](assets/screen_shot_2018-01-12at124437.png)

* **탐색 시작 수준** - 탐색 표시 구성 요소가 페이지에 추가될 때 탐색 표시 구성 요소가 현재 페이지로 이동하는 데 필요한 기본 값을 정의합니다.
* **숨겨진 탐색 항목 표시** - 탐색 표시 구성 요소가 페이지에 추가되면 숨겨진 탐색 항목 **표시** 옵션의 기본값을 정의합니다.

   * 작성자에 대한 옵션은 활성화 또는 비활성화되지 않습니다. 기본값을 설정합니다.

* **현재 페이지 숨기기**- 탐색 표시 구성 요소가 페이지에 추가되면 현재 페이지 **숨기기** 옵션의 기본값을 정의합니다.

   * 작성자에 대한 옵션은 활성화 또는 비활성화되지 않습니다. 기본값을 설정합니다.

### Styles Tab {#styles-tab}

The Breadcrumb Component supports the AEM [Style System](authoring.md#component-styling).
---
title: 제목 구성 요소
seo-title: 제목 구성 요소
description: 'null'
seo-description: 핵심 구성 요소 제목 구성 요소는 즉석 편집을 특징으로 하는 섹션 제목 구성 요소입니다.
uuid: CF 190861-E 5 CD -42 B 8-9193-842 B 8 DF 8 C 5 C 6
contentOwner: 사용자
content-type: 참조
topic-tags: 저작
products: sg_ Experiencemanager/Corecomponents-new
discoiquuid: 243 EFC 75-FCF 9-427 D -9303-9642 B 0602991
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: eef608fb06001485aa2c2c0b574af412ed7f15a4

---


# 제목 구성 요소{#title-component}

핵심 구성 요소 제목 구성 요소는 즉석 편집을 특징으로 하는 섹션 제목 구성 요소입니다.

## 사용량 {#usage}

제목 구성 요소는 컨텐츠 섹션의 제목 또는 제목으로 사용됩니다. The available heading levels can be defined by the template author in the [design dialog](#design-dialog). The content editor can select from available headings levels in the [edit dialog](#edit-dialog). 편의를 위해 제목 텍스트를 간단하게 즉석에서 편집할 수도 있습니다.

## Version and Compatibility {#version-and-compatibility}

제목 구성 요소의 현재 버전은 2018 년 1 월에 핵심 구성 요소의 릴리스 2.0.0에 도입된 v 2 이며, 이 문서에서는 설명합니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서에 대한 링크를 제공합니다.

| 구성 요소 버전 | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|---|---|---|---|
| v2 | 호환 가능 | 호환 가능 | 호환 가능 |
| [v1](title-v1.md) | 호환 가능 | 호환 가능 | 호환 가능 |

For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

To experience the Title Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/title.html).

### Technical Details {#technical-details}

The latest technical documentation about the Title Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/title/v2/title).

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md).

## Edit Dialog {#edit-dialog}

컨텐츠 작성자는 편집 대화 상자를 사용하여 제목 텍스트를 정의하고 제목 수준을 선택할 수 있습니다.

* **제목** - 비워 두면 페이지 제목이 사용됩니다.
* **유형/크기** - 제목의 제목 수준을 정의합니다.
* **링크** - 제목이 링크되는 컨텐츠를 정의합니다. 이것은 컨텐츠 페이지, 외부 URL 또는 페이지 앵커의 경로일 수 있습니다.

![](assets/screenshot_2018-10-19at110055.png)

>[!CAUTION]
>
>제목 링크를 정의하는 기능은 핵심 구성 요소의 릴리스 2.2.0에서 도입되었습니다.

즉석 편집기를 사용하여 제목 구성 요소의 텍스트를 편집할 수도 있습니다.

![](assets/chlimage_1-37.png)

## Design Dialog {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 사용하여 컨텐츠 작성자가 만들 때 제목 구성 요소가 가질 기본 머리글 수준을 정의할 수 있습니다.

### Sizes Tab {#sizes-tab}

![](assets/screenshot_2018-10-19at110120.png)

* **작성자에 허용된 유형/크기** - 컨텐츠 작성자가 제목 구성 요소를 사용할 때 사용할 수 있는 머리글 유형을 활성화하거나 비활성화할 수 있습니다.
* **기본 유형/크기**- 컨텐츠 작성자가 페이지에 제목 구성 요소를 추가할 때 자동으로 지정되는 머리글 유형을 정의합니다.
* **링크 비활성화**- 제목 구성 요소의 링크에 대한 지원을 비활성화하여 컨텐츠 작성자가 제목에서 연결할 수 없도록 합니다.

>[!CAUTION]
>
>제목 링크를 정의하는 기능은 핵심 구성 요소의 릴리스 2.2.0에서 도입되었습니다.

### Styles Tab {#styles-tab}

The Title Component supports the AEM [Style System](authoring.md#component-styling).
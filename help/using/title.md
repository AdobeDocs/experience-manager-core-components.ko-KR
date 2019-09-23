---
title: 제목 구성 요소
seo-title: 제목 구성 요소
description: 'null'
seo-description: The Core Component Title Component is a section heading component that features in-place editing.
uuid: cf190861-e5cd-42b8-9193-842b8df8c5c6
contentOwner: 사용자
content-type: 참조
topic-tags: authoring
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: 243efc75-fcf9-427d-9303-9642b0602991
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: eef608fb06001485aa2c2c0b574af412ed7f15a4

---


# 제목 구성 요소{#title-component}

The Core Component Title Component is a section heading component that features in-place editing.

## 사용량 {#usage}

제목 구성 요소는 컨텐츠 섹션의 제목이나 머리글로 사용됩니다. 사용 가능한 제목 수준은 [디자인 대화](#design-dialog)상자에서 템플릿 작성자가 정의할 수 있습니다. 컨텐츠 편집기는 [편집 대화 상자의](#edit-dialog)사용 가능한 머리글 수준 중에서 선택할 수 있습니다. 편리한 추가 기능을 위해 제목 텍스트를 직접 편집할 수도 있습니다.

## Version and Compatibility {#version-and-compatibility}

The current version of the Title Component is v2, which was introduced with release 2.0.0 of the Core Components in January 2018, and is described in this document.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소 버전이 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|---|---|---|---|
| v2 | 호환 가능 | 호환 가능 | 호환 가능 |
| [v1](title-v1.md) | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 핵심 구성 요소 [버전을 참조하십시오](versions.md).

## 샘플 구성 요소 출력 {#sample-component-output}

제목 구성 요소뿐만 아니라 구성 옵션 예와 HTML 및 JSON 출력을 보려면 구성 요소 [라이브러리를 참조하십시오](http://opensource.adobe.com/aem-core-wcm-components/library/title.html).

### 기술 정보 {#technical-details}

제목 구성 요소에 대한 최신 기술 문서는 GitHub에서 [찾을 수 있습니다](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/title/v2/title).

핵심 구성 요소 개발에 대한 자세한 내용은 핵심 구성 요소 개발자 [설명서를](developing.md)참조하십시오.

## Edit Dialog {#edit-dialog}

편집 대화 상자에서는 컨텐츠 작성자가 제목 텍스트를 정의할 수 있을 뿐만 아니라 제목 수준을 선택할 수 있습니다.

* **제목** - 비어 있으면 페이지 제목이 사용됩니다.
* **유형/크기** - 제목의 제목 수준을 정의합니다.
* **링크** - 제목을 연결할 컨텐츠를 정의합니다. 컨텐츠 페이지, 외부 URL 또는 페이지 앵커에 대한 경로일 수 있습니다.

![](assets/screenshot_2018-10-19at110055.png)

>[!CAUTION]
>
>제목에 대한 링크를 정의하는 기능은 핵심 구성 요소의 릴리스 2.2.0과 함께 도입되었습니다.

즉석 편집기를 사용하여 제목 구성 요소의 텍스트를 편집할 수도 있습니다.

![](assets/chlimage_1-37.png)

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 사용하여 컨텐츠 작성자가 작성할 때 제목 구성 요소가 가질 기본 제목 수준을 정의할 수 있습니다.

### 크기 탭 {#sizes-tab}

![](assets/screenshot_2018-10-19at110120.png)

* **작성자의 허용된 유형/크기** - 제목 구성 요소를 사용할 때 컨텐츠 작성자가 사용할 수 있는 머리글 유형을 활성화하거나 비활성화합니다.
* **기본 유형/크기**- 컨텐츠 작성자가 페이지에 제목 구성 요소를 추가할 때 자동으로 지정되는 제목 유형을 정의합니다.
* **링크**&#x200B;비활성화 - 제목 구성 요소의 링크에 대한 지원을 비활성화하여 컨텐츠 작성자가 제목에서 링크를 연결할 수 없도록 합니다.

>[!CAUTION]
>
>제목에 대한 링크를 정의하는 기능은 핵심 구성 요소의 릴리스 2.2.0과 함께 도입되었습니다.

### 스타일 탭 {#styles-tab}

제목 구성 요소는 AEM 스타일 [시스템을 지원합니다](authoring.md#component-styling).
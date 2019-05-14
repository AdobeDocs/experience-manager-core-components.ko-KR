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
source-git-commit: b179888d19a95257602656d456d5c6bfe82877af

---


# 제목 구성 요소{#title-component}

핵심 구성 요소 제목 구성 요소는 즉석 편집을 특징으로 하는 섹션 제목 구성 요소입니다.

## 사용량 {#usage}

제목 구성 요소는 컨텐츠 섹션의 제목 또는 제목으로 사용됩니다. 사용 가능한 머리글 수준은 [디자인 대화 상자에서 템플릿 작성자가 정의할](#design-dialog)수 있습니다. 컨텐츠 편집기는 [편집 대화 상자에서 사용 가능한 머리글 수준 중에서 선택할](#edit-dialog)수 있습니다. 편의를 위해 제목 텍스트를 간단하게 즉석에서 편집할 수도 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

제목 구성 요소의 현재 버전은 2018 년 1 월에 핵심 구성 요소의 릴리스 2.0.0에 도입된 v 2 이며, 이 문서에서는 설명합니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서에 대한 링크를 제공합니다.

| 구성 요소 버전 | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|---|---|---|---|
| v2 | 호환 가능 | 호환 가능 | 호환 가능 |
| [v1](title-v1.md) | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 문서 [코어 구성 요소 버전을 참조하십시오](versions.md).

## 샘플 구성 요소 출력 {#sample-component-output}

[다음은 We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html)에서 가져온 샘플입니다.

### 스크린샷 {#screenshot}

![](assets/chlimage_1-36.png)

### 구성 요소 라이브러리

제목 구성 요소를 경험하고 HTML 및 JSON 출력뿐만 아니라 구성 옵션의 예를 보려면 [구성 요소 라이브러리를 참조하십시오](http://opensource.adobe.com/aem-core-wcm-components/library/title.html).

### 기술 세부 정보 {#technical-details}

제목 구성 요소에 [대한 최신 기술 설명서는 Github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/title/v2/title)에서 찾을 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서를](developing.md)참조하십시오.

## 편집 대화 상자 {#edit-dialog}

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

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 사용하여 컨텐츠 작성자가 만들 때 제목 구성 요소가 가질 기본 머리글 수준을 정의할 수 있습니다.

### 크기 탭 {#sizes-tab}

![](assets/screenshot_2018-10-19at110120.png)

* **작성자에 허용된 유형/크기** - 컨텐츠 작성자가 제목 구성 요소를 사용할 때 사용할 수 있는 머리글 유형을 활성화하거나 비활성화할 수 있습니다.
* **기본 유형/크기**- 컨텐츠 작성자가 페이지에 제목 구성 요소를 추가할 때 자동으로 지정되는 머리글 유형을 정의합니다.
* **링크 비활성화**- 제목 구성 요소의 링크에 대한 지원을 비활성화하여 컨텐츠 작성자가 제목에서 연결할 수 없도록 합니다.

>[!CAUTION]
>
>제목 링크를 정의하는 기능은 핵심 구성 요소의 릴리스 2.2.0에서 도입되었습니다.

### 스타일 탭 {#styles-tab}

제목 구성 요소는 AEM [스타일 시스템을 지원합니다](authoring.md#component-styling).
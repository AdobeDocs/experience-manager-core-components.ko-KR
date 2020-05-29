---
title: 아코디언 구성 요소
description: 핵심 구성 요소 아코디언 구성 요소를 사용하면 페이지의 아코디언을 사용하여 패널 모음을 만들 수 있습니다.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '1051'
ht-degree: 1%

---


# 아코디언 구성 요소{#accordion-component}

핵심 구성 요소 아코디언 구성 요소를 사용하면 페이지의 아코디언을 사용하여 패널 모음을 만들 수 있습니다.

## 사용량 {#usage}

코어 구성 요소 아코디언 구성 요소를 사용하면 [탭 구성 요소와](tabs.md)유사하게 페이지에 아코디언 형태로 구성하고 패널로 구성된 구성 요소 모음을 만들 수 있지만 패널을 확장하고 축소할 수 있습니다.

* 아코디언 속성은 구성 대화 상자에서 [정의할 수 있습니다](#configure-dialog).
* 아코디언 패널의 순서는 구성 대화 상자와 [선택 패널 팝업에서 정의할 수 있습니다](#select-panel-popover).
* 페이지에 추가할 때 아코디언 구성 요소의 기본값은 [디자인 대화 상자에서 정의할 수 있습니다](#design-dialog).

## 패널에 대한 딥 링크 {#deep-linking}

아코디언 및 [탭 구성](tabs.md) 요소는 구성 요소 내의 패널에 직접 연결하는 것을 지원합니다.

이를 위해 진행되는 작업:

1. 페이지 편집기의 게시됨으로 **[보기](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/authoring/editing-content.html#view-as-published)**옵션을 사용하여 구성 요소가 있는 페이지를 봅니다.
1. 페이지의 컨텐츠를 검사하고 패널의 ID를 확인합니다.
   * 예 `id="accordion-86196c94d3-item-ca319dbb0b"`
1. ID는 해시(`#`)를 사용하여 URL에 추가할 수 있는 앵커가 됩니다.
   * 예 `https://wknd.site/content/wknd/language-masters/en/magazine/western-australia.html#accordion-86196c94d3-item-ca319dbb0b`

패널 ID를 앵커로 사용하여 URL로 이동하면 브라우저가 특정 구성 요소로 직접 스크롤되어 지정된 패널을 표시합니다. 패널을 기본적으로 확장하지 않도록 구성한 경우 자동으로 확장됩니다.

## 버전 및 호환성 {#version-and-compatibility}

아코디언 구성 요소의 현재 버전은 v1이며, 2019년 6월에 핵심 구성 요소 릴리스 2.5.0에서 도입되었으며 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전이 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | 클라우드 서비스로서의 AEM |
|--- |--- |---|---|
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전을 참조하십시오](/help/versions.md).

## 샘플 구성 요소 출력 {#sample-component-output}

아코디언 구성 요소뿐만 아니라 구성 옵션 예와 HTML 및 JSON 출력을 보려면 [구성 요소 라이브러리를 방문하십시오](https://adobe.com/go/aem_cmp_library_accordion).

## 기술 세부 정보 {#technical-details}

Accordion 구성 요소에 대한 최신 기술 문서는 GitHub에서 찾을 [수 있습니다](https://adobe.com/go/aem_cmp_tech_accordion_v1).

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서를 참조하십시오](/help/developing/overview.md).

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자에서는 컨텐츠 작성자가 아코디언 항목, 패널, 방문자가 페이지에 대해 동작하고 표시할 방법을 정의할 수 있습니다.

### 항목 탭 {#items-tab}

![아코디언 구성 요소의 편집 대화 상자 항목 탭](/help/assets/accordion-edit-items.png)

[ **추가** ] 단추를 사용하여 구성 요소 선택기를 열고 패널로 추가할 구성 요소를 선택합니다. 추가된 항목은 다음 열을 포함하는 목록에 추가됩니다.

* **아이콘** - 목록에서 쉽게 식별할 수 있는 패널의 구성 요소 유형의 아이콘입니다. 전체 구성 요소 이름을 툴팁으로 보려면 마우스를 가져갑니다.
* **설명** - 패널의 텍스트로 사용된 설명으로서, 패널에 선택된 구성 요소의 이름이 기본값으로 설정됩니다.
* **삭제** - 아코디언 구성 요소에서 패널을 삭제하려면 탭하거나 클릭합니다.
* **재배치** - 패널 순서를 누르거나 클릭하여 드래그합니다.

>[!TIP]
>
>페이지의 뷰포트가 축소되어 편집 대화 상자가 전체 화면이 되면 **추가** 단추가 숨겨집니다. 구성 요소 브라우저에서 [드래그하고 페이지 편집기의 아코디언 구성 요소를 놓아 구성 요소를 아코디언 구성 요소에 추가할 수 있습니다](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html#InsertingaComponent).

### 속성 탭 {#properties-tab}

![아코디언 구성 요소의 편집 대화 상자 속성 탭](/help/assets/accordion-edit-properties.png)

* **단일 항목 확장** - 이 옵션을 선택하면 단일 아코디언 항목이 한 번에 확장됩니다. 한 항목을 확장하면 다른 항목이 모두 축소됩니다.
* **확장된 항목** - 이 옵션은 페이지를 로드할 때 기본적으로 확장된 항목을 정의합니다.
   * 단일 **항목 확장을** 선택한 경우 하나의 패널을 선택해야 합니다. 기본적으로 첫 번째 패널이 선택됩니다.
   * 단일 항목 확장 **을** 선택하지 않으면 이 옵션은 다중 선택이며 선택 사항입니다.
* **ID** - 이 옵션을 사용하면 HTML과 [데이터 레이어에서 구성 요소의 고유 식별자를 제어할 수 있습니다](/help/developing/data-layer/overview.md).
   * 비워 두면 자동으로 고유 ID가 생성되어 결과 페이지를 검사하여 찾을 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID를 변경하면 CSS, JS 및 데이터 레이어 추적에 영향을 줄 수 있습니다.

## 패널 팝업 선택 {#select-panel-popover}

컨텐츠 작성자는 구성 요소 도구 모음의 **패널** 선택 옵션을 사용하여 편집할 수 있는 다른 패널로 변경할 수 있을 뿐만 아니라 아코디언 내의 패널 순서를 쉽게 재정렬할 수 있습니다.

![패널 아이콘 선택](/help/assets/select-panel-icon.png)

구성 요소 도구 모음에서 **패널** 선택 옵션을 선택하면 구성된 아코디언 패널이 드롭다운으로 표시됩니다.

![패널 선택 팝업](/help/assets/select-panel-popover.png)

* 목록이 패널의 지정된 배열별로 정렬되며 번호 매기기에 반영됩니다.
* 패널의 구성 요소 유형이 먼저 표시되고, 그 다음에 더 밝은 글꼴의 패널 설명이 표시됩니다.
* 드롭다운에서 항목을 탭하거나 클릭하면 편집기의 보기가 해당 패널로 전환됩니다.
* 끌기 핸들을 사용하여 패널의 위치를 조절할 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 사용하여 아코디언 구성 요소를 사용할 때 기본값과 아코디언 구성 요소를 가져올 때 설정한 옵션을 컨텐츠 작성자가 사용할 수 있는 옵션을 정의할 수 있습니다.

### 속성 탭 {#properties-tab-design}

![디자인 대화 상자 속성 탭](/help/assets/accordion-design-properties.png)

* **허용되는 머리글 요소** - 이 다중 선택 드롭다운은 작성자가 선택할 수 있는 아코디언 항목 제목 HTML 요소를 정의합니다.
* **기본 머리글 요소** - 이 드롭다운은 기본 아코디언 항목 제목 HTML 요소를 정의합니다.

### Allowed Components Tab {#allowed-components-tab}

허용된 구성 요소 **** 탭은 컨텐츠 작성자가 아코디언 구성 요소의 패널에 항목으로 추가할 수 있는 구성 요소를 정의하는 데 사용됩니다.

템플릿 편집기에서 레이아웃 컨테이너의 정책 및 속성을 [정의할 때 허용된 구성 요소 탭은 동일한 이름의 탭과 동일한 방식으로 작동합니다.](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/templates.html)

### 스타일 탭 {#styles-tab}

아코디언 구성 요소는 AEM [스타일 시스템을 지원합니다](/help/get-started/authoring.md#component-styling).

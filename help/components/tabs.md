---
title: 탭 구성 요소
description: 탭 구성 요소를 사용하면 여러 탭을 만들어 페이지에 컨텐츠를 정렬할 수 있습니다.
role: Architect, Developer, Admin, User
exl-id: 0031c5f3-447c-4932-898f-2f453801e492
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '1040'
ht-degree: 2%

---

# 탭 구성 요소 {#tabs-component}

코어 구성 요소 탭 구성 요소를 사용하면 컨텐츠를 여러 탭에 구성할 수 있습니다.

## 사용량 {#usage}

탭 구성 요소를 사용하면 컨텐츠 작성자가 여러 탭 내에서 페이지 컨텐츠를 구성할 수 있습니다.

[편집 대화 상자](#edit-dialog)를 사용하면 컨텐츠 작성자가 여러 탭을 정의하고 활성 탭을 설정할 수 있습니다. 템플릿 작성자는 [디자인 대화 상자](#design-dialog)를 사용하여 탭에 추가할 수 있는 구성 요소를 정의하고 스타일을 사용자 지정할 수 있습니다.

>[!TIP]
>
>중첩된 탭 구성 요소(탭 내의 탭)가 지원됩니다.
>
>[컨텐츠 트리](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html#content-tree)를 사용하여 단순(중첩된 아님) 탭 구성 요소를 찾거나 선택할 수 있지만 중첩된 탭은 할 수 없습니다.

## 패널에 대한 딥 링크 {#deep-linking}

탭 및 [아코디언 구성 요소](accordion.md)는 구성 요소 내의 패널에 직접 연결하는 것을 지원합니다.

이를 위해 진행되는 작업:

1. 페이지 편집기에서 **[게시됨으로 보기](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** 옵션을 사용하여 구성 요소가 있는 페이지를 봅니다.
1. Inspect 페이지의 컨텐츠를 표시하고 패널의 ID를 식별합니다.
   * 예 `id="accordion-86196c94d3-item-ca319dbb0b"`
1. ID는 해시(`#`)를 사용하여 URL에 추가할 수 있는 앵커가 됩니다.
   * 예 `https://wknd.site/content/wknd/language-masters/en/magazine/western-australia.html#accordion-86196c94d3-item-ca319dbb0b`

패널 ID가 앵커로 있는 URL로 이동하면 브라우저가 특정 구성 요소로 직접 스크롤하여 지정된 패널을 표시합니다. 패널이 기본적으로 확장되지 않도록 구성된 경우 자동으로 확장됩니다.

## 버전 및 호환성 {#version-and-compatibility}

탭 구성 요소의 현재 버전은 v1이며, 2018년 10월에 핵심 구성 요소 릴리스 2.2.0에서 도입되었으며, 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전이 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

탭 구성 요소와 HTML 및 JSON 출력 및 구성 옵션의 예를 보려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_tabs)를 방문하십시오.

### 기술 세부 정보 {#technical-details}

탭 구성 요소 [에 대한 최신 기술 설명서는 GitHub](https://adobe.com/go/aem_cmp_tech_tabs_v1)에 있습니다.

코어 구성 요소 개발에 대한 자세한 내용은 [코어 구성 요소 개발자 설명서](/help/developing/overview.md)에서 확인할 수 있습니다.

## 편집 대화 상자 {#edit-dialog}

편집 대화 상자에서는 컨텐츠 작성자가 탭을 만들고, 이름을 변경하고, 다시 배열하고, 활성 탭을 정의할 수 있습니다.

### 항목 탭 {#items-tab}

![탭 구성 요소의 편집 대화 상자 항목 탭](/help/assets/tabs-edit-items.png)

**추가** 단추를 사용하여 구성 요소 선택기를 열고 탭으로 추가할 구성 요소를 선택합니다. 추가된 항목이 목록에 추가되고 여기에 다음 열이 포함됩니다.

* **아이콘**  - 목록에서 쉽게 식별할 수 있도록 탭의 구성 요소 유형의 아이콘입니다. 전체 구성 요소 이름을 도구 설명으로 보려면 마우스를 가져갑니다.
* **설명**  - 탭의 텍스트로 사용되는 설명으로서, 탭에 대해 선택된 구성 요소의 이름에 대한 기본값이 설정됩니다.
* **삭제**  - 탭 구성 요소에서 탭을 삭제하려면 탭하거나 클릭합니다.
* **다시 정렬**  - 탭의 순서를 재정렬하려면 탭하거나 클릭하고 드래그합니다.

>[!TIP]
>
>페이지의 뷰포트가 축소되어 편집 대화 상자가 전체 화면이 되면 **추가** 단추가 숨겨집니다. 구성 요소 브라우저에서 [을 끌어서 페이지 편집기](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#inserting-a-component)의 탭 구성 요소를 끌어 놓아 탭 구성 요소에 구성 요소를 추가할 수 있습니다.

### 속성 탭 {#properties-tab}

![탭 구성 요소의 편집 대화 상자 속성 탭](/help/assets/tabs-edit-properties.png)

* **활성 항목**  - 컨텐츠 작성자는 페이지가 로드될 때 활성 상태인 탭을 정의할 수 있습니다.
   * **기본** 옵션을 사용하면 첫 번째 탭이 선택됩니다.
* **ID**  - 이 옵션을 사용하면 HTML과  [데이터 레이어에서 구성 요소의 고유 식별자를 제어할 수 있습니다](/help/developing/data-layer/overview.md).
   * 비워 두면 고유 ID가 자동으로 생성되며 결과 페이지를 검사하여 찾을 수 있습니다.
   * ID가 지정된 경우 ID가 고유한지 확인하는 것은 작성자의 책임입니다.
   * ID를 변경하면 CSS, JS 및 데이터 레이어 추적에 영향을 줄 수 있습니다.

### 액세스 가능성 탭 {#accessibility-tab}

![탭 구성 요소의 편집 대화 상자 액세스 가능성 탭](/help/assets/tabs-edit-accessibility.png)

**액세스 가능성** 탭에서 구성 요소의 [ARIA 액세스 가능성](https://www.w3.org/WAI/standards-guidelines/aria/) 레이블에 대한 값을 설정할 수 있습니다.

* **레이블**  - 구성 요소에 대한 ARIA 레이블 속성의 값

## 패널 선택 {#select-panel}

컨텐츠 작성자는 구성 요소 도구 모음의 **패널 선택** 옵션을 사용하여 편집할 다른 패널로 변경하고 탭의 순서를 쉽게 다시 정렬할 수 있습니다.

![패널 선택 아이콘](/help/assets/select-panel-icon.png)

구성 요소 도구 모음에서 **패널 선택** 옵션을 선택하면 구성된 탭이 드롭다운으로 표시됩니다.

* 목록이 지정된 탭 배열별로 정렬되며 번호 매기기에서 반영됩니다.
* 탭의 구성 요소 유형이 먼저 표시되고, 그 다음에 더 밝은 글꼴로 된 탭의 설명이 표시됩니다.

![패널 팝업 선택](/help/assets/select-panel-popover.png)

* 드롭다운에서 항목을 탭하거나 클릭하면 편집기에서 보기를 해당 탭으로 전환합니다.
* 끌기 핸들을 사용하여 탭을 제자리에 배치할 수 있습니다.

>[!NOTE]
>
>**편집** 모드에서는 작성자가 탭을 선택할 수 없습니다. 게시된 컨텐츠의 리더로 탭과 상호 작용하려면 **[미리 보기](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#preview-mode)** 모드 또는 **[게시됨으로 보기](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** 옵션을 사용합니다.

## 디자인 대화 상자 {#design-dialog}

디자인 대화 상자에서는 템플릿 작성자가 탭 구성 요소에 항목으로 추가할 수 있는 구성 요소를 정의하고 컨텐츠 작성자가 사용할 수 있는 사용자 지정 스타일을 정의할 수 있습니다.

### 허용된 구성 요소 탭 {#allowed-components-tab}

**허용된 구성 요소** 탭은 컨텐츠 작성자가 탭 구성 요소에 항목으로 추가할 수 있는 구성 요소를 정의하는 데 사용됩니다.

허용된 구성 요소 탭은 템플릿 편집기에서 레이아웃 컨테이너의 정책 및 속성을 정의할 때 동일한 이름의 탭과 동일한 방식으로 작동합니다.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)[

### 스타일 탭 {#styles-tab}

탭 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

## Adobe 클라이언트 데이터 레이어 {#data-layer}

탭 구성 요소는 [Adobe 클라이언트 데이터 계층을 지원합니다.](/help/developing/data-layer/overview.md)

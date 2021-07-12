---
title: 회전판 구성 요소
description: 회전판 구성 요소를 사용하면 컨텐츠 작성자가 회전 회전하는 회전판에 컨텐츠를 표시할 수 있습니다.
role: Architect, Developer, Admin, User
exl-id: 3331214c-a05c-47e1-b54c-fbfd1045bd60
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '1125'
ht-degree: 1%

---

# 회전판 구성 요소{#carousel-component}

코어 구성 요소 회전판 구성 요소를 사용하면 컨텐츠 작성자가 탐색 가능한 회전판에 컨텐츠를 표시할 수 있습니다.

## 사용량 {#usage}

컨텐츠 작성자는 회전 메뉴 구성 요소를 사용하여 회전 슬라이드 회전하면서 컨텐츠를 구성합니다.

[편집 대화 상자](#edit-dialog)를 사용하면 컨텐츠 작성자가 여러 슬라이드를 만들고, 이름을 지정하고, 순서를 지정하며, 지연으로 자동 전환을 활성화할 수 있습니다. 템플릿 작성자는 [디자인 대화 상자](#design-dialog)를 사용하여 회전판에 추가할 수 있는 구성 요소를 정의하고, 자동 전환을 활성화하거나 비활성화하고, 스타일을 사용자 지정할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

회전판 구성 요소의 현재 버전은 v1이며, 2018년 10월에 핵심 구성 요소 릴리스 2.2.0에서 도입되었으며, 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전이 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

캐러셀 구성 요소와 구성 옵션의 예 및 HTML 및 JSON 출력을 보려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_carousel)를 방문하십시오.

### 기술 세부 정보 {#technical-details}

회전판 구성 요소 [에 대한 최신 기술 설명서는 GitHub](https://adobe.com/go/aem_cmp_tech_carousel_v1)에 있습니다.

코어 구성 요소 개발에 대한 자세한 내용은 [코어 구성 요소 개발자 설명서](/help/developing/overview.md)에서 확인할 수 있습니다.

## 편집 대화 상자 {#edit-dialog}

편집 대화 상자에서는 컨텐츠 작성자가 슬라이드를 추가, 이름 변경 및 재정렬하고 자동 전환 설정을 정의할 수 있습니다.

### 항목 탭 {#items-tab}

![회전판 구성 요소의 편집 대화 상자에 있는 항목 탭](/help/assets/carousel-edit-items.png)

**추가** 단추를 사용하여 구성 요소 선택기를 열고 탭으로 추가할 구성 요소를 선택합니다. 추가된 항목이 목록에 추가되고 여기에 다음 열이 포함됩니다.

* **아이콘**  - 목록에서 쉽게 식별할 수 있도록 탭의 구성 요소 유형의 아이콘입니다. 전체 구성 요소 이름을 도구 설명으로 보려면 마우스를 가져갑니다.
* **설명**  - 탭의 텍스트로 사용되는 설명으로서, 탭에 대해 선택된 구성 요소의 이름에 대한 기본값이 설정됩니다.
* **삭제**  - 탭 구성 요소에서 탭을 삭제하려면 탭하거나 클릭합니다.
* **재정렬**  - 탭하거나 클릭하고 드래그하여 탭을 정렬합니다.

>[!TIP]
>
>페이지의 뷰포트가 축소되어 편집 대화 상자가 전체 화면이 되면 **추가** 단추가 숨겨집니다. 구성 요소 브라우저에서 [을 끌어서 페이지 편집기](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#inserting-a-component-from-the-components-browser)의 회전 구성 요소에 놓으면 구성 요소를 회전 구성 요소에 추가할 수 있습니다.

### 속성 탭 {#properties-tab}

![회전판 구성 요소의 편집 대화 상자에 있는 속성 탭](/help/assets/carousel-edit-properties.png)

**속성** 탭에서 컨텐츠 작성자는 슬라이드를 자동으로 전환하도록 설정할 수 있습니다.

* **슬라이드 자동 전환**  - 활성 상태가 되면 구성 요소는 지정된 지연 후 자동으로 다음 슬라이드로 이동합니다.
* **전환 지연**  - 자동 전환 슬라이드를 선택한 경우 이 값을 사용하여 전환 사이의 지연(밀리초)을 정의합니다.
* **마우스로 가리키면 자동 일시 정지**  비활성화 -  **슬라이드** 를 자동으로 전환하면 커서가 회전판 위를 가리킬 때마다 회전 전환이 자동으로 일시 중지됩니다. 전환이 일시 중지되지 않도록 이 옵션을 선택합니다.
* **ID**  - 이 옵션을 사용하면 HTML과  [데이터 레이어에서 구성 요소의 고유 식별자를 제어할 수 있습니다](/help/developing/data-layer/overview.md).
   * 비워 두면 고유 ID가 자동으로 생성되며 결과 페이지를 검사하여 찾을 수 있습니다.
   * ID가 지정된 경우 ID가 고유한지 확인하는 것은 작성자의 책임입니다.
   * ID를 변경하면 CSS, JS 및 데이터 레이어 추적에 영향을 줄 수 있습니다.

>[!NOTE]
>
>**편집** 모드에서는 슬라이드 고급 컨트롤을 사용할 수 없습니다. 게시된 컨텐츠의 리더로 회전판과 상호 작용하려면 [**미리 보기** 모드](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#preview-mode) 또는 **[게시됨으로 보기](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** 옵션을 사용합니다.
>
>**편집** 모드에서는 자동 고급 기능이 활성화되지 않습니다. **[게시됨으로 보기](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** 옵션을 사용하여 게시된 컨텐츠의 리더로 자동 고급 기능을 볼 수 있습니다.

### 액세스 가능성 탭 {#accessibility-tab}

![회전판 구성 요소의 편집 대화 상자에 있는 액세스 가능성 탭](/help/assets/carousel-edit-accessibility.png)

**액세스 가능성** 탭에서 구성 요소의 [ARIA 액세스 가능성](https://www.w3.org/WAI/standards-guidelines/aria/) 레이블에 대한 값을 설정할 수 있습니다.

* **레이블**  - 구성 요소에 대한 ARIA 레이블 속성의 값

## 패널 선택 {#select-panel}

컨텐츠 작성자는 구성 요소 도구 모음의 **패널 선택** 옵션을 사용하여 편집할 다른 슬라이드로 변경하고 슬라이드의 순서를 쉽게 다시 정렬할 수 있습니다.

![패널 선택 아이콘](/help/assets/select-panel-icon.png)

구성 요소 도구 모음에서 **패널 선택** 옵션을 선택하면 구성된 슬라이드가 드롭다운으로 표시됩니다.

* 목록은 지정된 슬라이드 배열별로 정렬되며 번호 매기기를 반영합니다.
* 슬라이드의 구성 요소 유형이 먼저 표시되고 슬라이드의 설명이 더 연한 글꼴로 표시됩니다.

![패널 선택](/help/assets/select-panel-popover.png)

* 드롭다운에서 항목을 탭하거나 클릭하면 편집기의 보기가 해당 슬라이드로 전환됩니다.
* 드래그 핸들을 사용하여 슬라이드의 순서를 제자리에 변경할 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자에서 회전 메뉴 구성 요소에 슬라이드로 추가할 수 있는 구성 요소를 정의하고 자동 전환 기본값과 컨텐츠 작성자가 사용할 수 있는 사용자 지정 스타일을 정의할 수 있습니다.

### 속성 탭 {#properties-tab-1}

**속성** 탭은 컨텐츠 작성자가 페이지에 회전 메뉴 구성 요소를 추가할 때 슬라이드 전환의 기본 설정을 정의하는 데 사용됩니다.

![회전판 구성 요소의 디자인 대화 상자](/help/assets/carousel-design.png)

* **슬라이드 자동 전환**  - 컨텐츠 작성자가 페이지에 회전 메뉴 구성 요소를 추가할 때 회전판을 다음 슬라이드로 자동 이동하는 옵션이 활성화되어 있는지 여부를 정의합니다.
* **전환 지연**  - 컨텐츠 작성자가 회전 메뉴 구성 요소를 페이지에 추가할 때 슬라이드 간 전환 지연의 기본값(밀리초)을 정의합니다.
* **마우스로 가리키면 자동 일시 중지 비활성화**  - 컨텐츠 작성자가  **슬라이드** 를 자동으로 전환하여 선택 시 자동 슬라이드 일시 중지 비활성화 옵션이 활성화되는지 여부를 정의합니다.

### 허용된 구성 요소 탭 {#allowed-components-tab}

**허용된 구성 요소** 탭은 컨텐츠 작성자가 회전 구성 요소에 슬라이드로 추가할 수 있는 구성 요소를 정의하는 데 사용됩니다.

허용된 구성 요소 탭은 템플릿 편집기에서 레이아웃 컨테이너의 정책 및 속성을 정의할 때 동일한 이름의 탭과 동일한 방식으로 작동합니다.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)[

### 스타일 탭 {#styles-tab}

회전판 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

## Adobe 클라이언트 데이터 레이어 {#data-layer}

회전판 구성 요소는 [Adobe 클라이언트 데이터 계층을 지원합니다.](/help/developing/data-layer/overview.md)

---
title: 회전판 구성 요소
description: 회전판 구성 요소를 사용하면 컨텐츠 작성자가 회전하는 회전하는 회전판 안에 컨텐츠를 표시할 수 있습니다.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '1112'
ht-degree: 1%

---


# 회전판 구성 요소{#carousel-component}

핵심 구성 요소 회전판 구성 요소를 사용하면 컨텐츠 작성자가 탐색 가능한 회전판에 컨텐츠를 표시할 수 있습니다.

## 사용량 {#usage}

컨텐츠 작성자는 캐러셀 구성 요소를 사용하여 회전하는 슬라이드 회전하면서 컨텐츠를 구성합니다.

[편집 대화 상자](#edit-dialog)를 사용하면 컨텐츠 작성자가 여러 슬라이드를 만들고 이름을 지정하고 순서를 지정할 수 있을 뿐만 아니라 지연 시 자동 전환을 활성화할 수 있습니다. 템플릿 작성자는 [디자인 대화 상자](#design-dialog)를 사용하여 캐러셀에 추가할 수 있는 구성 요소를 정의하고 자동 전환을 활성화 또는 비활성화하며 스타일을 사용자 정의할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

회전판 구성 요소의 현재 버전은 v1이며, 2018년 10월 핵심 구성 요소 릴리스 2.2.0에 도입되었으며 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소 버전이 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

Carousel 구성 요소를 경험할 수 있을 뿐만 아니라 구성 옵션의 예 및 HTML 및 JSON 출력을 보려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_carousel)를 방문하십시오.

### 기술 세부 정보 {#technical-details}

회전판 구성 요소 [에 대한 최신 기술 문서는 GitHub](https://adobe.com/go/aem_cmp_tech_carousel_v1)에서 찾을 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)에서 확인할 수 있습니다.

## 편집 대화 상자 {#edit-dialog}

편집 대화 상자를 사용하면 내용 작성자가 슬라이드를 추가, 이름 변경 및 재배치할 수 있을 뿐만 아니라 자동 전환 설정을 정의할 수 있습니다.

### 항목 탭 {#items-tab}

![회전판 구성 요소의 편집 대화 상자 항목 탭](/help/assets/carousel-edit-items.png)

**추가** 단추를 사용하여 구성 요소 선택기를 열고 탭으로 추가할 구성 요소를 선택합니다. 한 번 추가되면 다음 열이 포함된 항목이 목록에 추가됩니다.

* **아이콘**  - 목록에서 쉽게 식별할 수 있도록 탭의 구성 요소 유형의 아이콘입니다. 전체 구성 요소 이름을 툴팁으로 보려면 마우스를 위에 놓으십시오.
* **설명**  - 탭의 텍스트로 사용되는 설명으로서, 탭에 대해 선택된 구성 요소의 이름에 기본값으로 설정됩니다.
* **삭제**  - 탭 구성 요소에서 탭을 삭제하려면 탭하거나 클릭합니다.
* **순서**  바꾸기 - 탭을 탭하거나 클릭하고 드래그하여 탭을 정렬합니다.

>[!TIP]
>
>편집 대화 상자가 전체 화면이 되도록 페이지의 뷰포트를 축소하면 **추가** 단추가 숨겨집니다. 구성 요소 브라우저에서 [을 드래그하고 페이지 편집기](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#inserting-a-component-from-the-components-browser)의 회전판 구성 요소에 드롭하여 구성 요소를 회전판 구성 요소에 추가할 수 있습니다.

### 속성 탭 {#properties-tab}

![회전판 구성 요소의 편집 대화 상자의 속성 탭](/help/assets/carousel-edit-properties.png)

내용 작성자는 **속성** 탭에서 슬라이드를 자동으로 전환하도록 설정할 수 있습니다.

* **슬라이드**  자동 전환 - 활성 상태가 되면 구성 요소는 지정된 지연 후 자동으로 다음 슬라이드로 이동합니다.
* **전환 지연**  - [자동 전환] 슬라이드를 선택하면 이 값을 사용하여 전환 간 지연 시간(밀리초)을 정의합니다.
* **마우스로 가리키면**  자동 일시 정지 사용 안 함 **-** [자동으로] 전환슬라이드쇼가 선택된 경우 커서가 회전판 위를 가리킬 때마다 캐러셀 전환이 자동으로 일시 중지됩니다. 전환이 일시 중지되지 않도록 이 옵션을 선택합니다.
* **ID**  - 이 옵션을 사용하면 HTML 및 데이터 레이어에서 구성 요소의 고유 식별자를 제어할  [수 있습니다](/help/developing/data-layer/overview.md).
   * 비워 두면 자동으로 고유 ID가 생성되며 결과 페이지를 검사하여 찾을 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID를 변경하면 CSS, JS 및 데이터 레이어 추적에 영향을 줄 수 있습니다.

>[!NOTE]
>
>**편집** 모드에서는 슬라이드 고급 컨트롤을 사용할 수 없습니다. 게시된 컨텐츠의 판독기로 회전판을 상호 작용하려면 [**미리 보기** 모드](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#preview-mode) 또는 **[게시됨으로 보기](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** 옵션을 사용합니다.
>
>**편집** 모드에서는 자동 고급 기능이 활성화되지 않습니다. **[게시됨으로 보기](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** 옵션을 사용하여 게시된 컨텐츠의 판독기로 자동 고급 기능을 표시합니다.

### 액세스 가능성 탭 {#accessibility-tab}

![회전판 구성 요소의 편집 대화 상자의 액세스 가능성 탭](/help/assets/carousel-edit-accessibility.png)

**액세스 가능성** 탭에서 구성 요소에 대한 [ARIA 액세스 가능성](https://www.w3.org/WAI/standards-guidelines/aria/) 레이블에 대해 값을 설정할 수 있습니다.

* **레이블**  - 구성 요소에 대한 ARIA 레이블 속성의 값입니다.

## 패널 {#select-panel} 선택

내용 작성자는 구성 요소 도구 모음의 **패널 선택** 옵션을 사용하여 편집할 다른 슬라이드로 변경할 수 있을 뿐만 아니라 슬라이드의 순서를 쉽게 재정렬할 수 있습니다.

![패널 아이콘 선택](/help/assets/select-panel-icon.png)

구성 요소 도구 모음에서 **패널 선택** 옵션을 선택하면 구성된 슬라이드가 드롭다운으로 표시됩니다.

* 목록은 슬라이드의 지정된 배열별로 정렬되며 번호 매기기에 반영됩니다.
* 슬라이드의 구성 요소 유형이 먼저 표시되고 슬라이드의 설명이 더 연한 글꼴로 표시됩니다.

![패널 선택](/help/assets/select-panel-popover.png)

* 드롭다운에서 항목을 탭하거나 클릭하면 편집기의 보기가 해당 슬라이드로 전환됩니다.
* 드래그하여 핸들을 사용하여 슬라이드의 순서를 제자리에서 변경할 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 사용하여 슬라이드 구성 요소에 슬라이드로 추가할 수 있는 구성 요소를 정의할 수 있고 자동 전환 기본값을 정의할 수 있으며 내용 작성자가 사용할 수 있는 사용자 정의 스타일을 정의할 수 있습니다.

### 속성 탭 {#properties-tab-1}

내용 작성자가 회전판 구성 요소를 페이지에 추가할 때 **속성** 탭은 슬라이드 전환의 기본 설정을 정의하는 데 사용됩니다.

![회전판 구성 요소의 디자인 대화 상자](/help/assets/carousel-design.png)

* **슬라이드**  자동 전환 - 컨텐츠 작성자가 회전판 구성 요소를 페이지에 추가할 때 기본적으로 회전판을 다음 슬라이드로 자동으로 이동하는 옵션이 활성화되는지 여부를 정의합니다.
* **전환 지연**  - 컨텐츠 작성자가 회전판 구성 요소를 페이지에 추가할 때 슬라이드 간 전환 지연의 기본값(밀리초)을 정의합니다.
* **마우스로 가리키면 자동 일시 정지**  사용 안 함 - 컨텐츠 작성자가 슬라이드 **를 자동으로 전환하는** 경우 자동 슬라이드 일시 정지 사용 안 함 옵션이 기본적으로 활성화되어 있는지 여부를 정의합니다.

### 허용된 구성 요소 탭 {#allowed-components-tab}

**허용된 구성 요소** 탭은 내용 작성자가 슬라이드 구성 요소에 추가할 수 있는 구성 요소를 정의하는 데 사용됩니다.

허용된 구성 요소 탭은 템플릿 편집기에서 레이아웃 컨테이너의 정책 및 속성을 정의할 때 같은 이름의 탭과 동일한 방식으로 작동합니다.[](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)

### 스타일 탭 {#styles-tab}

캐러셀 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

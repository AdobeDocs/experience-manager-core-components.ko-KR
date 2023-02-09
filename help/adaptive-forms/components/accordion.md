---
title: 적응형 양식 아코디언
description: 아코디언을 사용하여 길고 복잡한 양식을 더 작고 관리하기 쉬운 섹션으로 분할하여 구성하고 단순화합니다.
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '1768'
ht-degree: 4%

---

# 아코디언 구성 요소 {#accordion-component-adaptive-forms-core-component}

아코디언 코어 구성 요소를 사용하면 적응형 양식에서 확장 및 축소 가능한 섹션을 만들 수 있습니다. 긴 또는 복잡한 양식을 더 작고 관리하기 쉬운 섹션으로 분리하여 구성하고 단순화하는 데 종종 사용됩니다. 아코디언의 각 섹션은 일반적으로 헤더로 표시되며, 사용자가 클릭하여 해당 콘텐츠를 확장하거나 축소할 수 있습니다. 컨텐츠는 모든 핵심 구성 요소일 수 있습니다.

## 사용 {#usage}

다음을 포함하여 적응형 양식에 아코디언을 포함하는 것이 좋은 몇 가지 이유가 있습니다.

* **공간 저장**: 아코디언을 사용하면 양식의 섹션을 확장하거나 축소하여 모든 양식 필드를 한 번에 표시하는 데 필요한 공간을 줄일 수 있습니다.

* **탐색**: 아코디언을 사용하여 계층 탐색 구조를 만들 수 있으므로 사용자가 필요한 양식 필드를 쉽게 찾을 수 있습니다.

* **사용자 경험**: 아코디언을 사용하여 사용자가 양식 필드에 액세스하고 채울 수 있는 명확하고 직관적인 방법을 제공하여 양식을 보다 사용자에게 친숙한 형식으로 만들 수 있습니다.

* **긴 Forms**: 아코디온은 많은 정보를 한꺼번에 처리하려고 하지 않고 한 번에 한 섹션에 집중할 수 있도록 해주므로 긴 양식을 처리하는 데 이상적인 구성 요소입니다.

다음을 사용할 수 있습니다.

* 다음 [대화 상자 구성](#configure-dialog) 아코디언 구성 요소의 속성을 지정하려면

* 다음 [패널 팝업 선택](#select-panel-popover)  아코디언 패널의 순서를 정의하기 위해. 이렇게 하면 작성자가 패널이 표시되어야 하는 순서대로 패널을 정렬할 수 있습니다.

* Forms 작성자가 [디자인 대화 상자](#design-dialog). 예를 들어 작성자는 양식의 특정 필드 또는 섹션을 비활성화하도록 선택할 수 있습니다. 이러한 옵션을 사용하면 작성자가 양식의 디자인과 기능을 보다 강력하게 제어할 수 있으므로 조직의 특정 요구 사항에 맞는 양식을 쉽게 만들 수 있습니다.

구성 대화 상자, 선택 패널 팝업 및 디자인 대화 상자는 양식을 쉽게 작성할 수 있도록 빌드된 핵심 구성 요소의 일부이며 복잡한 양식을 만드는 효율적인 방법을 제공합니다.

## 버전 및 호환성 {#version-and-compatibility}


적응형 Forms 아코디언 코어 구성 요소는 코어 구성 요소 2.0.4의 일부로 2023년 2월에 출시되었습니다. 다음은 지원되는 모든 버전, AEM 호환성 및 해당 설명서 링크를 보여주는 표입니다.

|  |  |
|---|---|
| 구성 요소 버전 | AEM as a Cloud Service |
| --- | --- |
| v1 | 호환 가능 with<br>[릴리스 2.0.4](/help/versions.md) 나중에 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md) 문서.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## 기술 세부 사항 {#technical-details}

기술 설명서에서 아코디언 구성 요소에 대한 최신 정보를 [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/accordion/v1/accordion). 핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md).

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자에서 방문자의 아코디언 경험을 쉽게 사용자 지정할 수 있습니다. 또한 원활한 사용자 경험을 위해 아코디언 항목, 패널, 동작 및 모양을 쉽게 정의할 수 있습니다.

### 기본 탭 {#basic-tab}

![기본 탭](/help/adaptive-forms/assets/accordion_basictab.png)

* **이름** - 양식 및 규칙 편집기에서 고유한 이름으로 양식 구성 요소를 쉽게 식별할 수 있지만 이름에 공백이나 특수 문자가 포함되어 있으면 안 됩니다.

* **제목** - 제목 을 사용하면 양식의 구성 요소를 쉽게 식별할 수 있으며, 기본적으로 제목이 구성 요소 위에 표시됩니다. 제목을 추가하지 않으면 제목 텍스트 대신 구성 요소의 이름이 표시됩니다.

* **제목 숨기기** - 구성 요소의 제목을 숨기려면 옵션을 선택합니다.

* **개체의 데이터 줄바꿈** - &quot;Wrap data in an object&quot;를 선택하여 마법사의 필드 데이터를 JSON 개체 내에 넣습니다. 선택하지 않은 경우, 데이터 제출 JSON에는 마법사 필드에 대한 플랫 구조가 있습니다.

* **레이아웃** - 마법사에 고정 레이아웃(단순) 또는 유연한 레이아웃(응답형 그리드)을 사용할 수 있습니다. 단순 레이아웃은 모든 것을 제자리에 고정하고 응답형 그리드를 사용하면 필요에 따라 구성 요소의 위치를 조정할 수 있습니다. 예를 들어, 응답형 그리드를 사용하여 한 행의 양식에 &quot;이름&quot;, &quot;중간 이름&quot; 및 &quot;성&quot;을 정렬합니다.

* **바인딩 참조** - 바인딩 참조는 외부 데이터 소스에 저장되고 양식에 사용되는 데이터 요소에 대한 참조입니다. 바인딩 참조를 사용하면 데이터를 양식 필드에 동적으로 바인딩할 수 있으므로 폼에서 데이터 소스의 최신 데이터를 표시할 수 있습니다. 예를 들어 바인딩 참조를 사용하여 양식에 입력한 고객 ID를 기반으로 고객의 이름과 주소를 양식에 표시할 수 있습니다. 바인딩 참조를 사용하여 양식에 입력한 데이터로 데이터 소스를 업데이트할 수도 있습니다. 이러한 방식으로 AEM Forms을 사용하면 외부 데이터 소스와 상호 작용하는 양식을 만들어 데이터를 수집 및 관리하기 위한 원활한 사용자 경험을 제공할 수 있습니다.
* **구성 요소 숨기기** - 양식에서 구성 요소를 숨길 옵션을 선택합니다. 구성 요소는 규칙 편집기에서 계산에 사용하는 것과 같이 다른 목적으로 액세스할 수 있습니다. 이 기능은 사용자가 직접 보거나 볼 필요가 없는 정보를 저장해야 하는 경우 유용합니다.
* **구성 요소 비활성화** - 구성 요소를 비활성화하는 옵션을 선택합니다. 비활성화된 구성 요소는 최종 사용자가 활성 상태이거나 편집할 수 없습니다. 사용자는 필드의 값을 볼 수 있지만 수정할 수 없습니다. 구성 요소는 규칙 편집기에서 계산에 사용하는 것과 같이 다른 목적으로 액세스할 수 있습니다.

### 항목 탭 {#items-tab}

![항목 탭](/help/adaptive-forms/assets/accordion_itemstab.png)

추가 단추를 사용하면 구성 요소 선택 창에서 패널로 추가할 구성 요소를 선택할 수 있습니다. 구성 요소를 추가한 후 다음 옵션을 볼 수 있습니다.

* **아이콘** - 아이콘은 목록에서 패널의 구성 요소를 식별합니다. 아이콘 위로 마우스를 가져가면 전체 구성 요소 이름을 도구 설명으로 볼 수 있습니다.
* **설명** - 패널의 텍스트로 사용되는 설명입니다. 기본적으로 패널에 대해 구성 요소의 이름이 선택됩니다.
* **삭제** - 탭하거나 클릭하여 아코디언 구성 요소에서 패널을 삭제합니다.
* **재배열** - 탭하거나 클릭하고 드래그하여 패널의 순서를 재배열합니다.

### 도움말 컨텐츠 탭 {#help-content}

![도움말 콘텐츠 탭](/help/adaptive-forms/assets/accordion_helpcontent.png)

* **간단한 설명** - 간단한 설명은 특정 양식 필드의 용도에 대한 추가 정보나 설명을 제공하는 간단한 텍스트 설명입니다. 필드를 통해 사용자는 필드에 입력해야 하는 데이터 유형을 이해하고, 입력한 정보가 유효하고 원하는 기준을 충족하는지 확인하는 데 도움이 되는 지침이나 예를 제공할 수 있습니다. 기본적으로 짧은 설명은 숨겨집니다. 를 활성화합니다 **항상 짧은 설명 표시** 구성 요소 아래에 표시하는 옵션.

* **항상 짧은 설명 표시** - 구성 요소 아래에 짧은 설명을 표시하려면 옵션을 활성화합니다.

* **도움말 텍스트** - 도움말 텍스트는 사용자가 양식 필드를 올바르게 입력할 수 있도록 돕기 위해 제공하는 추가 정보 또는 지침을 나타냅니다. 사용자가 구성 요소 옆에 있는 도움말 아이콘(i)을 클릭하면 표시됩니다. 도움말 텍스트는 양식 필드의 레이블이나 자리 표시자 텍스트보다 더 자세한 정보를 제공하며 사용자가 필드의 요구 사항이나 제한 사항을 이해하는 데 도움이 되도록 설계되었습니다. 또한 양식 작성을 더 쉽고 정확하게 하기 위한 제안이나 예를 제공할 수 있습니다.

### 접근성 탭 {#accessibility}

![액세스 가능성 탭](/help/adaptive-forms/assets/accordion_accessibility.png)

설정 **접근성** 탭에서, 값들에 대해 설정됩니다. [ARIA 액세스 가능성](https://www.w3.org/WAI/standards-guidelines/aria/) 구성 요소의 레이블입니다. 화면 판독기 텍스트를 사용하는 데 다양한 옵션을 사용할 수 있습니다.

* **화면 판독기를 위한 텍스트** - 화면 판독기에 대한 텍스트는 시각 장애가 있는 사람이 사용하는 화면 판독기와 같은 보조 기술을 통해 특별히 읽을 수 있도록 만들어진 추가 텍스트를 나타냅니다. 이 텍스트는 양식 필드의 용도에 대한 오디오 설명을 제공하며 필드의 제목, 설명, 이름 및 관련 메시지(사용자 정의 텍스트)에 대한 정보를 포함할 수 있습니다. 화면 판독기 텍스트는 시각 장애가 있는 사용자를 비롯하여 모든 사용자가 양식에 액세스할 수 있도록 지원하고 양식 필드 및 해당 요구 사항을 완전히 이해할 수 있도록 해줍니다.


   * **사용자 정의 텍스트**: ARIA 액세스 가능성 레이블에 사용자 지정 텍스트를 사용하려면 이 옵션을 선택합니다. 이 옵션을 선택하면 사용자 정의 텍스트 대화 상자가 표시됩니다. 사용자 정의 텍스트 대화 상자에서 관련 정보를 추가할 수 있습니다.
   * **설명**: ARIA 액세스 가능성 레이블에 대한 설명을 사용하려면 이 옵션을 선택합니다.
   * **제목**: ARIA 액세스 가능성 레이블에 제목을 사용하려면 이 옵션을 선택합니다.
   * **이름**: ARIA 액세스 가능성 레이블의 이름을 사용하려면 이 옵션을 선택합니다.
   * **없음**: ARIA 액세스 가능성 레이블에 대해 를 추가하지 않으려면 이 옵션을 선택합니다.

<!--

### Properties Tab {#properties-tab}

![Properties tab of the edit dialog of the Accordion Component](/help/assets/accordion-edit-properties.png)

*   **Single item expansion** - When selected, this option forces a single accordion item to be expanded at a time. Expanding one item will then collapse all others.
*   **Expanded items** - This option defines the items that are expanded by default when the page is loaded.
    * When **Single item expansion** is selected, one panel must be selected. By default the first panel is selected.
    * When **Single item expansion** is not selected, this option is a multi-select and is optional.
*   **ID** - This option allows to control the unique identifier of the component in the HTML and in the [Data Layer](/help/developing/data-layer/overview.md).
    * If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
    * If an ID is specified, it is the responsibility of the author to make sure that it is unique.
    * Changing the ID can have an impact on CSS, JS and Data Layer tracking.

## Select Panel Popover {#select-panel-popover}

The **Select Panel** option (![Select panel icon](/help/assets/select-panel-icon.png)) on the component toolbar enables content authors to modify the panels in an accordion with ease. By selecting this option, the author can switch to a different panel for editing and rearrange the order of the panels in the accordion. The configured panels will be displayed in a drop-down menu for the author to choose from. This feature optimizes the editing process and makes it user-friendly for content authors.

![Select panel popover](/help/assets/select-panel-popover.png)


* The panels are displayed in a numbered list, reflecting the assigned arrangement.
* Each panel is listed with its component type in bold, followed by a brief description in lighter font.
* By clicking or tapping on a panel in the drop-down, you can easily switch the view in the editor to that specific panel.
* To rearrange the panels, simply use the drag handles to move them into the desired order. -->

## 디자인 대화 상자 {#design-dialog}

디자인 대화 상자를 사용하면 템플릿 작성자가 기본적으로 표시되는 방식을 제어할 수 있습니다. 응용 Forms 아코디언 구성 요소의 경우 다음을 설정할 수 있습니다.

* 허용 및 기본값으로 설정되는 HTML 제목 요소의 유형(예: H1, H2, H3 등)
* 양식 작성자가 적응형 Forms 편집기의 아코디언에 추가할 수 있는 핵심 구성 요소
* 응용 Forms 편집기에서 아코디언 구성 요소의 속성 대화 상자에 적용할 수 있는 스타일(CSS 클래스)에 대한 단순 이름.

따라서 양식을 보다 간단하고 효율적으로 만들고 사용자 지정하는 과정을 수행할 수 있습니다.

### 속성 탭 {#properties-tab-design}

속성 탭에서는 템플릿 작성자가 양식 작성자에 대한 기본 및 허용된 HTML 제목 요소를 설정할 수 있습니다.

![디자인 대화 상자 속성 탭](/help/assets/accordion-design-properties.png)

* **허용된 제목 요소**: 템플릿 작성자가 아코디언에 사용할 수 있는 머리글 요소를 선택할 수 있는 여러 옵션이 있는 드롭다운 목록입니다.

* **기본 제목 요소**: 드롭다운 목록은 아코디언 구성 요소의 기본 제목 요소를 설정합니다.

### 허용된 구성 요소 탭 {#allowed-components-tab}

다음 **허용된 구성 요소** 템플릿 편집기에서 적응형 Forms 편집기에서 아코디언 구성 요소의 패널에 항목으로 추가할 수 있는 구성 요소를 설정할 수 있습니다.

### 스타일 탭 {#styles-tab}

디자인 대화 상자는 구성 요소의 CSS 스타일을 정의하고 관리하는 데 사용됩니다. 응용 Forms 아코디언 코어 구성 요소는 AEM을 지원합니다 [스타일 시스템](/help/get-started/authoring.md#component-styling).

**기본 CSS 클래스**: 아코디언 구성 요소에 기본 CSS 클래스를 제공할 수 있습니다.

**허용된 스타일**: 스타일을 나타내는 이름과 CSS 클래스를 제공하여 스타일을 정의할 수 있습니다. 예를 들어 &quot;bold text&quot;라는 스타일을 만들고 CSS 클래스 &quot;font-weight: 굵게. 적응형 Forms 편집기에서 적응형 양식에 이러한 스타일을 사용하거나 적용할 수 있습니다. 스타일을 적용하려면 적응형 Forms 편집기에서 스타일을 적용할 구성 요소를 선택하고 속성 대화 상자로 이동한 다음, **스타일** 드롭다운 목록. 스타일을 업데이트하거나 수정해야 하는 경우, 디자인 대화 상자로 돌아가서 스타일 탭에서 스타일을 업데이트하고 변경 사항을 저장하면 됩니다.


<!-- 

The design dialog allows the template author to define the options available to the content author who uses the Accordion Component and the defaults set when placing the Accordion Component.


### Properties Tab {#properties-tab-design}

![Design dialog properties tab](/help/assets/accordion-design-properties.png)

* **Allowed Heading Elements** - This multi-select drop-down defines the accordion item heading HTML elements that are allowed to be selected by an author.
* **Default Heading Element** - This drop-down defines the default accordion item heading HTML element.

### Allowed Components Tab {#allowed-components-tab}

The **Allowed Components** tab is used to define which components can be added as items to panels in the Accordion Component by the content author.

The Allowed Components tab functions in the same way as the tab of the same name when [defining the policy and properties of a Layout Container in the Template Editor.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html#editing-a-template-layout-template-author)

### Styles Tab {#styles-tab}

The Accordion Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

## Adobe Client Data Layer {#data-layer}

The Accordion Component supports the [Adobe Client Data Layer.](/help/developing/data-layer/overview.md)

-->





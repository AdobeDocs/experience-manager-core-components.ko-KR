---
title: 적응형 양식 아코디언
description: 아코디언을 사용하여 길거나 복잡한 양식을 더 작고 관리하기 쉬운 섹션으로 나누어 구성하고 단순화합니다.
role: Architect, Developer, Admin, User
exl-id: 0ed38eee-fc22-4708-82eb-3fb1839b1ff2
source-git-commit: e0ed415bd7f45fdca6fbbb8ba409604d9e82a647
workflow-type: ht
source-wordcount: '2202'
ht-degree: 100%

---

# 아코디언 구성 요소 {#accordion-component-adaptive-forms-core-component}

아코디언 구성 요소를 사용하면 적응형 양식에서 확장 및 축소 가능한 섹션을 만들 수 있습니다. 아코디언 구성 요소는 길거나 복잡한 양식을 더 작고 관리하기 쉬운 섹션으로 나누어 구성하고 단순화하는 데 사용됩니다. 아코디언의 각 섹션은 일반적으로 헤더로 표시되며 사용자는 헤더를 클릭하여 해당 콘텐츠를 확장하거나 축소할 수 있습니다. 콘텐츠는 모든 핵심 구성 요소가 될 수 있습니다.

![예](/help/adaptive-forms/assets/example-accordion.png)

## 사용 {#usage}

적응형 양식에 아코디언을 포함하는 것이 유익한 몇 가지 이유는 다음과 같습니다.

- **공간 절약**: 아코디언을 사용하면 사용자가 양식 섹션을 확장하고 축소할 수 있으므로 모든 양식 필드를 한 번에 표시하는 데 필요한 공간을 절약할 수 있습니다.

- **탐색**: 아코디언을 사용하여 계층형 탐색 구조를 만들 수 있으므로 필요한 양식 필드를 더 쉽게 찾을 수 있습니다.

- **사용자 경험**: 아코디언을 사용하면 사용자가 명확하고 직관적으로 양식 필드에 액세스하고 채울 수 있으므로 양식을 보다 사용자 친화적으로 만들 수 있습니다.

- **긴 양식**: 아코디언은 긴 양식을 처리하는 데 이상적인 구성 요소입니다. 한 번에 많은 정보를 처리하지 않고 한 번에 한 섹션에 집중할 수 있기 때문입니다.

다음과 같은 기능을 사용할 수 있습니다.

- [구성 대화 상자](#configure-dialog): 아코디언 구성 요소의 속성을 지정합니다.

- [패널 선택 팝오버](#select-panel-popover): 아코디언 패널의 순서를 정의합니다. 이를 통해 작성자는 패널을 표시되어야 하는 순서대로 정렬할 수 있습니다.

- [디자인 대화 상자](#design-dialog): 양식 작성자는 특정 기능을 활성화 또는 비활성화하는 옵션을 사용할 수 있습니다. 예를 들어 작성자는 양식의 특정 필드나 섹션을 비활성화하도록 선택할 수 있습니다. 이러한 옵션을 통해 작성자는 양식의 디자인과 기능을 더 잘 제어할 수 있으므로 조직의 특정 요구 사항에 맞는 양식을 더 쉽게 만들 수 있습니다.

구성 대화 상자, 패널 선택 팝오버 및 디자인 대화 상자는 모두 양식을 손쉽게 작성할 수 있도록 돕고 복잡한 양식을 만드는 효율적인 방법을 제공하기 위해 구축된 핵심 구성 요소의 일부입니다.

## 버전 및 호환성 {#version-and-compatibility}


적응형 양식 아코디언 핵심 구성 요소는 핵심 구성 요소 2.0.4의 일부로 2023년 2월에 릴리스되었습니다. 다음 표에서는 지원되는 모든 버전, AEM 호환성 및 해당 문서에 대한 링크를 보여 줍니다.

|  |  |
|---|---|
| 구성 요소 버전 | AEM as a Cloud Service |
| --- | --- |
| v1 | 호환 가능 <br>[2.0.4](/help/versions.md) 및 이후 릴리스 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md) 문서를 참조하십시오.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## 기술 세부 정보 {#technical-details}

아코디언 구성 요소에 대한 최신 정보는 [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/accordion/v1/accordion)의 기술 설명서에서 확인할 수 있습니다. 핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 확인하십시오.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자를 사용하여 방문자를 위한 아코디언 경험을 손쉽게 사용자 정의할 수 있습니다. 원활한 사용자 경험을 위해 아코디언 항목, 패널, 동작 및 모양을 간편하게 정의할 수도 있습니다.

### 기본 탭 {#basic-tab}

![기본 탭](/help/adaptive-forms/assets/acc-basic.png)

- **이름** - 양식과 규칙 편집기 모두에서 고유한 이름으로 양식 구성 요소를 쉽게 식별할 수 있습니다. 단, 이름에는 공백이나 특수 문자가 포함되어서는 안 됩니다.

- **제목** - 제목을 사용하면 양식에서 구성 요소를 쉽게 식별할 수 있으며, 기본적으로 제목은 구성 요소 상단에 나타납니다. 제목을 추가하지 않으면 제목 텍스트 대신 구성 요소의 이름이 표시됩니다.

- **제목 숨기기** - 구성 요소의 제목을 숨기려면 이 옵션을 선택합니다.

- **양식 제출 시 하위 구성 요소의 데이터 그룹화(오브젝트에 데이터 래핑)** - 이 옵션을 선택하면 하위 구성 요소의 데이터가 상위 구성 요소의 JSON 오브젝트 내에 중첩됩니다. 그러나 이 옵션을 선택하지 않으면 제출된 JSON 데이터는 상위 구성 요소에 대한 오브젝트가 없는 평면 구조를 갖습니다. 예:

   - 이 옵션을 선택하면 하위 구성 요소(예: 도로 번호, 구/군/시 및 우편 번호)의 데이터가 상위 구성 요소(주소) 내에 JSON 오브젝트로 중첩됩니다. 이렇게 하면 계층 구조가 생성되고 데이터는 상위 구성 요소 아래에 구성됩니다.

     제출된 데이터의 구조:

     ```JSON
     { "Address":
     
     { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
     
     }
     ```

   - 이 옵션을 선택하지 않으면 제출된 JSON 데이터는 상위 구성 요소(주소)에 대한 오브젝트가 없는 평면 구조를 갖습니다. 모든 데이터는 계층 구조 없이 동일한 수준에 있습니다.


     제출된 데이터의 구조:

     ```JSON
        { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
     ```

- **레이아웃** - 마법사에 대해 고정 레이아웃(단순) 또는 유연한 레이아웃(반응형 격자)을 설정할 수 있습니다. 단순 레이아웃은 모든 요소를 제자리에 고정하고 반응형 격자를 사용하면 필요에 맞게 구성 요소의 위치를 조정할 수 있습니다. 예를 들어 반응형 격자를 사용하여 양식의 “이름”, “중간 이름” 및 “성”을 단일 행에 정렬할 수 있습니다.

- **바인드 참조** - 바인드 참조는 외부 데이터 소스에 저장되고 양식에서 사용되는 데이터 요소에 대한 참조입니다. 바인드 참조를 사용하면 데이터를 양식 필드에 동적으로 바인딩하여 양식이 데이터 소스의 최신 데이터를 표시하도록 할 수 있습니다. 예를 들어 바인드 참조를 사용하여 양식에 입력된 고객의 ID를 기반으로 고객의 이름과 주소를 양식에 표시할 수 있습니다. 바인드 참조를 사용하여 양식에 입력된 데이터로 데이터 소스를 업데이트할 수도 있습니다. 이러한 방식으로 AEM Forms를 사용하면 외부 데이터 소스와 상호 작용하는 양식을 만들어 데이터 수집 및 관리를 위한 원활한 사용자 경험을 제공할 수 있습니다.

- **구성 요소 숨기기** - 양식에서 구성 요소를 숨기려면 이 옵션을 선택합니다. 구성 요소는 다른 용도로(예: 규칙 편집기에서 계산에 사용) 계속 액세스할 수 있습니다. 구성 요소 숨기기는 사용자가 보거나 직접 변경할 필요가 없는 정보를 저장해야 할 때 유용합니다.

- **구성 요소 비활성화** - 구성 요소를 비활성화하려면 이 옵션을 선택합니다. 비활성화된 구성 요소는 활성 상태가 아니므로 최종 사용자가 편집할 수 없습니다. 사용자는 필드 값을 볼 수 있지만 수정할 수는 없습니다. 구성 요소는 다른 용도로(예: 규칙 편집기에서 계산에 사용) 계속 액세스할 수 있습니다.

### 아코디언 반복 {#repeat-accordion}

![repeat-accordion](/help/adaptive-forms/assets/repeat-accordion.png)

반복 옵션을 사용하여 아코디언 패널과 해당 하위 구성 요소를 복제하고, 최소 및 최대 반복 횟수를 정의하고, 양식 내에서 유사한 섹션을 손쉽게 복제할 수 있습니다. 아코디언 구성 요소와 상호 작용하고 설정에 액세스할 때 다음 옵션이 표시됩니다.

- **아코디언이 반복 가능하도록 설정**: 사용자가 반복 기능을 활성화 또는 비활성화할 수 있는 토글 기능입니다.
- **최소 반복**: 아코디언 패널을 반복할 수 있는 최소 횟수를 설정합니다. 값이 0이면 아코디언 패널이 반복되지 않음을 나타냅니다. 기본값은 0입니다.
- **최대 반복**: 아코디언 패널을 반복할 수 있는 최대 횟수를 설정합니다. 기본적으로 이 값은 무제한입니다.

아코디언 내에서 반복 가능한 섹션을 효율적으로 관리하려면 [반복 가능한 섹션이 있는 양식 만들기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html) 문서에 기재되어 있는 단계를 따르십시오.

### 항목 탭 {#items-tab}

![항목 탭](/help/adaptive-forms/assets/acc-items.png)

[추가] 버튼을 사용하면 구성 요소 선택 창에서 패널로 추가할 구성 요소를 선택할 수 있습니다. 구성 요소를 추가하면 다음 옵션이 표시됩니다.

- **아이콘** - 목록에서 패널 구성 요소를 식별하는 아이콘입니다. 아이콘 위에 마우스를 가져다 대면 전체 구성 요소 이름을 툴팁으로 조회할 수 있습니다.
- **설명** - 패널의 텍스트로 사용되는 설명입니다. 기본적으로 구성 요소의 이름이 패널에 대해 선택되어 있습니다.
- **삭제** - 탭하거나 클릭하여 아코디언 구성 요소에서 패널을 삭제합니다.
- **재배열** - 패널의 순서를 재배열하려면 탭하거나 클릭하고 드래그합니다.

### 도움말 콘텐츠 탭 {#help-content}

![도움말 콘텐츠 탭](/help/adaptive-forms/assets/acc-helpcontent.png)

- **간단한 설명** - 간단한 설명은 특정 양식 필드의 용도에 대한 추가 정보 또는 설명을 제공하는 간단한 텍스트 설명입니다. 사용자가 필드에 입력해야 하는 데이터 유형을 이해하는 데 도움이 되며 입력된 정보가 유효하고 원하는 기준을 충족하는지 확인하는 데 도움이 되는 지침 또는 예시를 제공할 수 있습니다. 기본적으로 간단한 설명은 숨겨진 상태로 유지됩니다. **간단한 설명 항상 표시** 옵션을 활성화하여 구성 요소 아래에 표시할 수 있습니다.

- **간단한 설명 항상 표시** - 이 옵션을 활성화하여 구성 요소 아래에 간단한 설명을 표시할 수 있습니다.

- **도움말 텍스트** - 도움말 텍스트는 양식 필드를 올바르게 작성하는 데 도움이 되도록 사용자에게 제공되는 추가 정보 또는 지침을 나타냅니다. 구성 요소 옆에 있는 도움말 아이콘(i)을 클릭하면 표시됩니다. 도움말 텍스트는 양식 필드의 레이블이나 플레이스홀더 텍스트보다 더 자세한 정보를 제공하며 사용자가 필드의 요구 사항이나 제한 사항을 이해하는 데 도움이 되도록 설계되었습니다. 또한 양식을 보다 쉽고 정확하게 작성할 수 있도록 제안이나 예시를 제공할 수도 있습니다.

### 접근성 탭 {#accessibility}

![접근성 탭](/help/adaptive-forms/assets/acc-accessisbilty.png)

**접근성** 탭에는 구성 요소에 대한 [ARIA 접근성](https://www.w3.org/WAI/standards-guidelines/aria/) 레이블에 값이 설정되어 있습니다. 다양한 옵션을 통해 화면 판독기용 텍스트를 사용할 수 있습니다.

- **화면 판독기용 텍스트** - 화면 판독기용 텍스트는 시각 장애인이 사용하는 화면 판독기와 같은 보조 기술로 읽을 수 있도록 특별히 고안된 추가 텍스트를 나타냅니다. 이 텍스트는 양식 필드의 용도에 대한 오디오 설명을 제공하며, 여기에는 필드의 제목, 설명, 이름 및 관련 메시지(사용자 정의 텍스트)에 대한 정보가 포함될 수 있습니다. 화면 판독기 텍스트는 시각 장애가 있는 사용자를 포함한 모든 사용자가 양식에 액세스할 수 있도록 돕고 양식 필드 및 해당 요구 사항을 완전히 이해할 수 있도록 합니다.


   - **사용자 정의 텍스트**: ARIA 접근성 레이블에 사용자 정의 텍스트를 사용하려면 이 옵션을 선택합니다. 이 옵션을 선택하면 사용자 정의 텍스트 대화 상자가 표시됩니다. 사용자 정의 텍스트 대화 상자에서 관련 정보를 추가할 수 있습니다.
   - **설명**: ARIA 접근성 레이블에 설명을 사용하려면 이 옵션을 선택합니다.
   - **제목**: ARIA 접근성 레이블에 제목을 사용하려면 이 옵션을 선택합니다.
   - **이름**: ARIA 접근성 레이블에 이름을 사용하려면 이 옵션을 선택합니다.
   - **없음**: ARIA 접근성 레이블에 아무 것도 추가하지 않으려면 이 옵션을 선택합니다.

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

디자인 대화 상자를 사용하면 템플릿 작성자가 요소들이 기본적으로 표시되는 방식을 제어할 수 있습니다. 적응형 양식 아코디언 구성 요소의 경우 다음과 같은 옵션을 설정할 수 있습니다.

- 허용되고 기본값으로 설정된 HTML 제목 요소의 유형 (예: H1, H2, H3 등)
- 양식 작성자가 적응형 양식 편집기에서 아코디언에 추가할 수 있는 핵심 구성 요소
- 적응형 양식 편집기에서 아코디언 구성 요소의 속성 대화 상자에 적용할 수 있는 스타일(CSS 클래스)의 간단한 이름

이렇게 하면 양식을 만들고 사용자 정의하는 프로세스를 보다 간단하고 효율적으로 만들 수 있습니다.

### 속성 탭 {#properties-tab-design}

[속성] 탭을 사용하면 템플릿 작성자가 양식 작성자의 기본 및 허용된 HTML 제목 요소를 설정할 수 있습니다.

![디자인 대화 상자 속성 탭](/help//adaptive-forms/assets/accordion-design-properties.png)

- **허용된 제목 요소**: 템플릿 작성자가 양식 작성자가 아코디언에 사용할 수 있는 제목 요소를 선택할 수 있도록 하는 여러 옵션을 제공하는 드롭다운 목록입니다.

- **기본 제목 요소** - 아코디언 구성 요소의 기본 제목 요소를 설정하는 드롭다운 목록입니다.

### 허용된 구성 요소 탭 {#allowed-components-tab}

![디자인 대화 상자 허용된 구성 요소 탭](/help//adaptive-forms/assets/accordion-allowed-components.png)

**허용된 구성 요소** 탭을 사용하면 템플릿 편집기에서 적응형 양식 편집기의 아코디언 구성 요소 패널에 항목으로 추가할 수 있는 구성 요소를 설정할 수 있습니다.

### 스타일 탭 {#styles-tab}

![디자인 대화 상자 스타일 탭](/help/adaptive-forms/assets/accordion-styles-tab.png)

디자인 대화 상자는 구성 요소의 CSS 스타일을 정의하고 관리하는 데 사용됩니다. 적응형 양식 아코디언 핵심 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

- **기본 CSS 클래스**: 아코디언 구성 요소에 기본 CSS 클래스를 제공할 수 있습니다.

- **허용된 스타일**: 이름과 스타일을 나타내는 CSS 클래스를 제공하여 스타일을 정의할 수 있습니다. 예를 들어 “bold text”라는 스타일을 만들고 “font-weight: bold”라는 CSS 클래스를 제공할 수 있습니다. 적응형 양식 편집기에서 이러한 스타일을 적응형 양식에 사용하거나 적용할 수 있습니다. 스타일을 적용하려면 적응형 양식 편집기에서 스타일을 적용할 구성 요소를 선택하고 속성 대화 상자로 이동한 다음 **스타일** 드롭다운 목록에서 원하는 스타일을 선택합니다. 스타일을 업데이트하거나 수정해야 하는 경우 디자인 대화 상자로 돌아가서 스타일 탭에서 스타일을 업데이트하고 변경 내용을 저장하면 됩니다.

### 사용자 정의 속성

![아코디언 사용자 정의 속성 탭](/help/adaptive-forms/assets/accordion-custom-properties-tab.png)

사용자 정의 속성을 사용하면 양식 템플릿을 사용하여 사용자 정의 속성(키-값 쌍)을 적응형 양식 핵심 구성 요소에 연결할 수 있습니다. 사용자 정의 속성은 구성 요소의 헤드리스 렌디션에서 속성 섹션에 반영됩니다. 사용자 정의 속성 값에 따라 조정되는 동적 양식 동작을 만들 수 있습니다. 예를 들어 개발자는 모바일, 데스크탑 또는 웹 플랫폼을 위한 헤드리스 양식 구성 요소의 다양한 표현을 디자인하여 다양한 디바이스에서 사용자 경험을 크게 향상시킬 수 있습니다.

- **그룹 이름**: 사용자 정의 속성 그룹을 식별하기 위해 이름을 제공할 수 있습니다. 여러 사용자 정의 속성 그룹을 추가, 삭제 또는 재배열할 수 있습니다. 사용자 정의 속성 그룹을 추가하면 다음 옵션이 표시됩니다.

   - **키-값 쌍**: 각 사용자 정의 속성 그룹의 **추가** 버튼을 클릭하여 여러 사용자 정의 속성 이름과 사용자 정의 속성 값을 추가할 수 있습니다.

   - **삭제**: 사용자 정의 속성 이름과 사용자 정의 속성 값을 탭하거나 클릭하여 삭제할 수 있습니다.

   - **재배열**: 사용자 정의 속성 이름과 사용자 정의 속성 값을 누르거나 클릭하고 드래그하면 순서를 재배열할 수 있습니다.

## 관련 문서 {#related-articles}

{{more-like-this}}

## 추가 참조 {#see-also}

{{see-also}}
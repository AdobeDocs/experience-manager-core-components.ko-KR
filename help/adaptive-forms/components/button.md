---
title: 적응형 양식 핵심 구성 요소 - 버튼
description: 적응형 양식 버튼 핵심 구성 요소를 사용 또는 사용자 정의합니다.
role: Architect, Developer, Admin, User
exl-id: cb75929b-8c86-49d1-b51a-368f5b80b1a9
source-git-commit: 732efc9ed450aa31078ecaad65c0c306679fe97e
workflow-type: ht
source-wordcount: '1660'
ht-degree: 100%

---

# 버튼 구성 요소 {#button-component-adaptive-forms-core-component}

적응형 양식의 버튼은 사용자가 클릭하여 작업을 시작할 수 있는 UI 요소입니다. 버튼 요소를 사용하여 양식을 제출하거나, 양식을 재설정하거나, 다른 작업을 수행(예: 다른 페이지로 이동 또는 사용자 정의 코드 트리거)할 수 있습니다. 버튼은 버튼 핵심 구성 요소를 사용하여 만들 수 있습니다.

적응형 양식 규칙 편집기를 사용하면 버튼 구성 요소에 다양한 작업을 설정할 수 있습니다. 이러한 작업에는 웹 사이트 열기, 양식 구성 요소 표시 또는 숨기기, 패널 또는 구성 요소 인스턴스 추가, 양식 제출 또는 재설정 등이 포함됩니다.

적응형 양식은 [제출 버튼](/help/adaptive-forms/components/submit-button.md)과 [재설정 버튼](/help/adaptive-forms/components/reset-button.md)을 위한 별도의 구성 요소를 갖추고 있어 사용자가 편리하게 양식을 제출하거나 재설정할 수 있습니다. 버튼 구성 요소는 특정 요구 사항에 따라 이러한 작업을 실행하도록 유연하게 구성할 수 있습니다.

사용자는 적응형 양식 규칙 편집기를 사용하여 버튼 구성 요소에 대해 지원되는 전체 작업 목록에 액세스할 수 있습니다. 규칙 편집기를 사용하면 버튼을 클릭할 때, 양식이 로드될 때 또는 필드 값이 변경될 때와 같은 다양한 이벤트에 의해 트리거되는 규칙을 만들 수 있습니다. 그런 다음 이러한 규칙을 사용하여 구성 요소 표시 또는 숨기기, 필드 값 설정 또는 양식 제출과 같은 다양한 작업을 수행할 수 있습니다.

**예**

![버튼 예](/help/adaptive-forms/assets/example-button.png)

## 사용 {#reasons-to-use-button}

적응형 양식에 버튼을 포함하는 것이 유익한 몇 가지 이유는 다음과 같습니다.

- **양식 제출**: 버튼은 일반적으로 양식을 제출하는 데 사용되며, 이를 통해 사용자가 처리를 위해 서버에 입력한 데이터를 전송할 수 있습니다.

- **양식 재설정**: 버튼을 사용하여 양식을 재설정하여 사용자가 입력한 모든 데이터를 지울 수도 있습니다.

- **탐색**: 버튼을 사용하여 양식의 다른 섹션 또는 웹 사이트의 다른 페이지 사이를 탐색할 수 있습니다.

- **이벤트 처리**: 버튼을 사용하여 웹 사이트 열기, 구성 요소 표시/숨기기, 버튼에 패널 또는 구성 요소 인스턴스 추가와 같은 다양한 이벤트를 트리거할 수 있습니다.

- **상호 작용**: 버튼을 사용하여 대화형 양식을 만들 수 있습니다. 예를 들어 버튼을 사용하여 모달 대화 상자를 열거나 양식 섹션을 전환할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

적응형 양식 버튼 핵심 구성 요소는 Cloud Service의 핵심 구성 요소 2.0.4 및 AEM 6.5.16.0 Forms 이상의 핵심 구성 요소 1.1.12 일부로 2023년 2월에 릴리스되었습니다. 다음 표에서는 지원되는 모든 버전, AEM 호환성 및 해당 문서에 대한 링크를 보여 줍니다.

| 구성 요소 버전 | AEM as a Cloud Service | AEM 6.5.16.0 Forms 이상 |
|---|---|---|
| v1 | <br>[릴리스 2.0.4](/help/adaptive-forms/version.md) 이상 버전과 호환 가능 | <br>[릴리스 1.1.12](/help/adaptive-forms/version.md) 이상과 호환합니다(2.0.0 이전 버전). |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/adaptive-forms/version.md) 문서를 참조하십시오.


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion_kr). -->

## 기술 세부 정보 {#technical-details}

적응형 양식 버튼 핵심 구성 요소에 대한 최신 정보는 [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/button/v1/button)의 기술 설명서에서 확인할 수 있습니다. 핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 확인하십시오.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자를 사용하여 방문자를 위한 버튼 경험을 손쉽게 사용자 정의할 수 있습니다. 버튼 속성을 간편하게 정의하여 원활한 사용자 경험을 제공할 수도 있습니다.

### 기본 탭 {#basic-tab}

![기본 탭](/help/adaptive-forms/assets/button_basictab.png)

- **이름** - 양식과 규칙 편집기 모두에서 고유한 이름으로 양식 구성 요소를 쉽게 식별할 수 있습니다. 단, 이름에는 공백이나 특수 문자가 포함되어서는 안 됩니다.

- **제목** - 제목을 사용하면 양식에서 구성 요소를 쉽게 식별할 수 있으며, 기본적으로 제목은 구성 요소 상단에 나타납니다. 제목을 추가하지 않으면 제목 텍스트 대신 구성 요소의 이름이 표시됩니다.

- **제목에 대해 서식 있는 텍스트 허용** - 이 기능을 사용하면 사용자가 굵게, 기울임꼴, 밑줄 친 텍스트, 다양한 글꼴, 글꼴 크기, 색상, 추가 옵션과 같은 기능을 통합해 일반 텍스트 제목의 서식을 지정하여 시각적 표현 및 사용자 정의를 향상할 수 있습니다. 더 큰 유연성과 창의적인 제어 기능으로 문서, 웹 사이트 또는 애플리케이션 내에서 제목을 돋보이게 할 수 있습니다.\
  **제목에 대해 서식 있는 텍스트 허용** 확인란을 선택하면 구성 요소 제목의 스타일을 지정할 수 있는 서식 지정 옵션이 표시됩니다. 사용 가능한 모든 서식 옵션에 액세스하려면 ![전체 화면 아이콘](/help/adaptive-forms/assets/fullscreen-icon.png) 탭을 클릭하면 됩니다.

  ![서식 있는 텍스트 지원](/help/adaptive-forms/assets/richtext-support-title.png)

- **바인드 참조** - 바인드 참조는 외부 데이터 소스에 저장되고 양식에서 사용되는 데이터 요소에 대한 참조입니다. 바인드 참조를 사용하면 데이터를 양식 필드에 동적으로 바인딩하여 양식이 데이터 소스의 최신 데이터를 표시하도록 할 수 있습니다. 예를 들어 바인드 참조를 사용하여 양식에 입력된 고객의 ID를 기반으로 고객의 이름과 주소를 양식에 표시할 수 있습니다. 바인드 참조를 사용하여 양식에 입력된 데이터로 데이터 소스를 업데이트할 수도 있습니다. 이러한 방식으로 AEM Forms를 사용하면 외부 데이터 소스와 상호 작용하는 양식을 만들어 데이터 수집 및 관리를 위한 원활한 사용자 경험을 제공할 수 있습니다.

<!--   **Document of Record bind reference** - This option allows you to associate an Adaptive Form field with Document of Record field. When user enters any value in a linked field of an Adaptive Form that value also appears in the linked field of the corresponding Document of Record. For example, a Document of Record bind reference can be used to display a customer's name and address in a Document of Record, based on the customer's ID entered into the form. In this way, AEM Forms enables you to generate Document of Record and offers a seamless user experience for collecting and managing data.-->

- **언바운드 양식 요소로 표시**: 어떤 스키마에도 연결되지 않은 양식 필드를 구성하려면 이 옵션을 선택합니다. 이 옵션을 사용하면 데이터 소스를 업데이트하지 않고도 데이터를 저장할 수 있습니다. 또한 표준 데이터베이스 통합과 별도로 사용자 정의 방식으로 데이터를 처리할 수 있습니다.
- **구성 요소 숨기기** - 양식에서 구성 요소를 숨기려면 이 옵션을 선택합니다. 구성 요소는 다른 용도로(예: 규칙 편집기에서 계산에 사용) 계속 액세스할 수 있습니다. 구성 요소 숨기기는 사용자가 보거나 직접 변경할 필요가 없는 정보를 저장해야 할 때 유용합니다.
- **구성 요소 비활성화** - 구성 요소를 비활성화하려면 이 옵션을 선택합니다. 비활성화된 구성 요소는 활성 상태가 아니므로 최종 사용자가 편집할 수 없습니다. 사용자는 필드 값을 볼 수 있지만 수정할 수는 없습니다. 구성 요소는 다른 용도로(예: 규칙 편집기에서 계산에 사용) 계속 액세스할 수 있습니다.

<!--   **Read-only** - Select the option to make the component non-editable. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.-->

### 도움말 콘텐츠 탭 {#help-content}

![도움말 콘텐츠 탭](/help/adaptive-forms/assets/button_helptab.png)

- **간단한 설명** - 간단한 설명은 특정 양식 필드의 용도에 대한 추가 정보 또는 설명을 제공하는 간단한 텍스트 설명입니다. 사용자가 필드에 입력해야 하는 데이터 유형을 이해하는 데 도움이 되며 입력된 정보가 유효하고 원하는 기준을 충족하는지 확인하는 데 도움이 되는 지침 또는 예시를 제공할 수 있습니다. 기본적으로 간단한 설명은 숨겨진 상태로 유지됩니다. **간단한 설명 항상 표시** 옵션을 활성화하여 구성 요소 아래에 표시할 수 있습니다.

- **간단한 설명 항상 표시** - 이 옵션을 활성화하여 구성 요소 아래에 간단한 설명을 표시할 수 있습니다.

- **도움말 텍스트** - 도움말 텍스트는 양식 필드를 올바르게 작성하는 데 도움이 되도록 사용자에게 제공되는 추가 정보 또는 지침을 나타냅니다. 구성 요소 옆에 있는 도움말 아이콘(i)을 클릭하면 표시됩니다. 도움말 텍스트는 양식 필드의 레이블이나 플레이스홀더 텍스트보다 더 자세한 정보를 제공하며 사용자가 필드의 요구 사항이나 제한 사항을 이해하는 데 도움이 되도록 설계되었습니다. 또한 양식을 보다 쉽고 정확하게 작성할 수 있도록 제안이나 예시를 제공할 수도 있습니다.

### 접근성 {#accessibility}

![접근성 탭](/help/adaptive-forms/assets/button_accessibilitytab.png)


- **화면 판독기용 텍스트** - 화면 판독기용 텍스트는 시각 장애인이 사용하는 화면 판독기와 같은 보조 기술로 읽을 수 있도록 특별히 고안된 추가 텍스트를 나타냅니다. 이 텍스트는 양식 필드의 용도에 대한 오디오 설명을 제공하며, 여기에는 필드의 제목, 설명, 이름 및 관련 메시지(사용자 정의 텍스트)에 대한 정보가 포함될 수 있습니다. 화면 판독기 텍스트는 시각 장애가 있는 사용자를 포함한 모든 사용자가 양식에 액세스할 수 있도록 돕고 양식 필드 및 해당 요구 사항을 완전히 이해할 수 있도록 합니다.
   - **사용자 정의 텍스트**: ARIA 접근성 레이블에 사용자 정의 텍스트를 사용하려면 이 옵션을 선택합니다. 이 옵션을 선택하면 사용자 정의 텍스트 대화 상자가 표시됩니다. 사용자 정의 텍스트 대화 상자에서 관련 정보를 추가할 수 있습니다.
   - **설명**: ARIA 접근성 레이블에 설명을 사용하려면 이 옵션을 선택합니다.
   - **제목**: ARIA 접근성 레이블에 제목을 사용하려면 이 옵션을 선택합니다.
   - **이름**: ARIA 접근성 레이블에 이름을 사용하려면 이 옵션을 선택합니다.
   - **없음**: ARIA 접근성 레이블에 아무 것도 추가하지 않으려면 이 옵션을 선택합니다.

## 디자인 대화 상자 {#design-dialog}

디자인 대화 상자는 버튼 구성 요소의 CSS 스타일을 정의하고 관리하는 데 사용됩니다.

### 스타일 탭 {#styles-tab}

적응형 양식 버튼 핵심 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

![디자인 대화 상자](/help/adaptive-forms/assets/checkbox-style.png)

- **기본 CSS 클래스**: 적응형 양식 버튼 핵심 구성 요소에 기본 CSS 클래스를 제공할 수 있습니다.

- **허용된 스타일**: 이름과 스타일을 나타내는 CSS 클래스를 제공하여 스타일을 정의할 수 있습니다. 예를 들어 “bold text”라는 스타일을 만들고 “font-weight: bold”라는 CSS 클래스를 제공할 수 있습니다. 적응형 양식 편집기에서 이러한 스타일을 적응형 양식에 사용하거나 적용할 수 있습니다. 스타일을 적용하려면 적응형 양식 편집기에서 스타일을 적용할 구성 요소를 선택하고 속성 대화 상자로 이동한 다음 **스타일** 드롭다운 목록에서 원하는 스타일을 선택합니다. 스타일을 업데이트하거나 수정해야 하는 경우 디자인 대화 상자로 돌아가서 스타일 탭에서 스타일을 업데이트하고 변경 내용을 저장하면 됩니다.

### 사용자 정의 속성

![사용자 정의 속성 대화 상자](/help/adaptive-forms/assets/checkbox-customproperties.png)

사용자 정의 속성을 사용하면 양식 템플릿을 사용하여 사용자 정의 속성(키-값 쌍)을 적응형 양식 핵심 구성 요소에 연결할 수 있습니다. 사용자 정의 속성은 구성 요소의 Headless 렌디션에서 속성 섹션에 반영됩니다. 사용자 정의 속성 값에 따라 조정되는 동적 양식 동작을 만들 수 있습니다. 예를 들어 개발자는 모바일, 데스크탑 또는 웹 플랫폼을 위한 Headless 양식 구성 요소의 다양한 표현을 디자인하여 다양한 디바이스에서 사용자 경험을 크게 향상시킬 수 있습니다.

- **그룹 이름**: 사용자 정의 속성 그룹을 식별하기 위해 이름을 제공할 수 있습니다. 여러 사용자 정의 속성 그룹을 추가, 삭제 또는 재배열할 수 있습니다. 사용자 정의 속성 그룹을 추가하면 다음 옵션이 표시됩니다.

   - **키-값 쌍**: 각 사용자 정의 속성 그룹의 **추가** 버튼을 클릭하여 여러 사용자 정의 속성 이름과 사용자 정의 속성 값을 추가할 수 있습니다.

   - **삭제**: 사용자 정의 속성 이름과 사용자 정의 속성 값을 탭하거나 클릭하여 삭제할 수 있습니다.

   - **재배열**: 사용자 정의 속성 이름과 사용자 정의 속성 값을 탭하거나 클릭하고 드래그하면 순서를 재배열할 수 있습니다.

## 관련 문서 {#related-articles}

{{more-like-this}}

## 추가 참조 {#see-also}

{{see-also}}


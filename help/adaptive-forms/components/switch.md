---
title: 적응형 양식 핵심 구성 요소 - 전환 구성 요소
description: 적응형 양식 전환 핵심 구성 요소를 사용 또는 사용자 정의합니다.
role: Architect, Developer, Admin, User
exl-id: 6ff2ca76-1514-42eb-bde3-60259af2d187
source-git-commit: 8c51bd29074e5977d3435d849033770cadc357b8
workflow-type: tm+mt
source-wordcount: '1689'
ht-degree: 100%

---

# 전환 구성 요소{#switch-adaptive-forms-core-component}

전환 구성 요소는 사용자가 두 가지 옵션 중에서 선택할 수 있도록 하는 양식에 사용되는 그래픽 사용자 인터페이스입니다. 이는 일반적으로 사용자가 기능 또는 설정을 활성화하거나 비활성화하는 두 가지 상태 중에서 선택할 수 있도록 하는 2가지 상태 토글입니다. 전환 구성 요소는 현재 상태를 시각적으로 나타내고 특정 기능이 켜져 있는지 여부를 표시하도록 설계되었습니다.

전환 구성 요소는 값을 true 또는 false로 설정하는 부울 제어 요소입니다. 예를 들어 사운드 음소거 또는 음소거 해제, Bluetooth 또는 WiFi 활성화 또는 비활성화와 같은 기능을 켜거나 끄는 데 사용됩니다.

![전환 구성 요소 예](/help/adaptive-forms/assets/switch-example.png)

## 사용 {#reasons-to-use-switch}

적응형 양식에서 전환을 사용하는 일반적인 이유는 다음과 같습니다.

- **사용자 상호 작용**: 사용자는 전환 구성 요소를 클릭하거나 탭하여 전환 구성 요소와 상호 작용할 수 있습니다.

- **상태**: 전환 구성 요소에는 켜짐과 꺼짐의 두 가지 상태가 있습니다. 전환 구성 요소의 초기 상태는 기본 설정이나 제어하는 &#x200B;&#x200B;기능의 현재 상태에 따라 달라집니다.

- **시각적 표현**: 전환 구성 요소는 색상이나 위치를 변경하여 현재 상태를 시각적으로 반영합니다.

- **제어 기능**: 전환 구성 요소는 AEM 양식의 특정 기능을 활성화하거나 비활성화하는 데 사용됩니다. 예를 들어 사용자는 기능을 켜거나 끌 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

적응형 양식 전환 핵심 구성 요소는 핵심 구성 요소 2.0.64의 일부로 릴리스되었습니다. 다음 표에서는 지원되는 모든 버전, AEM 호환성 및 해당 문서에 대한 링크를 보여 줍니다.

|  |  |
|---|---|
| 구성 요소 버전 | AEM as a Cloud Service |
| --- | --- |
| v1 | <br>[릴리스 2.0.64](/help/adaptive-forms/version.md) 이상 버전과 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/adaptive-forms/version.md) 문서를 참조하십시오.

## 기술 세부 정보 {#technical-details}

적응형 양식 전환 핵심 구성 요소에 대한 최신 정보는 [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/switch/v1/switch)의 기술 설명서에서 확인할 수 있습니다. 핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 확인하십시오.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자를 사용하여 방문자를 위한 전환 구성 요소 경험을 손쉽게 사용자 정의할 수 있습니다. 전환 구성 요소 옵션을 간편하게 정의하여 원활한 사용자 경험을 제공할 수도 있습니다.

### 기본 탭

![기본 탭](/help/adaptive-forms/assets/switch-basic.png)

- **이름** - 양식과 규칙 편집기 모두에서 고유한 이름으로 양식 구성 요소를 쉽게 식별할 수 있습니다. 단, 이름에는 공백이나 특수 문자가 포함되어서는 안 됩니다.

- **제목** - 제목을 사용하면 양식에서 구성 요소를 쉽게 식별할 수 있으며, 기본적으로 제목은 구성 요소 옆에 나타납니다. 제목을 추가하지 않으면 구성 요소가 표시되지 않습니다.
<!-- **Allow Rich Text for Title** - This features enables users to format plain text titles, incorporating features like bold, italic, underlined text, various fonts, font sizes, colors, and additional option to enhance visual presentation and customization. It offers greater flexibility and creative control in making titles stand out within documents, websites, or applications.  
    Upon selecting the checkbox for **Allow Rich Text for Title** , formatting options become visible to style the component's title. To access all available formatting options, you can click on the ![Fullscreen icon](/help/adaptive-forms/assets/fullscreen-icon.png) tab.
     
     ![Rich text support](/help/adaptive-forms/assets/richtext-support-title.png)-->

- **제목 숨기기** - 구성 요소의 제목을 숨기려면 이 옵션을 선택합니다.

- **선택 해제 상태 값 유지** - 이 옵션을 선택하면 전환 구성 요소가 선택되지 않은 경우 반환될 값을 지정할 수 있습니다.
- **옵션** - 데이터 값을 지정하고 각 옵션에 대한 텍스트를 표시합니다.
   - **켜짐 데이터 값** - 적응형 양식에서 전환이 활성화될 때 제출할 값을 지정합니다.
   - **켜짐 표시 텍스트** - 적응형 양식에서 전환이 활성화될 때 레이블로 표시할 텍스트를 지정합니다.
   - **꺼짐 데이터 값** - 적응형 양식에서 전환이 비활성화될 때 제출할 값을 지정합니다. 이 옵션은 **선택 해제 상태 값 유지** 전환이 활성화된 경우에만 표시됩니다.
   - **꺼짐 표시 텍스트** - 적응형 양식에서 전환이 비활성화될 때 레이블로 표시할 텍스트를 지정합니다. 이 옵션은 **선택 해제 상태 값 유지** 전환이 활성화된 경우에만 표시됩니다.

<!-- You can also format the options for switch using **Allow Rich Text for Options**. 
  
     ![Rich text support for options](/help/adaptive-forms/assets/switch-optipn-rich-text.png)

    Once you select the checkbox for **Allow Rich Text for options** formatting options become visible to style the component's options. To access all available formatting options, you can click on the `Fullscreen` ![Fullscreen icon](/help/adaptive-forms/assets/fullscreen-icon.png) tab.
    
    ![Rich text support for options](/help/adaptive-forms/assets/switch-richtext-for-display.png) -->


- **바인드 참조** - 바인드 참조는 외부 데이터 소스에 저장되고 양식에서 사용되는 데이터 요소에 대한 참조입니다. 바인드 참조를 사용하면 데이터를 양식 필드에 동적으로 바인딩하여 양식이 데이터 소스의 최신 데이터를 표시하도록 할 수 있습니다. 예를 들어 바인드 참조를 사용하여 양식에 입력된 고객의 ID를 기반으로 고객의 이름과 주소를 양식에 표시할 수 있습니다. 바인드 참조를 사용하여 양식에 입력된 데이터로 데이터 소스를 업데이트할 수도 있습니다. 이러한 방식으로 AEM Forms를 사용하면 외부 데이터 소스와 상호 작용하는 양식을 만들어 데이터 수집 및 관리를 위한 원활한 사용자 경험을 제공할 수 있습니다.
- **언바운드 양식 요소로 표시**: 어떤 스키마에도 연결되지 않은 양식 필드를 구성하려면 이 옵션을 선택합니다. 이 옵션을 사용하면 데이터 소스를 업데이트하지 않고도 데이터를 저장할 수 있습니다. 또한 표준 데이터베이스 통합과 별도로 사용자 정의 방식으로 데이터를 처리할 수 있습니다.

- **제출된 값의 데이터 유형**: 이 옵션을 선택하면 전송되는 값의 데이터 유형이 지정됩니다. **제출된 값의 데이터 유형**&#x200B;이 `Number`로 설정되어 있고 **옵션** 탭의 **데이터 값**&#x200B;에 문자열 데이터를 추가하면 화면에 `Value type mismatch` 오류 메시지가 표시됩니다.
- **구성 요소 숨기기** - 양식에서 구성 요소를 숨기려면 이 옵션을 선택합니다. 구성 요소는 다른 용도로(예: 규칙 편집기에서 계산에 사용) 계속 액세스할 수 있습니다. 구성 요소 숨기기는 사용자가 보거나 직접 변경할 필요가 없는 정보를 저장해야 할 때 유용합니다.

- **구성 요소 비활성화** - 구성 요소를 비활성화하거나 잠그려면 이 옵션을 선택합니다. 비활성화된 구성 요소는 활성 상태가 아니므로 최종 사용자가 편집할 수 없습니다. 사용자는 필드 값을 볼 수 있지만 수정할 수는 없습니다. 구성 요소는 다른 용도로(예: 규칙 편집기에서 계산에 사용) 계속 액세스할 수 있습니다.

- **기본값**: 이 옵션을 사용하면 양식 필드에 기본값을 추가할 수 있습니다. **비활성화된 구성 요소** 또는 **읽기 전용 구성 요소**&#x200B;를 선택하면 화면에 기본값이 표시됩니다. 사용자가 양식 필드에 값을 입력하지 않으면 이 값이 양식 제출 시 함께 제출됩니다.

### 유효성 검사 탭 {#validation-tab}

![유효성 검사 탭](/help/adaptive-forms/assets/switch-validation.png)

- **필수** - 적응형 양식에 구성 요소를 표시하려면 이 옵션을 선택합니다. 이 옵션을 선택하면 양식 제출을 진행하기 전에 선택을 해야 합니다. 이 옵션이 선택되어 있으면 **기본** 탭에서 **구성 요소 숨기기** 또는 **구성 요소 비활성화**&#x200B;를 선택할 수 없습니다.

- **오류 메시지** - 이 옵션을 사용하면 **필수** 확인란이 선택되어 있고 양식 필드가 비어 있는 경우 표시되는 메시지를 입력할 수 있습니다.

- **스크립트 유효성 검사 메시지** - 이 옵션을 사용하면 스크립트 유효성 검사가 실패할 경우 표시할 메시지를 입력할 수 있습니다.

### 도움말 콘텐츠 탭 {#helpcontent-tab}

![도움말 콘텐츠 탭](/help/adaptive-forms/assets/switch-help.png)

- **간단한 설명** - 간단한 설명은 특정 양식 필드의 용도에 대한 추가 정보 또는 설명을 제공하는 간단한 텍스트 설명입니다. 사용자가 필드에 입력해야 하는 데이터 유형을 이해하는 데 도움이 되며 입력된 정보가 유효하고 원하는 기준을 충족하는지 확인하는 데 도움이 되는 지침 또는 예시를 제공할 수 있습니다. 기본적으로 간단한 설명은 숨겨진 상태로 유지됩니다. **간단한 설명 항상 표시** 옵션을 활성화하여 구성 요소 아래에 표시할 수 있습니다.

- **간단한 설명 항상 표시** - 이 옵션을 활성화하여 구성 요소 아래에 간단한 설명을 표시할 수 있습니다.

- **도움말 텍스트** - 도움말 텍스트는 양식 필드를 올바르게 작성하는 데 도움이 되도록 사용자에게 제공되는 추가 정보 또는 지침을 나타냅니다. 구성 요소 옆에 있는 도움말 아이콘(i)을 클릭하면 표시됩니다. 도움말 텍스트는 양식 필드의 레이블이나 플레이스홀더 텍스트보다 더 자세한 정보를 제공하며 사용자가 필드의 요구 사항이나 제한 사항을 이해하는 데 도움이 되도록 설계되었습니다. 또한 양식을 보다 쉽고 정확하게 작성할 수 있도록 제안이나 예시를 제공할 수도 있습니다.

### 접근성 탭 {#accessibility-tab}

![접근성 탭](/help/adaptive-forms/assets/switch-accessibility.png)

**화면 판독기용 텍스트** - 화면 판독기용 텍스트는 시각 장애인이 사용하는 화면 판독기와 같은 보조 기술로 읽을 수 있도록 고안된 추가 텍스트를 나타냅니다. 이 텍스트는 양식 필드의 용도에 대한 오디오 설명을 제공하며, 여기에는 필드의 제목, 설명, 이름 및 관련 메시지(사용자 정의 텍스트)에 대한 정보가 포함될 수 있습니다. 화면 판독기 텍스트는 시각 장애가 있는 사용자를 포함한 모든 사용자가 양식에 액세스할 수 있도록 돕고 양식 필드 및 해당 요구 사항을 완전히 이해할 수 있도록 합니다.

### 스타일 탭 {#styles-tab}

![스타일 탭](/help/adaptive-forms/assets/switch-styles.png)

- **레이블 숨기기** - 전환 구성 요소의 레이블을 숨기려면 이 옵션을 선택합니다.

- **레이블 표시** - 전환 구성 요소의 레이블 표시하려면 이 옵션을 선택합니다.

## 디자인 대화 상자 {#design-dialog}

디자인 대화 상자는 전환 구성 요소의 CSS 스타일을 정의하고 관리하는 데 사용됩니다.

### 스타일 탭 {#styles-design-tab}

적응형 양식 전환 핵심 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

![디자인 대화 상자](/help/adaptive-forms/assets/checkbox-style.png)

- **기본 CSS 클래스**: 적응형 양식 전환 그룹 핵심 구성 요소에 기본 CSS 클래스를 제공할 수 있습니다.

- **허용된 스타일**: 이름과 스타일을 나타내는 CSS 클래스를 제공하여 스타일을 정의할 수 있습니다. 예를 들어 “bold text”라는 스타일을 만들고 “font-weight: bold”라는 CSS 클래스를 제공할 수 있습니다. 적응형 양식 편집기에서 이러한 스타일을 적응형 양식에 사용하거나 적용할 수 있습니다. 스타일을 적용하려면 적응형 양식 편집기에서 스타일을 적용할 구성 요소를 선택하고 속성 대화 상자로 이동한 다음 **스타일** 드롭다운 목록에서 원하는 스타일을 선택합니다. 스타일을 업데이트하거나 수정해야 하는 경우 디자인 대화 상자로 돌아가서 스타일 탭에서 스타일을 업데이트하고 변경 내용을 저장하면 됩니다.

### 사용자 정의 속성

![사용자 정의 속성 대화 상자](/help/adaptive-forms/assets/checkbox-customproperties.png)

사용자 정의 속성을 사용하면 양식 템플릿을 사용하여 사용자 정의 속성(키-값 쌍)을 적응형 양식 핵심 구성 요소에 연결할 수 있습니다. 사용자 정의 속성은 구성 요소의 Headless 렌디션에서 속성 섹션에 반영됩니다. 사용자 정의 속성 값에 따라 조정되는 동적 양식 동작을 만들 수 있습니다. 예를 들어 개발자는 모바일, 데스크탑 또는 웹 플랫폼을 위한 Headless 양식 구성 요소의 다양한 표현을 디자인하여 다양한 디바이스에서 사용자 경험을 크게 향상시킬 수 있습니다.

- **그룹 이름**: 사용자 정의 속성 그룹을 식별하기 위해 이름을 제공할 수 있습니다. 여러 사용자 정의 속성 그룹을 추가, 삭제 또는 재배열할 수 있습니다. 사용자 정의 속성 그룹을 추가하면 다음 옵션이 표시됩니다.

   - **키-값 쌍**: 각 사용자 정의 속성 그룹의 **추가** 버튼을 클릭하여 여러 사용자 정의 속성 이름과 사용자 정의 속성 값을 추가할 수 있습니다.

   - **삭제**: 사용자 정의 속성 이름과 사용자 정의 속성 값을 탭하거나 클릭하여 삭제할 수 있습니다.

   - **재배열**: 사용자 정의 속성 이름과 사용자 정의 속성 값을 누르거나 클릭하고 드래그하면 재배열할 수 있습니다.

## 관련 문서 {#related-articles}

{{more-like-this}}

## 추가 참조 {#see-also}

{{see-also}}

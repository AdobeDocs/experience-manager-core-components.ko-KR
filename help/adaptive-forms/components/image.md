---
title: 적응형 양식 핵심 구성 요소 - 이미지
description: 적응형 양식 이미지 핵심 구성 요소를 사용 또는 사용자 정의합니다.
role: Architect, Developer, Admin, User
exl-id: 9ee42d5d-16e3-4973-8364-5bc512ebe72e
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: ht
source-wordcount: '1056'
ht-degree: 100%

---


# 이미지 구성 요소{#image-adaptive-forms-core-component}

적응형 양식의 이미지 구성 요소를 사용하여 양식에 이미지를 포함할 수 있습니다. 이러한 이미지를 사용하여 양식의 전반적인 디자인을 개선하거나, 추가 정보를 제공하거나, 사용자가 양식의 용도를 이해하는 데 도움이 되는 시각 자료로 사용할 수 있습니다. 이미지 구성 요소를 사용하여 양식에 로고, 사진 또는 그래픽을 추가할 수 있습니다.

접근성을 위해 이미지에 대한 **대체 텍스트**&#x200B;를 지정하여 이미지를 볼 수 없는 사용자에게 이미지를 설명하는 간단한 대체 텍스트를 제공하는 것이 중요합니다.

{{traditional-aem}}

**예**

![예](/help/adaptive-forms/assets/image.png)


## 사용 {#reasons-to-use-image-in-a-form}

적응형 양식에 이미지 구성 요소를 포함하는 것이 유익한 몇 가지 이유는 다음과 같습니다.

- **브랜딩**: 이미지를 사용하여 양식을 만든 조직의 로고나 이름을 표시할 수 있으므로 브랜드 인지도와 신뢰성을 확립하는 데 도움이 됩니다.

- **시각 자료**: 이미지는 사용자가 양식의 용도를 이해하는 데 도움이 되는 시각 자료 역할을 하여 사용자에게 추가 정보를 제공하는 데 도움이 될 수 있습니다.

- **장식**: 이미지를 사용하여 양식의 전반적인 디자인을 개선하고 시각적으로 더 매력적으로 만들 수 있습니다.

- **사용자 경험**: 이미지를 사용하면 사용자가 명확하고 직관적으로 양식 필드에 액세스하고 채울 수 있으므로 양식을 보다 사용자 친화적으로 만들 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

적응형 양식 이미지 핵심 구성 요소는 Cloud Service의 핵심 구성 요소 2.0.4 및 AEM 6.5.16.0 Forms 이상의 핵심 구성 요소 1.1.12 일부로 2023년 2월에 릴리스되었습니다. 다음 테이블에서는 지원되는 모든 버전, AEM 호환성 및 해당 문서에 대한 링크를 보여 줍니다.

| 구성 요소 버전 | AEM as a Cloud Service | AEM 6.5.16.0 Forms 이상 |
|---|---|---|
| v1 | <br>[릴리스 2.0.4](/help/adaptive-forms/version.md) 이상 버전과 호환 가능 | <br>[릴리스 1.1.12](/help/adaptive-forms/version.md) 이상과 호환합니다(2.0.0 이전 버전). |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/adaptive-forms/version.md) 문서를 참조하십시오.


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion_kr). -->

## 기술 세부 정보 {#technical-details}

적응형 양식 이미지 핵심 구성 요소에 대한 최신 정보는 [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/image/v1/image)의 기술 설명서에서 확인할 수 있습니다. 핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 확인하십시오.


## 구성 대화 상자 {#configure-dialog}

구성 대화 상자를 사용하여 방문자를 위한 이미지 경험을 손쉽게 사용자 정의할 수 있습니다. 이미지 옵션을 간편하게 정의하여 원활한 사용자 경험을 제공할 수도 있습니다.

![속성 탭](/help/adaptive-forms/assets/image_properties.png)

- **이름** - 양식과 규칙 편집기 모두에서 고유한 이름으로 양식 구성 요소를 쉽게 식별할 수 있습니다. 단, 이름에는 공백이나 특수 문자가 포함되어서는 안 됩니다.

- **제목** - 제목을 사용하면 양식에서 구성 요소를 쉽게 식별할 수 있으며, 기본적으로 제목은 구성 요소 상단에 나타납니다. 제목을 추가하지 않으면 제목 텍스트 대신 구성 요소의 이름이 표시됩니다.

- **언바운드 양식 요소로 표시**: 어떤 스키마에도 연결되지 않은 양식 필드를 구성하려면 이 옵션을 선택합니다. 이 옵션을 사용하면 데이터 소스를 업데이트하지 않고도 데이터를 저장할 수 있습니다. 또한 표준 데이터베이스 통합과 별도로 사용자 정의 방식으로 데이터를 처리할 수 있습니다.

<!--   **Document of Record bind reference** - This option allows you to associate an Adaptive Form field with Document of Record field. When user enters any value in a linked field of an Adaptive Form that value also appears in the linked field of the corresponding Document of Record. For example, a Document of Record bind reference can be used to display a customer's name and address in a Document of Record, based on the customer's ID entered into the form. In this way, AEM Forms enable you to generate Document of Record and offers a seamless user experience for collecting and managing data.-->

- **설명** - 설명은 특정 이미지의 용도에 대한 추가 정보 또는 설명을 제공하는 간단한 텍스트 설명입니다.

- **여기에 자산을 놓거나 업로드할 파일 검색** - 이 옵션을 사용하면 마우스 드래그 앤 드롭으로 이미지와 같은 자산을 놓을 수 있습니다. **검색** 버튼을 사용하여 로컬 파일 시스템에서 파일을 업로드할 수도 있습니다. 이미지를 추가하면 이미지 하단에 세 개의 버튼이 나타납니다.
   - **편집** - 자산 편집기에서 자산 렌디션을 관리하려면 **편집**&#x200B;을 탭하거나 클릭합니다.
   - **지우기** - 현재 선택된 이미지의 선택을 해제하려면 **지우기**&#x200B;를 탭하거나 클릭합니다.
   - **선택** - 자산 폴더에서 다른 이미지를 선택하려면 **선택**&#x200B;을 탭하거나 클릭합니다.

- **대체 텍스트** - 이 옵션은 시각 장애가 있는 사용자에게 이미지를 설명해 주는 이미지에 대한 간단한 대체 텍스트를 제공하는 텍스트를 입력하는 데 사용됩니다.

- **구성 요소 숨기기** - 양식에서 구성 요소를 숨기려면 이 옵션을 선택합니다. 구성 요소는 다른 용도로(예: 규칙 편집기에서 계산에 사용) 계속 액세스할 수 있습니다. 구성 요소 숨기기는 사용자가 보거나 직접 변경할 필요가 없는 정보를 저장해야 할 때 유용합니다.

<!--   **Read-only** - Select the option to make the component non-editable. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.
-->

## 디자인 대화 상자 {#design-dialog}

디자인 대화 상자는 이미지 구성 요소의 CSS 스타일을 정의하고 관리하는 데 사용됩니다.

### 스타일 탭 {#styles-tab}

탭은 구성 요소의 CSS 스타일을 정의하고 관리하는 데 사용됩니다. 적응형 양식 이미지 핵심 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

![디자인 대화 상자](/help/adaptive-forms/assets/checkbox-style.png)

- **기본 CSS 클래스**: 적응형 양식 이미지 핵심 구성 요소에 기본 CSS 클래스를 제공할 수 있습니다.

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
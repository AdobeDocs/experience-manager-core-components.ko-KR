---
title: 적응형 양식 핵심 구성 요소 - 텍스트
description: 적응형 양식 텍스트 핵심 구성 요소를 사용 또는 사용자 정의합니다.
role: Architect, Developer, Admin, User
exl-id: b8de68e4-ca0d-4ae5-9a04-104cc617f1be
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: ht
source-wordcount: '996'
ht-degree: 100%

---


# 텍스트 구성 요소 {#text-adaptive-forms-core-component}

적응형 양식에서 텍스트는 사용자가 읽을 수 있도록 양식에 표시되는 콘텐츠를 나타냅니다. 여기에는 텍스트 필드와 같은 양식 요소 그룹에 레이블을 지정하는 데 사용되는 텍스트와 사용자에게 제공되는 추가 지침 또는 정보가 포함될 수 있습니다.

양식의 구조를 논리 섹션으로 나누는 데 도움이 되므로 사용자는 양식을 더 쉽게 이해하고 완성할 수 있습니다. 또한 연결된 요소에 대한 간략한 설명을 제공하기 위해 접근성 용도로 사용할 수도 있습니다. 이러한 텍스트 필드는 일반적으로 양식 구성 요소 근처(예: 전 또는 후)에 표시됩니다.

{{traditional-aem}}

**예**

![텍스트의 예](/help/adaptive-forms/assets/text.png)

## 사용 {#reasons-to-use-text-label}

양식에서 텍스트를 사용하는 데에는 다음과 같은 몇 가지 이유가 있습니다.

- **지침 제공**: 텍스트를 사용하여 양식을 작성하는 방법이나 필요한 정보에 대한 지침을 제공할 수 있습니다.

- **컨텍스트 제공**: 텍스트를 사용하여 양식의 용도나 정보를 수집하는 조직에 대해 설명하는 것과 같이 양식에 대한 컨텍스트를 제공할 수 있습니다.

- **양식을 논리 섹션으로 나누기**: 텍스트를 사용하여 양식을 논리 섹션으로 나눌 수 있으므로 사용자는 양식을 더 쉽게 이해하고 완성할 수 있습니다.

- **브랜딩 및 정체성 강조**: 양식에 조직의 이름을 포함하는 등 텍스트를 브랜딩 및 정체성 강조 용도로 사용할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

적응형 양식 텍스트 핵심 구성 요소는 Cloud Service의 핵심 구성 요소 2.0.4 및 AEM 6.5.16.0 Forms 이상의 핵심 구성 요소 1.1.12 일부로 2023년 2월에 릴리스되었습니다. 다음 테이블에서는 지원되는 모든 버전, AEM 호환성 및 해당 문서에 대한 링크를 보여 줍니다.

| 구성 요소 버전 | AEM as a Cloud Service | AEM 6.5.16.0 Forms 이상 |
|---|---|---|
| v1 | <br>[릴리스 2.0.4](/help/adaptive-forms/version.md) 이상 버전과 호환 가능 | <br>[릴리스 1.1.12](/help/adaptive-forms/version.md) 이상과 호환합니다(2.0.0 이전 버전). |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/adaptive-forms/version.md) 문서를 참조하십시오.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## 기술 세부 정보 {#technical-details}

적응형 양식 텍스트 핵심 구성 요소에 대한 최신 정보는 [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/text/v1/text)의 기술 설명서에서 확인할 수 있습니다. 핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 확인하십시오.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자를 사용하여 방문자를 위한 텍스트 경험을 손쉽게 사용자 정의할 수 있습니다. 텍스트 옵션을 간편하게 정의하여 원활한 사용자 경험을 제공할 수도 있습니다.

### 기본 탭

![기본 탭](/help/adaptive-forms/assets/text_properties.png)

- **이름** - 양식과 규칙 편집기 모두에서 고유한 이름으로 양식 구성 요소를 쉽게 식별할 수 있습니다. 단, 이름에는 공백이나 특수 문자가 포함되어서는 안 됩니다.

- **바인드 참조** - 바인드 참조는 외부 데이터 소스에 저장되고 양식에서 사용되는 데이터 요소에 대한 참조입니다. 바인드 참조를 사용하면 데이터를 양식 필드에 동적으로 바인딩하여 양식이 데이터 소스의 최신 데이터를 표시하도록 할 수 있습니다. 예를 들어 바인드 참조를 사용하여 양식에 입력된 고객의 ID를 기반으로 고객의 이름과 주소를 양식에 표시할 수 있습니다. 바인드 참조를 사용하여 양식에 입력된 데이터로 데이터 소스를 업데이트할 수도 있습니다. 이러한 방식으로 AEM Forms를 사용하면 외부 데이터 소스와 상호 작용하는 양식을 만들어 데이터 수집 및 관리를 위한 원활한 사용자 경험을 제공할 수 있습니다.
- **언바운드 양식 요소로 표시**: 어떤 스키마에도 연결되지 않은 양식 필드를 구성하려면 이 옵션을 선택합니다. 이 옵션을 사용하면 데이터 소스를 업데이트하지 않고도 데이터를 저장할 수 있습니다. 또한 표준 데이터베이스 통합과 별도로 사용자 정의 방식으로 데이터를 처리할 수 있습니다.
- **구성 요소 숨기기** - 양식에서 구성 요소를 숨기려면 이 옵션을 선택합니다. 구성 요소는 다른 용도로(예: 규칙 편집기에서 계산에 사용) 계속 액세스할 수 있습니다. 구성 요소 숨기기는 사용자가 보거나 직접 변경할 필요가 없는 정보를 저장해야 할 때 유용합니다.
  <!--    **Read-only** - Select the option to make the component non-editable. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.-->

## 디자인 대화 상자 {#design-dialog}

디자인 대화 상자는 텍스트 구성 요소의 CSS 스타일을 정의하고 관리하는 데 사용됩니다.

### 스타일 탭 {#styles-tab}

탭은 구성 요소의 CSS 스타일을 정의하고 관리하는 데 사용됩니다. 적응형 양식 텍스트 핵심 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

![디자인 대화 상자](/help/adaptive-forms/assets/checkbox-style.png)

- **기본 CSS 클래스**: 적응형 양식 텍스트 핵심 구성 요소에 기본 CSS 클래스를 제공할 수 있습니다.

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
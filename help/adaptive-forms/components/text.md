---
title: 응용 Forms 코어 구성 요소 - 텍스트
description: 응용 Forms 텍스트 코어 구성 요소 사용 또는 사용자 지정
role: Architect, Developer, Admin, User
source-git-commit: 1e6460d318f4f9a5dfdcbb81723da01b51b72f3f
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 3%

---


# 텍스트 {#text-adaptive-forms-core-component}

적응형 양식에서 텍스트는 사용자가 읽을 양식에 표시되는 컨텐츠를 나타냅니다. 여기에는 텍스트 필드와 같은 양식 요소 그룹에 레이블을 지정하는 데 사용되는 텍스트와 사용자에게 제공된 추가 지침이나 정보가 포함될 수 있습니다.

또한 양식의 구조를 논리 섹션으로 나누면 사용자가 양식을 쉽게 이해하고 완료할 수 있습니다. 또한 액세스 가능성 용도로 사용하여 연결된 요소에 대한 간단한 설명을 제공할 수 있습니다. 이러한 텍스트 필드는 일반적으로 양식 구성 요소 근처에 표시됩니다(예: 양식 구성 요소 앞 또는 뒤).

**예**

![](/help/adaptive-forms/assets/text.png)

## 사용 {#reasons-to-use-text-label}

양식에 텍스트를 사용해야 하는 이유는 다음과 같습니다.

* **지침 제공**: 텍스트를 사용하여 양식을 채우는 방법 또는 필요한 정보를 지정할 수 있습니다.

* **컨텍스트 제공**: 텍스트는 양식의 목적을 설명하거나 정보를 수집하는 조직에서 양식 컨텍스트를 제공하는 데 사용할 수 있습니다.

* **양식을 논리 섹션으로 나누기**: 텍스트를 사용하여 양식을 논리 섹션으로 나눌 수 있으므로 사용자가 양식을 쉽게 이해하고 완료할 수 있습니다.

* **브랜딩 및 ID**: 텍스트는 양식에 조직의 이름을 포함하는 등의 브랜딩 및 ID 용도로 사용할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

응용 Forms 텍스트 코어 구성 요소는 코어 구성 요소 2.0.4의 일부로 2023년 2월에 출시되었습니다. 다음은 지원되는 모든 버전, AEM 호환성 및 해당 설명서 링크를 보여주는 표입니다.

| 구성 요소 버전 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | 호환 가능 with<br>[릴리스 2.0.4](/help/versions.md) 나중에 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md) 문서.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## 기술 세부 사항 {#technical-details}

응용 Forms 텍스트 코어 구성 요소에 대한 최신 정보를 다음 기술 문서에서 얻습니다. [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/text/v1/text). 핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md).

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자에서 방문자의 텍스트 경험을 쉽게 사용자 지정할 수 있습니다. 원활한 사용자 경험을 위해 텍스트 옵션을 쉽게 정의할 수도 있습니다.

![기본 탭](/help/adaptive-forms/assets/text_properties.png)

* **이름** - 양식 및 규칙 편집기에서 고유한 이름으로 양식 구성 요소를 쉽게 식별할 수 있지만 이름에 공백이나 특수 문자가 포함되어 있으면 안 됩니다.

* **바인딩 참조** - 바인딩 참조는 외부 데이터 소스에 저장되고 양식에 사용되는 데이터 요소에 대한 참조입니다. 바인딩 참조를 사용하면 데이터를 양식 필드에 동적으로 바인딩할 수 있으므로 폼에서 데이터 소스의 최신 데이터를 표시할 수 있습니다. 예를 들어 바인딩 참조를 사용하여 양식에 입력한 고객 ID를 기반으로 고객의 이름과 주소를 양식에 표시할 수 있습니다. 바인딩 참조를 사용하여 양식에 입력한 데이터로 데이터 소스를 업데이트할 수도 있습니다. 이러한 방식으로 AEM Forms을 사용하면 외부 데이터 소스와 상호 작용하는 양식을 만들어 데이터를 수집 및 관리하기 위한 원활한 사용자 경험을 제공할 수 있습니다.
* **구성 요소 숨기기** - 양식에서 구성 요소를 숨길 옵션을 선택합니다. 구성 요소는 규칙 편집기에서 계산에 사용하는 것과 같이 다른 목적으로 액세스할 수 있습니다. 이 기능은 사용자가 직접 보거나 볼 필요가 없는 정보를 저장해야 하는 경우 유용합니다.
* **읽기 전용** - 구성 요소를 편집할 수 없도록 하려면 옵션을 선택합니다. 사용자는 필드의 값을 볼 수 있지만 수정할 수 없습니다. 구성 요소는 규칙 편집기에서 계산에 사용하는 것과 같이 다른 목적으로 액세스할 수 있습니다.


## 디자인 대화 상자 {#design-dialog}

디자인 대화 상자는 텍스트 구성 요소의 CSS 스타일을 정의하고 관리하는 데 사용됩니다.


### 스타일 탭 {#styles-tab}

디자인 대화 상자는 구성 요소의 CSS 스타일을 정의하고 관리하는 데 사용됩니다. 응용 Forms 텍스트 코어 구성 요소는 AEM을 지원합니다 [스타일 시스템](/help/get-started/authoring.md#component-styling).

**기본 CSS 클래스**: 응용 Forms 텍스트 코어 구성 요소에 기본 CSS 클래스를 제공할 수 있습니다.

**허용된 스타일**: 스타일을 나타내는 이름과 CSS 클래스를 제공하여 스타일을 정의할 수 있습니다. 예를 들어 &quot;bold text&quot;라는 스타일을 만들고 CSS 클래스 &quot;font-weight: 굵게. 적응형 Forms 편집기에서 적응형 양식에 이러한 스타일을 사용하거나 적용할 수 있습니다. 스타일을 적용하려면 적응형 Forms 편집기에서 스타일을 적용할 구성 요소를 선택하고 속성 대화 상자로 이동한 다음, **스타일** 드롭다운 목록. 스타일을 업데이트하거나 수정해야 하는 경우, 디자인 대화 상자로 돌아가서 스타일 탭에서 스타일을 업데이트하고 변경 사항을 저장하면 됩니다.

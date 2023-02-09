---
title: 응용 Forms 코어 구성 요소 - 제목
description: 응용 Forms 제목 코어 구성 요소 사용 또는 사용자 지정
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '836'
ht-degree: 14%

---


# 제목 {#title-input-adaptive-forms-core-component}

적응형 양식에서 &quot;제목&quot;은 양식 맨 위에 나타나는 텍스트를 나타내며, 일반적으로 머리글 아래에 있습니다. 제목은 제목 구성 요소를 사용하여 지정됩니다. 이 구성 요소를 양식 레이아웃에 추가할 수 있으며, 양식의 목적이나 주제와 일치하도록 텍스트를 편집할 수 있습니다. 제목은 사용자에게 양식의 레이블이나 간단한 설명 역할을 하며 양식을 다른 사용자와 구분하는 데 도움이 됩니다.

**예**

![](/help/adaptive-forms/assets/title.png)

## 사용 {#reasons-to-use-title-in-an-adaptive-form}

폼에서 제목을 사용하는 것이 좋은 이유는 다음과 같습니다.

* **명확성**: 제목은 양식의 목적을 명확하게 식별하며 사용자가 제공하는 정보를 이해할 수 있도록 해줍니다.

* **조직**: 제목을 사용하면 주제 또는 용도별로 양식을 구성할 수 있으므로 사용자가 필요한 양식을 쉽게 찾을 수 있습니다.

* **접근성**: 제목은 화면 판독기에서 소리내어 읽으므로 사용자가 양식의 컨텍스트를 이해하는 데 도움이 되므로 액세스 가능성이 필요한 사용자를 위한 주요 요소입니다.

* **브랜딩**: 제목을 사용하여 회사 또는 조직의 이름을 표시할 수도 있으며, 이를 통해 사용자에 대한 신뢰와 친근감을 얻을 수 있습니다.

* **탐색**: 특히 양식이 길거나 복잡한 경우 제목을 사용하여 양식을 탐색할 수도 있습니다.

* **SEO(검색 엔진 최적화)**: 검색 엔진은 제목을 사용하여 검색 쿼리에 대한 웹 페이지의 관련성을 결정하므로 SEO에도 제목이 있습니다.

전체적으로 양식의 제목은 사용자 경험의 중요한 측면이며 사용자가 양식의 컨텍스트 및 목적을 이해하는 데 도움이 되는 명확하고 간결한 레이블을 제공하는 데 사용해야 합니다.

## 버전 및 호환성 {#version-and-compatibility}

응용 Forms 제목 코어 구성 요소는 코어 구성 요소 2.0.4의 일부로 2023년 2월에 출시되었습니다. 다음은 지원되는 모든 버전, AEM 호환성 및 해당 설명서 링크를 보여주는 표입니다.

|  |  |
|---|---|
| 구성 요소 버전 | AEM as a Cloud Service |
| --- | --- |
| v1 | 호환 가능 with<br>[릴리스 2.0.4](/help/versions.md) 나중에 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md) 문서.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## 기술 세부 사항 {#technical-details}

응용 Forms 제목 코어 구성 요소에 대한 최신 정보를 다음 기술 문서에서 얻습니다. [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/title/v1/title). 핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md).

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자에서 방문자의 제목 경험을 쉽게 사용자 지정할 수 있습니다. 또한 원활한 사용자 경험을 위해 쉽게 제목 옵션을 정의할 수 있습니다.

![기본 탭](/help/adaptive-forms/assets/title_properties.png)

콘텐츠 작성자는 편집 대화 상자를 통해 제목 텍스트를 정의하고 머리말 수준을 선택할 수 있습니다.

* **제목** - 제목 을 사용하면 양식의 구성 요소를 쉽게 식별할 수 있으며, 기본적으로 제목이 구성 요소 위에 표시됩니다. 제목을 추가하지 않으면 제목 텍스트 대신 구성 요소의 이름이 표시됩니다.
* **Type /Size** - 제목의 제목 수준을 정의합니다.
* **ID** - 이 옵션을 통해 HTML과 데이터 레이어에서 구성 요소의 고유 식별자를 제어할 수 있습니다.
   * 비워 두면 고유 ID는 자동으로 생성되고 결과 페이지 검사를 통해 발견될 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID가 변경되면 CSS, JS 및 데이터 레이어 추적에 영향을 미칠 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

디자인 대화 상자는 날짜-선택기 구성 요소의 CSS 스타일을 정의하고 관리하는 데 사용됩니다.

### 제목

제목 탭에서는 템플릿 작성자가 양식 작성자에 대한 기본 및 허용된 HTML 제목 요소를 설정할 수 있습니다.

![디자인 대화 상자 제목 탭](/help/assets/accordion-design-properties.png)

* **허용된 제목 요소**: 템플릿 작성자가 제목에 사용할 수 있는 머리글 요소를 선택할 수 있는 여러 옵션이 있는 목록입니다.

* **기본 제목 요소**: 제목 구성 요소의 기본 제목 요소를 설정하는 드롭다운 목록입니다.


### 스타일 탭 {#styles-tab}

디자인 대화 상자는 구성 요소의 CSS 스타일을 정의하고 관리하는 데 사용됩니다. 응용 Forms 날짜 선택기 핵심 구성 요소는 AEM을 지원합니다 [스타일 시스템](/help/get-started/authoring.md#component-styling).

**기본 CSS 클래스**: 응용 Forms 날짜 선택기 코어 구성 요소에 기본 CSS 클래스를 제공할 수 있습니다.

**허용된 스타일**: 스타일을 나타내는 이름과 CSS 클래스를 제공하여 스타일을 정의할 수 있습니다. 예를 들어 &quot;bold text&quot;라는 스타일을 만들고 CSS 클래스 &quot;font-weight: 굵게. 적응형 Forms 편집기에서 적응형 양식에 이러한 스타일을 사용하거나 적용할 수 있습니다. 스타일을 적용하려면 적응형 Forms 편집기에서 스타일을 적용할 구성 요소를 선택하고 속성 대화 상자로 이동한 다음, **스타일** 드롭다운 목록. 스타일을 업데이트하거나 수정해야 하는 경우, 디자인 대화 상자로 돌아가서 스타일 탭에서 스타일을 업데이트하고 변경 사항을 저장하면 됩니다.

### 형식 탭 {#format-tab}

형식 탭에서는 기본 및 사용자 지정 날짜 형식을 지정할 수 있습니다.


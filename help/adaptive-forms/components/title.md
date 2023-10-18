---
title: 적응형 양식 핵심 구성 요소 - 제목
description: 적응형 양식 제목 핵심 구성 요소를 사용 또는 사용자 정의합니다.
role: Architect, Developer, Admin, User
exl-id: 33eac885-8d66-4a5c-9a32-0ba11e6de293
source-git-commit: 0bebc248ee2b708f7677950d90356abd5bc70a98
workflow-type: tm+mt
source-wordcount: '935'
ht-degree: 100%

---

# 제목 {#title-input-adaptive-forms-core-component}

적응형 양식에서 “제목”은 양식 상단, 일반적으로 헤더 아래에 표시되는 텍스트를 나타냅니다. 제목은 제목 구성 요소를 사용하여 지정됩니다. 이 구성 요소는 양식 레이아웃에 추가할 수 있으며 양식의 용도나 주제에 맞게 해당 텍스트를 편집할 수 있습니다. 제목은 사용자를 위한 양식에 대한 레이블 또는 간략한 설명 역할을 하며 양식을 다른 양식과 구별하는 데 도움이 됩니다.

**예**

![](/help/adaptive-forms/assets/title.png)

## 사용 {#reasons-to-use-title-in-an-adaptive-form}

양식에서 제목을 사용하는 것이 좋은 것에는 다음과 같은 몇 가지 이유가 있습니다.

* **명확성**: 제목은 양식의 용도를 명확하게 식별하여 사용자가 제공해야 하는 정보를 이해하는 데 도움을 줍니다.

* **구성**: 제목을 사용하여 주제나 용도별로 양식을 구성할 수 있으므로 사용자가 필요한 양식을 쉽게 찾을 수 있습니다.

* **접근성**: 제목은 접근성이 필요한 사용자에게 중요한 요소입니다. 화면 판독기에서 제목을 큰 소리로 읽어 주면 사용자가 양식의 컨텍스트를 이해하는 데 도움이 되기 때문입니다.

* **브랜딩**: 제목을 사용하여 회사 또는 조직의 이름을 표시할 수도 있으며, 이는 사용자의 신뢰감과 친숙함을 형성하는 데 도움이 됩니다.

* **탐색**: 제목은 특히 양식이 길거나 복잡한 경우 양식을 탐색하는 데 유용할 수 있습니다.

* **검색 엔진 최적화(SEO)**: 검색 엔진이 제목을 사용하여 검색 쿼리에 대한 웹 페이지의 관련성을 결정하기 때문에, 양식에 제목을 지정하는 것도 SEO에 도움이 됩니다.

전체적으로 볼 때 양식의 제목은 사용자 경험의 중요한 측면이며, 제목을 사용하여 양식에 대한 명확하고 간결한 레이블을 제공하여 사용자가 양식의 컨텍스트와 목적을 이해하는 데 도움을 주어야 합니다.

## 버전 및 호환성 {#version-and-compatibility}

적응형 양식 아코디언 핵심 구성 요소는 Cloud Service의 핵심 구성 요소 2.0.4 및 AEM 6.5.16.0 Forms 이상의 핵심 구성 요소 1.1.12 일부로 2023년 2월에 릴리스되었습니다. 다음 표에서는 지원되는 모든 버전, AEM 호환성 및 해당 문서에 대한 링크를 보여 줍니다.

| 구성 요소 버전 | AEM as a Cloud Service | AEM 6.5.16.0 Forms 이상 |
|---|---|---|
| v1 | 호환 가능 <br>[2.0.4](/help/adaptive-forms/version.md) 및 이후 릴리스 | <br>[릴리스 1.1.12](/help/adaptive-forms/version.md) 이상과 호환합니다(2.0.0 이전 버전). |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/adaptive-forms/version.md) 문서를 참조하십시오.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## 기술 세부 정보 {#technical-details}

적응형 양식 제목 핵심 구성 요소에 대한 최신 정보는 [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/title/v1/title)의 기술 설명서에서 확인할 수 있습니다. 핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 확인하십시오.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자를 사용하여 방문자를 위한 제목 경험을 손쉽게 사용자 정의할 수 있습니다. 제목 옵션을 간편하게 정의하여 원활한 사용자 경험을 제공할 수도 있습니다.

![기본 탭](/help/adaptive-forms/assets/title_properties.png)

콘텐츠 작성자는 편집 대화 상자를 통해 제목 텍스트를 정의하고 제목 수준을 선택할 수 있습니다.

* **제목** - 제목을 사용하면 양식에서 구성 요소를 쉽게 식별할 수 있으며, 기본적으로 제목은 구성 요소 상단에 나타납니다. 제목을 추가하지 않으면 제목 텍스트 대신 구성 요소의 이름이 표시됩니다.
* **유형/크기** - 제목의 제목 수준을 정의합니다.
* **ID** - 이 옵션을 통해 HTML과 데이터 레이어에서 구성 요소의 고유 식별자를 제어할 수 있습니다.
   * 비워 두면 고유 ID는 자동으로 생성되고 결과 페이지 검사를 통해 발견될 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID가 변경되면 CSS, JS 및 데이터 레이어 추적에 영향을 미칠 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

디자인 탭은 날짜 선택기 구성 요소의 CSS 스타일을 정의하고 관리하는 데 사용됩니다.

### 제목

[제목] 탭을 사용하면 템플릿 작성자가 양식 작성자의 기본 및 허용된 HTML 제목 요소를 설정할 수 있습니다.

![디자인 대화 상자 제목 탭](/help/adaptive-forms/assets/title_heading.png)

* **허용된 제목 요소**: 템플릿 작성자가 양식 작성자가 제목에 사용할 수 있는 제목 요소를 선택할 수 있도록 하는 여러 옵션을 제공하는 목록입니다.

* **기본 제목 요소** - 제목 구성 요소의 기본 제목 요소를 설정하는 드롭다운 목록입니다.

### 스타일 탭 {#styles-tab}

탭은 구성 요소의 CSS 스타일을 정의하고 관리하는 데 사용됩니다. 적응형 양식 날짜 선택기 핵심 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

![디자인 대화 상자 제목 탭](/help/adaptive-forms/assets/title_styles.png)

* **기본 CSS 클래스**: 적응형 양식 날짜 선택기 핵심 구성 요소에 기본 CSS 클래스를 제공할 수 있습니다.

* **허용된 스타일**: 이름과 스타일을 나타내는 CSS 클래스를 제공하여 스타일을 정의할 수 있습니다. 예를 들어 “bold text”라는 스타일을 만들고 “font-weight: bold”라는 CSS 클래스를 제공할 수 있습니다. 적응형 양식 편집기에서 이러한 스타일을 적응형 양식에 사용하거나 적용할 수 있습니다. 스타일을 적용하려면 적응형 양식 편집기에서 스타일을 적용할 구성 요소를 선택하고 속성 대화 상자로 이동한 다음 **스타일** 드롭다운 목록에서 원하는 스타일을 선택합니다. 스타일을 업데이트하거나 수정해야 하는 경우 디자인 대화 상자로 돌아가서 스타일 탭에서 스타일을 업데이트하고 변경 내용을 저장하면 됩니다.

### 형식 탭 {#format-tab}

형식 탭에서는 기본 및 사용자 정의 날짜 형식을 지정할 수 있습니다.

![형식 탭](/help/adaptive-forms/assets/title_styles.png)

## 관련 문서 {#related-article}

* [AEM Sites 페이지 또는 경험 조각에서 적응형 양식 만들기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html)

* [독립 적응형 양식 만들기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

>[!MORELIKETHIS]
>
>* [아코디언](/help/adaptive-forms/components/accordion.md)
>* [버튼](/help/adaptive-forms/components/button.md)
>* [확인란 그룹](/help/adaptive-forms/components/checkbox-group.md)
>* [날짜 선택기](/help/adaptive-forms/components/date-picker.md)
>* [드롭다운 목록](/help/adaptive-forms/components/drop-down.md)
>* [이메일 입력](/help/adaptive-forms/components/email-input.md)
>* [양식 컨테이너](/help/adaptive-forms/components/form-container.md)
>* [첨부 파일](/help/adaptive-forms/components/file-attachment.md)
>* [바닥글](/help/adaptive-forms/components/footer.md)
>* [헤더](/help/adaptive-forms/components/header.md)
>* [가로 탭](/help/adaptive-forms/components/horizontal-tabs.md)
>* [이미지](/help/adaptive-forms/components/image.md)
>* [숫자 입력](/help/adaptive-forms/components/number-input.md)
>* [패널 컨테이너](/help/adaptive-forms/components/panel-container.md)
>* [라디오 버튼](/help/adaptive-forms/components/radio-button.md)
>* [재설정 버튼](/help/adaptive-forms/components/reset-button.md)
>* [제출 버튼](/help/adaptive-forms/components/submit-button.md)
>* [전화번호 입력](/help/adaptive-forms/components/telephone-input.md)
>* [텍스트 입력](/help/adaptive-forms/components/text-input.md)
>* [텍스트](/help/adaptive-forms/components/text.md)
>* [마법사](/help/adaptive-forms/components/wizard.md)

## 추가 참조 {#see-also}

{{see-also}}
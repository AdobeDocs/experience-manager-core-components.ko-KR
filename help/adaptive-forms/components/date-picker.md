---
title: 적응형 양식 핵심 구성 요소 - 날짜 선택기
description: 적응형 양식 날짜 선택기 핵심 구성 요소를 사용 또는 사용자 정의합니다.
role: Architect, Developer, Admin, User
exl-id: aa9402de-ca57-4c19-8d36-2dd0a78d6806
source-git-commit: be630c4d0a10ebaa679b77419b901fac818addb1
workflow-type: ht
source-wordcount: '1702'
ht-degree: 100%

---

# 날짜 선택기 {#date-picker-adaptive-forms-core-component}

적응형 양식의 날짜 선택기 구성 요소는 사용자가 달력에서 날짜를 선택하거나 특정 형식으로 날짜를 수동으로 입력할 수 있도록 하는 사용자 인터페이스 요소입니다. 다른 형식 지정, 유효성 검사 및 기본값을 갖도록 날짜 선택기 구성 요소를 구성할 수 있습니다.

**예**

![](/help/adaptive-forms/assets/date-picker.png)

## 사용 {#reasons-to-use-drop-date-picker}

적응형 양식에 날짜 선택기를 포함하는 것이 유익한 몇 가지 이유는 다음과 같습니다.

* **편의성**: 날짜 선택기 구성 요소를 사용하면 텍스트 필드에 날짜를 수동으로 입력하지 않고도 달력에서 날짜를 간편하게 선택할 수 있습니다. 이렇게 하면 시간을 절약하고 오류를 줄일 수 있습니다.

* **사용자 경험**: 날짜 선택기 구성 요소를 사용하면 사용자가 명확하고 직관적으로 날짜를 선택할 수 있으므로 양식을 보다 사용자 친화적으로 만들 수 있습니다.

* **데이터 분석**: 날짜 선택기 구성 요소를 사용하여 다양한 소스에서 데이터를 수집하고 분석하거나 추가 처리를 위한 입력으로 사용할 수 있습니다.

* **이벤트 관리**: 이벤트 관리 웹 사이트에서 날짜 선택기 구성 요소를 사용하여 이벤트 날짜를 선택할 수 있습니다.

* **예약**: 예약 웹 사이트에서 날짜 선택기 구성 요소를 사용하여 체크인 및 체크아웃 날짜를 선택할 수 있습니다.

* **날짜 형식**: 날짜 선택기 구성 요소를 사용하여 날짜가 표시되고 입력되는 형식을 수정할 수 있습니다. 일관된 사용자 경험을 위해 양식 전체에서 날짜 형식의 일관성을 유지해야 합니다.

## 버전 및 호환성 {#version-and-compatibility}

적응형 양식 아코디언 핵심 구성 요소는 Cloud Service의 핵심 구성 요소 2.0.4 및 AEM 6.5.16.0 Forms 이상의 핵심 구성 요소 1.1.12 일부로 2023년 2월에 릴리스되었습니다. 다음 표에서는 지원되는 모든 버전, AEM 호환성 및 해당 문서에 대한 링크를 보여 줍니다.

| 구성 요소 버전 | AEM as a Cloud Service | AEM 6.5.16.0 Forms 이상 |
|---|---|---|
| v1 | 호환 가능 <br>[2.0.4](/help/adaptive-forms/version.md) 및 이후 릴리스 | <br>[릴리스 1.1.12](/help/adaptive-forms/version.md) 이상과 호환합니다(2.0.0 이전 버전). |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/adaptive-forms/version.md) 문서를 참조하십시오.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## 기술 세부 정보 {#technical-details}

적응형 양식 날짜 선택기 핵심 구성 요소에 대한 최신 정보는 [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/datepicker/v1/datepicker)의 기술 설명서에서 확인할 수 있습니다. 핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 확인하십시오.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자를 사용하여 방문자를 위한 날짜 선택기 경험을 손쉽게 사용자 정의할 수 있습니다. 날짜 선택기 옵션을 간편하게 정의하여 원활한 사용자 경험을 제공할 수도 있습니다.

### 기본 탭 {#basic-tab}

![기본 탭](/help/adaptive-forms/assets/datepicker_basictab.png)

* **이름** - 이름은 규칙 편집기에서 구성 요소를 고유하게 식별합니다. 이름 문자열에는 특수 문자나 공백이 포함되어서는 안 됩니다.

* **제목** - 제목은 적응형 양식의 구성 요소 상단에 표시되는 문자열입니다. 제목은 적응형 양식의 트리 구조에서 구성 요소를 고유하게 식별합니다. 제목을 추가하지 않으면 제목 텍스트 대신 구성 요소의 이름이 표시됩니다.

* **제목 숨기기** - 적응형 양식에서 구성 요소 유형의 제목을 숨기려면 이 옵션을 선택합니다.

* **플레이스홀더 텍스트** - 양식 구성 요소의 플레이스홀더 텍스트는 입력 필드에 입력할 것으로 예상되는 정보 유형에 대한 힌트로 입력 필드 내에 표시되는 간단한 레이블 또는 프롬프트를 나타냅니다. 플레이스홀더 텍스트는 사용자가 필드에 입력을 시작하면 사라지고 필드가 비어 있으면 다시 나타납니다. 사용자에게 시각적인 단서를 제공하지만 필드에 대한 영구적인 레이블 또는 값으로 작동하지는 않습니다.

* **구성 요소 숨기기** - 양식에서 구성 요소를 숨기려면 이 옵션을 선택합니다. 구성 요소는 다른 용도로(예: 규칙 편집기에서 계산에 사용) 계속 액세스할 수 있습니다. 구성 요소 숨기기는 사용자가 보거나 직접 변경할 필요가 없는 정보를 저장해야 할 때 유용합니다.
* **구성 요소 비활성화** - 구성 요소를 비활성화하려면 이 옵션을 선택합니다. 비활성화된 구성 요소는 활성 상태가 아니므로 최종 사용자가 편집할 수 없습니다. 사용자는 필드 값을 볼 수 있지만 수정할 수는 없습니다. 구성 요소는 다른 용도로(예: 규칙 편집기에서 계산에 사용) 계속 액세스할 수 있습니다.
* **읽기 전용** - 구성 요소를 편집할 수 없도록 만들려면 이 옵션을 선택합니다. 사용자는 필드 값을 볼 수 있지만 수정할 수는 없습니다. 구성 요소는 다른 용도로(예: 규칙 편집기에서 계산에 사용) 계속 액세스할 수 있습니다.
* **기본 날짜** - 이 옵션을 사용하면 양식 필드에 날짜를 추가할 수 있습니다. 입력한 날짜는 기본적으로 구성 요소 위치에 나타납니다. 사용자가 날짜를 입력하지 않으면 이 값이 양식 제출 시 함께 제출됩니다. **비활성화된 구성 요소** 또는 **읽기 전용 구성 요소**&#x200B;를 선택한 경우 기본 날짜가 화면에 표시되며 양식 제출 시 함께 제출됩니다.


### 유효성 검사 탭 {#validation-tab}

![유효성 검사 탭](/help/adaptive-forms/assets/datepicker_validation.png)

* **필수** - 적응형 양식에 구성 요소를 표시하려면 이 옵션을 선택합니다. 이 옵션이 선택되어 있으면 **기본** 탭에서 **구성 요소 숨기기** 또는 **구성 요소 비활성화**&#x200B;를 선택할 수 없습니다.

* **오류 메시지** - 이 옵션을 사용하면 **필수** 확인란이 선택되어 있고 양식 필드가 비어 있는 경우 표시되는 메시지를 입력할 수 있습니다.

* **스크립트 유효성 검사 메시지** - 이 옵션을 사용하면 스크립트 유효성 검사가 실패할 경우 표시할 메시지를 입력할 수 있습니다.

* **최소 날짜** - 이 옵션을 사용하면 최소 필수 날짜를 입력할 수 있습니다. 최소 날짜에 지정된 날짜 이전의 날짜를 입력하면 화면에 오류 메시지가 표시됩니다. **최소 오류 메시지** 대화 상자에서 사용자 정의 오류 메시지를 추가할 수 있습니다.

* **최소 오류 메시지** - **최소 날짜** 옵션에 지정된 날짜 이전의 날짜를 입력한 경우, **최소 오류 메시지** 대화 상자를 사용하면 표시할 사용자 정의 오류 메시지를 추가할 수 있습니다.

* **최대 날짜** - 이 옵션을 사용하면 최대 필수 날짜를 입력할 수 있습니다. 최대 날짜에 지정된 날짜 이후의 날짜를 입력하면 화면에 오류 메시지가 표시됩니다. **최대 오류 메시지** 대화 상자에서 사용자 정의 오류 메시지를 추가할 수 있습니다.

* **최대 오류 메시지** - **최대 날짜** 옵션에 지정된 날짜 이후의 날짜를 입력한 경우, **최대 오류 메시지** 대화 상자를 사용하면 표시할 사용자 정의 오류 메시지를 추가할 수 있습니다.


### 도움말 콘텐츠 탭 {#help-content-tab}

![도움말 콘텐츠 탭](/help/adaptive-forms/assets/datepicker_helptab.png)

* **간단한 설명** - 간단한 설명은 특정 양식 필드의 용도에 대한 추가 정보 또는 설명을 제공하는 간단한 텍스트 설명입니다. 사용자가 필드에 입력해야 하는 데이터 유형을 이해하는 데 도움이 되며 입력된 정보가 유효하고 원하는 기준을 충족하는지 확인하는 데 도움이 되는 지침 또는 예시를 제공할 수 있습니다. 기본적으로 간단한 설명은 숨겨진 상태로 유지됩니다. **간단한 설명 항상 표시** 옵션을 활성화하여 구성 요소 아래에 표시할 수 있습니다.

* **간단한 설명 항상 표시** - 이 옵션을 활성화하여 구성 요소 아래에 간단한 설명을 표시할 수 있습니다.

* **도움말 텍스트** - 도움말 텍스트는 양식 필드를 올바르게 작성하는 데 도움이 되도록 사용자에게 제공되는 추가 정보 또는 지침을 나타냅니다. 구성 요소 옆에 있는 도움말 아이콘(i)을 클릭하면 표시됩니다. 도움말 텍스트는 양식 필드의 레이블이나 플레이스홀더 텍스트보다 더 자세한 정보를 제공하며 사용자가 필드의 요구 사항이나 제한 사항을 이해하는 데 도움이 되도록 설계되었습니다. 또한 양식을 보다 쉽고 정확하게 작성할 수 있도록 제안이나 예시를 제공할 수도 있습니다.


### 접근성 탭 {#accessibility-tab}

![접근성 탭](/help/adaptive-forms/assets/datepicker_accessibilitytab.png)

**화면 판독기용 텍스트** - 화면 판독기용 텍스트는 시각 장애인이 사용하는 화면 판독기와 같은 보조 기술로 읽을 수 있도록 특별히 고안된 추가 텍스트를 나타냅니다. 이 텍스트는 양식 필드의 용도에 대한 오디오 설명을 제공하며, 여기에는 필드의 제목, 설명, 이름 및 관련 메시지(사용자 정의 텍스트)에 대한 정보가 포함될 수 있습니다. 화면 판독기 텍스트는 시각 장애가 있는 사용자를 포함한 모든 사용자가 양식에 액세스할 수 있도록 돕고 양식 필드 및 해당 요구 사항을 완전히 이해할 수 있도록 합니다.

### 형식 탭 {#format-tab}

![형식 탭](/help/adaptive-forms/assets/datepicker_formattab.png)

* **표시 형식** - 사용자에게 표시되는 날짜 형식을 나타냅니다. **유형** 옵션을 사용하면 날짜 형식을 선택할 수 있습니다. **유형** 드롭다운 메뉴의 **사용자 정의** 옵션을 사용하여 날짜 형식을 사용자 정의할 수도 있습니다.

* **편집 형식** - 사용자가 날짜를 편집할 수 있는 날짜 형식을 나타냅니다. **유형** 옵션을 사용하면 날짜 형식을 선택할 수 있습니다. **유형** 드롭다운 메뉴의 **사용자 정의** 옵션을 사용하여 날짜 형식을 사용자 정의할 수도 있습니다.

* **표시 형식** - 사용자에게 표시되는 날짜 형식을 나타냅니다. 유형 옵션을 사용하면 날짜 형식을 선택할 수 있습니다. **유형** 드롭다운 메뉴의 **사용자 정의** 옵션을 사용하여 날짜 형식을 사용자 정의할 수도 있습니다.

* **편집 형식** - 사용자가 날짜를 편집하는 날짜 형식을 나타냅니다. 유형 옵션을 사용하면 날짜 형식을 선택할 수 있습니다. **유형** 드롭다운 메뉴의 **사용자 정의** 옵션을 사용하여 날짜 형식을 사용자 정의할 수도 있습니다.

## 디자인 대화 상자 {#design-dialog}

디자인 대화 상자는 날짜 선택기 구성 요소의 CSS 스타일을 정의하고 관리하는 데 사용됩니다.

### 스타일 탭 {#styles-tab}

탭은 구성 요소의 CSS 스타일을 정의하고 관리하는 데 사용됩니다. 적응형 양식 날짜 선택기 핵심 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

![스타일 탭](/help/adaptive-forms/assets/datepicker_styletab.png)

* **기본 CSS 클래스**: 적응형 양식 날짜 선택기 핵심 구성 요소에 기본 CSS 클래스를 제공할 수 있습니다.

* **허용된 스타일**: 이름과 스타일을 나타내는 CSS 클래스를 제공하여 스타일을 정의할 수 있습니다. 예를 들어 “bold text”라는 스타일을 만들고 “font-weight: bold”라는 CSS 클래스를 제공할 수 있습니다. 적응형 양식 편집기에서 이러한 스타일을 적응형 양식에 사용하거나 적용할 수 있습니다. 스타일을 적용하려면 적응형 양식 편집기에서 스타일을 적용할 구성 요소를 선택하고 속성 대화 상자로 이동한 다음 **스타일** 드롭다운 목록에서 원하는 스타일을 선택합니다. 스타일을 업데이트하거나 수정해야 하는 경우 디자인 대화 상자로 돌아가서 스타일 탭에서 스타일을 업데이트하고 변경 내용을 저장하면 됩니다.

### 형식 탭 {#formats-tab}

형식 탭에서는 기본 및 사용자 정의 날짜 형식을 지정할 수 있습니다.

![형식 탭](/help/adaptive-forms/assets/datepicker_formatpolicy.png)

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->


>[!MORELIKETHIS]
>
>* [아코디언](/help/adaptive-forms/components/accordion.md)
>* [버튼](/help/adaptive-forms/components/button.md)
>* [확인란 그룹](/help/adaptive-forms/components/checkbox-group.md)
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
>* [제목](/help/adaptive-forms/components/title.md)
>* [마법사](/help/adaptive-forms/components/wizard.md)

## 추가 참조 {#see-also}

{{see-also}}
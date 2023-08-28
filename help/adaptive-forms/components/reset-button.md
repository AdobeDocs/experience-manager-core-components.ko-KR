---
title: 적응형 양식 핵심 구성 요소 - 재설정 버튼
description: 적응형 양식 재설정 버튼 핵심 구성 요소를 사용 또는 사용자 정의합니다.
role: Architect, Developer, Admin, User
exl-id: e5aa9d89-aece-491e-80a1-7fb9ea6c4b60
source-git-commit: ad3e3bca5cb46f14e864e4704c90ac3b62779794
workflow-type: tm+mt
source-wordcount: '1266'
ht-degree: 99%

---

# 재설정 {#reset-button}

적응형 양식의 재설정 버튼은 사용자가 모든 양식 필드를 지우거나 기본값으로 재설정할 수 있도록 하는 버튼입니다. 재설정 버튼을 클릭하면 양식 필드에 입력된 모든 데이터가 삭제되고 필드가 원래 상태로 돌아갑니다. 재설정 버튼은 일반적으로 제출 버튼의 대안으로 사용되며 사용자가 양식에 부정확하거나 원치 않는 데이터를 입력한 경우 다시 시작할 수 있는 방법을 제공합니다.


## 사용 {#reasons-to-use-reset-button}

적응형 양식에서 재설정 버튼을 사용하는 데에는 다음과 같은 이유가 있습니다.

* **사용자 편의성**: 재설정 버튼은 사용자가 각 필드를 수동으로 삭제하지 않고도 양식을 지우고 다시 시작할 수 있는 빠르고 쉬운 방법을 제공합니다.

* **유용성 개선**: 재설정 버튼은 사용자가 간편하게 실수를 수정하거나 입력 내용을 변경할 수 있도록 하여 사용자 경험을 개선할 수 있습니다.

* **오류 방지**: 사용자는 재설정 버튼을 사용하여 실수로 잘못된 데이터를 제출하여 오류나 처리 문제를 일으킬 수 있는 것을 방지할 수 있습니다.

* **일관성**: 재설정 버튼은 양식의 일반적인 기능이므로 양식에 재설정 버튼을 포함하면 사용자 경험의 일관성을 유지할 수 있습니다.

* **더 나은 데이터 관리**: 재설정 버튼을 사용하면 사용자가 일관되지 않거나 잘못된 데이터를 제출할 가능성이 줄어들기 때문에 양식 데이터를 체계적이고 정확하게 유지할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

적응형 양식 아코디언 핵심 구성 요소는 Cloud Service의 핵심 구성 요소 2.0.4 및 AEM 6.5.16.0 Forms 이상의 핵심 구성 요소 1.1.12 일부로 2023년 2월에 릴리스되었습니다. 다음 표에서는 지원되는 모든 버전, AEM 호환성 및 해당 문서에 대한 링크를 보여 줍니다.

| 구성 요소 버전 | AEM as a Cloud Service | AEM 6.5.16.0 Forms 이상 |
|---|---|---|
| v1 | 호환 가능 <br>[2.0.4](/help/adaptive-forms/version.md) 및 이후 릴리스 | <br>[릴리스 1.1.12](/help/adaptive-forms/version.md) 이상과 호환합니다(2.0.0 이전 버전). |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/adaptive-forms/version.md) 문서를 참조하십시오.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## 기술 세부 정보 {#technical-details}

적응형 양식 재설정 버튼 핵심 구성 요소에 대한 최신 정보는 [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/button/v1/button)의 기술 설명서에서 확인할 수 있습니다. 핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 확인하십시오.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자를 사용하여 방문자를 위한 재설정 버튼 경험을 손쉽게 사용자 정의할 수 있습니다. 재설정 버튼 옵션을 간편하게 정의하여 원활한 사용자 경험을 제공할 수도 있습니다.

### 기본 탭 {#basic-tab}

![기본 탭](/help/adaptive-forms/assets/button_basictab.png)

* **이름** - 양식과 규칙 편집기 모두에서 고유한 이름으로 양식 구성 요소를 쉽게 식별할 수 있습니다. 단, 이름에는 공백이나 특수 문자가 포함되어서는 안 됩니다.

* **제목** - 제목을 사용하면 양식에서 구성 요소를 쉽게 식별할 수 있으며, 기본적으로 제목은 구성 요소 상단에 나타납니다. 제목을 추가하지 않으면 제목 텍스트 대신 구성 요소의 이름이 표시됩니다.

* **바인드 참조** - 바인드 참조는 외부 데이터 소스에 저장되고 양식에서 사용되는 데이터 요소에 대한 참조입니다. 바인드 참조를 사용하면 데이터를 양식 필드에 동적으로 바인딩하여 양식이 데이터 소스의 최신 데이터를 표시하도록 할 수 있습니다. 예를 들어 바인드 참조를 사용하여 양식에 입력된 고객의 ID를 기반으로 고객의 이름과 주소를 양식에 표시할 수 있습니다. 바인드 참조를 사용하여 양식에 입력된 데이터로 데이터 소스를 업데이트할 수도 있습니다. 이러한 방식으로 AEM Forms를 사용하면 외부 데이터 소스와 상호 작용하는 양식을 만들어 데이터 수집 및 관리를 위한 원활한 사용자 경험을 제공할 수 있습니다.

* **구성 요소 숨기기** - 양식에서 구성 요소를 숨기려면 이 옵션을 선택합니다. 구성 요소는 다른 용도로(예: 규칙 편집기에서 계산에 사용) 계속 액세스할 수 있습니다. 구성 요소 숨기기는 사용자가 보거나 직접 변경할 필요가 없는 정보를 저장해야 할 때 유용합니다.
* **구성 요소 비활성화** - 구성 요소를 비활성화하려면 이 옵션을 선택합니다. 비활성화된 구성 요소는 활성 상태가 아니므로 최종 사용자가 편집할 수 없습니다. 사용자는 필드 값을 볼 수 있지만 수정할 수는 없습니다. 구성 요소는 다른 용도로(예: 규칙 편집기에서 계산에 사용) 계속 액세스할 수 있습니다.
* **읽기 전용** - 구성 요소를 편집할 수 없도록 만들려면 이 옵션을 선택합니다. 사용자는 필드 값을 볼 수 있지만 수정할 수는 없습니다. 구성 요소는 다른 용도로(예: 규칙 편집기에서 계산에 사용) 계속 액세스할 수 있습니다.

### 도움말 콘텐츠 탭 {#help-content}

![도움말 콘텐츠 탭](/help/adaptive-forms/assets/button_helptab.png)

* **간단한 설명** - 간단한 설명은 특정 양식 필드의 용도에 대한 추가 정보 또는 설명을 제공하는 간단한 텍스트 설명입니다. 사용자가 필드에 입력해야 하는 데이터 유형을 이해하는 데 도움이 되며 입력된 정보가 유효하고 원하는 기준을 충족하는지 확인하는 데 도움이 되는 지침 또는 예시를 제공할 수 있습니다. 기본적으로 간단한 설명은 숨겨진 상태로 유지됩니다. **간단한 설명 항상 표시** 옵션을 활성화하여 구성 요소 아래에 표시할 수 있습니다.

* **간단한 설명 항상 표시** - 이 옵션을 활성화하여 구성 요소 아래에 간단한 설명을 표시할 수 있습니다.

* **도움말 텍스트** - 도움말 텍스트는 양식 필드를 올바르게 작성하는 데 도움이 되도록 사용자에게 제공되는 추가 정보 또는 지침을 나타냅니다. 구성 요소 옆에 있는 도움말 아이콘(i)을 클릭하면 표시됩니다. 도움말 텍스트는 양식 필드의 레이블이나 플레이스홀더 텍스트보다 더 자세한 정보를 제공하며 사용자가 필드의 요구 사항이나 제한 사항을 이해하는 데 도움이 되도록 설계되었습니다. 또한 양식을 보다 쉽고 정확하게 작성할 수 있도록 제안이나 예시를 제공할 수도 있습니다.

### 접근성 {#accessibility}

![접근성 탭](/help/adaptive-forms/assets/button_accessibilitytab.png)


**화면 판독기용 텍스트** - 화면 판독기용 텍스트는 시각 장애인이 사용하는 화면 판독기와 같은 보조 기술로 읽을 수 있도록 특별히 고안된 추가 텍스트를 나타냅니다. 이 텍스트는 양식 필드의 용도에 대한 오디오 설명을 제공하며, 여기에는 필드의 제목, 설명, 이름 및 관련 메시지(사용자 정의 텍스트)에 대한 정보가 포함될 수 있습니다. 화면 판독기 텍스트는 시각 장애가 있는 사용자를 포함한 모든 사용자가 양식에 액세스할 수 있도록 돕고 양식 필드 및 해당 요구 사항을 완전히 이해할 수 있도록 합니다.

## 디자인 대화 상자 {#design-dialog}

디자인 대화 상자는 재설정 버튼 구성 요소의 CSS 스타일을 정의하고 관리하는 데 사용됩니다.


### 스타일 탭 {#styles-tab}

탭은 구성 요소의 CSS 스타일을 정의하고 관리하는 데 사용됩니다. 적응형 양식 재설정 버튼 핵심 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

![디자인 대화 상자](/help/adaptive-forms/assets/reset_designdialog.png)

* **기본 CSS 클래스**: 적응형 양식 재설정 버튼 핵심 구성 요소에 기본 CSS 클래스를 제공할 수 있습니다.

* **허용된 스타일**: 이름과 스타일을 나타내는 CSS 클래스를 제공하여 스타일을 정의할 수 있습니다. 예를 들어 “bold text”라는 스타일을 만들고 “font-weight: bold”라는 CSS 클래스를 제공할 수 있습니다. 적응형 양식 편집기에서 이러한 스타일을 적응형 양식에 사용하거나 적용할 수 있습니다. 스타일을 적용하려면 적응형 양식 편집기에서 스타일을 적용할 구성 요소를 선택하고 속성 대화 상자로 이동한 다음 **스타일** 드롭다운 목록에서 원하는 스타일을 선택합니다. 스타일을 업데이트하거나 수정해야 하는 경우 디자인 대화 상자로 돌아가서 스타일 탭에서 스타일을 업데이트하고 변경 내용을 저장하면 됩니다.

## 관련 문서 {#related-article}

* [AEM Sites 페이지 또는 경험 조각에서 적응형 양식 만들기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html)

* [독립 적응형 양식 만들기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)


## 참조: {#see-also}

* [아코디언](/help/adaptive-forms/components/accordion.md)
* [버튼](/help/adaptive-forms/components/button.md)
* [확인란 그룹](/help/adaptive-forms/components/checkbox-group.md)
* [날짜 선택기](/help/adaptive-forms/components/date-picker.md)
* [드롭다운 목록](/help/adaptive-forms/components/drop-down.md)
* [이메일 입력](/help/adaptive-forms/components/email-input.md)
* [양식 컨테이너](/help/adaptive-forms/components/form-container.md)
* [첨부 파일](/help/adaptive-forms/components/file-attachment.md)
* [바닥글](/help/adaptive-forms/components/footer.md)
* [헤더](/help/adaptive-forms/components/header.md)
* [가로 탭](/help/adaptive-forms/components/horizontal-tabs.md)
* [이미지](/help/adaptive-forms/components/image.md)
* [숫자 입력](/help/adaptive-forms/components/number-input.md)
* [패널 컨테이너](/help/adaptive-forms/components/panel-container.md)
* [라디오 버튼](/help/adaptive-forms/components/radio-button.md)
* [제출 버튼](/help/adaptive-forms/components/submit-button.md)
* [전화번호 입력](/help/adaptive-forms/components/telephone-input.md)
* [텍스트 입력](/help/adaptive-forms/components/text-input.md)
* [텍스트](/help/adaptive-forms/components/text.md)
* [제목](/help/adaptive-forms/components/title.md)
* [마법사](/help/adaptive-forms/components/wizard.md)
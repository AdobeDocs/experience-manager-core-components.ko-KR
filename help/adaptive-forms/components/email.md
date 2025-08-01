---
title: 적응형 양식 핵심 구성 요소 - 이메일 입력
description: 적응형 양식 이메일 입력 핵심 구성 요소를 사용 또는 사용자 정의합니다.
role: Architect, Developer, Admin, User
exl-id: f6a2974b-991e-4cea-9ef8-0b03e8975eeb
source-git-commit: 6725784bd4c94d433c91d6bd65d14d03cbefd954
workflow-type: ht
source-wordcount: '2111'
ht-degree: 100%

---


# 이메일 구성 요소 {#Email-input-adaptive-forms-core-component}

적응형 양식 이메일 입력 핵심 구성 요소는 사용자로부터 이메일 주소를 수집하는 데 사용됩니다. 이메일 입력 필드를 통해 브라우저는 입력된 데이터가 유효한 이메일 주소 형식인지 확인할 수 있습니다. 일반적으로 텍스트 상자로 표시되며 유효한 이메일 주소만 허용하는 패턴 유효성 검사가 있습니다. 이메일 입력 필드를 추가로 사용자 정의하여 입력 데이터에 대한 유효성 검사를 설정하기 위해 “필수”, “플레이스홀더” 및 “패턴”과 같은 추가 속성을 사용할 수 있습니다.

{{traditional-aem}}

**예**

![예](/help/adaptive-forms/assets/emailid-example.png)

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion_kr). -->

적응형 양식에 이메일 입력 구성 요소를 포함하는 것이 유익한 몇 가지 이유는 다음과 같습니다.

- **사용자 편의성**: 이메일 입력은 예상되는 데이터를 필드에 명확하게 표시하므로 사용자가 이메일 주소를 더 쉽게 입력할 수 있습니다.

- **개인화된 커뮤니케이션**: 양식을 통해 사용자로부터 이메일 주소를 수집하면 확인 이메일 또는 뉴스레터 전송과 같은 개인화된 커뮤니케이션이 가능합니다.

- **리드 생성**: 기업은 양식을 통해 이메일 주소를 수집하여 이메일 목록을 작성하고 리드 생성에 사용할 수 있습니다.

- **사용자 인증**: 제한된 콘텐츠나 서비스에 액세스하기 위한 인증 수단으로 이메일 주소를 사용할 수 있습니다.

- **피드백 수집**: 기업은 피드백 양식의 이메일 입력을 통해 피드백에 대한 후속 조치 또는 설명을 위해 사용자와 통신할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

적응형 양식 이메일 핵심 구성 요소는 Cloud Service의 핵심 구성 요소 2.0.4 및 AEM 6.5.16.0 Forms 이상의 핵심 구성 요소 1.1.12 일부로 2023년 2월에 릴리스되었습니다. 다음 테이블에서는 지원되는 모든 버전, AEM 호환성 및 해당 문서에 대한 링크를 보여 줍니다.

| 구성 요소 버전 | AEM as a Cloud Service | AEM 6.5.16.0 Forms 이상 |
|---|---|---|
| v1 | <br>[릴리스 2.0.4](/help/adaptive-forms/version.md) 이상 버전과 호환 가능 | <br>[릴리스 1.1.12](/help/adaptive-forms/version.md) 이상과 호환합니다(2.0.0 이전 버전). |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/adaptive-forms/version.md) 문서를 참조하십시오.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion_kr). -->

## 기술 세부 정보 {#technical-details}

적응형 양식 이메일 입력 핵심 구성 요소에 대한 최신 정보는 [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/emailinput/v1/emailinput)의 기술 설명서에서 확인할 수 있습니다. 핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 확인하십시오.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자를 사용하여 방문자를 위한 이메일 입력 경험을 손쉽게 사용자 정의할 수 있습니다. 이메일 입력 옵션을 간편하게 정의하여 원활한 사용자 경험을 제공할 수도 있습니다.

### 기본 탭 {#basic-tab}

![기본 탭](/help/adaptive-forms/assets/email_basictab.png)

- **이름** - 이름은 규칙 편집기에서 구성 요소를 고유하게 식별합니다. 이름 문자열에는 특수 문자나 공백이 포함되어서는 안 됩니다.

- **제목** - 제목을 사용하면 양식에서 구성 요소를 쉽게 식별할 수 있으며, 기본적으로 제목은 구성 요소 상단에 나타납니다. 제목을 추가하지 않으면 제목 텍스트 대신 구성 요소의 이름이 표시됩니다.
- **제목에 대해 서식 있는 텍스트 허용** - 이 기능을 사용하면 사용자가 굵게, 기울임꼴, 밑줄 친 텍스트, 다양한 글꼴, 글꼴 크기, 색상, 추가 옵션과 같은 기능을 통합해 일반 텍스트 제목의 서식을 지정하여 시각적 표현 및 사용자 정의를 향상할 수 있습니다. 더 큰 유연성과 창의적인 제어 기능으로 문서, 웹 사이트 또는 애플리케이션 내에서 제목을 돋보이게 할 수 있습니다.\
  **제목에 대해 서식 있는 텍스트 허용** 확인란을 선택하면 구성 요소 제목의 스타일을 지정할 수 있는 서식 지정 옵션이 표시됩니다. 사용 가능한 모든 서식 옵션에 액세스하려면 ![전체 화면 아이콘](/help/adaptive-forms/assets/fullscreen-icon.png) 탭을 클릭하면 됩니다.

  ![서식 있는 텍스트 지원](/help/adaptive-forms/assets/richtext-support-title.png)

- **제목 숨기기** - 구성 요소의 제목을 숨기려면 이 옵션을 선택합니다.

- **플레이스홀더 텍스트** - 양식 구성 요소의 플레이스홀더 텍스트는 입력 필드에 입력할 것으로 예상되는 정보 유형에 대한 힌트로 입력 필드 내에 표시되는 간단한 레이블 또는 프롬프트를 나타냅니다. 플레이스홀더 텍스트는 사용자가 필드에 입력을 시작하면 사라지고 필드가 비어 있으면 다시 나타납니다. 사용자에게 시각적인 단서를 제공하지만 필드에 대한 영구적인 레이블 또는 값으로 작동하지는 않습니다.
- **바인드 참조** - 바인드 참조는 외부 데이터 소스에 저장되고 양식에서 사용되는 데이터 요소에 대한 참조입니다. 바인드 참조를 사용하면 데이터를 양식 필드에 동적으로 바인딩하여 양식이 데이터 소스의 최신 데이터를 표시하도록 할 수 있습니다. 예를 들어 바인드 참조를 사용하여 양식에 입력된 고객의 ID를 기반으로 고객의 이름과 주소를 양식에 표시할 수 있습니다. 바인드 참조를 사용하여 양식에 입력된 데이터로 데이터 소스를 업데이트할 수도 있습니다. 이러한 방식으로 AEM Forms를 사용하면 외부 데이터 소스와 상호 작용하는 양식을 만들어 데이터 수집 및 관리를 위한 원활한 사용자 경험을 제공할 수 있습니다.
- **언바운드 양식 요소로 표시**: 어떤 스키마에도 연결되지 않은 양식 필드를 구성하려면 이 옵션을 선택합니다. 이 옵션을 사용하면 데이터 소스를 업데이트하지 않고도 데이터를 저장할 수 있습니다. 또한 표준 데이터베이스 통합과 별도로 사용자 정의 방식으로 데이터를 처리할 수 있습니다.
- **구성 요소 숨기기** - 양식에서 구성 요소를 숨기려면 이 옵션을 선택합니다. 구성 요소는 다른 용도로(예: 규칙 편집기에서 계산에 사용) 계속 액세스할 수 있습니다. 구성 요소 숨기기는 사용자가 보거나 직접 변경할 필요가 없는 정보를 저장해야 할 때 유용합니다.
- **구성 요소 비활성화** - 구성 요소를 비활성화하려면 이 옵션을 선택합니다. 비활성화된 구성 요소는 활성 상태가 아니므로 최종 사용자가 편집할 수 없습니다. 사용자는 필드 값을 볼 수 있지만 수정할 수는 없습니다. 구성 요소는 다른 용도로(예: 규칙 편집기에서 계산에 사용) 계속 액세스할 수 있습니다.
- **읽기 전용** - 구성 요소를 편집할 수 없도록 만들려면 이 옵션을 선택합니다. 사용자는 필드 값을 볼 수 있지만 수정할 수는 없습니다. 구성 요소는 다른 용도로(예: 규칙 편집기에서 계산에 사용) 계속 액세스할 수 있습니다.

- **기본값** - 이 옵션을 사용하면 양식 필드에 기본값을 추가할 수 있습니다. **비활성화된 구성 요소** 또는 **읽기 전용 구성 요소**&#x200B;를 선택하면 화면에 기본값이 표시됩니다. 사용자가 양식 필드에 값을 입력하지 않으면 이 값이 양식 제출 시 함께 제출됩니다.
- **자동 채우기 속성**: 이 옵션을 사용하면 저장된 정보를 기반으로 양식 필드 내에 자동으로 채워지는 값을 사용자가 입력할 수 있습니다.

### 유효성 검사 탭 {#validation-tab}

![유효성 검사 탭](/help/adaptive-forms/assets/email_validationtab.png)

- **필수** - 적응형 양식에 구성 요소를 표시하려면 이 옵션을 선택합니다. 이 옵션을 선택하면 양식 제출을 진행하기 전에 값을 입력해야 합니다. 이 옵션이 선택되어 있으면 **기본** 탭에서 **구성 요소 숨기기** 또는 **구성 요소 비활성화**&#x200B;를 선택할 수 없습니다.

- **오류 메시지** - 이 옵션을 사용하면 **필수** 확인란이 선택되어 있고 양식 필드가 비어 있는 경우 표시되는 메시지를 입력할 수 있습니다.

- **스크립트 유효성 검사 메시지** - 이 옵션을 사용하면 스크립트 유효성 검사가 실패할 경우 표시할 메시지를 입력할 수 있습니다.

- **최대 문자 수** - 이 옵션을 사용하면 필드에 허용되는 최대 문자 수를 지정할 수 있습니다. **최대 문자 수**&#x200B;에 지정된 값보다 큰 문자를 입력하면 화면에 오류 메시지가 표시됩니다. **최대 문자 오류 메시지** 대화 상자에서 사용자 정의 오류 메시지를 추가할 수 있습니다.

- **최대 문자 오류 메시지** - **최대 문자 수** 옵션에 지정된 값보다 큰 문자를 입력한 경우, **최대 문자 오류 메시지** 대화 상자를 사용하면 표시할 사용자 정의 오류 메시지를 추가할 수 있습니다.

- **최소 문자 수** - 이 옵션을 사용하면 필드에 허용되는 최소 문자 수를 지정할 수 있습니다. **최소 문자 수**&#x200B;에 지정된 값보다 작은 문자를 입력하면 화면에 오류 메시지가 표시됩니다. **최소 문자 오류 메시지** 대화 상자에서 사용자 정의 오류 메시지를 추가할 수 있습니다.

- **최소 문자 오류 메시지** - **최소 문자 수** 옵션에 지정된 값보다 작은 문자를 입력한 경우, **최소 문자 오류 메시지** 대화 상자를 사용하면 표시할 사용자 정의 오류 메시지를 추가할 수 있습니다.
<br>

**유효성 검사 패턴** 옵션을 사용하면 입력한 이메일 ID의 유효성을 검사하는 패턴을 입력할 수 있습니다. 이메일 ID가 **패턴** 옵션에 입력된 값으로 유효성 검사에 실패한 경우 화면에 오류 메시지가 표시됩니다.

- **패턴** - 이 옵션을 사용하면 이메일에 대해 허용된 확인 패턴을 입력할 수 있습니다. 정규 표현식도 허용됩니다.
- **오류 메시지** - 이 옵션을 사용하면 이메일 ID가 **패턴** 옵션에 입력된 값으로 유효성 검사에 실패할 경우 화면에 표시되는 메시지를 입력할 수 있습니다.

### 도움말 콘텐츠 탭 {#help-content-tab}

![도움말 콘텐츠 탭](/help/adaptive-forms/assets/email_helptab.png)

- **간단한 설명** - 간단한 설명은 특정 양식 필드의 용도에 대한 추가 정보 또는 설명을 제공하는 간단한 텍스트 설명입니다. 사용자가 필드에 입력해야 하는 데이터 유형을 이해하는 데 도움이 되며 입력된 정보가 유효하고 원하는 기준을 충족하는지 확인하는 데 도움이 되는 지침 또는 예시를 제공할 수 있습니다. 기본적으로 간단한 설명은 숨겨진 상태로 유지됩니다. **간단한 설명 항상 표시** 옵션을 활성화하여 구성 요소 아래에 표시할 수 있습니다.

- **간단한 설명 항상 표시** - 이 옵션을 활성화하여 구성 요소 아래에 간단한 설명을 표시할 수 있습니다.

- **도움말 텍스트** - 도움말 텍스트는 양식 필드를 올바르게 작성하는 데 도움이 되도록 사용자에게 제공되는 추가 정보 또는 지침을 나타냅니다. 구성 요소 옆에 있는 도움말 아이콘(i)을 클릭하면 표시됩니다. 도움말 텍스트는 양식 필드의 레이블이나 플레이스홀더 텍스트보다 더 자세한 정보를 제공하며 사용자가 필드의 요구 사항이나 제한 사항을 이해하는 데 도움이 되도록 설계되었습니다. 또한 양식을 보다 쉽고 정확하게 작성할 수 있도록 제안이나 예시를 제공할 수도 있습니다.

### 접근성 탭 {#accessibility-tab}

![접근성 탭](/help/adaptive-forms/assets/email_accessibilitytab.png)

- **화면 판독기용 텍스트** - 화면 판독기용 텍스트는 시각 장애인이 사용하는 화면 판독기와 같은 보조 기술로 읽을 수 있도록 특별히 고안된 추가 텍스트를 나타냅니다. 이 텍스트는 양식 필드의 용도에 대한 오디오 설명을 제공하며, 여기에는 필드의 제목, 설명, 이름 및 관련 메시지(사용자 정의 텍스트)에 대한 정보가 포함될 수 있습니다. 화면 판독기 텍스트는 시각 장애가 있는 사용자를 포함한 모든 사용자가 양식에 액세스할 수 있도록 돕고 양식 필드 및 해당 요구 사항을 완전히 이해할 수 있도록 합니다.

   - **사용자 정의 텍스트**: ARIA 접근성 레이블에 사용자 정의 텍스트를 사용하려면 이 옵션을 선택합니다. 이 옵션을 선택하면 사용자 정의 텍스트 대화 상자가 표시됩니다. 사용자 정의 텍스트 대화 상자에서 관련 정보를 추가할 수 있습니다.
   - **설명**: ARIA 접근성 레이블에 설명을 사용하려면 이 옵션을 선택합니다.
   - **제목**: ARIA 접근성 레이블에 제목을 사용하려면 이 옵션을 선택합니다.
   - **이름**: ARIA 접근성 레이블에 이름을 사용하려면 이 옵션을 선택합니다.
   - **없음**: ARIA 접근성 레이블에 아무 것도 추가하지 않으려면 이 옵션을 선택합니다.

## 디자인 대화 상자 {#design-dialog}

디자인 대화 상자는 이메일 입력 구성 요소의 CSS 스타일을 정의하고 관리하는 데 사용됩니다.

### 스타일 탭 {#styles-tab}

탭은 구성 요소의 CSS 스타일을 정의하고 관리하는 데 사용됩니다. 적응형 양식 이메일 입력 핵심 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

![스타일 탭](/help/adaptive-forms/assets/datepicker_styletab.png)

- **기본 CSS 클래스**: 적응형 양식 이메일 입력 핵심 구성 요소에 기본 CSS 클래스를 제공할 수 있습니다.

- **허용된 스타일**: 이름과 스타일을 나타내는 CSS 클래스를 제공하여 스타일을 정의할 수 있습니다. 예를 들어 “bold text”라는 스타일을 만들고 “font-weight: bold”라는 CSS 클래스를 제공할 수 있습니다. 적응형 양식 편집기에서 이러한 스타일을 적응형 양식에 사용하거나 적용할 수 있습니다. 스타일을 적용하려면 적응형 양식 편집기에서 스타일을 적용할 구성 요소를 선택하고 속성 대화 상자로 이동한 다음 **스타일** 드롭다운 목록에서 원하는 스타일을 선택합니다. 스타일을 업데이트하거나 수정해야 하는 경우 디자인 대화 상자로 돌아가서 스타일 탭에서 스타일을 업데이트하고 변경 내용을 저장하면 됩니다.

### 사용자 정의 속성

![사용자 정의 속성 대화 상자](/help/adaptive-forms/assets/datepicker_customproperties.png)

사용자 정의 속성을 사용하면 양식 템플릿을 사용하여 사용자 정의 속성(키-값 쌍)을 적응형 양식 핵심 구성 요소에 연결할 수 있습니다. 사용자 정의 속성은 구성 요소의 Headless 렌디션에서 속성 섹션에 반영됩니다. 사용자 정의 속성 값에 따라 조정되는 동적 양식 동작을 만들 수 있습니다. 예를 들어 개발자는 모바일, 데스크탑 또는 웹 플랫폼을 위한 Headless 양식 구성 요소의 다양한 표현을 디자인하여 다양한 디바이스에서 사용자 경험을 크게 향상시킬 수 있습니다.

- **그룹 이름**: 사용자 정의 속성 그룹을 식별하기 위해 이름을 제공할 수 있습니다. 여러 사용자 정의 속성 그룹을 추가, 삭제 또는 재배열할 수 있습니다. 사용자 정의 속성 그룹을 추가하면 다음 옵션이 표시됩니다.

   - **키-값 쌍**: 각 사용자 정의 속성 그룹의 **추가** 버튼을 클릭하여 여러 사용자 정의 속성 이름과 사용자 정의 속성 값을 추가할 수 있습니다.

   - **삭제**: 사용자 정의 속성 이름과 사용자 정의 속성 값을 탭하거나 클릭하여 삭제할 수 있습니다.

   - **재배열**: 사용자 정의 속성 이름과 사용자 정의 속성 값을 탭하거나 클릭하고 드래그하면 순서를 재배열할 수 있습니다.

### 형식 탭 {#formats-tab}

형식 탭에서는 기본 및 사용자 정의 날짜 형식을 지정할 수 있습니다.

![형식 탭](/help/adaptive-forms/assets/emailinput_formattab.png)

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=ko)

-->

## 관련 문서 {#related-articles}

{{more-like-this}}

## 추가 참조 {#see-also}

{{see-also}}

---
title: 이메일 세분화 구성 요소
description: 이메일 세분화 구성 요소
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: ht
source-wordcount: '1171'
ht-degree: 100%

---


# 이메일 세분화 구성 요소 {#email-segmentation-component}

이메일 세분화 구성 요소는 Adobe Campaign의 변수를 사용하여 콘텐츠 수신자에 따라 콘텐츠를 표시하거나 숨깁니다.

## 사용 {#usage}

콘텐츠 작성자는 이메일 세분화 구성 요소를 통해 Adobe Campaign에서 제공하는 수신자 관련 변수가 충족하는 조건에 따라 콘텐츠를 표시하거나 숨길 수 있습니다. 이 방법으로 콘텐츠 수신자는 세분화를 기반으로 콘텐츠를 볼 수 있습니다.

* 템플릿 작성자는 [디자인 대화 상자](#design-dialog)를 사용해 세그먼트로 추가될 수 있는 구성 요소를 정의할 수 있습니다.
* 콘텐츠 작성자는 [구성 대화 상자](#configure-dialog)를 사용해 구성 요소를 세그먼트로 추가하고 Adobe Campaign 변수를 기반으로 표시되는 세그먼트를 구성할 수 있습니다.

구성 대화 상자를 사용하는 대신 콘텐츠 작성자가 이메일 세분화 구성 요소를 콘텐츠 페이지에 추가하면 콘텐츠 작성자는 추가 구성 요소를 이메일 세분화 구성 요소로 끌어다 놓아 새 세그먼트를 만들 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

현재 버전의 이메일 제목 구성 요소는 2022년 10월 이메일 세분화 구성 요소 릴리스 x과(와) 함께 도입된 v1입니다. 이 문서에서는 해당 구성 요소에 대해 설명합니다.

다음 표에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | 호환 가능 | 호환 가능 |

## 샘플 구성 요소 출력 {#sample-component-output}

이메일 세분화 구성 요소를 경험하고 구성 옵션의 샘플뿐만 아니라 HTML 및 JSON 출력을 확인하려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_email_segmentation_kr)를 참조하십시오.

### 기술 세부 사항 {#technical-details}

이메일 티저 구성 요소에 대한 최신 기술 설명서는 [GitHub에서 확인할 수 있습니다.](https://adobe.com/go/aem_cmp_tech_email_segmentation_v1_kr)

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

콘텐츠 작성자는 구성 대화 상자를 통해 세그먼트를 만들고, 이름을 바꾸고 배열할 수 있을 뿐만 아니라 활성 세그먼트를 정의할 수 있습니다. 이메일 세분화 구성 요소에서 세그먼트는 단순히 콘텐츠 수신자가 충족하는 조건에 따라 숨겨지거나 표시되는 또 다른 구성 요소입니다. [핵심 구성 요소 탭 구성 요소](/help/components/tabs.md)와 비교할 수 있으나, 세분화 구성 요소에서는 조건이 충족된 탭의 콘텐츠만 표시됩니다.

### 항목 탭 {#items-tab}

![이메일 세분화 구성 요소의 구성 대화 상자 항목 탭](/help/email/assets/email-segmentation-configure-items.png)

**세그먼트 추가** 버튼을 사용하여 세그먼트로 추가할 구성 요소를 선택하는 구성 요소 선택기를 엽니다. 추가되면 다음 요소가 포함된 목록에 항목을 추가합니다.

* **아이콘** - 목록에서 간단히 식별할 수 있는 세그먼트 구성 요소 유형의 아이콘. 마우스를 가져가 툴팁으로 전체 구성 요소 이름을 조회합니다.
* **조건** - 이 세그먼트가 콘텐츠 수신자에게 표시되기 위해 충족되어야 하는 조건입니다.
   * 사용 가능한 조건은 [디자인 대화 상자](#design-dialog)에서 정의합니다.
   * **기본** - 다른 조건이 충족되지 않았을 때 표시할 기본 세그먼트 정의
   * **사용자 정의** - 작성자가 조건 정의 가능
      * 조건은 Adobe Campaign 개인화 변수에 기반
      * [Adobe Campaign Standard 개인화 리소스는 여기를 참조하십시오.](https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/personalization.html?)
      * [Adobe Campaign Classic 개인화 리소스는 여기를 참조하십시오.](https://experienceleague.adobe.com/docs/campaign-classic/using/sending-messages/personalizing-deliveries/personalization-fields.html)
* **삭제** - 탭하거나 클릭하여 이메일 세분화 구성 요소에서 세그먼트를 삭제합니다.
* **재배열** - 탭하거나 클릭하고 드래그하여 세그먼트를 재배열합니다.

>[!TIP]
>
>콘텐츠 뷰포트가 작아져 편집 대화 상자가 전체 화면이 되면 **추가** 버튼이 표시되지 않습니다. [구성 요소 브라우저에서 드래그하여 콘텐츠 편집기의 이메일 세분화 구성 요소에 드롭하여](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#inserting-a-component) 구성 요소를 이메일 세분화 구성 요소에 추가할 수 있습니다.

### 속성 탭 {#properties-tab}

![이메일 세분화 구성 요소의 구성 대화 상자 속성 탭](/help/email/assets/email-segmentation-configure-properties.png)

* **ID** - 이 옵션을 통해 HTML에서 구성 요소의 고유 식별자를 제어할 수 있습니다.
   * 비워 두면 고유 ID는 자동으로 생성되고 결과 콘텐츠 검사를 통해 발견될 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID를 변경하면 CSS에 영향을 줄 수 있습니다.

### 접근성 탭 {#accessibility-tab}

![이메일 세분화 구성 요소의 구성 대화 상자 접근성 탭](/help/email/assets/email-segmentation-configure-accessibility.png)

**접근성** 탭에서 구성 요소에 대한 [ARIA 접근성](https://www.w3.org/WAI/standards-guidelines/aria/) 라벨 값을 설정할 수 있습니다.

* **라벨** - 구성 요소에 대한 ARIA 라벨 속성 값

### 스타일 탭 {#styles-tab-edit}

이메일 세분화 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

드롭다운을 사용하여 구성 요소에 적용할 스타일을 선택합니다. 편집 대화 상자에서 선택한 항목은 구성 요소 툴바에서 선택한 항목과 동일한 효과를 가집니다.

탭을 사용하려면 [디자인 대화 상자](#design-dialog)에서 이 구성 요소에 대한 스타일을 구성해야 합니다.

## 패널 선택 {#select-panel}

콘텐츠 작성자는 구성 요소 툴바의 **패널 선택** 옵션을 사용하여 다른 세그먼트 편집으로 변경하고 세그먼트를 간단히 재배열할 수 있습니다.

![패널 선택 아이콘](/help/email/assets/select-panel-icon.png)

구성 요소 툴바에서 **패널 선택** 옵션을 선택하면 구성된 세그먼트가 드롭다운으로 표시됩니다.

* 할당된 세그먼트 배열로 목록 순서가 변경되고 번호 매기기에 반영됩니다.
* 먼저 세그먼트의 구성 요소 유형을 표시한 다음 더 밝은 글꼴로 세그먼트에 대한 설명을 표시합니다.

![패널 선택 팝오버](/help/email/assets/select-panel-popover.png)

* 드롭다운의 항목을 탭하거나 클릭하여 편집기의 보기를 해당 세그먼트로 전환합니다.
* 드래그 핸들러를 사용하여 세그먼트를 바로 재배열할 수 있습니다.

>[!NOTE]
>
>세그먼트는 페이지 편집기 내에서 탭으로 렌더링되어 최종 콘텐츠에 대한 여러 옵션이 있음을 보여 줍니다. 이 탭은 페이지 편집기 내에서 작성자가 선택할 수 없습니다. 선택 패널을 사용하여 표시된 세그먼트 사이를 전환합니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 통해 세그먼트로 이메일 세분화 구성 요소에 추가 가능한 구성 요소뿐만 아니라 콘텐츠 작성자가 사용할 수 있는 사용자 정의 스타일을 정의할 수 있습니다.

### 허용된 구성 요소 탭 {#allowed-components-tab}

콘텐츠 작성자는 **허용된 구성 요소**&#x200B;를 통해 세그먼트로 이메일 세분화 구성 요소에 추가 가능한 구성 요소를 정의할 수 있습니다.

[템플릿 편집기의 레이아웃 컨테이너 정책 및 속성을 정의하는 경우](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html) **허용된 구성 요소** 탭은 동일한 이름의 탭과 동일한 방식으로 작동합니다.

### 스타일 탭 {#styles-tab}

이메일 세분화 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

### 정의된 조건 탭 {#defined-conditions}

템플릿 편집기에서 **정의된 조건** 탭을 사용해 콘텐츠 작성자가 세그먼트를 만들 때 선택 가능한 조건을 정의할 수 있습니다.

![디자인 대화 상자 정의된 조건 탭](/help/email/assets/email-segmentation-design-defined-conditions.png)

**추가** 버튼을 탭하거나 클릭하여 새 조건을 만듭니다.

* **세그먼트 조건 이름** - 조건에 대한 설명
* **세그먼트 조건** - Adobe Campaign 개인화 변수를 기준으로 충족해야 하는 실제 조건
   * [Adobe Campaign Standard 개인화 리소스는 여기를 참조하십시오.](https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/personalization.html?)
   * [Adobe Campaign Classic 개인화 리소스는 여기를 참조하십시오.](https://experienceleague.adobe.com/docs/
* **제거** - 탭하거나 클릭하여 조건 제거
* **재배열** - 탭하거나 클릭하고 드래그하여 조건의 순서 재배열

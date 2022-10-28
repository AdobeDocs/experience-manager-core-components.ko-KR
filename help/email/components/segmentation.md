---
title: 이메일 세그멘테이션 구성 요소
description: 이메일 세그먼테이션 구성 요소
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: tm+mt
source-wordcount: '1171'
ht-degree: 15%

---


# 이메일 세그멘테이션 구성 요소 {#email-segmentation-component}

이메일 세그먼테이션 구성 요소는 Adobe Campaign의 변수를 사용하여 컨텐츠의 수신자를 기반으로 컨텐츠를 표시하고 숨깁니다.

## 사용량 {#usage}

이메일 세그멘테이션 구성 요소를 사용하면 컨텐츠 작성자는 Adobe Campaign에서 제공한 수신자에 대한 변수가 충족하는 조건을 기반으로 컨텐츠를 숨기고 표시할 수 있습니다. 이러한 방식으로 컨텐츠를 받는 사람은 세그멘테이션에 따라 컨텐츠를 보게 됩니다.

* 템플릿 작성자는 [디자인 대화 상자](#design-dialog) 를 추가하여 세그먼트로 추가할 수 있는 구성 요소를 정의합니다.
* 컨텐츠 작성자는 [대화 상자 구성](#configure-dialog) 구성 요소를 세그먼트로 추가하고 Adobe Campaign 변수를 기반으로 표시되는 세그먼트를 구성하려면 다음을 수행하십시오.

구성 대화 상자를 사용하는 대신 컨텐츠 작성자가 이메일 세그멘테이션 구성 요소를 컨텐츠 페이지에 추가했으면 컨텐츠 작성자가 추가 구성 요소를 이메일 세그멘테이션 구성 요소에 끌어다 놓아 새 세그먼트를 만들 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

이메일 세그멘테이션 구성 요소의 현재 버전은 v1이며, 이 버전은 2022년 10월에 이메일 코어 구성 요소 릴리스 x에서 도입되었으며 이 문서에 설명되어 있습니다.

다음 표에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | 호환 가능 | 호환 가능 |

## 샘플 구성 요소 출력 {#sample-component-output}

이메일 세그멘테이션 구성 요소를 경험하고 구성 옵션의 예와 HTML 및 JSON 출력을 보려면 [구성 요소 라이브러리.](https://adobe.com/go/aem_cmp_library_email_segmentation)

### 기술 세부 사항 {#technical-details}

이메일 티저 구성 요소에 대한 최신 기술 문서입니다 [GitHub에서 찾을 수 있습니다.](https://adobe.com/go/aem_cmp_tech_email_segmentation_v1)

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서입니다.](/help/developing/overview.md)

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자에서는 컨텐츠 작성자가 세그먼트를 만들고, 이름을 변경하고, 다시 정렬할 수 있을 뿐만 아니라 활성 세그먼트를 정의할 수 있습니다. 이메일 세그멘테이션 구성 요소에서 세그먼트는 컨텐츠의 수신자가 충족한 조건을 기반으로 숨기거나 표시되는 다른 구성 요소입니다. 와 비교할 수 있습니다 [코어 구성 요소 탭 구성 요소,](/help/components/tabs.md) 하지만 세그멘테이션 구성 요소에서는 조건이 충족되는 탭의 콘텐츠만 표시됩니다.

### 항목 탭 {#items-tab}

![이메일 세그먼테이션 구성 요소의 구성 대화 상자 항목 탭](/help/email/assets/email-segmentation-configure-items.png)

를 사용하십시오 **세그먼트 추가** 구성 요소 선택기를 열어 세그먼트로 추가할 구성 요소를 선택합니다. 추가한 항목은 다음 요소를 포함하는 목록에 추가됩니다.

* **아이콘** - 목록에서 쉽게 식별할 수 있도록 세그먼트의 구성 요소 유형의 아이콘입니다. 마우스를 가져가 툴팁으로 전체 구성 요소 이름을 조회합니다.
* **조건** - 이 세그먼트를 컨텐츠 수신자에게 표시하기 위해 충족해야 하는 조건입니다.
   * 사용 가능한 조건은 [디자인 대화 상자](#design-dialog)
   * **기본값** - 다른 조건이 충족되지 않을 경우 표시할 기본 세그먼트를 정의합니다
   * **사용자 지정** - 작성자가 조건을 정의할 수 있습니다
      * 조건은 Adobe Campaign 개인화 변수를 기반으로 합니다
      * [Adobe Campaign Standard 개인화 리소스는 여기 를 참조하십시오.](https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/personalization.html?)
      * [Adobe Campaign Classic 개인화 리소스는 여기 를 참조하십시오.](https://experienceleague.adobe.com/docs/campaign-classic/using/sending-messages/personalizing-deliveries/personalization-fields.html)
* **삭제** - 이메일 세그멘테이션 구성 요소에서 세그먼트를 삭제하려면 탭하거나 클릭합니다.
* **다시 정렬** - 탭하거나 클릭하고 드래그하여 세그먼트를 재정렬합니다.

>[!TIP]
>
>컨텐츠의 뷰포트가 축소되어 편집 대화 상자가 전체 화면이 되면 **추가** 단추가 숨겨집니다. 구성 요소는 여전히 다음 방법으로 이메일 세그멘테이션 구성 요소에 추가할 수 있습니다 [구성 요소 브라우저에서 끌어서 콘텐츠 편집기의 이메일 세그멘테이션 구성 요소에 놓습니다.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#inserting-a-component)

### 속성 탭 {#properties-tab}

![이메일 세그먼테이션 구성 요소의 구성 대화 상자 속성 탭](/help/email/assets/email-segmentation-configure-properties.png)

* **ID** - 이 옵션을 사용하면 HTML에서 구성 요소의 고유 식별자를 제어할 수 있습니다.
   * 비워 두면 고유 ID가 자동으로 생성되며 결과 컨텐츠를 검사하여 찾을 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID를 변경하면 CSS에 영향을 줄 수 있습니다.

### 접근성 탭 {#accessibility-tab}

![이메일 세그멘테이션 구성 요소의 구성 대화 상자 액세스 가능성 탭](/help/email/assets/email-segmentation-configure-accessibility.png)

**접근성** 탭에서 구성 요소에 대한 [ARIA 접근성](https://www.w3.org/WAI/standards-guidelines/aria/) 라벨 값을 설정할 수 있습니다.

* **라벨** - 구성 요소에 대한 ARIA 라벨 속성 값

### 스타일 탭 {#styles-tab-edit}

이메일 세그먼테이션 구성 요소는 AEM을 지원합니다 [스타일 시스템.](/help/get-started/authoring.md#component-styling)

드롭다운을 사용하여 구성 요소에 적용할 스타일을 선택합니다. 편집 대화 상자에서 선택한 항목은 구성 요소 툴바에서 선택한 항목과 동일한 효과를 가집니다.

스타일을 [디자인 대화 상자](#design-dialog) 을 클릭하여 탭을 사용할 수 있습니다.

## 패널 선택 {#select-panel}

컨텐츠 작성자는 **패널 선택** 구성 요소 도구 모음의 옵션을 사용하여 편집할 수 있는 다른 세그먼트로 변경하고 세그먼트를 쉽게 다시 정렬할 수 있습니다.

![패널 선택 아이콘](/help/email/assets/select-panel-icon.png)

선택 후 **패널 선택** 구성 요소 도구 모음의 옵션을 선택하면 구성된 세그먼트가 드롭다운으로 표시됩니다.

* 목록은 세그먼트의 지정된 배열별로 정렬되며 번호 지정에 반영됩니다.
* 먼저 세그먼트의 구성 요소 유형이 표시되고, 그 뒤에는 더 밝은 글꼴로 세그먼트에 대한 설명이 표시됩니다.

![패널 선택 팝오버](/help/email/assets/select-panel-popover.png)

* 드롭다운에서 항목을 탭하거나 클릭하면 편집기의 보기가 해당 세그먼트로 전환됩니다.
* 끌기 핸들을 사용하여 세그먼트를 제자리에서 재배열할 수 있습니다.

>[!NOTE]
>
>세그먼트는 최종 컨텐츠에 대한 여러 옵션이 있음을 보여주기 위해 페이지 편집기 내에 탭으로 렌더링됩니다. 이러한 탭은 페이지 편집기 내에서 작성자가 선택할 수 없습니다. [선택] 패널을 사용하여 표시된 세그먼트 간에 전환할 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자에서 이메일 세그멘테이션 구성 요소에 세그먼트로 추가할 수 있는 구성 요소를 정의하고 컨텐츠 작성자가 사용할 수 있는 사용자 지정 스타일을 정의할 수 있습니다.

### 허용된 구성 요소 탭 {#allowed-components-tab}

다음 **허용된 구성 요소** 탭 을 사용하여 컨텐츠 작성자가 이메일 세그멘테이션 구성 요소에 세그먼트로 추가할 수 있는 구성 요소를 정의합니다.

다음 **허용된 구성 요소** 탭은 동일한 이름의 탭과 동일한 방식으로 작동합니다. [템플릿 편집기에서 레이아웃 컨테이너의 정책 및 속성 정의.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html)

### 스타일 탭 {#styles-tab}

이메일 세그먼테이션 구성 요소는 AEM을 지원합니다 [스타일 시스템.](/help/get-started/authoring.md#component-styling)

### 정의된 조건 탭 {#defined-conditions}

사용 **정의된 조건** 탭에서 템플릿 편집기는 세그먼트를 만들 때 컨텐츠 작성자가 선택할 수 있는 조건을 정의할 수 있습니다.

![디자인 대화 상자 정의된 조건 탭](/help/email/assets/email-segmentation-design-defined-conditions.png)

을(를) 탭하거나 클릭합니다 **추가** 새 조건을 만드는 단추입니다.

* **세그먼트 조건 이름** - 조건에 대한 설명입니다
* **세그먼트 조건** - Adobe Campaign 개인화 변수를 기반으로 하여 충족해야 하는 실제 조건
   * [Adobe Campaign Standard 개인화 리소스는 여기 를 참조하십시오.](https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/personalization.html?)
   * [Adobe Campaign Classic 개인화 리소스는 여기 를 참조하십시오.](https://experienceleague.adobe.com/docs/)
* **제거** - 를 탭하여 조건을 제거합니다
* **다시 정렬** - 탭하거나 클릭하고 드래그하여 조건 순서를 재정렬합니다

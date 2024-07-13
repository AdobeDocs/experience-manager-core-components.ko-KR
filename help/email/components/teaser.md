---
title: 이메일 티저 구성 요소
description: 이메일 티저 구성 요소에 이미지, 제목, 서식 있는 텍스트 및 추가 콘텐츠 링크(선택 사항)가 표시될 수 있습니다.
role: Architect, Developer, Admin, User
exl-id: d6123b22-7cba-406c-986d-b6f00322d135
source-git-commit: 3abc29e0c186a84f079d5938b8b716f4c7378d65
workflow-type: tm+mt
source-wordcount: '999'
ht-degree: 100%

---


# 이메일 티저 구성 요소 {#email-teaser-component}

이메일 티저 구성 요소에 이미지, 제목, 서식 있는 텍스트 및 추가 콘텐츠 링크(선택 사항)가 표시될 수 있습니다.

## 사용 {#usage}

콘텐츠 작성자는 이메일 티저 구성 요소를 통해 이미지, 제목이나 서식 있는 텍스트와 추가 콘텐츠 링크 또는 기타 작업을 통해 티저를 손쉽게 제작할 수 있습니다.

* 템플릿 작성자는 [디자인 대화 상자](#design-dialog)를 통해 콜 투 액션을 만들고 링크를 추가하는 옵션을 사용할 수 있는지, 여러 디스플레이 옵션을 활성화할 수 있는지 정의할 수 있습니다.
* 콘텐츠 작성자는 [구성 대화 상자](#configure-dialog)를 통해 이미지를 설정하고, CTA를 정의하고, 제목 및 설명을 설정하고 링크를 개별 티저로 구성할 수 있습니다.
* [이메일 이미지 구성 요소](image.md)의 [편집 대화 상자](image.md#edit-dialog)에 액세스하여 티저 이미지를 수정할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

현재 버전의 이메일 티저 구성 요소는 2022년 10월 이메일 핵심 구성 요소 릴리스 x과(와) 함께 도입된 v1입니다. 이 문서에서는 해당 구성 요소에 대해 설명합니다.

다음 표에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | 호환 가능 | - |

### 기술 세부 사항 {#technical-details}

이메일 티저 구성 요소에 대한 최신 기술 설명서는 [GitHub에서 확인할 수 있습니다.](https://adobe.com/go/aem_cmp_tech_email_teaser_v1_kr)

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

콘텐츠 작성자는 구성 대화 상자를 통해 개별 티저의 속성을 정의할 수 있습니다. 이미지가 선택된 경우 [편집 대화 상자](#edit-dialog)에서도 티저 이미지를 수정할 수 있습니다.

### 링크 탭 {#links-tab}

![이메일 티저 구성 요소의 편집 대화 상자 링크 탭](/help/email/assets/email-teaser-edit-links.png)

티저 제목, 설명 및 이미지는 링크된 콘텐츠 또는 첫 번째 콜 투 액션에서 링크된 콘텐츠에서 상속될 수 있습니다. 링크나 콜 투 액션이 지정되지 않은 경우 제목, 설명 및 이미지가 현재 콘텐츠에서 상속됩니다.

* **링크** - 이 파일은 콘텐츠, 외부 URL 또는 앵커로 연결됩니다.
   * Campaign 아이콘을 클릭하여 Adobe Campaign의 다이내믹 콘텐츠를 삽입하기 위한 [Adobe Campaign 변수 선택](/help/email/campaign-variables.md) 대화 상자를 엽니다.
* **콜 투 액션** - 이 옵션을 사용하여 여러 대상에 연결할 수 있습니다.
   * 첫 번째 콜 투 액션에서 링크된 페이지는 티저 제목, 설명 또는 이미지를 상속할 때 사용됩니다.
   * Campaign 아이콘을 클릭하여 Adobe Campaign의 다이내믹 콘텐츠를 삽입하기 위한 [Adobe Campaign 변수 선택](/help/email/campaign-variables.md) 대화 상자를 엽니다.

### 텍스트 탭 {#text-tab}

![이메일 티저 구성 요소의 편집 대화 상자 텍스트 탭](/help/email/assets/email-teaser-edit-text.png)

* **사전 제목** - 사전 제목은 티저 제목 앞에 표시될 수 있습니다.
* **제목 유형** - 티저의 헤드라인으로 표시할 제목을 정의합니다.
   * Campaign 아이콘을 클릭하여 Adobe Campaign의 다이내믹 콘텐츠를 삽입하기 위한 [Adobe Campaign 변수 선택](/help/email/campaign-variables.md) 대화 상자를 엽니다.
   * **링크된 페이지에서 제목 다운로드** - 확인 표시가 되어 있으면 제목은 링크된 페이지 제목으로 채워집니다.
* **설명** - 티저의 하위 머리글로 표시할 설명을 정의합니다.
   * **Adobe Campaign 변수 선택** 아이콘을 클릭하여 Adobe Campaign의 다이내믹 콘텐츠를 삽입하기 위한 [Adobe Campaign 변수 선택](/help/email/campaign-variables.md) 대화 상자를 엽니다.
   * **링크된 페이지에서 설명 다운로드** - 확인 표시가 되어 있으면 제목은 링크된 페이지 설명으로 채워집니다.
* **ID** - 이 옵션을 통해 HTML에서 구성 요소의 고유 식별자를 제어할 수 있습니다.
   * 비워 두면 고유 ID는 자동으로 생성되고 결과 콘텐츠 검사를 통해 발견될 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID를 변경하면 CSS에 영향을 줄 수 있습니다.

### 에셋 탭 {#asset-tab}

![이메일 티저 구성 요소의 편집 대화 상자 이미지 탭](/help/email/assets/email-teaser-edit-image.png)

* **페이지에서 추천 이미지 상속** - 링크된 페이지의 페이지 속성에 정의된 이미지를 사용하거나 찾을 수 없는 경우 현재 페이지를 사용합니다.
* **이미지 자산** - [자산 브라우저](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html)에서 자산을 삭제하거나 **검색** 옵션을 탭하여 로컬 파일 시스템에서 로드합니다.
   * **지우기**&#x200B;를 탭하거나 클릭하여 현재 선택된 이미지 선택을 해제합니다.
   * **편집**&#x200B;을 탭하거나 클릭하여 에셋 편집기에서 [에셋 렌디션을 관리합니다](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html).
* **접근성을 위한 그림 설명** 필드에서는 시각 장애인 독자를 위한 이미지 설명을 정의할 수 있습니다.
   * **페이지에서 그림 설명 상속** 옵션은 DAM에 있는 `dc:description` 메타데이터 또는 연결된 자산이 없는 경우 현재 페이지의 연결된 자산 값에 대한 대체 설명을 사용합니다.
* **그림 설명을 제공하지 않음** 옵션은 이미지가 단순히 장식용이거나 페이지에 추가 정보를 전달하지 않는 경우 화면 판독기와 같은 보조 기술에서 무시되도록 이미지를 표시합니다.

>[!NOTE]
>
>[Dynamic Media 기능](image.md#dynamic-media)은 현재 티저 구성 요소에서 사용할 수 없습니다.

### 스타일 탭 {#styles-tab-edit}

이메일 티저 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

드롭다운을 사용하여 구성 요소에 적용할 스타일을 선택합니다. 편집 대화 상자에서 선택한 항목은 구성 요소 툴바에서 선택한 항목과 동일한 효과를 가집니다.

탭을 사용하려면 [디자인 대화 상자](#design-dialog)에서 이 구성 요소에 대한 스타일을 구성해야 합니다.

## 편집 대화 상자 {#edit-dialog}

이메일 티저 구성 요소는 이미지 렌더링을 [이미지 구성 요소](image.md)로 전달합니다. 따라서 콘텐츠 작성자는 이미지 구성 요소의 [편집 대화 상자](image.md#edit-dialog)를 티저 이미지를 조작하는 데 사용할 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 통해 구성 요소 사용 시 필요한 티저 옵션을 정의할 수 있습니다.

### 티저 탭 {#teaser-tab}

![이메일 티저 구성 요소의 디자인 대화 상자](/help/email/assets/email-teaser-design.png)

* **허용된 제목 요소** - 드롭다운을 사용해 작성자가 티저의 제목 유형으로 선택할 수 있는 제목 HTML 요소를 정의합니다.
* **제목의 기본 제목 요소** - 티저의 제목 유형에 사용되는 기본 제목 HTML 요소
* **콜 투 액션**
   * **콜 투 액션 비활성화** - 콘텐츠 작성자를 위한 **콜 투 액션** 옵션을 숨깁니다.
* **요소**
   * **사전 제목 숨기기** - 콘텐츠 작성자를 위한 **사전 제목**&#x200B;을 숨깁니다.
   * **제목 숨기기** - 콘텐츠 작성자를 위한 **제목**&#x200B;을 숨깁니다.
      * 선택한 경우 **제목 유형**&#x200B;을 숨깁니다.
   * **제목 유형 표시**
   * **설명 숨기기** - 콘텐츠 작성자를 위한 **설명**&#x200B;을 숨깁니다.
* **이미지 전달** - 이미지 처리 시 이메일 티저가 전달하는 구성 요소의 정보가 표시됩니다.

### 스타일 탭 {#styles-tab}

이메일 티저 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

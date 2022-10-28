---
title: 이메일 티저 구성 요소
description: 이메일 티저 구성 요소는 이미지, 제목, 리치 텍스트를 표시하고 선택적으로 추가 컨텐츠에 연결할 수 있습니다.
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: tm+mt
source-wordcount: '1056'
ht-degree: 52%

---


# 이메일 티저 구성 요소 {#email-teaser-component}

이메일 티저 구성 요소는 이미지, 제목, 리치 텍스트를 표시하고 선택적으로 추가 컨텐츠에 연결할 수 있습니다.

## 사용량 {#usage}

이메일 티저 구성 요소를 사용하면 컨텐츠 작성자는 이미지, 제목 또는 리치 텍스트를 사용하여 티저를 쉽게 만들고 추가 컨텐츠 또는 기타 작업에 연결할 수 있습니다.

* 템플릿 작성자는 [디자인 대화 상자](#design-dialog)를 통해 콜 투 액션을 만들고 링크를 추가하는 옵션을 사용할 수 있는지, 여러 디스플레이 옵션을 활성화할 수 있는지 정의할 수 있습니다.
* 콘텐츠 작성자는 [구성 대화 상자](#configure-dialog)를 통해 이미지를 설정하고, CTA를 정의하고, 제목 및 설명을 설정하고 링크를 개별 티저로 구성할 수 있습니다.
* 다음 [대화 상자 편집](image.md#edit-dialog) 의 [이메일 이미지 구성 요소](image.md) teaser 이미지를 수정하기 위해 액세스할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

이메일 티저 구성 요소의 현재 버전은 v1이며, 2022년 10월에 이메일 핵심 구성 요소의 릴리스 x에서 도입되었으며 이 문서에 설명되어 있습니다.

다음 표에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | 호환 가능 | 호환 가능 |

## 샘플 구성 요소 출력 {#sample-component-output}

Email Teaser 구성 요소와 구성 옵션의 예 및 HTML 및 JSON 출력을 보려면 [구성 요소 라이브러리.](https://adobe.com/go/aem_cmp_library_email_teaser)

### 기술 세부 사항 {#technical-details}

이메일 티저 구성 요소에 대한 최신 기술 문서입니다 [GitHub에서 찾을 수 있습니다.](https://adobe.com/go/aem_cmp_tech_email_teaser_v1)

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서입니다.](/help/developing/overview.md)

## 구성 대화 상자 {#configure-dialog}

콘텐츠 작성자는 구성 대화 상자를 통해 개별 티저의 속성을 정의할 수 있습니다. 이미지가 선택된 경우 [편집 대화 상자](#edit-dialog)에서도 티저 이미지를 수정할 수 있습니다.

### 링크 탭 {#links-tab}

![이메일 티저 구성 요소의 편집 대화 상자 링크 탭](/help/email/assets/email-teaser-edit-links.png)

티저 제목, 설명 및 이미지는 연결된 컨텐츠나 첫 번째 클릭유도문장에 연결된 컨텐츠에서 상속될 수 있습니다. 링크와 클릭유도문안 중 어느 것도 지정하지 않으면 제목, 설명 및 이미지가 현재 콘텐츠에서 상속됩니다.

* **링크** - 이 파일은 컨텐츠, 외부 URL 또는 앵커에 연결됩니다.
   * Campaign 아이콘을 클릭하여 [Adobe Campaign 변수 선택](/help/email/campaign-variables.md) 대화 상자에서 Adobe Campaign의 동적 콘텐츠를 삽입할 수 있습니다.
* **콜 투 액션** - 이 옵션을 사용하여 여러 대상에 연결할 수 있습니다.
   * 첫 번째 콜 투 액션에서 링크된 페이지는 티저 제목, 설명 또는 이미지를 상속할 때 사용됩니다.
   * Campaign 아이콘을 클릭하여 [Adobe Campaign 변수 선택](/help/email/campaign-variables.md) 대화 상자에서 Adobe Campaign의 동적 콘텐츠를 삽입할 수 있습니다.

### 텍스트 탭 {#text-tab}

![이메일 티저 구성 요소의 편집 대화 상자 텍스트 탭](/help/email/assets/email-teaser-edit-text.png)

* **사전 제목** - 사전 제목은 티저 제목 앞에 표시될 수 있습니다.
* **제목 유형** - 티저의 헤드라인으로 표시할 제목을 정의합니다.
   * Campaign 아이콘을 클릭하여 [Adobe Campaign 변수 선택](/help/email/campaign-variables.md) 대화 상자에서 Adobe Campaign의 동적 콘텐츠를 삽입할 수 있습니다.
   * **링크된 페이지에서 제목 다운로드** - 확인 표시가 되어 있으면 제목은 링크된 페이지 제목으로 채워집니다.
* **설명** - 티저의 하위 머리글로 표시할 설명을 정의합니다.
   * 을(를) 클릭합니다. **Adobe Campaign 변수 선택** 아이콘을 클릭하여 열기 [Adobe Campaign 변수 선택](/help/email/campaign-variables.md) 대화 상자에서 Adobe Campaign의 동적 콘텐츠를 삽입할 수 있습니다.
   * **링크된 페이지에서 설명 다운로드** - 확인 표시가 되어 있으면 제목은 링크된 페이지 설명으로 채워집니다.
* **ID** - 이 옵션을 사용하면 HTML에서 구성 요소의 고유 식별자를 제어할 수 있습니다.
   * 비워 두면 고유 ID가 자동으로 생성되며 결과 컨텐츠를 검사하여 찾을 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID를 변경하면 CSS에 영향을 줄 수 있습니다.

### 에셋 탭 {#asset-tab}

![이메일 티저 구성 요소의 편집 대화 상자 이미지 탭](/help/email/assets/email-teaser-edit-image.png)

* **페이지에서 추천 이미지 상속** - 링크된 페이지의 페이지 속성에 정의된 이미지를 사용하거나 찾을 수 없는 경우 현재 페이지를 사용합니다.
* **이미지 에셋** - [에셋 브라우저](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html)에서 에셋을 삭제하거나 **검색** 옵션을 탭하여 로컬 파일 시스템에서 로드합니다.
   * **지우기**&#x200B;를 탭하거나 클릭하여 현재 선택된 이미지 선택을 해제합니다.
   * 탭 또는 클릭 **편집** to [자산의 표현물 관리](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) 를 입력합니다.
* **접근성을 위한 대체 텍스트** 필드에서는 시각 장애인 독자를 위한 이미지 설명을 정의할 수 있습니다.
   * **페이지에서 대체 텍스트 상속** 옵션은 DAM에 있는 `dc:description` 메타데이터 또는 연결된 에셋이 없는 경우 현재 페이지의 연결된 에셋 값에 대한 대체 설명을 사용합니다.
* **대체 텍스트를 제공하지 않음** 옵션은 이미지가 단순히 장식용이거나 페이지에 추가 정보를 전달하지 않는 경우 화면 판독기와 같은 보조 기술에서 무시되도록 이미지를 표시합니다.

>[!NOTE]
>
>[Dynamic Media 기능](image.md#dynamic-media)은 현재 티저 구성 요소에서 사용할 수 없습니다.

### 스타일 탭 {#styles-tab-edit}

이메일 티저 구성 요소는 AEM을 지원합니다 [스타일 시스템.](/help/get-started/authoring.md#component-styling)

드롭다운을 사용하여 구성 요소에 적용할 스타일을 선택합니다. 편집 대화 상자에서 선택한 항목은 구성 요소 툴바에서 선택한 항목과 동일한 효과를 가집니다.

스타일을 [디자인 대화 상자](#design-dialog) 을 클릭하여 탭을 사용할 수 있습니다.

## 편집 대화 상자 {#edit-dialog}

이메일 티저 구성 요소는 이미지 렌더링을 [이미지 구성 요소](image.md). 따라서 콘텐츠 작성자는 이미지 구성 요소의 [편집 대화 상자](image.md#edit-dialog)를 티저 이미지를 조작하는 데 사용할 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 통해 구성 요소 사용 시 필요한 티저 옵션을 정의할 수 있습니다.

### 티저 탭 {#teaser-tab}

![이메일 티저 구성 요소의 디자인 대화 상자](/help/email/assets/email-teaser-design.png)

* **허용된 제목 요소** - 드롭다운을 사용하여 티저의 제목 유형에 대해 작성자가 선택할 수 있는 제목 HTML 요소를 정의합니다.
* **제목의 기본 제목 요소** - 티저의 제목 유형에 사용되는 기본 제목 HTML 요소입니다
* **콜 투 액션**
   * **콜 투 액션 비활성화** - 콘텐츠 작성자를 위한 **콜 투 액션** 옵션을 숨깁니다.
* **요소**
   * **사전 제목 숨기기** - 콘텐츠 작성자를 위한 **사전 제목**&#x200B;을 숨깁니다.
   * **제목 숨기기** - 콘텐츠 작성자를 위한 **제목**&#x200B;을 숨깁니다.
      * 선택한 경우 **제목 유형**&#x200B;을 숨깁니다.
   * **제목 유형 표시**
   * **설명 숨기기** - 콘텐츠 작성자를 위한 **설명**&#x200B;을 숨깁니다.
* **이미지 위임** - 이메일 티저가 이미지 처리를 위임하는 구성 요소를 나타내는 정보 표시입니다.

### 스타일 탭 {#styles-tab}

이메일 티저 구성 요소는 AEM을 지원합니다 [스타일 시스템.](/help/get-started/authoring.md#component-styling)

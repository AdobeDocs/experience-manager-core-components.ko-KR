---
title: 티저 구성 요소
description: 티저 구성 요소에 이미지, 제목, 서식 있는 텍스트 및 추가 콘텐츠 링크(선택 사항)가 표시될 수 있습니다.
role: Architect, Developer, Admin, User
exl-id: ec75e168-6f3b-4dff-8df6-06ca7dc18688
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: ht
source-wordcount: '1046'
ht-degree: 100%

---

# 티저 구성 요소 {#teaser-component}

핵심 구성 요소의 티저 구성 요소에 이미지, 제목, 서식 있는 텍스트 및 추가 콘텐츠 링크(선택 사항)가 표시될 수 있습니다.

## 사용 {#usage}

콘텐츠 작성자는 티저 구성 요소를 통해 이미지, 제목이나 서식 있는 텍스트와 추가 콘텐트 링크 또는 기타 작업을 통해 티저를 손쉽게 제작할 수 있습니다.

템플릿 작성자는 [디자인 대화 상자](#design-dialog)를 통해 콜 투 액션을 만들고 링크를 추가하는 옵션을 사용할 수 있는지, 여러 디스플레이 옵션을 활성화할 수 있는지 정의할 수 있습니다. 콘텐츠 작성자는 [구성 대화 상자](#configure-dialog)를 통해 이미지를 설정하고, CTA를 정의하고, 제목 및 설명을 설정하고 링크를 개별 티저로 구성할 수 있습니다. [이미지 구성 요소](image.md)의 [편집 대화 상자](image.md#edit-dialog)에 액세스하여 티저 이미지를 수정할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

현재 버전의 티저 구성 요소는 2022년 2월 핵심 구성 요소 릴리스 2.18.0과 함께 도입된 v2입니다. 이 문서에서는 해당 구성 요소에 대해 설명합니다.

다음 테이블에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|---|
| v2 | - | 호환 가능 | 호환 가능 | 호환 가능 |
| [v1](v1/teaser.md) | 호환 가능 | 호환 가능 | - | 호환 가능 |

## 원격 자산 지원 {#remote-assets}

티저 구성 요소([릴리스 2.23.2](/help/versions.md)부터)는 원격 자산을 지원합니다. [구성한 다음](/help/developing/remote-assets.md) 티저 구성 요소에 대해 원격 서비스에서 자산을 선택할 수 있습니다.

## 샘플 구성 요소 출력 {#sample-component-output}

티저 구성 요소를 경험하고 구성 옵션의 샘플뿐만 아니라 HTML 및 JSON 출력을 확인하려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_teaser_kr)를 참조하십시오.

### 기술 세부 정보 {#technical-details}

티저 구성 요소에 대한 최신 기술 설명서는 [GitHub](https://adobe.com/go/aem_cmp_tech_teaser_v1_kr)에서 찾아볼 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

콘텐츠 작성자는 구성 대화 상자를 통해 개별 티저의 속성을 정의할 수 있습니다. 이미지가 선택된 경우 [편집 대화 상자](#edit-dialog)에서도 티저 이미지를 수정할 수 있습니다.

### 링크 탭 {#links-tab}

![티저 구성 요소의 편집 대화 상자 링크 탭](/help/assets/teaser-edit-links.png)

티저 제목, 설명 및 이미지는 연결된 페이지 또는 첫 번째 콜 투 액션에서 연결된 페이지에서 상속될 수 있습니다. 링크나 콜 투 액션을 지정하지 않으면 현재 페이지에서 제목, 설명 및 이미지가 상속됩니다.

* **링크** - 이 파일은 콘텐츠 페이지, 외부 URL 또는 페이지 앵커로 연결됩니다.
* **새 탭에서 링크 열기** - 활성화된 경우 링크가 새 브라우저 탭에서 열립니다.
* **콜 투 액션** - 이 옵션을 사용하여 여러 대상에 연결할 수 있습니다.
   * 첫 번째 콜 투 액션에서 링크된 페이지는 티저 제목, 설명 또는 이미지를 상속할 때 사용됩니다.

### 텍스트 탭 {#text-tab}

![티저 구성 요소의 편집 대화 상자 텍스트 탭](/help/assets/teaser-edit-text.png)

* **사전 제목** - 사전 제목은 티저 제목 앞에 표시될 수 있습니다.
* **제목 유형** - 티저의 헤드라인으로 표시할 제목을 정의합니다.
   * **링크된 페이지에서 제목 다운로드** - 확인 표시가 되어 있으면 제목은 링크된 페이지 제목으로 채워집니다.
* **설명** - 티저의 하위 머리글로 표시할 설명을 정의합니다.
   * **링크된 페이지에서 설명 다운로드** - 확인 표시가 되어 있으면 제목은 링크된 페이지 설명으로 채워집니다.
* **ID** - 이 옵션을 통해 HTML과 [데이터 레이어](/help/developing/data-layer/overview.md)에서 구성 요소의 고유 식별자를 제어할 수 있습니다.
   * 비워 두면 고유 ID는 자동으로 생성되고 결과 페이지 검사를 통해 발견될 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID가 변경되면 CSS, JS 및 데이터 레이어 추적에 영향을 미칠 수 있습니다.

### 자산 탭 {#asset-tab}

![티저 구성 요소의 편집 대화 상자 이미지 탭](/help/assets/teaser-edit-image.png)

* **페이지에서 추천 이미지 상속** - 링크된 페이지의 페이지 속성에 정의된 이미지를 사용하거나 찾을 수 없는 경우 현재 페이지를 사용합니다.
* **이미지 자산** - [자산 브라우저](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html)에서 자산을 삭제하거나 **검색** 옵션을 탭하여 로컬 파일 시스템에서 로드합니다.
   * **지우기**&#x200B;를 탭하거나 클릭하여 현재 선택된 이미지 선택을 해제합니다.
   * **선택**&#x200B;을 탭하거나 클릭하여 [자산 브라우저](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html)를 열고 이미지를 선택합니다.
      * [원격 자산 지원](#remote-assets)이 활성화된 경우 자산 선택을 위한 여러 옵션이 있습니다.
         * **로컬**&#x200B;은 로컬 AEM 자산 라이브러리에서 선택할 수 있습니다.
         * **원격**&#x200B;은 AEM 인스턴스 외부의 Dynamic Media 라이브러리에서 선택할 수 있습니다.
   * **편집**&#x200B;을 탭하거나 클릭하여 자산 편집기에서 [자산 렌디션을 관리합니다](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html).
* **접근성을 위한 그림 설명** 필드에서는 시각 장애인 독자를 위한 이미지 설명을 정의할 수 있습니다.
   * **페이지에서 그림 설명 상속** 옵션은 DAM에 있는 `dc:description` 메타데이터 또는 연결된 자산이 없는 경우 현재 페이지의 연결된 자산 값에 대한 대체 설명을 사용합니다.
* **그림 설명을 제공하지 않음** 옵션은 이미지가 단순히 장식용이거나 페이지에 추가 정보를 전달하지 않는 경우 화면 판독기와 같은 보조 기술에서 무시되도록 이미지를 표시합니다.

### 스타일 탭 {#styles-tab-edit}

![티저 목록 구성 요소의 편집 대화 상자 스타일 탭](/help/assets/teaser-edit-styles.png)

티저 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

드롭다운을 사용하여 구성 요소에 적용할 스타일을 선택합니다. 편집 대화 상자에서 선택한 항목은 구성 요소 툴바에서 선택한 항목과 동일한 효과를 가집니다.

드롭다운 메뉴를 사용하려면 [디자인 대화 상자](#design-dialog)에서 이 구성 요소에 대한 스타일을 구성해야 합니다.

## 편집 대화 상자 {#edit-dialog}

티저 구성 요소는 이미지 렌더링을 [이미지 구성 요소](image.md)로 위임합니다. 따라서 콘텐츠 작성자는 이미지 구성 요소의 [편집 대화 상자]&#x200B;(image.md#edit-dialog)를 티저 이미지를 조작하는 데 사용할 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 통해 구성 요소 사용 시 필요한 티저 옵션을 정의할 수 있습니다.

### 티저 탭 {#teaser-tab}

![티저 구성 요소의 디자인 대화 상자](/help/assets/teaser-design.png)

* **콜 투 액션**
   * **콜 투 액션 비활성화** - 콘텐츠 작성자를 위한 **콜 투 액션** 옵션을 숨깁니다.
* **요소**
   * **사전 제목 숨기기** - 콘텐츠 작성자를 위한 **사전 제목**&#x200B;을 숨깁니다.
   * **제목 숨기기** - 콘텐츠 작성자를 위한 **제목**&#x200B;을 숨깁니다.
      * 선택한 경우 **제목 유형**&#x200B;을 숨깁니다.
   * **설명 숨기기** - 콘텐츠 작성자를 위한 **설명**&#x200B;을 숨깁니다.
* **기본 제목 유형** - 티저의 제목에 사용될 H 태그를 정의합니다.
* **이미지 위임** - 이미지 처리 시 티저가 위임하는 구성 요소의 정보가 표시됩니다.

### 스타일 탭 {#styles-tab}

티저 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

## Adobe 클라이언트 데이터 레이어 {#data-layer}

티저 구성 요소는 [Adobe 클라이언트 데이터 레이어](/help/developing/data-layer/overview.md)를 지원합니다.

---
title: 티저 구성 요소 (v1)
description: 티저 구성 요소에 이미지, 제목, 서식 있는 텍스트 및 추가 콘텐츠 링크(선택 사항)가 표시될 수 있습니다.
role: Architect, Developer, Admin, User
exl-id: 48e56938-660a-43e7-9e62-8069283ae73f
index: n
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: tm+mt
source-wordcount: '722'
ht-degree: 100%

---


# 티저 구성 요소 (v1) {#teaser-component}

핵심 구성 요소의 티저 구성 요소에 이미지, 제목, 서식 있는 텍스트 및 추가 콘텐츠 링크(선택 사항)가 표시될 수 있습니다.

## 사용 {#usage}

콘텐츠 작성자는 티저 구성 요소를 통해 이미지, 제목이나 서식 있는 텍스트와 추가 콘텐트 링크 또는 기타 작업을 통해 티저를 손쉽게 제작할 수 있습니다.

템플릿 작성자는 [디자인 대화 상자](#design-dialog)를 통해 콜 투 액션을 만들고 링크를 추가하는 옵션을 사용할 수 있는지, 여러 디스플레이 옵션을 활성화할 수 있는지 정의할 수 있습니다. 콘텐츠 작성자는 [구성 대화 상자](#configure-dialog)를 통해 이미지를 설정하고, CTA를 정의하고, 제목 및 설명을 설정하고 링크를 개별 티저로 구성할 수 있습니다. [이미지 구성 요소](image-v1.md)의 [편집 대화 상자](image-v1.md#edit-dialog)에 액세스하여 티저 이미지를 수정할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

티저 구성 요소는 2018년 7월 핵심 구성 요소 릴리스 2.1.0과 함께 도입된 v1입니다. 이 문서에서는 해당 구성 요소에 대해 설명합니다.

>[!CAUTION]
>
>이 문서에서는 티저 구성 요소 v1에 대해 설명합니다.
>
>현재 버전의 티저 구성 요소에 대한 자세한 내용은 [티저 구성 요소](/help/components/teaser.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

티저 구성 요소를 경험하고 구성 옵션의 샘플뿐만 아니라 HTML 및 JSON 출력을 확인하려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_teaser_kr)를 참조하십시오.

### 기술 세부 정보 {#technical-details}

티저 구성 요소에 대한 최신 기술 설명서는 [GitHub](https://adobe.com/go/aem_cmp_tech_teaser_v1_kr)에서 찾아볼 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

콘텐츠 작성자는 구성 대화 상자를 통해 개별 티저의 속성을 정의할 수 있습니다. 이미지가 선택된 경우 [편집 대화 상자](#edit-dialog)에서도 티저 이미지를 수정할 수 있습니다.

### 이미지 {#image}

![티저 구성 요소의 편집 대화 상자 이미지 탭](/help/assets/teaser-edit-image.png)

* **이미지 에셋**
   * [자산 브라우저](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html)에서 자산을 삭제하거나 **검색** 옵션을 탭하여 로컬 파일 시스템에서 로드합니다.
   * **지우기**&#x200B;를 탭하거나 클릭하여 현재 선택된 이미지 선택을 해제합니다.
   * **편집**&#x200B;을 탭하거나 클릭하여 에셋 편집기에서 [에셋 렌디션을 관리합니다](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html).

>[!NOTE]
>
>[Dynamic Media 기능](image-v1.md#dynamic-media)은 현재 티저 구성 요소에서 사용할 수 없습니다.

### 텍스트 {#text}

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

### 링크 및 작업 {#links-actions}

![티저 구성 요소의 편집 대화 상자 링크 탭](/help/assets/teaser-edit-link.png)

* **링크** - 티저에 적용되는 링크. 경로 브라우저를 사용하여 링크 대상을 선택합니다.
* **콜 투 액션 활성화** - 확인 시 콜 투 액션의 정의를 활성화합니다. 목록의 첫 번째 콜 투 액션 링크는 다른 티저 요소의 링크로 사용됩니다.

## 편집 대화 상자 {#edit-dialog}

티저 구성 요소는 이미지 렌더링을 [이미지 구성 요소](image-v1.md)로 위임합니다. 따라서 콘텐츠 작성자는 이미지 구성 요소의 [편집 대화 상자](image-v1.md#edit-dialog)를 티저 이미지를 조작하는 데 사용할 수 있습니다.

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
* **제목 유형** - 티저의 제목에 사용될 H 태그를 정의합니다.
* **링크**
   * **이미지가 연결되지 않음** - 선택한 경우 티저 이미지는 연결되지 않습니다.
   * **제목이 연결되지 않음** - 선택한 경우 티저 제목이 연결되지 않습니다.
* **이미지 전달** - 이미지 처리 시 티저가 전달하는 구성 요소의 정보가 표시됩니다.

### 스타일 탭 {#styles-tab}

티저 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

## Adobe 클라이언트 데이터 레이어 {#data-layer}

티저 구성 요소는 [Adobe 클라이언트 데이터 레이어](/help/developing/data-layer/overview.md)를 지원합니다.

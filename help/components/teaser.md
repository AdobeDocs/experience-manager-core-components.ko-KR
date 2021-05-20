---
title: 티저 구성 요소
description: 티저 구성 요소는 이미지, 제목, 리치 텍스트 및 선택적으로 추가 컨텐츠에 연결할 수 있습니다.
role: Architect, Developer, Administrator, Business Practitioner
exl-id: ec75e168-6f3b-4dff-8df6-06ca7dc18688
source-git-commit: 8ff36ca143af9496f988b1ca65475497181def1d
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 2%

---

# Teaser 구성 요소 {#teaser-component}

핵심 구성 요소 티저 구성 요소는 이미지, 제목, 리치 텍스트를 표시하고 선택적으로 추가 컨텐츠에 연결할 수 있습니다.

## 사용량 {#usage}

티저 구성 요소를 사용하면 컨텐츠 작성자가 이미지, 제목 또는 리치 텍스트를 사용하여 추가 컨텐츠에 티저를 쉽게 만들고 추가 컨텐츠나 기타 작업에 연결할 수 있습니다.

템플릿 작성자는 [디자인 대화 상자](#design-dialog)를 사용하여 클릭유도문안 만들기 및 링크 추가 옵션을 사용할 수 있는지 여부와 다양한 표시 옵션을 비활성화할 수 있습니다. 컨텐츠 작성자는 [구성 대화 상자](#configure-dialog)를 사용하여 이미지를 설정하고, CTA를 정의하고, 제목과 설명을 설정하고, 개별 Teaser에 대한 링크를 구성할 수 있습니다. [이미지 구성 요소](image.md)의 [편집 대화 상자](image.md#edit-dialog)에 액세스하여 티저 이미지를 수정할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

Teaser 구성 요소의 현재 버전은 v1이며, 2018년 7월에 핵심 구성 요소 릴리스 2.1.0에서 도입되었으며 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전이 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |

## 샘플 구성 요소 출력 {#sample-component-output}

Teaser 구성 요소를 경험하고 구성 옵션의 예와 HTML 및 JSON 출력을 보려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_teaser)를 방문하십시오.

### 기술 세부 정보 {#technical-details}

Teaser 구성 요소 [에 대한 최신 기술 설명서는 GitHub](https://adobe.com/go/aem_cmp_tech_teaser_v1)에 있습니다.

코어 구성 요소 개발에 대한 자세한 내용은 [코어 구성 요소 개발자 설명서](/help/developing/overview.md)에서 확인할 수 있습니다.

## 구성 대화 상자 {#configure-dialog}

컨텐츠 작성자는 구성 대화 상자를 사용하여 개별 Teaser의 속성을 정의할 수 있습니다. 또한 [편집 대화 상자](#edit-dialog)가 선택되어 있으면 Teaser 이미지를 수정할 수 있습니다.

### 이미지 {#image}

![Teaser 구성 요소의 편집 대화 상자 이미지 탭](/help/assets/teaser-edit-image.png)

* **이미지 자산**
   * [자산 브라우저](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html)에서 자산을 끌어 놓거나 **찾아보기** 옵션을 탭하여 로컬 파일 시스템에서 업로드합니다.
   * **지우기**&#x200B;를 탭하거나 클릭하여 현재 선택한 이미지를 선택 취소합니다.
   * **편집**&#x200B;을 탭하거나 클릭하여 [자산 편집기에서 자산](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/manage/manage-digital-assets.html)의 변환을 관리합니다.

>[!NOTE]
>
>[Dynamic Media ](image.md#dynamic-media) 기능은 현재 티저 구성 요소에서 사용할 수 없습니다.

### 텍스트 {#text}

![Teaser 구성 요소의 편집 대화 상자 텍스트 탭](/help/assets/teaser-edit-text.png)

* **사전 제목**  - 사전 제목이 티저의 제목 앞에 표시됩니다.
* **제목**  - 티저의 헤드라인으로 표시할 제목을 정의합니다.
   * **연결된 페이지에서 제목 가져오기**  - 이 확인란을 선택하면 제목이 연결된 페이지의 제목으로 채워집니다.
* **설명**  - 티저의 하위 머리글로 표시할 설명을 정의합니다.
   * **연결된 페이지에서 설명 가져오기**  - 이 확인란을 선택하면 설명이 연결된 페이지의 설명으로 채워집니다.
* **ID**  - 이 옵션을 사용하면 HTML과  [데이터 레이어에서 구성 요소의 고유 식별자를 제어할 수 있습니다](/help/developing/data-layer/overview.md).
   * 비워 두면 고유 ID가 자동으로 생성되며 결과 페이지를 검사하여 찾을 수 있습니다.
   * ID가 지정된 경우 ID가 고유한지 확인하는 것은 작성자의 책임입니다.
   * ID를 변경하면 CSS, JS 및 데이터 레이어 추적에 영향을 줄 수 있습니다.

### 링크 및 작업 {#links-actions}

![Teaser 구성 요소의 편집 대화 상자 링크 탭](/help/assets/teaser-edit-link.png)

* **링크**  - 티저에 적용되는 링크. 경로 브라우저를 사용하여 링크 대상을 선택합니다.
* **클릭유도문안 사용**  - 이 확인란을 선택하면 클릭유도문안 정의를 사용할 수 있습니다. 목록에 있는 첫 번째 클릭유도문안 링크는 다른 티저 요소에 대한 링크로 사용됩니다.

## 편집 대화 상자 {#edit-dialog}

Teaser 구성 요소는 [이미지 구성 요소](image.md)에 이미지 렌더링을 위임합니다. 따라서 컨텐츠 작성자는 [편집 대화 상자](이미지 구성 요소의 image.md#edit-dialog)를 사용하여 티저 이미지를 조작할 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

디자인 대화 상자에서는 템플릿 작성자가 이 구성 요소를 사용할 때 컨텐츠 작성자가 갖는 티저 옵션을 정의할 수 있습니다.

### Teaser 탭 {#teaser-tab}

![Teaser 구성 요소의 디자인 대화 상자](/help/assets/teaser-design.png)

* **클릭 유도 문안**
   * **클릭유도문안 사용 안 함**  -  **컨텐츠 작성자에 대한** 클릭유도문안 옵션 숨기기
* **요소**
   * **사전 제목 숨기기**  - 컨텐츠 작성자에  **** 대한 사전 제목 옵션을 숨깁니다.
   * **제목 숨기기**  - 컨텐츠 작성자에  **** 대한 제목 옵션을 숨깁니다.
      * **제목 유형**&#x200B;이 숨겨집니다
   * **설명 숨기기**  - 컨텐츠 작성자에  **** 대한 설명 옵션을 숨깁니다.
* **제목 유형**  - 티저의 제목에 사용할 H 태그를 정의합니다.
* **링크**
   * **이미지를 연결하지 않음**  - 선택하면 티저 이미지가 연결되지 않습니다
   * **제목 연결 안 함**  - 선택하면 티저 제목이 연결되지 않습니다
* **이미지 위임**  - Teaser가 이미지 처리를 위임하는 구성 요소를 나타내는 정보 표시입니다.

### 스타일 탭 {#styles-tab}

Teaser 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

## Adobe 클라이언트 데이터 계층 {#data-layer}

Teaser 구성 요소는 [Adobe 클라이언트 데이터 계층을 지원합니다.](/help/developing/data-layer/overview.md)

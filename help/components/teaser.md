---
title: Teaser 구성 요소
description: Teaser 구성 요소는 이미지, 제목, 리치 텍스트 및 추가 컨텐츠에 연결할 수 있습니다.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Teaser 구성 요소 {#teaser-component}

핵심 구성 요소 티저 구성 요소는 이미지, 제목, 리치 텍스트 및 선택적으로 추가 컨텐츠에 연결할 수 있습니다.

## 사용량 {#usage}

Teaser 구성 요소를 사용하면 컨텐츠 작성자가 이미지, 제목 또는 리치 텍스트를 사용하여 추가 컨텐츠에 Teaser를 쉽게 만들고 추가 컨텐츠 또는 기타 작업에 연결할 수 있습니다.

템플릿 작성자는 [디자인 대화 상자를](#design-dialog) 사용하여 클릭유도문안 작성 및 링크 추가 옵션을 사용할 수 있는지 여부와 다양한 표시 옵션을 비활성화할 수 있습니다. 컨텐츠 작성자는 [구성 대화 상자를](#configure-dialog) 사용하여 이미지를 설정하고, CTA를 정의하고, 제목과 설명을 설정하고, 개별 Teaser에 대한 링크를 구성할 수 있습니다. 이미지 구성 요소의 [편집 대화](image.md#edit-dialog) 상자를 [](image.md) 사용하여 티저 이미지를 수정할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

Teaser 구성 요소의 현재 버전은 v1이며, 이 버전은 2018년 7월 핵심 구성 요소 릴리스 2.1.0에서 도입되었으며 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소 버전이 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.3 | AEM 6.4 | AEM 6.5 | 클라우드 서비스로 AEM 사용 |
|---|---|---|---|---|
| v1 | 호환 가능 | 호환 가능 | 호환 가능 | 호환 가능 |

## 샘플 구성 요소 출력 {#sample-component-output}

Teaser 구성 요소뿐만 아니라 구성 옵션의 예제도 및 HTML 및 JSON 출력을 보려면 구성 요소 [라이브러리를 방문하십시오](https://adobe.com/go/aem_cmp_library_teaser).

### 기술 정보 {#technical-details}

Teaser 구성 요소에 대한 최신 기술 문서는 GitHub에서 [찾을 수 있습니다](https://adobe.com/go/aem_cmp_tech_teaser_v1).

핵심 구성 요소 개발에 대한 자세한 내용은 핵심 구성 요소 개발자 [설명서를](/help/developing/overview.md)참조하십시오.

## 구성 대화 상자 {#configure-dialog}

컨텐츠 작성자는 구성 대화 상자를 사용하여 개별 티저의 속성을 정의할 수 있습니다. Teaser 이미지를 선택한 경우 [편집 대화 상자가](#edit-dialog) 있습니다.

### 이미지 {#image}

![](/help/assets/screen_shot_2018-07-03at104125.png)

* **이미지 자산**
   * 자산 브라우저에서 [자산을 삭제하거나](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) 찾아보기 **** 옵션을 눌러 로컬 파일 시스템에서 업로드합니다.
   * 지우기를 탭하거나 **클릭하여** 현재 선택한 이미지를 선택 취소합니다.
   * 편집을 탭하거나 **클릭하여** 자산 [편집기에서 자산의](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) 표현물을관리합니다.

### 텍스트 {#text}

![](/help/assets/screen_shot_2018-07-03at104138.png)

* **제목티저의**&#x200B;제목으로 표시할 제목을 정의합니다.
* **연결된 페이지에서**&#x200B;제목 가져오기가 선택되면 연결된 페이지의 제목으로 제목이 채워집니다.
* **설명** Teaser의 하위 머리글로 표시할 설명을 정의합니다.
* **연결된 페이지에서**&#x200B;설명 가져오기 이 확인란을 선택하면 연결된 페이지의 설명이 채워집니다.

### 링크 및 작업 {#links-actions}

![](/help/assets/screen_shot_2018-07-03at104146.png)

* **링크** Teaser에 적용된 링크입니다. 경로 브라우저를 사용하여 링크 대상을 선택합니다.
* **클릭유도문안 사용**&#x200B;이 선택되면 클릭유도문안의 정의를 활성화합니다. 목록의 첫 번째 클릭유도문안 링크는 다른 티저 요소에 대한 링크로 사용됩니다.

## Edit Dialog {#edit-dialog}

Teaser 구성 요소는 이미지 구성 요소에 이미지 렌더링을 [위임합니다](image.md). 따라서 컨텐츠 작성자는 [편집 대화]상자(이미지 구성 요소의 image.md#edit-dialog)를 사용하여 티저 이미지를 조작할 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 사용하여 컨텐츠 작성자가 이 구성 요소를 사용할 때 가지는 티저 옵션을 정의할 수 있습니다.

### Teaser 탭 {#teaser-tab}

![](/help/assets/screen_shot_2018-07-03at105958.png)

* **클릭 유도 문안**
   * **클릭유도문안 사용**&#x200B;컨텐츠 작성자에 **대한 클릭유도문안** 옵션 숨기기
* **요소**
   * **제목 숨기기**
      * 컨텐츠 작성자의 **제목** 옵션을 숨깁니다.
      * 이 옵션을 선택하면 **제목 유형이** 숨겨집니다
   * **설명**&#x200B;숨기기컨텐츠 작성자에 **대한 설명** 옵션 숨기기
* **제목**&#x200B;유형티저의 제목에 사용할 H 태그를 정의합니다.
* **링크**
   * **이미지**&#x200B;연결 안 함
   * **제목**&#x200B;연결 안 함

### 스타일 탭 {#styles-tab}

Teaser 구성 요소는 AEM Style [System을 지원합니다](/help/get-started/authoring.md#component-styling).

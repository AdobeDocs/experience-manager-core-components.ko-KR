---
title: 구성 요소 다운로드
description: 코어 구성 요소 다운로드 구성 요소를 사용하면 페이지에 다운로드 옵션을 만들 수 있습니다.
role: Architect, Developer, Administrator, Business Practitioner
exl-id: 48e7ade0-b849-4d1f-b836-51196e5ac507
source-git-commit: 8ff36ca143af9496f988b1ca65475497181def1d
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 1%

---

# 구성 요소 다운로드{#download-component}

코어 구성 요소 다운로드 구성 요소를 사용하면 페이지에 다운로드 옵션을 만들 수 있습니다.

## 사용량 {#usage}

핵심 구성 요소 다운로드 구성 요소를 사용하면 다운로드 옵션 및 관련 자산을 페이지에 포함할 수 있습니다.

* [구성 대화 상자](#configure-dialog)에서 다운로드 옵션의 속성을 선택할 수 있습니다.
* 다운로드 구성 요소의 기본값은 [디자인 대화 상자](#design-dialog)에서 정의할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

다운로드 구성 요소의 현재 버전은 v1이며, 2019년 6월에 핵심 구성 요소 릴리스 2.5.0에서 도입되었으며, 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전이 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

구성 요소 다운로드 와 구성 옵션의 예 및 HTML 및 JSON 출력을 보려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_download)를 방문하십시오.

## 기술 세부 정보 {#technical-details}

구성 요소 다운로드 [에 대한 최신 기술 설명서는 GitHub](https://adobe.com/go/aem_cmp_tech_download_v1)에 있습니다.

코어 구성 요소 개발에 대한 자세한 내용은 [코어 구성 요소 개발자 설명서](/help/developing/overview.md)에서 확인할 수 있습니다.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자에서는 컨텐츠 작성자가 다운로드 항목 및 방문자가 페이지에 대해 어떻게 작동하고 나타나는지 정의할 수 있습니다.

![구성 요소 편집 대화 상자의 자산 탭](/help/assets/download-edit-asset.png)

### 자산 탭 {#asset-tab}

다운로드 자산을 선택하는 것은 [이미지 구성 요소](image.md)의 기능과 매우 유사하며, 마찬가지로 AEM DAM을 활용합니다.

* **자산 다운로드**
   * [자산 브라우저](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html)에서 자산을 끌어 놓거나 **찾아보기** 옵션을 탭하여 로컬 파일 시스템에서 업로드합니다.
   * **지우기**&#x200B;를 탭하거나 클릭하여 현재 선택한 이미지를 선택 취소합니다.
   * **편집**&#x200B;을 탭하거나 클릭하여 [자산 편집기에서 자산](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/manage/manage-digital-assets.html)의 변환을 관리합니다.

### 속성 탭 {#properties-tab}

![구성 요소 편집 대화 상자의 속성 탭](/help/assets/download-edit-properties.png)

* **제목**  - 다운로드 항목의 헤드라인으로 표시됩니다
   * **DAM 자산에서 제목 가져오기**  - 이 옵션을 선택하면 제목이 DAM 자산의 제목으로 자동으로 채워집니다.
* **설명**  - 다운로드 항목의 설명 하위 헤드라인으로 표시됩니다
   * **DAM 자산에서 설명 가져오기**  - 이 옵션을 선택하면 설명이 DAM 자산의 설명으로 자동으로 채워집니다.
* **작업 텍스트**  - 다운로드 항목에 대한 작업 텍스트로 표시됩니다
   * 이 필드는 파일 시스템에서 자산을 업로드할 때 필요합니다.
   * **인라인 표시**  - 제공된 작업 텍스트 **를** 선택하면 인라인이 표시됩니다.
* **ID**  - 이 옵션을 사용하면 HTML과  [데이터 레이어에서 구성 요소의 고유 식별자를 제어할 수 있습니다](/help/developing/data-layer/overview.md).
   * 비워 두면 고유 ID가 자동으로 생성되며 결과 페이지를 검사하여 찾을 수 있습니다.
   * ID가 지정된 경우 ID가 고유한지 확인하는 것은 작성자의 책임입니다.
   * ID를 변경하면 CSS, JS 및 데이터 레이어 추적에 영향을 줄 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

디자인 대화 상자에서는 템플릿 작성자가 다운로드 구성 요소를 사용하는 컨텐츠 작성자가 사용할 수 있는 옵션을 정의할 수 있습니다.

### 속성 탭 {#properties-tab-design}

![구성 요소 다운로드 의 디자인 대화 상자](/help/assets/download-design.png)

* **파일 시스템에서 업로드 허용**  - 컨텐츠 작성자가 로컬 파일 시스템의 자산을 다운로드 자산으로 업로드할 수 있습니다.
   * 기본값이 선택되어 있지 않습니다.
* **제목 유형**  - 다운로드 구성 요소의 제목에 사용되는 HTML 요소입니다.
   * 값을 선택하지 않으면 기본값은 H3입니다.
* **파일 크기 표시**  - 선택하면 자산의 파일 크기가 다운로드 구성 요소에 표시됩니다.
   * 기본값이 선택되어 있습니다.
* **파일 형식 표시**  - 선택하면 자산의 파일 형식이 다운로드 구성 요소에 표시됩니다.
   * 기본값이 선택되어 있습니다.
* **파일 이름 표시**  - 이 옵션을 선택하면 자산의 파일 이름이 다운로드 구성 요소에 표시됩니다.
   * 기본값이 선택되어 있습니다.

### 스타일 탭 {#styles-tab}

이미지 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

---
title: 구성 요소 다운로드 (v1)
description: 핵심 구성 요소의 다운로드 구성 요소를 사용하여 페이지에서 다운로드 옵션을 만들 수 있습니다.
role: Architect, Developer, Admin, User
exl-id: ebd63522-218d-4784-bea0-1627c64f5230
index: n
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: ht
source-wordcount: '621'
ht-degree: 100%

---


# 구성 요소 다운로드 (v1) {#download-component}

핵심 구성 요소의 다운로드 구성 요소를 사용하여 페이지에서 다운로드 옵션을 만들 수 있습니다.

## 사용량 {#usage}

핵심 구성 요소의 다운로드 구성 요소를 사용하여 페이지에 다운로드 옵션과 연결된 자산을 포함할 수 있습니다.

* [구성 대화 상자](#configure-dialog)에서 다운로드 옵션의 속성을 선택할 수 있습니다.
* [디자인 대화 상자](#design-dialog)에서 다운로드 구성 요소의 기본값을 정의할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

다운로드 구성 요소는 2019년 6월 핵심 구성 요소 릴리스 2.5.0과 함께 도입된 v1입니다. 이 문서에서는 해당 구성 요소에 대해 설명합니다.

>[!CAUTION]
>
>이 문서에서는 다운로드 구성 요소 v1에 대해 설명합니다.
>
>현재 버전의 다운로드 구성 요소에 대한 자세한 내용은 [다운로드 구성 요소](/help/components/download.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

다운로드 구성 요소를 경험하고 구성 옵션의 샘플뿐만 아니라 HTML 및 JSON 출력을 확인하려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_download_kr)를 참조하십시오.

## 기술 세부 정보 {#technical-details}

다운로드 구성 요소에 대한 최신 기술 설명서는 [GitHub에서 확인할 수 있습니다](https://adobe.com/go/aem_cmp_tech_download_v1_kr).

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

콘텐츠 작성자는 구성 대화 상자를 통해 다운로드 항목과 방문자를 위한 페이지 작동 및 표시 방법을 정의할 수 있습니다.

![다운로드 구성 요소의 디자인 대화 상자 자산 탭](/help/assets/download-edit-asset.png)

### 자산 탭 {#asset-tab}

자산 다운로드 선택은 [이미지 구성 요소](image-v1.md) 기능과 매우 유사합니다. 이와 마찬가지로 AEM의 DAM을 활용합니다.

* **자산 다운로드**
   * [자산 브라우저](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html)에서 자산을 삭제하거나 **검색** 옵션을 탭하여 로컬 파일 시스템에서 로드합니다.
   * **지우기**&#x200B;를 탭하거나 클릭하여 현재 선택된 이미지 선택을 해제합니다.
   * **편집**&#x200B;을 탭하거나 클릭하여 자산 편집기에서 [자산 렌디션을 관리합니다](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html).

### 속성 탭 {#properties-tab}

![다운로드 구성 요소의 디자인 대화 상자 속성 탭](/help/assets/download-edit-properties.png)

* **제목** - 다운로드 항목의 헤드라인으로 표시됩니다.
   * **DAM 자산에서 제목 다운로드** - 선택되면 제목이 DAM 자산의 제목으로 자동 채워집니다.
* **설명** - 다운로드 항목의 설명 서브헤드라인으로 표시됩니다.
   * **DAM 자산에서 설명 다운로드** - 선택되면 설명이 DAM 자산의 설명으로 자동 채워집니다.
* **작업 텍스트** - 다운로드 항목의 작업 텍스트로 표시됩니다.
   * 파일 시스템에서 자산을 업로드할 때 이 필드가 필수입니다.
   * **인라인 표시** - 선택되면 제공된 **작업 텍스트**&#x200B;가 인라인으로 표시됩니다.
* **ID** - 이 옵션을 통해 HTML과 [데이터 레이어](/help/developing/data-layer/overview.md)에서 구성 요소의 고유 식별자를 제어할 수 있습니다.
   * 비워 두면 고유 ID는 자동으로 생성되고 결과 페이지 검사를 통해 발견될 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID가 변경되면 CSS, JS 및 데이터 레이어 추적에 영향을 미칠 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 통해 다운로드 구성 요소를 사용하는 콘텐츠 작성자에게 제공되는 옵션을 정의할 수 있습니다.

### 속성 탭 {#properties-tab-design}

![다운로드 구성 요소의 디자인 대화 상자](/help/assets/download-design.png)

* **파일 시스템에서 업로드 허용** - 콘텐츠 작성자는 자신의 로컬 파일 시스템에서 자산 다운로드로 자산을 업로드할 수 있습니다.
   * 기본값이 선택되지 않습니다.
* **제목 유형** - 다운로드 구성 요소 제목에 사용되는 HTML 요소.
   * 값이 선택되지 않으면 기본값은 H3입니다.
* **파일 크기 표시** - 선택되면 자산의 파일 크기가 다운로드 구성 요소에 표시됩니다.
   * 기본값이 선택됩니다.
* **파일 포맷 표시** - 선택되면 자산의 파일 포맷이 다운로드 구성 요소에 표시됩니다.
   * 기본값이 선택됩니다.
* **파일 이름 표시** - 선택되면 자산의 파일 이름이 다운로드 구성 요소에 표시됩니다.
   * 기본값이 선택됩니다.

### 스타일 탭 {#styles-tab}

이미지 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

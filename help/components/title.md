---
title: 제목 구성 요소
description: 코어 구성 요소 제목 구성 요소는 즉석 편집 기능을 하는 섹션 제목 구성 요소입니다.
role: Architect, Developer, Administrator, Business Practitioner
exl-id: 393af72c-549f-4609-afb0-2712f827b549
source-git-commit: 8ff36ca143af9496f988b1ca65475497181def1d
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 3%

---

# 제목 구성 요소{#title-component}

코어 구성 요소 제목 구성 요소는 즉석 편집 기능을 하는 섹션 제목 구성 요소입니다.

## 사용량 {#usage}

제목 구성 요소는 컨텐츠 섹션의 제목 또는 머리글로 사용됩니다. 사용 가능한 제목 수준은 [디자인 대화 상자](#design-dialog)에서 템플릿 작성자가 정의할 수 있습니다. 콘텐츠 편집기는 [편집 대화 상자의 사용 가능한 머리글 수준 중에서 선택할 수 있습니다](#edit-dialog). 편의상, 제목 텍스트를 즉석 편집할 수도 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

제목 구성 요소의 현재 버전은 v2이며, 2018년 1월에 핵심 구성 요소 릴리스 2.0.0에서 도입되었으며, 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전이 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v2 | 호환 가능 | 호환 가능 | 호환 가능 |
| [v1](v1/title-v1.md) | 호환 가능 | 호환 가능 | - |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

제목 구성 요소 와 구성 옵션의 예 및 HTML 및 JSON 출력을 보려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_title)를 방문하십시오.

### 기술 세부 정보 {#technical-details}

제목 구성 요소 [에 대한 최신 기술 설명서는 GitHub](https://adobe.com/go/aem_cmp_tech_title_v2)에 있습니다.

코어 구성 요소 개발에 대한 자세한 내용은 [코어 구성 요소 개발자 설명서](/help/developing/overview.md)에서 확인할 수 있습니다.

## 편집 대화 상자 {#edit-dialog}

편집 대화 상자에서는 컨텐츠 작성자가 제목 텍스트를 정의하고 제목 수준을 선택할 수 있습니다.

* **제목**  - 비어 있으면 페이지 제목이 사용됩니다
* **유형 / 크기**  - 제목의 제목 수준을 정의합니다
* **링크**  - 제목을 연결할 콘텐츠를 정의합니다. 컨텐츠 페이지, 외부 URL 또는 페이지 앵커의 경로일 수 있습니다.
* **ID**  - 이 옵션을 사용하면 HTML과  [데이터 레이어에서 구성 요소의 고유 식별자를 제어할 수 있습니다](/help/developing/data-layer/overview.md).
   * 비워 두면 고유 ID가 자동으로 생성되며 결과 페이지를 검사하여 찾을 수 있습니다.
   * ID가 지정된 경우 ID가 고유한지 확인하는 것은 작성자의 책임입니다.
   * ID를 변경하면 CSS, JS 및 데이터 레이어 추적에 영향을 줄 수 있습니다.

![제목 구성 요소의 편집 대화 상자](/help/assets/title-edit.png)

>[!NOTE]
>
>제목에 대한 링크를 정의하는 기능이 핵심 구성 요소의 릴리스 2.2.0에서 도입되었습니다.

즉석 편집기를 사용하여 제목 구성 요소의 텍스트를 편집할 수도 있습니다.

![제목 구성 요소의 즉석 편집](/help/assets/title-edit-inline.png)

## 디자인 대화 상자 {#design-dialog}

디자인 대화 상자에서는 템플릿 작성자가 컨텐츠 작성자가 만들 때 제목 구성 요소가 가질 기본 제목 수준을 정의할 수 있습니다.

### 크기 탭 {#sizes-tab}

![제목 구성 요소의 디자인 대화 상자](/help/assets/title-design.png)

* **작성자에 대해 허용되는 유형/크기**  - 컨텐츠 작성자가 제목 구성 요소를 사용할 때 사용할 수 있는 제목 유형을 활성화하거나 비활성화합니다.
* **기본 유형 / 크기** - 컨텐츠 작성자가 페이지에 제목 구성 요소를 추가할 때 자동으로 지정되는 제목 유형을 정의합니다.
* **링크 비활성화** - 컨텐츠 작성자가 제목에서 링크하지 못하도록 제목 구성 요소의 링크에 대한 지원을 비활성화합니다.

>[!NOTE]
>
>제목에 대한 링크를 정의하는 기능이 핵심 구성 요소의 릴리스 2.2.0에서 도입되었습니다.

### 스타일 탭 {#styles-tab}

제목 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

## Adobe 클라이언트 데이터 계층 {#data-layer}

제목 구성 요소는 [Adobe 클라이언트 데이터 계층을 지원합니다.](/help/developing/data-layer/overview.md)

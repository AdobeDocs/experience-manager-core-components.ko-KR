---
title: 제목 구성 요소 (v2)
description: 핵심 구성 요소의 제목 구성 요소는 바로 편집 기능이 있는 섹션 머리말 구성 요소입니다.
role: Architect, Developer, Admin, User
exl-id: f853ec46-19fd-4569-a9d3-5c376d2a2101
index: n
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: ht
source-wordcount: '521'
ht-degree: 100%

---


# 제목 구성 요소 (v2) {#title-component}

핵심 구성 요소의 제목 구성 요소는 바로 편집 기능이 있는 섹션 머리말 구성 요소입니다.

## 사용량 {#usage}

제목 구성 요소는 콘텐츠 섹션의 제목이나 머리글로 사용하기 위한 목적으로 작성되었습니다. 템플릿 작성자는 [디자인 대화 상자](#design-dialog)에서 사용 가능한 제목 수준을 정의할 수 있습니다. 콘텐츠 편집기는 [편집 대화 상자](#edit-dialog)에서 사용 가능한 제목 수준 중 하나를 선택할 수 있습니다. 편리성을 추가하기 위해 머리글 텍스트의 간단한 바로 편집 기능을 사용할 수도 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

제목 구성 요소는 2018년 1월 핵심 구성 요소 릴리스 2.0.0과 함께 도입된 v2입니다. 이 문서에서는 해당 구성 요소에 대해 설명합니다.

>[!CAUTION]
>
>이 문서에서는 제목 구성 요소 v2에 대해 설명합니다.
>
>현재 버전의 제목 구성 요소에 대한 자세한 내용은 [제목 구성 요소](/help/components/title.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

제목 구성 요소를 경험하고 구성 옵션의 샘플뿐만 아니라 HTML 및 JSON 출력을 확인하려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_title_kr)를 참조하십시오.

### 기술 세부 정보 {#technical-details}

제목 구성 요소에 대한 최신 기술 설명서는 [GitHub에서 확인할 수 있습니다](https://adobe.com/go/aem_cmp_tech_title_v2_kr).

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

## 편집 대화 상자 {#edit-dialog}

콘텐츠 작성자는 편집 대화 상자를 통해 제목 텍스트를 정의하고 제목 수준을 선택할 수 있습니다.

* **제목** - 비어 있는 경우 페이지 제목이 사용됩니다.
* **유형/크기** - 제목의 제목 수준을 정의합니다.
* **링크** - 제목이 링크할 콘텐츠를 정의합니다. 콘텐츠 페이지, 외부 URL이나 페이지 앵커의 경로일 수 있습니다.
* **ID** - 이 옵션을 통해 HTML과 [데이터 레이어](/help/developing/data-layer/overview.md)에서 구성 요소의 고유 식별자를 제어할 수 있습니다.
   * 비워 두면 고유 ID는 자동으로 생성되고 결과 페이지 검사를 통해 발견될 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID가 변경되면 CSS, JS 및 데이터 레이어 추적에 영향을 미칠 수 있습니다.

![제목 구성 요소의 편집 대화 상자](/help/assets/title-edit.png)

>[!NOTE]
>
>핵심 구성 요소 릴리스 2.2.0과 함께 제목의 링크 정의 기능이 도입되었습니다.

바로 편집 기능을 가진 편집기를 사용하여 제목 구성 요소의 텍스트를 편집합니다.

![제목 구성 요소 바로 편집](/help/assets/title-edit-inline.png)

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 통해 콘텐츠 작성자가 제목 구성 요소를 생성할 때 이에 포함될 기본 제목 수준을 정의할 수 있습니다.

### 크기 탭 {#sizes-tab}

![제목 구성 요소의 디자인 대화 상자](/help/assets/title-design.png)

* **작성자에게 허용된 유형/크기** - 제목 구성 요소를 사용하는 경우 콘텐츠 작성자가 사용할 수 있는 머리말 유형을 활성화하거나 비활성화합니다.
* **기본 유형/크기** - 구성 요소를 페이지에 추가할 때 콘텐츠 작성자는 자동으로 할당되는 머리말 유형을 정의합니다.
* **링크 비활성화** - 제목 구성 요소에서 링크 지원을 비활성화하면 콘텐츠 작성자는 제목에서 링크할 수 없습니다.

>[!NOTE]
>
>핵심 구성 요소 릴리스 2.2.0과 함께 제목의 링크 정의 기능이 도입되었습니다.

### 스타일 탭 {#styles-tab}

제목 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

## Adobe 클라이언트 데이터 레이어 {#data-layer}

제목 구성 요소는 [Adobe 클라이언트 데이터 레이어](/help/developing/data-layer/overview.md)를 지원합니다.

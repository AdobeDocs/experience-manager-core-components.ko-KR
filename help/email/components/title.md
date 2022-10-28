---
title: 이메일 제목 구성 요소
description: 이메일 제목 구성 요소는 즉석 편집 기능을 제공하는 이메일의 섹션 제목 구성 요소입니다.
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: tm+mt
source-wordcount: '636'
ht-degree: 47%

---


# 이메일 제목 구성 요소 {#email-title-component}

이메일 제목 구성 요소는 즉석 편집 기능을 제공하는 이메일의 섹션 제목 구성 요소입니다.

## 사용량 {#usage}

이메일 제목 구성 요소는 이메일의 제목 또는 머리글로 사용됩니다.

* 템플릿 작성자는 [디자인 대화 상자](#design-dialog)에서 사용 가능한 머리말 수준을 정의할 수 있습니다.
* 컨텐츠 작성자는 [편집 대화 상자](#edit-dialog)

편리성을 추가하기 위해 머리글 텍스트의 간단한 바로 편집 기능을 사용할 수도 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

이메일 제목 구성 요소의 현재 버전은 v1이며, 2022년 10월에 이메일 핵심 구성 요소의 릴리스 x에서 도입되었으며 이 문서에 설명되어 있습니다.

다음 표에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 문서를 참조하십시오 [핵심 이메일 구성 요소 버전](/help/versions.md).

## 샘플 구성 요소 출력 {#sample-component-output}

제목 구성 요소 와 구성 옵션의 예 및 HTML 및 JSON 출력을 보려면 [구성 요소 라이브러리.](https://adobe.com/go/aem_cmp_library_email_title)

### 기술 세부 사항 {#technical-details}

제목 구성 요소에 대한 최신 기술 설명서는[ GitHub에서 확인할 수 있습니다](https://adobe.com/go/aem_cmp_tech_email_title_v1).

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

## 편집 대화 상자 {#edit-dialog}

콘텐츠 작성자는 편집 대화 상자를 통해 제목 텍스트를 정의하고 머리말 수준을 선택할 수 있습니다.

* **제목** - 비어 있는 경우 페이지 제목이 사용됩니다.
   * Campaign 아이콘을 클릭하여 [Adobe Campaign 변수 선택](/help/email/campaign-variables.md) 대화 상자에서 Adobe Campaign의 동적 콘텐츠를 삽입할 수 있습니다.
* **유형/크기** - 제목의 머리말 수준을 정의합니다.
* **링크** - 제목이 링크할 콘텐츠를 정의합니다. 콘텐츠 페이지, 외부 URL이나 페이지 앵커의 경로일 수 있습니다.
   * Campaign 아이콘을 클릭하여 [Adobe Campaign 변수 선택](/help/email/campaign-variables.md) 대화 상자에서 Adobe Campaign의 동적 콘텐츠를 삽입할 수 있습니다.
* **ID** - 이 옵션을 사용하면 HTML에서 구성 요소의 고유 식별자를 제어할 수 있습니다.
   * 비워 두면 고유 ID는 자동으로 생성되고 결과 페이지 검사를 통해 발견될 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID를 변경하면 CSS에 영향을 줄 수 있습니다.

![이메일 제목 구성 요소의 편집 대화 상자](/help/email/assets/email-title-edit.png)

바로 편집 기능을 가진 편집기를 사용하여 제목 구성 요소의 텍스트를 편집합니다.

![이메일 제목 구성 요소의 즉석 편집](/help/email/assets/email-title-edit-inline.png)

### 스타일 탭 {#styles-tab-edit}

이메일 제목 구성 요소는 AEM을 지원합니다 [스타일 시스템.](/help/get-started/authoring.md#component-styling)

드롭다운을 사용하여 구성 요소에 적용할 스타일을 선택합니다. 편집 대화 상자에서 선택한 항목은 구성 요소 툴바에서 선택한 항목과 동일한 효과를 가집니다.

스타일을 [디자인 대화 상자](#design-dialog) 을 클릭하여 드롭다운 메뉴를 사용할 수 있습니다.

![제목 구성 요소의 디자인 대화 상자 스타일 탭](/help/email/assets/email-title-edit-styles.png)

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 통해 콘텐츠 작성자가 제목 구성 요소를 생성할 때 이에 포함될 기본 머리말 수준을 정의할 수 있습니다.

### 크기 탭 {#sizes-tab}

![제목 구성 요소의 디자인 대화 상자](/help/email/assets/email-title-design.png)

* **작성자에 대해 허용되는 유형/크기** - 컨텐츠 작성자가 이메일 제목 구성 요소를 사용할 때 사용할 수 있는 제목 유형을 활성화하거나 비활성화합니다.
* **기본 유형 / 크기** - 컨텐츠 작성자가 페이지에 이메일 제목 구성 요소를 추가할 때 자동으로 할당되는 제목 유형을 정의합니다.
* **링크 비활성화** - 컨텐츠 작성자가 제목에서 연결할 수 없도록 하려면 이메일 제목 구성 요소의 링크에 대한 지원을 비활성화합니다.

### 스타일 탭 {#styles-tab}

이메일 제목 구성 요소는 AEM을 지원합니다 [스타일 시스템](/help/get-started/authoring.md#component-styling).

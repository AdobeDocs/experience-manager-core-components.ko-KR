---
title: 이메일 제목 구성 요소
description: 이메일 제목 구성 요소는 바로 편집 기능이 있는 이메일 섹션 머리말 구성 요소입니다.
role: Architect, Developer, Admin, User
exl-id: f65b6973-bb36-406f-bbea-f85a23f5340b
index: false
source-git-commit: eb77567dc32cccb81a9fc131493d11fb55b7e93b
workflow-type: ht
source-wordcount: '596'
ht-degree: 100%

---


# 이메일 제목 구성 요소 {#email-title-component}

이메일 제목 구성 요소는 바로 편집 기능이 있는 이메일 섹션 머리말 구성 요소입니다.

## 사용 {#usage}

이메일 제목 구성 요소는 이메일 섹션의 제목이나 머리글로 사용하기 위한 목적으로 작성되었습니다.

* 템플릿 작성자는 [디자인 대화 상자](#design-dialog)에서 사용 가능한 머리말 수준을 정의할 수 있습니다.
* 콘텐츠 작성자는 [편집 대화 상자](#edit-dialog)에서 사용 가능한 머리말 수준 중 하나를 선택할 수 있습니다.

편리성을 추가하기 위해 머리글 텍스트의 간단한 바로 편집 기능을 사용할 수도 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

현재 버전의 이메일 제목 구성 요소는 2022년 10월 이메일 핵심 구성 요소 릴리스 x과(와) 함께 도입된 v1입니다. 이 문서에서는 해당 구성 요소에 대해 설명합니다.

다음 테이블에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| v1 | 호환 가능 | - | - |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 문서 [이메일 핵심 이메일 구성 요소 버전](/help/versions.md)을 참조하십시오.

### 기술 세부 정보 {#technical-details}

제목 구성 요소에 대한 최신 기술 설명서는 [GitHub에서 확인할 수 있습니다](https://adobe.com/go/aem_cmp_tech_email_title_v1_kr).

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

## 편집 대화 상자 {#edit-dialog}

콘텐츠 작성자는 편집 대화 상자를 통해 제목 텍스트를 정의하고 머리말 수준을 선택할 수 있습니다.

* **제목** - 비어 있는 경우 페이지 제목이 사용됩니다.
   * Campaign 아이콘을 클릭하여 Adobe Campaign의 다이내믹 콘텐츠를 삽입하기 위한 [Adobe Campaign 변수 선택](/help/email/campaign-variables.md) 대화 상자를 엽니다.
* **유형/크기** - 제목의 머리말 수준을 정의합니다.
* **링크** - 제목이 링크할 콘텐츠를 정의합니다. 콘텐츠 페이지, 외부 URL이나 페이지 앵커의 경로일 수 있습니다.
   * Campaign 아이콘을 클릭하여 Adobe Campaign의 다이내믹 콘텐츠를 삽입하기 위한 [Adobe Campaign 변수 선택](/help/email/campaign-variables.md) 대화 상자를 엽니다.
* **ID** - 이 옵션을 통해 HTML에서 구성 요소의 고유 식별자를 제어할 수 있습니다.
   * 비워 두면 고유 ID는 자동으로 생성되고 결과 페이지 검사를 통해 발견될 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID를 변경하면 CSS에 영향을 줄 수 있습니다.

![이메일 제목 구성 요소의 편집 대화 상자](/help/email/assets/email-title-edit.png)

바로 편집 기능을 가진 편집기를 사용하여 제목 구성 요소의 텍스트를 편집합니다.

![이메일 제목 구성 요소 바로 편집](/help/email/assets/email-title-edit-inline.png)

### 스타일 탭 {#styles-tab-edit}

이메일 제목 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

드롭다운을 사용하여 구성 요소에 적용할 스타일을 선택합니다. 편집 대화 상자에서 선택한 항목은 구성 요소 툴바에서 선택한 항목과 동일한 효과를 가집니다.

드롭다운 메뉴를 사용하려면 [디자인 대화 상자](#design-dialog)에서 이 구성 요소에 대한 스타일을 구성해야 합니다.

![제목 구성 요소의 디자인 대화 상자 스타일 탭](/help/email/assets/email-title-edit-styles.png)

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 통해 콘텐츠 작성자가 제목 구성 요소를 생성할 때 이에 포함될 기본 머리말 수준을 정의할 수 있습니다.

### 크기 탭 {#sizes-tab}

![제목 구성 요소의 디자인 대화 상자](/help/email/assets/email-title-design.png)

* **작성자에게 허용된 유형/크기** - 이메일 제목 구성 요소를 사용하는 경우 콘텐츠 작성자가 사용할 수 있는 머리말 유형을 활성화하거나 비활성화합니다.
* **기본 유형/크기** - 콘텐츠 작성자가 이메일 제목 구성 요소를 페이지에 추가할 때 자동으로 할당되는 머리말 유형을 정의합니다.
* **링크 비활성화** - 이메일 제목 구성 요소에서 링크 지원을 비활성화하면 콘텐츠 작성자는 제목에서 링크할 수 없습니다.

### 스타일 탭 {#styles-tab}

이메일 제목 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

---
title: 이메일 버튼 구성 요소
description: 이메일 버튼 구성 요소를 사용하여 콘텐츠의 버튼 항목을 구성하고 표시할 수 있습니다.
role: Architect, Developer, Admin, User
exl-id: b144e8d1-1097-475d-b2eb-3353c176afb9
source-git-commit: 91969e4956bef1a511b8d588d5290a7999bf86ec
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 100%

---


# 이메일 버튼 구성 요소 {#email-button-component}

이메일 버튼 구성 요소를 사용하여 콘텐츠의 버튼 항목을 구성하고 표시할 수 있습니다.

## 사용 {#usage}

이메일 버튼 구성 요소를 사용하면 콘텐츠 독자가 클릭 가능한 버튼을 콘텐츠에 포함하여 추가 리소스를 연결할 수 있습니다.

* [구성 대화 상자](#configure-dialog)에서 버튼의 속성을 선택할 수 있습니다.
* [디자인 대화 상자](#design-dialog)에서 이메일 버튼 구성 요소의 스타일을 정의할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

현재 버전의 이메일 버튼 구성 요소는 2022년 10월 이메일 핵심 구성 요소 릴리스 x과(와) 함께 도입된 v1입니다. 이 문서에서는 해당 구성 요소에 대해 설명합니다.

다음 테이블에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| v1 | 호환 가능 | - | - |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 문서 [이메일 핵심 구성 요소 버전](/help/email/versions.md)을 참조하십시오.

## 기술 세부 정보 {#technical-details}

이메일 버튼 구성 요소에 대한 최신 기술 설명서는 [GitHub에서 확인할 수 있습니다.](https://adobe.com/go/aem_cmp_tech_email_button_v1_kr)

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

콘텐츠 작성자는 구성 대화 상자를 통해 버튼 항목과 콘텐츠 독자를 위한 작동 및 표시 방법을 정의할 수 있습니다.

### 속성 탭 {#properties-tab}

![버튼 구성 요소의 디자인 대화 상자 속성 탭](/help/email/assets/email-button-edit-properties.png)

* **텍스트** - 버튼에 표시할 텍스트
   * Campaign 아이콘을 클릭하여 Adobe Campaign의 다이내믹 콘텐츠를 삽입하기 위한 [Adobe Campaign 변수 선택](/help/email/campaign-variables.md) 대화 상자를 엽니다.
* **링크** - AEM, 외부 소스 또는 앵커 내의 콘텐츠 페이지 링크
   * **선택 대화 상자**&#x200B;를 사용하여 AEM 내부 경로를 선택합니다.
   * Campaign 아이콘을 클릭하여 Adobe Campaign의 다이내믹 콘텐츠를 삽입하기 위한 [Adobe Campaign 변수 선택](/help/email/campaign-variables.md) 대화 상자를 엽니다.
* **아이콘** - 버튼에 아이콘을 표시하는 아이콘 식별자
* **ID** - 이 옵션을 통해 HTML에서 구성 요소의 고유 식별자를 제어할 수 있습니다.
   * 비워 두면 고유 ID는 자동으로 생성되고 결과 콘텐츠 검사를 통해 발견될 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID를 변경하면 CSS에 영향을 줄 수 있습니다.
* **새 탭에서 링크 열기** - 확인 표시가 되어 있는 경우 링크가 새 브라우저 탭에서 열립니다.

### 접근성 탭 {#accessibility-tab}

![버튼 구성 요소의 디자인 대화 상자 접근성 탭](/help/email/assets/email-button-edit-accessibility.png)

**접근성** 탭에서 구성 요소에 대한 [ARIA 접근성](https://www.w3.org/WAI/standards-guidelines/aria/) 라벨 값을 설정할 수 있습니다.

* **라벨** - 구성 요소에 대한 ARIA 라벨 속성 값

### 스타일 탭 {#styles-tab-edit}

이메일 버튼 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

드롭다운을 사용하여 구성 요소에 적용할 스타일을 선택합니다. 편집 대화 상자에서 선택한 항목은 구성 요소 툴바에서 선택한 항목과 동일한 효과를 가집니다.

탭을 사용하려면 [디자인 대화 상자](#design-dialog)에서 이 구성 요소에 대한 스타일을 구성해야 합니다.

## 디자인 대화 상자 {#design-dialog}

### 스타일 탭 {#styles-tab}

이메일 버튼 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

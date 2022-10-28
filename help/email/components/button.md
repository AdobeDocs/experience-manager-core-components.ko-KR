---
title: 이메일 단추 구성 요소
description: 이메일 단추 구성 요소를 사용하면 컨텐츠에 단추 항목을 구성하고 표시할 수 있습니다.
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: tm+mt
source-wordcount: '563'
ht-degree: 38%

---


# 이메일 단추 구성 요소 {#email-button-component}

이메일 단추 구성 요소를 사용하면 컨텐츠에 단추 항목을 구성하고 표시할 수 있습니다.

## 사용량 {#usage}

이메일 단추 구성 요소를 사용하면 컨텐츠 리더에서 클릭하여 추가 리소스에 연결하는 컨텐츠에 단추를 포함할 수 있습니다.

* 단추의 속성은 [구성 대화 상자.](#configure-dialog)
* 이메일 단추 구성 요소의 스타일은 [디자인 대화 상자](#design-dialog)

## 버전 및 호환성 {#version-and-compatibility}

이메일 단추 구성 요소의 현재 버전은 v1이며, 이 버전은 2022년 10월에 이메일 핵심 구성 요소의 릴리스 x에서 도입되었으며, 이 문서에 설명되어 있습니다.

다음 표에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 문서를 참조하십시오 [이메일 핵심 구성 요소 버전.](/help/email/versions.md)

## 샘플 구성 요소 출력 {#sample-component-output}

구성 옵션뿐만 아니라 HTML 및 JSON 출력에 대한 예를 보려면 이메일 단추 구성 요소 를 방문하십시오. [구성 요소 라이브러리.](https://adobe.com/go/aem_cmp_library_email_button)

## 기술 세부 사항 {#technical-details}

이메일 단추 구성 요소에 대한 최신 기술 문서입니다 [GitHub에서 찾을 수 있습니다.](https://adobe.com/go/aem_cmp_tech_email_button_v1)

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서입니다.](/help/developing/overview.md)

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자에서는 컨텐츠 작성자가 버튼을 정의하고 컨텐츠 리더에게 이 버튼을 어떻게 동작하고 나타나는지를 정의할 수 있습니다.

### 속성 탭 {#properties-tab}

![버튼 구성 요소의 디자인 대화 상자 속성 탭](/help/email/assets/email-button-edit-properties.png)

* **텍스트** - 버튼에 표시할 텍스트
   * Campaign 아이콘을 클릭하여 [Adobe Campaign 변수 선택](/help/email/campaign-variables.md) 대화 상자에서 Adobe Campaign의 동적 콘텐츠를 삽입할 수 있습니다.
* **링크** - AEM, 외부 소스 또는 앵커 내의 콘텐츠 페이지 링크
   * **선택 대화 상자**&#x200B;를 사용하여 AEM 내부 경로를 선택합니다.
   * Campaign 아이콘을 클릭하여 [Adobe Campaign 변수 선택](/help/email/campaign-variables.md) 대화 상자에서 Adobe Campaign의 동적 콘텐츠를 삽입할 수 있습니다.
* **아이콘** - 버튼에 아이콘을 표시하는 아이콘 식별자
* **ID** - 이 옵션을 사용하면 HTML에서 구성 요소의 고유 식별자를 제어할 수 있습니다.
   * 비워 두면 고유 ID가 자동으로 생성되며 결과 컨텐츠를 검사하여 찾을 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID를 변경하면 CSS에 영향을 줄 수 있습니다.
* **새 탭에서 링크 열기** - 확인 표시가 되어 있는 경우 링크가 새 브라우저 탭에서 열립니다.

### 접근성 탭 {#accessibility-tab}

![버튼 구성 요소의 디자인 대화 상자 접근성 탭](/help/email/assets/email-button-edit-accessibility.png)

**접근성** 탭에서 구성 요소에 대한 [ARIA 접근성](https://www.w3.org/WAI/standards-guidelines/aria/) 라벨 값을 설정할 수 있습니다.

* **라벨** - 구성 요소에 대한 ARIA 라벨 속성 값

### 스타일 탭 {#styles-tab-edit}

이메일 단추 구성 요소는 AEM을 지원합니다 [스타일 시스템.](/help/get-started/authoring.md#component-styling).

드롭다운을 사용하여 구성 요소에 적용할 스타일을 선택합니다. 편집 대화 상자에서 선택한 항목은 구성 요소 툴바에서 선택한 항목과 동일한 효과를 가집니다.

스타일을 [디자인 대화 상자](#design-dialog) 을 클릭하여 탭을 사용할 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

### 스타일 탭 {#styles-tab}

이메일 단추 구성 요소는 AEM을 지원합니다 [스타일 시스템](/help/get-started/authoring.md#component-styling).

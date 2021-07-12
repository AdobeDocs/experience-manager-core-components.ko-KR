---
title: 양식 숨김 구성 요소
description: 코어 구성 요소 양식 숨김 구성 요소로 숨김 필드를 표시할 수 있습니다.
role: Architect, Developer, Admin, User
exl-id: 0364cd3b-3c09-46db-9392-a67e3f9ea7a5
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 3%

---

# 양식 숨김 구성 요소{#form-hidden-component}

코어 구성 요소 양식 숨김 구성 요소로 숨김 필드를 표시할 수 있습니다.

## 사용량 {#usage}

코어 구성 요소 양식 숨김 구성 요소 를 사용하면 숨겨진 필드를 만들어 현재 페이지에 대한 정보를 다시 AEM에 전달할 수 있습니다. 이 필드는 [양식 컨테이너 구성 요소](form-container.md)와 함께 사용하기 위한 것입니다.

필드 속성은 [구성 대화 상자](form-hidden.md)에서 컨텐츠 편집기에서 정의할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

양식 숨김 구성 요소의 현재 버전은 v2이며, 2018년 1월에 핵심 구성 요소 릴리스 2.0.0에서 도입되었으며, 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전이 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | 호환 가능 | 호환 가능 | 호환 가능 |
| [v1](/help/components/v1/form-hidden-v1.md) | 호환 가능 | 호환 가능 | - |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

양식 숨김 구성 요소와 구성 옵션의 예 및 HTML 및 JSON 출력을 보려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_form_hidden)를 방문하십시오.

### 기술 세부 정보 {#technical-details}

양식 숨김 구성 요소 [에 대한 최신 기술 설명서는 GitHub](https://adobe.com/go/aem_cmp_tech_form_hidden_v2)에 있습니다.

코어 구성 요소 개발에 대한 자세한 내용은 [코어 구성 요소 개발자 설명서](/help/developing/overview.md)에서 확인할 수 있습니다.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자에서는 컨텐츠 작성자가 숨김 필드의 매개 변수를 정의할 수 있습니다.

![양식 숨김 편집 대화 상자](/help/assets/form-hidden-edit.png)

* **이름**  - 양식 데이터와 함께 제출되는 필드의 이름입니다
* **값**  - 양식 데이터와 함께 제출되는 필드의 값입니다
* **ID**  - 이 옵션을 사용하면 HTML과  [데이터 레이어에서 구성 요소의 고유 식별자를 제어할 수 있습니다](/help/developing/data-layer/overview.md).
   * 비워 두면 고유 ID가 자동으로 생성되며 결과 페이지를 검사하여 찾을 수 있습니다.
   * ID가 지정된 경우 ID가 고유한지 확인하는 것은 작성자의 책임입니다.
   * ID를 변경하면 CSS, JS 및 데이터 레이어 추적에 영향을 줄 수 있습니다.

양식 숨김 구성 요소에는 일반적으로 표시되는 속성이 없으므로 작성자가 적절한 양식 숨김 구성 요소를 식별하는 데 도움이 되도록 지정된 경우 편집기에 있는 구성 요소의 자리 표시자 **이름** 및 **값** 필드 값이 표시됩니다.

![숨겨진 구성 요소의 예](/help/assets/form-hidden-example.png)

## 디자인 대화 상자 {#design-dialog}

### 스타일 탭 {#styles-tab}

양식 숨김 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

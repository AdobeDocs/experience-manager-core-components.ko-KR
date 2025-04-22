---
title: 양식 버튼 구성 요소
description: 핵심 구성 요소의 양식 숨기기 구성 요소를 사용하여 양식에 숨겨진 필드를 포함할 수 있습니다.
role: Architect, Developer, Admin, User
exl-id: 1e5cff43-57db-4bfc-b2d2-23307eaf5eb3
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 99%

---

# 양식 버튼 구성 요소 {#form-button-component}

핵심 구성 요소의 양식 버튼 요소 다운로드를 사용하여 작업을 페이지에 트리거할 버튼을 포함할 수 있습니다.

## 사용량 {#usage}

핵심 구성 요소의 양식 버튼 구성 요소를 사용하여 버튼 필드를 생성하고, 종종 양식 제출을 트리거하고 [양식 컨테이너 구성 요소](form-container.md)와 함께 이 구성 요소를 사용할 수 있습니다.

콘텐츠 편집기는 [구성 대화 상자](#configure-dialog)에서 버튼의 속성을 정의할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

현재 버전의 양식 버튼 구성 요소는 2018년 1월 핵심 구성 요소 릴리스 2.0.0과 함께 도입된 v2입니다. 이 문서에서는 해당 구성 요소에 대해 설명합니다.

다음 테이블에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v2 | <br>[릴리스 2.17.4](/help/versions.md) 및 이전 버전과 호환 가능 | 호환 가능 | 야영용 | 호환 가능 |
| [v1](/help/components/v1/form-button-v1.md) | 호환 가능 | 호환 가능 | - | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md)을 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

양식 버튼 구성 요소를 경험하고 구성 옵션의 샘플뿐만 아니라 HTML 및 JSON 출력을 확인하려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_form_button_kr)를 참조하십시오.

### 기술 세부 사항 {#technical-details}

양식 버튼 구성 요소에 대한 최신 기술 설명서는 [GitHub에서 확인할 수 있습니다](https://adobe.com/go/aem_cmp_tech_form_button_v2_kr).

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

콘텐츠 작성자는 구성 대화 상자를 통해 버튼의 매개 변수를 정의할 수 있습니다.

### 속성 탭 {#properties-tab}

![양식 버튼 구성 요소의 편집 대화 상자](/help/assets/form-button-edit.png)

* **유형**

   * **버튼**
   * **제출**

* **제목** - 버튼에 표시된 텍스트

   * 제공되지 않은 경우 기본값은 버튼 유형으로 설정됩니다.

* **이름** - 양식 데이터로 제출된 버튼의 이름
* **값** - 양식 데이터로 제출된 버튼의 값

* **ID** - 이 옵션을 통해 HTML과 [데이터 레이어](/help/developing/data-layer/overview.md)에서 구성 요소의 고유 식별자를 제어할 수 있습니다.
   * 비워 두면 고유 ID는 자동으로 생성되고 결과 페이지 검사를 통해 발견될 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID가 변경되면 CSS, JS 및 데이터 레이어 추적에 영향을 미칠 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

### 스타일 탭 {#styles-tab}

양식 버튼 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

---
title: 양식 단추 구성 요소
description: 핵심 구성 요소 양식 숨김 구성 요소를 사용하면 숨김 필드를 양식에 포함할 수 있습니다.
translation-type: tm+mt
source-git-commit: 4813748bcfa83ce7c73e81d4e4d445ecc8215d26
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 4%

---


# 양식 단추 구성 요소 {#form-button-component}

핵심 구성 요소 양식 단추 구성 요소를 사용하면 단추를 포함하여 페이지에 동작을 트리거할 수 있습니다.

## 사용량 {#usage}

핵심 구성 요소 양식 단추 구성 요소를 사용하면 종종 양식 제출을 트리거하는 단추 필드를 만들 수 있으며 [양식 컨테이너 구성 요소와 함께 사용할 수 있습니다](form-container.md).

단추 속성은 [구성 대화 상자의 컨텐츠 편집기에서 정의할 수 있습니다](#configure-dialog).

## 버전 및 호환성 {#version-and-compatibility}

양식 단추 구성 요소의 현재 버전은 v2입니다. v2는 2018년 1월에 핵심 구성 요소 릴리스 2.0.0에서 도입되었으며 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전이 호환되는 AEM 버전 및 이전 버전의 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | 클라우드 서비스로서의 AEM |
|--- |--- |--- |---|
| v2 | 호환 가능 | 호환 가능 | 호환 가능 |
| [v1](/help/components/v1/form-button-v1.md) | 호환 가능 | 호환 가능 | - |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전을 참조하십시오](/help/versions.md).

## 샘플 구성 요소 출력 {#sample-component-output}

양식 단추 구성 요소뿐만 아니라 구성 옵션 예와 HTML 및 JSON 출력을 보려면 [구성 요소 라이브러리를 방문하십시오](https://adobe.com/go/aem_cmp_library_form_button).

### 기술 세부 정보 {#technical-details}

양식 단추 구성 요소에 대한 최신 기술 문서는 GitHub에서 [찾을 수 있습니다](https://adobe.com/go/aem_cmp_tech_form_button_v2).

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서를 참조하십시오](/help/developing/overview.md).

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자에서는 컨텐츠 작성자가 단추의 매개 변수를 정의할 수 있습니다.

### 속성 탭 {#properties-tab}

![양식 단추 구성 요소의 편집 대화 상자](/help/assets/form-button-edit.png)

* **유형**

   * **단추**
   * **전송**

* **제목** - 단추에 표시된 텍스트

   * 제공된 것이 없으면 기본적으로 단추 유형이 됩니다

* **이름** - 양식 데이터와 함께 제출하는 단추의 이름
* **값** - 양식 데이터와 함께 제출하는 단추의 값

* **ID** - 이 옵션을 사용하면 HTML과 [데이터 레이어에서 구성 요소의 고유 식별자를 제어할 수 있습니다](/help/developing/data-layer/overview.md).
   * 비워 두면 자동으로 고유 ID가 생성되어 결과 페이지를 검사하여 찾을 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID를 변경하면 CSS, JS 및 데이터 레이어 추적에 영향을 줄 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

### 스타일 탭 {#styles-tab}

양식 단추 구성 요소는 AEM [스타일 시스템을 지원합니다](/help/get-started/authoring.md#component-styling).

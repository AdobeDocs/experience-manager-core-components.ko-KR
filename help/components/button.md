---
title: 단추 구성 요소
description: 핵심 구성 요소 단추 구성 요소를 사용하면 단추를 만들고 표시할 수 있습니다.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 2%

---


# 단추 구성 요소{#button-component}

핵심 구성 요소 단추 구성 요소를 사용하면 페이지에 있는 단추 항목을 구성하고 표시할 수 있습니다.

## 사용량 {#usage}

핵심 구성 요소 단추 구성 요소를 사용하면 페이지에 단추를 포함할 수 있습니다.

* 구성 대화 상자에서 단추의 속성을 선택할 수 [있습니다](#configure-dialog).
* 단추 구성 요소의 스타일은 [디자인 대화 상자에서 정의할 수 있습니다](#design-dialog).

## 버전 및 호환성 {#version-and-compatibility}

단추 구성 요소의 현재 버전은 v1이며, 2019년 6월에 핵심 구성 요소의 릴리스 2.5.0에서 도입되었으며 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전이 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | 클라우드 서비스로서의 AEM |
|--- |--- |---|---|
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전을 참조하십시오](/help/versions.md).

## 샘플 구성 요소 출력 {#sample-component-output}

HTML 및 JSON 출력뿐만 아니라 단추 구성 요소의 구성 옵션 예를 보려면 [구성 요소 라이브러리를 방문하십시오](https://adobe.com/go/aem_cmp_library_button).

## 기술 세부 정보 {#technical-details}

단추 구성 요소에 대한 최신 기술 문서는 GitHub에서 확인할 [수 있습니다](https://adobe.com/go/aem_cmp_tech_button_v1).

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서를 참조하십시오](/help/developing/overview.md).

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자에서는 컨텐츠 작성자가 단추를 정의하고 페이지 방문자에 대해 단추 동작과 표시 방법을 정의할 수 있습니다.

### 속성 탭 {#properties-tab}

![단추 구성 요소의 편집 대화 상자의 속성 탭](/help/assets/button-edit-properties.png)

* **텍스트** - 단추에 표시할 텍스트
* **링크** - AEM 내의 컨텐츠 페이지, 외부 리소스 또는 앵커에 링크
   * 선택 대화 **상자를** 사용하여 AEM 내의 경로를 선택합니다.
* **아이콘** - 단추에 아이콘을 표시하는 식별자
* **ID** - 이 옵션을 사용하면 HTML과 [데이터 레이어에서 구성 요소의 고유 식별자를 제어할 수 있습니다](/help/developing/data-layer/overview.md).
   * 비워 두면 자동으로 고유 ID가 생성되어 결과 페이지를 검사하여 찾을 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID를 변경하면 CSS, JS 및 데이터 레이어 추적에 영향을 줄 수 있습니다.

### 접근성 탭 {#accessibility-tab}

![단추 구성 요소의 편집 대화 상자의 액세스 가능성 탭](/help/assets/button-edit-accessibility.png)

접근성 **탭** 에서 구성 요소의 [ARIA 액세서빌러티](https://www.w3.org/WAI/standards-guidelines/aria/) 레이블에 대한 값을 설정할 수 있습니다.

* **레이블** - 구성 요소에 대한 ARIA 레이블 속성의 값

## 디자인 대화 상자 {#design-dialog}

### 스타일 탭 {#styles-tab}

이미지 구성 요소는 AEM [스타일 시스템을 지원합니다](/help/get-started/authoring.md#component-styling).

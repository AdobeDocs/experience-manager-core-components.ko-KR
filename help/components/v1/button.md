---
title: 버튼 구성 요소 (v1)
description: 핵심 구성 요소의 버튼 구성 요소를 사용하여 버튼을 생성하고 표시할 수 있습니다.
role: Architect, Developer, Admin, User
exl-id: 63af16e4-dd4d-426d-88ef-769ecd1b3175
index: n
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: ht
source-wordcount: '397'
ht-degree: 100%

---


# 버튼 구성 요소 (v1) {#button-component}

핵심 구성 요소의 버튼 구성 요소를 사용하여 페이지에서 버튼 항목을 구성하고 표시할 수 있습니다.

## 사용량 {#usage}

핵심 구성 요소의 버튼 구성 요소를 사용하여 페이지에 버튼을 포함할 수 있습니다.

* [구성 대화 상자](#configure-dialog)에서 버튼의 속성을 선택할 수 있습니다.
* [디자인 대화 상자](#design-dialog)에서 버튼 구성 요소의 스타일을 정의할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

버튼 구성 요소는 2019년 6월 핵심 구성 요소 릴리스 2.5.0과 함께 도입된 v1입니다. 이 문서에서는 해당 구성 요소에 대해 설명합니다.

>[!CAUTION]
>
>이 문서에서는 버튼 구성 요소 v1에 대해 설명합니다.
>
>현재 버전의 버튼 구성 요소에 대한 자세한 내용은 [버튼 구성 요소](/help/components/button.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

버튼 구성 요소를 경험하고 구성 옵션의 샘플뿐만 아니라 HTML 및 JSON 출력을 확인하려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_button_kr)를 참조하십시오.

## 기술 세부 정보 {#technical-details}

버튼 구성 요소에 대한 최신 기술 설명서는 [GitHub에서 확인할 수 있습니다](https://adobe.com/go/aem_cmp_tech_button_v1_kr).

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

콘텐츠 작성자는 구성 대화 상자를 통해 버튼 항목과 방문자를 위한 페이지 작동 및 표시 방법을 정의할 수 있습니다.

### 속성 탭 {#properties-tab}

![버튼 구성 요소의 디자인 대화 상자 속성 탭](/help/assets/button-edit-properties.png)

* **텍스트** - 버튼에 표시할 텍스트
* **링크** - AEM, 외부 소스 또는 앵커 내의 콘텐츠 페이지 링크
   * **선택 대화 상자**&#x200B;를 사용하여 AEM 내부 경로를 선택합니다.
* **아이콘** - 버튼에 아이콘을 표시하는 아이콘 식별자
* **ID** - 이 옵션을 통해 HTML과 [데이터 레이어](/help/developing/data-layer/overview.md)에서 구성 요소의 고유 식별자를 제어할 수 있습니다.
   * 비워 두면 고유 ID는 자동으로 생성되고 결과 페이지 검사를 통해 발견될 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID가 변경되면 CSS, JS 및 데이터 레이어 추적에 영향을 미칠 수 있습니다.

### 접근성 탭 {#accessibility-tab}

![버튼 구성 요소의 디자인 대화 상자 접근성 탭](/help/assets/button-edit-accessibility.png)

**접근성** 탭에서 구성 요소에 대한 [ARIA 접근성](https://www.w3.org/WAI/standards-guidelines/aria/) 라벨 값을 설정할 수 있습니다.

* **라벨** - 구성 요소에 대한 ARIA 라벨 속성 값

## 디자인 대화 상자 {#design-dialog}

### 스타일 탭 {#styles-tab}

버튼 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

## Adobe 클라이언트 데이터 레이어 {#data-layer}

버튼 구성 요소는 [Adobe 클라이언트 데이터 레이어](/help/developing/data-layer/overview.md)를 지원합니다.

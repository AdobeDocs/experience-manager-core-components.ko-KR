---
title: 이동 경로 구성 요소 (v2)
description: 핵심 구성 요소의 이동 경로 구성 요소는 콘텐츠 계층 구조의 페이지 위치에 따라 링크의 이동 경로를 빌드하는 탐색 구성 요소입니다.
role: Architect, Developer, Admin, User
source-git-commit: f8aa86d58ba71ede3c3cd867c45aafff06923325
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 97%

---


# 이동 경로 구성 요소 (v2) {#breadcrumb-component}

핵심 구성 요소의 이동 경로 구성 요소는 콘텐츠 계층 구조의 페이지 위치에 따라 링크의 이동 경로를 빌드하는 탐색 구성 요소입니다.

## 사용량 {#usage}

이동 경로 구성 요소의 사이트 계층 구조 내부에 현재 페이지 위치가 표시되면 페이지 방문자는 현재 위치에서 페이지 계층 구조를 탐색할 수 있습니다. 이는 종종 페이지 머리글이나 바닥글에 통합됩니다.

템플릿 작성자는 [디자인 대화 상자](#design-dialog)에서 기본 탐색 수준과 현재 페이지 또는 숨겨진 페이지 표시하기 기능 등 사용 가능한 옵션을 정의할 수 있습니다. 그런 다음 콘텐츠 편집기는 숨겨진 페이지 표시 여부를 선택하고 [편집 대화 상자](#edit-dialog)에서 구성 요소의 실제 탐색 수준을 선택할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

이 문서에서는 2018년 1월에 핵심 구성 요소 릴리스 2.0.0과 함께 소개된 탐색 표시 구성 요소의 v2에 대해 설명합니다.

>[!CAUTION]
>
>이 문서에서는 이동 경로 구성 요소 v2에 대해 설명합니다.
>
>현재 버전의 이동 경로 구성 요소에 대한 자세한 내용은 [이동 경로 구성 요소](/help/components/breadcrumb.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

이동 경로 구성 요소를 경험하고 구성 옵션의 샘플뿐만 아니라 HTML 및 JSON 출력을 확인하려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_breadcrumb_kr)를 참조하십시오.

>[!NOTE]
>
>이동 경로 구성 요소 릴리스 2.1.0부터 탐색 구성 요소는 [schema.org microdata](https://schema.org/BreadcrumbList)를 지원합니다.

## 기술 세부 사항 {#technical-details}

이동 경로 구성 요소에 대한 최신 기술 설명서는[ GitHub에서 확인할 수 있습니다](https://adobe.com/go/aem_cmp_tech_breadcrumb_v2_kr).

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

## 편집 대화 상자 {#edit-dialog}

콘텐츠 작성자는 편집 대화 상자를 통해 이동 경로의 숨겨진 페이지 및 활성 페이지뿐만 아니라 표시할 계층 구조의 깊이를 표시하지 않을 수 있습니다.

![이동 경로 구성 요소의 편집 대화 상자](/help/assets/breadcrumb-edit.png)

* **탐색 시작 레벨** - 계층 구조에서 이동 경로 구성 요소가 현재 페이지로 하강하는 시작점. 예:

   * `/content`에서 0차 시작
   * `/content/<yourSite>`에서 1차 시작
   * `/content/<yourSite>/<country>`에서 2차 시작

* **탐색 항목 숨김 표시** - 숨김으로 표시된 이동 경로의 페이지를 표시함(기본적으로 표시되지 않음)
* **현재 페이지 숨김** - 이동 경로의 현재 페이지를 표시하지 않음(기본적으로 표시됨)
* **섀도잉 비활성화** - 계층 구조 내의 페이지가 리디렉션된 경우 대상이 아닌 리디렉션된 페이지 이름이 표시됩니다. 자세한 내용은 탐색 구성 요소의 [새도 사이트 구조 지원](../v1/navigation.md#shadow-structure)을 참조하십시오.
* **ID** - 이 옵션을 통해 HTML과 [데이터 레이어](/help/developing/data-layer/overview.md)에서 구성 요소의 고유 식별자를 제어할 수 있습니다.
   * 비워 두면 고유 ID는 자동으로 생성되고 결과 페이지 검사를 통해 발견될 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID가 변경되면 CSS, JS 및 데이터 레이어 추적에 영향을 미칠 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 통해 이동 경로의 숨겨진 페이지 및 활성 페이지뿐만 아니라 표시할 계층 구조의 깊이를 표시하지 않도록 옵션의 기본값을 정의할 수 있습니다.

### 메인 탭 {#main-tab}

![](/help/assets/breadcrumb-design.png)

* **탐색 시작 레벨** - 이동 경로 구성 요소가 페이지에 추가되면 계층 구조에서 이동 경로 구성 요소가 현재 페이지로 하강하는 시작점을 대한 기본값을 정의합니다.
* **탐색 항목 숨김 표시** - 이동 경로 구성 요소가 페이지에 추가되면 **숨김 표시** 옵션에 대한 기본값을 정의합니다.

   * 이로 인해 작성자의 옵션이 활성화되거나 비활성화되지 않습니다. 기본값만 설정됩니다.

* **현재 페이지 숨김** - 이동 경로 구성 요소가 페이지에 추가되면 **현재 숨김** 옵션에 대한 기본값을 정의합니다.

   * 이로 인해 작성자의 옵션이 활성화되거나 비활성화되지 않습니다. 기본값만 설정됩니다.

* **섀도잉 비활성화** - 이동 경로 구성 요소가 페이지에 추가되면 **섀도잉 비활성화** 옵션에 대한 기본값을 정의합니다.

### 스타일 탭 {#styles-tab}

이동 경로 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

## Adobe 클라이언트 데이터 레이어 {#data-layer}

이동 경로 구성 요소는 [Adobe 클라이언트 데이터 레이어](/help/developing/data-layer/overview.md)를 지원합니다.
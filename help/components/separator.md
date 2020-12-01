---
title: 분리자 구성 요소
description: 구분 문자 구성 요소는 페이지의 구성 요소 간에 나누기를 만듭니다
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 5%

---


# 분리자 구성 요소 {#separator-component}

핵심 구성 요소 구분 기호 구성 요소는 컨텐츠를 구분하기 위한 가로 규칙을 표시합니다.

## 사용량 {#usage}

구분 문자 구성 요소를 사용하면 컨텐츠 작성자는 페이지에서 정보를 보다 효율적으로 구성하기 위해 컨텐츠 간의 구분으로 가로 규칙을 쉽게 만들 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

현재 버전의 구분 구성 요소는 v1이며, 2019년 2월에 핵심 구성 요소의 릴리스 2.3.0에서 도입되었으며 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전이 호환되는 AEM 버전 및 이전 버전의 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |

## 샘플 구성 요소 출력 {#sample-component-output}

HTML 및 JSON 출력뿐만 아니라 구성 옵션의 예를 보려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_separator)를 방문하십시오.

### 기술 세부 정보 {#technical-details}

Separator 구성 요소 [에 대한 최신 기술 문서는 GitHub](https://adobe.com/go/aem_cmp_tech_separator_v1)에서 찾을 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)에서 확인할 수 있습니다.

## 구성 대화 상자 {#configure-dialog}

![분리 구성 요소의 편집 대화 상자](/help/assets/separator-edit.png)

* **ID**  - 이 옵션을 사용하면 HTML과  [데이터 레이어에서 구성 요소의 고유 식별자를 제어할 수 있습니다](/help/developing/data-layer/overview.md).
   * 비워 두면 자동으로 고유 ID가 생성되어 결과 페이지를 검사하여 찾을 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID를 변경하면 CSS, JS 및 데이터 레이어 추적에 영향을 줄 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 사용하여 구분 문자 구성 요소에 적용된 스타일을 정의할 수 있습니다.

### 스타일 탭 {#styles-tab}

구분 문자 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

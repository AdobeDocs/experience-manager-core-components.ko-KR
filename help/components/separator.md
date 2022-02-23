---
title: 분리자 구성 요소
description: 분리자 구성 요소는 페이지에서 구성 요소를 일시 중단할 수 있습니다.
role: Architect, Developer, Admin, User
exl-id: 79f19368-67fa-4864-93f7-2aa801d13fdb
source-git-commit: 9767a3a10cb9a77f385edc0ac3fb00096c0087af
workflow-type: ht
source-wordcount: '308'
ht-degree: 100%

---

# 분리자 구성 요소 {#separator-component}

핵심 구성 요소의 분리자 구성 요소에는 콘텐츠 분리에 대한 가로 규칙이 표시됩니다.

## 사용량 {#usage}

효율적인 페이지 정보 구성을 위해 콘텐츠 작성자는 분리자 구성 요소를 통해 간단한 가로 규칙을 제작하여 콘텐츠를 일시 중단할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

현재 버전의 분리자 구성 요소는 2018년 2월 핵심 구성 요소 릴리스 2.3.0과 함께 도입된 v1입니다. 이 문서에서는 해당 구성 요소에 대해 설명합니다.

다음 표에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v1 | 호환 가능 <br>[2.17.4](/help/versions.md) 및 이전 릴리스 | 호환 가능 | 호환 가능 |

## 샘플 구성 요소 출력 {#sample-component-output}

분리자 구성 요소를 경험하고 구성 옵션의 샘플뿐만 아니라 HTML 및 JSON 출력을 확인하려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_separator_kr)를 참조하십시오.

### 기술 세부 사항 {#technical-details}

분리자 구성 요소에 대한 최신 기술 설명서는[ GitHub에서 확인할 수 있습니다](https://adobe.com/go/aem_cmp_tech_separator_v1_kr).

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

![분리자 구성 요소의 편집 대화 상자](/help/assets/separator-edit.png)

* **ID** - 이 옵션을 통해 HTML과 [데이터 레이어](/help/developing/data-layer/overview.md)에서 구성 요소의 고유 식별자를 제어할 수 있습니다.
   * 비워 두면 고유 ID는 자동으로 생성되고 결과 페이지 검사를 통해 발견될 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID가 변경되면 CSS, JS 및 데이터 레이어 추적에 영향을 미칠 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 통해 분리자 구성 요소에 적용되는 스타일을 정의할 수 있습니다.

### 스타일 탭 {#styles-tab}

분리자 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

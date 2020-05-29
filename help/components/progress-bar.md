---
title: 진행률 표시줄 구성 요소
description: 진행률 표시줄 구성 요소는 목표를 향해 진행 상태를 시각적으로 나타냅니다
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 3%

---


# 진행률 표시줄 구성 요소 {#progress-bar-component}

핵심 구성 요소 진행률 막대 구성 요소는 목표를 향한 진행 상태를 시각적으로 나타냅니다.

## 사용량 {#usage}

진행률 표시줄 구성 요소를 사용하면 컨텐츠 작성자는 완료 비율을 정의하여 진행률 표시줄을 손쉽게 만들 수 있으므로 목표를 향해 진행 상황을 직관적으로 시각적으로 표시할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

진행률 표시줄 구성 요소의 현재 버전은 v1이며, 2020년 5월 핵심 구성 요소의 릴리스 2.9.0에서 도입되었으며 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전이 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | 클라우드 서비스로서의 AEM |
|---|---|---|---|
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |

## 샘플 구성 요소 출력 {#sample-component-output}

HTML 및 JSON 출력뿐만 아니라 구성 옵션의 예를 보려면 [구성 요소 라이브러리를 방문하십시오](https://adobe.com/go/aem_cmp_library_progress).

### 기술 세부 정보 {#technical-details}

진행률 표시줄 구성 요소에 대한 최신 기술 문서는 GitHub에서 [찾을 수 있습니다](https://adobe.com/go/aem_cmp_tech_progress_v1).

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서를 참조하십시오](/help/developing/overview.md).

## 구성 대화 상자 {#configure-dialog}

![진행률 표시줄 구성 요소의 편집 대화 상자](/help/assets/progress-bar-edit.png)

* **완료** - 백분율로 표시되는 진행률
* **ID** - 이 옵션을 사용하면 HTML과 [데이터 레이어에서 구성 요소의 고유 식별자를 제어할 수 있습니다](/help/developing/data-layer/overview.md).
   * 비워 두면 자동으로 고유 ID가 생성되어 결과 페이지를 검사하여 찾을 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID를 변경하면 CSS, JS 및 데이터 레이어 추적에 영향을 줄 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 사용하여 진행률 표시줄 구성 요소에 적용된 스타일을 정의할 수 있습니다.

### 스타일 탭 {#styles-tab}

진행률 표시줄 구성 요소는 AEM [스타일 시스템을 지원합니다](/help/get-started/authoring.md#component-styling).
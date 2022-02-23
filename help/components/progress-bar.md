---
title: 진행률 표시줄 구성 요소
description: 진행률 표시줄 구성 요소는 목표에 대한 진행률을 시각적으로 표시합니다.
role: Architect, Developer, Admin, User
exl-id: 47afc5a6-ac57-4b6c-92c4-015ca956a20b
source-git-commit: 9767a3a10cb9a77f385edc0ac3fb00096c0087af
workflow-type: ht
source-wordcount: '342'
ht-degree: 100%

---

# 진행률 표시줄 구성 요소 {#progress-bar-component}

핵심 구성 요소의 진행률 표시줄 구성 요소는 목표에 대한 진행률을 시각적으로 표시합니다.

## 사용량 {#usage}

콘텐츠 작성자는 진행률 표시줄 구성 요소를 통해 완료 시 백분율을 정의하여 진행률 표시줄을 쉽게 만들 수 있습니다. 이로써 목표에 대한 진행률을 직관적이고 시각적으로 표시할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

현재 버전의 진행률 표시줄 구성 요소는 2020년 5월 핵심 구성 요소 릴리스 2.9.0과 함께 도입된 v1입니다. 이 문서에서는 해당 구성 요소에 대해 설명합니다.

다음 표에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v1 | 호환 가능 <br>[2.17.4](/help/versions.md) 및 이전 릴리스 | 호환 가능 | 호환 가능 |

## 샘플 구성 요소 출력 {#sample-component-output}

진행률 표시줄 구성 요소를 경험하고 구성 옵션의 샘플뿐만 아니라 HTML 및 JSON 출력을 확인하려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_progressbar_kr)를 참조하십시오.

### 기술 세부 사항 {#technical-details}

진행률 표시줄 구성 요소에 대한 최신 기술 설명서는[ GitHub에서 확인할 수 있습니다](https://adobe.com/go/aem_cmp_tech_progress_v1_kr).

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

![진행률 표시줄 구성 요소의 편집 대화 상자](/help/assets/progress-bar-edit.png)

* **완료** - 진행률은 백분율로 표시됩니다.
* **ID** - 이 옵션을 통해 HTML과 [데이터 레이어](/help/developing/data-layer/overview.md)에서 구성 요소의 고유 식별자를 제어할 수 있습니다.
   * 비워 두면 고유 ID는 자동으로 생성되고 결과 페이지 검사를 통해 발견될 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID가 변경되면 CSS, JS 및 데이터 레이어 추적에 영향을 미칠 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 통해 진행률 표시줄 구성 요소에 적용되는 스타일을 정의할 수 있습니다.

### 스타일 탭 {#styles-tab}

진행률 표시줄 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

## Adobe 클라이언트 데이터 레이어 {#data-layer}

진행률 표시줄 구성 요소는 [ Adobe 클라이언트 데이터 레이어](/help/developing/data-layer/overview.md)지원합니다.

---
title: 컨텐츠 AI 검색 구성 요소
description: 콘텐츠 AI 검색 구성 요소는 사이트 방문자에게 생성 AI 기반 검색을 제공합니다.
role: Developer, Admin, User
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: e721e8b9469646300432b87d42bfb742aaf5f3fb
workflow-type: tm+mt
source-wordcount: 805
ht-degree: 16%

---


# 컨텐츠 AI 검색 구성 요소 {#content-ai-search-component}

콘텐츠 AI 검색 구성 요소는 사이트 방문자에게 생성 AI 기반 검색을 제공합니다.

{{traditional-aem}}

## 사용량 {#usage}

콘텐츠 AI 검색 구성 요소를 통해 방문자는 페이지에서 직접 [콘텐츠 Source](https://experienceleague.adobe.com/ko/docs/experience-manager-content-ai/using/contentsources)을(를) 검색하고 선택적으로 AI가 생성한 결과 요약을 볼 수 있습니다. 표준 전체 텍스트/의미 체계 검색 상자와 AEM Content AI에서 제공하는 전환 가능한 **AI 생성 요약 표시** 패널을 결합합니다.

콘텐츠 작성자는 [편집 대화 상자](#edit-dialog)를 통해 검색, 검색 동작 및 생성 설정의 콘텐츠 범위를 정의할 수 있습니다. 템플릿 수준에서 사용할 수 있는 설정이 없으므로 디자인 대화 상자가 없습니다.

>[!NOTE]
>
>콘텐츠 AI 검색 구성 요소를 사용하려면 콘텐츠 AI Source에 대한 액세스 권한이 있어야 하며 관리자가 프로젝트에 대해 구성 요소를 활성화해야 합니다. 자세한 내용은 [콘텐츠 AI 검색 구성 요소 구성](/help/developing/ai-search.md) 문서를 참조하십시오.

## 버전 및 호환성 {#version-and-compatibility}

현재 버전의 콘텐츠 AI 검색 구성 요소는 2026년 7월 핵심 구성 요소 릴리스 2.32.0과 함께 도입된 v1입니다. 이 문서에서는 해당 구성 요소에 대해 설명합니다.

다음 테이블에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|---|
| v1 | - | - | - | 진행 중 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 문서 [핵심 구성 요소 버전](/help/versions.md)을 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

콘텐츠 AI 검색 구성 요소를 경험하고 구성 옵션의 샘플뿐만 아니라 HTML 및 JSON 출력을 확인하려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_ai_search)를 참조하십시오.

## 기술 세부 정보 {#technical-details}

콘텐츠 AI 검색 구성 요소 [에 대한 최신 기술 설명서는 GitHub에서 확인할 수 있습니다.](https://adobe.com/go/aem_cmp_tech_ai_search_v1)

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

## 편집 대화 상자 {#edit-dialog}

콘텐츠 작성자는 편집 대화 상자를 통해 검색, 검색 비헤이비어 및 생성 설정의 콘텐츠 범위를 정의할 수 있습니다. 템플릿 수준에서 사용할 수 있는 설정이 없으므로 디자인 대화 상자가 없습니다.

### 콘텐츠 범위 탭 {#content-scope}

![편집 대화 상자의 콘텐츠 범위 탭](/help/assets/content-ai-search-edit-content-scope.png)

* **ID** - 이 옵션을 사용하면 HTML 및 [데이터 계층에서 구성 요소의 고유 식별자를 제어할 수 있습니다.](/help/developing/data-layer/overview.md)
  * 비워 두면 고유 ID는 자동으로 생성되고 결과 페이지 검사를 통해 발견될 수 있습니다.
  * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
  * ID가 변경되면 CSS, JS 및 데이터 레이어 추적에 영향을 미칠 수 있습니다.
* **컨텐츠 Source 유형** - 이 필드는 컨텐츠 소스의 유형을 정의합니다. 유형을 선택하면 **컨텐츠 Source** 드롭다운이 일치하는 소스로 채워집니다.
  * **ACQUISITION** - 크롤링/acquisition 파이프라인을 통해 인덱싱된 공개 익명 액세스 소스에 사용되는 기본값
  * **AEM_AUTHOR** - AEM 작성자 인스턴스에서 콘텐츠를 수집한 Content-AI 측 소스
  * **AEM_PUBLISH** - AEM 게시 인스턴스에서 콘텐츠가 수집된 Content-AI 측 소스
  * **CUSTOM** - AEM 자체 수집 파이프라인 외부에 등록된 소스
* **콘텐츠 원본** - 이 구성 요소가 검색하는 콘텐츠 Source을 정의합니다.
  * 사용 가능한 항목은 이미 존재하고 **사용 가능**&#x200B;이며 **컨텐츠 Source 유형**&#x200B;에 설정된 유형과 일치하는 컨텐츠 소스와 일치합니다.
  * 자세한 내용은 [콘텐츠 AI 소스 설정 및 관리](https://experienceleague.adobe.com/ko/docs/experience-manager-content-ai/using/contentsources) 문서를 참조하십시오.

### 검색 비헤이비어 탭 {#search-behavior}

![편집 대화 상자의 검색 동작 탭](/help/assets/content-ai-search-edit-search-behavior.png)

* **결과 레이아웃** - 이 옵션은 방문자에게 검색 결과가 표시되는 방법을 정의합니다.
  * **카드** - 이 옵션은 격자 형식으로 결과를 표시합니다.
  * **목록** - 이 옵션은 결과를 목록 형식으로 표시합니다.
* **결과 크기** - 검색 요청당 가져온 결과 수를 정의합니다.
  * 기본값은 `12`입니다.
  * 추가 일치 항목이 있는 경우 방문자가 더 많은 결과를 로드할 수 있습니다.
* **자리 표시자 텍스트** - 방문자가 검색 쿼리를 입력하기 전에 빈 검색 입력 필드에 표시되는 텍스트입니다.

### 생성 검색 탭 {#generative-search}

편집 대화 상자의 ![생성 검색 탭](/help/assets/content-ai-search-edit-generative-search.png)

* **방문자에 대한 생성 요약 표시** - 선택하지 않으면 방문자가 AI 요약의 표시 여부를 변경할 수 없습니다.
  * 기본값은 활성화되어 있습니다.
* **기본적으로 생성 요약 표시** - 이 옵션은 AI 생성 요약에 대한 방문자 표시 토글 기본 상태를 제어합니다.
  * 기본값은 활성화되어 있습니다.
* **GenSearch 오류 대체** - 검색 동작 또는 오류 방식을 정의합니다.
  * **결과 전용(오류 숨기기)** - 오류가 있는 경우 오류 및 다시 시도 단추가 아닌 반환된 결과만 표시합니다. 이 값은 기본값입니다.
  * **다시 시도할 때 오류 표시** - 오류가 있으면 다시 시도 단추로 오류를 표시합니다.
  * **오류 메시지만 표시** - 오류가 있으면 오류 메시지만 표시하고 결과는 표시하지 않습니다.

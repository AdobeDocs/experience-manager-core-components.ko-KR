---
title: 페이지 구성 요소
description: 페이지 구성 요소는 템플릿 편집기로 작업하고 페이지 머리글/바닥글 및 구조 구성 요소를 템플릿 편집기로 조합하도록 설계된 확장 가능한 페이지 구성 요소입니다.
translation-type: tm+mt
source-git-commit: f4a45b2af87e5a5f0396b335c65856ce821455c9
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 3%

---


# 페이지 구성 요소{#page-component}

페이지 구성 요소는 [템플릿 편집기](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)와 함께 작동하도록 설계된 확장 가능한 페이지 구성 요소로서, 페이지 머리글/바닥글 및 구조 구성 요소를 템플릿 편집기로 조합할 수 있도록 합니다.

## 사용량 {#usage}

페이지 구성 요소는 편집 가능한 템플릿뿐만 아니라 핵심 구성 요소로 디자인된 모든 페이지의 기반을 형성합니다. 페이지 구성 요소를 사용하여 머리글, 바닥글 및 페이지 구조를 다른 핵심 구성 요소를 사용하여 템플릿으로 정의할 수 있습니다.

[디자인 대화 상자](#design-dialog)를 사용하여 페이지에 대한 사용자 정의 클라이언트측 라이브러리를 정의할 수 있습니다. 페이지 구성 요소는 페이지 자체이므로 구성 요소에서 직접 액세스할 수 있는 편집 대화 상자가 있는 다른 구성 요소와 달리 페이지 구성 요소의 [편집 대화 상자](#edit-dialog)는 페이지 속성 창입니다.

## 점진적 웹 앱 지원 {#pwa-support}

핵심 구성 요소의 릴리스 2.15.0은 Cloud Service의 내장된 점진적 웹 앱(PWA) 기능으로 AEM에 대한 지원을 도입했습니다. 사이트 수준에서 간단한 구성을 통해 AEM 경험을 PWA으로 전환하십시오!

## 버전 및 호환성 {#version-and-compatibility}

페이지 구성 요소의 현재 버전은 v2이며, 2018년 1월에 핵심 구성 요소 릴리스 2.0.0에 도입되었으며 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소 버전이 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v2 | 호환 가능 | 호환 가능 | 호환 가능 |
| [v1](v1/page-v1.md) | 호환 가능 | 호환 가능 | - |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md) 문서를 참조하십시오.

### 기술 세부 정보 {#technical-details}

페이지 구성 요소 [에 대한 최신 기술 문서는 GitHub](https://adobe.com/go/aem_cmp_tech_page_v2)에서 찾을 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)에서 확인할 수 있습니다.

## 편집 대화 상자 {#edit-dialog}

구성 요소는 전체 페이지를 나타내므로, 일반적으로 편집 대화 상자에 있는 설정은 [페이지 속성](https://docs.adobe.com/content/help/ko-KR/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html) 창에 있습니다.

## 디자인 대화 상자 {#design-dialog}

구성 요소는 전체 페이지를 나타내므로 페이지 템플릿을 편집할 때 **페이지 정보 -> 페이지 정책**&#x200B;을 통해 디자인 대화 상자에 액세스합니다.

![페이지 정책](/help/assets/page-policy.png)

>[!NOTE]
>
>이전 버전의 AEM에서는 **페이지 정책**&#x200B;을 **페이지 디자인**&#x200B;이라고 불렀습니다.

### 속성 탭 {#properties-tab}

페이지 디자인 창에서 로드할 클라이언트 라이브러리와 페이지의 웹 리소스 라이브러리를 정의할 수 있습니다.

* **클라이언트 라이브러리**  - 로드할 클라이언트 라이브러리 범주를 정의합니다. JavaScript는 본문 끝에 추가되고 CSS가 페이지 헤드에 추가됩니다.
* **클라이언트 라이브러리 JavaScript 페이지**  헤드 - 페이지 헤드에 로드할 JavaScript 클라이언트 라이브러리 범주를 정의합니다.
   * 여기에 정의된 카테고리는 **클라이언트 라이브러리** 필드에도 있으며 본문 끝이 아니라 페이지 헤드에 JavaScript가 로드됩니다.
   * 카테고리가 **클라이언트 라이브러리** 필드에도 없는 경우 CSS가 로드되지 않습니다.

* **웹 리소스 클라이언트 라이브러리**  - 파비콘 등의 웹 리소스를 제공하는 데 사용되는 클라이언트 라이브러리 카테고리입니다.

* **기본 컨텐츠 요소 선택기로**  건너뛰기 - 액세서빌러티 기능으로 사용하여 페이지의 기본 컨텐츠로 바로 건너뛸 수 있습니다.

![페이지 구성 요소 디자인 대화 상자](/help/assets/page-design.png)

라이브러리는 다음과 같이 **클라이언트 라이브러리** 및 **클라이언트 라이브러리 JavaScript 페이지 헤드** 필드에 모두 구성할 수 있습니다.

* 새 필드를 추가하려면 필드 아래에 있는 **추가** 단추를 클릭하거나 탭합니다.
* 필드를 제거하려면 제거할 필드 옆에 있는 휴지통 아이콘을 클릭하거나 탭합니다.
* 로드 순서를 재정렬하려면 이동할 필드 옆에 있는 핸들을 클릭하거나 탭하고 드래그합니다.

클라이언트측 라이브러리 사용에 대한 자세한 내용은 [클라이언트측 라이브러리 사용](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/clientlibs.html)을 참조하십시오.

>[!CAUTION]
>
>페이지 헤드에 대한 클라이언트 라이브러리를 별도로 정의하는 기능은 핵심 구성 요소 릴리스 2.2.0과 함께 도입되었습니다.

### 스타일 탭 {#styles-tab}

페이지 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

## Adobe 클라이언트 데이터 레이어 {#data-layer}

페이지 구성 요소는 [Adobe 클라이언트 데이터 레이어를 지원합니다.](/help/developing/data-layer/overview.md)

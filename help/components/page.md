---
title: 페이지 구성 요소
description: 페이지 구성 요소는 템플릿 편집기로 작업하고, 페이지 머리글과 바닥글 및 구조 구성 요소를 조합할 수 있는 확장 가능한 페이지 구성 요소입니다.
role: Architect, Developer, Admin, User
exl-id: 2503e067-abed-427d-8a54-8b79e3451487
source-git-commit: 327c239b02e0aecee878784c918bfa98d960530e
workflow-type: ht
source-wordcount: '716'
ht-degree: 100%

---

# 페이지 구성 요소{#page-component}

페이지 구성 요소는 [템플릿 편집기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html)로 작업하고, 페이지 머리글과 바닥글 및 구조 구성 요소를 조합할 수 있는 확장 가능한 페이지 구성 요소입니다.

## 사용량 {#usage}

페이지 구성 요소는 핵심 구성 요소와 편집 가능한 템플릿으로 디자인된 모든 페이지의 기초 구성 요소입니다. 페이지 구성 요소를 사용하여 머리말, 바닥글과 페이지 구조를 다른 핵심 구성 요소를 사용하는 템플릿으로 정의할 수 있습니다.

[디자인 대화 상자](#design-dialog)를 사용하여 페이지에 대한 맞춤형 클라이언트측 라이브러리를 정의할 수 있습니다. 구성 요소에서 바로 편집 대화 상자에 액세스할 수 있는 기타 구성 요소와 다르게, 페이지 구성 요소는 페이지 자체이므로 페이지 구성 요소의 [편집 대화 상자](#edit-dialog)가 페이지 속성 창입니다.

## 버전 및 호환성 {#version-and-compatibility}

현재 버전의 페이지 구성 요소는 2022년 2월 핵심 구성 요소 릴리스 2.18.0과 함께 도입된 v3입니다. 이 문서에서는 해당 구성 요소에 대해 설명합니다.

다음 표에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v3 | - | 호환 가능 | 호환 가능 |
| [v2](v2/page.md) | 호환 가능 | 호환 가능 | 호환 가능 |
| [v1](v1/page-v1.md) | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md)을 참조하십시오.

## 점진적 웹 앱 지원 {#pwa-support}

핵심 구성 요소의 릴리스 2.15.0에서는 AEM as a Cloud Service 빌트인 [점진적 웹 앱(PWA) 기능에 대한 지원을 도입했습니다.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/enable-pwa.html) 사이트 수준의 간단한 구성을 통해 AEM 경험을 PWA로 전환할 수 있습니다.

### 기술 세부 사항 {#technical-details}

페이지 구성 요소에 대한 최신 기술 설명서는[ GitHub에서 확인할 수 있습니다](https://adobe.com/go/aem_cmp_tech_page_v3).

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

## 편집 대화 상자 {#edit-dialog}

구성 요소는 전체 이미지를 보여 주기 때문에 일반적으로 편집 대화 상자에 포함된 설정은 [페이지 속성](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html)에서 찾을 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

구성 요소는 전체 이미지를 보여 주기 때문에 페이지 템플릿 편집 시 디자인 편집 상자는 **페이지 정보 -> 페이지 정책**&#x200B;을 통해 액세스할 수 있습니다.

![페이지 정책](/help/assets/page-policy.png)

>[!NOTE]
>
>이전 버전의 AEM에서 **페이지 정책**&#x200B;은 **페이지 디자인**&#x200B;입니다.

### 속성 탭 {#properties-tab}

페이지 디자인 창을 사용하여 페이지에 로드할 클라이언트 라이브러리와 웹 리소스를 정의할 수 있습니다.

* **클라이언트 라이브러리** - 로드할 클라이언트 라이브러리 범주를 정의합니다. JavaScript는 본문 끝에 추가하고 CSS는 페이지 헤드에 추가합니다.
* **클라이언트 라이브러리 JavaScript 페이지 헤드** - 페이지 헤드에 로드할 클라이언트 라이브러리 범주를 정의합니다.
   * 또한 **클라이언트 라이브러리** 필드에 존재하는 범주를 정의하게 되면 본문 끝이 아닌 페이지 헤드에 JavaScript를 로드할 수 있습니다.
   * 또한 범주가 **클라이언트 라이브러리** 필드에 존재하지 않으면 CSS를 로드할 수 없습니다.

* **웹 리소스 클라이언트 라이브러리** - favicons와 같은 웹 리소스를 제공하는 데 사용되는 클라이언트 라이브러리 범주

* **메인 콘텐츠 요소 선택기로 건너뛰기** - 페이지의 메인 콘텐츠로 바로 건너뛸 수 있는 접근성 기능으로 사용

* **대체 언어 링크 렌더링** - 활성화된 경우 동일한 사이트에 있는 페이지의 대체 언어 버전에 대한 링크가 페이지 헤드에 추가됩니다.

![페이지 구성 요소의 디자인 대화 상자](/help/assets/page-design.png)

**클라이언트 라이브러리**&#x200B;와 **클라이언트 라이브러리 JavaScript 페이지 헤드** 필드 모두에 라이브러리를 구성될 수 있습니다.

* 새 필드를 추가하려면 필드 아래의 **추가** 버튼을 클릭하거나 탭합니다.
* 필드를 제거하려면 필드 옆 휴지통 아이콘을 클릭하거나 탭하여 제거합니다
* 로드 순서를 재배열하려면 필드 옆 핸들을 클릭하거나 탭하고 드래그하여 이동합니다.

client-side 라이브러리 사용에 대한 자세한 내용은 [클라이언트측 라이브러리 사용](https://helpx.adobe.com/kr/experience-manager/6-5/sites/developing/using/clientlibs.html)을 참조하십시오.

>[!CAUTION]
>
>핵심 구성 요소 릴리스 2.2.0과 함께 페이지 헤드용 클라이언트 라이브러리를 별도로 정의하는 기능이 도입되었습니다.

### 스타일 탭 {#styles-tab}

페이지 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

## Adobe 클라이언트 데이터 레이어 {#data-layer}

페이지 구성 요소는 [ Adobe 클라이언트 데이터 레이어](/help/developing/data-layer/overview.md)지원합니다.

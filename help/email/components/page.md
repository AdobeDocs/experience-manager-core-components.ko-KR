---
title: 이메일 페이지 구성 요소
description: 이메일 페이지 구성 요소
role: Architect, Developer, Admin, User
exl-id: 17fd0f5e-2b85-41a1-abaf-8ad190a5341a
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 99%

---


# 이메일 페이지 구성 요소 {#email-page-component}

이메일 페이지 구성 요소는 [템플릿 편집기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=ko-KR)로 작업하고, 페이지 머리글과 바닥글 및 구조 구성 요소를 조합하여 Adobe Campaign 콘텐츠를 맞춤형으로 만들 수 있는 확장 가능한 페이지 구성 요소입니다.

## 사용 {#usage}

이메일 페이지 구성 요소는 이메일 핵심 구성 요소와 편집 가능한 템플릿으로 디자인된 모든 페이지의 기초 구성 요소입니다. 이메일 페이지 구성 요소를 사용하여 머리말, 바닥글과 페이지 구조를 다른 이메일 핵심 구성 요소를 사용하는 템플릿으로 정의할 수 있습니다.

* [디자인 대화 상자](#design-dialog)를 사용하여 페이지에 대한 사용자 정의 클라이언트측 라이브러리를 정의할 수 있습니다.
* 구성 요소에서 바로 편집 대화 상자에 액세스할 수 있는 기타 구성 요소와 다르게, 이메일 페이지 구성 요소는 페이지 자체이므로 이메일 페이지 구성 요소의 [편집 대화 상자](#edit-dialog)가 페이지 속성 창입니다.

## 버전 및 호환성 {#version-and-compatibility}

현재 버전의 이메일 페이지 구성 요소는 2022년 10월 이메일 핵심 구성 요소 릴리스 X과(와) 함께 도입된 v1입니다. 이 문서에서는 해당 구성 요소에 대해 설명합니다.

다음 테이블에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| v1 | 호환 가능 | 호환 가능 | - |

이메일 핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 문서 [이메일 핵심 구성 요소 버전](/help/email/versions.md)을 참조하십시오.

### 기술 세부 사항 {#technical-details}

페이지 구성 요소에 대한 최신 기술 설명서는 [GitHub에서 확인할 수 있습니다.](https://adobe.com/go/aem_cmp_tech_email_page_v1_kr)

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

## 편집 대화 상자 {#edit-dialog}

구성 요소는 전체 이미지를 보여 주기 때문에 일반적으로 편집 대화 상자에 포함된 설정은 [페이지 속성](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html)에서 찾을 수 있습니다.

### 클라우드 서비스 탭 {#cloud-services}

이메일 핵심 구성 요소에서 캠페인 변수 및 데이터를 검색할 수 있으려면 페이지가 Adobe Campaign 구성에 연결되어 있어야 합니다.

![이메일 페이지 속성](/help/email/assets/email-page-properties.png)

**클라우드 서비스 구성** 제목 아래의 드롭다운에서 **구성 추가**&#x200B;를 선택합니다.

**Adobe Campaign** 제목 아래에서 Adobe Campaign과의 통합을 위한 구성을 선택합니다.

이메일 핵심 구성 요소 설정에 대한 자세한 내용은 문서 [이메일 핵심 구성 요소 사용](/help/email/using.md)을 참조하십시오.

### 이메일 탭 {#email-tab}

이메일 탭은 이메일 제목 및 일반 텍스트 콘텐츠와 같은 이 페이지의 콘텐츠를 기반으로 Adobe Campaign을 통해 전송되는 이메일의 속성을 정의합니다.

![이메일 페이지 속성](/help/email/assets/email-page-properties-email.png)

* **제목** - 이 페이지를 기반으로 Adobe Campaign에서 전송하는 이메일의 제목
   * **Adobe Campaign 변수 선택** 아이콘을 클릭하여 Adobe Campaign의 다이내믹 콘텐츠를 삽입하기 위한 [Adobe Campaign 변수 선택](/help/email/campaign-variables.md) 대화 상자를 엽니다.
* **사전 머리글**
   * **Adobe Campaign 변수 선택** 아이콘을 클릭하여 Adobe Campaign의 다이내믹 콘텐츠를 삽입하기 위한 [Adobe Campaign 변수 선택](/help/email/campaign-variables.md) 대화 상자를 엽니다.
* **일반 텍스트** - Adobe Campaign에서 전송하는 이메일의 일반 텍스트 버전
   * **Adobe Campaign 변수 선택** 아이콘을 클릭하여 Adobe Campaign의 다이내믹 콘텐츠를 삽입하기 위한 [Adobe Campaign 변수 선택](/help/email/campaign-variables.md) 대화 상자를 엽니다.
* **참조 URL**

## 디자인 대화 상자 {#design-dialog}

구성 요소는 전체 이미지를 보여 주기 때문에 페이지 템플릿 편집 시 디자인 편집 상자는 **페이지 정보 -> 페이지 정책**&#x200B;을 통해 액세스할 수 있습니다.

![페이지 정책](/help/assets/page-policy.png)

### 속성 탭 {#properties-tab}

페이지 디자인 창을 사용하여 페이지에 로드할 클라이언트 라이브러리와 웹 리소스를 정의할 수 있습니다.

![이메일 페이지 구성 요소의 디자인 대화 상자](/help/email/assets/email-page-design.png)

* **클라이언트 라이브러리** - 로드할 클라이언트 라이브러리 범주를 정의합니다. JavaScript는 본문 끝에 추가하고 CSS는 페이지 헤드에 추가합니다.
* **클라이언트 라이브러리 JavaScript 페이지 헤드** - 페이지 헤드에 로드할 JavaScript 클라이언트 라이브러리 범주를 정의합니다.
   * 또한 **클라이언트 라이브러리** 필드에 존재하는 범주를 정의하게 되면 본문 끝이 아닌 페이지 헤드에 JavaScript를 로드할 수 있습니다.
   * 또한 범주가 **클라이언트 라이브러리** 필드에 존재하지 않으면 CSS를 로드할 수 없습니다.
* **JavaScript 라이브러리를 비동기식으로 로드** - 활성화된 경우 사용자 정의 JavaScript 라이브러리가 비동기식으로 로드됩니다.
* **웹 리소스 클라이언트 라이브러리** - favicons와 같은 웹 리소스를 제공하는 데 사용되는 클라이언트 라이브러리 범주
* **메인 콘텐츠 요소 선택기로 건너뛰기** - 페이지의 메인 콘텐츠로 바로 건너뛸 수 있는 접근성 기능으로 사용

**클라이언트 라이브러리**&#x200B;와 **클라이언트 라이브러리 JavaScript 페이지 헤드** 필드 모두에 라이브러리를 구성될 수 있습니다.

* 새 필드를 추가하려면 필드 아래의 **추가** 버튼을 클릭하거나 탭합니다.
* 필드를 제거하려면 필드 옆 휴지통 아이콘을 클릭하거나 탭하여 제거합니다.
* 로드 순서를 재배열하려면 필드 옆 핸들을 클릭하거나 탭하고 드래그하여 이동합니다.

클라이언트측 라이브러리 사용에 대한 자세한 내용은 [클라이언트측 라이브러리 사용](https://helpx.adobe.com/kr/experience-manager/6-5/sites/developing/using/clientlibs.html)을 참조하십시오.

### 스타일 탭 {#styles-tab}

페이지 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

---
title: 이메일 페이지 구성 요소
description: 이메일 페이지 구성 요소
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 40%

---


# 이메일 페이지 구성 요소 {#email-page-component}

이메일 페이지 구성 요소는 [템플릿 편집기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=ko-KR) 그리고 페이지 머리글/바닥글 및 구조 구성 요소를 템플릿 편집기로 취합하여 Adobe Campaign 컨텐츠를 만들 수 있도록 합니다.

## 사용량 {#usage}

이메일 페이지 구성 요소는 이메일 핵심 구성 요소 및 편집 가능한 템플릿으로 디자인된 모든 페이지의 기준을 형성합니다. 이메일 페이지 구성 요소, 머리글, 바닥글 및 페이지의 구조는 다른 이메일 핵심 구성 요소를 사용하여 템플릿으로 정의할 수 있습니다.

* 사용 [디자인 대화 상자,](#design-dialog) 페이지에 대해 사용자 지정 클라이언트측 라이브러리를 정의할 수 있습니다.
* 이메일 페이지 구성 요소는 페이지 자체이므로, 구성 요소에서 직접 액세스할 수 있는 편집 대화 상자가 있는 다른 구성 요소와 달리, [대화 상자 편집](#edit-dialog) 이메일 페이지 구성 요소 는 페이지 속성 창입니다.

## 버전 및 호환성 {#version-and-compatibility}

이메일 페이지 구성 요소의 현재 버전은 v1이며, 이 버전은 2022년 10월에 이메일 핵심 구성 요소의 릴리스 X에서 도입되었으며, 이 문서에 설명되어 있습니다.

다음 표에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | 호환 가능 | 호환 가능 |

이메일 핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 문서를 참조하십시오 [이메일 핵심 구성 요소 버전](/help/email/versions.md)

### 기술 세부 사항 {#technical-details}

페이지 구성 요소에 대한 최신 기술 설명서는[ GitHub에서 확인할 수 있습니다.](https://adobe.com/go/aem_cmp_tech_email_page_v1)

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

## 편집 대화 상자 {#edit-dialog}

구성 요소는 전체 이미지를 보여 주기 때문에 일반적으로 편집 대화 상자에 포함된 설정은 [페이지 속성](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html)에서 찾을 수 있습니다.

### Cloud Services 탭 {#cloud-services}

이메일 핵심 구성 요소가 캠페인 변수와 데이터를 검색하려면 페이지를 Adobe Campaign 구성에 연결해야 합니다.

![이메일 페이지 속성](/help/email/assets/email-page-properties.png)

아래 **Cloud Service 구성** 제목, 드롭다운 선택에서 **구성 추가**.

아래 **Adobe Campaign** 제목: Adobe Campaign과 통합하기 위한 구성을 선택합니다.

문서를 참조하십시오 [이메일 핵심 구성 요소 사용](/help/email/using.md) 이메일 코어 구성 요소 설정에 대한 자세한 정보.

### 이메일 탭 {#email-tab}

이메일 탭은 이메일 제목과 일반 텍스트 컨텐츠와 같은 이 페이지의 컨텐츠를 기반으로 Adobe Campaign을 통해 전송된 이메일의 속성을 정의합니다.

![이메일 페이지 속성](/help/email/assets/email-page-properties-email.png)

* **제목** - 이 페이지를 기반으로 Adobe Campaign에서 보낸 이메일 제목입니다
   * 을(를) 클릭합니다. **Adobe Campaign 변수 선택** 아이콘을 클릭하여 열기 [Adobe Campaign 변수 선택](/help/email/campaign-variables.md) 대화 상자에서 Adobe Campaign의 동적 콘텐츠를 삽입할 수 있습니다.
* **사전 헤더**
   * 을(를) 클릭합니다. **Adobe Campaign 변수 선택** 아이콘을 클릭하여 열기 [Adobe Campaign 변수 선택](/help/email/campaign-variables.md) 대화 상자에서 Adobe Campaign의 동적 콘텐츠를 삽입할 수 있습니다.
* **일반 텍스트** - Adobe Campaign에서 보낸 이메일의 일반 텍스트 버전
   * 을(를) 클릭합니다. **Adobe Campaign 변수 선택** 아이콘을 클릭하여 열기 [Adobe Campaign 변수 선택](/help/email/campaign-variables.md) 대화 상자에서 Adobe Campaign의 동적 콘텐츠를 삽입할 수 있습니다.
* **참조 Url**

## 디자인 대화 상자 {#design-dialog}

구성 요소는 전체 이미지를 보여 주기 때문에 페이지 템플릿 편집 시 디자인 편집 상자는 **페이지 정보 -> 페이지 정책**&#x200B;을 통해 액세스할 수 있습니다.

![페이지 정책](/help/assets/page-policy.png)

### 속성 탭 {#properties-tab}

페이지 디자인 창을 사용하여 페이지에 로드할 클라이언트 라이브러리와 웹 리소스를 정의할 수 있습니다.

![이메일 페이지 구성 요소 디자인 대화 상자](/help/email/assets/email-page-design.png)

* **클라이언트 라이브러리** - 로드할 클라이언트 라이브러리 범주를 정의합니다. JavaScript는 본문 끝에 추가하고 CSS는 페이지 헤드에 추가합니다.
* **클라이언트 라이브러리 JavaScript 페이지 헤드** - 페이지 헤드에 로드할 JavaScript 클라이언트 라이브러리 카테고리를 정의합니다.
   * 또한 **클라이언트 라이브러리** 필드에 존재하는 범주를 정의하게 되면 본문 끝이 아닌 페이지 헤드에 JavaScript를 로드할 수 있습니다.
   * 또한 범주가 **클라이언트 라이브러리** 필드에 존재하지 않으면 CSS를 로드할 수 없습니다.
* **비동기적으로 JavaScript 라이브러리 로드** - 활성화된 경우 사용자 지정 JavaScript 라이브러리가 비동기식으로 로드됩니다.
* **웹 리소스 클라이언트 라이브러리** - favicons와 같은 웹 리소스를 제공하는 데 사용되는 클라이언트 라이브러리 범주
* **메인 콘텐츠 요소 선택기로 건너뛰기** - 페이지의 메인 콘텐츠로 바로 건너뛸 수 있는 접근성 기능으로 사용

**클라이언트 라이브러리**&#x200B;와 **클라이언트 라이브러리 JavaScript 페이지 헤드** 필드 모두에 라이브러리를 구성될 수 있습니다.

* 새 필드를 추가하려면 **추가** 필드 아래에 있는 버튼을 클릭합니다.
* 필드를 제거하려면 제거할 필드 옆에 있는 휴지통 아이콘을 클릭하거나 탭합니다.
* 로드 순서를 재배열하려면 필드 옆 핸들을 클릭하거나 탭하고 드래그하여 이동합니다.

클라이언트측 라이브러리 사용에 대한 자세한 내용은 다음을 참조하십시오 [클라이언트 측 라이브러리 사용.](https://helpx.adobe.com/kr/experience-manager/6-5/sites/developing/using/clientlibs.html)

### 스타일 탭 {#styles-tab}

페이지 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

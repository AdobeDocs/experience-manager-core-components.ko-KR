---
title: 적응형 양식 핵심 구성 요소 - 양식 컨테이너
description: 웹 페이지에 적응형 양식을 추가합니다.
role: Developer, Admin, User
exl-id: 03c4cf7c-51d6-4850-a566-1c0514d52dab
TQID: https://experienceleague.adobe.com/kMG6SKHisAUmKhOh9AFLI8NG6w0vH7tP4XimBKAMo-I
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
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 0af65c80f9cc58c4ba48d5b3dc7a026820bd2833
workflow-type: tm+mt
source-wordcount: 2555
ht-degree: 64%

---

# 양식 컨테이너 {#form-container-adaptive-forms-core-component}

<span class="preview"> 이 문서에서는 시험판 기능인 **초안** 및 **햄버거 메뉴 지원** 기능에 대해 설명합니다. 이 프리릴리스 기능은 [프리릴리스 채널](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html#new-features)을 통해서만 액세스할 수 있습니다.</span>

양식을 사용하면 웹 사이트 방문자가 가치 있는 정보를 제공하여 웹 사이트와 상호 작용할 수 있으므로 참여도와 사용자 만족도를 높일 수 있습니다. AEM(Adobe Experience Manager) Sites의 적응형 양식 컨테이너를 사용하면 웹 사이트 소유자가 자신의 페이지에 간편하게 양식을 추가할 수 있습니다. 이는 방문자가 피드백을 제공하고, 문의하고, 기타 작업을 완료할 수 있는 간소화된 방법을 제공하여 웹 사이트 방문자와 웹 사이트 소유자 또는 조직 간의 커뮤니케이션을 촉진하는 데 도움이 됩니다.

{{traditional-aem}}

## 사용 {#reasons-to-use-forms-container}

웹 사이트에 양식을 추가하는 데에는 다음과 같은 몇 가지 이유가 있습니다.
- **데이터 수집**: 양식을 사용하여 시장 조사, 사용자 행동 분석 등과 같은 다양한 용도를 위해 웹 사이트 방문자로부터 데이터를 수집할 수 있습니다.

- **리드 생성**: 양식을 사용하여 잠재 고객으로부터 이름 및 이메일 주소와 같은 정보를 수집하여 판매 및 마케팅 활동을 위한 리드를 생성할 수 있습니다.

- **전자 상거래**: 온라인 쇼핑에 양식을 사용할 수 있으므로 고객은 웹 사이트를 통해 주문하고 결제할 수 있습니다.

- **연락처**: 연락처 양식을 사용하면 웹 사이트 방문자가 웹 사이트 소유자 또는 조직에 쉽게 연락할 수 있습니다.

- **설문 조사**: 양식을 사용하여 설문 조사를 통해 웹 사이트 방문자로부터 피드백과 의견을 수집할 수 있습니다.

- **이벤트 등록**: 웹 사이트 방문자가 이벤트나 웨비나에 등록할 수 있도록 이벤트 등록에 양식을 사용할 수 있습니다.

- **구독**: 방문자가 뉴스레터 또는 기타 정기 커뮤니케이션에 등록할 수 있도록 웹 사이트 구독에 양식을 사용할 수 있습니다.

- **사용자 인증**: 웹 사이트 방문자가 계정을 만들고 로그인하여 독점 콘텐츠 또는 기능에 액세스할 수 있도록 사용자 인증에 양식을 사용할 수 있습니다.

- **전환율 증가**: 잘 디자인된 양식은 사용자가 제품 구매 또는 서비스 가입과 같은 원하는 작업을 쉽게 완료할 수 있도록 하여 전환율을 높일 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

적응형 양식 아코디언 핵심 구성 요소는 Cloud Service의 핵심 구성 요소 2.0.4 및 AEM 6.5.16.0 Forms 이상의 핵심 구성 요소 1.1.12 일부로 2023년 2월에 릴리스되었습니다. 다음 테이블에서는 지원되는 모든 버전, AEM 호환성 및 해당 문서에 대한 링크를 보여 줍니다.

| 구성 요소 버전 | AEM as a Cloud Service | AEM 6.5.16.0 Forms 이상 |
|---|---|---|
| v1 | <br>[릴리스 2.0.4](/help/adaptive-forms/version.md) 이상 버전과 호환 가능 | <br>[릴리스 1.1.12](/help/adaptive-forms/version.md) 이상과 호환합니다(2.0.0 이전 버전). |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/adaptive-forms/version.md) 문서를 참조하십시오.
<!--
## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). 
-->

## 기술 세부 정보 {#technical-details}

적응형 양식 컨테이너 핵심 구성 요소에 대한 최신 정보는 [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/container/v1/container)의 기술 설명서에서 확인할 수 있습니다. 핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 확인하십시오.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자를 사용하여 방문자를 위한 양식 컨테이너 경험을 손쉽게 사용자 정의할 수 있습니다. 양식 컨테이너 옵션을 간편하게 정의하여 원활한 사용자 경험을 제공할 수도 있습니다.

### 기본 탭 {#basic-tab}

![기본 탭](/help/adaptive-forms/assets/formcontainer_basictab1.png)

- **제목** - 제목을 사용하면 양식에서 구성 요소를 쉽게 식별할 수 있으며, 기본적으로 제목은 구성 요소 상단에 나타납니다. 제목을 추가하지 않으면 제목 텍스트 대신 구성 요소의 이름이 표시됩니다.

- **미리 채우기 서비스** - 이 옵션을 사용하여 적응형 양식이 렌더링될 때 미리 채우기 서비스를 선택하여 데이터를 검색할 수 있습니다. [미리 채우기 서비스를 만들고 구성하는 방법](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/prepopulate-adaptive-form-fields.html?lang=ko#aem-forms-custom-prefill-service)에 대해 자세히 알아보십시오.

- **역할**: 역할은 화면 판독기와 같은 보조 기술에 대한 HTML 요소의 용도를 지정하는 데 사용되는 HTML 속성입니다. 역할 속성은 요소에 추가 컨텍스트 및 의미를 제공하는 데 사용되며, 이를 통해 화면 판독기는 콘텐츠를 더 쉽게 해석하고 사용자에게 알릴 수 있습니다. 예를 들어 AEM Forms에서 양식 필드의 레이블은 “레이블”이라는 역할을 가질 수 있으며 해당 입력 필드는 “텍스트 상자”라는 역할을 가질 수 있습니다. 이렇게 하면 화면 판독기가 레이블과 입력 필드 간의 관계를 이해하고 사용자에게 올바르게 알릴 수 있습니다.

- **클라이언트 라이브러리 카테고리** - 사용자는 적응형 양식별로 사용자 정의 JavaScript 라이브러리를 구성할 수 있습니다. jquery 및 underscore.js 서드파티 라이브러리에 종속된 재사용 가능한 함수만 라이브러리에 유지하는 것이 좋습니다.**복잡한 유효성 검사 규칙**&#x200B;이 있는 경우에는 정확한 유효성 검사 스크립트는 사용자 정의 함수에 있고 사용자는 필드 유효성 검사 표현식에서 이러한 사용자 정의 함수를 호출합니다. 서버측 유효성 검사를 수행하면서 이 사용자 정의 함수 라이브러리를 이해하고 사용할 수 있도록 양식 사용자는 적응형 양식 컨테이너 속성의 **[!UICONTROL 기본]** 탭 아래에서 AEM 클라이언트 라이브러리 이름을 구성할 수 있습니다.사용자는 적응형 양식별로 사용자 정의 JavaScript 라이브러리를 구성할 수 있습니다. jquery 및 underscore.js 서드파티 라이브러리에 종속된 재사용 가능한 함수만 라이브러리에 유지됩니다.

- **모바일 보기용 햄버거 메뉴를 사용하도록 설정** - 모바일 보기용 폼에 햄버거 메뉴를 통합하려면 확인란을 선택하십시오. 세로로 스택된 세 개의 가로 라인으로 표시된 이 메뉴는 작은 장치, 특히 모바일 장치의 패널에 대해 명확하고 깔끔한 디스플레이를 제공합니다. 햄버거 메뉴에 대한 자세한 내용은 [햄버거 메뉴에 대한 자세한 정보](#learn-more-about-the-hamburger-menu) 섹션을 참조하세요.


### 데이터 모델 탭 {#data-model-tab}

![데이터 모델 탭](/help/adaptive-forms/assets/formcontainer_fdmtab.png)

양식 데이터 모델을 사용하면 양식을 데이터 소스에 연결하여 사용자 작업에 따라 데이터를 보내고 받을 수 있습니다. 양식을 JSON 스키마에 연결하여 미리 정의된 형식으로 제출된 데이터를 받을 수도 있습니다. 요구 사항에 따라 양식을 JSON 스키마 또는 양식 데이터 모델에 연결합니다.
- **없음** - 양식을 데이터 모델과 연결하지 마십시오.
- **스키마** - 환경에 업로드된 JSON 스키마에 양식을 연결합니다.
- **양식 데이터 모델** - 양식을 양식 데이터 모델에 연결하여 외부 데이터 소스와 통합합니다.
- **커넥터** - 양식을 커넥터 기반 데이터 원본에 연결합니다.
- **양식 서식 파일** - 양식을 양식 서식 파일과 연결합니다.

### 초안 탭 {#drafts-tab}

![초안 탭](/help/adaptive-forms/assets/formcontainer_autosavetab.png)

- **자동으로 초안 저장**: **자동으로 초안 저장** 확인란을 선택하면 양식을 초안으로 저장할 수 있습니다.
- **환경 설정 저장**: **정기적으로 초안 저장**&#x200B;으로 **환경 설정 저장**&#x200B;을 구성하면 일정 시간이 지날 때 양식을 자동으로 저장하게 할 수 있습니다.
  **간격 빈도(초) 저장**: 정의된 간격으로 양식이 자동 저장되는 기간을 설정할 시간 간격(초)을 지정합니다.

### 제출 탭 {#submission-tab}

사용자는 적응형 양식 제출에 대해 다양한 작업을 구성할 수 있습니다.

- **제출 시** - 제출 후 양식 사용자를 구성된 페이지로 보내려면 **URL로 리디렉션**&#x200B;을 선택하고, 양식에 확인 메시지를 표시하려면 **메시지 표시**&#x200B;를 선택합니다.

- **리디렉션 URL/경로** - 이 옵션을 사용하면 사용자가 적응형 양식을 제출한 후 양식 사용자가 리디렉션되는 각 양식에 대한 페이지를 구성할 수 있습니다. [리디렉션 페이지 구성 방법](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-redirect-page.html?lang=ko)에 대한 자세한 내용을 보려면 여기를 클릭하십시오.

![제출 탭](/help/adaptive-forms/assets/formcontainer_submissiontab.png)

- **메시지 표시** - 이 옵션을 사용하면 적응형 양식이 정상적으로 제출될 때 표시되는 메시지를 추가할 수 있습니다. 대화 상자에는 사전 정의된 텍스트가 포함되며 사용자는 이를 수정할 수 있습니다. 메시지 표시 대화 상자는 사용자가 추가된 텍스트의 서식을 지정할 수 있도록 하는 서식 있는 텍스트 서식 도구를 지원합니다.

![메시지 표시 탭](/help/adaptive-forms/assets/formconatiner_showmessage.png)

- **제출 액션** - 사용자가 적응형 양식에서 [제출] 버튼을 클릭하면 제출 액션이 트리거됩니다. 사용자는 기본적으로 지원되는 드롭다운 목록에서 [제출 작업]을 선택할 수 있습니다. [[제출] 탭에서 제출 액션을 구성](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html?lang=ko#supporting-custom-functions-in-validation-expressions-br)하는 방법에 대해 알아보십시오.

- **작업 구성** - 필드 값을 감사 페이지 요청 매개 변수로 전달하기 위한 매핑을 구성합니다.

- **POST 요청 활성화** - HTTP POST 요청을 사용하여 양식 데이터를 제출하려면 이 옵션을 선택하십시오.

### 기록 문서 탭 {#document-of-record-tab}

![기록 문서 탭](/help/adaptive-forms/assets/formcontainer_dortab.png)

[DoR(Document of Record)](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/generate-document-of-record-core-components)은(는) 양식을 통해 제출된 데이터를 공식적으로 인쇄할 수 있는 표현입니다. **기록 문서** 탭을 사용하여 사용자가 양식을 제출할 때 DoR이 생성되는 방법을 구성하십시오.

- **없음** - 양식에 대한 기록 문서를 생성하지 않습니다.
- **양식 템플릿을 기록 문서 템플릿으로 연결** - 기존 양식 템플릿을 DoR 템플릿으로 사용
- **기록 문서 생성** - 제출된 양식 데이터를 기반으로 DoR을 자동으로 생성합니다.
- **기록 문서에서 첨부 파일 제외** - 생성된 DoR에서 첨부 파일을 생략하려면 이 옵션을 선택하십시오.

## 디자인 대화 상자 {#design-dialog}

디자인 대화 상자는 양식 컨테이너 구성 요소의 CSS 스타일을 정의하고 관리하는 데 사용됩니다.

### 허용된 구성 요소 탭 {#allowed-components-tab}

![디자인 대화 상자 허용된 구성 요소 탭](/help/adaptive-forms/assets/formcontainer-allowedcomponents.png)

**허용된 구성 요소** 탭을 사용하면 템플릿 편집기에서 적응형 양식 편집기의 구성 요소 패널에 항목으로 추가할 수 있는 구성 요소를 설정할 수 있습니다.

### 기본 구성 요소 탭 {#default-components-tab}

![디자인 대화 상자 기본 구성 요소 탭](/help/adaptive-forms/assets/formcontainer-defaultcomponents.png)

**기본 구성 요소** 탭을 통해 템플릿 편집기에서 적응형 양식 편집기의 양식 컨테이너 구성 요소에 항목으로 기본 표시되는 구성 요소를 지정할 수 있습니다.

### 반응형 설정 탭 {#responsive-tab}

![디자인 대화 상자 반응형 설정 탭](/help/adaptive-forms/assets/formcontainer-responsivestyle.png)

**반응형 설정** 탭을 통해 템플릿 편집기에서 적응형 양식 편집기의 양식 컨테이너 구성 요소 내 격자의 열 수를 지정할 수 있습니다.

### 스타일 탭 {#styles-tab}

적응형 양식 첨부 파일 핵심 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

![디자인 대화 상자](/help/adaptive-forms/assets/formcontainer-styletab.png)

- **기본 CSS 클래스**: 적응형 양식 양식 컨테이너 핵심 구성 요소에 기본 CSS 클래스를 제공할 수 있습니다.

- **허용된 스타일**: 이름과 스타일을 나타내는 CSS 클래스를 제공하여 스타일을 정의할 수 있습니다. 예를 들어 “bold text”라는 스타일을 만들고 “font-weight: bold”라는 CSS 클래스를 제공할 수 있습니다. 적응형 양식 편집기에서 이러한 스타일을 적응형 양식에 사용하거나 적용할 수 있습니다. 스타일을 적용하려면 적응형 양식 편집기에서 스타일을 적용할 구성 요소를 선택하고 속성 대화 상자로 이동한 다음 **스타일** 드롭다운 목록에서 원하는 스타일을 선택합니다. 스타일을 업데이트하거나 수정해야 하는 경우 디자인 대화 상자로 돌아가서 스타일 탭에서 스타일을 업데이트하고 변경 내용을 저장하면 됩니다.

### 사용자 정의 속성 탭

![사용자 정의 속성 대화 상자](/help/adaptive-forms/assets/formcontainer-custompropertiestab.png)

사용자 정의 속성을 사용하면 양식 템플릿을 사용하여 사용자 정의 속성(키-값 쌍)을 적응형 양식 핵심 구성 요소에 연결할 수 있습니다. 사용자 정의 속성은 구성 요소의 Headless 렌디션에서 속성 섹션에 반영됩니다. 사용자 정의 속성 값에 따라 조정되는 동적 양식 동작을 만들 수 있습니다. 예를 들어 개발자는 모바일, 데스크탑 또는 웹 플랫폼을 위한 Headless 양식 구성 요소의 다양한 표현을 디자인하여 다양한 디바이스에서 사용자 경험을 크게 향상시킬 수 있습니다.

- **그룹 이름**: 사용자 정의 속성 그룹을 식별하기 위해 이름을 제공할 수 있습니다. 여러 사용자 정의 속성 그룹을 추가, 삭제 또는 재배열할 수 있습니다. 사용자 정의 속성 그룹을 추가하면 다음 옵션이 표시됩니다.

   - **키-값 쌍**: 각 사용자 정의 속성 그룹의 **추가** 버튼을 클릭하여 여러 사용자 정의 속성 이름과 사용자 정의 속성 값을 추가할 수 있습니다.

   - **삭제**: 사용자 정의 속성 이름과 사용자 정의 속성 값을 탭하거나 클릭하여 삭제할 수 있습니다.

   - **재배열**: 사용자 정의 속성 이름과 사용자 정의 속성 값을 탭하거나 클릭하고 드래그하면 순서를 재배열할 수 있습니다.

## 햄버거 메뉴에 대해 자세히 알아보기 {#learn-more-about-the-hamburger-menu}

모바일 메뉴 또는 탐색 서랍 이라고도 하는 햄버거 메뉴는 모바일 사용자 인터페이스에서 많이 사용되는 디자인 요소입니다. 세로로 3개의 가로줄이 햄버거를 연상케 하는 것이 특징이다. 이 디자인은 특히 모바일과 같은 작은 디바이스에서 보조 탐색 옵션이 필요할 때까지 숨겨서 화면 공간을 효율적으로 절약합니다. 햄버거 메뉴 내에서 AEM 양식을 효율적으로 구성할 수 있어 메인 인터페이스를 압도하지 않고도 양식 내에서 다양한 패널에 액세스할 수 있습니다.

금융 기관에서 사용자가 개인 세부 정보, 금융 정보, 대출 선호도 및 지원 문서 등 여러 패널에 걸쳐 세부 정보를 제공하도록 하는 온라인 대출 신청 양식을 제공하는 시나리오를 고려하십시오. 양식에는 특히 모바일 장치에서 인터페이스를 더 복잡하게 만들 수 있는 여러 패널과 옵션이 포함되어 있습니다. 사용자는 부담감을 느끼지 않고 이러한 패널을 탐색할 수 있는 체계적인 방법이 필요합니다. 햄버거 메뉴는 모바일 장치에서 사용자 경험을 개선하기 위해 구현되었습니다.

### 햄버거 메뉴의 구성 요소

![햄버거 메뉴](/help/adaptive-forms/assets/hamburger-menu.png){width=50%, align=center}

**A. 햄버거 메뉴**: 햄버거 메뉴에는 햄버거 아이콘을 클릭하거나 탭하면 슬라이드 아웃되거나 드롭되는 탐색 패널이 있습니다. 메뉴에 패널 제목이 표시되고 패널을 선택하면 포커스가 해당 패널로 이동합니다. 사용자가 다른 패널 간을 쉽게 탐색할 수 있습니다.

![햄버거 메뉴](/help/adaptive-forms/assets/hamburger-menu-icon.png){width=50%}

**B. 이동 경로**: 이동 경로는 양식 내에서 사용자의 현재 위치를 나타냅니다. 사용자의 탐색 경로를 보여 주고 형식에서 사용자의 위치를 이해하는 데 도움이 되는 계층 구조 추적을 제공합니다.

**C. 활성 패널**: 활성 패널은 현재 표시 중인 양식의 섹션 또는 일부를 참조합니다. 사용자가 햄버거 메뉴에서 옵션을 선택하면 해당 패널이 활성 패널이 되어 해당 섹션에 대한 관련 필드 및 정보가 표시됩니다.

### 햄버거 메뉴를 사용하여 작업하는 동안 고려해야 할 사항

- 햄버거 메뉴에는 패널 이름만 표시됩니다. 다음은 패널의 구성 속성에 따라 햄버거 메뉴의 탐색 창에 패널 이름이 표시되는 방식을 보여 주는 여러 가지 시나리오입니다.

   - 패널의 속성을 숨김으로 설정하면 햄버거 메뉴의 탐색 창에 패널 이름이 나타나지 않습니다. 예를 들어 `Financial Information` 패널의 속성을 `hidden`(으)로 구성하는 경우 햄버거 메뉴의 탐색 창에 패널 이름이 표시되지 않습니다.

     ![숨겨진 패널](/help/adaptive-forms/assets/hidden-panel.png){width=50%}

   - 패널의 속성을 `disabled`(으)로 설정하면 해당 이름이 햄버거 메뉴의 탐색 창에 표시되지만 해당 이름을 선택하거나 편집할 수는 없습니다. 예를 들어 `Financial Information` 패널의 속성을 `disabled`(으)로 구성하면 탐색 창에 패널 이름이 표시되지만 패널 이름을 선택하거나 편집할 수는 없습니다.

     ![비활성화된 패널](/help/adaptive-forms/assets/disabled-panel.png){width=50%}

   - 패널 제목을 숨기면 햄버거 메뉴의 탐색 창에 패널 제목이 표시되지 않습니다. 대신 빈 공백이 표시되지만, 해당 공백을 클릭하여 패널의 필드로 이동할 수 있습니다. 예를들어 `Financial Information` 패널의 제목을 숨기면 햄버거 메뉴의 탐색 창에 빈 공백이 그 위치에 나타납니다. 빈 공간을 클릭하여 패널의 필드로 이동할 수 있습니다.

     ![숨겨진 제목 패널](/help/adaptive-forms/assets/hidden-title-panel.png){width=50%}

- 이동 경로 구성 요소의 탐색 창은 기본적으로 최대 3가지 수준의 탐색을 지원합니다. 그러나 사용자 지정 구성 요소를 사용하여 필요한 만큼 많은 수준을 수용하도록 탐색 계층을 구성할 수 있습니다.
- 햄버거 메뉴를 사용할 때 사용자는 화살표를 사용하여 패널 사이를 탐색할 수 있습니다. 그러나 패널을 선택하면 메뉴가 자동으로 닫히고 포커스가 선택한 패널 내의 필드로 이동합니다.

<!--
### Advantages to use hamburger menu

- **Space efficiency**: By hiding form navigation options until needed, the hamburger menu maximizes screen space, which is especially beneficial on smaller devices.

- **Clutter reduction**: It minimizes visual clutter by consolidating various form navigation links into a single, collapsible menu.

- **Improved focus**: With fewer visible navigation elements, users can concentrate on the main content of the form without being distracted by secondary options.

- **Simplified design**: It creates a more streamlined user interface, resulting in a cleaner and more organized form layout.

- **Enhanced mobile experience**: On mobile devices, where screen space is limited, the hamburger menu offers an efficient way to access all form navigation options without overwhelming the user.

### How to enable hamburger menu for your form?

To enable hamburger menu for form, perform the following steps:

1. Open form in an edit mode.
1. Open the Content browser, and select the **[!UICONTROL Guide Container]** component of your Adaptive Form. 
1. Click the Guide Container properties ![Guide properties](/help/adaptive-forms/assets/configure_icon.png) icon. The Adaptive Form Container dialog box opens. 
1. Click the  **[!UICONTROL Basic]** tab. 
1. Select the **[!UICONTROL Add hamburger menu support]** checkbox.
1. Click **[!UICONTROL Done]**.

![Basic tab](/help/adaptive-forms/assets/formcontainer_basictab1.png)
-->

## 관련 문서 {#related-articles}

{{more-like-this}}

## 추가 참조 {#see-also}

{{see-also}}
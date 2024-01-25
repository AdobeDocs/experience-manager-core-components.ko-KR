---
title: 적응형 양식 핵심 구성 요소 - 양식 컨테이너
description: 웹 페이지에 적응형 양식을 추가합니다.
role: Architect, Developer, Admin, User
exl-id: 03c4cf7c-51d6-4850-a566-1c0514d52dab
source-git-commit: 4d01c75fadb0220f0093a6647c27c4002cc979c9
workflow-type: tm+mt
source-wordcount: '1297'
ht-degree: 91%

---

# 양식 컨테이너 {#form-container-adaptive-forms-core-component}

양식을 사용하면 웹 사이트 방문자가 가치 있는 정보를 제공하여 웹 사이트와 상호 작용할 수 있으므로 참여도와 사용자 만족도를 높일 수 있습니다. AEM(Adobe Experience Manager) Sites의 적응형 양식 컨테이너를 사용하면 웹 사이트 소유자가 자신의 페이지에 간편하게 양식을 추가할 수 있습니다. 이는 방문자가 피드백을 제공하고, 문의하고, 기타 작업을 완료할 수 있는 간소화된 방법을 제공하여 웹 사이트 방문자와 웹 사이트 소유자 또는 조직 간의 커뮤니케이션을 촉진하는 데 도움이 됩니다.

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

적응형 양식 아코디언 핵심 구성 요소는 Cloud Service의 핵심 구성 요소 2.0.4 및 AEM 6.5.16.0 Forms 이상의 핵심 구성 요소 1.1.12 일부로 2023년 2월에 릴리스되었습니다. 다음 표에서는 지원되는 모든 버전, AEM 호환성 및 해당 문서에 대한 링크를 보여 줍니다.

| 구성 요소 버전 | AEM as a Cloud Service | AEM 6.5.16.0 Forms 이상 |
|---|---|---|
| v1 | <br>[릴리스 2.0.4](/help/adaptive-forms/version.md) 이상 버전과 호환 가능 | <br>[릴리스 1.1.12](/help/adaptive-forms/version.md) 이상과 호환합니다(2.0.0 이전 버전). |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/adaptive-forms/version.md) 문서를 참조하십시오.
<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## 기술 세부 정보 {#technical-details}

적응형 양식 컨테이너 핵심 구성 요소에 대한 최신 정보는 [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/container/v1/container)의 기술 설명서에서 확인할 수 있습니다. 핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 확인하십시오.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자를 사용하여 방문자를 위한 양식 컨테이너 경험을 손쉽게 사용자 정의할 수 있습니다. 양식 컨테이너 옵션을 간편하게 정의하여 원활한 사용자 경험을 제공할 수도 있습니다.

### 기본 탭 {#basic-tab}

![기본 탭](/help/adaptive-forms/assets/formcontainer_basictab.png)

- **미리 채우기 서비스** - 이 옵션을 사용하여 적응형 양식이 렌더링될 때 미리 채우기 서비스를 선택하여 데이터를 검색할 수 있습니다. [미리 채우기 서비스를 만들고 구성하는 방법](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/prepopulate-adaptive-form-fields.html?lang=ko#aem-forms-custom-prefill-service)에 대해 자세히 알아보십시오.

- **클라이언트 라이브러리 범주** - 사용자는 적응형 양식별로 사용자 정의 JavaScript 라이브러리를 구성할 수 있습니다. jquery 및 underscore.js 타사 라이브러리에 종속성이 있는 재사용 가능한 함수만 라이브러리에 유지하는 것이 좋습니다.
다음과 같은 경우 **복잡한 유효성 검사 규칙**, 정확한 유효성 검사 스크립트는 사용자 정의 함수에 상주하며 사용자는 필드 유효성 검사 표현식에서 이러한 사용자 정의 함수를 호출합니다. 서버측 유효성 검사를 수행하는 동안 이 사용자 정의 함수 라이브러리를 알고 사용할 수 있도록 하기 위해 양식 사용자는 아래 AEM 클라이언트 라이브러리의 이름을 구성할 수 있습니다. **[!UICONTROL 기본]** 아래 표시된 대로 적응형 양식 컨테이너 속성의 탭

사용자는 적응형 양식에 따라 customJavaScript 라이브러리를 구성할 수 있습니다. jquery 및 underscore.js 서드파티 라이브러리에 종속된 재사용 가능한 함수만 라이브러리에 유지됩니다.

### 데이터 모델 탭 {#data-model-tab}

![전송 탭](/help/adaptive-forms/assets/formcontainer_fdmtab.png)

양식 데이터 모델을 사용하면 양식을 데이터 소스에 연결하여 사용자 작업에 따라 데이터를 보내고 받을 수 있습니다. 양식을 JSON 스키마에 연결하여 미리 정의된 형식으로 제출된 데이터를 받을 수도 있습니다. 요구 사항에 따라 양식을 JSON 스키마 또는 양식 데이터 모델에 연결합니다.
- JSON 스키마를 만들고 환경에 업로드
- 양식 데이터 모델 만들기

### 전송 탭 {#submission-tab}

![전송 탭](/help/adaptive-forms/assets/formcontainer_submissiontab.png)

사용자는 적응형 양식 제출에 대해 다양한 작업을 구성할 수 있습니다.

- **리디렉션 URL/경로** - 이 옵션을 사용하면 사용자가 적응형 양식을 제출한 후 양식 사용자가 리디렉션되는 각 양식에 대한 페이지를 구성할 수 있습니다. [리디렉션 페이지 구성 방법](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-redirect-page.html)에 대한 자세한 내용을 보려면 여기를 클릭하십시오.

![메시지 표시 탭](/help/adaptive-forms/assets/formconatiner_showmessage.png)

- **메시지 표시** - 이 옵션을 사용하면 적응형 양식이 정상적으로 제출될 때 표시되는 메시지를 추가할 수 있습니다. 대화 상자에는 사전 정의된 텍스트가 포함되며 사용자는 이를 수정할 수 있습니다. 메시지 표시 대화 상자는 사용자가 추가된 텍스트의 서식을 지정할 수 있도록 하는 서식 있는 텍스트 서식 도구를 지원합니다.

- **제출 액션** - 사용자가 적응형 양식에서 [제출] 버튼을 클릭하면 제출 액션이 트리거됩니다. 사용자는 기본적으로 지원되는 드롭다운 목록에서 [제출 작업]을 선택할 수 있습니다. [[제출] 탭에서 제출 액션을 구성](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#supporting-custom-functions-in-validation-expressions-br)하는 방법에 대해 알아보십시오.

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

**반응형 설정** 탭을 통해 템플릿 편집기에서 적응형 양식 편집기의 양식 컨테이너 구성 요소 내 그리드의 열 수를 지정할 수 있습니다.

### 스타일 탭 {#styles-tab}

적응형 양식 첨부 파일 핵심 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

![디자인 대화 상자](/help/adaptive-forms/assets/formcontainer-styletab.png)

- **기본 CSS 클래스**: 적응형 Forms 양식 컨테이너 핵심 구성 요소에 대한 기본 CSS 클래스를 제공할 수 있습니다.

- **허용된 스타일**: 이름과 스타일을 나타내는 CSS 클래스를 제공하여 스타일을 정의할 수 있습니다. 예를 들어 “bold text”라는 스타일을 만들고 “font-weight: bold”라는 CSS 클래스를 제공할 수 있습니다. 적응형 양식 편집기에서 이러한 스타일을 적응형 양식에 사용하거나 적용할 수 있습니다. 스타일을 적용하려면 적응형 양식 편집기에서 스타일을 적용할 구성 요소를 선택하고 속성 대화 상자로 이동한 다음 **스타일** 드롭다운 목록에서 원하는 스타일을 선택합니다. 스타일을 업데이트하거나 수정해야 하는 경우 디자인 대화 상자로 돌아가서 스타일 탭에서 스타일을 업데이트하고 변경 내용을 저장하면 됩니다.

### 사용자 정의 속성 탭

![사용자 정의 속성 대화 상자](/help/adaptive-forms/assets/formcontainer-custompropertiestab.png)

사용자 정의 속성을 사용하면 양식 템플릿을 사용하여 사용자 정의 속성(키-값 쌍)을 적응형 양식 핵심 구성 요소에 연결할 수 있습니다. 사용자 정의 속성은 구성 요소의 Headless 렌디션에서 속성 섹션에 반영됩니다. 사용자 정의 속성 값에 따라 조정되는 동적 양식 동작을 만들 수 있습니다. 예를 들어 개발자는 모바일, 데스크탑 또는 웹 플랫폼을 위한 Headless 양식 구성 요소의 다양한 표현을 디자인하여 다양한 디바이스에서 사용자 경험을 크게 향상시킬 수 있습니다.

- **그룹 이름**: 사용자 정의 속성 그룹을 식별하기 위해 이름을 제공할 수 있습니다. 여러 사용자 정의 속성 그룹을 추가, 삭제 또는 재배열할 수 있습니다. 사용자 정의 속성 그룹을 추가하면 다음 옵션이 표시됩니다.

   - **키-값 쌍**: 각 사용자 정의 속성 그룹의 **추가** 버튼을 클릭하여 여러 사용자 정의 속성 이름과 사용자 정의 속성 값을 추가할 수 있습니다.

   - **삭제**: 사용자 정의 속성 이름과 사용자 정의 속성 값을 탭하거나 클릭하여 삭제할 수 있습니다.

   - **재배열**: 사용자 정의 속성 이름과 사용자 정의 속성 값을 누르거나 클릭하고 드래그하면 순서를 재배열할 수 있습니다.

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## 관련 문서 {#related-articles}

{{more-like-this}}

## 추가 참조 {#see-also}

{{see-also}}
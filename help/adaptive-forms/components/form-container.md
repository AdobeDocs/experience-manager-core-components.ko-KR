---
title: 적응형 Forms 코어 구성 요소 - 양식 컨테이너
description: 웹 페이지에 적응형 양식 추가
role: Architect, Developer, Admin, User
source-git-commit: 7f680eac1da61b55f9d90db6c0842421d03ac1dc
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 3%

---


# 양식 컨테이너 {#form-container-adaptive-forms-core-component}

Forms을 사용하면 웹 사이트 방문자가 중요한 정보를 제공하여 웹 사이트와 상호 작용할 수 있으므로 참여도와 사용자 만족도를 높일 수 있습니다. AEM(Adobe Experience Manager) 사이트의 적응형 양식 컨테이너를 사용하면 웹 사이트 소유자가 페이지에 양식을 쉽게 추가할 수 있습니다. 따라서 방문자가 피드백을 제공하고, 문의하고, 기타 작업을 완료할 수 있는 간소화된 방법을 제공하여 웹 사이트 방문자와 웹 사이트 소유자 또는 조직 간의 커뮤니케이션을 용이하게 할 수 있습니다

## 사용 {#reasons-to-use-forms-container}

웹 사이트에 양식을 추가할 수 있는 이유는 다음과 같습니다.

* **데이터 수집**: Forms은 시장 조사, 사용자 행동 분석 등과 같은 다양한 용도로 웹 사이트 방문자의 데이터를 수집하는 데 사용할 수 있습니다.

* **리드 생성**: 양식을 사용하여 이름 및 이메일 주소와 같은 잠재 고객의 정보를 수집하여 영업 및 마케팅 활동에 대한 리드를 생성할 수 있습니다.

* **전자 상거래**: Forms은 온라인 쇼핑에 사용될 수 있으며, 고객이 웹 사이트를 통해 주문을 하고 대금을 결제할 수 있습니다.

* **연락처**: 웹 사이트 방문자가 웹 사이트 소유자 또는 조직에 쉽게 연락할 수 있는 연락처 양식을 제공합니다.

* **설문 조사 및 투표**: Forms은 설문 조사와 여론 조사를 통해 웹 사이트 방문자의 피드백과 의견을 수집하는 데 사용할 수 있습니다.

* **이벤트 등록**: Forms은 이벤트 등록에 사용할 수 있으므로 웹 사이트 방문자가 이벤트 또는 웨비나에 등록할 수 있습니다.

* **구독**: Forms은 웹 사이트 가입에 사용할 수 있으므로 방문자가 뉴스레터 또는 기타 일반 커뮤니케이션에 등록할 수 있습니다.

* **사용자 인증**: Forms은 사용자 인증에 사용할 수 있으므로 웹 사이트 방문자가 계정을 만들고 로그인하여 단독 컨텐츠 또는 기능에 액세스할 수 있습니다.

* **전환율 증가**: 잘 디자인된 양식은 사용자가 제품 구매나 서비스 등록과 같은 원하는 작업을 쉽게 완료할 수 있도록 하여 전환율을 높일 수 있습니다.


## 버전 및 호환성 {#version-and-compatibility}

응용 Forms 컨테이너 코어 구성 요소는 코어 구성 요소 2.0.4의 일부로 2023년 2월에 출시되었습니다. 다음은 지원되는 모든 버전, AEM 호환성 및 해당 설명서 링크를 보여주는 표입니다.

| 구성 요소 버전 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | 호환 가능 with<br>[릴리스 2.0.4](/help/versions.md) 나중에 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md) 문서.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## 기술 세부 사항 {#technical-details}

응용 Forms 컨테이너 코어 구성 요소에 대한 최신 정보를 다음에 대한 기술 문서에서 얻습니다. [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/container/v1/container). 핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md).

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자에서 방문자의 양식 컨테이너 경험을 쉽게 사용자 지정할 수 있습니다. 또한 원활한 사용자 경험을 위해 양식 컨테이너 옵션을 쉽게 정의할 수 있습니다.

### 기본 탭 {#basic-tab}

![기본 탭](/help/adaptive-forms/assets/formcontainer_basictab.png)

* **미리 채우기 서비스** - 이 옵션을 사용하면 적응형 양식을 렌더링할 때 데이터를 검색할 미리 채우기 서비스를 선택할 수 있습니다. 추가 정보 [미리 채우기 서비스를 만들고 구성하는 방법](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/prepopulate-adaptive-form-fields.html?lang=en#aem-forms-custom-prefill-service).

* **클라이언트 라이브러리 카테고리** - 사용자는 적응형 양식에 따라 사용자 지정 JavaScript 라이브러리를 구성할 수 있습니다. jquery 및 underscore.js 타사 라이브러리에 대한 종속성이 있는 재사용 가능한 함수만 라이브러리에 유지하는 것이 좋습니다.

### 제출 탭 {#submission-tab}

![제출 탭](/help/adaptive-forms/assets/formcontainer_submissiontab.png)

사용자는 적응형 양식 제출에 대해 다른 작업을 구성할 수 있습니다.
* **리디렉션 URL/경로** - 이 옵션을 사용하면 적응형 양식을 제출한 후 양식 사용자가 리디렉션되는 각 양식에 대해 페이지를 구성할 수 있습니다. 자세한 내용을 보려면 여기를 클릭하십시오. [리디렉션 페이지 구성 방법](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-redirect-page.html).

![메시지 탭 표시](/help/adaptive-forms/assets/formconatiner_showmessage.png)

* **메시지 표시** - 이 옵션을 사용하면 적응형 양식을 성공적으로 제출할 때 표시되는 메시지를 추가할 수 있습니다. 사전 정의된 텍스트가 대화 상자에 포함되어 있으며 사용자가 수정할 수 있습니다. 메시지 표시 대화 상자는 사용자가 추가된 텍스트의 서식을 지정할 수 있도록 해주는 리치 텍스트 형식 도구를 지원합니다.

* **작업 제출** - 사용자가 적응형 양식에서 제출 단추를 클릭하면 제출 작업이 트리거됩니다. 사용자는 드롭다운 목록에서 즉시 지원되는 작업 제출 을 선택할 수 있습니다. 방법 알아보기 [제출 탭에서 제출 작업 구성](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#supporting-custom-functions-in-validation-expressions-br).

## 디자인 대화 상자 {#design-dialog}




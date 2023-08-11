---
title: AEM Forms용 샘플 테마 및 템플릿을 가져오는 방법은 무엇입니까?
description: AEM Forms Core Components는 샘플 적응형 양식 테마, 템플릿 및 양식 데이터 모델을 제공합니다.
solution: Experience Manager Forms
topic: Administration
role: Admin, User
hide: true
hidefromtoc: true
level: Intermediate
source-git-commit: ebbe3471164341076fe085bbef9c93fcb1fe382a
workflow-type: ht
source-wordcount: '1259'
ht-degree: 100%

---


# 샘플 테마, 템플릿 및 양식 데이터 모델 {#sample-themes-templates-and-data-models}

[!DNL AEM Forms] 코어 구성 요소는 바로 사용할 수 있는 샘플 테마, 템플릿 및 양식 데이터 모델을 제공하여 다목적 적응형 양식을 빠르게 생성합니다. 또한 양식 작성자가 [AEM Forms 코어 구성 요소](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html)의 확장성, 적응성 및 응답성을 학습하여 데이터베이스와 원활하게 연결하면서 즉시 간단한 양식을 만들고 복잡한 양식을 쉽게 만들 수 있도록 합니다.

참조 콘텐츠 패키지에 포함된 샘플 테마, 템플릿 및 양식 데이터 모델은 다음과 같습니다.

| 템플릿 | 테마 | 양식 데이터 모델 |
---------|----------|---------
| [기본](#Basic) | [캔버스](#Canvas) | Microsoft® Dynamics 365 |
| [비어 있음](#Blank) | [WKND](#WKND) | Salesforce |
| [문의하기](#Contact-Us) | [이젤](#Easel) |  |
| [연락처 세부 정보 업데이트](#Contact-Details-Update) |   |   |
| [동의서 양식](#Consent-Form) | |  |
| [로그 서비스 요청](#Log-Service-Request) |  |  |
| [피드백 제공](#Give-Feedback) |  |  |
| [혜택 등록](#Benefits-Enrollment) |  |   |
| [직원 혜택 요약](#Employee-Benefits-Summary) |   |   |
| [계정 명세서 요청](#Request-for-Account-Statement) |   |   |
| [안전성 검사 양식](#Safety-Inspection) |   |   |
| [품질 관리 검사](#Quality-Control-Inspection) |   |   |
| [구매 요청](#Purchase-Request) |  |  |

## 샘플 테마 {#Sample-Themes}

참조 샘플 테마는 작성자가 양식에 대한 스타일을 정의하고 맞춤화하는 데 도움이 되며, CSS에 대해 기본적인 지식만 있는 작성자도 필요에 따라 테마를 맞춤화할 수 있습니다.

**이 테마를 가져오는 방법은 무엇입니까?**
* **Forms as a Cloud Service** 환경에서 이 테마를 가져오려면 [적응형 양식 코어 구성 요소](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/enable-adaptive-forms-core-components.html)를 활성화하고 [프론트엔드 파이프라인](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components.html)을 사용하여 이 테마를 배포합니다.
* **AEM 6.5 Forms** 환경에서 이 테마를 가져오려면 [Adaptive Forms 핵심 구성 요소를 활성화](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-core-components/enable-adaptive-forms-core-components.html)하고 [패키지 관리자](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-core-components/create-or-customize-themes-for-adaptive-forms-core-components)를 사용하여 이 테마를 배포합니다.

**즉시 사용 가능한** [적응형 양식 코어 구성 요소](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html) 테마:

![OOTB 테마](/help/adaptive-forms/assets/OOTB-themes.png)

### 캔버스 {#Canvas}

캔버스 테마는 양식의 기본 테마이며 기본 색상, 투명도 및 플랫 아이콘의 사용을 강조합니다. 아래 스크린샷에서 캔버스 테마의 외형을 확인할 수 있습니다.

![캔버스 테마](/help/adaptive-forms/assets/Safety-Inspection-Theme-Canvas.png)

### WKND {#WKND}

WKND 테마는 생동감 있고 창의적이며 매력적인 디자인을 구현하여 양식을 세련되게 만듭니다. 테마는 [Adobe Experience Manager 코어 구성 요소](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html)를 기반으로 구축된 여행 및 모험 웹 사이트인 [WKND 사이트](https://wknd.site/us/en.html)의 모양과 스타일을 기반으로 합니다.

![WKND 테마](/help/adaptive-forms/assets/Safety-Inspection-Form-Theme.png)


### 이젤 {#Easel}

이젤 테마를 사용하여 매력적이고 간단하게 설정할 수 있는 양식 모양을 만들 수 있습니다. 이 테마는 단순성과 사용자 친화성을 위해 맞춤화됩니다. 이젤 테마는 아티스트가 그림 작업을 할 때 캔버스를 지지하기 위해 사용하는 휴대용 스탠드의 개념을 기반으로 합니다.

![이젤 테마](/help/adaptive-forms/assets/Safety-Inspection-Theme-Easel.png)

## 샘플 템플릿 {#Sample-templates}

템플릿은 초기 양식 구조, 콘텐츠 및 작업을 정의하여 양식에 복제하거나 동의서 양식, 혜택 등록 양식 등 양식과 유사한 템플릿 구조를 사용합니다.

**이 템플릿을 가져오는 방법은 무엇입니까?**
[AEM Archetype 43 이상을 기반으로 하는 프로젝트](https://github.com/adobe/aem-project-archetype)를 **AEM Forms as a Cloud Service** 또는 **AEM 6.5** Forms 환경에 배포하여 템플릿을 가져올 수 있습니다.

**즉시 사용 가능한** [적응형 양식 코어 구성 요소](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html) 템플릿:

![참조 템플릿](/help/adaptive-forms/assets/reference-templates-core-components.png)

### 기본 {#Basic}

기본 템플릿을 사용하면 등록 환경 양식을 빠르게 생성할 수 있습니다. 또한 이를 사용하여 [Adaptive Forms 코어 구성 요소](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html)의 기능을 미리 볼 수도 있습니다. 데이터를 섹션별로 표시하기 위한 마법사 레이아웃이 제공됩니다.

![기본 템플릿](/help/adaptive-forms/assets/Basic-template-desktop-view.png)

### 비어 있음 {#Blank}

빈 캔버스 템플릿은 적응형 양식 구조, 콘텐츠 및 규칙을 처음부터 만드는 데 사용됩니다. 빈 템플릿에는 양식 구성 요소가 미리 통합되어 있지 않습니다.

![비어 있는 템플릿](/help/adaptive-forms/assets/Blank-temp-desktop-view.png)

### 문의하기 {#Contact-Us}

문의 양식 템플릿은 웹 사이트 방문자와 양식 관리자 간의 커뮤니케이션을 용이하게 하는 양식을 만드는 데 사용됩니다. 사용자는 해당 양식을 통해 쿼리, 피드백 또는 지원 요청을 제출할 수 있습니다.

![문의 템플릿](/help/adaptive-forms/assets/Contact-us-desktop-view.png)

### 연락처 세부 정보 업데이트 {#Contact-Details-Update}

작성자는 연락처 세부 정보 업데이트 템플릿을 사용하여 고객의 주소 및 연락처 세부 정보를 업데이트하기 위한 양식을 만들 수 있습니다. 또한 이 양식은 고객이 구독 또는 혜택과 관련된 개인 정보를 업데이트하여 원활한 커뮤니케이션과 서비스 또는 혜택에 대한 중단 없는 액세스를 보장하도록 지원합니다.

![문의 정보 업데이트](/help/adaptive-forms/assets/Contact-details-update.png)

### 동의서 양식 {#Consent-Form}

동의 양식 템플릿은 특정 활동, 연구, 의료 절차 또는 개인 정보나 권리에 관련될 수 있는 상황에 참여하는 참가자로부터 법적 문서를 제공받기 위한 양식을 만드는 데 사용됩니다. 이 양식은 투명성을 보장하고 참가자의 권리를 보호하며 개인이 동의하게 되는 내용에 대해 명확히 이해하도록 합니다.

![동의서 양식](/help/adaptive-forms/assets/Consent-form-desktop-view.png)

### 로그 서비스 요청 {#Log-Service-Request}

로그 서비스 요청 템플릿을 사용하여 서비스 공급자에게 로그별 로깅 서비스를 요청하는 양식을 만들 수 있습니다. 이 양식은 모니터링 또는 추적 상태를 위해 기록된 이벤트, 활동 또는 데이터에 대한 티켓을 생성하기 위한 공식 요청으로 사용됩니다.

![로그 서비스 요청 템플릿](/help/adaptive-forms/assets/Log-service-request-desktop-view.png)


### 피드백 제공 {#Give-Feedback}

피드백 제공 양식 템플릿을 사용하여 다른 사용자 또는 팀에 건설적인 피드백을 제공하기 위한 양식을 작성할 수 있습니다. 이 양식은 피드백이 명확하고, 구체적이며, 실행 가능하도록 보장하여 개방적인 커뮤니케이션과 개선을 촉진합니다.

![피드백 제공 템플릿](/help/adaptive-forms/assets/Give-feedback-desktop-view.png)


### 혜택 등록 {#Benefits-Enrollment}

혜택 등록 양식 템플릿은 직원들로부터 선호하는 혜택 및 보상 옵션에 관한 필수 정보를 수집하기 위한 양식을 만드는 데 사용됩니다. 일반적으로 연간 혜택 등록 기간에 제공됩니다.

![혜택 등록 템플릿](/help/adaptive-forms/assets/Benefits-enrollment-form-template.png)


### 직원 혜택 요약 {#Employee-Benefits-Summary}

직원 혜택 요약 양식 템플릿은 개인 혜택에 대한 필수 세부 정보를 수집하기 위한 양식을 만드는 데 사용됩니다. 이는 보장 범위를 빠르고 정확하게 평가하는 데 도움이 되며 효율적인 지원을 위한 포괄적인 개요를 제공합니다.
![직원 혜택 요약](/help/adaptive-forms/assets/Employee-benefits-summary.png)


### 계정 명세서 요청 {#Request-for-Account-Statement}

계정 명세서 요청 템플릿을 사용하여 고객의 정확한 최신 명세서를 제공받는 프로세스를 시작하기 위한 양식을 만들 수 있습니다. 이 명세서는 금융 거래, 활동 또는 이 양식을 사용하는 고객의 기타 관련 정보에 대한 자세한 기록을 제공합니다.

![계정 명세서 요청](/help/adaptive-forms/assets/Request-for-account-statment.png)

### 안전성 검사 {#Safety-Inspection}

안전성 검사 양식 템플릿을 사용하여 안전한 작업 환경을 위한 세부 사항을 입력하는 양식을 만들 수 있습니다. 이 양식을 사용하여 정기 점검을 수행하면 잠재적인 위험을 식별할 수 있습니다. 이 양식은 비상구, 화재 안전, 전기 안전, 위험 물질, 개인 보호 장비, 직원, 방문자 및 고객의 안전과 복지를 위한 워크스테이션 인체 공학과 같은 다양한 측면을 포함합니다.

![안전성 검사 양식](/help/adaptive-forms/assets/Safety-inspection-form.png)

### 품질 관리 검사 {#Quality-Control-Inspection}

품질 관리 검사 양식 템플릿은 제품 또는 항목의 시각적 모양, 치수, 기능, 문서, 테스트 결과 및 전반적인 품질을 평가하고 문서화하기 위한 양식을 만드는 데 사용됩니다. 이는 품질 표준을 준수하는 데 필요한 결함, 부적합 및 시정 조치를 식별하는 데 도움이 됩니다.

![품질 관리 검사](/help/adaptive-forms/assets/Quality-Control-Inspection.png)


### 구매 요청 {#Purchase-Request}

구매 요청 양식 템플릿을 사용하여 구매 프로세스를 시작하고 직원이 업무에 필요한 상품 또는 서비스 구매를 공식적으로 요청하기 위한 양식을 작성할 수 있습니다. 이 양식은 항목 설명, 수량, 선호하는 공급자(해당되는 경우), 예산 할당, 구매 이유, 배송 정보 및 필요한 승인과 같은 필수 세부 정보를 포함합니다.

![구매 요청](/help/adaptive-forms/assets/Purchase-request-form.png)

## 참조 양식 데이터 모델 {#reference-models}

[코어 구성 요소](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/adaptive-forms/introduction.html)를 기반으로 적응형 양식을 만든 후 양식을 데이터베이스 Microsoft® Dynamics 365 및 Salesforce 서버와 연결하여 비즈니스 워크플로를 활성화할 수 있습니다. 예:

* 적응형 양식 제출 시 Microsoft® Dynamics 365 및 Salesforce에 데이터를 씁니다.
* 양식 데이터 모델에 정의된 사용자 정의 엔티티를 통해 Microsoft® Dynamics 365 및 Salesforce에 데이터를 작성하며 그 반대의 경우도 마찬가지입니다.
* Microsoft® Dynamics 365 및 Salesforce 서버에서 데이터를 쿼리하고 적응형 양식을 미리 채웁니다.
* Microsoft® Dynamics 365 및 Salesforce 서버에서 데이터를 읽습니다.

[참조 콘텐츠 패키지](https://experience.adobe.com/#/downloads/content/software-distribution/en/aemcloud.html?package=/content/software-distribution/en/details.html/content/dam/aemcloud/public/aem-forms-reference-content.ui.content-2.1.0.zip)를 설치하여 다음 양식 데이터 모델을 가져올 수 있습니다.

* Microsoft® Dynamics 365
* Salesforce

이러한 모델 사용에 대한 자세한 내용은 [Microsoft® Dynamics 365 및 Salesforce 클라우드 서비스 구성](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/configure-msdynamics-salesforce.html#configure-dynamics-cloud-service)을 참조하십시오.

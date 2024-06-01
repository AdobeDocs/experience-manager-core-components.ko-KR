---
title: AEM 적응형 Forms의 Captcha
description: hCaptcha&reg; 서비스를 통해 손쉽게 양식 보안을 강화할 수 있습니다. 내부의 단계별 가이드!
feature-set: Experience Manager Sites, Experience Manager Forms
feature: Adaptive Forms, Core Components
role: Architect, Developer, Admin, User
source-git-commit: 08d44e4db42594fb5aaf33d7d42df6fe19c70f59
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 12%

---

# Captcha 구성 요소{#hCaptcha-component-adaptive-forms-core-component}

<span class="preview"> 이 기능은 얼리어답터 프로그램 아래에 있습니다. 공식 이메일 ID에서 aem-forms-ea@adobe.com에 작성하여 얼리어답터 프로그램에 참여하고 기능에 대한 액세스를 요청할 수 있습니다. </span>

Captcha® 서비스는 보트, 스팸 및 자동 남용으로부터 양식을 보호합니다. 확인란 위젯 문제를 제기하고 사용자 응답을 평가하여 양식과 상호 작용하는 사람인지 보트인지를 확인합니다. 테스트가 실패할 경우 사용자가 진행할 수 없도록 막고 봇이 스팸이나 악의적인 활동을 게시하지 않도록 해 온라인 거래를 안전하게 만드는 데 도움을 준다.

![hCaptcha®](/help/adaptive-forms/assets/hCaptcha-challenge.png)

## 사용 {#usage}

양식 제출 프로세스에 hCaptcha 문제를 포함하는 것이 유용한 이유는 다음과 같습니다.

- **보트 방지**: 사람이 양식을 제출하면 스팸 및 자동 제출이 줄어듭니다.

- **보안**: 추가 보안 계층을 추가하여 각 양식 제출의 정당성을 확인하고 악의적인 공격으로부터 보호합니다.

- **데이터 무결성**: 여러 번 또는 부정 제출을 방지하여 양식을 통해 수집된 데이터의 무결성과 정확성을 유지하는 데 도움이 됩니다.

- **사용자 확인**: 양식을 제출하는 사용자의 ID를 확인하여 인증된 사용자만 민감한 트랜잭션을 완료할 수 있도록 합니다.

- **로드 관리**: 양식 제출 속도를 제어하여 트래픽이 많은 기간 동안 시스템 과부하를 방지하여 서버 로드를 관리하는 데 도움이 됩니다.

## 기술 세부 정보 {#technical-details}

의 기술 설명서에서 hCaptcha 구성 요소에 대한 최신 정보를 얻으십시오. [GitHub](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/hCaptcha/v1/hCaptcha/README.md). 핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 확인하십시오.

다음을 사용하여 hCaptcha 구성 요소의 속성을 지정합니다. [구성 대화 상자](#configure-dialog). 구성 대화 상자는 양식을 쉽게 작성하고 복잡한 양식을 효율적으로 만들 수 있도록 빌드된 핵심 구성 요소의 일부입니다.

## 버전 및 호환성 {#version-and-compatibility}


적응형 Forms hCaptcha 구성 요소는 2024년 5월에 의 일부로 출시됩니다. [코어 구성 요소 3.0.20](https://github.com/adobe/aem-core-forms-components/commit/a4cb97131ffad47137a8f5f173401128a1cf3491). 다음 표에서는 지원되는 모든 버전, AEM 호환성 및 해당 문서에 대한 링크를 보여 줍니다.

|  |  |
|---|---|
| 구성 요소 버전 | AEM as a Cloud Service |
| --- | --- |
| v1 | <br>[릴리스 2.0.4](/help/adaptive-forms/version.md) 이상 버전과 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/adaptive-forms/version.md) 문서를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

다양한 속성을 맞춤화하기 위한 기본 탭과 유효성 검사 탭이 있는 구성 대화 상자를 통해 hCaptcha 구성 요소의 속성을 손쉽게 맞춤화할 수 있습니다.

### 기본 탭 {#basic-tab}

- **[!UICONTROL 이름]:** hCaptcha 구성 요소의 이름을 지정하십시오. 양식 및 규칙 편집기에서 고유한 이름으로 양식 구성 요소를 쉽게 식별할 수 있습니다.
- **[!UICONTROL 제목]:** hCaptcha 구성 요소의 제목을 지정합니다.
- **[!UICONTROL 구성 설정]:** hCaptcha®에 대해 구성된 클라우드 구성을 선택합니다.
- **Captcha 크기:** Captcha® 챌린지 대화 상자의 표시 크기를 선택할 수 있습니다. 사용 **[!UICONTROL 콤팩트]** 작은 크기 및 을 표시하는 옵션 **[!UICONTROL 기본]** 비교적 큰 크기의 hCaptcha® 문제 대화 상자를 표시하는 옵션입니다.<!-- or **[!UICONTROL Invisible]** to validate hCaptcha&reg; without explicitly rendering the checkbox widget on the user interface. -->

  ![Captcha 기본 탭](/help/adaptive-forms/assets/hcaptcha-basic.png)

### 유효성 검사 탭 {#validation-tab}

- **[!UICONTROL 유효성 확인 메시지]:** 양식 제출에서 Captcha 유효성 검사에 대한 유효성 검사 메시지를 제공합니다.
- **[!UICONTROL 스크립트 유효성 메시지]** - 스크립트 유효성 검사에 실패한 경우 이 옵션을 사용하여 프롬프트 메시지를 입력합니다.

  ![hCaptcha 유효성 검사 탭](/help/adaptive-forms/assets/hcaptcha-validation-tab.png)

**hCaptcha®는 Intutory Machines, Inc.의 등록 상표입니다.**

**자세히 알아보기** 기타 정보 **Captcha 구성 요소** 및 다음과 같은 서비스:

- [핵심 구성 요소를 위한 적응형 양식에서 hCaptcha 사용](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/integrate-adaptive-forms-hCaptcha-core-components)

- [기초 구성 요소를 위한 적응형 양식에서 hCaptcha 사용](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-hcaptcha)

- [기초 구성 요소를 위한 적응형 양식에서 턴스타일 CAPTCHA 사용](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-turnstile)

- [기초 구성 요소를 위한 적응형 양식에서 Google reCAPTCHA 사용](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/captcha-adaptive-forms-core-components)

## 관련 문서 {#related-articles}

{{more-like-this}}

## 추가 참조 {#see-also}

{{see-also}}
---
title: AEM 적응형 양식의 hCaptcha
description: hCaptcha&reg; 서비스를 통해 손쉽게 양식 보안을 강화할 수 있습니다. 단계별 안내서가 포함되어 있습니다.
feature-set: Experience Manager Sites, Experience Manager Forms
feature: Adaptive Forms, Core Components
role: Architect, Developer, Admin, User
exl-id: eecb38d5-711e-4dc5-bc19-498e003f37e7
source-git-commit: 4b05fb9d8db515289095f4d3c6a4efbe872dbde5
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 100%

---

# hCaptcha 구성 요소{#hCaptcha-component-adaptive-forms-core-component}

<span class="preview"> 이 기능은 얼리 어답터 프로그램에서 제공됩니다. 공식 이메일 ID를 사용하여 aem-forms-ea@adobe.com으로 이메일을 보내 얼리 어답터 프로그램에 참여하고 기능에 대한 액세스 권한을 요청할 수 있습니다. </span>

hCaptcha® 서비스는 봇, 스팸 및 자동화된 남용으로부터 양식을 보호합니다. 확인란 위젯 챌린지를 제기하고 사용자의 답변을 평가하여 양식과 상호 작용하는 것이 인간인지 또는 봇인지 판단합니다. 테스트가 실패할 경우 사용자가 진행하지 못하도록 차단하고 봇이 스팸을 게시하거나 악의적인 활동으로 상호 작용하는 것을 방지하여 온라인 거래를 안전하게 할 수 있도록 도와줍니다.

![hCaptcha®](/help/adaptive-forms/assets/hCaptcha-challenge.png)

## 사용 {#usage}

양식 제출 프로세스에 hCaptcha 챌린지를 포함하는 것이 유익한 몇 가지 이유는 다음과 같습니다.

- **봇 방지**: 사람이 양식을 제출하는지 확인하여 스팸 및 자동화된 제출을 줄입니다.

- **보안**: 추가적인 보안 계층을 추가하여 각 양식 제출의 적격성을 확인하고 악의적인 공격으로부터 보호합니다.

- **데이터 무결성**: 다중 제출 또는 사기성 제출을 방지함으로써 양식을 통해 수집된 데이터의 무결성과 정확성을 유지하는 데 도움이 됩니다.

- **사용자 확인**: 양식을 제출하는 사용자의 신원을 확인하여 인증된 사용자만 민감한 거래를 완료할 수 있도록 합니다.

- **부하 관리**: 양식 제출 속도를 제어하여 트래픽이 많은 기간 동안 시스템 과부하를 방지함으로써 서버의 부하를 관리하는 데 도움이 됩니다.

## 기술 세부 정보 {#technical-details}

hCaptcha 구성 요소에 대한 최신 정보는 [GitHub](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/hCaptcha/v1/hCaptcha/README.md)의 기술 설명서에서 확인할 수 있습니다. 핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 확인하십시오.

[구성 대화 상자](#configure-dialog)를 사용하여 hCaptcha 구성 요소의 속성을 지정합니다. 구성 대화 상자는 양식을 손쉽게 작성할 수 있도록 돕고 복잡한 양식을 만드는 효율적인 방법을 제공하기 위해 빌드된 핵심 구성 요소의 일부입니다.

## 버전 및 호환성 {#version-and-compatibility}


적응형 양식 hCaptcha 구성 요소는 [핵심 구성 요소 3.0.20](https://github.com/adobe/aem-core-forms-components/commit/a4cb97131ffad47137a8f5f173401128a1cf3491)의 일부로 2024년 5월에 릴리스되었습니다. 다음 표에서는 지원되는 모든 버전, AEM 호환성 및 해당 문서에 대한 링크를 보여 줍니다.

|  |  |
|---|---|
| 구성 요소 버전 | AEM as a Cloud Service |
| --- | --- |
| v1 | <br>[릴리스 2.0.4](/help/adaptive-forms/version.md) 이상 버전과 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/adaptive-forms/version.md) 문서를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

다양한 속성을 사용자 정의하기 위한 기본 탭과 유효성 검사 탭이 있는 구성 대화 상자를 사용하여 hCaptcha 구성 요소의 속성을 손쉽게 사용자 정의할 수 있습니다.

### 기본 탭 {#basic-tab}

- **[!UICONTROL 이름]:** hCaptcha 구성 요소의 이름을 지정합니다. 양식과 규칙 편집기 모두에서 고유한 이름으로 양식 구성 요소를 손쉽게 식별할 수 있습니다.
- **[!UICONTROL 제목]:** hCaptcha 구성 요소의 제목을 지정합니다.
- **[!UICONTROL 구성 설정]:** hCaptcha®용으로 구성된 클라우드 구성을 선택합니다.
- **Captcha 크기:** hCaptcha® 챌린지 대화 상자의 표시 크기를 선택할 수 있습니다. 작은 크기로 표시하려면 **[!UICONTROL 소형]** 옵션을 사용하고 상대적으로 큰 크기의 hCaptcha® 챌린지 대화 상자를 표시하려면 **[!UICONTROL 보통]** 옵션을 사용하십시오.<!-- or **[!UICONTROL Invisible]** to validate hCaptcha&reg; without explicitly rendering the checkbox widget on the user interface. -->

  ![hCaptcha 기본 탭](/help/adaptive-forms/assets/hcaptcha-basic.png)

### 유효성 검사 탭 {#validation-tab}

- **[!UICONTROL 유효성 검사 메시지]:** 양식 제출 시 Captcha 유효성 검사를 위한 확인 메시지를 제공합니다.
- **[!UICONTROL 스크립트 유효성 검사 메시지]** - 스크립트 유효성 검사가 실패할 경우 이 옵션을 사용하여 메시지를 입력할 수 있습니다.

  ![hCaptcha 유효성 검사 탭](/help/adaptive-forms/assets/hcaptcha-validation-tab.png)

**hCaptcha®는 Intuition Machines, Inc.의 등록 상표입니다.**

다음과 같은 기타 **Captcha 구성 요소** 및 해당 서비스에 대해 **자세히** 알아보십시오.

- [핵심 구성 요소에 대한 적응형 양식에서의 hCaptcha 사용](https://experienceleague.adobe.com/kr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/integrate-adaptive-forms-hCaptcha-core-components)

- [기초 구성 요소에 대한 적응형 양식에서의 hCaptcha 사용](https://experienceleague.adobe.com/kr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-hcaptcha)

- [기초 구성 요소에 대한 적응형 양식에서의 Turnstile CAPTCHA 사용](https://experienceleague.adobe.com/kr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-turnstile)

- [기초 구성 요소에 대한 적응형 양식에서의 Google reCAPTCHA 사용](https://experienceleague.adobe.com/kr/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/captcha-adaptive-forms-core-components)

## 관련 문서 {#related-articles}

{{more-like-this}}

## 추가 참조 {#see-also}

{{see-also}}

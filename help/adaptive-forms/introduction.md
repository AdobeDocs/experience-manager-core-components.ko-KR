---
title: AEM 적응형 양식 핵심 구성 요소 소개
description: 적응형 양식 핵심 구성 요소의 유연성을 사용하여 매력적인 등록 경험(양식)을 만들고 Adobe Experience Manager의 강력한 기능으로 전달하십시오.
role: Architect, Developer, Admin, User
exl-id: 6d0f2845-bbb8-4488-a254-b69d7a6290b1
source-git-commit: 12a829c164839fdcb2c98d52e409ec3ac2079c41
workflow-type: tm+mt
source-wordcount: '2123'
ht-degree: 100%

---

# 적응형 양식 핵심 구성 요소  {#adaptive-forms-core-components-introduction}

Adobe Experience Manager의 적응형 양식 핵심 구성 요소를 사용하면 매력적인 등록 경험을 만들 수 있습니다.

## 핵심 구성 요소 {#overview}

Adobe Experience Manager(AEM)에서 구성 요소는 페이지와 양식을 작성하는 데 사용되는 빌딩 블록입니다. 작성자가 콘텐츠를 만들고 관리할 수 있는 간단하고 강력한 방법을 제공하는 동시에 개발자에게 사용자 정의 구성 요소를 만드는 데 필요한 유연성과 확장성을 제공합니다. 이는 개발을 가속화하고 웹 사이트 및 양식의 유지 관리 비용을 절감하도록 설계되었으며, 유연하고 웹 사이트 및 양식의 특정 요구 사항에 맞게 쉽게 사용자 정의할 수 있습니다.

또한 핵심 구성 요소는 응답성이 뛰어나며 데스크탑, 태블릿 및 스마트폰을 포함한 다양한 디바이스를 지원하도록 설계되었습니다. 최신 웹 표준 및 모범 사례를 준수하여 강력하고 신뢰할 수 있는 웹 콘텐츠 제작 솔루션이기도 합니다.

전반적으로 핵심 구성 요소는 AEM에서 웹 콘텐츠를 만들고 관리하기 위한 필수 도구이며, 개발 시간과 유지 관리 비용을 줄이는 데 도움이 되는 강력하고 유연한 솔루션을 제공하는 동시에 웹 사이트 방문자에게 훌륭한 사용자 경험을 제공합니다.

## 적응형 양식 핵심 구성 요소

적응형 양식 핵심 구성 요소는 Adobe Experience Manager WCM 핵심 구성 요소를 기반으로 구축된 30개의 오픈 소스 BEM 호환 구성 요소 세트입니다. 사용자의 디바이스, 브라우저 및 화면 크기에 맞춰 조정되는 양식인 적응형 양식을 만드는 데 사용하도록 특별히 설계되었습니다.

이러한 구성 요소를 사용하면 텍스트 필드, 확인란, 드롭다운 메뉴 등을 포함한 다양한 양식 필드 옵션을 제공하여 탁월한 데이터 캡처 및 등록 경험을 만들 수 있습니다. 또한 여기에는 사용자 친화적이고 사용하기 쉬운 양식을 만드는 데 사용할 수 있는 유효성 검사, 조건부 논리 및 반응형 디자인과 같은 기능이 포함되어 있습니다.

이와 더불어 이러한 구성 요소는 오픈 소스이므로 개발자가 조직의 특정 요구 사항에 맞게 구성 요소를 쉽게 사용자 정의하고 확장할 수 있습니다. 그리고 이러한 구성 요소는 BEM 방법론을 기반으로 구축되어 있으므로 확장 및 유지 관리가 가능합니다.

![적응형 양식 이미지](assets/sample-adaptive-form.png)

## 기능 {#features}

|  |  |
|---|---|
| 제작 준비 | 반응형 양식 핵심 구성 요소는 24개의 강력한 WCM 구성 요소입니다. |
| 클라우드 기반 | [AEM Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/home.html?lang=ko)에 사용할 수 있습니다. |
| 유연성 | 구성 요소는 양식 작성자가 거의 모든 레이아웃을 조합할 수 있는 일반적인 개념을 나타냅니다. |
| 구성 가능 | 템플릿 수준의 [콘텐츠 정책](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html?lang=ko#content-policies)은 사용하거나 사용할 수 없는 기능이 무엇인지 정의합니다. |
| 액세스 가능 | ARIA 레이블을 제공하고, 키보드 탐색을 지원하며, 화면 판독기와 같은 보조 기술용 텍스트를 제공합니다. |
| 테마 적용 가능 | 구성 요소는 [스타일 시스템](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=ko)을 구현하고 마크업이 [BEM CSS 명명](https://getbem.com/)을 따릅니다 |
| 사용자 정의 가능 | 몇 가지 패턴을 사용하여 HTML 조정부터 고급 기능 재사용까지 간편한 맞춤화를 구현할 수 있습니다. |
| 버전 관리 | [버전 관리 정책](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies)을 사용하여 몇 가지 개선 사항을 수정하면 사이트는 핵심 구성 요소에 의해 연결이 끊기지 않습니다. |
| 오픈 소스 | 매출이 평소와 같지 않다면 자신의 성과를 공개하십시오. |

<!-- comply with [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), -->


## 이점 {#benefits}

데이터 캡처 경험은 리드 생성 및 등록에 매우 중요하며 적응형 양식 핵심 구성 요소는 데이터 캡처에 최적화된 양식을 만들기 위한 강력한 솔루션을 제공합니다. 핵심 구성 요소를 사용하여 기초 구성 요소에 대한 이러한 경험을 만드는 데에는 다음과 같은 몇 가지 이유가 있습니다.

* **[GitHub에서의 가용성](https://github.com/adobe/aem-core-forms-components)**: AEM 적응형 양식 핵심 구성 요소는 오픈 소스이며 포괄적인 설명서와 함께 GitHub에서 사용할 수 있습니다. 이를 통해 개발자는 구성 요소와 작동 방식을 보다 쉽게 이해할 수 있을 뿐만 아니라 개발에 기여할 수 있습니다. 개발자가 작동 중인 구성 요소를 확인하고 자세한 설명서에 액세스할 수 있는 유용한 리소스인 [emcomponents.dev](https://www.aemcomponents.dev/) 웹 사이트도 있습니다.

* **[스타일링용 BEM 모델](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components)**: 핵심 구성 요소는 CSS를 구성하기 위해 잘 정립되고 널리 사용되는 방법론인 스타일링용 BEM(블록 요소 수정자) 모델을 따릅니다. 이를 통해 개발자가 스타일을 구성하는 방법과 특정 요구 사항에 맞게 스타일을 수정하는 방법을 보다 쉽게 이해할 수 있습니다.

* **서드파티 라이브러리에 대한 종속성 없음**: 핵심 구성 요소의 장점 중 하나는 JQuery 및 Underscore를 비롯한 서드파티 JavaScript 라이브러리에 종속되지 않는다는 점입니다. 이를 통해 구성 요소가 더 빠르고 가벼워질 뿐만 아니라 기존 AEM 구현에 쉽게 통합될 수 있습니다.

* **성능 및 접근성에 대한 포커스**: 핵심 구성 요소는 성능과 접근성을 염두에 두고 구축되었으며, 이는 높은 Google Lighthouse 및 웹 바이탈 점수에 반영됩니다. 이를 통해 개발자는 오늘날의 디지털 환경에서 점점 더 중요해지고 있는 접근성이 뛰어난 고성능 웹 페이지를 보다 쉽게 만들 수 있습니다.

* **Sites 30 템플릿 및 테마의 양식 구성 요소**: 핵심 구성 요소는 Sites 30 템플릿 및 테마의 양식 구성 요소를 지원하므로 개발자가 AEM 내에서 양식을 보다 쉽게 만들고 사용자 정의할 수 있습니다.

* **[스타일링 용이성](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/using-themes-in-core-components)**: 핵심 구성 요소는 기초 구성 요소보다 스타일링이 더 쉽습니다. 테마 생성 프로세스는 Sites와 유사하며 상위 Sites 페이지에서 동일한 테마/CSS를 상속할 수 있습니다. 또한 스타일링용 BEM 모델을 사용하면 스타일을 보다 쉽게 이해하고 수정할 수 있습니다.

* **접근성**: 적응형 양식 핵심 구성 요소는 접근성 표준 및 지침을 지원하여 화면 판독기와 같은 보조 기술을 사용하는 사용자를 포함하여 장애를 가진 사용자도 양식을 사용할 수 있도록 합니다.

* **[버전 관리](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/add-comments-annotations-versioning-adaptive-form-core-components)**: 핵심 구성 요소 기반 적응형 양식의 여러 버전을 만들고 관리하고, 주석을 통해 공동 작업 토론에 참여하고, 특정 양식 구성 요소에 주석을 첨부하여 전반적인 양식 작성 경험을 향상할 수 있습니다.

## 사용 가능한 구성 요소: 구성 요소 유형별 분류

AEM Forms의 현재 버전에는 다음과 같은 핵심 구성 요소, [기초 구성 요소](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/create-an-adaptive-form-on-forms-cs/introduction-forms-authoring#component-toolbar) 및 [양식 블록 구성 요소(Edge Delivery Services)](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/edge-delivery/build-forms/forms-references/form-components)가 있습니다.

| 구성 요소 | 기초 구성 요소 | 핵심 구성 요소 | 양식 블록 구성 요소 | 추가 정보 |
|------------|:---------------------:|:---------------:|:---------------------:|-----------------------|
| Adobe Sign 차단 | ✔️ | | | [Adobe Sign 통합](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/forms/integrate/services/adobe-sign-integration-adaptive-forms#adobe-acrobat-sign-for-government)은 기초 구성 요소에만 사용할 수 있습니다. |
| 아코디언 | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/accordion.md)</span> | | 기초 구성 요소의 경우 [패널 구성 요소 속성](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-layout-of-an-adaptive-form/layout-capabilities-adaptive-forms#panel-layout)에서 아코디언 레이아웃을 구성할 수 있습니다. |
| 적응형 양식 조각 | ✔️ | ✔️ | | 기초 구성 요소의 경우 자산 브라우저에서 [조각을 추가](https://experienceleague.adobe.com/ko/docs/experience-manager-65/content/forms/adaptive-forms-basic-authoring/adaptive-form-fragments#insert-a-fragment-in-an-adaptive-form)할 수 있습니다. |
| 적응형 양식 reCAPTCHA | ✔️ | ✔️ | ✔️ | 기초 구성 요소의 경우 Captcha 구성 요소를 사용하여 [양식에 Google reCaptcha를 추가](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/captcha-adaptive-forms#google-reCAPTCHA)합니다. |
| 버튼 | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/button.md)</span> | ✔️ | |
| 차트 | ✔️ | | | |
| 확인란 | ✔️ | ✔️ | | |
| 확인란 그룹 | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/checkbox-group.md)</span> | ✔️ | 기초 구성 요소의 경우 확인란 구성 요소를 사용하여 여러 확인란을 추가합니다. |
| 데이터 입력 필드 | ✔️ | | | 핵심 구성 요소의 경우 [날짜 선택기](/help/adaptive-forms/components/date-picker.md) 구성 요소를 사용합니다. 별도의 [텍스트 상자](/help/adaptive-forms/components/text-box.md) 또는 [숫자 상자](/help/adaptive-forms/components/numeric-box.md) 구성 요소를 추가하여 일, 월 및 연도를 캡처할 수도 있습니다. |
| 날짜 선택기 | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/date-picker.md)</span> | ✔️ | |
| 드롭다운 목록 | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/drop-down-list.md)</span> | ✔️ | |
| 이메일 | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/email.md)</span> | ✔️ | |
| 첨부 파일 | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/file-attachment.md)</span> | ✔️ | |
| 첨부 파일 나열 | ✔️ | | | |
| 바닥글 | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/footer.md)</span> | ✔️ | |
| 각주 플레이스홀더 | ✔️ | | | |
| 양식 컨테이너 | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/form-container.md)</span> | ✔️ | 기초 구성 요소의 경우 [루트 패널 구성 요소](https://experienceleague.adobe.com/ko/docs/experience-manager-learn/cloud-service/forms/create-first-af/configure-root-panel)를 사용합니다. |
| 양식 제목 | ✔️ | ✔️ | | 기초 구성 요소의 경우 제목 구성 요소를 사용합니다. |
| hCaptcha | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/hcaptcha.md)</span> |  | 기초 구성 요소의 경우, 기초 구성 요소 기반 양식에 대해 [적응형 양식을 hCaptcha와 연결](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-turnstile.html)할 수 있습니다. |
| 헤더 | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/header.md)</span> | ✔️ | |
| 가로 탭 | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/horizontal-tabs.md)</span> | | 기초 구성 요소의 경우 패널 구성 요소 속성에서 [상단 탭(가로 탭) 레이아웃](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-layout-of-an-adaptive-form/layout-capabilities-adaptive-forms#panel-layout)을 구성할 수 있습니다. |
| 이미지 | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/image.md)</span> | ✔️ | |
| 다음 버튼 | ✔️ | ✔️ | | 여러 패널 사이를 이동하려면 다음 및 이전 버튼에 대해 [마법사 구성 요소](/help/adaptive-forms/components/wizard.md)를 사용합니다. |
| 숫자 상자 | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/numeric-box.md)</span> | ✔️ | |
| 숫자 스텝퍼 | ✔️ | | | |
| 패널 | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/panel.md)</span> | ✔️ | |
| 전화 | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/phone.md)</span> | ✔️ | |
| 이전 버튼 | ✔️ | ✔️ | | 여러 패널 사이를 이동하려면 다음 및 이전 버튼에 대해 [마법사 구성 요소](/help/adaptive-forms/components/wizard.md)를 사용합니다. |
| 라디오 버튼 그룹 | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/radio-button.md)</span> | ✔️ | |
| 재설정 버튼 | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/reset-button.md)</span> | ✔️ | |
| 검토 |  | <span style="color:blue">[✔️](/help/adaptive-forms/components/reset-button.md)</span> |  | |
| 낙서 서명 | ✔️ | | | |
| 구분자 | ✔️ | | | WCM [구분자](/help/components/separator.md) 구성 요소 사용 |
| 제출 버튼 | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/submit-button.md)</span> | ✔️ | |
| 요약 단계 | ✔️ | | | |
| 전환 | ✔️ | <span style="color:blue"> [✔️](/help/adaptive-forms/components/adaptive-form-switch.md) | | |
| 테이블 | ✔️ | | | |
| 약관 | ✔️ | ✔️ | | |
| 텍스트 | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/text.md)</span> | ✔️ | |
| 텍스트 상자 | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/text-box.md)</span> | ✔️ | |
| Turnstile Captcha | ✔️ | | | [Turnstile Captcha](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/add-components-to-an-adaptive-form/integrate-adaptive-forms-turnstile)는 기초 구성 요소에만 사용할 수 있습니다. |
| 세로 탭 | ✔️ | ✔️ | | 기초 구성 요소의 경우 패널 구성 요소 속성에서 [왼쪽 탭(세로 탭) 레이아웃](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-layout-of-an-adaptive-form/layout-capabilities-adaptive-forms#panel-layout)을 구성할 수 있습니다. |
| 마법사 | ✔️ | <span style="color:blue">[✔️](/help/adaptive-forms/components/wizard.md)</span> | ✔️ | 기초 구성 요소의 경우 패널 구성 요소 속성에서 [마법사 레이아웃](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-layout-of-an-adaptive-form/layout-capabilities-adaptive-forms#panel-layout)을 구성할 수 있습니다. |

<!--| Password Box | ✔️ | ✔️| ✔️ | |
| Image Choice | ✔️ | | | |
-->


>[!NOTE]
>
>
> * 위에 나열된 구성 요소 외에도 양식 블록은 모든 유효한 [HTML5 입력 유형](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#input_types) 및 [텍스트 영역](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/textarea)을 구성 요소로 지원합니다.
> * 위에 나열되지 않은 구성 요소가 필요하십니까? 공식 주소에서 aem-forms-ea@adobe.com으로 이메일을 보내 요청하십시오.


<!-- >
* [Accordion](/help/adaptive-forms/components/accordion.md)
* [Adaptive Form Fragment](/help/adaptive-forms/components/adaptive-form-fragment.md)
* [Adaptive Form Switch](/help/adaptive-forms/components/adaptive-form-switch.md)
* [Button](/help/adaptive-forms/components/button.md)
* [Check Box Group](/help/adaptive-forms/components/checkbox-group.md)
* [Date Picker](/help/adaptive-forms/components/date-picker.md)
* [Drop-down list](/help/adaptive-forms/components/drop-down-list.md)
* [Email](/help/adaptive-forms/components/email.md)
* [Form Container](/help/adaptive-forms/components/form-container.md)
* [File Attachment](/help/adaptive-forms/components/file-attachment.md)
* [Footer](/help/adaptive-forms/components/footer.md)
* [Header](/help/adaptive-forms/components/header.md)
* [Horizontal Tabs](/help/adaptive-forms/components/horizontal-tabs.md)
* [Image](/help/adaptive-forms/components/image.md)
* [Numeric Box](/help/adaptive-forms/components/numeric-box.md)
* [Panel](/help/adaptive-forms/components/panel.md)
* [Phone](/help/adaptive-forms/components/phone.md)
* [Radio Button](/help/adaptive-forms/components/radio-button.md)
* [Adaptive Form reCAPTCHA](/help/adaptive-forms/components/adaptive-form-recaptcha.md)
* [Reset Button](/help/adaptive-forms/components/reset-button.md)
* [Submit Button](/help/adaptive-forms/components/submit-button.md)
* [Text Box](/help/adaptive-forms/components/text-box.md)
* [Text](/help/adaptive-forms/components/text.md)
* [Form Title](/help/adaptive-forms/components/form-title.md)
* [Wizard](/help/adaptive-forms/components/wizard.md)

-->

## 사용하기 쉬운 양식 편집기

핵심 구성 요소 기반 적응형 양식용 편집기는 AEM Sites 페이지를 만드는 데 이미 사용하는 것과 유사합니다. 이점은 다음과 같습니다.


* **친숙한 UI 요소 및 설정**: 양식 구성 요소에 대한 속성을 구성할 때 WCM 핵심 구성 요소에 사용하는 것과 동일한 속성 대화 상자가 표시됩니다. 덕분에 필요한 옵션을 더 빨리 찾을 수 있습니다. WCM 핵심 구성 요소와 마찬가지로 양식 구성 요소의 경우 기본 및 고급 옵션, 도움말 텍스트 및 접근성 정보를 구분하는 명확한 탭과 함께 편집기 중앙에 속성 대화 상자가 표시되며, 모두 쉽게 탐색할 수 있도록 탭 형식을 취합니다.

* **[규칙 편집기](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/rule-editor-core-components)**: 코드를 작성하지 않고도 양식에 로직 및 동적 기능을 추가할 수 있습니다. 기본 제공 규칙 편집기를 사용하여 다음과 같은 작업을 수행할 수 있습니다.
   * 사용자 선택에 따라 필드 표시 또는 숨기기
   * 오브젝트 활성화 또는 비활성화
   * 오브젝트의 값 설정
   * 계산 수행
   * 오브젝트의 속성 설정
   * 데이터 입력 유효성 검사
   * 서비스 호출 (외부 기능 호출)
   * 기본 제공 기능 사용 (일반 작업을 위해 사전 정의된 기능)
   * 사용자 정의 기능 사용 (특정 요구에 맞는 자체 코드)
   * 필드 및 패널 유효성 검사 (데이터가 요구 사항을 충족하는지 확인)
   * 오브젝트 값의 유효성 검사
   * 오브젝트의 값을 계산하는 함수 실행
   * 양식 데이터 모델(FDM) 서비스 호출 및 작업 수행
   * 동적으로 스타일 추가 (조건에 따라 모양 변경)
   * 다른 규칙 만들기 (체인 작업 및 로직)
   * 이 외에도 다양한 내용이 있습니다!

  규칙 편집기에는 코드 편집기가 없습니다. [사용자 정의 함수](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-and-use-custom-functions)를 사용하여 규칙 편집기에 특정 요구 사항에 맞는 자체 코드를 추가할 수 있습니다.



* **양식 사전 채우기**: 사용자가 양식을 열 때 양식의 특정 필드를 기존 데이터로 자동으로 채울 수 있습니다. 덕분에 이미 확인된 정보를 수동으로 입력할 필요가 없으므로 사용자의 시간과 노력이 절약됩니다. 핵심 구성 요소 편집기는 양식 데이터 모델의 도움으로 양식 필드를 채우는 OOTB 사전 채우기 서비스를 제공합니다. 더 복잡한 시나리오를 위해 사용자 정의 사전 채우기 서비스를 만들 수도 있습니다.

* **[기록 문서(DoR)](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/generate-document-of-record-core-components)**: 기록 문서(DoR)는 양식을 통해 제출된 데이터의 인쇄 가능한 공식 형태입니다. 사용자가 입력한 정보의 영구 기록 역할을 하며, 제출된 데이터의 스냅샷을 사용자에게 친숙한 형식(일반적으로 PDF 문서)으로 제공합니다. 편집기를 사용하여 사용자 정의 템플릿을 쉽게 구성하거나 OOTB 템플릿을 사용하여 DoR을 생성할 수 있습니다.

* **[양식 데이터 모델](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/using-form-data-model)**: 적응형 양식 데이터 모델(FDM)은 적응형 양식과 데이터 소스 간의 브리지 역할을 합니다. 기본적으로 양식이 수집하고 상호 작용하는 데이터의 구조와 구성을 정의합니다. 편집기를 사용하여 양식을 양식 데이터 모델(FDM)과 쉽게 연결할 수 있습니다.

* **[양식 제출](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Adaptive%20Form%20Submit%20Action&amp;text=Adobe%20recommends%20using%20Core%20Components,to%20create%20standalone%20Adaptive%20Forms.&amp;text=A%20Submit%20Action%20lets%20you,button%20on%20an%20Adaptive%20Form)**: 양식 제출은 사용자가 작성한 양식을 완료하고 전송하는 프로세스를 의미합니다. 양식 구성 내에 정의된 일련의 작업을 트리거하여, 궁극적으로 제출된 데이터의 저장 또는 처리로 이어집니다. 적응형 양식 편집기는 양식 제출 구성을 위한 다양한 옵션을 제공합니다. 일반적인 제출 작업으로는 다음이 있습니다.

   * [이메일 보내기](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Adaptive%20Form%20Submit%20Action&amp;text=Adobe%20recommends%20using%20Core%20Components,to%20create%20standalone%20Adaptive%20Forms.&amp;text=A%20Submit%20Action%20lets%20you,button%20on%20an%20Adaptive%20Form.)
   * [Power Automate 플로우 호출](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/forms/integrate/services/forms-microsoft-power-automate-integration)
   * [SharePoint에 제출](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-action-sharepoint)
   * [Workfront Fusion 호출](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Invoke%20a%20Workfront%20Fusion)
   * [양식 데이터 모델(FDM)을 사용하여 제출](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/forms/integrate/use-form-data-model/using-form-data-model)
   * [Azure Blob 스토리지에 제출](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Submit%20to%20Azure%20Blob%20Storage)
   * [REST 엔드포인트에 제출](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-action-restpoint)
   * [OneDrive에 제출](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=to%20REST%20endpoint-,Submit%20to%20OneDrive,-Invoke%20an%20AEM)
   * [AEM Workflow 호출](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/configure-submit-actions-core-components#:~:text=Invoke%20an%20AEM%20Workflow)


* [Sites 페이지 편집기의 적응형 양식 핵심 구성 요소](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page): AEM 페이지 편집기 및 AEM 경험 조각에서 적응형 양식 핵심 구성 요소를 활성화하고 사용하여 Sites 페이지 구축과 함께 데이터 캡처 환경을 직접 만들 수 있습니다.

  >[!VIDEO](https://video.tv.adobe.com/v/3419284?quality=12&learn=on)


<!-- 
* **Preview Forms**: You can use the editor to  simulates how the form would appear on various devices like desktops, tablets, and smartphones.
-->



## 적응형 양식 핵심 구성 요소 활성화

AEM Forms as a Cloud Service에서 적응형 양식 핵심 구성 요소를 활성화하면 여러 채널에 AEM Forms Cloud Service 인스턴스를 사용하여 핵심 구성 요소 기반 적응형 양식 및 Headless 양식을 만들고, 게시하고, 게재할 수 있습니다. 적응형 양식 핵심 구성 요소 활성화를 위한 자세한 지침은 [AEM Forms as a Cloud Service 및 로컬 개발 환경에서 적응형 양식 핵심 구성 요소 활성화](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/enable-adaptive-forms-core-components.html?lang=ko)를 참조하십시오.

적응형 양식 핵심 구성 요소에는 다음과 같은 요구 사항이 있습니다.

| AEM 버전 | AEM Forms 추가 기능 | 적응형 양식 핵심 구성 요소 |
|---|---|---|
| AEM as a Cloud Service | Forms - 디지털 등록 | [릴리스 2.0.10](version.md)+ |
| AEM 6.5 | Forms 추가 기능 | [릴리스 1.1.12](version.md)+ |

적응형 양식 핵심 구성 요소는 2023.02.0 릴리스 이전의 프리릴리스 일부로 제공되었으므로 사용 중인 AEM Cloud Service SDK 버전이 2023.02.0 이전 버전이라면 [해당 환경에서 `prerelease` 플래그가 활성화](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html?lang=ko#new-features)되어 있어야 합니다.


## 핵심 구성 요소 기반 적응형 양식 만들기

AEM Forms as a Cloud Service 또는 AEM 6.5 Forms 환경 모두에서 다음 작업을 수행할 수 있습니다.

| 작업 | AEM Forms 버전 |
|--------|------------------|
| 독립 적응형 양식 만들기 | [AEM Forms as Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=ko) |
| AEM Sites 페이지에서 적응형 양식 만들기 | [AEM 6.5 Forms](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-basic-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=ko#create-an-adaptive-form-in-sites-editor-or-experience-fragment), [AEM Forms as Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=ko#create-an-adaptive-form-in-sites-editor-or-experience-fragment) |
| AEM 경험 조각에서 적응형 양식 만들기 | [AEM 6.5 Forms](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-basic-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=ko#create-an-adaptive-form-in-experience-fragment), [AEM Forms as Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=ko#create-an-adaptive-form-in-experience-fragment) |
| 적응형 양식을 경험 조각으로 변환 | [AEM 6.5 Forms](https://experienceleague.adobe.com/docs/experience-manager-65/forms/adaptive-forms-basic-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=ko#convert-an-adaptive-form-in-sites-page-to-an-experience-fragment), [AEM Forms as Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=ko#convert-an-adaptive-form-in-sites-page-to-an-experience-fragment) |





<!-- >, such as  [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), to ensure that forms can be used by people with disabilities, including those using assistive technologies such as screen readers.

*   **Alignment with AEM Sites**: The Core Components are designed to be more aligned with AEM Sites, making it easier for Sites users to adopt and use them without having to learn anything new. The components use the same front-end pipeline as Sites, making it easier to style and modify their appearance. 

<!-- Additionally, the following points further illustrate this alignment:

    *   **Authoring experience inline with Page editor**: The Core Components have an authoring experience that is inline with the Sites editor, with dialogs and other experiences similar to the Page editor. This makes it easier for Sites users to create and manage forms within the familiar context of the Sites editor.

    *   **Inline form editing in Sites editor**: The Core Components allow  inline form editing within the Sites editor, avoiding the need to switch back and forth between editors. This streamlines the authoring experience and makes it easier to create and manage forms.

    *   **Inheriting Sites features in Forms**: Forms authored within a Sites page inherit the same features as Sites. This provides a seamless and integrated experience for creating and managing forms within the context of AEM Sites 
    
    <!--including Multi Site Manager, the ability to use Sites components within a form for static content, support for scheduled publish/unpublish, form translation aligned with Sites translation, versioning, and targeting -->

## 추가 참조 {#see-also}

{{see-also}}

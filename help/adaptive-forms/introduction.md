---
title: AEM 적응형 양식 핵심 구성 요소 소개
description: 적응형 양식 핵심 구성 요소의 유연성을 사용하여 매력적인 등록 경험(양식)을 만들고 Adobe Experience Manager의 강력한 기능으로 전달하십시오.
role: Architect, Developer, Admin, User
exl-id: 6d0f2845-bbb8-4488-a254-b69d7a6290b1
source-git-commit: a450d265d10984b879fcb1ad4ffe0f3ce3edef5b
workflow-type: tm+mt
source-wordcount: '1147'
ht-degree: 100%

---

# 적응형 양식 핵심 구성 요소 소개 {#adaptive-forms-core-components-introduction}

Adobe Experience Manager의 적응형 양식 핵심 구성 요소를 사용하면 유연성과 사용 가능한 맞춤화 옵션을 활용하여 매력적인 등록 경험을 만들 수 있습니다.

## 핵심 구성 요소  {#overview}

Adobe Experience Manager(AEM)에서 구성 요소는 페이지와 양식을 작성하는 데 사용되는 빌딩 블록입니다. 작성자가 콘텐츠를 만들고 관리할 수 있는 간단하고 강력한 방법을 제공하는 동시에 개발자에게 사용자 정의 구성 요소를 만드는 데 필요한 유연성과 확장성을 제공합니다. 이는 개발을 가속화하고 웹 사이트 및 양식의 유지 관리 비용을 절감하도록 설계되었으며, 유연하고 웹 사이트 및 양식의 특정 요구 사항에 맞게 쉽게 사용자 정의할 수 있습니다.

또한 핵심 구성 요소는 응답성이 뛰어나며 데스크탑, 태블릿 및 스마트폰을 포함한 다양한 디바이스를 지원하도록 설계되었습니다. 최신 웹 표준 및 모범 사례를 준수하여 강력하고 신뢰할 수 있는 웹 콘텐츠 제작 솔루션이기도 합니다.

전반적으로 핵심 구성 요소는 AEM에서 웹 콘텐츠를 만들고 관리하기 위한 필수 도구이며, 개발 시간과 유지 관리 비용을 줄이는 데 도움이 되는 강력하고 유연한 솔루션을 제공하는 동시에 웹 사이트 방문자에게 훌륭한 사용자 경험을 제공합니다.

## 적응형 양식 핵심 구성 요소

적응형 양식 핵심 구성 요소는 Adobe Experience Manager WCM 핵심 구성 요소를 기반으로 구축된 24개의 오픈 소스 BEM 호환 구성 요소 세트입니다. 사용자의 디바이스, 브라우저 및 화면 크기에 맞춰 조정되는 양식인 적응형 양식을 만드는 데 사용하도록 특별히 설계되었습니다.

이러한 구성 요소를 사용하면 텍스트 필드, 확인란, 드롭다운 메뉴 등을 포함한 다양한 양식 필드 옵션을 제공하여 탁월한 데이터 캡처 및 등록 경험을 만들 수 있습니다. 또한 여기에는 사용자 친화적이고 사용하기 쉬운 양식을 만드는 데 사용할 수 있는 유효성 검사, 조건부 논리 및 반응형 디자인과 같은 기능이 포함되어 있습니다.

이와 더불어 이러한 구성 요소는 오픈 소스이므로 개발자가 조직의 특정 요구 사항에 맞게 구성 요소를 쉽게 사용자 정의하고 확장할 수 있습니다. 그리고 이러한 구성 요소는 BEM 방법론을 기반으로 구축되어 있으므로 확장 및 유지 관리가 가능합니다.

![](assets/sample-adaptive-form.png)

## 기능 {#features}

|  |  |
|---|---|
| 제작 준비 | 반응형 양식 핵심 구성 요소는 24개의 강력한 WCM 구성 요소입니다. |
| 클라우드 기반 | [AEM Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/home.html)에 사용할 수 있습니다. |
| 유연성 | 구성 요소는 양식 작성자가 거의 모든 레이아웃을 조합할 수 있는 일반적인 개념을 나타냅니다. |
| 구성 가능 | 템플릿 수준의 [콘텐츠 정책](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html#content-policies)은 사용하거나 사용할 수 없는 기능이 무엇인지 정의합니다. |
| 액세스 가능 | ARIA 레이블을 제공하고, 키보드 탐색을 지원하며, 화면 판독기와 같은 보조 기술용 텍스트를 제공합니다. |
| 테마 적용 가능 | 구성 요소는 [스타일 시스템](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html)을 구현하고 마크업이 [BEM CSS 명명](https://getbem.com/)을 따릅니다 |
| 사용자 정의 가능 | 몇 가지 패턴을 사용하여 HTML 조정부터 고급 기능 재사용까지 간편한 맞춤화를 구현할 수 있습니다. |
| 버전 관리 | [버전 관리 정책](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies)을 사용하여 몇 가지 개선 사항을 수정하면 사이트는 핵심 구성 요소에 의해 연결이 끊기지 않습니다. |
| 오픈 소스 | 매출이 평소와 같지 않다면 자신의 성과를 공개하십시오. |

<!-- comply with [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), -->


## 이점 {#benefits}

데이터 캡처 경험은 리드 생성 및 등록에 매우 중요하며 적응형 양식 핵심 구성 요소는 데이터 캡처에 최적화된 양식을 만들기 위한 강력한 솔루션을 제공합니다. 핵심 구성 요소를 사용하여 기초 구성 요소에 대한 이러한 경험을 만드는 데에는 다음과 같은 몇 가지 이유가 있습니다.

* **GitHub 및 포괄적인 설명서에 대한 가용성**: AEM 적응형 양식 핵심 구성 요소는 오픈 소스이며 포괄적인 설명서와 함께 GitHub에서 사용할 수 있습니다. 이를 통해 개발자는 구성 요소와 작동 방식을 보다 쉽게 이해할 수 있을 뿐만 아니라 개발에 기여할 수 있습니다. 개발자가 작동 중인 구성 요소를 확인하고 자세한 설명서에 액세스할 수 있는 유용한 리소스인 [emcomponents.dev](https://www.aemcomponents.dev/) 웹 사이트도 있습니다.

* **스타일링용 BEM 모델**: 핵심 구성 요소는 CSS를 구성하기 위해 잘 정립되고 널리 사용되는 방법론인 스타일링용 BEM(블록 요소 수정자) 모델을 따릅니다. 이를 통해 개발자가 스타일을 구성하는 방법과 특정 요구 사항에 맞게 스타일을 수정하는 방법을 보다 쉽게 이해할 수 있습니다.

* **서드파티 라이브러리에 대한 종속성 없음**: 핵심 구성 요소의 장점 중 하나는 JQuery 및 Underscore를 비롯한 서드파티 JavaScript 라이브러리에 종속되지 않는다는 점입니다. 이를 통해 구성 요소가 더 빠르고 가벼워질 뿐만 아니라 기존 AEM 구현에 쉽게 통합될 수 있습니다.

* **성능 및 접근성에 대한 포커스**: 핵심 구성 요소는 성능과 접근성을 염두에 두고 구축되었으며, 이는 높은 Google Lighthouse 및 웹 바이탈 점수에 반영됩니다. 이를 통해 개발자는 오늘날의 디지털 환경에서 점점 더 중요해지고 있는 접근성이 뛰어난 고성능 웹 페이지를 보다 쉽게 만들 수 있습니다.

* **Sites 30 템플릿 및 테마의 양식 구성 요소**: 핵심 구성 요소는 Sites 30 템플릿 및 테마의 양식 구성 요소를 지원하므로 개발자가 AEM 내에서 양식을 보다 쉽게 만들고 사용자 정의할 수 있습니다.

* **스타일링 용이성**: 핵심 구성 요소는 기초 구성 요소보다 스타일링이 더 쉽습니다. 테마 생성 프로세스는 Sites와 유사하며 상위 Sites 페이지에서 동일한 테마/CSS를 상속할 수 있습니다. 또한 스타일링용 BEM 모델을 사용하면 스타일을 보다 쉽게 이해하고 수정할 수 있습니다.

* **접근성**: 적응형 양식 핵심 구성 요소는 접근성 표준 및 지침을 지원하여 화면 판독기와 같은 보조 기술을 사용하는 사용자를 포함하여 장애를 가진 사용자도 양식을 사용할 수 있도록 합니다

## 적응형 양식 핵심 구성 요소 {#components}

현재 버전의 적응형 양식 핵심 구성 요소에는 아래 나열된 구성 요소가 포함되어 있습니다.

* [아코디언](/help/adaptive-forms/components/accordion.md)
* [버튼](/help/adaptive-forms/components/button.md)
* [확인란 그룹](/help/adaptive-forms/components/checkbox-group.md)
* [날짜 선택기](/help/adaptive-forms/components/date-picker.md)
* [드롭다운 목록](/help/adaptive-forms/components/drop-down.md)
* [이메일 입력](/help/adaptive-forms/components/email-input.md)
* [양식 컨테이너](/help/adaptive-forms/components/form-container.md)
* [첨부 파일](/help/adaptive-forms/components/file-attachment.md)
* [바닥글](/help/adaptive-forms/components/footer.md)
* [헤더](/help/adaptive-forms/components/header.md)
* [가로 탭](/help/adaptive-forms/components/horizontal-tabs.md)
* [이미지](/help/adaptive-forms/components/image.md)
* [숫자 입력](/help/adaptive-forms/components/number-input.md)
* [패널 컨테이너](/help/adaptive-forms/components/panel-container.md)
* [라디오 버튼](/help/adaptive-forms/components/radio-button.md)
* [재설정 버튼](/help/adaptive-forms/components/reset-button.md)
* [제출 버튼](/help/adaptive-forms/components/submit-button.md)
* [전화번호 입력](/help/adaptive-forms/components/telephone-input.md)
* [텍스트 입력](/help/adaptive-forms/components/text-input.md)
* [텍스트](/help/adaptive-forms/components/text.md)
* [제목](/help/adaptive-forms/components/title.md)
* [마법사](/help/adaptive-forms/components/wizard.md)

## 적응형 양식 핵심 구성 요소 설정

AEM Forms as a Cloud Service에서 적응형 양식 핵심 구성 요소를 활성화하면 여러 채널에 AEM Forms Cloud Service 인스턴스를 사용하여 핵심 구성 요소 기반 적응형 양식 및 Headless 양식을 만들고, 게시하고, 게재할 수 있습니다. 적응형 양식 핵심 구성 요소 활성화를 위한 자세한 지침은 [AEM Forms as a Cloud Service 및 로컬 개발 환경에서 적응형 양식 핵심 구성 요소 활성화](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/enable-adaptive-forms-core-components.html)를 참조하십시오.

적응형 양식 핵심 구성 요소에는 다음과 같은 요구 사항이 있습니다.

| AEM | AEM Forms 추가 기능 | 적응형 양식 핵심 구성 요소 |
|---|---|---|
| AEM as a Cloud Service | Forms - 디지털 등록 | [릴리스 2.0.10](version.md)+ |
| AEM 6.5 | Forms 추가 기능 | [릴리스 1.1.12](version.md)+ |

적응형 양식 핵심 구성 요소는 2023.02.0 릴리스 이전의 프리릴리스 일부로 제공되었으므로 사용 중인 AEM Cloud Service SDK 버전이 2023.02.0 이전 버전이라면 [해당 환경에서 `prerelease` 플래그가 활성화](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html?lang=ko#new-features)되어 있어야 합니다.


### 핵심 구성 요소 기반 적응형 양식 만들기

AEM Forms as a Cloud Service에서 적응형 양식을 만들려면 [적응형 양식 만들기 (핵심 구성 요소)](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?)를 참조하십시오.





<!-- >, such as  [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), to ensure that forms can be used by people with disabilities, including those using assistive technologies such as screen readers.

*   **Alignment with AEM Sites**: The Core Components are designed to be more aligned with AEM Sites, making it easier for Sites users to adopt and use them without having to learn anything new. The components use the same front-end pipeline as Sites, making it easier to style and modify their appearance. 

<!-- Additionally, the following points further illustrate this alignment:

    *   **Authoring experience inline with Page editor**: The Core Components have an authoring experience that is inline with the Sites editor, with dialogs and other experiences similar to the Page editor. This makes it easier for Sites users to create and manage forms within the familiar context of the Sites editor.

    *   **Inline form editing in Sites editor**: The Core Components allow  inline form editing within the Sites editor, avoiding the need to switch back and forth between editors. This streamlines the authoring experience and makes it easier to create and manage forms.

    *   **Inheriting Sites features in Forms**: Forms authored within a Sites page inherit the same features as Sites. This provides a seamless and integrated experience for creating and managing forms within the context of AEM Sites 
    
    <!--including Multi Site Manager, the ability to use Sites components within a form for static content, support for scheduled publish/unpublish, form translation aligned with Sites translation, versioning, and targeting -->

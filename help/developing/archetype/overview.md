---
title: AEM Project Archetype
description: AEM 기반 애플리케이션의 템플릿 역할을 하는 AEM Project Archetype에 대해 알아봅니다.
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 58994726-9b65-4035-9d45-60b745d577bb
source-git-commit: 8940285f4c5e5870b6a135dac674f06e4c1d8b5a
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 56%

---


# AEM Project Archetype {#aem-project-archetype}

AEM Project Archetype은 웹 사이트의 시작점으로 최소한의 우수 사례 기반 Adobe Experience Manager(AEM) 프로젝트를 만드는 Maven 템플릿입니다. 이 설명서에서는 Archetype 및 일반적인 사용의 이점에 대해 간략히 설명합니다. 자세한 기술 지침 및 문서는 Archetype GitHub 저장소에서 찾을 수 있습니다.

>[!TIP]
>
>최신 AEM Project Archetype 및 관련 기술 설명서 [는 GitHub에서 찾을 수 있습니다.](https://github.com/adobe/aem-project-archetype)

## 이 Archetype을 사용하는 이유 {#why-use-the-archetype}

AEM Project Archetype을 사용하여 몇 번의 키 입력만으로 모범 사례 기반 AEM 프로젝트를 빌드할 수 있습니다. Archetype을 사용하여, 결과 프로젝트가 최소화되도록 모든 콘텐츠를 활용하고 맨 위에서 프로젝트를 빌드하고 확장하도록 AEM의 [주요 기능](/help/developing/archetype/using.md#what-you-get)을 모두 구현합니다.

물론 다음과 같은 요소가 많이 있습니다. [성공적인 AEM 프로젝트,](/help/developing/success.md) 그러나 AEM Project Archetype을 사용하는 것은 건전한 기반이며 모든 AEM 프로젝트에 권장됩니다.

## 기능 {#features}

* **모범 관행:** Adobe 권장 최신 모범 사례를 사용하여 Bootstrap으로 사이트를 제작합니다.
* **로우 코드:** 템플릿을 편집하고, 콘텐츠를 제작하고 CSS를 배포하면 사이트 실행이 준비됩니다.
* **클라우드 기반:** 필요한 경우 [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html)를 사용하여 며칠 내에 사이트를 실행하고 간단히 확장 및 관리할 수 있습니다.
* **발송자:** 속도와 보안을 보장하는 [발송자 구성](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/dispatcher.html)만으로 프로젝트를 완료합니다.
* **다중 사이트:** 필요한 경우 Archetype은 [다국어 및 다중 지역 설정](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/msm/overview.html)용 콘텐츠 구조를 생성합니다.
* **핵심 구성 요소:** 작성자는 다목적 [세트의 표준화된 구성 요소](/help/introduction.md)를 사용하여 거의 모든 레이아웃을 제작할 수 있습니다.
* **편집 가능한 템플릿:** 코드 없이 거의 모든 [템플릿을 조합하고](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html) 작성자가 편집할 내용을 정의합니다.
* **반응형 레이아웃:** 템플릿 또는 개별 페이지에서 [정의된 중단점에 대한 요소를 재배치하는 방법](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/get-started/localization.html)을 정의합니다.
* **머리글 및 바닥글:** [구성 요소의 현지화 기능](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/get-started/localization.html)을 사용하여 코드 없이 이를 조합하고 현지화합니다.
* **스타일 시스템:** 작성자가 [다른 스타일을 적용](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/project-archetype/style-system.html)하면 사용자 정의 구성 요소를 빌드하지 마십시오.
* **프론트엔드 빌드:** 프론트엔드 개발자는 [샘플 AEM 페이지 및 빌드 클라이언트 라이브러리](front-end.md) Webpack, TypeScript 및 SASS 포함
* **WebApp 기반:** React 또는 Angular을 사용하는 사이트의 경우 [SPA SDK](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/hybrid/developing.html) 유지하려면 [앱의 컨텍스트 내 작성](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html).
* **Commerce 활성화됨:** 프로젝트에서 [상거래 핵심 구성 요소](https://github.com/adobe/aem-core-cif-components)를 사용하여 [AEM Commerce](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/home.html)와 상거래 솔루션(예: [Magento](https://magento.com/))을 통합하는 경우.
* **예제 코드:** HelloWorld 구성 요소와 샘플 모드, 서블릿, 필터 및 스케줄러 체크아웃.
* **오픈 소스:** 매출이 평소와 같지 않다면 자신의 성과를 [공개](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md)하십시오.

## 추가 참조 {#further-reading}

* **[AEM Project Archetype GitHub](https://github.com/adobe/aem-project-archetype)** - Archetype의 전체 사용 및 기술 세부 정보
* **[Archetype 사용](using.md)** - 프로젝트에서 Archetype을 사용하는 방법과 결과 생성된 모듈에 대한 개요
* **[AEM Project Archetype을 통한 프론트엔드 개발](front-end.md)** - Archetype의 프론트엔드 모듈 사용 방법
* **다음 튜토리얼은 Archetype에 따라 작성됩니다.**
   * **[WKND 사이트](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)** - 새로운 웹 사이트를 시작하는 방법에 대해 알아봅니다.
   * **[WKND 단일 페이지 앱](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)** - AEM에서 완전히 작성할 수 있는 React 또는 Angular 웹 앱을 빌드하는 방법을 알아봅니다.

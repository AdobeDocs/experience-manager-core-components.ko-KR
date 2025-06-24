---
title: 핵심 구성 요소 소개
description: 핵심 구성 요소와 관련된 문제에 대한 해결책을 구하고 다른 구성 요소가 AEM 내에서 작성되도록 허용합니다.
role: Architect, Developer, Admin, User
exl-id: d294db22-4cb0-48a4-9366-03fda5b8bb8e
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: tm+mt
source-wordcount: '816'
ht-degree: 100%

---


# 핵심 구성 요소 소개{#core-components-introduction}

{{traditional-aem}}

Adobe Experience Manager에서 구성 요소는 작성 중인 페이지의 콘텐츠를 구성하는 구조적 요소입니다. 구성 요소는 항상 AEM 경험의 기본 요소로, 이를 통해 작성자는 간단하지만 강력한 페이지를 만들 수 있고 개발자는 유연하고 확장 가능한 구성 요소를 개발할 수 있습니다.

핵심 구성 요소는 AEM에서 개발 시간을 가속화고 웹 사이트의 유지 관리 비용을 절감할 수 있는 표준화된 웹 콘텐츠 관리(WCM) 구성 요소입니다.

## 리소스 {#resources}

* **[구성 요소 라이브러리:](https://www.adobe.com/kr/go/aem_cmp_library)** 다양한 구성으로 구성 요소를 확인할 수 있는 예제 컬렉션
* **구성 요소 설명서(본 문서):** 개발자 및 작성자용 (각 구성 요소에 대한 세부 정보 포함)
* **[핵심 구성 요소 GitHub 저장소:](https://github.com/adobe/aem-core-wcm-components)** 개발자용 (각 구성 요소에 대한 세부 정보 및 프로젝트 다운로드 포함)
* 시작하기:
   * **[핵심 구성 요소로 성공하기:](/help/developing/success.md)** 핵심 구성 요소를 사용할 프로젝트를 시작하기 전 충분히 고려해야 할 가이드라인
   * **[WKND 튜토리얼:](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html?lang=ko)** 2일간 진행되는 신규 사이트 구축 튜토리얼
   * **[서밋 튜토리얼:](https://expleague.azureedge.net/labs/L767/index.html)** 2시간 동안 진행되는 신규 사이트 구축 튜토리얼 (출처: 2019년 US Summit 랩)
   * **[Gems 웨비나:](https://helpx.adobe.com/kr/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)** 핵심 구성 요소 둘러보기 (2018년 12월 녹화분)

## 기능 {#features}

|  |  |
|---|---|
| 제작 준비 | 핵심 구성 요소는 충분한 테스트를 받고, 용도가 다양하고 성능이 탁월한 30개의 강력한 WCM 구성 요소입니다. |
| 클라우드 기반 | [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html?lang=ko), [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) 또는 온프레미스 등 어디에 있든 작동합니다. |
| 유연성 | 구성 요소는 작성자가 거의 모든 레이아웃을 조합할 수 있는 일반 개념을 보여 줍니다. |
| 구성 가능 | 템플릿 수준의 [콘텐츠 정책](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html?#content-policies)은 페이지 작성자가 사용하거나 사용할 수 없는 기능을 정의합니다. |
| [반응형](responsive.md) | 모든 핵심 구성 요소는 완벽하게 반응하도록 설계되어 여러 장치에서 원활한 경험을 보장합니다. |
| 추적 가능 | [Adobe 클라이언트 데이터 레이어](/help/developing/data-layer/overview.md) 통합 기능을 통해 모든 측면의 방문자 경험을 추적할 수 있습니다. |
| 액세스 가능 | [WCAG 2.1 표준](https://www.w3.org/TR/WCAG21/)을 준수하고 ARIA 레이블을 제공하며 키보드 탐색을 지원합니다([알려진 문제](https://github.com/adobe/aem-core-wcm-components/issues?utf8=✓&q=is%3Aissue+is%3Aopen+accessibility+in%3Atitle)). |
| SEO 친화도 | HTML 출력은 의미가 있으며 [schema.org](https://schema.org) 마이크로 데이터 주석을 제공합니다. |
| WebApp 기반 | [간소화된 JSON 출력](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/development/develop-sling-model-exporter.html?lang=ko)을 통해 클라이언트측을 렌더링하고 [상황에 맞게 편집](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html?lang=ko)할 수 있습니다. |
| AMP 지원 | 구성 요소는 [AMP 표준에 대한 지원](/help/developing/amp.md)을 기본 제공하고 모바일 경험을 가속화합니다. |
| 디자인 키트 | 디자이너는 [Adobe XD용 UL 키트](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/AEM-CoreComponents-UI-Kit.xd)를 통해 [필요에 따라 스타일링](https://github.com/adobe/aem-guides-wknd/releases/download/aem-guides-wknd-0.0.2/AEM_UI-kit-WKND.xd)될 수 있는 와이어프레임을 만들 수 있습니다. |
| 테마 적용 가능 | 구성 요소는 [스타일 시스템](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=ko)을 구현하고 마크업이 [BEM CSS 명명](https://getbem.com/)을 따릅니다 |
| 사용자 정의 가능 | 몇 가지 패턴을 사용하여 HTML 조정부터 고급 기능 재사용까지 [간편한 맞춤화](developing/customizing.md)를 구현할 수 있습니다. |
| 버전 관리 | [버전 관리 정책](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies)을 사용하여 몇 가지 개선 사항을 수정하면 사이트는 핵심 구성 요소에 의해 연결이 끊기지 않습니다. |
| 현지화 가능 | 스마트 참조 해상도를 사용하면 특정 구성 요소에서 [현지화된 해당 콘텐츠를 자동으로 검색하여 렌더링할 수 있습니다](get-started/localization.md). |
| 오픈 소스 | 매출이 평소와 같지 않다면 [자신의 성과를 공개하십시오](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md). |


## WCM 구성 요소 {#the-wcm-components}

핵심 구성 요소의 현재 버전은 다음 구성 요소 기능이 있습니다.

### 템플릿 구성 요소 {#template-components}

* [페이지](components/page.md)
* [탐색](components/navigation.md)
* [언어 탐색](components/language-navigation.md)
* [이동 경로](components/breadcrumb.md)
* [빠른 검색](components/quick-search.md)
* [목차](components/tableofcontents.md)

### 페이지 작성 구성 요소 {#page-authoring-components}

* [제목](components/title.md)
* [텍스트](components/text.md)
* [이미지](components/image.md)
* [버튼](components/button.md)
* [티저](components/teaser.md)
* [다운로드](components/download.md)
* [목록](components/list.md)
* [경험 조각](components/experience-fragment.md)
* [콘텐츠 조각](components/content-fragment-component.md)
* [콘텐츠 조각 목록](components/content-fragment-list.md)
* [임베드](components/embed.md)
* [소셜 미디어 공유](components/sharing.md) (사용 안 함)
* [구분자](components/separator.md)
* [진행률 표시줄](components/progress-bar.md)
* [PDF 뷰어](components/pdf-viewer.md)

### 컨테이너 구성 요소 {#container-components}

* [컨테이너](components/container.md)
* [슬라이드](components/carousel.md)
* [탭](components/tabs.md)
* [아코디언](components/accordion.md)

### 양식 구성 요소 {#form-components}

* [양식 컨테이너](components/forms/form-container.md)
* [양식 텍스트](components/forms/form-text.md)
* [양식 옵션](components/forms/form-options.md)
* [양식 숨김](components/forms/form-hidden.md)
* [양식 버튼](components/forms/form-button.md)

>[!NOTE]
>
>작성자는 핵심 구성 요소를 즉시 사용할 수 없으며, [개발 팀에서 먼저 핵심 구성 요소를 환경에 통합](get-started/using.md)해야 합니다. 통합되면 [템플릿 편집기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=ko)를 통해 사용 및 사전 구성할 수 있습니다.

>[!NOTE]
>
>개별 핵심 구성 요소의 일부 버전은 특정 AEM 버전과 호환될 수 있습니다.
>
>특정 구성 요소에 대한 개별 도움말 페이지(이전 목록에 연결됨)에서 호환성 정보를 참조하거나 [핵심 구성 요소 버전](versions.md) 문서에서 자세한 내용을 참조하십시오.

## 시스템 요구 사항 {#system-requirements}

| 핵심 구성 요소 릴리스 | AEM as a Cloud Service | AEM 6.5 LTS | AEM 6.5 | Java SE 버전 | Maven 버전 |
|---|---|---|---|---|---|
| [2.28.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.28.0) | 반복 | 6.5LTS GA | 6.5.21.0+ | 8, 11 | 3.3.9+ |

이전 핵심 구성 요소 릴리스의 요구 사항을 알아보려면 [핵심 구성 요소 버전](versions.md)을 참조하십시오.

구성 요소는 [편집 가능한 템플릿](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html?lang=ko)을 사용하고 클래식 UI와 정적 템플릿을 지원하지 않습니다. 필요한 경우 [AEM 현대화 도구](https://opensource.adobe.com/aem-modernize-tools/)를 사용하여 해당 최신 AEM 기능이 포함된 프로젝트를 업데이트합니다.

로컬 개발 환경을 설정하려면 기존 버전의 AEM에 대한 [AEM as a Cloud Service SDK](https://experienceleague.adobe.com/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html?lang=ko) 개요나 [본 문서](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html?lang=ko)를 참조하십시오.

>[!TIP]
>
>핵심 구성 요소는 자동으로 AEM as a Cloud Service의 일부로 적용되고, 핵심 구성 요소 릴리스는 언제나 최신 버전입니다.
>
>AEMaaCS와 온프레미스에서 핵심 구성 요소를 시작하는 방법에 대한 자세한 내용은 [핵심 구성 요소 사용](/help/get-started/using.md) 문서를 참조하십시오.

## 기타 구성 요소 {#other-components}

핵심 구성 요소에 빌드된 AEM 작성자가 사용할 수 있는 추가 구성 요소가 있습니다.

* [이메일 핵심 구성 요소](/help/email/introduction.md) - 특히 Adobe Campaign과 함께 사용하기 위해 핵심 구성 요소의 상단에 빌드된 구성 요소를 살펴보십시오.

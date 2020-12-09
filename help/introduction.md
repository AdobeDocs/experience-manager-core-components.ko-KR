---
title: 핵심 구성 요소 소개
description: '핵심 구성 요소는 최신 기술과 우수 사례를 기반으로 구축된 강력하고 확장 가능한 기본 구성 요소를 제공합니다. '
translation-type: tm+mt
source-git-commit: 456bd449f5776355923bcd859a2afb6b00f33d5c
workflow-type: tm+mt
source-wordcount: '889'
ht-degree: 25%

---


# 핵심 구성 요소 소개{#core-components-introduction}

Adobe Experience Manager에서 구성 요소는 작성 중인 페이지의 콘텐츠를 구성하는 구조적 요소입니다. 구성 요소는 항상 AEM 경험의 기본 요소로, 이를 통해 작성자는 간단하지만 강력한 페이지를 만들 수 있고 개발자는 유연하고 확장 가능한 구성 요소를 개발할 수 있습니다.

핵심 구성 요소는 개발 시간을 단축하고 웹 사이트의 유지 관리 비용을 줄일 수 있는 AEM용 표준화된 WCM(Web Content Management) 구성 요소 세트입니다.

## 리소스 {#resources}

* **[구성 요소 라이브러리:](https://www.adobe.com/go/aem_cmp_library)** 다양한 구성의 구성 요소를 보는 예제 모음입니다.
* **구성 요소 설명서(이 문서):** 개발자와 작성자를 위한 각 구성 요소에 대한 세부 정보입니다.
* **[핵심 구성 요소 GitHub 저장소:](https://github.com/adobe/aem-core-wcm-components)** 각 구성 요소 및 프로젝트 다운로드에 대한 개발자 세부 정보를 참조하십시오.
* 시작하기:
   * **[핵심 구성 요소 사용 성공:](/help/developing/success.md)** 핵심 구성 요소를 사용할 프로젝트를 시작하기 전에 미리 고려하는 가이드라인.
   * **[WKND 자습서: ](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)** 새 사이트 구축을 위한 2일 자습서입니다.
   * **[Summit 자습서: ](https://expleague.azureedge.net/labs/L767/index.html)** 새로운 사이트 구축을 위한 2시간 자습서(2019년 Summit의 Lab)입니다.
   * **[Gems 웨비나:](https://helpx.adobe.com/kr/experience-manager/kt/eseminars/gems/AEM-Core-Components.html에서 확인하십시오.)** 핵심 구성 요소의 둘러보기(2018년 12월 녹화)

## 기능 {#features}

|  |  |
|---|---|
| 프로덕션 준비 | 핵심 구성 요소는 28개의 강력한 구성 요소로서, 테스트를 잘 거친, 널리 사용되고, 그 성능이 우수합니다. |
| 클라우드 지원 | [AEM에서 Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html), [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) 또는 온-프레미스 중 어느 것이든 모두 작동합니다. |
| 유연성 | 구성 요소는 작성자가 거의 모든 레이아웃을 구성할 수 있는 일반 개념을 나타냅니다. |
| 구성 가능 | 템플릿 수준 [컨텐츠 정책](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/components-templates/templates.html#content-policies)은 페이지 작성자가 사용할 수 있거나 사용할 수 없는 기능을 정의합니다. |
| 추적 가능 | [Adobe 클라이언트 데이터 레이어 통합](/help/developing/data-layer/overview.md)을 사용하면 방문자 경험의 모든 측면을 추적할 수 있습니다. |
| 액세스 가능 | 이러한 디자이너는 [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/)를 준수하고, ARIA 레이블을 제공하고, 키보드 탐색([알려진 문제](https://github.com/adobe/aem-core-wcm-components/issues?utf8=✓&amp;q=is%3Aissue+is%3Aopen+accessibility+in%3Attle))을 지원합니다. |
| SEO-Friendly | HTML 출력은 의미적이며 [schema.org](https://schema.org) 마이크로데이터 주석을 제공합니다. |
| WebApp-Ready | [간소화된 JSON 출력](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/develop-sling-model-exporter.html)은 클라이언트측 렌더링을 허용하지만 [상황에 맞는 편집](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)의 가능성이 있습니다. |
| AMP 지원 | 이 구성 요소는 모바일 경험을 가속화하는 AMP 표준인 [에 대한 기본 지원을 제공합니다.](/help/developing/amp.md) |
| 디자인 키트 | 디자이너는 Adobe XD](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/AEM-CoreComponents-UI-Kit.xd)용 [UI 키트를 사용하여 필요한 경우 [스타일을 지정할 수 있는 와이어프레임을 만들 수 있습니다.](https://github.com/adobe/aem-guides-wknd/releases/download/aem-guides-wknd-0.0.2/AEM_UI-kit-WKND.xd). |
| 사용 가능 | 구성 요소는 [Style System](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/components-templates/style-system.html)을 구현하며 마크업은 [BEM CSS 규칙](http://getbem.com/)을 따릅니다. |
| 사용자 정의 가능 | 일부 패턴에서는 [사용자 정의](developing/customizing.md)이(가) HTML을 조정하는 것부터 고급 기능 재사용에 이르기까지 간단합니다. |
| 버전 관리 | [버전 관리 정책](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies)에서는 영향을 줄 수 있는 사항을 개선할 때 핵심 구성 요소가 사이트를 벗어나지 않도록 합니다. |
| 현지화 가능 | 스마트 참조 해상도를 사용하면 특정 구성 요소가 해당 지역화된 컨텐츠를 자동으로 찾아 [렌더링할 수 있습니다.](get-started/localization.md) |
| 오픈 소스 | 원하는 내용이 아닌 경우 [개선 사항을 증여합니다!](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) |

## 구성 요소 {#the-components}

핵심 구성 요소의 현재 버전은 다음 구성 요소 기능이 있습니다.

### 템플릿 구성 요소 {#template-components}

* [페이지](components/page.md)
* [탐색](components/navigation.md)
* [언어 탐색](components/language-navigation.md)
* [탐색 표시](components/breadcrumb.md)
* [빠른 검색](components/quick-search.md)

### 페이지 작성 구성 요소 {#page-authoring-components}

* [제목](components/title.md)
* [텍스트](components/text.md)
* [이미지](components/image.md)
* [단추](components/button.md)
* [티저](components/teaser.md)
* [다운로드](components/download.md)
* [목록](components/list.md)
* [경험 조각](components/experience-fragment.md)
* [콘텐츠 조각](components/content-fragment-component.md)
* [콘텐츠 조각 목록](components/content-fragment-list.md)
* [포함](components/embed.md)
* [소셜 미디어 공유](components/sharing.md)
* [분리자](components/separator.md)
* [진행률 표시줄](components/progress-bar.md)
* [PDF 뷰어](components/pdf-viewer.md)

### 컨테이너 구성 요소 {#container-components}

* [컨테이너](components/container.md)
* [회전판](components/carousel.md)
* [탭](components/tabs.md)
* [어코디언](components/accordion.md)

### 양식 구성 요소 {#form-components}

* [양식 컨테이너](components/forms/form-container.md)
* [양식 텍스트](components/forms/form-text.md)
* [양식 옵션](components/forms/form-options.md)
* [숨겨진 양식](components/forms/form-hidden.md)
* [양식 단추](components/forms/form-button.md)

>[!NOTE]
>
>작성자는 핵심 구성 요소를 즉시 사용할 수 없습니다. [개발 팀에서 먼저 핵심 구성 요소를 환경에 통합해야 합니다](get-started/using.md). 통합된 후에는 [템플릿 편집기](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)를 통해 사용 및 사전 구성할 수 있습니다.

>[!NOTE]
>
>개별 핵심 구성 요소의 일부 버전은 특정 AEM 버전과 호환될 수 있습니다.
>
>특정 구성 요소에 대한 개별 도움말 페이지(이전 목록에 연결됨)에서 호환성 정보를 참조하거나 [핵심 구성 요소 버전](versions.md) 문서에서 자세한 내용을 참조하십시오.

## 시스템 요구 사항 {#system-requirements}

| 코어 구성 요소 | AEM as a Cloud Service | AEM 6.5 | AEM 6.4 | Java SE | 마벤 |
|---------|---------|---------|---------|---------|---------|
| [2.13.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.13.0) | 지속적인 | 6.5.5.0+ * | 6.4.8.1+ * | 8, 11 | 3.3.9+ |

>[!NOTE]
>
>(*) 버전 2.11.0부터 `org.apache.sling.models.impl` 버전 1.4.12 이상이 필요합니다([SLING-8781](https://issues.apache.org/jira/browse/SLING-8781)). 이 서비스는 향후 서비스 팩에서 AEM 6.4 및 6.5용으로 제공됩니다. 그때까지 Sling Models 번들은 `core.wcm.components.all` 패키지에 포함됩니다.

이전 코어 구성 요소 릴리스의 요구 사항은 [핵심 구성 요소 버전](versions.md)을 참조하십시오.

핵심 구성 요소는 [편집 가능한 템플릿](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html)을 사용해야 하며 클래식 UI나 정적 템플릿을 지원하지 않습니다. 필요한 경우 [AEM Modern Tools](https://opensource.adobe.com/aem-modernize-tools/pages/tools.html)에서 최신 AEM 기능으로 프로젝트를 업데이트하십시오.

로컬 개발 환경을 설정하려면, AEM에 대한 이 개요를 Cloud Service SDK[ 또는 이전 버전의 AEM[의 경우 이 문서 ](https://docs.adobe.com/content/help/en/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html)로 확인하십시오.](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html)

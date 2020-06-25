---
title: 핵심 구성 요소 소개
description: '핵심 구성 요소는 최신 기술과 우수 사례를 기반으로 구축된 강력하고 확장 가능한 기본 구성 요소를 제공하기 위해 도입되었습니다. '
translation-type: tm+mt
source-git-commit: 5a953588f83e13e50924a2bd9afa2466e3ef6f4d
workflow-type: tm+mt
source-wordcount: '848'
ht-degree: 28%

---


# 핵심 구성 요소 소개{#core-components-introduction}

Adobe Experience Manager에서 구성 요소는 작성 중인 페이지의 콘텐츠를 구성하는 구조적 요소입니다. 구성 요소는 항상 AEM 경험의 기본 요소로, 이를 통해 작성자는 간단하지만 강력한 페이지를 만들 수 있고 개발자는 유연하고 확장 가능한 구성 요소를 개발할 수 있습니다.

핵심 구성 요소는 개발 시간을 단축하고 웹 사이트의 유지 관리 비용을 줄이기 위해 AEM을 위한 표준화된 WCM(Web Content Management) 구성 요소 세트입니다.

## 리소스 {#resources}

* **[구성 요소 라이브러리:](https://www.adobe.com/go/aem_cmp_library)**다양한 구성의 구성 요소를 보는 예제 모음입니다.
* **구성 요소 설명서(이 문서):** 개발자 및 작성자를 위한 자세한 내용은 각 구성 요소에 대한 정보를 참조하십시오.
* **[핵심 구성 요소 GitHub 저장소:](https://github.com/adobe/aem-core-wcm-components)**각 구성 요소 및 프로젝트 다운로드에 대한 개발자 세부 정보를 참조하십시오.
* 시작하기:
   * **[핵심 구성 요소를 사용한 성공:](/help/developing/success.md)**핵심 구성 요소를 사용할 프로젝트를 시작하기 전에 미리 고려하는 지침
   * **[WKND 자습서:](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)**새 사이트 구축을 위한 2일 자습서입니다.
   * **[Summit 자습서:](https://expleague.azureedge.net/labs/L767/index.html)**새로운 사이트 구축을 위한 2시간 자습서(US Summit 2019의 랩에서 제공)
   * **[Gems 웨비나:](https://helpx.adobe.com/kr/experience-manager/kt/eseminars/gems/AEM-Core-Components.html에서 확인하십시오.)**핵심 구성 요소 둘러보기(2018년 12월 녹화)

## 기능 {#features}

|  |  |
|---|---|
| 프로덕션 준비 | 핵심 구성 요소는 28개의 강력한 구성 요소로서, 테스트를 잘 거친, 널리 사용되고, 그 성능이 우수합니다. |
| 클라우드 지원 | AEM에서 [Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html), [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams)또는 온-프레미스 중 어느 것이든 모두 작동합니다. |
| 유연성 | 구성 요소는 작성자가 거의 모든 레이아웃을 구성할 수 있는 일반 개념을 나타냅니다. |
| 구성 가능 | 템플릿 수준 [컨텐츠 정책은](https://docs.adobe.com/content/help/en/experience-manager-65/developing/platform/templates/page-templates-editable.html#content-policies) 페이지 작성자가 사용할 수 있거나 사용하지 않을 수 있는 기능을 정의합니다. |
| 추적 가능 | Adobe [Client Data Layer 통합을](/help/developing/data-layer/overview.md) 통해 방문자 경험의 모든 측면을 추적할 수 있습니다. |
| 액세스 가능 | They comply [WCAG 2.1 standard](https://www.w3.org/TR/WCAG21/), provide ARIA labels, and support keyboard navigation ([known issues](https://github.com/adobe/aem-core-wcm-components/issues?utf8=✓&amp;q=is%3Aissue+is%3Aopen+accessibility+in%3Attle)). |
| SEO-Friendly | The HTML output is semantic and provides [schema.org](https://schema.org) microdata annotations. |
| WebApp-Ready | 간소화된 [JSON 출력](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/develop-sling-model-exporter.html) 덕분에 클라이언트측 렌더링을 할 수 있으며 상황에 맞는 편집 [이 가능합니다](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html). |
| 디자인 키트 | 디자이너는 [Adobe XD용](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/assets/overview/AEM_UI-kit_Wireframe.xd) UI 키트를 사용하여 와이어프레임을 만들고 필요에 따라 [스타일을 지정할 수 있습니다](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/assets/overview/AEM_UI-kit_WKND.xd). |
| 사용 가능 | The components implement the [Style System](https://docs.adobe.com/content/help/en/experience-manager-65/developing/components/style-system.html), and the markup follows [BEM CSS conventions](http://getbem.com/). |
| 사용자 정의 가능 | HTML을 조정하거나 고급 기능을 재사용할 때 [손쉽게 사용자 지정할](developing/customizing.md)수 있는 패턴도 있습니다. |
| 버전 관리 | 버전 [관리 정책은](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies) 사용자에게 영향을 줄 수 있는 사항을 개선할 때 핵심 구성 요소가 사이트를 벗어나지 않도록 합니다. |
| 현지화 가능 | Smart reference resolution allows certain components to find and [render corresponding localized content automatically](get-started/localization.md). |
| 오픈 소스 | 만약 어떤 것이 제대로 되어 있지 않다면, [여러분의 개선점을 기부하세요!](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) |

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
>작성자는 핵심 구성 요소를 즉시 사용할 수 없습니다. [개발 팀에서 먼저 핵심 구성 요소를 환경에 통합해야 합니다](get-started/using.md). Once integrated, they may be made available and pre-configured via the [template editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

>[!NOTE]
>
>개별 핵심 구성 요소의 일부 버전은 특정 AEM 버전과 호환될 수 있습니다.
>
>특정 구성 요소에 대한 개별 도움말 페이지(이전 목록에 연결됨)에서 호환성 정보를 참조하거나 [핵심 구성 요소 버전](versions.md) 문서에서 자세한 내용을 참조하십시오.

## 시스템 요구 사항 {#system-requirements}

| 코어 구성 요소 | 클라우드 서비스로서의 AEM | AEM 6.5 | AEM 6.4 | Java SE | 마벤 |
---------|---------|---------|---------|---------|---------
| [2.10.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.10.0) | 지속적인 | 6.5.5.0+ | 6.4.8.1+ | 8, 11 | 3.3.9+ |

이전 코어 구성 요소 릴리스의 요구 사항은 [핵심 구성 요소 버전을 참조하십시오](versions.md).

핵심 구성 요소는 [편집 가능한 템플릿을](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html) 사용해야 하며 클래식 UI나 정적 템플릿을 지원하지 않습니다. 필요한 경우 AEM [Modern](https://opensource.adobe.com/aem-modernize-tools/pages/tools.html) Tools를 참조하여 최신 AEM 기능으로 프로젝트를 업데이트하십시오.

로컬 개발 환경을 설정하려면 AEM에 대한 [이 개요를 Cloud Service SDK로](https://docs.adobe.com/content/help/en/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html) 확인하거나 이전 버전의 AEM에 [대한 이 문서를 확인하십시오](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html).

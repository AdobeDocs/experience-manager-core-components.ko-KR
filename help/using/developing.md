---
title: 핵심 구성 요소 개발
seo-title: 핵심 구성 요소 개발
description: 핵심 구성 요소는 기능이 풍부한 기능, 지속적인 전달, 구성 요소 버전 관리, 최신 구현, Lean Markup 및 JSON 내보내기를 제공하는 강력하고 확장 가능한 기본 구성 요소를 제공합니다.
seo-description: 핵심 구성 요소는 기능이 풍부한 기능, 지속적인 전달, 구성 요소 버전 관리, 최신 구현, Lean Markup 및 JSON 내보내기를 제공하는 강력하고 확장 가능한 기본 구성 요소를 제공합니다.
uuid: 68569 da 2-9 bc 8-4 e 20-9 a 71-e 5816 ace 51 ce
contentOwner: 사용자
content-type: 참조
topic-tags: developing
products: sg_ Experiencemanager/Corecomponents-new
discoiquuid: 157 A 2 EC 3-9 FCA -4 FAD -977 A-D 93013 EEB 218
translation-type: tm+mt
source-git-commit: f30a6a9f4d41c672472beb60767f3766479d9c16

---


# Developing Core Components{#developing-core-components}

## 개요 {#overview}

핵심 구성 요소는 강력하고 확장 가능한 기본 구성 요소를 제공하며 다음과 같습니다.

* 기능이 풍부한 기능
   * [다양한 활용 사례를 수용할 수 있는 유연한 구성 옵션](authoring.md)
   * [페이지 작성자가 사용할 수 있는 기능을 정의하기](authoring.md#pre-configuring-core-components) 위한 사전 구성 가능 기능
* 지속적인 전달
   * 향상된 증분 기능
   * Availability of the [source code on GitHub](https://github.com/adobe/aem-core-wcm-components) to allow the developer community to give feedback and contribute
   * Installation through a [separately released content package](https://github.com/adobe/aem-core-wcm-components/releases) for component upgrades to be done independently from AEM upgrades
* [구성 요소 버전 관리](guidelines.md#component-versioning)
   * [구성 요소 간에 호환성이 보장되는 버전](#upgrade-of-core-components)내 호환성 보장
   * 한 구성 요소의 여러 버전이 동일한 환경에서 공존하도록 허용
* 최신 구현
   * Markup defined in [HTML Template Language](https://helpx.adobe.com/experience-manager/htl/using/overview.html) (HTL)
   * Content model logic implemented with [Sling Models](https://sling.apache.org/documentation/bundles/models.html)
* Lean Markup
   * Following [Block Element Modifier](https://getbem.com/) (BEM) notation as of Release 2.0.0
      * Prior release follow [Bootstrap](https://getbootstrap.com/css/) naming conventions
   * Built around [accessibility guidelines](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html)
   * 반응형 및 모바일 사이트에 사용 가능
* 헤드리스 CMS 사용 사례를 위한 컨텐츠 모델로 JSON 직렬화 기능
* 액세스 가능
   * [WCAG 2.0 AA 표준을 준수하는 표준](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html)

>[!CAUTION]
>
>Core Components require AEM 6.3 or later and Java 8 and and require the use of [editable templates](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)
>
>핵심 구성 요소는 클래식 UI 또는 정적 템플릿과 함께 작동하지 않습니다.

## Gems Session Overview {#gems-session-overview}

For an introduction to the Core Components, the features they offer, and how they are leveraged in AEM, check out the AEM Gems Session [AEM Core Components.](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)

[Adobe Experience Manager](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/aem-index.html) 의 Gems는 Adobe 전문가가 제공하는 일련의 기술 심층 선봉입니다. 이 시리즈는 제품 설명서와 기타 모든 기술 채널을 보완해 주므로 개발자는 특정 주제를 자세히 살펴볼 수 있습니다.

## WKND Developer Tutorial {#wknd-developer-tutorial}

Get started developing AEM Sites with Core Components by following [this step-by-step tutorial.](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/getting-started.html)

## Delivered over GitHub {#delivered-over-github}

핵심 구성 요소는 Github를 통해 개발되고 제공됩니다.

Github의 코드

Github에서 이 페이지의 코드를 찾을 수 있습니다.

* [Github에서 AEM-core-wcm-components 프로젝트 열기](https://github.com/adobe/aem-core-wcm-components)
* Download the project as [a ZIP file](https://github.com/adobe/aem-core-wcm-components/archive/master.zip)

See the [Using Core Components](using.md) documentation page to learn how to get started using them in your project.

Github의 핵심 구성 요소를 사용하면 자주 업데이트를 수행하고 AEM 개발자 커뮤니티의 피드백을 수렴할 수 있습니다. 또한 사용자 지정 구성 요소를 빌드할 때 이와 유사한 패턴을 따라야 합니다.

>[!NOTE]
>
>To keep up-to-date on the latest changes to the core components, you can watch the [Core Components repository](https://github.com/adobe/aem-core-wcm-components) on GitHub.

## 구성 요소 라이브러리

Check out the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library.html), which showcases the current release of the Core Components and gives examples of their usage.

### Sample Content Run-Mode {#sample-content-run-mode}

The Core Components are visible in the Quickstart when the sample content is present, because the [We.Retail reference site](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html) uses them. However, when running in production (in `nosamplecontent` runmode, without sample content enabled), the core components won&#39;t be present anymore and must be installed on the AEM instances by the development and/or operations team.

>[!NOTE]
>
>In production environments, always run the Quickstart in `nosamplecontent` runmode. To use the Core Components in `nosamplecontent` runmode, follow the instructions of the [Using Core Components](using.md) documentation page.

## Technical Capabilities {#technical-capabilities}

다음 표에서는 핵심 구성 요소와 기본 구성 요소 간의 차이점을 대략적으로 설명합니다.

For details about their authoring capabilities and options to pre-configurable them, [refer to the authoring page about them](authoring.md).

| **기능** | **핵심 구성 요소** | **Foundation 구성 요소** |
|-----|---|---|
| 논리 구현 | [Sling Models](https://sling.apache.org/documentation/bundles/models.html) 주석이 있는 Java Pojos | JSP 코드 |
| 마크업 정의 | [HTML (HTML Template Language)](https://helpx.adobe.com/experience-manager/htl/user-guide.html) 구문 | JSP 코드 |
| XSS 기밀 정보 가리기 | HTL에서 자동화 | 대부분의 수동 설명서 |
| CSS 클래스 이름 지정 | Standardized naming convention based on [Block Element Modifier](https://getbem.com/) (BEM) notation (as of release 2.0.0) | 맞춤형 구성 |
| 대화 상자 정의 | [Coral 3](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/reference-materials/coral-ui/coralui3/index.html) | Coral 2 + Classic UI |
| JSON 출력 | [Jackson 일련화 관련 Sling Models Exporter](https://sling.apache.org/documentation/bundles/models.html#exporter-framework-since-130) | 기본 Sling 서블릿 |
| 버전 관리 | [The Model and the HTL](guidelines.md) | 없음 |
| 테스트 | 유닛 테스트 + 통합 테스트 | 통합 테스트 |
| 배달 | [공용 Github를 통해](https://github.com/adobe/aem-core-wcm-components) | 빠른 시작 |
| 라이센스 | [Apache License](https://www.apache.org/licenses/LICENSE-2.0) | Adobe 독점 |
| 기여도 | 가져오기 요청 | 가능하지 않음 |
| 액세스 가능성 | Fully compliant with the [WCAG 2.0 AA standard](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html) | Only partially compliant with the [WCAG 2.0 AA standard](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html) |

## Component List {#component-list}

다음 표에는 API에 연결하는 사용 가능한 핵심 구성 요소가 나와 있으며 해당 구성 요소가 대체할 기본 구성 요소가 나와 있습니다.

| 핵심 구성 요소 | 설명 | Foundation 구성 요소 대체 |
|---|---|---|
| [페이지](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/page/v2/page) | 템플릿 편집기를 사용한 반응형 페이지 | `/libs/foundation/components/page /libs/wcm/foundation/components/page` |
| [탐색 표시](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb) | 페이지 계층 탐색 | `/libs/foundation/components/breadcrumb` |
| [제목](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/title/v2/title) | H 1-H 6 제목 | `/libs/foundation/components/title /libs/wcm/foundation/components/title` |
| [텍스트](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v2/text) | 리치 텍스트 | `/libs/foundation/components/text /libs/foundation/components/table /libs/wcm/foundation/components/text` |
| [이미지](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/image/v2/image) | 최적의 변환 크기 스마트 및 지연 로딩 | `/libs/foundation/components/image /libs/foundation/components/adaptiveimage /libs/foundation/components/logo /libs/foundation/components/mobileimage  /libs/foundation/components/mobilelogo /libs/wcm/foundation/components/image` |
| [목록](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/list/v2/list) | 페이지 목록 | `/libs/foundation/components/list /libs/foundation/components/mobilelist /libs/wcm/foundation/components/list` |
| [소셜 미디어 공유](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/sharing/v1/sharing) | Facebook 및 Pinterest 공유 위젯 | `-` |
| [양식 컨테이너](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/container/v2/container) | 반응형 양식 단락 시스템 | `/libs/foundation/components/form/start /libs/foundation/components/form/end` |
| [양식 텍스트](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v2/text) | 텍스트 입력 필드 | `/libs/foundation/components/form/text /libs/foundation/components/form/password` |
| [양식 옵션](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/options/v2/options) | 다중 옵션 입력 필드 | `/libs/foundation/components/form/checkbox /libs/foundation/components/form/radio /libs/foundation/components/form/dropdown` |
| [숨겨진 양식](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/hidden/v2/hidden) | 숨겨진 입력 필드 | `/libs/foundation/components/form/hidden` |
| [양식 단추](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/button/v2/button) | 제출 또는 사용자 지정 단추 | `/libs/foundation/components/form/submit` |
| [탐색](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/navigation/v1/navigation) | 중첩된 페이지 계층 구조를 나열하는 사이트 탐색 구성 요소 | `/libs/foundation/components/topnav /libs/foundation/components/mobiletopnav` |
| [언어 탐색](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/languagenavigation/v1/languagenavigation) | 글로벌 언어 구조를 나열하는 언어 및 국가 전환기 | `-` |
| [빠른 검색](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/search/v1/search) | 드롭다운 메뉴에서 결과를 즉석 제안 사항으로 표시하는 검색 구성 요소 | `/libs/foundation/components/search` |
| [티저](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/teaser/v1/teaser) | 컨텐츠 작성자가 이미지, 제목 또는 리치 텍스트를 사용하여 추가 컨텐츠에 대한 티저를 쉽게 만들고 추가 컨텐츠 또는 기타 작업을 연결할 수 있도록 합니다. | `-` |
| [탭](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/tabs/v1/tabs) | 컨텐츠 작성자가 여러 탭 내에서 페이지 컨텐츠를 구성할 수 있도록 설정 | `-` |
| [회전판](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/carousel/v1/carousel) | 컨텐츠 작성자가 회전 슬라이드 회전판에서 컨텐츠를 구성할 수 있도록 합니다. | `/libs/foundation/components/carousel` |
| [컨텐츠 조각](https://github.com/adobe/aem-core-wcm-components/tree/master/extension/contentfragment/content/src/content/jcr_root/apps/core/wcm/extension/components/contentfragment/v1/contentfragment) | 컨텐츠 조각을 표시할 수 있습니다. | `-` |
| [컨텐츠 조각 목록](https://github.com/adobe/aem-core-wcm-components/tree/master/extension/contentfragment/content/src/content/jcr_root/apps/core/wcm/extension/components/contentfragmentlist/v1/contentfragmentlist) | 컨텐츠 조각 목록 표시를 허용합니다. | `-` |
| [분리자](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/separator/v1/separator) | 페이지의 컨텐츠 분리 | `-` |
| [어코디언](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/accordion/v1/accordion) | 축소 가능한 아코디언에서 컨텐츠 패널 구성 | `-` |
| [컨테이너](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/container/v1/container) | 컨테이너 내의 구성 요소 구성 | `-` |
| [단추](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/button/v1/button) | 페이지에 단추 만들기 | `-` |
| [다운로드](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/download/v1/download) | 페이지에 다운로드 가능한 에셋 추가 | `-` |

### Upcoming Components {#upcoming-components}

For an overview of the upcoming Core Componente roadmap see the [project wiki on GitHub](https://github.com/adobe/aem-core-wcm-components/wiki/home).

## Upgrade of Core Components {#upgrade-of-core-components}

버전 구성 요소의 한 가지 이점은 새 AEM 버전으로 마이그레이션과 새 구성 요소 버전으로 마이그레이션을 분리할 수 있다는 것입니다. 또한 새 구성 요소 버전을 사용할 수 있는 경우 각 구성 요소를 새 버전으로 개별 마이그레이션할 수 있습니다.

새 AEM 버전으로 마이그레이션하면 핵심 구성 요소가 작동하는 방식에는 영향을 주지 않습니다. 단, 해당 버전은 마이그레이션되는 새 AEM 버전도 지원합니다. Customizations made to the Core Components should not be affected either, as long as they don&#39;t use APIs that have been [deprecated or removed](https://helpx.adobe.com/experience-manager/6-5/release-notes/deprecated-removed-features.html).

새 버전의 핵심 구성 요소로 마이그레이션해도 구성 요소가 작동하는 방식에는 영향을 주지 않지만, 새 기능이 페이지 작성자에게 소개될 수 있는데, 이 기능은 기본 비헤이비어가 원하지 않는 경우에 템플릿 편집기에 의한 일부 구성이 필요할 수 있습니다. Customizations however might need to be adapted, for more details see the [Customizing Core Components](customizing.md#upgrade-compatibility-of-customizations) page.

## When to Use the Core Components? {#when-to-use-the-core-components}

핵심 구성 요소가 완전히 새로워지고 여러 이점을 제공하므로 새로운 AEM 프로젝트를 사용하는 것이 좋습니다. 기존 프로젝트의 경우 마이그레이션은 다시 브랜딩이나 전체 리팩토링과 같은 대규모 프로젝트 작업의 일부여야 합니다.

따라서 Adobe는 다음 권장 사항을 제공합니다.

* **새 프로젝트**새 프로젝트는
항상 핵심 구성 요소를 사용하려고 합니다. If Core Components cannot be used directly or [extended](customizing.md) to satisfy project requirements, then create a custom component following the component architecture set forth in core components. Except where not otherwise possible, avoid using the [foundation components](developing.md).
* **사이트 또는 구성 요소 리팩토링이 계획되지 않은 한 기존 프로젝트**
권장 사항은 [기본 구성 요소를](developing.md)계속 사용합니다.\
   As they are very widely used by most existing projects, the foundation components [will continue to be supported.](developing.md)
* **새로운 맞춤형 구성 요소는**
기존의 [핵심 구성 요소를 맞춤화할](customizing.md)수 있는지 여부를 평가합니다.\
   If not, recommendation is to build a new custom component following the [Component Guidelines](guidelines.md).
* **기존 사용자 지정 구성**
요소가 예상대로 작동하면 그대로 유지합니다.\
   그렇지 않은 경우 위의 &quot;새로운 사용자 지정 구성 요소&quot; 를 참조하십시오.

## 핵심 구성 요소로 마이그레이션

모든 새 프로젝트는 핵심 구성 요소로 구현해야 합니다. 그러나 기존 프로젝트에는 일반적으로 기본 구성 요소가 광범위하게 구현되어 있습니다.

기존 프로젝트 (예: 리브랜딩 또는 전체 리팩토링) 에 대한 큰 노력은 종종 핵심 구성 요소로 마이그레이션할 기회를 제공합니다. Adobe는 이 마이그레이션을 용이하게 하기 위해 핵심 구성 요소 및 최신 AEM 기술의 채택을 장려하기 위한 다양한 마이그레이션 도구를 제공했습니다.

[AEM 현대화 도구를](http://opensource.adobe.com/aem-modernize-tools/) 사용하면 다음을 쉽게 변환할 수 있습니다.

* 편집 툴이다. 이제는 실시간 미리보기를 통해 더
* 정책에 대한 디자인 구성
* 핵심 구성 요소에 대한 기본 구성 요소
* 터치 활성화 UI에 대한 클래식 UI

For further information about the usage of these tools, [see their documentation](http://opensource.adobe.com/aem-modernize-tools/).

>[!NOTE]
>
>AEM 현대화 도구는 커뮤니티 활동이며 Adobe가 지원하거나 보증하지 않습니다.

## Core Component Support {#core-component-support}

핵심 구성 요소는 AEM의 핵심적인 부분으로, Quickstart의 일부로 제공된 것과 동일한 조건에서 동일한 조건에서 지원됩니다.

다른 AEM 제품 기능과 마찬가지로 일반 규칙은 다음과 같습니다. 구성 요소는 처음 발표될 것으로 발표되며 다음 AEM 릴리스에 대해 가장 일찍 제거되었습니다. 지원 놓기 전에 고객에게 최소 1 개의 릴리스 주기가 새로운 버전의 구성 요소로 이동하도록 합니다.

각 구성 요소의 버전은 지원되는 AEM 버전을 명시합니다. 지원이 AEM 버전에 대해 중지되면 해당 버전의 AEM에 대한 핵심 구성 요소가 지원됩니다.

For details about the support of component customizations, see the [Customizing Core Components](customizing.md) page.

## Foundation Component Support {#foundation-component-support}

Foundation 구성 요소는 많은 AEM 버전에 대한 많은 프로젝트 개발의 기초로 제공되기 때문에 향후 계속 지원될 것입니다.

However, Adobe&#39;s development emphasis has shifted to the Core Components and new features will be added to them, whereas [nearly all Foundation Components have been deprecated with AEM 6.5](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-foundation.html) and only bug fixes will be made to the Foundation Components going forward.

**다음을 참조하십시오.**

* [핵심 구성 요소 사용](using.md) - 프로젝트에 핵심 구성 요소를 사용할 수 있습니다.
* [구성 요소 지침](guidelines.md) - 핵심 구성 요소의 구현 패턴을 학습합니다.

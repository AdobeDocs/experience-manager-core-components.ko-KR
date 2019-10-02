---
title: 핵심 구성 요소 버전
seo-title: 핵심 구성 요소 버전
description: 핵심 구성 요소는 동일한 핵심 구성 요소의 두 개 이상의 버전을 포함할 수 있는 릴리스로 게시됩니다. 이 문서에서는 릴리스 및 버전이 무엇이며 핵심 구성 요소 및 AEM과의 호환성을 이해하는 방법에 대해 설명합니다.
seo-description: 핵심 구성 요소는 동일한 핵심 구성 요소의 두 개 이상의 버전을 포함할 수 있는 릴리스로 게시됩니다. 이 문서에서는 릴리스 및 버전이 무엇이며 핵심 구성 요소 및 AEM과의 호환성을 이해하는 방법에 대해 설명합니다.
uuid: a916a923-8c5e-456a-84b5-b5228e21434
contentOwner: 사용자
content-type: 참조
topic-tags: 소개
products: SG_EXPERIENCEMANAGER/CORCOMPONENTS-new
discoiquuid: a3a98b2f-65bf-4493-82ad-01717938fdbc
translation-type: tm+mt
source-git-commit: 97f1461b57079806f9f96d325d9b763538e32127

---


# 핵심 구성 요소 버전{#core-components-versions}

핵심 구성 요소의 현재 릴리스는 2.7.0이며 AEM 6.5와 호환됩니다.릴리스 2.0.0에 대한 중요 업데이트로 2019년 9월에 릴리스되었습니다.릴리스 2.0.0에서는 기존 구성 요소의 v2 업데이트와 함께 새로운 구성 요소를 도입했습니다.

자세한 내용은 [이 문서의 릴리스](#versions-and-releases) 내역 및 호환성 섹션을 참조하십시오.

또한 구성 요소 라이브러리를 확인할 수 [있으며](http://opensource.adobe.com/aem-core-wcm-components/library.html), 이 라이브러리는 핵심 구성 요소의 현재 릴리스를 보여주고 사용 예를 제공합니다.

## 버전 및 릴리스 {#versions-and-releases}

핵심 구성 요소는 GitHub를 통해 배포됩니다. 이를 통해 Adobe는 구성 요소에 기능을 보다 신속하게 추가할 수 있고 AEM 릴리스 주기 외부의 커뮤니티 입력을 허용할 수 있습니다.

핵심 구성 요소는 호환되는 정의된 AEM 버전에서 사용할 수 있습니다. 즉, 하나의 AEM 버전이 여러 버전 또는 핵심 구성 요소의 릴리스를 지원할 수 있습니다. 이는 특정 버전의 AEM에 연결된 이전 Foundation 구성 요소보다 더 많은 유연성을 제공합니다.

### 버전 {#versions}

핵심 구성 요소의 주 이터레이션은 **버전입니다**. 각 구성 요소에는 버전이 있습니다. 버전은 **v** 에 v1 및 v2와 같은 0이 아닌 양의 정수가 추가됩니다. 버전은 이전 버전과 호환하지 않는 변경 사항에 대해서만 증가되며, 이는 일반적으로 새로운 기능 및 기능이 추가될 때 해당됩니다.

개발자와 관리자는 핵심 구성 요소의 버전을 리소스 유형 경로 및 구현의 정규화된 Java 클래스 이름에서 번호별로 인식할 수 있습니다. 이 버전 번호는 [의미 체계 버전 관리 지침에](https://semver.org/)의해 정의된 주요 버전을 나타냅니다.

핵심 구성 요소 버전에 대한 자세한 내용은 핵심 구성 요소의 [개발자 설명서를 참조하십시오](guidelines.md).

### 릴리스 {#releases}

The core components are made available through releases and represent the actual published artifacts available on GitHub. ****[](https://github.com/adobe/aem-core-wcm-components/releases) Releases are denoted with a decimal number of the format X.Y.Z and collect all core components together as a deliverable package.

* **Major releases can introduce new versions of existing components along with entirely new components as well as standard bug fixes.** This is represented by an increment in the X component of the release number.
* **Important releases can introduce new functionality to existing versions of components along with bug fixes.** This is represented by an increment in the Y component of the release number.
* **Minor releases contain only bug fixes.** This is represented by an increment in the Z component of the release number.

>[!NOTE]
>
>릴리스에는 동일한 구성 요소의 여러 버전이 포함될 수 있습니다.
>
>The same version of a component can appear in multiple releases.

## Release History and Compatibility {#release-history-and-compatibility}

The Core Components were first released with AEM 6.3 and are designed to be flexible and compatible with all supported AEM versions. Because of this a release of the components can contain multiple versions of the same component.

The following tables illustrate the compatibility of the releases of the Core Components along with which component versions are contained in which releases.

### Release History &amp; Supported AEM Versions {#release-history-supported-aem-versions}

The following table, the contents of which are available on GitHub with full release details, gives an overview of the releases of the Core Components and their compatibility with AEM releases and Java versions.[](https://github.com/adobe/aem-core-wcm-components/releases)

| 릴리스 | 설명 | AEM 6.3 | AEM 6.4 | AEM 6.5 | Java | 릴리스 날짜 |
|---|---|---|---|---|---|---|
| [2.7.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.7.0) | 이 릴리스에서는 새로운 포함 구성 요소가 도입되었습니다. | 6.3.3.4+ | 6.4.4.0+ | 6.5.0.0+ | 8, 11 | 2019년 9월 25일 |
| [2.6.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.6.0) | 이 릴리스에서는 새로운 경험 조각 구성 요소가 소개되었습니다. | 6.3.3.4+ | 6.4.4.0+ | 6.5.0.0+ | 8, 11 | 2019년 9월 6일 |
| [2.5.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.5.0) | 이 릴리스에서는 새로운 아코디언, 단추, 컨테이너 및 다운로드 구성 요소가 소개되었습니다. | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | 8, 11 | 2019년 6월 25일 |
| [2.4.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.4.0) | 이 릴리스에서는 컨텐츠 조각 목록 구성 요소가 소개되었습니다. | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | 8, 11 | 2019년 5월 7일 |
| [2.3.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.2) | 이 릴리스에서는 구성 요소 라이브러리에 대한 구체화에 중점을 두었지만, 분리자 구성 요소에 대한 일부 기능 개선 사항도 포함되어 있습니다 | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | 8 | 2019년 3월 14일 |
| [2.3.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.0) | 이 릴리스에서는 구성 요소 라이브러리 및 새로운 구분 문자 구성 요소를 소개할 뿐만 아니라 이미지 구성 요소에 대한 일부 기능 개선 사항도 포함되어 있습니다 | 6.3.3.0+ | 6.4.2.0+ | - | 8 | 2019년 2월 11일 |
| [2.2.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.2) | 이 릴리스에는 주로 버그 수정에 중점을 두지만 Carousel 구성 요소에 대한 일부 기능 개선 사항도 포함되어 있습니다 | 6.3.3.0+ | 6.4.2.0+ | - | 8 | 2018년 11월 27일 |
| [2.2.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.0) | 새롭게 추가된 탭 및 회전판 구성 요소, 향상된 이미지, 페이지 및 제목 구성 요소 및 향상된 추적 | 6.3.3.0+ | 6.4.2.0+ | - | 8 | 2018년 10월 16일 |
| [2.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.1.0) | Teaser 구성 요소 소개, 이미지 구성 요소 개선 사항 및 다양한 버그 수정 | 6.3.3.0+ | 6.4.2.0+ | - | 8 | 2018년 7월 13일 |
| [2.0.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.8) | 버그 수정 릴리스 | 6.3.2.0+ | 6.4.0.0+ | - | 8 | 2018년 6월 12일 |
| [2.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.6) | 향상된 추가 백그라운드 기능, 버그 수정 및 이미지 플립 지원을 비롯한 작은 개선 사항 | 6.3.2.0+ | 6.4.0.0+ | - | 8 | 2018년 4월 11일 |
| [2.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.4) | 주로 백그라운드 개선 사항, 버그 수정, 이미지, 페이지 및 컨텐츠 조각 구성 요소에 대한 일부 개선 사항 | 6.3.2.0+ | 6.4.0.0+ | - | 8 | 2018년 3월 7일 |
| [2.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.0) | 탐색, 언어 탐색 및 빠른 검색 구성 요소가 도입되었습니다. Style system implemented for all components. | 6.3.2.0+ | 6.4.0.0+ | - | 8 | 16 January 2018 |
| [1.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.1.0) | Implementation of JSON export on all components, introduction of the Content Fragment component | 6.3.1.0 | 6.4.0.0+ | - | 8 | 10 October 2017 |
| [1.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.6) | Several fixes for the Image component | 6.3.0.0+ | 6.4.0.0+ | - | 8 | 4 August 2017 |
| [1.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.4) | Fixes of Page Component, Image Component, various global fixes and improvements | 6.3.0.0+ | 6.4.0.0+ | - | 8 | 26 April 2017 |
| [1.0.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.all-1.0.2) | Fixes for animated GIF images in Image component | 6.3.0.0+ | 6.4.0.0+ | - | 7 | 22 March 2017 |
| [1.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.0) | Initial release of Core Components | 6.3.0.0+ | 6.4.0.0+ | - | 7 | 20 March 2017 |

>[!NOTE]
>
>AEM과 마찬가지로, 개발자는 최신 수정 사항 및 기능을 활용하기 위해 실행 중인 AEM 버전과 [호환되는 사용 가능한 핵심 구성 요소의](https://github.com/adobe/aem-core-wcm-components/releases/latest) 최신 릴리스 및 버전을 사용하는 것이 좋습니다.

### 구성 요소 버전 및 릴리스 {#component-versions-and-releases}

다음 표에서는 핵심 구성 요소의 릴리스에 포함된 구성 요소 버전을 자세히 설명합니다.

|  | Release 1.0.0 - 1.0.6 | 릴리스 1.1.0 | 릴리스 2.0.0 - 2.0.8 | 릴리스 2.1.0 | 릴리스 2.2.0-2.2.0 | 릴리스 2.3.0-2.3.2 | 릴리스 2.4.0 | 릴리스 2.5.0 | 릴리스 2.6.0 | 릴리스 2.7.0+ |
|---|---|---|---|---|---|---|---|---|---|---|
| **[페이지](page.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[제목](title.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[이미지](image.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[목록](list.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[탐색 표시](breadcrumb.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[소셜 미디어 공유](sharing.md)** | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[양식 컨테이너](form-container.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[양식 텍스트](form-text.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[양식 옵션](form-options.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[숨겨진 양식](form-hidden.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[양식 단추](form-button.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[컨텐츠 조각](content-fragment-component.md)** |  | 샌드박스 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[탐색](navigation.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[언어 탐색](language-navigation.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[빠른 검색](quick-search.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[티저](teaser.md)** |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[탭](tabs.md)** |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 |
| **[회전판](carousel.md)** |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 |
| **[구분 문자](separator.md)** |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 |
| **[콘텐츠 조각 목록](content-fragment-list.md)** |  |  |  |  |  |  | v1 | v1 | v1 | v1 |
| **[아코디언](accordion.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 |
| **[단추](button.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 |
| **[컨테이너](separator.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 |
| **[다운로드](separator.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 |
| **[경험 조각](separator.md)** |  |  |  |  |  |  |  |  | v1 | v1 |
| **[포함](separator.md)** |  |  |  |  |  |  |  |  |  | v1 |

## 설명서 {#documentation}

[핵심 구성 요소를](authoring.md) 사용하여 작성하는 작업은 핵심 구성 요소의 사용 방법과 컨텐츠 작성자 및 템플릿 작성자에게 표시되는 기능에 대해 설명합니다. 각 구성 요소는 자세히 설명되어 있습니다.

[구성 요소](http://opensource.adobe.com/aem-core-wcm-components/library.html) 라이브러리는 대부분의 핵심 구성 요소의 현재 버전을 보여주는 쇼케이스로, 구성 요소를 사용하는 방법을 보여 줍니다.

[핵심 구성 요소](developing.md) 개발에서는 핵심 구성 요소의 기술 기능, 프로젝트에서 이러한 구성 요소를 사용하는 방법, 사용자 정의 방법 및 우수 사례에 대해 설명합니다.

[핵심 구성 요소 소개에서는](introduction.md) 버전, 사용 사례 및 지원 간에 핵심 구성 요소 호환성에 대한 개요를 제공합니다.

[WKND 자습서는](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html) 핵심 구성 요소 사용을 포함하여 AEM용 개발을 위한 유용한 단계별 소개입니다.

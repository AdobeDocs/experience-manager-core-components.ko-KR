---
title: 구성 요소 버전
description: 핵심 구성 요소는 동일한 핵심 구성 요소의 두 개 이상의 버전을 포함할 수 있는 릴리스로 게시됩니다. 이 문서에서는 릴리스 및 버전에 대해 설명하고 핵심 구성 요소 및 AEM과의 호환성을 이해하는 방법을 설명합니다.
translation-type: tm+mt
source-git-commit: cef65c3fdf99130086136fe9019ca759bbf1926c
workflow-type: tm+mt
source-wordcount: '1717'
ht-degree: 25%

---


# 구성 요소 버전 {#core-components-versions}

핵심 구성 요소의 현재 릴리스는 2.10.0이며 Cloud Service [및](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html) 온프레미스 AEM [](https://docs.adobe.com/content/help/en/experience-manager-65/user-guide/home.html) 설치로서 AEM과 호환됩니다. 릴리스 2.0.0에 대한 중요한 업데이트로 2020년 6월에 출시되었습니다. 릴리스 2.0.0에서는 기존 구성 요소의 v2 업데이트와 함께 새로운 구성 요소를 도입했습니다.

## 릴리스 내역 및 호환성 {#release-history-and-compatibility}

핵심 구성 요소는 AEM 6.3에서 처음 릴리스되었으며, 지원되는 모든 AEM 버전과 유연하고 호환되도록 설계되었습니다. 이러한 구성 요소 릴리스에는 동일한 구성 요소의 여러 버전이 포함될 수 있습니다.

다음 표에서는 릴리스에 포함된 구성 요소 버전과 함께 핵심 구성 요소 릴리스의 호환성을 보여줍니다.

### 릴리스 내역 및 요구 사항 {#release-history-requirements}

전체 릴리스 세부 [정보와 함께 GitHub에서](https://github.com/adobe/aem-core-wcm-components/releases)사용할 수 있는 컨텐츠가 있는 다음 표는 핵심 구성 요소의 릴리스 및 AEM 릴리스 및 Java 버전과의 호환성에 대한 개요를 제공합니다.

| 릴리스 | 설명 | AEM 6.3 | AEM 6.4 | AEM 6.5 | 클라우드 서비스로서의 AEM | Java | 릴리스 날짜 |
|---|---|---|---|---|---|---|---|
| [2.10.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.10.0) | 이 릴리스에서는 PDF 뷰어 구성 요소가 도입되었습니다. | - | 6.4.4.0+ | 6.5.0.0+ | 지속적인 | 8, 11 | 2020년 6월 17일 |
| [2.9.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.9.0) | 이 릴리스는 Adobe 클라이언트 데이터 레이어와의 통합을 활성화했으며 진행률 표시줄 구성 요소를 도입했습니다. | - | 6.4.4.0+ | 6.5.0.0+ | 지속적인 | 8, 11 | 2020년 5월 29일 |
| [2.8.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.8.0) | 이 릴리스는 작은 개선 사항이 있는 수정 사항에 중점을 두었습니다. | 6.3.3.4+ | 6.4.4.0+ | 6.5.0.0+ | 지속적인 | 8, 11 | 2019년 12월 5일 |
| [2.7.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.7.0) | 이 릴리스에서는 새로운 포함 구성 요소가 도입되었습니다. | 6.3.3.4+ | 6.4.4.0+ | 6.5.0.0+ | 지속적인 | 8, 11 | 2019년 9월 25일 |
| [2.6.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.6.0) | 이 릴리스에서는 새로운 경험 조각 구성 요소가 도입되었습니다. | 6.3.3.4+ | 6.4.4.0+ | 6.5.0.0+ | 지속적인 | 8, 11 | 2019년 9월 6일 |
| [2.5.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.5.0) | 이 릴리스에서는 새로운 아코디언, 단추, 컨테이너 및 다운로드 구성 요소가 도입되었습니다. | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | 지속적인 | 8, 11 | 2019년 6월 25일 |
| [2.4.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.4.0) | 이 릴리스에서는 컨텐츠 조각 목록 구성 요소가 도입되었습니다. | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | 지속적인 | 8, 11 | 2019년 5월 7일 |
| [2.3.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.2) | 이 릴리스에서는 구성 요소 라이브러리에 대한 구체화에 중점을 두었으며 구분 문자 구성 요소에 대한 일부 기능 개선 사항도 포함되어 있습니다 | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | 지속적인 | 8 | 2019년 3월 14일 |
| [2.3.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.0) | 이 릴리스는 구성 요소 라이브러리 및 새로운 구분 문자 구성 요소를 소개합니다. 또한 이미지 구성 요소에 대한 일부 기능 개선 사항도 포함합니다 | 6.3.3.0+ | 6.4.2.0+ | - | - | 8 | 2019년 2월 11일 |
| [2.2.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.2) | 이 릴리스는 주로 버그 수정에 중점을 두지만 Carousel 구성 요소에 대한 일부 기능 개선 사항을 포함합니다 | 6.3.3.0+ | 6.4.2.0+ | - | - | 8 | 2018년 11월 27일 |
| [2.2.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.0) | 새롭게 추가된 탭 및 회전판 구성 요소, 향상된 이미지, 페이지 및 제목 구성 요소 및 향상된 추적 | 6.3.3.0+ | 6.4.2.0+ | - | - | 8 | 2018년 10월 16일 |
| [2.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.1.0) | Teaser 구성 요소 도입, 이미지 구성 요소 개선 및 다양한 버그 수정 | 6.3.3.0+ | 6.4.2.0+ | - | - | 8 | 2018년 7월 13일 |
| [2.0.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.8) | 버그 수정 릴리스 | 6.3.2.0+ | 6.4.0.0+ | - | - | 8 | 2018년 6월 12일 |
| [2.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.6) | 향상된 추가 백그라운드 기능, 버그 수정 및 이미지 플립 지원을 비롯한 작은 향상 기능 | 6.3.2.0+ | 6.4.0.0+ | - | - | 8 | 2018년 4월 11일 |
| [2.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.4) | 주로 백그라운드 개선 사항, 버그 수정, 이미지, 페이지 및 컨텐츠 조각 구성 요소에 대한 일부 개선 사항 | 6.3.2.0+ | 6.4.0.0+ | - | - | 8 | 2018년 3월 7일 |
| [2.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.0) | 탐색, 언어 탐색 및 빠른 검색 구성 요소가 도입되었습니다. 모든 구성 요소에 대해 구현된 스타일 시스템입니다. | 6.3.2.0+ | 6.4.0.0+ | - | - | 8 | 2018년 1월 16일 |
| [1.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.1.0) | 모든 구성 요소에 대한 JSON 내보내기 구현, 컨텐츠 조각 구성 요소 소개 | 6.3.1.0 | 6.4.0.0+ | - | - | 8 | 2017년 10월 10일 |
| [1.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.6) | 이미지 구성 요소에 대한 몇 가지 수정 사항 | 6.3.0.0+ | 6.4.0.0+ | - | - | 8 | 2017년 8월 4일 |
| [1.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.4) | 페이지 구성 요소, 이미지 구성 요소, 다양한 전역 수정 사항 및 개선 사항 | 6.3.0.0+ | 6.4.0.0+ | - | - | 8 | 2017년 4월 26일 |
| [1.0.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.all-1.0.2) | 이미지 구성 요소의 애니메이션 GIF 이미지에 대한 수정 사항 | 6.3.0.0+ | 6.4.0.0+ | - | - | 7 | 2017년 3월 22일 |
| [1.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.0) | 핵심 구성 요소의 초기 릴리스 | 6.3.0.0+ | 6.4.0.0+ | - | - | 7 | 2017년 3월 20일 |

>[!NOTE]
>
>AEM과 마찬가지로 최신 수정 사항 및 기능을 활용하기 위해 개발자가 실행 중인 AEM 버전과 호환되는 [최신 릴리스 및 핵심 구성 요소](https://github.com/adobe/aem-core-wcm-components/releases/latest) 버전을 사용하는 것이 좋습니다.

### 구성 요소 버전 및 릴리스 {#component-versions-and-releases}

다음 표에서는 핵심 구성 요소의 릴리스에 포함된 구성 요소의 버전을 자세히 설명합니다.

|  | 릴리스 1.0.0 - 1.0.6 | 릴리스 1.1.0 | 릴리스 2.0.0 - 2.0.8 | 릴리스 2.1.0 | 릴리스 2.2.0-2.2.0 | 릴리스 2.3.0-2.3.2 | 릴리스 2.4.0 | 릴리스 2.5.0 | 릴리스 2.6.0 | 릴리스 2.7.0-2.8.0 | 릴리스 2.9.0+ |
|---|---|---|---|---|---|---|---|---|---|---|---|
| **[페이지](components/page.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[제목](components/title.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[이미지](components/image.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[목록](components/list.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[탐색 표시](components/breadcrumb.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[소셜 미디어 공유](components/sharing.md)** | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[양식 컨테이너](components/forms/form-container.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[양식 텍스트](components/forms/form-text.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[양식 옵션](components/forms/form-options.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[숨겨진 양식](components/forms/form-hidden.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[양식 단추](components/forms/form-button.md)** | v1 | v1 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 | v1, v2 |
| **[콘텐츠 조각](components/content-fragment-component.md)** |  | 샌드박스 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1, v2 | v1, v2 |
| **[탐색](components/navigation.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[언어 탐색](components/language-navigation.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[빠른 검색](components/quick-search.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[티저](components/teaser.md)** |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[탭](components/tabs.md)** |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[회전판](components/carousel.md)** |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[분리자](components/separator.md)** |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 |
| **[콘텐츠 조각 목록](components/content-fragment-list.md)** |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 |
| **[어코디언](components/accordion.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 |
| **[단추](components/button.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 |
| **[컨테이너](components/container.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 |
| **[다운로드](components/download.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 |
| **[경험 조각](components/experience-fragment.md)** |  |  |  |  |  |  |  |  | v1 | v1 | v1 |
| **[포함](components/embed.md)** |  |  |  |  |  |  |  |  |  | v1 | v1 |
| **[진행률 표시줄](components/progress-bar.md)** |  |  |  |  |  |  |  |  |  |  | v1 |
| **[PDF 뷰어](components/pdf-viewer.md)** |  |  |  |  |  |  |  |  |  |  | v1 |

## 버전 및 릴리스 {#versions-and-releases}

핵심 구성 요소는 GitHub를 통해 배포됩니다. 이를 통해 Adobe는 구성 요소에 기능을 보다 신속하게 추가할 수 있으며 AEM 릴리스 주기 외부에서 커뮤니티 입력을 허용할 수도 있습니다.

핵심 구성 요소는 호환되는 정의된 AEM 버전에서 사용할 수 있습니다. 즉, 하나의 AEM 버전이 여러 버전 또는 핵심 구성 요소의 릴리스를 지원할 수 있습니다. 이는 특정 버전의 AEM에 연결된 이전 Foundation 구성 요소보다 더 많은 유연성을 제공합니다.

### 버전 {#versions}

핵심 구성 요소의 주 이터레이션은 **버전입니다**. 각 구성 요소에는 버전이 있습니다. 버전은 **v** 와 v1 및 v2와 같은 0이 아닌 양의 정수가 추가되어 표시됩니다. 버전은 이전 버전과 호환하지 않는 변경 사항에 대해서만 증가하며, 일반적으로 새로운 기능과 기능을 도입하기 위한 경우가 많습니다.

개발자와 관리자는 해당 리소스 유형 경로 및 구현의 정규화된 Java 클래스 이름에서 여러 가지 핵심 구성 요소의 버전을 인식할 수 있습니다. 이 버전 번호는 [의미 체계 버전 관리 지침에 의해 정의된 주요 버전을 나타냅니다](https://semver.org/).

핵심 구성 요소 버전에 대한 자세한 내용은 핵심 구성 요소의 [개발자 설명서를 참조하십시오](developing/guidelines.md).

### 릴리스 {#releases}

핵심 구성 요소는 **릴리스를 통해** 사용할 수 [있으며 GitHub에서 사용할 수 있는 실제 게시된 객체를 나타냅니다](https://github.com/adobe/aem-core-wcm-components/releases). 릴리스는 X.Y.Z 형식의 십진수로 표시되며 모든 핵심 구성 요소를 산출물 패키지로 수집합니다.

* **주요 릴리스는** 표준 버그 수정 뿐만 아니라 완전히 새로운 구성 요소와 함께 기존 구성 요소의 새로운 버전을 도입할 수 있습니다. 이것은 릴리즈 번호의 X 구성 요소에서 증가하여 나타냅니다.
* **중요 릴리스에서는** 버그 수정과 함께 기존 버전의 구성 요소에 새로운 기능을 적용할 수 있습니다. 릴리스 번호의 Y 구성 요소의 증분으로 표시됩니다.
* **일부 릴리스에는** 버그 수정만 포함되어 있습니다. 이것은 릴리즈 번호의 Z 구성 요소의 증분으로 표시됩니다.

>[!NOTE]
>
>릴리스에는 동일한 구성 요소의 여러 버전이 포함될 수 있습니다.
>
>동일한 버전의 구성 요소는 여러 릴리스에 표시될 수 있습니다.

## 핵심 구성 요소 지원 {#core-components-support}

핵심 구성 요소는 AEM의 필수적인 부분으로, 빠른 시작의 일부로 전달된 것처럼 동일한 이용 약관에 따라 지원됩니다.

다른 제품 기능과 마찬가지로 수명 종료에 대한 일반적인 규칙은 다음과 같습니다.

* 구성 요소는 제거되기 전에 먼저 사용을 중단한다고 발표했습니다.
* 공지 후 가장 빠른 시일 내에 AEM 릴리스에서 제거됩니다.

따라서 지원이 종료되기 전에 고객에게 구성 요소의 새 버전으로 이동할 수 있는 릴리스 주기를 1개 이상 제공합니다.

각 구성 요소의 버전은 지원되는 AEM 버전을 명확하게 설명합니다. AEM 버전에 대한 지원이 중단되면 해당 버전의 AEM에 대한 핵심 구성 요소에 대한 지원도 중단됩니다.

구성 요소 사용자 정의에 대한 자세한 내용은 관련 핵심 구성 요소 버전의 [핵심 구성 요소 사용자 정의](developing/customizing.md)를 참조하십시오.

## 기초 구성 요소 지원 {#foundation-component-support}

기초 구성 요소는 많은 버전에 대해 프로젝트 개발 기준 역할을 했기 때문에 가까운 미래에도 계속 지원됩니다.

However, Adobe&#39;s development emphasis has shifted to the Core Components and new features will be added to them, whereas [nearly all Foundation Components have been deprecated with AEM 6.5](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/default-components-foundation.html) and only bug fixes will be made to the Foundation Components going forward.

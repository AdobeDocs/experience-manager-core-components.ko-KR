---
title: 구성 요소 버전
description: 핵심 구성 요소는 동일한 핵심 구성 요소의 두 개 이상의 버전을 포함할 수 있는 릴리스로 게시됩니다. 이 문서에서는 릴리스 및 버전에 대해 설명하고 핵심 구성 요소 및 AEM과의 호환성을 이해하는 방법을 설명합니다.
translation-type: tm+mt
source-git-commit: c64276bb95aeaef4223fc2a0dc2c3cfdf8609f5a
workflow-type: tm+mt
source-wordcount: '1848'
ht-degree: 22%

---


# 구성 요소 버전 {#core-components-versions}

핵심 구성 요소의 현재 릴리스는 2.12.1이며 Cloud Service [및](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html) 온프레미스 AEM [설치로서](https://docs.adobe.com/content/help/ko-KR/experience-manager-65/user-guide/home.html) AEM과 호환됩니다. 2.12.0에 대한 패치 릴리스로 2020년 11월에 출시되었습니다. 릴리스 2.12.0에서는 양식, 메타데이터 및 데이터 레이어에 대한 몇 가지 새로운 기능을 도입했습니다.

## 릴리스 내역 및 호환성 {#release-history-and-compatibility}

핵심 구성 요소는 지원되는 모든 AEM 버전과 유연하게 호환되도록 설계되었습니다. 이러한 구성 요소 릴리스에는 동일한 구성 요소의 여러 버전이 포함될 수 있습니다.

다음 표에서는 릴리스에 포함된 구성 요소 버전과 함께 핵심 구성 요소 릴리스의 호환성을 보여줍니다.

### 릴리스 내역 및 요구 사항 {#release-history-requirements}

전체 릴리스 세부 [정보와 함께 GitHub에서](https://github.com/adobe/aem-core-wcm-components/releases)사용할 수 있는 컨텐츠는 다음 표에 핵심 구성 요소의 릴리스 및 AEM 릴리스 및 Java 버전과의 호환성에 대한 개요를 제공합니다.

| 릴리스 | 설명 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service | Java | 릴리스 날짜 |
|---|---|---|---|---|---|---|
| [2.12.1](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.11.1) | 이미지 구성 요소의 주요 버그를 수정하는 2.12.0용 패치 릴리스입니다. | 6.4.8.1+ * | 6.5.5.0+ * | 지속적인 | 8, 11 | 2020년 11월 5일 |
| [2.12.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.11.0) | 이 릴리스 [는 새로운 POST 양식 핸들러를 도입했습니다.](/help/components/forms/form-container.md#post-data) 컨텍스트 인식 구성을 통해 사용자 지정 CSS, Javascript 및 메타데이터 [태그를 포함하는 기능;](/help/developing/including-clientlibs.md#context-aware-loading) 사용자 `DataLayerBuilder` 정의 구성 요소에서 데이터 [레이어 통합을 간소화하는 유틸리티](/help/developing/data-layer/integrations.md#enabling-custom-components) | 6.4.8.1+ * | 6.5.5.0+ * | 지속적인 | 8, 11 | 2020년 10월 29일 |
| [2.11.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.11.0) | 이 릴리스에서는 [AMP 지원이 도입되었습니다.](/help/developing/amp.md) | 6.4.8.1+ * | 6.5.5.0+ * | 지속적인 | 8, 11 | 2020년 7월 20일 |
| [2.10.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.10.0) | 이 릴리스에서는 [PDF 뷰어 구성 요소가 도입되었습니다.](/help/components/pdf-viewer.md) | 6.4.8.1+ | 6.5.5.0+ | 지속적인 | 8, 11 | 2020년 6월 17일 |
| [2.9.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.9.0) | 이 릴리스는 [Adobe 클라이언트 데이터 레이어와의 통합을 활성화했으며](/help/developing/data-layer/overview.md) 진행률 [표시줄 구성 요소를 도입했습니다.](/help/components/progress-bar.md) | 6.4.8.0+ | 6.5.4.0+ | 지속적인 | 8, 11 | 2020년 5월 29일 |
| [2.8.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.8.0) | 이 릴리스는 작은 개선 사항이 있는 수정 사항에 중점을 두었습니다. | 6.4.4.0+ | 6.5.0.0+ | 지속적인 | 8, 11 | 2019년 12월 5일 |
| [2.7.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.7.0) | 이 릴리스에서는 새로운 [포함 구성 요소가 도입되었습니다.](/help/components/embed.md) | 6.4.4.0+ | 6.5.0.0+ | 지속적인 | 8, 11 | 2019년 9월 25일 |
| [2.6.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.6.0) | 이 릴리스에서는 새로운 [경험 조각 구성 요소가 도입되었습니다.](/help/components/experience-fragment.md) | 6.4.4.0+ | 6.5.0.0+ | 지속적인 | 8, 11 | 2019년 9월 6일 |
| [2.5.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.5.0) | 이 릴리스에서는 새로운 [아코디언,](/help/components/accordion.md) [단추,](/help/components/button.md) [컨테이너](/help/components/container.md) 및 [다운로드 구성 요소를도입했습니다.](/help/components/download.md) | 6.4.2.0+ | 6.5.0.0+ | 지속적인 | 8, 11 | 2019년 6월 25일 |
| [2.4.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.4.0) | 이 릴리스에서는 [컨텐츠 조각 목록 구성 요소를 도입했습니다.](/help/components/content-fragment-list.md) | 6.4.2.0+ | 6.5.0.0+ | 지속적인 | 8, 11 | 2019년 5월 7일 |
| [2.3.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.2) | 이 릴리스는 구성 요소 [라이브러리에 대한 구체화에 중점을 두었으며](https://aemcomponents.dev) 분리 [구성 요소에 대한 일부 기능 개선 사항도 포함되어 있습니다.](/help/components/separator.md) | 6.4.2.0+ | 6.5.0.0+ | 지속적인 | 8 | 2019년 3월 14일 |
| [2.3.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.0) | 이 릴리스는 [구성 요소 라이브러리](https://aemcomponents.dev) 와 새로운 [구분 문자 구성 요소](/help/components/separator.md) 소개 [에 중점을 두었으며이미지 구성 요소에 대한 일부 기능 개선 사항도포함합니다.](/help/components/image.md) | 6.4.2.0+ | - | - | 8 | 2019년 2월 11일 |
| [2.2.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.2) | 이 릴리스에는 주로 버그 수정에 중점을 두지만 회전판 구성 요소에 대한 일부 기능 개선 사항도 [포함되어 있습니다.](/help/components/carousel.md) | 6.4.2.0+ | - | - | 8 | 2018년 11월 27일 |
| [2.2.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.0) | 이번 릴리스에서는 [탭 구성 요소](/help/components/tabs.md)[및](/help/components/carousel.md) 회전판 구성 요소 [](/help/components/image.md) 와 [이미지 구성 요소,](/help/components/page.md) 페이지 구성 요소, [페이지 구성 요소,](/help/components/title.md) 및 향상된 제목 구성 요소 및 향상된 추적 기능이도입되었습니다. | 6.4.2.0+ | - | - | 8 | 2018년 10월 16일 |
| [2.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.1.0) | 이 릴리스에서는 [이미지 구성 요소](/help/components/teaser.md) 및 많은 버그 수정 사항과 함께 [티저 구성](/help/components/image.md) 요소를도입했습니다. | 6.4.2.0+ | - | - | 8 | 2018년 7월 13일 |
| [2.0.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.8) | 버그 수정 릴리스였습니다. | 6.4.0.0+ | - | - | 8 | 2018년 6월 12일 |
| [2.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.6) | 이 릴리스는 [이미지 구성 요소의 이미지 플립 지원 등 백그라운드 개선, 버그 수정 및 작은 개선 사항을 추가했습니다.](/help/components/image.md) | 6.4.0.0+ | - | - | 8 | 2018년 4월 11일 |
| [2.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.4) | 이 릴리스는 주로 백그라운드 개선 사항, 버그 수정, [이미지 구성 요소,](/help/components/image.md) 페이지 구성 요소 및 [컨텐츠 조각 구성 요소](/help/components/page.md) 에 대한 일부 [일부 개선사항에 중점을두었습니다.](/help/components/content-fragment-component.md) | 6.4.0.0+ | - | - | 8 | 2018년 3월 7일 |
| [2.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.0) | 이 릴리스에서는 [탐색 구성 요소,](/help/components/navigation.md) [언어 탐색 구성 요소](/help/components/language-navigation.md) 및 [](/help/components/quick-search.md) 빠른 검색 구성 요소를 [소개하고 모든 구성 요소에 대해](/help/get-started/authoring.md#component-styling) 스타일 시스템을 구현했습니다. | 6.4.0.0+ | - | - | 8 | 2018년 1월 16일 |
| [1.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.1.0) | 이 릴리스는 모든 구성 요소에 대해 JSON 내보내기를 구현하고 [컨텐츠 조각 구성 요소를 도입합니다.](/help/components/content-fragment-component.md) | 6.4.0.0+ | - | - | 8 | 2017년 10월 10일 |
| [1.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.6) | 이 릴리스에서는 [이미지 구성 요소에 대한 몇 가지 수정 사항이 추가되었습니다.](/help/components/image.md) | 6.4.0.0+ | - | - | 8 | 2017년 8월 4일 |
| [1.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.4) | 이 릴리스에는 [페이지 구성 요소,](/help/components/page.md) 이미지 구성 요소 [에](/help/components/image.md) 대한 수정 사항,다양한 전역 수정 사항 및 개선 사항이 추가되었습니다. | 6.4.0.0+ | - | - | 8 | 2017년 4월 26일 |
| [1.0.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.all-1.0.2) | 이 릴리스에서는 이미지 구성 요소의 애니메이션 GIF 이미지에 대한 수정 사항이 [추가되었습니다.](/help/components/image.md) | 6.4.0.0+ | - | - | 7 | 2017년 3월 22일 |
| [1.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.0) | 핵심 구성 요소의 초기 릴리스. | 6.4.0.0+ | - | - | 7 | 2017년 3월 20일 |

>[!NOTE]
>
>(*) 버전 2.11.0부터 `org.apache.sling.models.impl` 버전 1.4.12 이상이 필요합니다(SLING- [8781](https://issues.apache.org/jira/browse/SLING-8781)때문). 이 서비스는 향후 서비스 팩에서 AEM 6.4 및 6.5용으로 제공됩니다. 그때까지 Sling Models 번들은 패키지에 `core.wcm.components.all` 포함됩니다.

>[!TIP]
>
>AEM에서와 마찬가지로, 개발자는 최신 수정 사항 및 기능을 활용하기 위해 실행 중인 AEM 버전과 호환되는 [최신 릴리스와 버전의 핵심 구성](https://github.com/adobe/aem-core-wcm-components/releases/latest) 요소를 사용하는 것이 좋습니다.

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

핵심 구성 요소는 GitHub를 통해 배포됩니다. 이를 통해 Adobe은 구성 요소에 기능을 보다 신속하게 추가할 수 있고 AEM 릴리스 주기 외부에서 커뮤니티 입력을 허용할 수 있습니다.

핵심 구성 요소는 호환되는 정의된 AEM 버전에서 사용할 수 있습니다. 즉, 한 AEM 버전이 여러 버전 또는 핵심 구성 요소의 릴리스를 지원할 수 있습니다. 이는 특정 버전의 AEM에 연결된 이전 Foundation Components보다 더 많은 유연성을 제공합니다.

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

Adobe의 개발 강조가 핵심 구성 요소로 전환되었으며 새로운 기능은 계속 추가될 예정입니다.

[거의 모든 Foundation 구성 요소는 AEM 6.5에서 더 이상 사용되지 않으며](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/default-components-foundation.html) Foundation 구성 요소의 경우 주요 버그 수정만 고려됩니다.

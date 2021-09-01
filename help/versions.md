---
title: 구성 요소 버전
description: 코어 구성 요소는 동일한 핵심 구성 요소의 두 개 이상의 버전을 포함할 수 있는 릴리스로 게시됩니다. 이 문서에서는 릴리스 및 버전이 무엇이고 핵심 구성 요소 및 AEM와의 호환성을 이해하는 방법에 대해 설명합니다.
role: Architect, Developer, Admin, User
exl-id: 7d4dbe46-4013-4217-b815-cdb1462072c6
source-git-commit: 5271174f5c325a9793dc155c763054752c7308b8
workflow-type: tm+mt
source-wordcount: '2275'
ht-degree: 21%

---

# 구성 요소 버전 {#core-components-versions}

코어 구성 요소의 현재 릴리스는 2.17.8이며 [AEM as a1/> 및 [온-프레미스 AEM](https://docs.adobe.com/content/help/ko-KR/experience-manager-65/user-guide/home.html) 설치와 호환됩니다.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html)

## 릴리스 내역 및 호환성 {#release-history-and-compatibility}

코어 구성 요소는 지원되는 모든 AEM 버전과 유연하고 호환되도록 설계되었습니다. 이러한 이유로 구성 요소 릴리스는 동일한 구성 요소의 여러 버전을 포함할 수 있습니다.

다음 표에서는 릴리스에 포함된 구성 요소 버전과 함께 코어 구성 요소 릴리스의 호환성을 보여줍니다.

### 릴리스 내역 및 요구 사항 {#release-history-requirements}

다음 표는 전체 릴리스 세부 정보](https://github.com/adobe/aem-core-wcm-components/releases)가 있는 GitHub에서 사용 가능한 [이 포함된 내용으로, 코어 구성 요소 릴리스의 개요와 AEM 릴리스 및 Java 버전과의 호환성을 설명합니다.

| 릴리스 | 설명 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service | Java | 릴리스 날짜 |
|---|---|---|---|---|---|---|
| [2.17.10](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.10) | 이 패치는 [List](/help/components/list.md) 및 [Navigation](/help/components/navigation.md) 구성 요소를 개선하여 리디렉션 대상에 대한 외부 URL을 표시하고 [Teaser](/help/components/teaser.md) 구성 요소에 대한 페이지 이미지 상속을 활성화하며 추가 버그 수정을 포함합니다. | 6.4.8.4+ * | 6.5.6.0+ * | 계속 | 8,11 | 2021년 8월 31일 |
| [2.17.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.8) | 이 패치 릴리스 이전에 도입된 호환되지 않는 변경 사항을 수정하기 위한 패치 릴리스입니다. | 6.4.8.4+ * | 6.5.6.0+ * | 계속 | 8,11 | 2021년 8월 2일 |
| [2.17.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.6) | 이 패치 릴리스는 페이지에 대한 사이트 맵에 대한 지원을 추가하며 다양한 액세스 가능성 개선 사항을 포함합니다. | 6.4.8.4+ * | 6.5.6.0+ * | 계속 | 8,11 | 2021년 7월 29일 |
| [2.17.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.2) | 이 패치 릴리스에는 AEMaaCS에서 작동하지 않는 [데이터 레이어](/help/developing/data-layer/overview.md)에 대한 수정 사항이 포함되어 있습니다. | 6.4.8.4+ * | 6.5.6.0+ * | 계속 | 8,11 | 2021년 7월 8일 |
| [2.17.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.0) | 이 릴리스에는 링크 핸들러 기능을 지원하는 많은 새 구성 요소 버전의 기술 미리 보기가 포함되며 [페이지 구성 요소에 대한 주요 이미지 기능의 기술 미리 보기가 포함됩니다.](/help/components/page.md) 몇 가지 버그 수정 사항이 포함되어 있습니다. | 6.4.8.4+ * | 6.5.6.0+ * | 계속 | 8,11 | 2021년 6월 16일 |
| [2.16.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.16.4) | 새 링크 핸들러 문제를 해결하는 패치 릴리스입니다. | 6.4.8.1+ * | 6.5.5.0+ * | 계속 | 8,11 | 2021년 5월 19일 |
| [2.16.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.16.2) | 이는 주로 새 링크 처리기의 문제를 해결하는 패치 릴리스이며 [PWA에 대한 다중 페이지 응용 프로그램을 지원하도록 기능이 추가되었습니다.](/help/components/page.md#pwa-support) | 6.4.8.1+ * | 6.5.5.0+ * | 계속 | 8,11 | 2021년 5월 15일 |
| [2.16.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.16.0) | 이 릴리스는 기존 구성 요소에 새 링크 핸들러를 도입했을 뿐만 아니라 액세스 가능성 개선에 중점을 두고 있습니다. | 6.4.8.1+ * | 6.5.5.0+ * | 계속 | 8,11 | 2021년 4월 22일 |
| [2.15.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.15.2) | 이는 [데이터 계층](/help/developing/data-layer/overview.md) 이전 버전과의 호환성을 주로 해결하고 특정 상황에서 실패하는 IT 테스트와 관련된 문제를 해결하는 패치 릴리스입니다. | 6.4.8.1+ * | 6.5.5.0+ * | 계속 | 8,11 | 2021년 3월 16일 |
| [2.15.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.15.0) | 이 릴리스에는 페이지 구성 요소](/help/components/page.md#pwa-support)의 [점진적 웹 앱(PWA)에 대한 지원이 포함되며, [Adobe 데이터 레이어 버전 2.0.0을 지원합니다.](/help/developing/data-layer/overview.md) | 6.4.8.1+ * | 6.5.5.0+ * | 계속 | 8,11 | 2021년 2월 23일 |
| [2.14.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.14.0) | 이 릴리스에는 [포함 구성 요소](/help/components/embed.md)에 대한 새 옵션이 포함되어 있으며, 많은 문제를 해결할 뿐만 아니라 [페이지](/help/components/page.md) 수준에서 브랜드 개요 를 소개합니다. | 6.4.8.1+ * | 6.5.5.0+ * | 계속 | 8,11 | 2021년 2월 9일 |
| [2.13.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.13.2) | AEMaaCS에서 사용할 때 RTE와 관련된 문제를 해결하는 패치 릴리스입니다 | 6.4.8.1+ * | 6.5.5.0+ * | 계속 | 8,11 | 2020년 12월 16일 |
| [2.13.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.13.0) | 이 릴리스에는 [이미지 구성 요소에 대한 새 Dynamic Media 기능이 포함되어 있습니다.](/help/components/image.md) | 6.4.8.1+ * | 6.5.5.0+ * | 계속 | 8,11 | 2020년 12월 4일 |
| [2.12.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.2) | 사소한 수정 사항이 포함된 2.12.0용 패치 릴리스입니다. | 6.4.8.1+ * | 6.5.5.0+ * | 계속 | 8,11 | 2020년 11월 11일 |
| [2.12.1](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.1) | [이미지 구성 요소의 주요 버그를 수정하는 2.12.0용 패치 릴리스입니다.](/help/components/image.md) | 6.4.8.1+ * | 6.5.5.0+ * | 계속 | 8,11 | 2020년 11월 5일 |
| [2.12.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.0) | 이 릴리스에서는 [새 POST 양식 핸들러;](/help/components/forms/form-container.md#post-data) 컨텍스트 인식 구성을 통해 사용자 지정 CSS, Javascript 및 메타데이터 [태그를 포함하는 기능;](/help/developing/including-clientlibs.md#context-aware-loading) 및 `DataLayerBuilder` 유틸리티를 도입하여 사용자 지정 구성 요소에서 데이터 레이어 통합을 단순화합니다.](/help/developing/data-layer/integrations.md#enabling-custom-components)[ | 6.4.8.1+ * | 6.5.5.0+ * | 계속 | 8,11 | 2020년 10월 29일 |
| [2.11.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.11.0) | 이 릴리스에서는 [AMP 지원이 도입되었습니다.](/help/developing/amp.md) | 6.4.8.1+ * | 6.5.5.0+ * | 계속 | 8,11 | 2020년 7월 20일 |
| [2.10.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.10.0) | 이 릴리스에서는 [PDF 뷰어 구성 요소가 도입되었습니다.](/help/components/pdf-viewer.md) | 6.4.8.1+ | 6.5.5.0+ | 계속 | 8,11 | 2020년 6월 17일 |
| [2.9.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.9.0) | 이 릴리스를 통해 [Adobe 클라이언트 데이터 레이어](/help/developing/data-layer/overview.md)와의 통합이 활성화되고 [진행률 표시줄 구성 요소가 도입되었습니다.](/help/components/progress-bar.md) | 6.4.8.0+ | 6.5.4.0+ | 계속 | 8,11 | 2020년 5월 29일 |
| [2.8.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.8.0) | 이 릴리스는 작은 개선 사항이 있는 수정 사항에 중점을 둡니다. | 6.4.4.0+ | 6.5.0.0+ | 계속 | 8,11 | 2019년 12월 5일 |
| [2.7.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.7.0) | 이 릴리스에서는 새 [포함 구성 요소가 도입되었습니다.](/help/components/embed.md) | 6.4.4.0+ | 6.5.0.0+ | 계속 | 8,11 | 2019년 9월 25일 |
| [2.6.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.6.0) | 이 릴리스에서는 새 [경험 조각 구성 요소가 도입되었습니다.](/help/components/experience-fragment.md) | 6.4.4.0+ | 6.5.0.0+ | 계속 | 8,11 | 2019년 9월 6일 |
| [2.5.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.5.0) | 이 릴리스에서는 새 [아코디언,](/help/components/accordion.md) [Button,](/help/components/button.md) [컨테이너,](/help/components/container.md) 및 [구성 요소 다운로드가 도입되었습니다.](/help/components/download.md) | 6.4.2.0+ | 6.5.0.0+ | 계속 | 8,11 | 2019년 6월 25일 |
| [2.4.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.4.0) | 이 릴리스에서는 [컨텐츠 조각 목록 구성 요소가 도입되었습니다.](/help/components/content-fragment-list.md) | 6.4.2.0+ | 6.5.0.0+ | 계속 | 8,11 | 2019년 5월 7일 |
| [2.3.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.2) | 이 릴리스는 [구성 요소 라이브러리,](https://aemcomponents.dev)에 대한 개선 사항에 중점을 두지만, [구분 기호 구성 요소에 대한 몇 가지 기능 개선 사항도 포함합니다.](/help/components/separator.md) | 6.4.2.0+ | 6.5.0.0+ | 계속 | 8 | 2019년 3월 14일 |
| [2.3.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.0) | 이 릴리스는 [구성 요소 라이브러리](https://aemcomponents.dev)에 초점을 맞추고 새로운 [구분 기호 구성 요소](/help/components/separator.md)를 도입했지만, [이미지 구성 요소에 대한 몇 가지 기능 개선 사항도 포함되어 있습니다.](/help/components/image.md) | 6.4.2.0+ | - | - | 8 | 2019년 2월 11일 |
| [2.2.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.2) | 이 릴리스는 주로 버그 수정에 중점을 두지만, [캐러셀 구성 요소에 대한 몇 가지 기능 개선 사항이 포함되어 있습니다.](/help/components/carousel.md) | 6.4.2.0+ | - | - | 8 | 2018년 11월 27일 |
| [2.2.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.0) | 이 릴리스에서는 [탭 구성 요소](/help/components/tabs.md) 및 [회전 구성 요소](/help/components/carousel.md)와 [이미지 구성 요소,](/help/components/image.md) [페이지 구성 요소,](/help/components/page.md) 및 [제목 구성 요소](/help/components/title.md)에 대한 개선 사항이 소개되었습니다. | 6.4.2.0+ | - | - | 8 | 2018년 10월 16일 |
| [2.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.1.0) | 이 릴리스에서는 [이미지 구성 요소](/help/components/image.md)에 대한 개선 사항과 다양한 버그 수정이 함께 [Teaser 구성 요소](/help/components/teaser.md)가 도입되었습니다. | 6.4.2.0+ | - | - | 8 | 2018년 7월 13일 |
| [2.0.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.8) | 버그 수정 릴리스였습니다. | 6.4.0.0+ | - | - | 8 | 2018년 6월 12일 |
| [2.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.6) | 이 릴리스는 [이미지 구성 요소에서 이미지 뒤집기를 지원하는 등 후드형 개선 사항, 버그 수정 및 작은 개선 사항을 추가했습니다.](/help/components/image.md) | 6.4.0.0+ | - | - | 8 | 2018년 4월 11일 |
| [2.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.4) | 이 릴리스는 주로 후드형 개선 사항, 버그 수정 및 [이미지 구성 요소,](/help/components/image.md) [페이지 구성 요소,](/help/components/page.md) 및 [컨텐츠 조각 구성 요소에 대한 일부 개선 사항에 중점을 둡니다.](/help/components/content-fragment-component.md) | 6.4.0.0+ | - | - | 8 | 2018년 3월 7일 |
| [2.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.0) | 이 릴리스에서는 [탐색 구성 요소,](/help/components/navigation.md) [언어 탐색 구성 요소,](/help/components/language-navigation.md) 및 [빠른 검색 구성 요소](/help/components/quick-search.md)를 도입하고 모든 구성 요소에 대해 [스타일 시스템](/help/get-started/authoring.md#component-styling)을 구현했습니다. | 6.4.0.0+ | - | - | 8 | 2018년 1월 16일 |
| [1.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.1.0) | 이 릴리스는 모든 구성 요소에 대해 JSON 내보내기를 구현하고 [컨텐츠 조각 구성 요소를 도입합니다.](/help/components/content-fragment-component.md) | 6.4.0.0+ | - | - | 8 | 2017년 10월 10일 |
| [1.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.6) | 이 릴리스는 [이미지 구성 요소에 대한 몇 가지 수정 사항을 추가합니다.](/help/components/image.md) | 6.4.0.0+ | - | - | 8 | 2017년 8월 4일 |
| [1.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.4) | 이 릴리스에서는 [페이지 구성 요소,](/help/components/page.md) [이미지 구성 요소,](/help/components/image.md) 및 다양한 글로벌 수정 사항 및 개선 사항에 대한 수정 사항이 추가됩니다. | 6.4.0.0+ | - | - | 8 | 2017년 4월 26일 |
| [1.0.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.all-1.0.2) | 이 릴리스는 [이미지 구성 요소에 애니메이션 GIF 이미지에 대한 수정 사항을 추가합니다.](/help/components/image.md) | 6.4.0.0+ | - | - | 7 | 2017년 3월 22일 |
| [1.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.0) | 핵심 구성 요소의 초기 릴리스. | 6.4.0.0+ | - | - | 7 | 2017년 3월 20일 |

>[!NOTE]
>
>(*) 버전 2.11.0부터 `org.apache.sling.models.impl` 버전 1.4.12 이상이 필요합니다( [SLING-8781](https://issues.apache.org/jira/browse/SLING-8781)). 향후 서비스 팩에서 AEM 6.4 및 6.5용으로 제공됩니다. 그때까지 Sling 모델 번들은 `core.wcm.components.all` 패키지에 포함되어 있습니다.

>[!TIP]
>
>AEM에서와 마찬가지로, Adobe은 개발자가 최신 수정 사항 및 기능을 활용하기 위해 실행 중인 AEM 버전과 호환되는 코어 구성 요소](https://github.com/adobe/aem-core-wcm-components/releases/latest)의 최신 릴리스 및 버전을 사용할 것을 권장합니다.[

### 구성 요소 버전 및 릴리스 {#component-versions-and-releases}

다음 표에서는 코어 구성 요소 릴리스에 포함된 구성 요소 버전을 자세히 설명합니다.

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

코어 구성 요소는 GitHub를 통해 배포됩니다. 이렇게 하면 Adobe이 구성 요소에 기능을 더 빨리 추가하고 AEM 릴리스 주기 외부에서 커뮤니티 입력을 허용할 수도 있습니다.

핵심 구성 요소는 호환하는 정의된 AEM 버전에서 사용할 수 있게 됩니다. 즉, 하나의 AEM 버전에서 코어 구성 요소의 여러 버전 또는 릴리스를 지원할 수 있습니다. 이렇게 하면 특정 버전의 AEM에 연결된 이전 기초 구성 요소보다 더 유연하게 대처할 수 있습니다.

### 버전 {#versions}

코어 구성 요소의 주요 이터레이션은 **버전**&#x200B;입니다. 각 구성 요소에는 버전이 있습니다. 버전은 **v**&#x200B;에 v1 및 v2와 같은 0이 아닌 양의 정수가 추가되었다고 표시됩니다. 버전은 이전 버전과 호환되지 않는 변경 사항에만 증가되며, 일반적으로 새 기능 및 기능을 도입하기 위해 사용됩니다.

개발자 및 관리자는 리소스 유형 경로 및 구현의 정규화된 Java 클래스 이름에서 여러 개 핵심 구성 요소의 버전을 인식할 수 있습니다. 이 버전 번호는 [시맨틱 버전 관리 지침](https://semver.org/)에 정의된 주요 버전을 나타냅니다.

코어 구성 요소 버전에 대한 자세한 내용은 코어 구성 요소](developing/guidelines.md)의 [개발자 설명서를 참조하십시오.

### 릴리스 {#releases}

코어 구성 요소는 **릴리스** 및 [를 통해 사용할 수 있게 되며 GitHub](https://github.com/adobe/aem-core-wcm-components/releases)에서 사용할 수 있는 실제 게시된 아티팩트를 나타냅니다. 릴리스는 X.Y.Z 형식의 십진수로 표시되며 모든 코어 구성 요소를 산출물 패키지로 수집합니다.

* **주요** 릴리스에서는 완전히 새로운 구성 요소 및 표준 버그 수정 사항과 함께 기존 구성 요소의 새로운 버전을 도입할 수 있습니다. 이는 릴리스 번호의 X 구성 요소에서 증가하여 표시됩니다.
* **중요** 릴리스에서는 버그 수정 와 함께 기존 버전의 구성 요소에 새로운 기능을 도입할 수 있습니다. 이것은 릴리스 번호의 Y 구성 요소에서 증가분으로 표시됩니다.
* **사소한** 릴리스에는 버그 수정만 포함됩니다. 이것은 릴리스 번호의 Z 구성 요소에서 증가분으로 표시됩니다.

>[!NOTE]
>
>릴리스에는 동일한 구성 요소의 여러 버전이 포함될 수 있습니다.
>
>구성 요소의 동일한 버전이 여러 릴리스에 표시될 수 있습니다.

## 핵심 구성 요소 지원 {#core-components-support}

핵심 구성 요소는 AEM의 필수적인 부분으로, 빠른 시작의 일부로 전달된 것처럼 동일한 이용 약관에 따라 지원됩니다.

다른 제품 기능과 마찬가지로 수명 종료에 대한 일반적인 규칙은 다음과 같습니다.

* 구성 요소는 제거되기 전에 먼저 사용을 중단한다고 발표했습니다.
* 공지 후 가장 빠른 시일 내에 AEM 릴리스에서 제거됩니다.

따라서 지원이 종료되기 전에 고객에게 구성 요소의 새 버전으로 이동할 수 있는 릴리스 주기를 1개 이상 제공합니다.

각 구성 요소의 버전은 지원되는 AEM 버전을 명확하게 설명합니다. AEM 버전에 대한 지원이 중단되면 해당 버전의 AEM에 대한 핵심 구성 요소에 대한 지원도 중단됩니다.

구성 요소 사용자 정의에 대한 자세한 내용은 관련 핵심 구성 요소 버전의 [핵심 구성 요소 사용자 정의](developing/customizing.md)를 참조하십시오.

## 기초 구성 요소 지원 {#foundation-component-support}

Adobe의 개발 강조가 핵심 구성 요소로 변경되었으며 새 기능은 계속 추가됩니다.

[거의 모든 기초 구성 요소가 AEM 6.5에서 더 이상 사용되지 않으며](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/default-components-foundation.html) , 앞으로 기초 구성 요소에 대해 주요 버그 수정만 고려됩니다.

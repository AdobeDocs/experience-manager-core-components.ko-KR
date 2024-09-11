---
title: 핵심 구성 요소 버전
description: 핵심 구성 요소는 두 개 이상의 동일한 핵심 구성의 버전이 포함될 수 있는 릴리스로 게시됩니다. 이 문서에서는 릴리스 및 버전의 정의와 핵심 구성 요소 및 AEM의 호환성을 이해하는 방법에 대해 설명합니다.
role: Architect, Developer, Admin, User
exl-id: 7d4dbe46-4013-4217-b815-cdb1462072c6
source-git-commit: 1df528aec070c21c836f2fd6a92c7c6460f30798
workflow-type: ht
source-wordcount: '3087'
ht-degree: 100%

---

# 핵심 구성 요소 버전 {#core-components-versions}

핵심 구성 요소는 [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html?lang=ko) 및 [on-premise AEM](https://experienceleague.adobe.com/docs/experience-manager-65/user-guide/home.html?lang=ko) 설치와 호환됩니다.

## 릴리스 내역 및 호환성 {#release-history-and-compatibility}

핵심 구성 요소는 유연하고, 지원되는 모든 AEM 버전과 호환할 수 있도록 설계되었습니다. 이러한 이유로 구성 요소의 릴리스에는 동일한 구성 요소의 버전이 포함될 수 있습니다.

다음 표는 릴리스에 포함된 구성 요소 버전과 함께 핵심 구성 요소 릴리스의 호환성을 보여 줍니다.

### 릴리스 내역 및 요구 사항 {#release-history-requirements}

[전체 릴리스 정보와 함께 GitHub에 제공](https://github.com/adobe/aem-core-wcm-components/releases)되는 다음 목차에서는 핵심 구성 요소 릴리스와 AEM 릴리스 및 Java 버전의 호환성에 대한 개요를 제공합니다.

| 릴리스 | 설명 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service | Java | 릴리스 일자 |
|---|---|---|---|---|---|---|
| [2.26.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.26.0) | 이번 릴리스에서는 몇 가지 버그가 수정되었습니다. | - | 6.5.21.0+ | 반복 | 8, 11 | 2024년 7월 31일 |
| [2.25.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.25.4) | 일부 IT 오류를 수정하는 부 릴리스입니다. | - | 6.5.21.0+ | 반복 | 8, 11 | 2024년 5월 10일 |
| [2.25.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.25.2) | 일부 IT 오류를 수정하는 부 릴리스입니다. | - | 6.5.21.0+ | 반복 | 8, 11 | 2024년 5월 9일 |
| [2.25.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.25.0) | 이 릴리스에는 Dynamic Media에서 명명된 스마트 자르기에 대한 지원이 추가되었으며 성능 및 접근성 개선 사항과 다양한 버그 수정이 포함되었습니다. | - | 6.5.21.0+ | 반복 | 8, 11 | 2024년 5월 2일 |
| [2.24.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.24.6) | 이 패치 릴리스에는 데이터 레이어 초기화에 대한 개선 사항이 포함되어 있습니다. | - | 6.5.21.0+ | 반복 | 8, 11 | 2024년 4월 22일 |
| [2.24.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.24.4) | 이 패치 릴리스는 Sling 모델 초기화를 수정합니다. | - | 6.5.21.0+ | 반복 | 8, 11 | 2024년 4월 1일 |
| [2.24.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.24.2) | 이번 패치 릴리스는 통합 테스트의 안정성을 향상합니다. | - | 6.5.21.0+ | 반복 | 8, 11 | 2024년 2월 22일 |
| [2.24.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.24.0) | 이번 릴리스에는 Google 태그 관리자 데이터 레이어에 대한 지원이 추가되었으며 다양한 버그 수정이 포함되었습니다. | - | 6.5.21.0+ | 반복 | 8, 11 | 2024년 2월 14일 |
| [2.23.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.23.4) | 이번 패치 릴리스에는 다양한 버그 수정이 포함됩니다. | - | 6.5.17.0+ | 반복 | 8, 11 | 2023년 9월 15일 |
| [2.23.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.23.2) | 이 패치에서는 [이미지](/help/components/image.md) 및 [티저 구성 요소](/help/components/teaser.md)에 원격 자산에 대한 Dynamic Media 스마트 자르기가 추가되며 여러 버그가 수정됩니다. | - | 6.5.17.0+ | 반복 | 8, 11 | 2023년 8월 4일 |
| [2.23.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.23.0) | 이 릴리스에는 [차세대 Dynamic Media 원격 자산](/help/developing/remote-assets.md)에 대한 지원이 추가됩니다. | - | 6.5.17.0+ | 반복 | 8, 11 | 2023년 6월 6일 |
| [2.22.12](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.12) | 이 패치 릴리스는 두 가지 문제를 수정합니다. | - | 6.5.14.0+ | 반복 | 8, 11 | 2023년 5월 25일 |
| [2.22.10](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.10) | 이 패치 릴리스는 두 가지 회귀를 수정합니다. | - | 6.5.14.0+ | 반복 | 8, 11 | 2023년 5월 11일 |
| [2.22.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.8) | 이 패치 릴리스는 이전 릴리스에서 실수로 제거된 기능을 다시 가져옵니다. | - | 6.5.14.0+ | 반복 | 8, 11 | 2023년 5월 9일 |
| [2.22.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.6) | 이 패치 릴리스는 [컨테이너 구성 요소](/help/components/container.md)의 회귀를 수정합니다. | - | 6.5.14.0+ | 반복 | 8, 11 | 2023년 4월 21일 |
| [2.22.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.4) | 이는 [콘텐츠 조각 목록 구성 요소](/help/components/content-fragment-list.md)의 문제를 해결하기 위한 패치 릴리스입니다. | - | 6.5.14.0+ | 반복 | 8, 11 | 2023년 4월 5일 |
| [2.22.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.2) | 이는 2.22.0 버전에서 발생하는 두 가지 문제를 해결하기 위한 유지 관리 릴리스입니다. | - | 6.5.14.0+ | 반복 | 8, 11 | 2023년 3월 31일 |
| [2.22.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.22.0) | 이 릴리스에는 [티저](/help/components/teaser.md)에 대한 개선 사항, [PDF 뷰어](/help/components/pdf-viewer.md) 및 [캐러셀](/help/components/carousel.md) 업데이트와 더불어 새로운 버전의 [목록 구성 요소](/help/components/list.md)가 도입되었습니다. | - | 6.5.14.0+ | 반복 | 8, 11 | 2023년 2월 9일 |
| [2.21.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.21.2) | 이번 패치 릴리스에서는 v1 및 v2 [티저 구성 요소](/help/components/teaser.md)와 관련된 문제가 해결되었습니다. | - | 6.5.13.0+ | 반복 | 8, 11 | 2022년 9월 12일 |
| [2.21.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.21.0) | 이 릴리스에는 LinkHandler API의 게시, [이미지 구성 요소](/help/components/image.md) 및 [데이터 레이어](/help/developing/data-layer/overview.md)에 대한 개선 사항, 다중 패널 구성 요소에 대한 개선 사항을 비롯한 여러 개선 사항이 포함되어 있습니다. | - | 6.5.13.0+ | 반복 | 8, 11 | 2022년 9월 12일 |
| [2.20.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.8) | 이번 릴리스에서는 AdaptiveImageServlet을 통한 SVG 이미지 게재 문제가 해결되었습니다. | - | 6.5.13.0+ | 반복 | 8, 11 | 2022년 8월 4일 |
| [2.20.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.6) | 이 패치 릴리스에서는 새로운 [목차 구성 요소](/help/components/tableofcontents.md)와 관련된 문제가 해결되었습니다. | - | 6.5.13.0+ | 반복 | 8, 11 | 2022년 7월 7일 |
| [2.20.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.4) | 이 패치 릴리스에서는 새로운 [목차 구성 요소](/help/components/tableofcontents.md)와 관련된 문제가 해결되었습니다. | - | 6.5.13.0+ | 반복 | 8, 11 | 2022년 6월 29일 |
| [2.20.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.2) | 새 AEMaaCS [웹에 최적화된 자산 게재 서비스](/help/developing/web-optimized-image-delivery.md)와 관련된 문제를 해결하는 패치 릴리스입니다. | - | 6.5.13.0+ | 반복 | 8, 11 | 2022년 6월 20일 |
| [2.20.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.20.0) | 이 릴리스에는 새로운 [목차 구성 요소](/help/components/tableofcontents.md) 및 AEMaaCS [웹에 최적화된 자산 게재 서비스](/help/developing/web-optimized-image-delivery.md)에 대한 지원이 추가되었으며 버그 수정이 포함되어 있습니다. | - | 6.5.13.0+ | 반복 | 8, 11 | 2022년 6월 9일 |
| [2.19.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.19.0) | 이번 릴리스에서는 새로운 버전의 [검색 구성 요소](/help/components/quick-search.md) 및 [버튼 구성 요소](/help/components/button.md) 기능이 추가되었으며 다양한 접근성 개선 및 버그 수정이 이루어졌습니다. | - | 6.5.10.0+ | 반복 | 8, 11 | 2022년 4월 7일 |
| [2.18.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.18.8) | 이번 릴리스에서는 AEMaaCS 관련 문제가 해결되었습니다. | - | 6.5.10.0+ | 반복 | 8, 11 | 2022년 3월 17일 |
| [2.18.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.18.6) | 패치 릴리스입니다. | - | 6.5.10.0+ | 반복 | 8, 11 | 2022년 3월 3일 |
| [2.18.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.18.0) | 핵심 구성 요소의 주요 릴리스에서는 여러 구성 요소의 새로운 버전에 새 링크 핸들러가 도입되며 접근성 개선 및 버그 수정이 이루어집니다. | - | 6.5.10.0+ * | 반복 | 8, 11 | 2022년 2월 16일 |
| [2.17.14](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.12) | 패치 릴리스입니다. | 6.4.8.4+ | 6.5.6.0+ | 반복 | 8, 11 | 2021년 12월 13일 |
| [2.17.12](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.12) | 이전 릴리스와 함께 도입된 회귀 문제를 해결하는 패치 릴리스입니다. | 6.4.8.4+ | 6.5.6.0+ | 반복 | 8, 11 | 2021년 10월 1일 |
| [2.17.10](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.10) | 이 패치는 리디렉션 대상의 외부 URL이 표시되는 [목록](/help/components/list.md) 및 [탐색](/help/components/navigation.md) 구성 요소를 개선하고 [티저](/help/components/teaser.md) 구성 요소의 추후 v2용 페이지 이미지 상속을 활성화하고 패치에 추가 버그 수정이 포함됩니다. | 6.4.8.4+ | 6.5.6.0+ | 반복 | 8, 11 | 2021년 8월 31일 |
| [2.17.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.8) | 이전에 도입된 이전 버전과 호환 불가능한 변경 사항을 해결하는 패치 릴리스입니다. | 6.4.8.4+ | 6.5.6.0+ | 반복 | 8, 11 | 2021년 8월 2일 |
| [2.17.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.6) | 이 패치 릴리스는 페이지 사이트 맵에 대한 지원을 추가하고 패치에 여러 접근성 개선 사항이 포함됩니다. | 6.4.8.4+ | 6.5.6.0+ | 반복 | 8, 11 | 2021년 7월 29일 |
| [2.17.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.2) | 이 패치 릴리스에는 AEMaaCS에서 작동하지 않는 [데이터 레이어](/help/developing/data-layer/overview.md)에 대한 버그 수정이 포함됩니다. | 6.4.8.4+ | 6.5.6.0+ | 반복 | 8, 11 | 2021년 7월 8일 |
| [2.17.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.17.0) | 이 릴리스에는 링크 핸들러를 지원하는 여러 구성 요소 버전 및 [페이지 구성 요소의 이미지 추천 기능에 대한 기술 미리보기가 포함됩니다.](/help/components/page.md) 몇 가지 버그 수정도 포함됩니다. | 6.4.8.4+ | 6.5.6.0+ | 반복 | 8, 11 | 2021년 6월 16일 |
| [2.16.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.16.4) | 새 링크 핸들러 문제를 해결할 수 있는 패치 릴리스입니다. | 6.4.8.1+ | 6.5.5.0+ | 반복 | 8, 11 | 2021년 5월 19일 |
| [2.16.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.16.2) | 이는 새 링크 핸들러 문제를 해결하는 패치 릴리스이자 [PWA](/help/components/page.md#pwa-support) 다중 페이지 애플리케이션 지원을 위해 추가된 개선 사항입니다. | 6.4.8.1+ | 6.5.5.0+ | 반복 | 8, 11 | 2021년 5월 15일 |
| [2.16.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.16.0) | 이 릴리스는 접근성 개선 사항과 새 링크 핸들러의 기존 구성 요소 도입에 중점을 둡니다. | 6.4.8.1+ | 6.5.5.0+ | 반복 | 8, 11 | 2021년 4월 22일 |
| [2.15.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.15.2) | 특정 상황에서 실패한 이전 [데이터 레이어](/help/developing/data-layer/overview.md) 호환성과 IT 테스트 문제를 해결하는 패치 릴리스입니다. | 6.4.8.1+ | 6.5.5.0+ | 반복 | 8, 11 | 2021년 3월 16일 |
| [2.15.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.15.0) | 이 릴리스는 [페이지 구성 요소의 점진적 웹 앱(PWA)](/help/components/page.md#pwa-support)과 [Adobe 데이터 레이어](/help/developing/data-layer/overview.md)의 버전 2.0.0을 지원합니다. | 6.4.8.1+ | 6.5.5.0+ | 반복 | 8, 11 | 2021년 2월 23일 |
| [2.14.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.14.0) | 이 릴리스에는 [임베디드 구성 요소](/help/components/embed.md)에 대한 새 옵션, [페이지](/help/components/page.md) 수준의 브랜드 슬러그와 문제 버그 수정이 포함됩니다. | 6.4.8.1+ | 6.5.5.0+ | 반복 | 8, 11 | 2021년 2월 9일 |
| [2.13.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.13.2) | AEMaaCS에서 사용되는 경우 RTE 문제를 해결하는 패치 릴리스입니다. | 6.4.8.1+ | 6.5.5.0+ | 반복 | 8, 11 | 2020년 12월 16일 |
| [2.13.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.13.0) | 이 릴리스에는 [이미지 구성 요소](/help/components/image.md)에 대한 Dynamic Media 기능이 포함됩니다. | 6.4.8.1+ | 6.5.5.0+ | 반복 | 8, 11 | 2020년 12월 4일 |
| [2.12.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.2) | 사소한 문제를 해결하는 2.12.0 패치 릴리스입니다. | 6.4.8.1+ | 6.5.5.0+ | 반복 | 8, 11 | 2020년 11월 11일 |
| [2.12.1](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.1) | [이미지 구성 요소](/help/components/image.md)에서 주요 버그를 해결하는 2.12.0 패치 릴리스입니다. | 6.4.8.1+ | 6.5.5.0+ | 반복 | 8, 11 | 2020년 11월 5일 |
| [2.12.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.12.0) | 이 릴리스에는 [새 POST 양식 핸들러](/help/components/forms/form-container.md#post-data), [컨텍스트 인식 구성을 통해](/help/developing/including-clientlibs.md#context-aware-loading) 사용자 정의 CSS, JavaScript 및 메타데이터 태그를 포함하는 기능 및 `DataLayerBuilder`utility로 [사용자 정의 구성 요소의 데이터 레이어 통합을 단순화는 기능](/help/developing/data-layer/integrations.md#enabling-custom-components)이 도입되었습니다. | 6.4.8.1+ | 6.5.5.0+ | 반복 | 8, 11 | 2020년 10월 29일 |
| [2.11.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.11.0) | 이 릴리스에는 [AMP 지원](/help/developing/amp.md)이 도입되었습니다. | 6.4.8.1+ | 6.5.5.0+ | 반복 | 8, 11 | 2020년 7월 20일 |
| [2.10.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.10.0) | 이 릴리스에는 [PDF 뷰어 구성 요소](/help/components/pdf-viewer.md)가 도입되었습니다. | 6.4.8.1+ | 6.5.5.0+ | 반복 | 8, 11 | 2020년 6월 17일 |
| [2.9.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.9.0) | 이번 릴리스를 통해 [Adobe 클라이언트 데이터 레이어](/help/developing/data-layer/overview.md) 통합 기능이 활성화되고 [진행률 표시줄 구성 요소](/help/components/progress-bar.md)가 도입되었습니다. | 6.4.8.0+ | 6.5.4.0+ | 반복 | 8, 11 | 2020년 5월 29일 |
| [2.8.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.8.0) | 이 릴리스는 개선 사항 문제 해결에 중점을 둡니다. | 6.4.4.0+ | 6.5.0.0+ | 반복 | 8, 11 | 2019년 12월 5일 |
| [2.7.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.7.0) | 이 릴리스에는 새 [임베디드 구성 요소](/help/components/embed.md)가 도입되었습니다. | 6.4.4.0+ | 6.5.0.0+ | 반복 | 8, 11 | 2019년 9월 25일 |
| [2.6.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.6.0) | 이 릴리스에는 새 [경험 조각 구성 요소](/help/components/experience-fragment.md)가 도입되었습니다. | 6.4.4.0+ | 6.5.0.0+ | 반복 | 8, 11 | 2019년 9월 6일 |
| [2.5.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.5.0) | 이 릴리스에는 새 [아코디언](/help/components/accordion.md), [버튼](/help/components/button.md) [컨테이너](/help/components/container.md) 및 [다운로드 구성 요소](/help/components/download.md)가 도입되었습니다. | 6.4.2.0+ | 6.5.0.0+ | 반복 | 8, 11 | 2019년 6월 25일 |
| [2.4.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.4.0) | 이 릴리스에는 새 [콘텐츠 조각 목록 구성 요소](/help/components/content-fragment-list.md)가 도입되었습니다. | 6.4.2.0+ | 6.5.0.0+ | 반복 | 8, 11 | 2019년 5월 7일 |
| [2.3.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.2) | 이 릴리스는 [구성 요소 라이브러리](https://aemcomponents.dev)에 대한 세분화 내용에 중점을 두고 있으며, 릴리스에는 [구분자 구성 요소](/help/components/separator.md)에 대한 몇 가지 기능 개선이 포함됩니다. | 6.4.2.0+ | 6.5.0.0+ | 반복 | 8 | 2019년 3월 14일 |
| [2.3.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.0) | 이 릴리스는 [구성 요소 라이브러리](https://aemcomponents.dev)와 새로운 [구분자 구성 요소](/help/components/separator.md) 도입에 중점을 두고 있으며, 릴리스에는 [이미지 구성 요소](/help/components/image.md)에 대한 몇 가지 기능 개선이 포함됩니다. | 6.4.2.0+ | - | - | 8 | 2019년 2월 11일 |
| [2.2.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.2) | 이 릴리스는 주로 버그 수정에 중점을 두고 있으며, 릴리스에는 [슬라이드 구성 요소](/help/components/carousel.md)에 대한 몇 가지 기능 개선이 포함됩니다. | 6.4.2.0+ | - | - | 8 | 2018년 11월 27일 |
| [2.2.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.0) | 이 릴리스에는 [탭 구성 요소](/help/components/tabs.md) 및 [슬라이드 구성 요소](/help/components/carousel.md)뿐만 아니라 [이미지 구성 요소](/help/components/image.md), [페이지 구성 요소](/help/components/page.md) 및 [제목 구성 요소](/help/components/title.md)에 대한 개선 사항과 강화 추적 기능이 포함됩니다. | 6.4.2.0+ | - | - | 8 | 2018년 10월 16일 |
| [2.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.1.0) | 이 릴리스에는 [이미지 구성 요소](/help/components/image.md)에 대한 개선 사항 및 버그 수정과 함께 [티저 구성 요소](/help/components/teaser.md)가 도입되었습니다. | 6.4.2.0+ | - | - | 8 | 2018년 7월 13일 |
| [2.0.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.8) | 버그 해결 릴리스입니다. | 6.4.0.0+ | - | - | 8 | 2018년 6월 12일 |
| [2.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.6) | 이 릴리스에는 내부 개선 사항, 버그 수정 및 [이미지 구성 요소](/help/components/image.md)의 이미지 플립 지원 등 사소한 개선 사항 등이 추가됩니다. | 6.4.0.0+ | - | - | 8 | 2018년 4월 11일 |
| [2.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.4) | 이 릴리스는 주로 내부 개선 사항, 버그 수정을 비롯해 [이미지 구성 요소](/help/components/image.md), [페이지 구성 요소](/help/components/page.md) 및 [콘텐츠 조각 구성 요소](/help/components/content-fragment-component.md)에 대한 몇 가지 사소한 개선 사항에 중점을 둡니다. | 6.4.0.0+ | - | - | 8 | 2018년 3월 7일 |
| [2.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.0) | 이 릴리스에는 [탐색 구성 요소](/help/components/navigation.md), [언어 탐색 구성 요소](/help/components/language-navigation.md) 및 [빠른 검색 구성 요소](/help/components/quick-search.md)가 도입되었고, 모든 구성 요소의 [스타일 시스템](/help/get-started/authoring.md#component-styling)이 구현되었습니다. | 6.4.0.0+ | - | - | 8 | 2018년 1월 16일 |
| [1.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.1.0) | 이 릴리스의 모든 구성 요소에서 JSON 내보내기가 구현되고 [콘텐츠 조각 구성 요소](/help/components/content-fragment-component.md)가 도입됩니다. | 6.4.0.0+ | - | - | 8 | 2017년 10월 10일 |
| [1.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.6) | 이 릴리스에는 [이미지 구성 요소](/help/components/image.md)에 대한 몇 가지 버그 수정이 추가됩니다. | 6.4.0.0+ | - | - | 8 | 2017년 8월 4일 |
| [1.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.4) | 이 릴리스에는 [페이지 구성 요소](/help/components/page.md) 및 [이미지 구성 요소](/help/components/image.md)에 대한 버그 수정, 여러 전역 버그 수정 및 개선 사항이 추가됩니다. | 6.4.0.0+ | - | - | 8 | 2017년 4월 26일 |
| [1.0.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.all-1.0.2) | 이 릴리스에는 [이미지 구성 요소](/help/components/image.md)의 애니메이션 GIF 이미지에 대한 버그 수정이 추가됩니다. | 6.4.0.0+ | - | - | 7 | 2017년 3월 22일 |
| [1.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.0) | 핵심 구성 요소의 초기 릴리스 | 6.4.0.0+ | - | - | 7 | 2017년 3월 20일 |

>[!TIP]
>
>AEM과 마찬가지로 Adobe에서는 개발자가 실행 중인 AEM 버전과 호환되는 [핵심 구성 요소의 최신 릴리스와 버전](https://github.com/adobe/aem-core-wcm-components/releases/latest)을 사용하여 최신 버그 수정 및 기능을 활용하기를 권장합니다.

### 구성 요소 버전 및 릴리스 {#component-versions-and-releases}

다음 표에서 핵심 구성 요소 릴리스에 포함된 구성 요소에 대해 자세히 살펴볼 수 있습니다.

|  | 릴리스 1.0.0 - 1.0.6 | 릴리스 1.1.0 | 릴리스 2.0.0 - 2.0.8 | 릴리스 2.1.0 | 릴리스 2.2.0 - 2.2.0 | 릴리스 2.3.0 - 2.3.2 | 릴리스 2.4.0 | 릴리스 2.5.0 | 릴리스 2.6.0 | 릴리스 2.7.0 - 2.8.0 | 릴리스 2.9.0 - 2.17.14 | 릴리스 2.18.0 | 릴리스 2.19.0 | 릴리스 2.20.0 - 2.21.2 | 릴리스 2.22.0+ |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| **[페이지](components/page.md)** | v1 | v1 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 |
| **[제목](components/title.md)** | v1 | v1 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 |
| **[이미지](components/image.md)** | v1 | v1 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 |
| **[목록](components/list.md)** | v1 | v1 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3, v4 |
| **[이동 경로](components/breadcrumb.md)** | v1 | v1 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 | v1, v2, v3 |
| **[소셜 미디어 공유](components/sharing.md)** | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1, 사용 안 함 | v1, 사용 안 함 | v1, 사용 안 함 | v1, 사용 안 함 |
| **[양식 컨테이너](components/forms/form-container.md)** | v1 | v1 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 |
| **[양식 텍스트](components/forms/form-text.md)** | v1 | v1 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 |
| **[양식 옵션](components/forms/form-options.md)** | v1 | v1 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 |
| **[양식 숨김](components/forms/form-hidden.md)** | v1 | v1 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 |
| **[양식 버튼](components/forms/form-button.md)** | v1 | v1 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 |
| **[콘텐츠 조각](components/content-fragment-component.md)** |  | 샌드박스 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 | v1 v2 |
| **[탐색](components/navigation.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 v2 | v1 v2 | v1 v2 | v1 v2 |
| **[언어 탐색](components/language-navigation.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 v2 | v1 v2 | v1 v2 | v1 v2 |
| **[빠른 검색](components/quick-search.md)** |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 v2 | v1 v2 | v1 v2 |
| **[티저](components/teaser.md)** |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 v2 | v1 v2 | v1 v2 | v1 v2 |
| **[탭](components/tabs.md)** |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[슬라이드](components/carousel.md)** |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[구분자](components/separator.md)** |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[콘텐츠 조각 목록](components/content-fragment-list.md)** |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 v2 | v1 v2 | v1 v2 | v1 v2 |
| **[아코디언](components/accordion.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[버튼](components/button.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 v2 | v1 v2 | v1 v2 | v1 v2 |
| **[컨테이너](components/container.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 | v1 | v1 | v1 |
| **[다운로드](components/download.md)** |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 v2 | v1 v2 | v1 v2 | v1 v2 |
| **[경험 조각](components/experience-fragment.md)** |  |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 v2 | v1 v2 | v1 v2 | v1 v2 |
| **[임베드](components/embed.md)** |  |  |  |  |  |  |  |  |  | v1 | v1 | v1 v2 | v1 v2 | v1 v2 | v1 v2 |
| **[진행률 표시줄](components/progress-bar.md)** |  |  |  |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 |
| **[PDF 뷰어](components/pdf-viewer.md)** |  |  |  |  |  |  |  |  |  |  | v1 | v1 | v1 | v1 | v1 |
| **[목차](components/tableofcontents.md)** |  |  |  |  |  |  |  |  |  |  |  |  |  | v1 | v1 |

## 버전 및 릴리스 {#versions-and-releases}

핵심 구성 요소는 GitHub를 통해 배포됩니다. 이를 통해 Adobe는 기능을 빠르게 구성 요소에 추가하고, AEM 릴리스 주기 외부에서 커뮤니티 입력을 사용할 수 있습니다.

핵심 구성 요소는 호환되는 AEM 버전을 정의하는 데 사용할 수 있습니다. 즉, AEM 버전 하나로 핵심 구성 요소의 여러 버전 또는 릴리스를 지원할 수 있습니다.

### 버전 {#versions}

**버전**&#x200B;은 핵심 구성 요소에 대한 주요 반복 버전입니다. 각 구성 요소에는 버전이 있습니다. 버전은 v1, v2 등 0이 아닌 양의 정수로 추가된 **v**&#x200B;로 표시됩니다. 변경 사항이 이전에 호환되지 않은 경우에만 버전이 증가합니다. 새로운 기능 도입의 일반적인 사례입니다.

개발자와 관리자는 리소스 유형 경로의 횟수와 정규화된 Java 구현 클래스 이름으로 핵심 구성 요소의 버전을 인식할 수 있습니다. 이 버전 번호는 [시맨틱 버전 관리 가이드라인](https://semver.org/)에서 정의된 주요 버전을 나타냅니다.

핵심 구성 요소 버전에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](developing/guidelines.md)를 참조하십시오.

### 릴리스 {#releases}

**릴리스**&#x200B;를 통해 핵심 구성 요소를 사용할 수 있으며 [핵심 구성 요소는 GitHub에 제공되는 실제 게시된 아티팩트를 나타냅니다.](https://github.com/adobe/aem-core-wcm-components/releases) 릴리스는 포맷 `X.Y.Z`의 10진법으로 표시되고, 제공 가능한 패키지로 모든 핵심 구성 요소를 수집합니다.

* **주요 릴리스**&#x200B;에는 전체 새 구성 요소 및 표준 버그 수정과 함께 기존 버전의 구성 요소에 대한 개선이 도입됩니다. `X` 구성 요소 릴리스 횟수가 증가하면 나타납니다.
* **마이너 릴리스**&#x200B;에는 새 구성 요소, 버그 수정과 함께 기존 버전의 구성 요소에 새로운 기능이 도입됩니다. `Y` 구성 요소 릴리스 횟수가 증가하면 나타납니다.
* **패치 릴리스**&#x200B;에는 버그 수정만 포함됩니다. `Z` 구성 요소 릴리스 횟수가 증가하면 나타납니다.

>[!NOTE]
>
>릴리스에는 동일한 구성 요소의 여러 버전이 포함될 수 있습니다.
>
>동일한 구성 요소 버전이 여러 릴리스에 나타날 수 있습니다.

## 핵심 구성 요소 지원 {#core-components-support}

핵심 구성 요소는 AEM의 필수적인 부분이며 빠른 시작의 일부로 전달된 것처럼 동일한 이용 약관에 따라 지원됩니다.

다른 제품 기능과 마찬가지로 수명 종료에 대한 일반적인 규칙은 다음과 같습니다.

* 구성 요소가 제거되기에 앞서 사용 중지와 관련된 공지가 발표됩니다.
* 공지 후 가장 빠른 시일 내에 AEM 릴리스에서 제거됩니다.

따라서 지원이 종료되기 전에 고객에게 구성 요소의 새 버전으로 이동할 수 있는 릴리스 주기를 1개 이상 제공합니다.

각 구성 요소의 버전은 지원되는 AEM 버전을 명확하게 설명합니다. AEM 버전에 대한 지원이 중단되면 해당 버전의 AEM에 대한 핵심 구성 요소에 대한 지원도 중단됩니다.

구성 요소 사용자 정의에 대한 자세한 내용은 관련 핵심 구성 요소 버전의 [핵심 구성 요소 사용자 정의](developing/customizing.md)를 참조하십시오.

## 기초 구성 요소 지원 {#foundation-component-support}

Adobe의 개발 역점이 핵심 구성 요소로 전환되면서 새 기능이 추가될 예정입니다.

[거의 모든 기초 구성 요소가 AEM 6.5에서 사용되지 않으며](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/siteandpage/default-components-foundation.html?lang=ko) 주요 버그 해결만 향후 기초 구성 요소로 간주됩니다.

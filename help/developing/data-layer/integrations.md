---
title: 통합 및 Adobe 클라이언트 데이터 레이어
description: Adobe 클라이언트 데이터와 맞춤형 구성 요소를 통합할 수 있는 방법과 Adobe Analytics와 Adobe Target의 통합 기능으로 웹 사이트에 대한 통찰력을 얻을 수 있는 방법에 대해 알아봅니다.
feature: Core Components, Adobe Client Data Layer
role: Architect, Developer, Admin
exl-id: 503dd3dc-fe95-4a17-83f5-1f0c1960993d
source-git-commit: 2ac16b15718128feefbe903e92f276b16fe96f69
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 100%

---

# Adobe 클라이언트 데이터 레이어와 통합 {#integrations}

Adobe 클라이언트 데이터 레이어는 스크립트용 데이터 노출 및 사용을 위한 표준화된 방법을 제공하여 웹 사이트를 측정하는 수고를 줄여 줍니다.

Adobe 클라이언트 데이터와 맞춤형 구성 요소를 통합할 수 있고 Adobe Analytics와 Adobe Target의 통합 기능으로 웹 사이트에 대한 통찰력을 얻을 수 있습니다.

## 맞춤형 구성 요소에 대한 데이터 레이어를 활성화합니다. {#enabling-custom-components}

맞춤형 구성 요소를 데이터 레이어에 자동 추가하려면

1. 추적할 맞춤형 구성 요소 모델의 속성을 정의합니다.
1. `data-cmp-data-layer` 속성을 맞춤형 구성 요소 HTL에 추가합니다. 예: `data-cmp-data-layer="${mycomponent.data.json}"`

맞춤형 구성 요소의 특정 요소가 클릭될 때마다 데이터 레이어가 `cmp:click` 이벤트를 자동으로 트리거하려면 `data-cmp-clickable` 속성을 맞춤형 구성 요소 HTL에서 추적할 요소에 추가합니다.

클라이언트측에서 `data-cmp-data-layer-enabled` 속성에 대해 쿼리를 수행하면 데이터 레이어 활성화 여부를 확인할 수 있습니다.

>[!TIP]
>
>Adobe 클라이언트 데이터 레이어와 핵심 구성 요소 통합 및 맞춤형 구성 요소에서의 데이터 레이어 활성화 방법에 대한 추가 기술 세부 정보는 핵심 구성 요소 저장소의 [`DATA_LAYER_INTEGRATION.md`](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) 파일을 참조하십시오.

## Adobe Analytics와 Adobe Target 통합 {#analytics-target}

Adobe Analytics와 Adobe Target가 결합되면 Adobe 클라이언트 데이터 레이어는 디지털 경험에 대한 통찰력을 확보할 수 있는 매우 강력하고 유연한 도구가 됩니다. 다음 튜토리얼은 통합 과정의 예를 보여 줍니다.

### Adobe Analytics로 페이지 데이터를 수집합니다. {#collect-page-data}

AEM 핵심 구성 요소로 Adobe 클라이언트 데이터 레이어의 빌트인 기능을 사용하여 Adobe Experience Manager Sites에서 페이지에 대한 데이터를 수집하는 방법에 대해 알아봅니다. Experience Platform Launch 및 Adobe Analytics 확장 기능을 사용하여 Adobe Analytics로 페이지 데이터를 전송할 규칙을 생성합니다.

[여기서 튜토리얼을 조회합니다](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/integrations/analytics/collect-data-analytics.html).

### Adobe Analytics로 구성 요소를 클릭 추적 {#track-clicked-components}

이벤트 중심의 Adobe 클라이언트 데이터 레이어를 AEM 핵심 구성 요소와 함께 사용하여 Adobe Experience Manager Site에서 특정 구성 요소의 클릭 수를 추적합니다. Experience Platform Launch의 규칙을 사용하여 클릭 이벤트를 수신하고, 구성 요소로 필터링하고 추적 링크 비콘으로 데이터를 Adobe Analytics로 전송하는 방법에 대해 알아봅니다.

[여기서 튜토리얼을 조회합니다](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/integrations/analytics/track-clicked-component.html).

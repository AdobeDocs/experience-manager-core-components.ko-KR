---
title: 통합 및 Adobe 클라이언트 데이터 레이어
description: Adobe 클라이언트 데이터 계층을 사용자 지정 구성 요소와 통합하는 방법과 Adobe Analytics 및 Adobe Target과의 통합을 통해 웹 사이트에 대한 통찰력을 얻는 방법을 알아봅니다
feature: 핵심 구성 요소, Adobe 클라이언트 데이터 레이어
role: Architect, Developer, Admin
exl-id: 503dd3dc-fe95-4a17-83f5-1f0c1960993d
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# Adobe 클라이언트 데이터 레이어와 통합 {#integrations}

Adobe 클라이언트 데이터 계층은 스크립트를 위한 모든 종류의 데이터를 노출하고 액세스하는 표준화된 방법을 제공하여 웹 사이트를 구현하는 노력을 줄입니다.

Adobe 클라이언트 데이터 레이어를 사용자 지정 구성 요소와 통합하고 Adobe Analytics 및 Adobe Target와의 통합을 통해 웹 사이트에 대한 통찰력을 얻을 수 있습니다.

## 사용자 지정 구성 요소에 대한 데이터 레이어 활성화 {#enabling-custom-components}

사용자 지정 구성 요소를 데이터 레이어에 자동으로 추가하려면 다음을 수행합니다.

1. 추적해야 하는 사용자 지정 구성 요소 모델의 속성을 정의합니다.
1. 사용자 지정 구성 요소 HTL에 `data-cmp-data-layer` 속성을 추가합니다. 예: `data-cmp-data-layer="${mycomponent.data.json}"`

사용자 지정 구성 요소의 특정 요소를 클릭할 때마다 데이터 계층이 `cmp:click` 이벤트를 자동으로 트리거하도록 하려면 사용자 지정 구성 요소 HTL에서 추적할 요소에 `data-cmp-clickable` 속성을 추가하십시오.

클라이언트측에 `data-cmp-data-layer-enabled` 속성을 쿼리하여 데이터 레이어가 활성화되어 있는지 확인할 수 있습니다.

>[!TIP]
>
>Adobe 클라이언트 데이터 레이어와 코어 구성 요소 간의 통합 및 사용자 지정 구성 요소에서 데이터 레이어를 활성화하는 방법에 대한 자세한 내용은 코어 구성 요소 리포지토리의 [`DATA_LAYER_INTEGRATION.md`](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) 파일을 참조하십시오.

## Adobe Analytics 및 Adobe Target과 통합 {#analytics-target}

Adobe Analytics 및 Adobe Target과 함께 Adobe 클라이언트 데이터 계층은 디지털 경험에 대한 통찰력을 얻을 수 있는 매우 강력하고 유연한 도구 세트의 기반이 됩니다. 다음 자습서에서는 샘플 통합을 안내합니다.

### Adobe Analytics으로 페이지 데이터 수집 {#collect-page-data}

AEM 핵심 구성 요소와 함께 Adobe 클라이언트 데이터 계층의 내장 기능을 사용하여 Adobe Experience Manager Sites의 페이지에 대한 데이터를 수집하는 방법을 알아봅니다. Experience Platform Launch 및 Adobe Analytics 확장은 페이지 데이터를 Adobe Analytics에 전송하는 규칙을 만드는 데 사용됩니다.

[자습서는 여기에서 확인할 수 있습니다.](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/integrations/analytics/collect-data-analytics.html)

### 클릭한 구성 요소를 Adobe Analytics에서 추적 {#track-clicked-components}

AEM 핵심 구성 요소와 함께 이벤트 기반 Adobe 클라이언트 데이터 계층을 사용하여 Adobe Experience Manager 사이트에서 특정 구성 요소의 클릭을 추적합니다. Experience Platform Launch의 규칙을 사용하여 클릭 이벤트를 수신하고, 구성 요소별로 필터링하고, 추적 링크 비콘이 있는 Adobe Analytics으로 데이터를 전송하는 방법을 알아봅니다.

[자습서는 여기에서 확인할 수 있습니다.](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/integrations/analytics/track-clicked-component.html)

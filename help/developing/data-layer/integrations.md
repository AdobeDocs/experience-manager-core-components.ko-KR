---
title: 통합 및 Adobe 클라이언트 데이터 레이어
description: Adobe 클라이언트 데이터 레이어가 사용자 정의 구성 요소와 어떻게 통합되고 Adobe Analytics 및 Adobe Target과의 통합을 통해 웹 사이트에 대한 통찰력을 얻을 수 있는지 살펴보십시오
translation-type: tm+mt
source-git-commit: ea7a0e08ea1b769b400fce275c8ce7e0db6f9407
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%

---


# Adobe 클라이언트 데이터 레이어와의 통합 {#integrations}

Adobe 클라이언트 데이터 레이어는 모든 스크립트의 모든 종류의 데이터를 노출하고 액세스하는 표준화된 방법을 제공하여 웹 사이트를 구축하는 노력을 줄이고 있습니다.

Adobe 클라이언트 데이터 레이어는 사용자 정의 구성 요소와 통합할 수 있고, Adobe Analytics 및 Adobe Target과의 통합을 통해 웹 사이트에 대한 통찰력을 얻을 수 있습니다.

## 사용자 지정 구성 요소에 대한 데이터 레이어 활성화 {#enabling-custom-components}

사용자 지정 구성 요소를 데이터 레이어에 자동으로 추가하려면:

1. 추적해야 하는 사용자 지정 구성 요소 모델의 속성을 정의합니다.
1. 사용자 지정 구성 요소 HTL에 `data-cmp-data-layer` 속성을 추가합니다. 예: `data-cmp-data-layer="${mycomponent.data.json}"`.

사용자 지정 구성 요소의 특정 요소를 클릭할 때마다 데이터 레이어가 `cmp:click` 이벤트를 자동으로 트리거하도록 하려면 사용자 지정 구성 요소 HTL에서 추적할 요소에 `data-cmp-clickable` 속성을 추가합니다.

클라이언트 쪽에서 속성을 쿼리하여 데이터 레이어가 활성화되었는지 확인할 수 `data-cmp-data-layer-enabled` 있습니다.

>[!TIP]
>
>Adobe 클라이언트 데이터 레이어와 핵심 구성 요소의 통합에 대한 자세한 기술 정보 및 사용자 지정 구성 요소에서 데이터 레이어를 활성화하는 방법에 대한 자세한 내용은 핵심 구성 요소 저장소의 [`DATA_LAYER_INTEGRATION.md`](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) 파일을 참조하십시오.

## Adobe Analytics 및 Adobe Target 통합 {#analytics-target}

Adobe Analytics 및 Adobe Target과 함께 제공되는 Adobe 클라이언트 데이터 레이어는 디지털 경험에 대한 통찰력을 얻을 수 있는 강력하고 유연한 툴셋의 기반이 됩니다. 다음 자습서에서는 샘플 통합을 소개합니다.

### Adobe Analytics에서 페이지 데이터 수집 {#collect-page-data}

AEM 코어 구성 요소와 함께 Adobe 클라이언트 데이터 레이어의 내장 기능을 사용하여 Adobe Experience Manager Sites의 페이지에 대한 데이터를 수집하는 방법을 학습합니다. Experience Platform Launch 및 Adobe Analytics 확장자는 페이지 데이터를 Adobe Analytics으로 보내는 규칙을 만드는 데 사용됩니다.

[튜토리얼을 확인하십시오.](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/integrations/analytics/collect-data-analytics.html)

### 클릭한 구성 요소 추적(Adobe Analytics 사용) {#track-clicked-components}

AEM 코어 구성 요소와 함께 이벤트 기반 Adobe 클라이언트 데이터 레이어를 사용하여 Adobe Experience Manager 사이트에서 특정 구성 요소의 클릭을 추적합니다. Experience Platform Launch의 규칙을 사용하여 클릭 이벤트를 수신하고, 구성 요소별로 필터링하고, 추적 링크 비콘이 있는 Adobe Analytics으로 데이터를 전송하는 방법을 알아봅니다.

[튜토리얼을 확인하십시오.](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/integrations/analytics/track-clicked-component.html)

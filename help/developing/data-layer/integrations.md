---
title: 통합 및 Adobe 클라이언트 데이터 레이어
description: Adobe 클라이언트 데이터 레이어가 사용자 정의 구성 요소와 통합하는 방법, Adobe Analytics 및 Adobe Target와의 통합을 통해 웹 사이트에 대한 통찰력을 얻는 방법을 살펴볼 수 있습니다
feature: Core Components, Adobe Client Data Layer
role: Architect, Developer, Administrator
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%

---


# Adobe 클라이언트 데이터 레이어 {#integrations}와의 통합

Adobe 클라이언트 데이터 레이어는 모든 스크립트의 모든 유형의 데이터를 노출하고 액세스하는 표준화된 방법을 제공하여 웹 사이트를 구축하는 노력을 줄여 줍니다.

Adobe 클라이언트 데이터 레이어는 사용자 정의 구성 요소와 통합하고 Adobe Analytics 및 Adobe Target와의 통합을 통해 웹 사이트에 대한 통찰력을 얻을 수 있습니다.

## 사용자 지정 구성 요소에 대한 데이터 레이어 활성화 {#enabling-custom-components}

사용자 지정 구성 요소를 데이터 레이어에 자동으로 추가하려면:

1. 추적해야 하는 사용자 지정 구성 요소 모델의 속성을 정의합니다.
1. `data-cmp-data-layer` 속성을 사용자 지정 구성 요소 HTL에 추가합니다. 예:`data-cmp-data-layer="${mycomponent.data.json}"`.

사용자 지정 구성 요소의 특정 요소를 클릭할 때마다 데이터 레이어가 `cmp:click` 이벤트를 자동으로 트리거하도록 하려면 사용자 지정 구성 요소 HTL에서 추적할 요소에 `data-cmp-clickable` 속성을 추가합니다.

`data-cmp-data-layer-enabled` 속성은 클라이언트측에서 쿼리하여 데이터 레이어가 활성화되었는지 확인할 수 있습니다.

>[!TIP]
>
>Adobe 클라이언트 데이터 레이어를 핵심 구성 요소와 통합하는 방법과 사용자 지정 구성 요소에서 데이터 레이어를 활성화하는 방법에 대한 자세한 내용은 핵심 구성 요소 저장소의 [`DATA_LAYER_INTEGRATION.md`](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) 파일을 참조하십시오.

## Adobe Analytics 및 Adobe Target {#analytics-target}과 통합

Adobe Analytics 및 Adobe Target과 함께 제공되는 Adobe 클라이언트 데이터 레이어는 디지털 경험에 대한 통찰력을 얻을 수 있는 강력하고 유연한 툴셋의 기반이 됩니다. 다음 자습서에서는 샘플 통합을 소개합니다.

### Adobe Analytics {#collect-page-data}을(를) 사용하여 페이지 데이터 수집

AEM 핵심 구성 요소와 함께 Adobe 클라이언트 데이터 레이어의 내장 기능을 사용하여 Adobe Experience Manager Sites의 페이지에 대한 데이터를 수집하는 방법에 대해 학습합니다. Experience Platform Launch 및 Adobe Analytics 확장 기능을 사용하여 페이지 데이터를 Adobe Analytics으로 보내는 규칙을 만듭니다.

[여기에서 자습서를 봅니다.](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/integrations/analytics/collect-data-analytics.html)

### Adobe Analytics {#track-clicked-components}을(를) 사용하여 클릭한 구성 요소 추적

AEM 핵심 구성 요소와 함께 이벤트 기반의 Adobe 클라이언트 데이터 레이어를 사용하여 Adobe Experience Manager 사이트에서 특정 구성 요소의 클릭 수를 추적할 수 있습니다. Experience Platform Launch에서 규칙을 사용하여 클릭 이벤트를 수신하고, 구성 요소별로 필터링하고, 추적 링크 비콘이 있는 Adobe Analytics으로 데이터를 보내는 방법을 알아봅니다.

[여기에서 자습서를 봅니다.](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/integrations/analytics/track-clicked-component.html)

---
title: Adobe 클라이언트 데이터 레이어 확장
description: 몇 가지 기본 패턴에 따라 Adobe 클라이언트 데이터 레이어를 확장할 수 있습니다.
feature: Core Components, Adobe Client Data Layer
role: Architect, Developer, Admin
exl-id: f3d5555b-4f08-49de-ab0f-dc0fb04aadf8
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 100%

---

# Adobe 클라이언트 데이터 레이어 확장 {#extending-acdl}

콘텐츠 작성자가 데이터 레이어 관련 정보를 추가 입력할 수 있도록 맞춤형 대화 상자 옵션을 통해 핵심 구성 요소를 확장할 수 있습니다.

핵심 구성 요소에서 제공하는 데이터 레이어에 해당 필드를 포함하려면 특정 데이터 레이어 방식을 구현하는 구성 요소의 모델을 확장해야 합니다.

## 예: 제목 구성 요소 {#example}

[제목 구성 요소](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java)와 같은 핵심 구성 요소는 기본적으로 [`ComponentData`를 반환하는 `getData` 방식이 있는 [구성 요소](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java)를 확장합니다.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/datalayer/ComponentData.java)

`ComponentData`는 [`TitleImpl`에서 구성 요소가 `getDataLayerLinkUrl` 및 `getDataLayerTitle`와 같이 구현할 사전 정의된 필드를 일련화합니다.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/internal/models/v1/TitleImpl.java)

따라서 맞춤형 슬링 모델에는 추가 필드를 반환하기 위한 `ComponentData`를 확장하는 오브젝트를 반환하는 `getData` 방식이 있습니다.

이렇게 하면 데이터 레이어에 채워질 데이터 JSON을 통해 구성 요소의 HTML 요소에 `data-cmp-data-layer` 속성이 추가됩니다. 이 시점에서 해당 데이터나 관련 이벤트를 수신하는 스크립트를 구현할 수 있습니다.

>[!TIP]
>
>데이터 레이어의 유연성에 대해 추가 살펴보려면 맞춤형 구성 요소에 대한 데이터 활성화 방법을 포함하여 통합 옵션에 대해 검토하십시오.

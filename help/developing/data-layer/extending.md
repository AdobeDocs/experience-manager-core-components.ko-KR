---
title: Adobe 클라이언트 데이터 레이어 확장
description: Adobe 클라이언트 데이터 계층은 몇 가지 기본 패턴을 따라 확장할 수 있습니다
feature: 핵심 구성 요소, Adobe 클라이언트 데이터 레이어
role: Architect, Developer, Administrator
exl-id: f3d5555b-4f08-49de-ab0f-dc0fb04aadf8
source-git-commit: 8ff36ca143af9496f988b1ca65475497181def1d
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# Adobe 클라이언트 데이터 레이어 {#extending-acdl} 확장

컨텐츠 작성자가 데이터 레이어와 관련된 추가 정보를 입력할 수 있는 사용자 지정 대화 상자 옵션을 사용하여 코어 구성 요소를 확장할 수 있습니다.

핵심 구성 요소에서 제공하는 데이터 레이어에 이러한 필드를 포함하려면 고유한 특정 데이터 계층 메서드를 구현하는 구성 요소의 모델을 확장해야 합니다.

## 예:제목 구성 요소 {#example}

[제목 구성 요소](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java)와 같은 핵심 구성 요소는 기본적으로 [`ComponentData`.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/datalayer/ComponentData.java)을 반환하는 `getData` 메서드가 있는 [구성 요소](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java)를 확장합니다.

`ComponentData` 및 처럼 구성 요소가 구현할 수 있는 사전 정의된 필드 `getDataLayerLinkUrl` 를  `getDataLayerTitle`   [`TitleImpl`serialize합니다.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/internal/models/v1/TitleImpl.java)

따라서 사용자 지정 Sling 모델에는 `ComponentData`을 확장하는 개체를 반환하여 더 많은 필드를 반환하는 `getData` 메서드가 있을 수 있습니다.

이렇게 하면 에서는 데이터 계층에 채울 데이터의 JSON을 사용하여 구성 요소의 HTML 요소에 `data-cmp-data-layer` 속성을 추가합니다. 이 시점에서 이 데이터 또는 관련 이벤트를 수신하는 스크립트를 구현할 수 있습니다.

>[!TIP]
>
>데이터 계층의 유연성을 자세히 살펴보려면 사용자 지정 구성 요소에 대해 데이터 레이어를 활성화하는 방법을 포함한 통합 옵션에 대해 검토하십시오.

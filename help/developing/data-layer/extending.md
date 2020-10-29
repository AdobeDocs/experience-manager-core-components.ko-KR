---
title: Adobe 클라이언트 데이터 레이어 확장
description: 일부 기본 패턴에 따라 Adobe 클라이언트 데이터 레이어를 확장할 수 있습니다
translation-type: tm+mt
source-git-commit: 1ada05d5089ccef95d41d47468776654e397f31d
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---


# Adobe 클라이언트 데이터 레이어 확장 {#extending-acdl}

컨텐츠 작성자가 데이터 레이어와 관련된 추가 정보를 입력할 수 있는 사용자 정의 대화 상자 옵션을 사용하여 핵심 구성 요소를 확장할 수 있습니다.

핵심 구성 요소에서 제공하는 데이터 레이어에 이러한 필드를 포함하려면 고유한 특정 데이터 레이어 메서드를 구현하는 구성 요소의 모델을 확장해야 합니다.

## 예:제목 구성 요소 {#example}

제목 구성 요소와 같은 핵심 구성 요소는 [구성](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java) 요소 [를 확장하며](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/Title.java) 구성 `getData` 요소에는 기본적으로 반환되는 [`ComponentData`메서드가 있습니다.](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/models/datalayer/ComponentData.java)

`ComponentData` 구성 요소가 구현할 수 있는 사전 정의된 필드 `getDataLayerLinkUrl` 를 정리합니다(예: and `getDataLayerTitle` for [`TitleImpl`the](https://github.com/adobe/aem-core-wcm-components/blob/master/bundles/core/src/main/java/com/adobe/cq/wcm/core/components/internal/models/v1/TitleImpl.java)

따라서 사용자 정의 Sling 모델에는 추가 필드를 반환하도록 확장되는 개체를 반환하는 `getData` 메서드가 있을 `ComponentData` 수 있습니다.

이렇게 하면 데이터 레이어에 채울 데이터의 JSON과 함께 구성 요소의 HTML 요소에 `data-cmp-data-layer` 속성이 추가됩니다. 이때 이 데이터 또는 관련 이벤트를 수신하는 스크립트를 구현할 수 있습니다.

>[!TIP]
>
>데이터 레이어의 유연성을 자세히 살펴보려면 사용자 지정 구성 요소에 대해 데이터 레이어를 활성화하는 방법을 포함한 통합 옵션에 대해 검토하십시오.

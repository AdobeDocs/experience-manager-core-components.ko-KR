---
title: 컨텍스트 인식 구성 및 핵심 구성 요소 슬링
description: 핵심 구성 요소는 특정 기능에 대한 Sling 컨텍스트 인식 구성을 사용합니다
translation-type: tm+mt
source-git-commit: 24a810ff634f8846881dfa0095e879476d0f16f0
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---


# 컨텍스트 인식 구성 및 핵심 구성 요소 슬링 {#sling-context-aware-configurations}

컨텍스트 인식 구성은 Sling의 기능이며 컨텐츠 리소스 또는 리소스 트리와 관련되어 있고 핵심 구성 요소에서 활용하여 사이트 전체의 구성을 허용합니다.

## Sling 컨텍스트 인식 구성 {#context-aware-configurations}

중첩 컨텍스트 및 전역 폴백 값에 대해 상속이 필요한 일부 매개 변수를 공유할 수 있는 경우, 사이트마다 다른 사이트 영역에 대해 다른 구성이 필요할 수 있습니다. Sling 컨텍스트 인식 구성을 사용하면 됩니다.

Sling 컨텍스트 인식 구성에 대한 자세한 내용은 Apache 설명서를 [참조하십시오.](https://sling.apache.org/documentation/bundles/context-aware-configuration/context-aware-configuration.html)

## 핵심 구성 요소에서 사용 {#core-components}

많은 핵심 구성 요소 기능은 컨텍스트 인식 구성을 활용합니다. 이러한 모든 구성은 다음 노드 아래에 있습니다.

* `/conf/<my-site>/sling:configs/<my-configuration>`

개별 구성은 특정 구성 요소나 기능에 따라 다릅니다. 컨텍스트 인식 구성을 사용하는 핵심 구성 요소의 기능은 다음과 같습니다.

* [PDF 뷰어 구성 요소](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config)
* [Adobe 클라이언트 데이터 레이어](/help/developing/data-layer/overview.md#installation-activation)
* [AMP 지원](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)

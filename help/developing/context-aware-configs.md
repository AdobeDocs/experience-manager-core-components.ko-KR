---
title: 컨텍스트 인식 구성 및 핵심 구성 요소 슬링
description: 핵심 구성 요소는 특정 기능에 대한 Sling 컨텍스트 인식 구성을 사용합니다
translation-type: tm+mt
source-git-commit: 11e2c6da0fa93084b601437fd45fd65dd8d73231
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---


# 컨텍스트 인식 구성 및 핵심 구성 요소 슬링 {#sling-context-aware-configurations}

컨텍스트 인식 구성은 Sling의 기능이며 컨텐츠 리소스 또는 리소스 트리와 관련되어 있고 핵심 구성 요소에서 활용하여 사이트 전체의 구성을 허용합니다.

## Sling 컨텍스트 인식 구성 {#context-aware-configurations}

중첩 컨텍스트 및 전역 폴백 값에 대해 상속이 필요한 일부 매개 변수를 공유할 수 있는 경우, 사이트마다 다른 사이트 영역에 대해 다른 구성이 필요할 수 있습니다. AEM은 이러한 가능성을 지원하는 Sling 컨텍스트 인식 구성을 활용합니다.

AEM 구성에 대한 자세한 내용은 구성 및 구성 브라우저 설명서를 [참조하십시오.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/developing/configurations.html)

## 핵심 구성 요소에서 사용 {#core-components}

많은 핵심 구성 요소 기능은 컨텍스트 인식 구성을 활용합니다. 이러한 모든 구성은 다음 노드 아래에 있습니다.

* `/conf/<my-site>/sling:configs/<my-configuration>`

개별 구성은 특정 구성 요소나 기능에 따라 다릅니다. 컨텍스트 인식 구성을 사용하는 핵심 구성 요소의 기능은 다음과 같습니다.

* [PDF 뷰어 구성 요소](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config)
* [Adobe 클라이언트 데이터 레이어](/help/developing/data-layer/overview.md#installation-activation)
* [AMP 지원](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)

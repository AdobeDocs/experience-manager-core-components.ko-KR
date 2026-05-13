---
title: 슬링 컨텍스트 인식 구성 및 핵심 구성 요소
description: 핵심 구성 요소는 특정 기능에 대한 슬링 컨텍스트 인식 구성을 활용합니다.
role: Developer, Admin
exl-id: d35210f7-a65d-4768-ab9e-f12ec406da2d
TQID: https://experienceleague.adobe.com/jCBeHjuqLJzIxggeZxpusUkv9ZAyE-Ktr5N-gakWK18
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: ht
source-wordcount: 257
ht-degree: 100%

---

# 슬링 컨텍스트 인식 구성 및 핵심 구성 요소 {#sling-context-aware-configurations}

텍스트 인식 구성은 [슬링 기능](https://sling.apache.org/documentation/bundles/context-aware-configuration/context-aware-configuration.html)입니다. 핵심 구성 요소는 콘텐츠 리소스 또는 리소스 트리 관련 구성을 활용하여 전체 사이트를 구성할 수 있습니다.

## 슬링 텍스트 인식 구성 {#context-aware-configurations}

예를 들어 중첩된 컨텍스트와 전역 대체 값을 상속하는 매개 변수를 공유할 수 있는 사이트 지역별로 사이트를 다양하게 구성할 수 있습니다. AEM은 이 기능을 활성화하는 슬링 컨텍스트 인식 구성을 활용합니다.

AEM의 구성에 대한 자세한 내용은 [구성 및 구성 브라우저 설명서를 참조하십시오](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/configurations.html).

## 핵심 구성 요소에서 사용 {#core-components}

다양한 핵심 구성 요소 기능이 컨텍스트 인식 구성을 활용합니다. 그러한 구성은 모두 다음 노드 아래에 위치합니다.

* `/conf/<my-site>/sling:configs/<my-configuration>`

개별 구성은 특정 구성 요소나 기능에 따라 다릅니다. 텍스트 인식 구성을 사용하는 핵심 구성 요소의 기능은 다음과 같습니다.

* [페이지 구성 요소](https://github.com/adobe/aem-core-wcm-components/tree/main/content/src/content/jcr_root/apps/core/wcm/components/page/v3/page#loading-of-context-aware-cssjs)는 `link`, `script` 및 `meta` 태그를 렌더링할 때 컨텍스트 인식 구성을 사용합니다.
* [PDF 뷰어 구성 요소](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config)
* [Adobe 클라이언트 데이터 레이어](/help/developing/data-layer/overview.md#installation-activation)
* [AMP 지원](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)

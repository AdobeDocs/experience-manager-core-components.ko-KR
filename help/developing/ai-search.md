---
title: 컨텐츠 AI 검색 구성 요소 구성
description: 콘텐츠 AI 검색 구성 요소는 사이트 방문자에게 생성 AI 기반 검색을 제공합니다. 콘텐츠 작성자에 대해 이 구성 요소를 활성화하는 방법을 알아봅니다.
role: Developer, Admin
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: c18d9e03-ac7d-4811-9c92-3e92ddc70ade
source-git-commit: 865622469555a773138d3ff1b54138f2b76994b0
workflow-type: tm+mt
source-wordcount: 485
ht-degree: 2%

---


# 컨텐츠 AI 검색 구성 요소 구성 {#configure-content-ai-search-component}

콘텐츠 AI 검색 구성 요소는 사이트 방문자에게 생성 AI 기반 검색을 제공합니다. 콘텐츠 작성자에 대해 이 구성 요소를 활성화하는 방법을 알아봅니다.

## 사전 요구 사항 {#prerequisites}

* [콘텐츠 Source](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/contentsources)이(가) 하나 이상 이미 만들어졌으며 상태가 **사용 가능**&#x200B;입니다.
* **AEM Content AI Client** OSGi 구성(`ContentAIClientImpl`)이 작성자와 게시 모두에 설정되었으며, 올바른 API 자격 증명과 **기본 콘텐츠 Source** 값이 있습니다. 자격 증명을 얻는 방법은 [Adobe Developer Console 프로젝트 설정](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/setup-adc-project) 문서를 참조하십시오.

## 프록시 구성 요소 만들기 {#proxy-component}

모든 핵심 구성 요소와 마찬가지로 AEM과 함께 제공되는 기본 콘텐츠 AI 검색 구성 요소에 대한 프록시 구성 요소를 만드는 것이 좋습니다. `/apps`의 프록시 구성 요소에서 프로젝트별 변경 내용을 유지하면 `/libs`의 기본 구성 요소가 Adobe에 의해 자동으로 업데이트되며 프로젝트 구성 요소는 이러한 업데이트를 자동으로 상속합니다. 자세한 내용은 [핵심 구성 요소 사용](/help/get-started/using.md#aemaacs) 및 [구성 요소 지침](/help/developing/guidelines.md) 문서를 참조하십시오.

## 클라이언트 라이브러리 구성 {#clientlib}

콘텐츠 AI 검색 구성 요소가 [핵심 구성 요소에 클라이언트 라이브러리를 포함하기 위한 표준 패턴을 따르지 않습니다.](/help/developing/including-clientlibs.md) 대신 다음 단계를 수행합니다.

프로젝트의 페이지 구성 요소 `customheaderlibs.html`(CSS의 경우) 및 `customfooterlibs.html`(JS의 경우)에 다음 내용을 추가하십시오.

```html
<sly data-sly-use.clientLib="/libs/granite/sightly/templates/clientlib.html"
     data-sly-call="${clientLib.css @ categories='core.wcm.components.contentaisearch.v1'}"></sly>
```

프로젝트가 맨 위에 자체 브랜드 스타일을 겹치는 경우 이 카테고리 뒤에 프로젝트 자체 클라이언트 라이브러리에 대한 두 번째 카테고리를 추가합니다.

## 컨텐츠 AI 검색 구성 요소 사용 {#using}

이제 콘텐츠 작성자는 페이지에 콘텐츠 AI 검색 구성 요소를 배치할 수 있습니다. 자세한 내용은 [콘텐츠 AI 검색 구성 요소](/help/components/ai-search.md) 문서를 참조하십시오.

## 구성 요소가 콘텐츠 AI를 사용하는 방법 {#how-it-works}

* 표준 검색 쿼리는 컨텐츠 Source 색인과 동일한 검색 계층에서 제공되며, 구성된 소스에서 일치하는 페이지, 조각 또는 에셋을 반환합니다.
* AI 생성 요약이 활성화되면 구성 요소는 AEM 콘텐츠 AI 생성 끝점을 추가로 호출하여 동일한 인덱싱된 콘텐츠에서 응답을 중단하고 방문자가 확인할 수 있도록 요약과 함께 소스를 표시합니다.
* 두 기능 모두 동일한 관리 콘텐츠 Source에서 읽으므로 결과 및 요약은 현재 색인화된 콘텐츠와 일관됩니다. 획득을 다시 실행하면([콘텐츠 원본 제어](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/contentsources) 참조) 두 항목이 모두 새로 고쳐집니다.

## 다음 단계 {#next-steps}

* [콘텐츠 소스 제어](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/contentsources) - 이 구성 요소가 검색하는 콘텐츠 Source을 만들고 관리합니다.
* [Adobe Developer Console 프로젝트 설정](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/setup-adc-project) — OSGi Content AI 클라이언트 구성에서 사용하는 자격 증명을 가져옵니다.
* [콘텐츠 AI API 참조](https://developer.adobe.com/experience-cloud/experience-manager-apis/api/experimental/contentai/) - 이 구성 요소가 호출하는 기본 검색 및 생성 요약 끝점을 이해합니다.

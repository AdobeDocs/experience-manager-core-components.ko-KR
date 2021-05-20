---
title: 핵심 구성 요소에 Adobe 클라이언트 데이터 레이어 사용
description: 핵심 구성 요소에 Adobe 클라이언트 데이터 레이어 사용
feature: 핵심 구성 요소, Adobe 클라이언트 데이터 레이어
role: Architect, Developer, Administrator
exl-id: 55c984d3-deb7-4eda-a81d-7768791d2b46
source-git-commit: 8ff36ca143af9496f988b1ca65475497181def1d
workflow-type: tm+mt
source-wordcount: '980'
ht-degree: 5%

---

# 핵심 구성 요소 {#data-layer-core-components}에서 Adobe 클라이언트 데이터 레이어 사용

Adobe 클라이언트 데이터 계층의 목표는 모든 스크립트에 대한 모든 종류의 데이터를 노출하고 액세스하는 표준화된 방법을 제공하여 웹 사이트를 구현하는 노력을 줄이는 것입니다.

Adobe 클라이언트 데이터 계층은 플랫폼에 영향을 받지 않지만 AEM에서 사용할 수 있도록 핵심 구성 요소에 완전히 통합됩니다.

핵심 구성 요소와 마찬가지로 Adobe 클라이언트 데이터 계층의 코드는 개발자 설명서와 함께 GitHub에서 사용할 수 있습니다. 이 문서에서는 코어 구성 요소가 데이터 레이어와 상호 작용하는 방법에 대한 개요를 제공하지만 전체 기술 세부 사항은 GitHub 문서로 지연됩니다.

>[!TIP]
>
>Adobe 클라이언트 데이터 계층에 대한 자세한 내용은 [해당 GitHub 리포지토리의 리소스를 참조하십시오.](https://github.com/adobe/adobe-client-data-layer)
>
>Adobe 클라이언트 데이터 레이어와 코어 구성 요소 통합에 대한 자세한 내용은 코어 구성 요소 리포지토리의 [`DATA_LAYER_INTEGRATION.md`](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) 파일을 참조하십시오.

## 설치 및 활성화 {#installation-activation}

코어 구성 요소 릴리스 2.9.0부터 데이터 계층은 핵심 구성 요소와 함께 AEM 클라이언트 라이브러리로 배포되며, 설치할 필요가 없습니다. [AEM Project Archetype v. 24+](/help/developing/archetype/overview.md)에서 생성된 모든 프로젝트에는 기본적으로 활성화된 데이터 레이어가 포함됩니다.

데이터 레이어를 수동으로 활성화하려면 [컨텍스트 인식 구성](/help/developing/context-aware-configs.md)을 만들어야 합니다.

1. `/conf/<mySite>` 폴더 아래에 다음 구조를 만듭니다. 여기서 `<mySite>`은 사이트 프로젝트의 이름입니다.
   * `/conf/<mySite>/sling:configs/com.adobe.cq.wcm.core.components.internal.DataLayerConfig`
   * 여기서 각 노드에는 `jcr:primaryType`이 `nt:unstructured`로 설정되어 있습니다.
1. `enabled` 부울 속성을 추가하고 `true`(으)로 설정합니다.

   ![WKND 참조 사이트에서 DataLayerConfig 위치](/help/assets/datalayer-contextaware-sling-config.png)

   *WKND 참조 사이트에서 DataLayerConfig 위치*

1. `/content` 아래에 있는 사이트의 `jcr:content` 노드에 `sling:configRef` 속성을 추가합니다(예:`/content/<mySite>/jcr:content`)를 사용하여 이전 단계에서 `/conf/<mySite>`로 설정합니다.

1. 활성화되면 편집기 외부에서 사이트의 페이지를 로드하여 활성화를 확인할 수 있습니다. 예를 들어 편집기에서 **게시됨으로 보기** 옵션을 사용합니다. Inspect 페이지 소스 및 `<body>` 태그는 `data-cmp-data-layer-enabled` 속성을 포함해야 합니다.

   ```html
   <body class="page basicpage" id="page-id" data-cmp-data-layer-enabled>
       <script>
         window.adobeDataLayer = window.adobeDataLayer || [];
         adobeDataLayer.push({
             page: JSON.parse("{\x22page\u002D6c5d4b9fdd\x22:{\x22xdm:language\x22:\x22en\x22,\x22repo:path\x22:\x22\/content\/wknd\/language\u002Dmasters\/en.html\x22,\x22xdm:tags\x22:[],\x22xdm:template\x22:\x22\/conf\/wknd\/settings\/wcm\/templates\/landing\u002Dpage\u002Dtemplate\x22,\x22@type\x22:\x22wknd\/components\/page\x22,\x22dc:description\x22:\x22WKND is a collective of outdoors, music, crafts, adventure sports, and travel enthusiasts that want to share our experiences, connections, and expertise with the world.\x22,\x22dc:title\x22:\x22WKND Adventures and Travel\x22,\x22repo:modifyDate\x22:\x222020\u002D09\u002D29T07:50:13Z\x22}}"),
             event:'cmp:show',
             eventInfo: {
                 path: 'page.page\u002D6c5d4b9fdd'
             }
         });
       </script>
   ```

1. 브라우저의 개발자 도구를 열 수도 있으며 콘솔에서 `adobeDataLayer` JavaScript 개체를 사용할 수 있어야 합니다. 다음 명령을 입력하여 현재 페이지의 데이터 레이어 상태를 가져옵니다.

   ```javascript
   window.adobeDataLayer.getState();
   ```

## 지원되는 구성 요소 {#supported-components}

다음 구성 요소는 데이터 계층을 지원합니다.

* [어코디언](/help/components/accordion.md)
* [탐색 표시](/help/components/breadcrumb.md)
* [단추](/help/components/button.md)
* [회전판](/help/components/carousel.md)
* [콘텐츠 조각](/help/components/content-fragment-component.md)
* [이미지](/help/components/image.md)
* [언어 탐색](/help/components/language-navigation.md)
* [목록](/help/components/list.md)
* [탐색](/help/components/navigation.md)
* [페이지](/help/components/page.md)
* [진행률 표시줄](/help/components/progress-bar.md)
* [탭](/help/components/tabs.md)
* [티저](/help/components/teaser.md)
* [텍스트](/help/components/text.md)
* [제목](/help/components/title.md)

구성 요소에 의해 트리거된 [이벤트를 참조하십시오.](#events-components)

## 코어 구성 요소 데이터 스키마 {#data-schemas}

다음은 핵심 구성 요소가 데이터 레이어에서 사용하는 스키마 목록입니다.

### 구성 요소/컨테이너 항목 스키마 {#item}

구성 요소/컨테이너 항목 스키마는 다음 구성 요소에 사용됩니다.

* [탐색 표시](/help/components/breadcrumb.md)
* [단추](/help/components/button.md)
* [언어 탐색](/help/components/language-navigation.md)
* [목록](/help/components/list.md)
* [탐색](/help/components/navigation.md)
* [티저](/help/components/teaser.md)
* [텍스트](/help/components/text.md)
* [제목](/help/components/title.md)

구성 요소/컨테이너 항목 스키마는 다음과 같이 정의됩니다.

```javascript
id: {                   // component ID
    @type               // resource type
    repo:modifyDate     // last modified date
    dc:title            // title
    dc:description      // description
    xdm:text            // text
    xdm:linkURL         // link URL
    parentId            // parent component ID
}
```

다음 [event](#events)은(는) 구성 요소/컨테이너 항목 스키마와 관련되어 있습니다.

* `cmp:click`

### 페이지 스키마 {#page}

페이지 스키마는 다음 구성 요소에서 사용됩니다.

* [페이지](/help/components/page.md)

페이지 스키마는 다음과 같이 정의됩니다.

```javascript
id: {
    @type
    repo:modifyDate
    dc:title
    dc:description
    xdm:text
    xdm:linkURL
    parentId
    xdm:tags            // page tags
    repo:path           // page path
    xdm:template        // page template
    xdm:language        // page language
}
```

페이지 로드 시 `cmp:show` 이벤트가 트리거됩니다. 이 이벤트는 열기 `<body>` 태그 바로 아래에 있는 인라인 JavaScript에서 전달되어 데이터 레이어 이벤트 큐에서 가장 빠른 이벤트로 만듭니다.

### 컨테이너 스키마 {#container}

컨테이너 스키마는 다음 구성 요소에서 사용됩니다.

* [어코디언](/help/components/accordion.md)
* [탭](/help/components/tabs.md)
* [회전판](/help/components/carousel.md)

컨테이너 스키마는 다음과 같이 정의됩니다.

```javascript
id: {
    @type
    repo:modifyDate
    dc:title
    dc:description
    xdm:text
    xdm:linkURL
    parentId
    shownItems          // array of the displayed item IDs
}
```

다음 [events](#events)는 컨테이너 스키마와 관련되어 있습니다.

* `cmp:click`
* `cmp:show`
* `cmp:hide`

### 이미지 스키마 {#image}

이미지 스키마는 다음 구성 요소에서 사용됩니다.

* [이미지](/help/components/image.md)

이미지 스키마는 다음과 같이 정의됩니다.

```javascript
id: {
    @type
    repo:modifyDate
    dc:title
    dc:description
    xdm:text
    xdm:linkURL
    parentId
    image               // asset detail (see below section)
}
```

다음 [event](#events)은 이미지 스키마와 관련되어 있습니다.

* `cmp:click`

### 자산 스키마 {#asset}

자산 스키마가 [이미지 구성 요소 내에 사용됩니다.](/help/components/image.md)

자산 스키마는 다음과 같이 정의됩니다.

```javascript
id: {
    repo:id             // asset UUID
    repo:path           // asset path
    @type               // asset resource type
    xdm:tags            // asset tags
    repo:modifyDate
}
```

다음 [event](#events)은 자산 스키마와 관련되어 있습니다.

* `cmp:click`

### 컨텐츠 조각 스키마 {#content-fragment}

컨텐츠 조각 스키마는 [컨텐츠 조각 구성 요소에서 사용됩니다.](/help/components/content-fragment-component.md)

컨텐츠 조각 스키마는 다음과 같이 정의됩니다.

```javascript
id: {
    @type
    repo:modifyDate
    dc:title
    dc:description
    xdm:text
    xdm:linkURL
    parentId
    elements            // array of the Content Fragment elements
}
```

컨텐츠 조각 요소에 사용되는 스키마는 다음과 같습니다.

```javascript
{
    xdm:title           // title
    xdm:text            // text
}
```

## 코어 구성 요소 이벤트 {#events}

핵심 구성 요소가 데이터 계층을 통해 트리거되는 이벤트는 많습니다. 데이터 레이어와 상호 작용하기 위한 가장 좋은 방법은 [이벤트 리스너](https://github.com/adobe/adobe-client-data-layer/wiki#addeventlistener)를 등록하고 *그런 다음*&#x200B;는 이벤트를 트리거한 이벤트 유형 및/또는 구성 요소를 기반으로 작업을 수행하는 것입니다. 이렇게 하면 비동기 스크립트가 있는 잠재적 경쟁 조건이 발생하지 않습니다.

다음은 AEM 코어 구성 요소에서 제공하는 특별 이벤트입니다.

* **`cmp:click`** - 클릭 가능한 요소(속성이 있는 요소) `data-cmp-clickable` 를 클릭하면 데이터 레이어가 이벤트를  `cmp:click` 트리거합니다.
* **`cmp:show`** 및  **`cmp:hide`** - 아코디언(확장/축소), 회전 메뉴(다음/이전 단추) 및 탭(탭 선택) 구성 요소를 조작하면 데이터 레이어가  `cmp:show` 트리거되고  `cmp:hide` 이벤트가 각각 트리거됩니다. `cmp:show` 이벤트는 페이지 로드 시에도 발송되며 첫 번째 이벤트여야 합니다.
* **`cmp:loaded`** - 데이터 레이어가 페이지의 핵심 구성 요소로 채워지면 데이터 레이어에서 이벤트를  `cmp:loaded` 트리거합니다.

### 구성 요소 {#events-components}에 의해 트리거된 이벤트

다음 표에는 해당 이벤트와 함께 이벤트를 트리거하는 표준 코어 구성 요소 가 나열되어 있습니다.

| 구성 요소 | 이벤트 |
|---|---|
| [어코디언](/help/components/accordion.md) | `cmp:show` 및 `cmp:hide` |
| [단추](/help/components/button.md) | `cmp:click` |
| [탐색 표시](/help/components/breadcrumb.md) | `cmp:click` |
| [회전판](/help/components/carousel.md) | `cmp:show` 및 `cmp:hide` |
| [언어 탐색](/help/components/language-navigation.md) | `cmp:click` |
| [탐색](/help/components/navigation.md) | `cmp:click` |
| [페이지](/help/components/page.md) | `cmp:show` |
| [탭](/help/components/tabs.md) | `cmp:show` 및 `cmp:hide` |
| [티저](/help/components/teaser.md) | `cmp:click` |

### 이벤트 경로 정보 {#event-path-info}

AEM 코어 구성 요소에 의해 트리거되는 각 데이터 레이어 이벤트에는 다음 JSON 개체가 있는 페이로드가 포함됩니다.

```json
eventInfo: {
    path: '<component-path>'
}
```

여기서 `<component-path>`은 이벤트를 트리거한 데이터 계층에서 구성 요소에 대한 JSON 경로입니다.  `event.eventInfo.path` 을 통해 사용할 수 있는 값은 이벤트를 트리거한 구성 요소의 현재 상태를 검색하는 `adobeDataLayer.getState(<component-path>)` 의 매개 변수로 사용할 수 있으므로 중요합니다. 이 매개 변수를 사용하면 사용자 지정 코드가 추가 데이터에 액세스하여 데이터 레이어에 추가할 수 있습니다.

예:

```javascript
function logEventObject(event) {
    if(event.hasOwnProperty("eventInfo") && event.eventInfo.hasOwnProperty("path")) {
        var dataObject = window.adobeDataLayer.getState(event.eventInfo.path);
        console.debug("The component that triggered this event: ");
        console.log(dataObject);
    }
}

window.adobeDataLayer = window.adobeDataLayer || [];
window.adobeDataLayer.push(function (dl) {
     dl.addEventListener("cmp:show", logEventObject);
});
```

## 자습서

데이터 레이어 및 핵심 구성 요소를 자세히 살펴보시겠습니까? [이 실습 자습서를 확인하십시오](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/integrations/adobe-client-data-layer/data-layer-overview.html).

>[!TIP]
>
>데이터 계층의 유연성을 자세히 살펴보려면 사용자 지정 구성 요소에 대해 데이터 레이어를 활성화하는 방법을 포함한 통합 옵션에 대해 검토하십시오.

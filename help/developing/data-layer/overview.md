---
title: 핵심 구성 요소로 함께 Adobe 클라이언트 데이터 레이어 사용
description: 핵심 구성 요소로 함께 Adobe 클라이언트 데이터 레이어 사용
feature: Core Components, Adobe Client Data Layer
role: Architect, Developer, Admin
exl-id: 55c984d3-deb7-4eda-a81d-7768791d2b46
source-git-commit: 5994133947ff697f7c866fe61598c58e37e77008
workflow-type: tm+mt
source-wordcount: '952'
ht-degree: 100%

---


# 핵심 구성 요소로 함께 Adobe 클라이언트 데이터 레이어 사용 {#data-layer-core-components}

Adobe 클라이언트 데이터 레이어의 목표는 스크립트용 데이터 노출 및 사용을 위한 표준화된 방법을 제공하여 웹 사이트를 측정하는 수고를 줄이는 것입니다.

Adobe 클라이언트 데이터 레이어는 독립적인 플랫폼이지만 핵심 구성 요소에 완전히 통합되어 AEM에 사용됩니다.

핵심 구성 요소와 마찬가지로 Adobe 클라이언트 데이터 레이어용 코드는 개발자 설명서와 함께 GitHub에서 사용할 수 있습니다. 이 문서는 핵심 구성 요소가 데이터 레이어와 인터렉션하는 방법에 대한 개요를 제공하지만 전체 기술 정보는 GitHub 문서를 기반으로 합니다.

>[!TIP]
>
>Adobe 클라이언트 데이터 레이어에 대한 추가 정보는 [GitHub 저장소의 리소스를 참조하십시오.](https://github.com/adobe/adobe-client-data-layer)
>
>Adobe 클라이언트 데이터 레이어와 핵심 구성 요소 통합에 대한 추가 기술 세부 정보는 핵심 구성 요소 저장소의 [`DATA_LAYER_INTEGRATION.md`](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) 파일을 참조하십시오.

{{traditional-aem}}

## 설치 및 활성화 {#installation-activation}

핵심 구성 요소 릴리스 2.9.0부터 데이터 레이어는 핵심 구성 요소와 함께 AEM 클라이언트 라이브러리로 배포되고 설치할 필요가 없습니다. [AEM Project Archetype v. 24+](/help/developing/archetype/overview.md)에서 생성한 모든 프로젝트에는 기본적으로 활성화된 데이터 레이어가 포함됩니다.

데이터 레이어를 수동으로 활성화하려면 해당되는 [컨텍스트 인식 구성](/help/developing/context-aware-configs.md)을 제작해야 합니다.

1. `<mySite>`가 사이트의 프로젝트 이름인 `/conf/<mySite>` 폴더 아래에 다음 구조를 만듭니다.
   * `/conf/<mySite>/sling:configs/com.adobe.cq.wcm.core.components.internal.DataLayerConfig`
   * 각 모드에 `nt:unstructured`로 설정된 `jcr:primaryType`가 있는 경우.
1. `enabled`라는 부울 속성을 추가하고 `true`로 설정합니다.

   ![WKND 참조 사이트의 DataLayerConfig 위치](/help/assets/datalayer-contextaware-sling-config.png)

   *WKND 참조 사이트의 DataLayerConfig 위치*

1. `sling:configRef` 속성을 `/content`(예: `/content/<mySite>/jcr:content`) 아래 사이트의 `jcr:content` 노드에 추가하고 이전 단계에서 `/conf/<mySite>`로 설정합니다.

1. 활성화되면 편집기 외부 사이트 페이지를 로드(예: 편집기의 **게시로 보기** 옵션 사용)하여 활성화를 확인할 수 있습니다. 페이지 소스를 검사하는 경우 `<body>` 태그에 속성 `data-cmp-data-layer-enabled`가 포함되어야 합니다.

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

1. 브라우저의 개발자 도구를 열 수도 있고 콘솔에서 `adobeDataLayer` JavaScript 오브젝트를 사용해야 합니다. 현재 페이지의 데이터 레이어 상태를 다운로드하려면 다음 명령을 입력합니다.

   ```javascript
   window.adobeDataLayer.getState();
   ```

## 지원되는 구성 요소 {#supported-components}

다음 구성 요소는 데이터 레이어를 지원합니다.

* [아코디언](/help/components/accordion.md)
* [이동 경로](/help/components/breadcrumb.md)
* [버튼](/help/components/button.md)
* [슬라이드](/help/components/carousel.md)
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

[구성 요소에 의해 트리거된 이벤트](#events-components)도 참조하십시오.

## 핵심 구성 요소 데이터 스키마 {#data-schemas}

다음은 데이터 레이어와 함께 핵심 구성 요소가 사용하는 스키마 목록입니다.

### 구성 요소/컨테이너 항목 스키마 {#item}

다음 구성 요소에서 구성 요소/컨테이너 항목 스키마를 사용합니다.

* [이동 경로](/help/components/breadcrumb.md)
* [버튼](/help/components/button.md)
* [언어 탐색](/help/components/language-navigation.md)
* [목록](/help/components/list.md)
* [탐색](/help/components/navigation.md)
* [티저](/help/components/teaser.md)
* [텍스트](/help/components/text.md)
* [제목](/help/components/title.md)

구성 요소/컨테이너 항목 스키마를 다음과 같이 정의합니다.

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

다음 [이벤트](#events)는 구성 요소/컨테이너 항목 스키마와 관련성이 있습니다.

* `cmp:click`

### 페이지 스키마 {#page}

다음 구성 요소는 페이지 스키마를 사용합니다.

* [페이지](/help/components/page.md)

페이지 스키마를 다음과 같이 정의합니다.

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

`cmp:show`이벤트는 페이지 로드에서 트리거됩니다. 열기 `<body>` 태그 바로 아래 인라인 JavaScript에서 이 이벤트를 발송하게 되면 데이터 레이어 이벤트 큐에서 가장 빠른 이벤트가 됩니다.

### 컨테이너 스키마 {#container}

다음 구성 요소는 컨테이너 스키마를 사용합니다.

* [아코디언](/help/components/accordion.md)
* [탭](/help/components/tabs.md)
* [슬라이드](/help/components/carousel.md)

컨테이너 스키마를 다음과 같이 정의합니다.

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

다음 [이벤트](#events)는 컨테이너 스키마와 관련성이 있습니다.

* `cmp:click`
* `cmp:show`
* `cmp:hide`

### 이미지 스키마 {#image}

다음 구성 요소는 이미지 스키마를 사용합니다.

* [이미지](/help/components/image.md)

이미지 스키마를 다음과 같이 정의합니다.

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

다음 [이벤트](#events)는 이미지 스키마와 관련성이 있습니다.

* `cmp:click`

### 에셋 스키마 {#asset}

[이미지 구성 요소](/help/components/image.md) 내부에서 에셋 스키마를 사용합니다.

에셋 스키마를 다음과 같이 정의합니다.

```javascript
id: {
    repo:id             // asset UUID
    repo:path           // asset path
    @type               // asset resource type
    xdm:tags            // asset tags
    repo:modifyDate
}
```

다음 [이벤트](#events)는 에셋 스키마와 관련성이 있습니다.

* `cmp:click`

### 콘텐츠 조각 스키마 {#content-fragment}

[콘텐츠 조각 구성 요소](/help/components/content-fragment-component.md)는 콘텐츠 조각 스키마를 사용합니다.

콘텐츠 조각 스키마를 다음과 같이 정의합니다.

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

콘텐츠 조각 요소에 사용되는 스키마는 다음과 같습니다.

```javascript
{
    xdm:title           // title
    xdm:text            // text
}
```

## 핵심 구성 요소 이벤트 {#events}

데이터 레이어를 통해 핵심 구성 요소가 트리거하는 여러 이벤트가 있습니다. 데이터 래이어와 인터렉션하는 가장 좋은 방법은 [이벤트 리스너를 등록](https://github.com/adobe/adobe-client-data-layer/wiki#addeventlistener)한 *다음* 이벤트 유형 및/또는 이벤트를 트리거하는 구성 요소에 따라 조치를 취하는 것입니다. 이로써 비동기 스크립트로 잠재적 경합 조건을 방지할 수 있습니다.

다음은 AEM 핵심 구성 요소에서 제공하는 박스 이벤트의 외부입니다.

* **`cmp:click`** - 클릭 가능한 요소(`data-cmp-clickable` 속성을 가진 요소)를 클릭하면 데이터 레이어가 `cmp:click` 이벤트를 트리거할 수 있습니다.
* **`cmp:show`** 및 **`cmp:hide`** - 아코디언(확장/축소), 슬라이드(다음/이전 버튼)와 탭(탭 선택) 구성 요소를 조작하면 데이터 레이어가 `cmp:show` 및 `cmp:hide` 이벤트를 각각 트리거할 수 있습니다. 또한 페이지 로드에서 `cmp:show` 이벤트를 발송하면 첫 번째 이벤트가 될 수 있습니다.
* **`cmp:loaded`** - 페이지에서 데이터 레이어가 핵심 구성 요소로 채워지는 즉시 데이터 레이어가 `cmp:loaded` 이벤트를 트리거합니다.

### 구성 요소에 의해 트리거된 이벤트 {#events-components}

다음 테이블은 해당 이벤트와 함께 이벤트를 트리거하는 표준 구성 요소를 보여 줍니다.

| 구성 요소 | 이벤트 |
|---|---|
| [아코디언](/help/components/accordion.md) | `cmp:show` 및 `cmp:hide` |
| [버튼](/help/components/button.md) | `cmp:click` |
| [이동 경로](/help/components/breadcrumb.md) | `cmp:click` |
| [슬라이드](/help/components/carousel.md) | `cmp:show` 및 `cmp:hide` |
| [언어 탐색](/help/components/language-navigation.md) | `cmp:click` |
| [탐색](/help/components/navigation.md) | `cmp:click` |
| [페이지](/help/components/page.md) | `cmp:show` |
| [탭](/help/components/tabs.md) | `cmp:show` 및 `cmp:hide` |
| [티저](/help/components/teaser.md) | `cmp:click` |

### 이벤트 경로 정보 {#event-path-info}

AEM 핵심 구성 요소에 의해 트리거된 각 데이터 레이어 이벤트에는 다음 JSON 오브젝트와 함께 페이로드가 포함됩니다.

```json
eventInfo: {
    path: '<component-path>'
}
```

`<component-path>`가 이벤트를 트리거한 데이터 레이어의 JSON 경로에 있는 경우.  `event.eventInfo.path`를 통해 사용할 수 있는 값은 이벤트를 트리거한 구성 요소의 현재 상태를 검색하는 `adobeDataLayer.getState(<component-path>)`에 대한 매개 변수로 사용할 수 있기 때문에 중요합니다. 이로써 맞춤형 코드는 추가 데이터에 액세스하여 해당 데이터를 데이터 레이어에 추가할 수 있습니다.

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

## 튜토리얼

데이터 레이어와 핵심 구성 요소에 대해 더 자세히 살펴보시겠습니까? [이 실습형 튜토리얼](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/integrations/adobe-client-data-layer/data-layer-overview.html)을 살펴보십시오.

>[!TIP]
>
>데이터 레이어의 유연성에 대해 추가 살펴보려면 맞춤형 구성 요소에 대한 데이터 활성화 방법을 포함하여 통합 옵션에 대해 검토하십시오.

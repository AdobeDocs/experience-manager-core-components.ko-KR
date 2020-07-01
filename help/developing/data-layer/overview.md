---
title: 핵심 구성 요소에서 Adobe 클라이언트 데이터 레이어 사용
description: 핵심 구성 요소에서 Adobe 클라이언트 데이터 레이어 사용
translation-type: tm+mt
source-git-commit: 57116fa8f8a71259400881609775af4047cd2225
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 3%

---


# 핵심 구성 요소에서 Adobe 클라이언트 데이터 레이어 사용 {#data-layer-core-components}

Adobe Client Data Layer의 목표는 웹 사이트를 구축하는 데 필요한 표준 방법을 제공하여 모든 스크립트의 모든 종류의 데이터를 노출하고 액세스할 수 있도록 함으로써 웹 사이트를 구축하는 노력을 줄이는 것입니다.

Adobe 클라이언트 데이터 레이어는 플랫폼에 관계없이 AEM과 함께 사용하기 위해 핵심 구성 요소에 완벽하게 통합됩니다.

핵심 구성 요소와 마찬가지로 Adobe 클라이언트 데이터 레이어의 코드는 개발자 설명서와 함께 GitHub에서 사용할 수 있습니다. 이 문서에서는 핵심 구성 요소가 데이터 레이어와 상호 작용하는 방법에 대해 간략하게 설명합니다. 그러나 전체 기술 세부 사항은 GitHub 문서로 연기됩니다.

>[!TIP]
>
>Adobe 클라이언트 데이터 레이어에 대한 자세한 내용은 해당 GitHub 저장소의 리소스를 [참조하십시오.](https://github.com/adobe/adobe-client-data-layer)
>
>Adobe 클라이언트 데이터 레이어와 핵심 구성 요소의 통합에 대한 자세한 기술 내용은 핵심 구성 요소 저장소의 [`DATA_LAYER_INTEGRATION.md`](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) 파일을 참조하십시오.


## 설치 및 활성화 {#installation-activation}

핵심 구성 요소 릴리스 2.9.0부터는 데이터 레이어가 핵심 구성 요소와 함께 clientlib로 배포됩니다. 설치할 필요가 없습니다.

하지만 데이터 레이어는 기본적으로 활성화되지 않습니다. 데이터 레이어를 활성화하려면

1. 노드 아래에 다음 구조를 `/conf` 만듭니다.
   * `/conf/<mySite>/sling:configs/com.adobe.cq.wcm.core.components.internal.DataLayerConfig`
   * 노드 유형: `nt:unstructured`
1. 부울 속성을 추가하고 `enabled` 설정합니다 `true`.
1. 아래 사이트 `sling:configRef` 의 `jcr:content` 노드에 속성을 `/content` 추가합니다(예: `/content/<mySite>/jcr:content`) and set it to `/conf/<mySite>`.

활성화되면 편집기 외부에서 사이트 페이지를 로드하여 활성화를 확인할 수 있습니다. 페이지를 검사하면 Adobe Client Data Layer가 로드되었음을 확인할 수 있습니다.

## 핵심 구성 요소 데이터 스키마 {#data-schemas}

다음은 핵심 구성 요소에서 데이터 레이어와 함께 사용하는 스키마 목록입니다.

### 구성 요소/컨테이너 항목 스키마 {#item}

구성 요소/컨테이너 항목 스키마는 다음 구성 요소에서 사용됩니다.

* [탐색 표시](/help/components/breadcrumb.md)
* [단추](/help/components/button.md)
* [언어 탐색](/help/components/language-navigation.md)
* [목록](/help/components/list.md)
* [탐색](/help/components/navigation.md)
* [티저](/help/components/teaser.md)
* [텍스트](/help/components/text.md)
* [제목](/help/components/title.md)

구성 요소/컨테이너 항목 스키마는 다음과 같이 정의됩니다.

```
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


### 페이지 스키마 {#page}

페이지 스키마는 다음 구성 요소에서 사용됩니다.

* [페이지](/help/components/page.md)

페이지 스키마는 다음과 같이 정의됩니다.

```
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

### 컨테이너 스키마 {#container}

컨테이너 스키마는 다음 구성 요소에서 사용됩니다.

* [어코디언](/help/components/accordion.md)
* [탭](/help/components/tabs.md)
* [회전판](/help/components/carousel.md)

컨테이너 스키마는 다음과 같이 정의됩니다.

```
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

### 이미지 스키마 {#image}

이미지 스키마는 다음 구성 요소에서 사용됩니다.

* [이미지](/help/components/image.md)

이미지 스키마는 다음과 같이 정의됩니다.

```
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

### 자산 스키마 {#asset}

자산 스키마가 [이미지 구성 요소 내에서 사용됩니다.](/help/components/image.md)

자산 스키마는 다음과 같이 정의됩니다.

```
id: {
    repo:id             // asset UUID
    repo:path           // asset path
    @type               // asset resource type
    xdm:tags            // asset tags
    repo:modifyDate
}
```


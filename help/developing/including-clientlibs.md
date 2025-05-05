---
title: 클라이언트 라이브러리 및 핵심 구성 요소
description: 핵심 구성 요소는 다양한 클라이언트 라이브러리와 함께 제공되며 자체 라이브러리를 포함할 수 있는 기능을 제공합니다.
role: Architect, Developer, Admin
exl-id: 84e7c178-247b-42a2-99bf-6d1699ecee14
source-git-commit: d39fe0084522f67664203a026340b23d325c1883
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 100%

---


# 클라이언트 라이브러리 및 핵심 구성 요소 {#client-libraries}

핵심 구성 요소는 다양한 클라이언트 라이브러리와 함께 제공되며 자체 라이브러리를 포함할 수 있는 기능을 제공합니다.

## 제공되는 클라이언트 라이브러리 {#provided}

핵심 구성 요소는 기본적으로 다음과 같은 클라이언트 라이브러리를 제공합니다.

* **site** clientlib는 사이트에 적용할 구성 요소의 최소한의 기능적 동작을 제공합니다.
   * 이는 구현이 프로젝트를 확장하고 [맞춤화](/help/developing/customizing.md)하여 원하는 모양과 기능을 달성하도록 장려하여 프로젝트를 가속화하는 출발점 역할을 합니다.
* **editor** clientlib는 작성 대화 상자에 적용되어 예상되는 기능과 모양을 보장합니다.
* **editorhook** clientlib는 편집 모드로 로드 시 사이트에 적용됩니다.
   * 여기에는 편집기가 트리거한 이벤트에서 실행되는 JavaScript 코드가 포함되어 있어 동적 기능의 초기화를 용이하게 합니다.
* 일부 구성 요소에는 [Dynamic Media](/help/components/image.md#dynamic-media)와 함께 사용하는 경우와 같이 특정 상황에서 사용하도록 설계된 특정 추가 clientlib가 포함될 수 있습니다.

## 클라이언트 라이브러리 포함 {#including}

사용 사례에 따라 [클라이언트 라이브러리](/help/developing/archetype/front-end.md#clientlibs)를 다양한 방식으로 포함시킬 수 있습니다. 다음은 각각 샘플 [HTL 스니펫](https://experienceleague.adobe.com/docs/experience-manager-htl/using/overview.html?lang=ko)이 포함된 예시입니다.

### 권장 기본 사용 {#recommended-default-usage}

상황에 맞는 모범 사례를 조사할 시간이 없다면 페이지 `head` 요소 내부에 다음 HTL 라인을 배치하여 클라이언트 라이브러리를 포함시킵니다.

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories='wknd.base', defer=true}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

페이지`head`의 CSS와 JS가 여기에 포함되지만, `defer` 속성을 JS `script`에 추가하는 경우 스크립트 실행 전에 브라우저는 DOM이 준비 상태가 될 때까지 기다리다가 페이지 로드 속도를 최적화합니다.

### 기본 사용 {#basic-usage}

해당 CSS 요소 `link` 및/또는 JS `script` 요소를 모두 생성하며 클라이언트 라이브러리 범주의 JS 및 CSS가 포함된 기본 구문은 다음과 같습니다.

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

여러 클라이언트 라이브러리 범주에서 동일한 작업을 동시에 수행하기 위해 문자열 배열을 `categories` 매개 변수에 전달할 수 있습니다.

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories=['wknd.base', 'cq.foundation']}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

### CSS 또는 JS만 해당 {#css-js-only}

CSS는 HTML `head` 요소에 포함되고, JS는 `body` 요소를 닫기 직전에 포함되는 경우가 자주 있습니다.

`head`에서 CSS만 포함되고 JS는 포함되지 않는 경우에 `cssIncludes`를 사용합니다.

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssIncludes @ context="unsafe"}
</sly>
```

`body` 닫기 전에 JS만 포함되고 CSS가 포함되지 않는 경우에 `jsIncludes`를 사용합니다.

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsIncludes @ context="unsafe"}
</sly>
```

### 속성 {#attributes}

속성을 생성된 CSS `link` 요소 및/또는 JS `script` 요소에 적용하려면 다음 여러 매개 변수를 사용합니다.

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories='wknd.base',
    media='print',
    async=true,
    defer=true,
    onload='console.log(\'loaded: \' + this.src)',
    crossorigin='anonymous'}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

CSS `link` 속성을 `jsAndCssIncludes` 및 `cssIncludes`에 전달할 수 있습니다.

* `media`: string JS `script` 속성을 `jsAndCssIncludes` 및 `jsIncludes`에 전달할 수 있습니다.
* `async`: 부울
* `defer`: 부울
* `onload`: 문자열
* `crossorigin`: 문자열

### 인라인 {#inlining}

최적화, 이메일 또는 [AMP](amp.md) 중 어떠한 경우든 CSS 또는 JS를 HTML 출력으로 인라인해야 합니다.

CSS를 인라인하려면 `cssInline`를 사용할 수 있으며, 이 경우 주변 `style` 요소를 작성해야 합니다.

```html
<style type="text/css"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssInline @ context="unsafe"}
</style>
```

마찬가지로 JS를 인라인하려면 `jsInline`를 사용할 수 있으며, 이 경우 주변 `script` 요소를 작성해야 합니다.

```html
<script type="text/javascript"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsInline @ context="unsafe"}
</script>
```

### 텍스트 인식 CSS 및 JavaScript 로드 중 {#context-aware-loading}

[페이지 구성 요소](/help/components/page.md)는 로드 중인 개발자 정의된 컨텍스트 인식 CSS, JavaScript 또는 메타 태그를 지원합니다.

이는 다음 구조를 사용하는 `com.adobe.cq.wcm.core.components.config.HtmlPageItemsConfig`의 [컨텍스트 인식 리소스](context-aware-configs.md)를 통해 수행됩니다.

```text
com.adobe.cq.wcm.core.components.config.HtmlPageItemsConfig
    - prefixPath="/some/path"
    + item01
        - element=["link"|"script"|"meta"]
        - location=["header"|"footer"]
        + attributes
            - attributeName01="attributeValue01"
            - attributeName02="attributeValue02"
            ...
    + item02
        ...
    ...
```

자세한 내용은 [페이지 구성 요소에 대한 기술 설명서](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/page/v2/page#loading-of-context-aware-cssjs)를 참조하십시오.

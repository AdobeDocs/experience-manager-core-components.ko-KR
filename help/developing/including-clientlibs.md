---
title: 클라이언트 라이브러리 포함
description: 사용 사례에 따라 클라이언트 라이브러리를 포함하는 방법에는 여러 가지가 있습니다.
role: Architect, Developer, Admin
exl-id: 84e7c178-247b-42a2-99bf-6d1699ecee14
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 3%

---

# 클라이언트 라이브러리 포함 {#including-client-libraries}

사용 사례에 따라 [클라이언트 라이브러리](/help/developing/archetype/uifrontend.md#clientlibs)를 포함하는 방법은 여러 가지가 있습니다. 이 문서에서는 각각에 대한 예제 및 샘플 [HTL 코드 조각](https://docs.adobe.com/content/help/ko/experience-manager-htl/using/overview.html)을 제공합니다.

## 권장 기본 사용 {#recommended-default-usage}

현재 상황에서 가장 좋은 결과를 조사할 시간이 없는 경우 페이지 `head` 요소 내에 다음 HTL 줄을 배치하여 클라이언트 라이브러리를 포함하십시오.

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories='wknd.base', defer=true}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

여기에는 페이지 `head`에 CSS와 JS가 모두 포함되지만, JS `defer` 속성에 `script`를 추가하면 브라우저가 스크립트를 실행하기 전에 DOM이 준비될 때까지 기다렸다가 페이지 로드 속도가 최적화됩니다.

## 기본 사용 {#basic-usage}

모든 해당 CSS `link` 요소 및/또는 JS `script` 요소를 생성하는 클라이언트 라이브러리 카테고리의 JS 및 CSS를 모두 포함하는 기본 구문은 다음과 같습니다.

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

한 번에 여러 클라이언트 라이브러리 카테고리에 대해 동일한 작업을 수행하려면 문자열 배열을 `categories` 매개 변수에 전달할 수 있습니다.

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories=['wknd.base', 'cq.foundation']}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

## CSS 또는 JS만 해당 {#css-js-only}

CSS를 HTML `head` 요소에 배치하려는 경우가 많은데 JS는 `body` 요소를 닫기 바로 전에 포함됩니다.

`head`에서 JS가 아닌 CSS만 포함하려면 `cssIncludes` 를 사용하십시오.

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssIncludes @ context="unsafe"}
</sly>
```

`body` 닫기 전에 CSS가 아닌 JS만 포함하려면 `jsIncludes` 를 사용하십시오.

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsIncludes @ context="unsafe"}
</sly>
```

## 속성 {#attributes}

생성된 CSS `link` 요소 및/또는 JS `script` 요소에 속성을 적용하려면 많은 매개 변수를 사용할 수 있습니다.

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

`jsAndCssIncludes` 및 `cssIncludes`에 전달할 수 있는 CSS `link` 속성:

* `media`: 및  `script` 에 전달할 수 있는 string JS  `jsAndCssIncludes` 속성  `jsIncludes`:
* `async`: 부울
* `defer`: 부울
* `onload`: 문자열
* `crossorigin`: 문자열

## 인라인 {#inlining}

최적화를 위해 또는 이메일이나 [AMP의 경우](amp.md) CSS 또는 JS를 HTML의 출력으로 인라인으로 설정해야 할 수도 있습니다.

CSS를 인라인으로 지정하려면 `cssInline`을 사용할 수 있습니다. 이 경우 주변 `style` 요소를 작성해야 합니다.

```html
<style type="text/css"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssInline @ context="unsafe"}
</style>
```

마찬가지로 JS를 인라인으로 채우려면 `jsInline` 을 사용할 수 있습니다. 이 경우 주변 `script` 요소를 작성해야 합니다.

```html
<script type="text/javascript"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsInline @ context="unsafe"}
</script>
```

## 컨텍스트 인식 CSS 및 JavaScript 로드 {#context-aware-loading}

[페이지 구성 요소](/help/components/page.md)는 개발자 정의 컨텍스트 인식 CSS, JavaScript 또는 메타 태그 로딩도 지원합니다.

이 작업은 다음 구조를 사용하여 `com.adobe.cq.wcm.core.components.config.HtmlPageItemsConfig`에 대한 [컨텍스트 인식 리소스](context-aware-configs.md)를 만들어 수행합니다.

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

[자세한 내용은 페이지 구성 요소에 대한 기술 설명서 를 참조하십시오.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/page/v2/page#loading-of-context-aware-cssjs)

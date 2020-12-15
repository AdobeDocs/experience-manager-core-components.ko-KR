---
title: 클라이언트 라이브러리 포함
description: 사용 사례에 따라 클라이언트 라이브러리를 포함하는 다양한 방법이 있습니다.
translation-type: tm+mt
source-git-commit: afce571ada011c38c83830628f09a9e268658965
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 3%

---


# 클라이언트 라이브러리 포함 {#including-client-libraries}

사용 사례에 따라 [클라이언트 라이브러리](/help/developing/archetype/uifrontend.md#clientlibs)를 포함하는 여러 가지 방법이 있습니다. 이 문서에서는 예시와 각 HTML 코드 조각](https://docs.adobe.com/content/help/ko-KR/experience-manager-htl/using/overview.html)에 대한 샘플 [을 제공합니다.

## 권장 기본 사용량 {#recommended-default-usage}

상황에 가장 적합한 항목을 조사할 시간이 없는 경우 페이지 `head` 요소 안에 다음 HTML 줄을 배치하여 클라이언트 라이브러리를 포함시키십시오.

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories='wknd.base', defer=true}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

CSS와 JS가 모두 페이지 `head`에 포함되지만 JS `defer` 속성에 `script`가 추가되므로 브라우저가 스크립트를 실행하기 전에 DOM이 준비될 때까지 기다렸다가 페이지 로드 속도를 최적화합니다.

## 기본 사용량 {#basic-usage}

해당 CSS `link` 요소 및/또는 JS `script` 요소를 모두 생성하는 클라이언트 라이브러리 범주의 JS와 CSS를 모두 포함하는 기본 구문은 다음과 같습니다.

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

여러 클라이언트 라이브러리 카테고리에 대해 동시에 동일한 작업을 수행하려면 문자열 배열을 `categories` 매개 변수로 전달할 수 있습니다.

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories=['wknd.base', 'cq.foundation']}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

## CSS 또는 JS만 {#css-js-only}

CSS를 HTML `head` 요소에 배치하려는 경우가 많고 JS에는 `body` 요소가 닫기 직전에 포함됩니다.

`head`에서 JS가 아닌 CSS만 포함하려면 `cssIncludes`:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssIncludes @ context="unsafe"}
</sly>
```

`body` 닫기 전에 CSS가 아닌 JS만 포함하려면 `jsIncludes`:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsIncludes @ context="unsafe"}
</sly>
```

## 속성 {#attributes}

생성된 CSS `link` 요소 및/또는 JS `script` 요소에 속성을 적용하려면 다양한 매개 변수를 사용할 수 있습니다.

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

* `media`:다음 `script` 으로 전달할 수 있는 문자열 JS  `jsAndCssIncludes` 속성 `jsIncludes`:
* `async`: 부울
* `defer`: 부울
* `onload`: 문자열
* `crossorigin`: 문자열

## {#inlining} 삽입

경우에 따라 최적화나 이메일 또는 [AMP의 경우,](amp.md)CSS나 JS를 HTML 출력으로 인라인으로 지정해야 할 수 있습니다.

CSS를 인라인으로 표시하려면 `cssInline`을 사용할 수 있습니다. 이 경우 주변 `style` 요소를 작성해야 합니다.

```html
<style type="text/css"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssInline @ context="unsafe"}
</style>
```

마찬가지로 JS의 인라인에 `jsInline`을 사용할 수 있습니다. 이 경우 주변 `script` 요소를 작성해야 합니다.

```html
<script type="text/javascript"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsInline @ context="unsafe"}
</script>
```

## 컨텍스트 인식 CSS 및 JavaScript {#context-aware-loading} 로드

[페이지 구성 요소](/help/components/page.md)는 개발자가 정의한 컨텍스트 인식 CSS, JavaScript 또는 메타 태그를 로드할 수도 있습니다.

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

[자세한 내용은 페이지 구성 요소에 대한 기술 설명서를 참조하십시오.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/page/v2/page#loading-of-context-aware-cssjs)

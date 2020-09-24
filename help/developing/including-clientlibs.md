---
title: 클라이언트 라이브러리 포함
description: 사용 사례에 따라 클라이언트 라이브러리를 포함하는 다양한 방법이 있습니다.
translation-type: tm+mt
source-git-commit: 24f718be2ba66113eda970c213c6ce4baec51752
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 3%

---


# 클라이언트 라이브러리 포함 {#including-client-libraries}

사용 사례에 따라 [클라이언트 라이브러리를](/help/developing/archetype/uifrontend.md#clientlibs) 포함하는 다양한 방법이 있습니다. 이 문서에서는 각각에 대한 예제 및 샘플 [HTML 코드 조각을](https://docs.adobe.com/content/help/ko-KR/experience-manager-htl/using/overview.html) 제공합니다.

## 권장 기본 사용 {#recommended-default-usage}

상황에 가장 적합한 요소를 조사할 시간이 없는 경우 다음 HTL 줄을 페이지 `head` 요소 내에 배치하여 클라이언트 라이브러리를 포함시키십시오.

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories='wknd.base', defer=true}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

여기에는 페이지에 CSS와 JS가 모두 포함되지만 JS에 `head``defer` `script` 속성을 추가하면 브라우저가 스크립트를 실행하기 전에 DOM이 준비될 때까지 기다렸다가 페이지 로드 속도를 최적화합니다.

## 기본 사용 {#basic-usage}

모든 해당 CSS `link` 요소 및/또는 JS `script` 요소를 생성하는 클라이언트 라이브러리 카테고리의 JS와 CSS를 모두 포함하는 기본 구문은 다음과 같습니다.

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

## CSS 또는 JS만 해당 {#css-js-only}

CSS 포함 사항을 HTML `head` 요소에 삽입하려는 경우가 많고 JS에 `body` 요소가 닫기 직전에 포함됩니다.&#x200B;
JS가 `head``cssIncludes`아닌 CSS만 포함하려면

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssIncludes @ context="unsafe"}
</sly>
```

닫기 전에 `body` CSS가 아닌 JS만 포함하려면 다음을 사용하십시오 `jsIncludes`.

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

및 `link` 에 전달할 수 있는 CSS 속성 `jsAndCssIncludes` `cssIncludes`:

* `media`:문자열&#x200B; JS `script` 속성 `jsAndCssIncludes` 및 `jsIncludes`다음

* `async`: 부울
* `defer`: 부울
* `onload`: 문자열
* `crossorigin`: 문자열

## 삽입 {#inlining}

최적화, 이메일 또는 [AMP의 경우](amp.md) CSS 또는 JS를 HTML의 출력으로 인라인으로 지정해야 하는 경우가 있습니다&#x200B;.
CSS를 인라인으로 만들려면, 사용할 `cssInline` 수 있습니다. 이 경우 주변 `style` 요소를 작성해야 합니다.

```html
<style type="text/css"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssInline @ context="unsafe"}
</style>
```

마찬가지로 JS의 인라인에 대해 사용할 `jsInline` 수 있습니다. 이 경우 주변 `script` 요소를 작성해야 합니다.

```html
<script type="text/javascript"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsInline @ context="unsafe"}
</script>
```

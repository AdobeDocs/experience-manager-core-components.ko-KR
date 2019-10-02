---
title: 구성 요소 포함
seo-title: Embed Component
description: 포함 구성 요소를 사용하면 AEM 컨텐츠 페이지에 외부 컨텐츠를 포함할 수 있습니다.
seo-description: 포함 구성 요소를 사용하면 AEM 컨텐츠 페이지에 외부 컨텐츠를 포함할 수 있습니다.
content-type: 참조
topic-tags: 핵심 구성 요소
translation-type: tm+mt
source-git-commit: d748bf211ec36d12cac016ca9bf707f24db1ce48

---


# 구성 요소 포함{#embed-component}

핵심 구성 요소 포함 구성 요소를 사용하면 AEM 컨텐츠 페이지에 외부 컨텐츠를 포함할 수 있습니다.

## 사용량 {#usage}

핵심 구성 요소 포함 구성 요소를 사용하면 컨텐츠 작성자가 AEM 컨텐츠 페이지에 포함할 선택된 외부 컨텐츠를 정의할 수 있습니다. 또한 포함할 자유 형식 HTML을 정의하는 옵션이 있습니다.

* 구성 요소의 속성은 [구성 대화 상자에서](#configure-dialog)정의할 수 있습니다.
* 구성 요소를 페이지에 추가할 때의 기본값은 [디자인 대화 상자에서](#design-dialog)정의할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

포함 구성 요소의 현재 버전은 v1이며, 이 버전은 2019년 9월 핵심 구성 요소 릴리스 2.7.0에서 도입되었으며 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소 버전이 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |---|
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 핵심 구성 요소 [버전을 참조하십시오](versions.md).

## 샘플 구성 요소 출력 {#sample-component-output}

포함 구성 요소와 구성 옵션의 예 및 HTML 및 JSON 출력을 보려면 구성 요소 [라이브러리를 참조하십시오](http://opensource.adobe.com/aem-core-wcm-components/library/embed.html).

## 기술 정보 {#technical-details}

포함 구성 요소에 대한 최신 기술 문서는 GitHub에서 [찾을 수 있습니다](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed).

핵심 구성 요소 개발에 대한 자세한 내용은 핵심 구성 요소 개발자 [설명서를](developing.md)참조하십시오.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자에서는 컨텐츠 작성자가 페이지에 포함할 외부 리소스를 정의할 수 있습니다. 먼저 포함할 리소스 유형을 선택합니다.URL ******,**&#x200B;임베드 가능한 **또는** HTML.

### URL {#url}

The simplest embed is the URL. URL 필드에 포함할 리소스의 URL을 **붙여넣으면** 됩니다. The component will attempt to access the resource and if it can be rendered by one of the processors, it will display a confirmation message below the URL field. **** If not, the field will be marked in error.

The Embed Component ships with processors for the following types of resources:

* Resources that comply with the oEmbed standard including Facebook Post, Instagram, SoundCloud, Twitter, and YouTube[](https://oembed.com/)
* Pinterest

개발자는 내장 구성 요소의 개발자 설명서를 [따라 추가 URL 프로세서를 추가할 수 있습니다.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![](assets/screen-shot-2019-09-25-10.08.29.png)

### 포함 가능 {#embeddable}

임베드 변수를 사용하면 임베드된 리소스를 보다 맞춤화하여 매개 변수화할 수 있으며 추가 정보를 포함할 수 있습니다. An author is able to select from pre-configured trusted embeddables and the component ships with a Youtube embeddable out-of-the-box.

임베드 **가능한** 필드는 사용할 프로세서 유형을 정의합니다. YouTube 임베드 가능한 경우 다음을 정의할 수 있습니다.

* **Video ID - The unique video ID from YouTube of the resource you want to embed**
* **Width - The width of the embedded video**
* **높이** - 포함된 비디오의 높이

Other embeddables would offer similar fields and can be defined by a developer by following the developer documentation of the Embed Component.[](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![](assets/screen-shot-2019-09-25-10.15.00.png)

>[!NOTE]
>Embeddables must be enabled at the template level via the Design Dialog to be available to the page author.[](#design-dialog)

### HTML {#html}

You can add free-form HTML to your page using the Embed Component.

![](assets/screen-shot-2019-09-25-10.20.00.png)

>[!NOTE]
>스크립트와 같은 안전하지 않은 태그는 입력한 HTML에서 필터링되며 결과 페이지에서 렌더링되지 않습니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 사용하여 포함 구성 요소를 사용하는 컨텐츠 작성자에게 사용 가능한 옵션과 포함 구성 요소를 배치할 때 설정된 기본값을 정의할 수 있습니다.

![](assets/screen-shot-2019-09-25-10.25.28.png)

* **URL 비활성화** - **선택 시 컨텐츠 작성자에** 대한 URL 옵션을 비활성화합니다.
* **포함 가능** 비활성화 - 임베드 가능한 **프로세서에 상관없이** 선택한 경우 컨텐츠 작성자에 대한 포함 가능 옵션을 비활성화합니다.
* **HTML 비활성화** - **선택 시 컨텐츠 작성자에** 대한 HTML 옵션을 비활성화합니다.
* **임베드 가능** - 임베드 가능한 프로세서가 활성 상태인 경우 컨텐츠 작성자가 사용할 수 있는 임베드 가능한 프로세서를 정의하는 **다중** 세그먼트입니다.

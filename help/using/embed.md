---
title: 구성 요소 포함
seo-title: 구성 요소 포함
description: 포함 구성 요소를 사용하면 AEM 컨텐츠 페이지에 외부 컨텐츠를 포함할 수 있습니다.
seo-description: 포함 구성 요소를 사용하면 AEM 컨텐츠 페이지에 외부 컨텐츠를 포함할 수 있습니다.
content-type: 참조
topic-tags: 핵심 구성 요소
translation-type: tm+mt
source-git-commit: 97f1461b57079806f9f96d325d9b763538e32127

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

가장 간단한 임베드란 URL입니다. URL 필드에 포함할 리소스의 URL을 **붙여넣으면** 됩니다. 구성 요소는 리소스에 액세스하려고 하며, 프로세서 중 하나에서 렌더링할 수 있는 경우 URL 필드 아래에 확인 메시지가 **표시됩니다** . 그렇지 않으면 필드가 오류로 표시됩니다.

포함 구성 요소는 다음과 같은 유형의 리소스에 대해 프로세서와 함께 제공됩니다.

* Resources that comply with the oEmbed standard including Facebook Post, Instagram, SoundCloud, Twitter, and YouTube[](https://oembed.com/)
* Pinterest

개발자는 내장 구성 요소의 개발자 설명서를 [따라 추가 URL 프로세서를 추가할 수 있습니다.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![](assets/screen-shot-2019-09-25-10.08.29.png)

### 포함 가능 {#embeddable}

Embeddables allow for more customization of the embedded resource, which can be parameterized and include additional information. An author is able to select from pre-configured trusted embeddables and the component ships with a Youtube embeddable out-of-the-box.

The Embeddable field defines the type of processor you want to use. **** In the case of the YouTube embeddable you can then define:

* **Video ID - The unique video ID from YouTube of the resource you want to embed**
* **Width - The width of the embedded video**
* **Height - The height of the embedded video**

Other embeddables would offer similar fields and can be defined by a developer by [following the developer documentation of the Embed Component.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![](assets/screen-shot-2019-09-25-10.15.00.png)

>[!NOTE]
>Embeddables must be enabled at the template level via the [Design Dialog](#design-dialog) to be available to the page author.

### HTML {#html}

You can add free-form HTML to your page using the Embed Component.

![](assets/screen-shot-2019-09-25-10.20.00.png)

>[!NOTE]
>Any unsafe tags such as scripts will be filtered from the entered HTML and will not be rendered on the resulting page.

## Design Dialog {#design-dialog}

The design dialog allows the template author to define the options available to the content author who uses the Embed Component and the defaults set when placing the Embed Component.

![](assets/screen-shot-2019-09-25-10.25.28.png)

* **URL 비활성화** - **선택 시 컨텐츠 작성자에** 대한 URL 옵션을 비활성화합니다.
* **Disable Embeddables** - Disables the **Embeddable** option for the content author when selected, regardless of which embeddable processors are allowed.
* **HTML 비활성화** - **선택 시 컨텐츠 작성자에** 대한 HTML 옵션을 비활성화합니다.
* **임베드 가능** - 임베드 가능한 프로세서가 활성 상태인 경우 컨텐츠 작성자가 사용할 수 있는 임베드 가능한 프로세서를 정의하는 **다중** 세그먼트입니다.

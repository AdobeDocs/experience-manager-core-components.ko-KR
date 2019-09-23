---
title: 페이지 구성 요소
seo-title: 페이지 구성 요소
description: The Page Component is an extensible page component designed to work with the template editor and allow page header/footer and structure components to be assembled with the template editor.
seo-description: The Page Component is an extensible page component designed to work with the template editor and allow page header/footer and structure components to be assembled with the template editor.
uuid: 7052a5b1-e7f1-4944-a55c-faf739b6e89c
contentOwner: 사용자
content-type: 참조
topic-tags: authoring
products: SG_EXPERIENCEMANAGER/CORCOMPONENTS-new
discoiquuid: cb1a745a-30c4-4ad6-a04f-fefb366cd95
translation-type: tm+mt
source-git-commit: 1243d6cc1b0b015ee2f37ae89d0e2e42d366cc02

---


# 페이지 구성 요소{#page-component}

페이지 구성 요소는 [템플릿 편집기와](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) 함께 작동하도록 설계된 확장 가능한 페이지 구성 요소로서, 템플릿 편집기로 페이지 머리글/바닥글 및 구조 구성 요소를 조합할 수 있도록 합니다.

## 사용량 {#usage}

페이지 구성 요소는 핵심 구성 요소뿐만 아니라 편집 가능한 템플릿으로 디자인된 모든 페이지의 기반을 형성합니다. 페이지 구성 요소, 머리글, 바닥글 및 페이지 구조를 다른 핵심 구성 요소를 사용하여 템플릿으로 정의할 수 있습니다.

페이지에 대한 사용자 정의 클라이언트측 라이브러리를 [디자인 대화](#design-dialog)상자를 사용하여 정의할 수 있습니다. 구성 요소가 페이지 자체이므로 구성 요소에서 직접 액세스할 수 있는 편집 대화 상자가 있는 다른 구성 요소와 달리 페이지 구성 요소의 [편집 대화](#edit-dialog) 상자는 페이지 속성 창입니다.

## 버전 및 호환성 {#version-and-compatibility}

페이지 구성 요소의 현재 버전은 v2이며, 이 버전은 2018년 1월 핵심 구성 요소 릴리스 2.0.0에서 도입되었으며 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소 버전이 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|---|---|---|---|
| [v2](page-v1.md) | 호환 가능 | 호환 가능 | 호환 가능 |
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 핵심 구성 요소 [버전을 참조하십시오](versions.md).

>[!NOTE]
>
>페이지 구성 요소 및 AEM 6.3의 버전 2에 대해 `cq:Page` 수준에서 리디렉션을 활성화하려면 [서비스 팩 2](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp2-release-notes.html) 이상이 필요합니다. 이전 릴리스에서는 이러한 리디렉션을 사용할 수 없었습니다.

## 샘플 구성 요소 출력 {#sample-component-output}

다음은 We.Retail에서 [가져온 샘플입니다](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### 스크린샷 {#screenshot}

![](assets/chlimage_1.png)

### 기술 정보 {#technical-details}

페이지 구성 요소에 대한 최신 기술 문서는 GitHub에서 [찾을 수 있습니다](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/page/v2/page).

핵심 구성 요소 개발에 대한 자세한 내용은 핵심 구성 요소 개발자 [설명서를](developing.md)참조하십시오.

## Edit Dialog {#edit-dialog}

Because the component represents the entire page, settings that would normally be in an edit dialog are found in the Page Properties window.[](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-page-properties.html)

## 디자인 대화 상자 {#design-dialog}

구성 요소는 전체 페이지를 나타내므로 페이지 템플릿을 편집할 때 페이지 정보 **-&gt; 페이지** 정책을 통해 디자인 대화 상자에 액세스합니다.

![](assets/screen_shot_2018-04-03at113410.png)

>[!NOTE]
>
>이전 버전의 AEM에서는 페이지 **정책을** 페이지 **디자인이라고 했습니다**.

### 속성 탭 {#properties-tab}

Using the Page Design window, you can define the client libraries to be loaded as well as the web resources library for the page.

* **Client Libraries
This defines the client library categories to load.** JavaScript is added at the body end and the CSS is added to the page head.
* **Client Libraries JavaScript Page Head
This defines the JavaScript Client library categories to load in the page head.**
   * Categories defined here that are also present in the Client Libraries field will have JavaScript loaded in the page head instead of at body end.****
   * No CSS will be loaded unless the category is also present in the Client Libraries field.****

* **웹 리소스 클라이언트 라이브러리**&#x200B;파비아이콘과 같은 웹 리소스를 제공하는 데 사용되는 클라이언트 라이브러리 범주입니다.

![](assets/screenshot_2018-10-19at104949.png)

Libraries can be configured for both the Client Libraries and Client Libraries JavaScript Page Head fields as follows:********

* To add a new field click or tap the Add button below the fields.****
* To remove a field click or tap the trash can icon next to the field to be removed.
* To rearrange the load order, click or tap and drag the handle next to the field to be moved.

For more information about using client-side libraries see Using Client Side Libraries.[](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/clientlibs.html)

>[!CAUTION]
>
>페이지 헤드에 대한 클라이언트 라이브러리를 별도로 정의하는 기능은 핵심 구성 요소 릴리스 2.2.0과 함께 도입되었습니다.

### 스타일 탭 {#styles-tab}

페이지 구성 요소는 AEM 스타일 [시스템을 지원합니다](authoring.md#component-styling).
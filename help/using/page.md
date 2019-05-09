---
title: 페이지 구성 요소
seo-title: 페이지 구성 요소
description: 페이지 구성 요소는 템플릿 편집기를 사용하여 작업하도록 설계된 확장 가능한 페이지 구성 요소로서 페이지 머리글/바닥글 및 구조 구성 요소를 템플릿 편집기로 조합할 수 있습니다.
seo-description: 페이지 구성 요소는 템플릿 편집기를 사용하여 작업하도록 설계된 확장 가능한 페이지 구성 요소로서 페이지 머리글/바닥글 및 구조 구성 요소를 템플릿 편집기로 조합할 수 있습니다.
uuid: 7052 A 5 B 1-E 7 F 1-4944-A 55 C-FAF 739 B 6 E 89 C
contentOwner: 사용자
content-type: 참조
topic-tags: 저작
products: sg_ Experiencemanager/Corecomponents-new
discoiquuid: cb 1 a 745 a -30 c 4-4 ad 6-a 04 f-fefb 3666 cd 95
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# 페이지 구성 요소{#page-component}

페이지 구성 요소는 [템플릿 편집기에서](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) 작동하도록 디자인된 확장 가능한 페이지 구성 요소로서 페이지 머리글/바닥글 및 구조 구성 요소를 템플릿 편집기로 조합할 수 있습니다.

## 사용량 {#usage}

페이지 구성 요소는 편집 가능한 템플릿뿐만 아니라 핵심 구성 요소로 디자인된 모든 페이지의 기초가 됩니다. 페이지 구성 요소, 머리글, 바닥글 및 페이지 구조를 다른 핵심 구성 요소를 사용하여 템플릿으로 정의할 수 있습니다.

[디자인 대화 상자를](#design-dialog)사용하여 페이지에 대해 사용자 정의 클라이언트측 라이브러리를 정의할 수 있습니다. 구성 요소에서 바로 액세스 가능한 편집 대화 상자가 있는 다른 구성 요소와 달리, 구성 요소는 페이지 자체이므로 페이지 구성 요소의 [편집 대화 상자는](#edit-dialog) 페이지 속성 창입니다.

## 버전 및 호환성 {#version-and-compatibility}

페이지 구성 요소의 현재 버전은 2018 년 1 월에 핵심 구성 요소의 릴리스 2.0.0에 도입된 v 2 이며, 이 문서에서는 설명합니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서에 대한 링크를 제공합니다.

| 구성 요소 버전 | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|---|---|---|---|
| [v2](page-v1.md) | 호환 가능 | 호환 가능 | 호환 가능 |
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 문서 [코어 구성 요소 버전을 참조하십시오](versions.md).

>[!NOTE]
>
>페이지 구성 요소 및 `cq:Page` AEM 6.3의 Verison 2에 대한 리디렉션을 활성화하려면 [서비스 팩 2](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp2-release-notes.html) 이상이 필요합니다. 이전 릴리스에서는 이러한 리디렉션을 사용할 수 없었습니다.

## 샘플 구성 요소 출력 {#sample-component-output}

[다음은 We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html)에서 가져온 샘플입니다.

### 스크린샷 {#screenshot}

![](assets/chlimage_1.png)

### 기술 세부 정보 {#technical-details}

페이지 구성 요소에 [대한 최신 기술 설명서는 Github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/page/v2/page)에서 찾을 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서를](developing.md)참조하십시오.

## 편집 대화 상자 {#edit-dialog}

구성 요소는 전체 페이지를 나타내므로 일반적으로 편집 대화 상자에 있는 설정은 [페이지 속성](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-page-properties.html) 창에 있습니다.

## 디자인 대화 상자 {#design-dialog}

구성 요소는 전체 페이지를 나타내므로 페이지 템플릿을 편집할 때 페이지 정보 **-&gt; 페이지 정책을** 통해 디자인 대화 상자에 액세스됩니다.

![](assets/screen_shot_2018-04-03at113410.png)

>[!NOTE]
>
>In previous versions of AEM, **Page Policy** was called **Page Design**.

### 속성 탭 {#properties-tab}

페이지 디자인 창을 사용하여 로드할 클라이언트 라이브러리 및 페이지에 대한 웹 리소스 라이브러리를 정의할 수 있습니다.

* **클라이언트 라이브러리**
클라이언트 라이브러리 카테고리를 로드할 정의입니다. JavaScript가 body 끝에 추가되고 CSS가 페이지 헤드에 추가됩니다.
* **클라이언트 라이브러리 JavaScript 페이지 헤드**
페이지 헤드에서 로드할 JavaScript 클라이언트 라이브러리 카테고리를 정의합니다.
   * 여기에서 정의된 카테고리도 **클라이언트 라이브러리** 필드에 body 종료 대신 페이지 헤드에 로드됩니다.
   * 카테고리가 **클라이언트 라이브러리** 필드에도 없으면 CSS가 로드되지 않습니다.

* **웹 리소스 클라이언트 라이브러리파비콘과 같은**
웹 리소스를 제공하는 데 사용되는 클라이언트 라이브러리 범주입니다.

![](assets/screenshot_2018-10-19at104949.png)

라이브러리는 **클라이언트 라이브러리와** **클라이언트 라이브러리 JavaScript 페이지 헤드** 필드 모두에 다음과 같이 구성할 수 있습니다.

* 새 필드를 추가하려면 필드 아래에 있는 **추가** 단추를 클릭하거나 탭합니다.
* 필드를 제거하려면 제거할 필드 옆에 있는 휴지통 아이콘을 클릭하거나 탭합니다.
* 로드 순서를 재배치하려면 이동할 필드 옆에 있는 핸들을 클릭하거나 탭한 다음 드래그합니다.

클라이언트측 라이브러리 사용에 대한 자세한 내용은 클라이언트측 라이브러리 [사용을](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/clientlibs.html)참조하십시오.

>[!CAUTION]
>
>페이지 헤드에 대한 클라이언트 라이브러리를 별도로 정의하는 기능은 핵심 구성 요소 릴리스 2.2.0에서 도입되었습니다.

### 스타일 탭 {#styles-tab}

페이지 구성 요소는 AEM [스타일 시스템을 지원합니다](authoring.md#component-styling).
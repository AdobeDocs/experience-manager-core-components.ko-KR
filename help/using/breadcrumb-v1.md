---
title: 브레드크럼 구성 요소 (v 1)
seo-title: 브레드크럼 구성 요소 (v 1)
description: 핵심 구성 요소 탐색 표시 구성 요소는 컨텐츠 계층 구조에서 페이지 위치를 기반으로 링크의 탐색 표시를 빌드하는 탐색 구성 요소입니다.
seo-description: AEM 핵심 구성 요소 탐색 표시 구성 요소는 컨텐츠 계층 구조에서 페이지 위치를 기반으로 링크의 탐색 표시를 빌드하는 탐색 구성 요소입니다.
uuid: C 1 F 20 A 82-B 6 FF -4 A 3 C -920 A -6710084 A 69 F 2
content-type: 참조
topic-tags: 핵심 구성 요소
discoiquuid: 0 b 3 a 7 d 8 f-d 110-424 f-b 531-ff 88 c 9 a 09128
disttype: dist5
gnavtheme: 밝음
groupsectionnavitems: 아니오
hidemerchandisingbar: 상속
hidepromocomponent: 상속
index: n
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# 브레드크럼 구성 요소 (v 1){#breadcrumb-component-v}

핵심 구성 요소 탐색 표시 구성 요소는 컨텐츠 계층 구조에서 페이지 위치를 기반으로 링크의 탐색 표시를 빌드하는 탐색 구성 요소입니다.

## 사용량 {#usage}

탐색 표시 구성 요소는 사이트 계층 구조 내에서 현재 페이지의 위치를 표시하므로 페이지 방문자가 현재 위치에서 페이지 계층을 탐색할 수 있습니다. 페이지 머리글이나 바닥글에 통합되는 경우가 많습니다.

기본 탐색 수준 및 현재 페이지 표시 기능 또는 숨겨진 페이지를 표시하는 기능은 [디자인 대화 상자의 템플릿 작성자가 정의할 수](breadcrumb-v1.md#main-pars_title_1995166862)있습니다. 그런 다음 컨텐츠 편집기에서는 숨겨진 페이지를 표시할지 여부를 선택할 수 있으며 [편집 대화 상자에서 구성 요소에 대한 실제 탐색 수준을 선택할](breadcrumb-v1.md#main-pars_title)수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

This document describes v 1 of the breadcrumb component, original introduce with the release 1.0.0 with the core components with AEM 6.3.

다음 표에는 탐색 표시 구성 요소의 v 1 호환성이 나와 있습니다.

| AEM 버전 | 탐색 표시 구성 요소 v 1 |
|--- |--- |
| 6.3 | 호환 가능 |
| 6.4 | 호환 가능 |

>[!CAUTION]
>
>이 문서에서는 탐색 표시 구성 요소의 v 1에 대해 설명합니다.
>탐색 표시 구성 요소의 현재 버전에 대한 자세한 내용은 [탐색 표시 구성 요소](breadcrumb.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

[다음은 We. Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html)에서 가져온 샘플입니다.

### 스크린샷 {#screenshot}

![](assets/chlimage_1-33.png)

### HTML {#html}

```
<div class="cmp cmp-breadcrumb aem-GridColumn aem-GridColumn--default--12">

<ol class="breadcrumb">
    <li class="breadcrumb-item ">
        <a href="/content/we-retail/us.html">
            United States
        </a>
    </li>

    <li class="breadcrumb-item ">
        <a href="/content/we-retail/us/en.html">
            English
        </a>
    </li>

    <li class="breadcrumb-item active">
        
            Experience
        
    </li>
</ol>
 
</div>
```

### JSON {#json}

```
"breadcrumb": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              ":type": "weretail/components/content/breadcrumb"
            }
```

>[!NOTE]
>
>핵심 구성 요소에서 JSON 내보내기를 사용하려면 핵심 구성 요소의 릴리스 1.1.0 이 필요합니다. 자세한 내용은 [핵심 구성 요소 v 1](versions.md#main-pars_title_236368006) 의 호환성 정보를 참조하십시오.

## 편집 대화 상자 {#edit-dialog}

컨텐츠 작성자는 편집 대화 상자를 사용하여 탐색 표시 시 숨겨진 페이지와 활성 페이지를 표시하지 않을 수 있습니다.

![](assets/chlimage_1-34.png)

* **탐색 수준 시작** - 계층에서 탐색 표시 구성 요소가 현재 페이지로 이동하기 시작해야 합니다. 예를 들어 We. Retail에서 다음을 수행합니다.

   * 1 시작 날짜: `/content/we-retail`
   * 2 시작 위치: `/content/we-retail/<country>`

* **숨김 표시** - 탐색 표시에 숨김으로 표시된 페이지를 표시합니다 (기본적으로 표시되지 않음).
* **현재**페이지 숨기기 - 탐색 표시를 통해 현재 페이지를 숨깁니다 (기본적으로 표시).

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 [디자인] 대화 상자를 사용하여 탐색 표시 시 숨겨진 페이지와 활성 페이지를 표시하지 않고 표시해야 하는 계층 구조의 깊이를 지정할 수 있습니다.

![](assets/chlimage_1-35.png)

* **탐색 수준 시작** - 탐색 Breadcrumb 구성 요소가 페이지에 추가될 때 탐색 표시 구성 요소가 현재 페이지로 시작하는 데 필요한 기본 값을 정의합니다.
* **숨김 표시** - 탐색 표시 구성 요소가 페이지에 추가되면 숨김 **표시** 옵션의 기본값을 정의합니다.

   * 작성자에 대한 옵션은 활성화 또는 비활성화되지 않습니다. 기본값을 설정합니다.

* **현재 숨기기** - 탐색 표시 구성 요소가 페이지에 추가되면 현재 **숨기기** 옵션의 기본값을 정의합니다.

   * 작성자에 대한 옵션은 활성화 또는 비활성화되지 않습니다. 기본값을 설정합니다.

## 기술 세부 정보 {#technical-details}

탐색 표시 구성 요소에 [대한 최신 기술 설명서는 Github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v1/breadcrumb)에서 찾을 수 있습니다.

Github에서 전체 핵심 구성 요소 프로젝트를 다운로드할 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서를](developing.md)참조하십시오.

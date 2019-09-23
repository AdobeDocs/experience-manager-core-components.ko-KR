---
title: 탐색 표시 구성 요소(v1)
seo-title: 탐색 표시 구성 요소(v1)
description: 핵심 구성 요소 탐색 표시 구성 요소는 컨텐츠 계층 구조에서 페이지의 위치를 기반으로 링크의 탐색 표시를 작성하는 탐색 구성 요소입니다.
seo-description: AEM 코어 구성 요소 탐색 표시 구성 요소는 컨텐츠 계층 구조에서 페이지의 위치를 기반으로 링크의 탐색 표시를 작성하는 탐색 구성 요소입니다.
uuid: c1f20a82-b6ff-4a3c-920a-6710084a69f2
content-type: 참조
topic-tags: 핵심 구성 요소
discoiquuid: 0b3a7d8f-d110-424f-b531-ff88c9a09128
disttype: dist5
gnavtheme: 밝음
groupsectionnavitems: 아니오
hidemerchandisingbar: 상속
hidepromocomponent: 상속
index: n
translation-type: tm+mt
source-git-commit: 4e74f10e2a4119484a597178dc4577b399833dbf

---


# 탐색 표시 구성 요소(v1){#breadcrumb-component-v}

핵심 구성 요소 탐색 표시 구성 요소는 컨텐츠 계층 구조에서 페이지의 위치를 기반으로 링크의 탐색 표시를 작성하는 탐색 구성 요소입니다.

## 사용량 {#usage}

탐색 표시 구성 요소는 사이트 계층 내에서 현재 페이지의 위치를 표시하여 페이지 방문자가 현재 위치에서 페이지 계층을 탐색할 수 있도록 합니다. 페이지 머리글이나 바닥글에 종종 통합되어 있습니다.

기본 탐색 수준 및 현재 페이지 또는 숨겨진 페이지를 표시하는 기능과 같은 사용 가능한 옵션은 [디자인 대화](breadcrumb-v1.md#main-pars_title_1995166862)상자에서 템플릿 작성자가 정의할 수 있습니다. 그런 다음 컨텐츠 편집기에서 숨겨진 페이지를 표시할지 여부를 선택하고 [편집 대화](breadcrumb-v1.md#main-pars_title)상자에서 구성 요소의 실제 탐색 수준을 선택할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

이 문서에서는 AEM 6.3의 핵심 구성 요소 릴리스 1.0.0에서 처음 소개된 탐색 표시 구성 요소의 v1에 대해 설명합니다.

다음 표는 탐색 표시 구성 요소의 v1 호환성을 보여줍니다.

| AEM 버전 | 탐색 표시 구성 요소 v1 |
|--- |--- |
| 6.3 | 호환 가능 |
| 6.4 | 호환 가능 |

>[!CAUTION]
>
>이 문서에서는 탐색 표시 구성 요소의 v1에 대해 설명합니다.
>탐색 표시 구성 요소의 현재 버전에 대한 자세한 내용은 탐색 표시 구성 [요소 문서를](breadcrumb.md) 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

다음은 We.Retail에서 [가져온 샘플입니다](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

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
>핵심 구성 요소에서 JSON을 내보내려면 핵심 구성 요소 릴리스 1.1.0이 필요합니다. 자세한 내용은 핵심 구성 요소 v1의 [](versions.md#main-pars_title_236368006) 호환성 정보를 참조하십시오.

## Edit Dialog {#edit-dialog}

편집 대화 상자를 사용하면 컨텐츠 작성자가 표시해야 하는 계층 구조의 깊이뿐만 아니라 탐색 표시의 숨김 및 활성 페이지를 표시하지 않을 수 있습니다.

![](assets/chlimage_1-34.png)

* **시작할** 탐색 수준 - 계층에서 탐색 표시 구성 요소가 현재 페이지로 이동하기 시작해야 하는 위치입니다. 예: We.Retail:

   * 1부터 시작 `/content/we-retail`
   * 2부터 시작 `/content/we-retail/<country>`

* **숨김** 표시 - 탐색 경로에서 숨김으로 표시된 페이지를 표시합니다(기본적으로 표시되지 않음).
* **현재**&#x200B;숨기기 - 탐색 경로에서 현재 페이지를 표시합니다(기본적으로 표시됨).

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 [디자인] 대화 상자를 사용하여 표시되는 계층 구조의 깊이뿐만 아니라 숨겨진 페이지와 활성 페이지를 표시하지 않는 옵션의 기본값을 정의할 수 있습니다.

![](assets/chlimage_1-35.png)

* **탐색 수준 시작** - 탐색 표시 구성 요소가 페이지에 추가될 때 계층 구조에서 탐색 표시 구성 요소가 현재 페이지로 이동하기 시작해야 하는 위치에 대한 기본값을 정의합니다.
* **숨김 표시** - 탐색 표시 구성 **요소가 페이지에 추가될 때** 숨겨진 표시 옵션의 기본값을 정의합니다.

   * 작성자에 대한 옵션을 활성화하거나 비활성화하지 않습니다. 기본값은 설정만 설정합니다.

* **현재** 숨기기 - 탐색 표시 구성 **요소가 페이지에 추가될** 때 현재 숨기기 옵션의 기본값을 정의합니다.

   * 작성자에 대한 옵션을 활성화하거나 비활성화하지 않습니다. 기본값은 설정만 설정합니다.

## 기술 정보 {#technical-details}

탐색 표시 구성 요소에 대한 최신 기술 문서는 GitHub에서 [찾을 수 있습니다](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v1/breadcrumb).

전체 핵심 구성 요소 프로젝트는 GitHub에서 다운로드할 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 핵심 구성 요소 개발자 [설명서를](developing.md)참조하십시오.

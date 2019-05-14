---
title: 탐색 표시 구성 요소
seo-title: 탐색 표시 구성 요소
description: 'null'
seo-description: 핵심 구성 요소 탐색 표시 구성 요소는 컨텐츠 계층 구조에서 페이지 위치를 기반으로 링크의 탐색 표시를 빌드하는 탐색 구성 요소입니다.
uuid: 13 e 858 d 5-24 ad -4144-adc 4-0 fa 1 ffd 257 c 1
contentOwner: 사용자
content-type: 참조
topic-tags: 저작
products: sg_ Experiencemanager/Corecomponents-new
discoiquuid: ECD 237 DF -08 B 8-4 DEB -9881-66 A 1 F 0 D 65 EF 3
modalsize: 426x240
translation-type: tm+mt
source-git-commit: 1243d6cc1b0b015ee2f37ae89d0e2e42d366cc02

---


# 탐색 표시 구성 요소{#breadcrumb-component}

핵심 구성 요소 탐색 표시 구성 요소는 컨텐츠 계층 구조에서 페이지 위치를 기반으로 링크의 탐색 표시를 빌드하는 탐색 구성 요소입니다.

## 사용량 {#usage}

탐색 표시 구성 요소는 사이트 계층 구조 내에서 현재 페이지의 위치를 표시하므로 페이지 방문자가 현재 위치에서 페이지 계층을 탐색할 수 있습니다. 페이지 머리글이나 바닥글에 통합되는 경우가 많습니다.

기본 탐색 수준, 현재 페이지 또는 숨겨진 페이지를 표시하는 기능 등 사용 가능한 옵션은 [디자인 대화 상자의 템플릿 작성자가 정의할](#design-dialog)수 있습니다. 그런 다음 컨텐츠 편집기에서는 숨겨진 페이지를 표시할지 여부를 선택할 수 있으며 [편집 대화 상자에서 구성 요소에 대한 실제 탐색 수준을 선택할](#edit-dialog)수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

Breadcrumb 구성 요소의 현재 버전은 2018 년 1 월에 핵심 구성 요소의 릴리스 2.0.0에 도입된 v 2 이며, 이 문서에서는 설명합니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서에 대한 링크를 제공합니다.

| 구성 요소 버전 | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | 호환 가능 | 호환 가능 | 호환 가능 |
| [v1](breadcrumb-v1.md) | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 문서 [코어 구성 요소 버전을 참조하십시오](versions.md).

## 샘플 구성 요소 출력 {#sample-component-output}

[다음은 We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html)에서 가져온 샘플입니다.

### 스크린샷 {#screenshot}

![](assets/chlimage_1.png)

### HTML {#html}

```
<nav class="cmp-breadcrumb">
    <ol class="cmp-breadcrumb__list">
        <li class="cmp-breadcrumb__item">
            <a href="/content/we-retail/us.html" class="cmp-breadcrumb__item-link">
                United States
            </a>
        </li>
    
        <li class="cmp-breadcrumb__item">
            <a href="/content/we-retail/us/en.html" class="cmp-breadcrumb__item-link">
                English
            </a>
        </li>
    
        <li class="cmp-breadcrumb__item cmp-breadcrumb__item--active">
            
                Experience
            
        </li>
    </ol>
</nav>
```

### JSON {#json}

```
"breadcrumb":{  
                     "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                     "items":[  
                        {  
                           "page":{  
                              "path":"/content/we-retail/us",
                              "pageTitle":null,
                              "name":"us",
                              "description":null,
                              "title":"United States"
                           },
                           "active":false
                        },
                        {  
                           "page":{  
                              "path":"/content/we-retail/us/en",
                              "pageTitle":null,
                              "name":"en",
                              "description":null,
                              "title":"English"
                           },
                           "active":false
                        },
                        {  
                           "page":{  
                              "path":"/content/we-retail/us/en/experience",
                              "pageTitle":null,
                              "name":"experience",
                              "description":null,
                              "title":"Experience"
                           },
                           "active":true
                        }
                     ],
                     ":type":"weretail/components/content/breadcrumb"
                  }
```

>[!NOTE]
>
>코어 구성 요소 릴리스 2.1.0 부터는 탐색 표시 구성 요소가 [schema.org 마이크로 데이터를 지원합니다](https://schema.org/BreadcrumbList).

### 기술 세부 정보 {#technical-details}

탐색 표시 구성 요소에 [대한 최신 기술 설명서는 Github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb)에서 찾을 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서를](developing.md)참조하십시오.

## 편집 대화 상자 {#edit-dialog}

컨텐츠 작성자는 편집 대화 상자를 사용하여 탐색 표시 시 숨겨진 페이지와 활성 페이지를 표시하지 않을 수 있습니다.

![](assets/screen_shot_2018-01-12at124250.png)

* **탐색 시작 수준** - 계층에서 탐색 표시 구성 요소가 현재 페이지로 이동하기 시작해야 합니다. 예를 들어 We. Retail에서 다음을 수행합니다.

   * 0는 (는) `/content`

   * 1 시작 날짜: `/content/we-retail`
   * 2 시작 위치: `/content/we-retail/<country>`

* **숨겨진 탐색 항목 표시** - 탐색 표시에 숨김으로 표시된 페이지 표시 (기본적으로 표시되지 않음)
* **현재 페이지 숨기기**- 탐색 표시를 통해 현재 페이지를 표시하지 않습니다 (기본적으로 표시).

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 [디자인] 대화 상자를 사용하여 탐색 표시 시 숨겨진 페이지와 활성 페이지를 표시하지 않고 표시해야 하는 계층 구조의 깊이를 지정할 수 있습니다.

### 기본 탭 {#main-tab}

![](assets/screen_shot_2018-01-12at124437.png)

* **탐색 시작 수준** - 탐색 표시 구성 요소가 페이지에 추가될 때 탐색 표시 구성 요소가 현재 페이지로 이동하는 데 필요한 기본 값을 정의합니다.
* **숨겨진 탐색 항목 표시** - 탐색 표시 구성 요소가 페이지에 추가되면 숨겨진 탐색 항목 **표시** 옵션의 기본값을 정의합니다.

   * 작성자에 대한 옵션은 활성화 또는 비활성화되지 않습니다. 기본값을 설정합니다.

* **현재 페이지 숨기기**- 탐색 표시 구성 요소가 페이지에 추가되면 현재 페이지 **숨기기** 옵션의 기본값을 정의합니다.

   * 작성자에 대한 옵션은 활성화 또는 비활성화되지 않습니다. 기본값을 설정합니다.

### 스타일 탭 {#styles-tab}

브레드크럼 구성 요소는 AEM [스타일 시스템을 지원합니다](authoring.md#component-styling).
---
title: 빠른 검색 구성 요소
seo-title: 빠른 검색 구성 요소
description: 'null'
seo-description: 빠른 검색 구성 요소는 방문자가 사이트를 검색하고 결과를 필터링할 수 있도록 웹 사이트에 검색 기능을 제공하고 검색 결과를 제공합니다.
uuid: 1ba69be3-537e-4f20-9f17-b4b7174a8e88
content-type: 참조
topic-tags: authoring
products: SG_EXPERIENCEMANAGER/CORCOMPONENTS-new
discoiquuid: 906a684d-5663-4497-bef3-37f13d5b46c7
disttype: dist5
gnavtheme: 밝음
groupsectionnavitems: 아니오
hidemerchandisingbar: 상속
hidepromocomponent: 상속
modalsize: 426x240
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 1243d6cc1b0b015ee2f37ae89d0e2e42d366cc02

---


# 빠른 검색 구성 요소{#quick-search-component}

빠른 검색 구성 요소는 방문자가 일치하는 컨텐츠를 쉽게 찾고 결과를 볼 수 있도록 웹 사이트에 검색 기능을 제공하고 검색 결과를 제공합니다.

## 사용량 {#usage}

빠른 검색 구성 요소는 사이트 방문자에게 컨텐츠를 검색하고, 결과를 적소에 보고, 일치하는 페이지로 쉽게 이동할 수 있는 기능을 제공합니다. 사용자가 검색 결과를 스크롤할 때 새로운 결과가 동적으로 가져옵니다.

컨텐츠 작성자는 [편집 대화](#edit-dialog) 상자를 사용하여 컨텐츠 트리에서 검색이 시작되는 위치를 정의할 수 있습니다. 템플릿 작성자는 [디자인 대화](#design-dialog)상자를 사용하여 컨텐츠 트리에서 검색이 시작되어야 하는 위치에 대한 기본값, 최대 결과 집합 크기 및 최소 검색 용어 길이를 설정할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

빠른 검색 구성 요소의 현재 버전은 v1이며, 이 버전은 2018년 1월 핵심 구성 요소 릴리스 2.0.0과 함께 도입되었으며 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소 버전이 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 핵심 구성 요소 [버전을 참조하십시오](versions.md).

## 샘플 구성 요소 출력 {#sample-component-output}

다음은 We.Retail에서 [가져온 샘플입니다](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### 스크린샷 {#screenshot}

![](assets/screen_shot_2018-01-19at094248.png)

### HTML {#html}

```
<section class="cmp-search" role="search" data-cmp-is="search" data-cmp-min-length="3" data-cmp-results-size="10">
    <form class="cmp-search__form" data-cmp-hook-search="form" method="get" action="/content/we-retail/us/en/equipment.searchresults.json/_jcr_content/root/responsivegrid/search" autocomplete="off">
        <div class="cmp-search__field">
            <i class="cmp-search__icon" data-cmp-hook-search="icon"></i>
            <span class="cmp-search__loading-indicator" data-cmp-hook-search="loadingIndicator"></span>
            <input class="cmp-search__input" data-cmp-hook-search="input" type="text" name="fulltext" placeholder="Search" role="combobox" aria-autocomplete="list" aria-haspopup="true" aria-invalid="false">
            <button class="cmp-search__clear" data-cmp-hook-search="clear">
                <i class="cmp-search__clear-icon"></i>
            </button>
        </div>
    </form>
    <div class="cmp-search__results" data-cmp-hook-search="results" role="listbox" aria-multiselectable="false"></div>
    
<script data-cmp-hook-search="itemTemplate" type="x-template">
    <a class="cmp-search__item" data-cmp-hook-search="item">
        <span class="cmp-search__item-title" data-cmp-hook-search="itemTitle"></span>
    </a>
</script>
</section>
```

### JSON {#json}

```
"search":{  
                     "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                     "relativePath":"/jcr:content/root/responsivegrid/search",
                     "resultsSize":10,
                     "searchTermMinimumLength":3,
                     ":type":"core/wcm/components/search/v1/search"
                  }
```

### 기술 정보 {#technical-details}

>[!NOTE]
>
>DOS 공격으로부터 검색 구성 요소 또는 AEM 기반 응용 프로그램을 보호하는 것은 보다 높은 수준에서(예: 디스패처에서 사용) `mod_security` 해야 합니다.

빠른 검색 구성 요소에 대한 최신 기술 문서는 GitHub에서 [찾을 수 있습니다](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/search/v1/search).

핵심 구성 요소 개발에 대한 자세한 내용은 핵심 구성 요소 개발자 [설명서를](developing.md)참조하십시오.

## Edit Dialog {#edit-dialog}

컨텐츠 작성자는 편집 대화 상자를 사용하여 컨텐츠 트리에서 검색이 시작되는 위치를 정의할 수 있습니다.

![](assets/screen_shot_2018-04-03at120132.png)

**검색 루트** - 검색을 시작할 루트 페이지입니다. 검색 루트는 블루프린트 마스터, 언어 마스터 또는 일반 페이지일 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 사용하여 컨텐츠 트리에서 검색이 시작되어야 하는 위치에 대한 기본값을 설정할 수 있고 최대 결과 세트 크기 및 최소 검색 조건 길이를 설정할 수 있습니다. 디자인 대화 상자를 사용하면 템플릿 작성자가 컨텐츠 작성자가 사용할 수 있는 텍스트 서식 지정 옵션을 정의할 수 있습니다.

### 속성 탭 {#properties-tab}

![](assets/screen_shot_2018-04-03at120028.png)

* **검색**&#x200B;루트컨텐츠 작성자가 컨텐츠 페이지에 빠른 검색 구성 요소를 배치할 때의 검색 루트의 기본값
* **결과**&#x200B;크기검색 요청으로 가져오는 최대 결과 수입니다.
* **검색어 최소**&#x200B;길이검색을 시작할 검색어의 최소 길이

>[!NOTE]
>
>**결과 크기** 및 **검색어 최소** 길이는 디자인 모드에서만 설정할 수 있으므로 컨텐츠 작성자가 이러한 값을 수정할 수 없음을 의미합니다.

>[!CAUTION]
>
>**결과 크기** 및 **검색어 최소** 길이는각각 너무 높거나 낮게 설정된 경우 성능에 영향을 줄 수 있습니다.

### 스타일 탭 {#styles-tab}

빠른 검색 구성 요소는 AEM 스타일 시스템을 [지원합니다](authoring.md#component-styling).
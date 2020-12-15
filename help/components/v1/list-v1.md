---
title: 목록 구성 요소(v1)
description: 핵심 구성 요소 목록 구성 요소를 사용하면 정적 목록뿐만 아니라 동적 목록을 쉽게 만들 수 있습니다.
index: n
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a
workflow-type: tm+mt
source-wordcount: '854'
ht-degree: 4%

---


# 목록 구성 요소(v1) {#list-component-v}

핵심 구성 요소 목록 구성 요소를 사용하면 정적 목록뿐만 아니라 동적 목록을 쉽게 만들 수 있습니다.

## 사용량 {#usage}

목록 구성 요소를 사용하여 하위 페이지의 동적 목록 또는 임의 정의된 항목의 정적 목록 등을 만들 수 있습니다.

사용 가능한 목록 및 서식 지정 옵션은 [디자인 대화 상자](#design-dialog)에서 템플릿 작성자가 정의할 수 있습니다. 컨텐트 편집기는 사용 가능한 목록 유형 및 [편집 대화 상자](#edit-dialog)에서 목록 요소의 형식을 지정하는 방법을 선택할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

이 문서에서는 AEM 6.3의 핵심 구성 요소 릴리스 1.0.0에 처음 소개된 목록 구성 요소의 v1에 대해 설명합니다.

다음 표는 목록 구성 요소의 v1 호환성을 보여줍니다.

| AEM 버전 | 목록 구성 요소 v1 |
|--- |--- |
| 6.3 | 호환 가능 |
| 6.4 | 호환 가능 |

>[!CAUTION]
>
>이 문서에서는 목록 구성 요소의 v1에 대해 설명합니다.
>
>목록 구성 요소의 현재 버전에 대한 자세한 내용은 [목록 구성 요소](/help/components/list.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

다음은 [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html)에서 가져온 샘플입니다.

### 스크린샷 {#screenshot}

![](/help/assets/chlimage_1-47.png)

### HTML {#html}

```
<div class="cmp cmp-list aem-GridColumn aem-GridColumn--default--12">

<ul>
    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/arctic-surfing-in-lofoten.html">
            <span class="cmp-list--item-title">Arctic Surfing In Lofoten</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/summit-success-in-the-himalayas.html">
            <span class="cmp-list--item-title">Summit Success in the Himalayas</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/climbing-on-kalymnos-island--greece.html">
            <span class="cmp-list--item-title">Climbing on Kalymnos Island, Greece</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/running-at-the-great-wall-marathon.html">
            <span class="cmp-list--item-title">Running at the Great Wall Marathon</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/skiing-deep-powder-in-siberia.html">
            <span class="cmp-list--item-title">Skiing deep powder in Siberia</span>
            
        </a>
        
    </article>
</li>

    <li>
    <article>
        <a href="/content/we-retail/us/en/experience/climbing-in-the-massif-du-mont-blanc.html">
            <span class="cmp-list--item-title">Climbing in the Massif du Mont Blanc</span>
            
        </a>
        
    </article>
</li>
</ul>

</div>
```

### JSON {#json}

```
"articles_list": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              ":type": "weretail/components/content/articleslist",
              "tagsMatch": "any",
              "displayAs": "teaser",
              "feedEnabled": "true",
              "listFrom": "children",
              "limit": "0",
              "orderBy": "cq:lastModified",
              "pageMax": "0"
            }
```

>[!NOTE]
>
>핵심 구성 요소에서 JSON 내보내기를 사용하려면 핵심 구성 요소의 릴리스 1.1.0이 필요합니다. 자세한 내용은 핵심 구성 요소 v1[에 대한 호환성 정보를 참조하십시오.](/help/versions.md)

## 편집 대화 상자 {#edit-dialog}

편집 대화 상자를 사용하면 컨텐츠 작성자가 목록과 목록 요소를 구성할 수 있습니다.

### 목록 설정 {#list-settings}

목록은 다른 방법으로 작성할 수 있습니다.

* [하위 페이지](#child-pages)
* [고정 목록](#fixed-list)
* [검색](#search-list)
* [태그](#tags)

목록이 작성되는 방식에 관계없이 항상 구성할 수 있는 [정렬 옵션](#sort-options)이 있습니다.

![](/help/assets/chlimage_1-38.png)

컨텐츠 작성자가 목록 작성을 선택하는 방법에 따라 추가 구성 옵션이 변경됩니다.

#### 하위 페이지 {#child-pages}

목록은 현재 페이지 또는 다른 페이지의 하위 페이지로 작성할 수 있습니다.

![](/help/assets/chlimage_1-39.png)

* **상위 페이지**
   * 하위 페이지가 목록에 포함되어야 하는 페이지
   * 현재 페이지를 사용하려면 비워 둡니다.
* **하위 깊이**  - 계층 구조에서 하위 수준 몇 개를 사용해야 합니까?

#### 고정 목록 {#fixed-list}

고정된 항목 목록을 사용하여 목록을 작성할 수 있습니다.

![](/help/assets/chlimage_1-40.png)

목록에 새 항목을 삽입하려면 **추가** 단추를 탭하거나 클릭합니다.

* 목록에 있는 항목의 텍스트를 입력하거나 **선택 대화 상자**&#x200B;를 사용하여 AEM에서 항목을 선택합니다.
* 드래그 핸들을 사용하여 목록의 항목을 다시 정렬합니다.
* 목록에서 항목을 삭제하려면 휴지통 아이콘을 사용합니다.

#### 검색 {#search-list}

AEM 컨텐츠 검색 결과를 사용하여 목록을 작성할 수 있습니다.

![](/help/assets/chlimage_1-41.png)

* **검색 쿼리**  - 목록 요소를 생성하기 위해 전체 텍스트 검색을 실행할 문자열입니다.
* **검색 위치**  - 검색을 실행해야 하는 위치
   * **선택 대화 상자**&#x200B;를 사용하여 AEM에서 위치를 선택합니다.
   * 현재 페이지를 비워 둘 경우 사용

#### 태그 {#tags}

특정 위치 아래의 특정 태그와 일치하는 페이지를 사용하여 목록을 작성할 수 있습니다.

![](/help/assets/chlimage_1-42.png)

* **상위 페이지**  - 태그 일치를 시작해야 하는 위치
   * **선택 대화 상자**&#x200B;를 사용하여 AEM에서 위치를 선택합니다.
   * 현재 페이지를 비워 둘 경우 사용
* **태그**  - 일치해야 하는 태그
   * **찾아보기** 대화 상자를 사용하여 태그를 선택합니다
* **일치**  - 목록에 포함할 페이지에 맞는 일치 유형을 정의합니다.
   * **임의의 태그**
   * **모든 태그**

#### 정렬 옵션 {#sort-options}

목록 작성 방법에 관계없이 항상 정의할 수 있는 특정 정렬 옵션이 있습니다.

![](/help/assets/chlimage_1-43.png)

* **정렬 기준**  - 요소를 정렬하는 방법
   * **제목**
   * **마지막으로 수정한 날짜**
* **정렬 순서**  - 항목을 주문해야 하는 순서
   * **오름차순**
   * **내림차순**
* **최대 항목**  수 - 목록에 표시되는 최대 항목 수입니다.
   * 모든 항목을 반환하려면 비워 둡니다.

### 항목 설정 {#item-settings}

**항목 설정** 탭을 사용하여 목록 요소의 형식을 구성할 수 있습니다.

![](/help/assets/chlimage_1-44.png)

* **항목**
연결항목을 해당 페이지에 연결
* **설명**
표시링크 항목의 설명 표시
* **날짜**
표시링크 항목의 수정 날짜 표시

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 통해 사용 가능한 항목 설정과 컨텐츠 작성자에게 허용해야 하는 목록 유형을 정의할 수 있습니다.

### 목록 설정 {#list-settings-1}

**목록 설정** 탭에서 날짜 형식을 정의할 수 있을 뿐만 아니라 컨텐츠 작성자가 구성 요소에서 사용할 수 있는 목록 유형을 정의할 수 있습니다.

![](/help/assets/chlimage_1-45.png)

* **날짜 형식**  - 마지막 수정 날짜 표시에 사용할 형식
* **하위**  항목 비활성화 - 구성 요소의 하위 목록 유형을 비활성화합니다.
* **정적**  비활성화 - 구성 요소에서 정적 목록 유형을 비활성화합니다.
* **검색**  비활성화 - 구성 요소에서 검색 목록 유형을 비활성화합니다.
* **태그**  비활성화 - 구성 요소에서 태그 목록 유형 비활성화

### 항목 설정 {#item-settings-1}

**항목 설정** 탭에서 컨텐츠 작성자에 대한 구성 요소에서 사용할 수 있어야 하는 개별 목록 요소의 서식 옵션을 정의할 수 있습니다.

![](/help/assets/chlimage_1-46.png)

* **링크 항목**  -  [편집 대화 상자에서 링크 항목 활성화 옵션](#edit-dialog)
* **설명 표시**  -  [편집 대화 상자에서 설명 표시 옵션 사용](#edit-dialog)
* **날짜 표시**  - 편집 대화 상자에서 날짜 표시  [옵션 사용](#edit-dialog)

## 기술 세부 정보 {#technical-details}

목록 구성 요소 [에 대한 최신 기술 문서는 GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/list/v1/list)에서 찾을 수 있습니다.

전체 핵심 구성 요소 프로젝트를 GitHub에서 다운로드할 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)에서 확인할 수 있습니다.

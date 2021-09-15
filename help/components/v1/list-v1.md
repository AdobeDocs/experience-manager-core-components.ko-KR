---
title: 목록 구성 요소 (v1)
description: 핵심 구성 요소의 목록 구성 요소를 사용하여 동적 목록과 정적 목록을 간단히 만들 수 있습니다.
index: n
role: Architect, Developer, Admin, User
exl-id: 510d059c-e60a-40aa-9032-66a901109f6e
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: ht
source-wordcount: '854'
ht-degree: 100%

---

# 목록 구성 요소 (v1) {#list-component-v}

핵심 구성 요소의 목록 구성 요소를 사용하여 동적 목록과 정적 목록을 간단히 만들 수 있습니다.

## 사용량 {#usage}

목록 구성 요소를 사용하여 하위 페이지에 대한 동적 목록 또는 임의로 정의된 항목에 대한 정적 목록을 만들 수 있습니다.

템플릿 작성자는 [디자인 대화 상자](#design-dialog)에서 사용 가능한 목록 유형 및 서식 지정 옵션을 정의할 수 있습니다. 콘텐츠 편집기는 [편집 대화 상자](#edit-dialog)에서 사용 가능한 목록 유형 및 목록 요소 서식 지정 방법을 선택할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

이 문서에서는 AEM 6.3을 포함하는 핵심 구성 요소 릴리스 1.0.0과 함께 최초 도입된 목록 구성 요소 v1에 대해 설명합니다.

다음 표에서 목록 구성 요소 v1의 호환성을 확인할 수 있습니다.

| AEM 버전 | 목록 구성 요소 v1 |
|--- |--- |
| 6.3 | 호환 가능 |
| 6.4 | 호환 가능 |

>[!CAUTION]
>
>이 문서에서는 목록 구성 요소 v1에 대해 설명합니다.
>
>현재 버전의 목록 구성 요소에 대한 자세한 내용은 [목록 구성 요소](/help/components/list.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

다음은 [We.Retail](https://helpx.adobe.com/kr/experience-manager/6-4/sites/developing/using/we-retail.html)에서 얻은 샘플입니다.

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
>핵심 구성 요소에서 JSON을 내보내는 데 핵심 구성 요소 릴리스 1.1.0이 필요합니다. 자세한 내용은 [핵심 구성 요소 v1에 대한 호환성 정보](/help/versions.md)를 참조하십시오.

## 편집 대화 상자 {#edit-dialog}

콘텐츠 작성자는 편집 대화 상자를 통해 목록 및 목록 요소를 구성할 수 있습니다.

### 목록 설정 {#list-settings}

다른 방식으로 목록을 빌드할 수 있습니다.

* [하위 페이지](#child-pages)
* [고정 목록](#fixed-list)
* [검색](#search-list)
* [태그](#tags)

목록의 빌드 방법에 관계없이 언제든지 구성할 수 있는 [정렬 옵션](#sort-options)이 있습니다.

![](/help/assets/chlimage_1-38.png)

콘텐츠 작성자의 목록 빌드 선택에 따라 추가 구성 옵션이 변경됩니다.

#### 하위 페이지 {#child-pages}

현재 페이지나 다른 페이지의 하위 페이지에서 목록을 빌드할 수 있습니다.

![](/help/assets/chlimage_1-39.png)

* **상위 페이지**
   * 목록을 작성하는 페이지의 하위 페이지
   * 현재 페이지를 사용하려면 비워 둡니다.
* **하위 깊이** - 사용되는 계층 구조의 레벨 횟수

#### 고정 목록 {#fixed-list}

항목의 고정 목록 통해 목록을 빌드할 수 있습니다.

![](/help/assets/chlimage_1-40.png)

**추가** 버튼을 탭하거나 클릭하여 새 항목을 목록에 삽입합니다.

* 목록에 항목의 텍스트를 입력하거나 **선택 대화 상자**&#x200B;를 사용하여 AEM에서 항목을 선택합니다.
* 드래그 핸들을 사용하여 목록의 항목을 재배열합니다.
* 휴지통을 사용하여 목록에서 항목을 삭제합니다.

#### 검색 {#search-list}

AEM 콘텐츠 검색 결과를 통해 목록을 빌드할 수 있습니다.

![](/help/assets/chlimage_1-41.png)

* **검색 쿼리** - 전체 텍스트 검색에 대한 문자열을 실행하여 목록 요소를 생성합니다.
* **검색** - 검색이 실행되는 위치
   * **선택 대화 상자**&#x200B;를 사용하여 AEM에서 위치를 선택합니다.
   * 비워 두면 현재 페이지를 사용합니다.

#### 태그 {#tags}

특정 위치에서 특정 태그와 일치하는 페이지를 사용하여 목록을 빌드할 수 있습니다

![](/help/assets/chlimage_1-42.png)

* **상위 페이지** - 태그 일치의 시작 위치
   * **선택 대화 상자**&#x200B;를 사용하여 AEM에서 위치를 선택합니다.
   * 비워 두면 현재 페이지를 사용합니다.
* **태그** - 태그가 일치하는 위치
   * **검색** 대화 상자를 통해 태그를 선택합니다.
* **일치** - 목록에 포함되는 페이지의 자격을 충족하는 일치 유형을 정의합니다.
   * **임의의 태그**
   * **모든 태그**

#### 정렬 옵션 {#sort-options}

목록의 빌드 방법에 관계없이 언제든지 정의할 수 있는 특정 정렬 옵션이 있습니다.

![](/help/assets/chlimage_1-43.png)

* **항목별 순서** - 요소 순서를 변경하는 방법
   * **제목**
   * **마지막으로 수정한 날짜**
* **항목별 순서** - 항목을 지정하는 순서
   * **오름차순**
   * **내림차순**
* **최대 항목** - 목록에 표시되는 최대 항목 수
   * 모든 항목을 반환하려면 비워 둡니다.

### 항목 설정 {#item-settings}

**항목 설정** 탭을 사용하여 목록 요소 서식 설정을 구성할 수 있습니다.

![](/help/assets/chlimage_1-44.png)

* **항목 연결**
해당 페이지에 항목 연결
* **설명 표시**
항목 연결에 대한 설명 표시
* **날짜 표시**
항목 연결의 수정 날짜 표시

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 통해 콘텐츠 작성자에게 허용된 목록 유형과 사용 가능한 설정을 정의할 수 있습니다.

### 목록 설정 {#list-settings-1}

**목록 설정** 탭에서 날짜 형식을 정의하고, 구성 요소에서 콘텐츠 작성자가 사용할 수 있는 목록 유형을 정의할 수 있습니다.

![](/help/assets/chlimage_1-45.png)

* **날짜 형식** - 마지막 수정 날짜 표시에 사용할 형식
* **하위 목록 유형 비활성화** - 구성 요소의 하위 목록 유형을 비활성화합니다.
* **정적 목록 유형 비활성화** - 구성 요소의 정적 목록 유형을 비활성화합니다.
* **검색 목록 유형 비활성화** - 구성 요소의 검색 목록 유형을 비활성화합니다.
* **태그 목록 유형 비활성화** - 구성 요소의 태그 목록 유형을 비활성화합니다.

### 항목 설정 {#item-settings-1}

**항목 설정** 탭에서, 콘텐츠 작성자가 구성 요소에서 사용할 수 있는 개별 목록 요소에 대한 서식 옵션을 정의할 수 있습니다.

![](/help/assets/chlimage_1-46.png)

* **항목 연결** - [편집 대화 상자](#edit-dialog)에서 항목 연결을 활성화합니다.
* **설명 표시** - [편집 대화 상자](#edit-dialog)에서 설명 표시를 활성화합니다.
* **날짜 표시** - [편집 대화 상자](#edit-dialog)에서 날짜 표시 옵션을 활성화합니다.

## 기술 세부 사항 {#technical-details}

목록 구성 요소에 대한 최신 기술 설명서는[ GitHub에서 확인할 수 있습니다](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/list/v1/list).

GitHub에서 전체 핵심 구성 요소 프로젝트를 다운로드할 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

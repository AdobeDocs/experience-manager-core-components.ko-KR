---
title: 탐색 표시 구성 요소(v1)
description: 핵심 구성 요소 브레드크럼 구성 요소는 컨텐츠 계층 구조에서 페이지의 위치를 기반으로 링크의 브레드크럼을 만드는 탐색 구성 요소입니다.
index: n
role: 건축가, 개발자, 관리자, 비즈니스 전문가
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 1%

---


# 탐색 표시 구성 요소(v1) {#breadcrumb-component-v}

핵심 구성 요소 브레드크럼 구성 요소는 컨텐츠 계층 구조에서 페이지의 위치를 기반으로 링크의 브레드크럼을 만드는 탐색 구성 요소입니다.

## 사용량 {#usage}

탐색 표시 구성 요소는 사이트 계층 내에 있는 현재 페이지의 위치를 표시하여 페이지 방문자가 현재 위치에서 페이지 계층을 탐색할 수 있도록 합니다. 페이지 머리글이나 바닥글에 자주 통합되어 있습니다.

기본 탐색 수준 및 현재 페이지 또는 숨겨진 페이지를 표시하는 기능과 같은 사용 가능한 옵션은 템플릿 작성자가 [디자인 대화 상자](#design-dialog)에서 정의할 수 있습니다. 그런 다음 내용 편집자는 [편집 대화 상자](#edit-dialog)에서 숨겨진 페이지를 표시할지 여부와 구성 요소에 대한 실제 탐색 수준을 선택할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

이 문서에서는 AEM 6.3의 핵심 구성 요소 릴리스 1.0.0에 처음 소개된 탐색 표시 구성 요소의 v1에 대해 설명합니다.

다음 표는 탐색 표시 구성 요소의 v1 호환성을 보여줍니다.

| AEM 버전 | 탐색 표시 구성 요소 v1 |
|--- |--- |
| 6.3 | 호환 가능 |
| 6.4 | 호환 가능 |

>[!CAUTION]
>
>이 문서에서는 탐색 표시 구성 요소의 v1에 대해 설명합니다.
>탐색 표시 구성 요소의 현재 버전에 대한 자세한 내용은 [탐색 표시 구성 요소](/help/components/breadcrumb.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

다음은 [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html)에서 가져온 샘플입니다.

### 스크린샷 {#screenshot}

![](/help/assets/chlimage_1-33.png)

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
>핵심 구성 요소에서 JSON 내보내기를 사용하려면 핵심 구성 요소의 릴리스 1.1.0이 필요합니다. 자세한 내용은 핵심 구성 요소 v1](/help/versions.md)에 대한 호환성 정보를 참조하십시오.[

## 편집 대화 상자 {#edit-dialog}

편집 대화 상자를 사용하면 컨텐츠 작성자가 표시해야 하는 계층 구조의 깊이뿐만 아니라 탐색 표시의 숨겨진 및 활성 페이지를 표시하지 않을 수 있습니다.

![](/help/assets/chlimage_1-34.png)

* **시작할**  탐색 수준 - 계층 구조에서 탐색 표시 구성 요소가 현재 페이지로 이동하기 시작해야 합니다. 예: We.Retail:

   * 1이 `/content/we-retail`에서 시작
   * 2는 `/content/we-retail/<country>`에서 시작

* **숨김**  표시 - 탐색 표시에 숨김으로 표시된 페이지를 표시합니다(기본적으로 표시되지 않음)
* **현재** 숨기기 - 탐색 표시의 현재 페이지를 표시합니다(기본적으로 표시됨).

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 사용하여 표시해야 하는 계층 구조의 깊이뿐만 아니라 탐색 표시의 숨겨진 페이지와 활성 페이지를 표시하지 않는 옵션에 대한 기본값을 정의할 수 있습니다.

![](/help/assets/chlimage_1-35.png)

* **시작할**  탐색 수준 - 탐색 표시 구성 요소가 페이지에 추가될 때 계층 구조에서 탐색 표시 구성 요소가 현재 페이지로 이동하기 시작하는 위치에 대한 기본값을 정의합니다.
* **숨김 표시**  - 탐색 표시 구성  **요소가 페이지에** 추가될 때 [숨겨진 표시] 옵션의 기본값을 정의합니다.

   * 이 옵션은 작성자에 대한 옵션을 활성화하거나 비활성화하지 않습니다. 기본값은 설정만 설정합니다.

* **현재**  숨기기 - 탐색 표시 구성 요소가 페이지에  **추가될** 때 [현재 숨기기] 옵션의 기본값을 정의합니다.

   * 이 옵션은 작성자에 대한 옵션을 활성화하거나 비활성화하지 않습니다. 기본값은 설정만 설정합니다.

## 기술 세부 정보 {#technical-details}

탐색 표시 구성 요소 [에 대한 최신 기술 문서는 GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v1/breadcrumb)에서 찾을 수 있습니다.

전체 핵심 구성 요소 프로젝트를 GitHub에서 다운로드할 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)에서 확인할 수 있습니다.

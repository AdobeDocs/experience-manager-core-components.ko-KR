---
title: 이동 경로 구성 요소 (v1)
description: 핵심 구성 요소의 이동 경로 구성 요소는 콘텐츠 계층 구조의 페이지 위치에 따라 링크의 이동 경로를 빌드하는 탐색 구성 요소입니다.
index: n
role: Architect, Developer, Admin, User
exl-id: 4845e649-033a-43a8-b5ee-892a3f2a8b98
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 100%

---


# 이동 경로 구성 요소 (v1) {#breadcrumb-component-v}

핵심 구성 요소의 이동 경로 구성 요소는 콘텐츠 계층 구조의 페이지 위치에 따라 링크의 이동 경로를 빌드하는 탐색 구성 요소입니다.

## 사용량 {#usage}

이동 경로 구성 요소의 사이트 계층 구조 내부에 현재 페이지 위치가 표시되면 페이지 방문자는 현재 위치에서 페이지 계층 구조를 탐색할 수 있습니다. 이는 종종 페이지 머리글이나 바닥글에 통합됩니다.

템플릿 작성자는 [디자인 대화 상자](#design-dialog)에서 기본 탐색 수준과 현재 페이지 또는 숨겨진 페이지 표시하기 기능 등 사용 가능한 옵션을 정의할 수 있습니다. 그런 다음 콘텐츠 편집기는 숨겨진 페이지 표시 여부를 선택하고 [편집 대화 상자](#edit-dialog)에서 구성 요소의 실제 탐색 수준을 선택할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

이 문서에서는 AEM 6.3을 포함하는 핵심 구성 요소 릴리스 1.0.0과 함께 최초 도입된 이동 경로 구성 요소 v1에 대해 설명합니다.

다음 테이블에서 이동 경로 구성 요소 v1의 호환성을 확인할 수 있습니다.

| AEM 버전 | 이동 경로 구성 요소 v1 |
|--- |--- |
| 6.3 | 호환 가능 |
| 6.4 | 호환 가능 |

>[!CAUTION]
>
>이 문서에서는 이동 경로 구성 요소 v1에 대해 설명합니다.
>>현재 버전의 이동 경로 구성 요소에 대한 자세한 내용은 [이동 경로 구성 요소](/help/components/breadcrumb.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

다음은 [We.Retail](https://helpx.adobe.com/kr/experience-manager/6-4/sites/developing/using/we-retail.html)에서 얻은 샘플입니다.

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
>핵심 구성 요소에서 JSON을 내보내는 데 핵심 구성 요소 릴리스 1.1.0이 필요합니다. 자세한 내용은 [핵심 구성 요소 v1에 대한 호환성 정보](/help/versions.md)를 참조하십시오.

## 편집 대화 상자 {#edit-dialog}

콘텐츠 작성자는 편집 대화 상자를 통해 이동 경로의 숨겨진 페이지 및 활성 페이지뿐만 아니라 표시할 계층 구조의 깊이를 표시하지 않을 수 있습니다.

![](/help/assets/chlimage_1-34.png)

* **탐색-수준 시작** - 계층 구조에서 이동 경로 구성 요소가 현재 페이지로 하강하는 시작점. 예를 들어 We.Retail에서:

   * `/content/we-retail`에서 1차 시작
   * `/content/we-retail/<country>`에서 2차 시작

* **숨김 표시** - 숨김으로 표시된 이동 경로의 페이지를 표시함(기본적으로 표시되지 않음)
* **현재 숨김** - 이동 경로의 현재 페이지를 표시하지 않음(기본적으로 표시됨)

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 통해 이동 경로의 숨겨진 페이지 및 활성 페이지뿐만 아니라 표시할 계층 구조의 깊이를 표시하지 않도록 옵션의 기본값을 정의할 수 있습니다.

![](/help/assets/chlimage_1-35.png)

* **탐색-수준 시작** - 이동 경로 구성 요소가 페이지에 추가되면 계층 구조에서 이동 경로 구성 요소가 현재 페이지로 하강하는 시작점을 대한 기본값을 정의합니다.
* **숨김 표시** - 이동 경로 구성 요소가 페이지에 추가되면 **숨김 표시** 옵션에 대한 기본값을 정의합니다.

   * 이로 인해 작성자의 옵션이 활성화되거나 비활성화되지 않습니다. 기본값만 설정됩니다.

* **현재 숨김** - 이동 경로 구성 요소가 페이지에 추가되면 **현재 숨김** 옵션에 대한 기본값을 정의합니다.

   * 이로 인해 작성자의 옵션이 활성화되거나 비활성화되지 않습니다. 기본값만 설정됩니다.

## 기술 세부 사항 {#technical-details}

이동 경로 구성 요소에 대한 최신 기술 설명서는[ GitHub에서 확인할 수 있습니다](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v1/breadcrumb).

GitHub에서 전체 핵심 구성 요소 프로젝트를 다운로드할 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

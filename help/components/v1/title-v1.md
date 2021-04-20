---
title: 제목 구성 요소(v1)
description: 핵심 구성 요소 제목 구성 요소는 즉석 편집을 제공하는 섹션 제목 구성 요소입니다.
index: n
role: Architect, Developer, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 2%

---


# 제목 구성 요소(v1) {#title-component-v}

핵심 구성 요소 제목 구성 요소는 즉석 편집을 제공하는 섹션 제목 구성 요소입니다.

## 사용량 {#usage}

제목 구성 요소는 컨텐츠 섹션의 제목 또는 머리글로 사용되도록 되어 있습니다.

사용 가능한 머리글 수준은 [디자인 대화 상자](#design-dialog)에서 템플릿 작성자가 정의할 수 있습니다. 내용 편집기는 [편집 대화 상자](#edit-dialog)에서 사용 가능한 머리글 수준 중에서 선택할 수 있습니다. 또한 편의를 위해 머리글 텍스트를 간단히 즉석 편집할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

이 문서에서는 AEM 6.3과 함께 핵심 구성 요소 릴리스 1.0.0에 처음 소개된 제목 구성 요소의 v1에 대해 설명합니다.

다음 표는 제목 구성 요소의 v1 호환성을 보여줍니다.

| AEM 버전 | 제목 구성 요소 v1 |
|--- |--- |
| 6.3 | 호환 가능 |
| 6.4 | 호환 가능 |

>[!CAUTION]
>
>이 문서에서는 제목 구성 요소의 버전 1에 대해 설명합니다.
>
>제목 구성 요소의 현재 버전에 대한 자세한 내용은 [제목 구성 요소](/help/components/title.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

다음은 [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html)에서 가져온 샘플입니다.

### 스크린샷 {#screenshot}

![](/help/assets/chlimage_1-36.png)

### HTML {#html}

```
<div class="cmp cmp-title aem-GridColumn aem-GridColumn--default--12">
     <h2>Welcome! This is our finest equipment!</h2>
</div>
```

### JSON {#json}

```
"title": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              ":type": "weretail/components/content/title",
              "jcr:title": "Welcome! This is our finest equipment!",
              "type": "h2"
            }
```

>[!NOTE]
>
>핵심 구성 요소에서 JSON 내보내기를 사용하려면 핵심 구성 요소의 릴리스 1.1.0이 필요합니다. 자세한 내용은 핵심 구성 요소 v1](/help/versions.md)에 대한 호환성 정보를 참조하십시오.[

## 편집 대화 상자 {#edit-dialog}

편집 대화 상자를 사용하면 컨텐츠 작성자가 제목 텍스트를 정의할 수 있을 뿐만 아니라 제목 수준을 선택할 수 있습니다.

>[!NOTE]
>
>제목에 빈 값을 사용하면 페이지 제목이 표시됩니다.

![](/help/assets/chlimage_1-91.png)

즉석 편집기를 사용하여 제목 구성 요소의 텍스트를 편집할 수도 있습니다.

![](/help/assets/chlimage_1-37.png)

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 사용하여 컨텐츠 작성자가 작성할 때 제목 구성 요소가 가질 기본 제목 수준을 정의할 수 있습니다.

![](/help/assets/chlimage_1-92.png)

## 기술 세부 정보 {#technical-details}

제목 구성 요소 [에 대한 최신 기술 문서는 GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/title/v1/title)에서 찾을 수 있습니다.

전체 핵심 구성 요소 프로젝트를 GitHub에서 다운로드할 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)에서 확인할 수 있습니다.

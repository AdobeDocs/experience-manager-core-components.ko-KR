---
title: 제목 구성 요소(v1)
description: 코어 구성 요소 제목 구성 요소는 즉석 편집 기능을 하는 섹션 제목 구성 요소입니다.
index: n
role: Architect, Developer, Admin, User
exl-id: 79549ac0-82f2-4ea0-9cce-d534d0b47b5c
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 2%

---

# 제목 구성 요소(v1) {#title-component-v}

코어 구성 요소 제목 구성 요소는 즉석 편집 기능을 하는 섹션 제목 구성 요소입니다.

## 사용량 {#usage}

제목 구성 요소는 컨텐츠 섹션의 제목 또는 머리글로 사용됩니다.

사용 가능한 제목 수준은 [디자인 대화 상자](#design-dialog)에서 템플릿 작성자가 정의할 수 있습니다. 콘텐츠 편집기는 [편집 대화 상자의 사용 가능한 머리글 수준 중에서 선택할 수 있습니다](#edit-dialog). 편의상, 제목 텍스트를 즉석 편집할 수도 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

이 문서에서는 원래 AEM 6.3과 함께 코어 구성 요소 릴리스 1.0.0에 소개된 제목 구성 요소 v1에 대해 설명합니다.

다음 표에는 제목 구성 요소 v1의 호환성이 나와 있습니다.

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
>코어 구성 요소에서 JSON 내보내기를 사용하려면 핵심 구성 요소 릴리스 1.1.0이 필요합니다. 자세한 내용은 코어 구성 요소 v1](/help/versions.md)에 대한 호환성 정보를 참조하십시오.[

## 편집 대화 상자 {#edit-dialog}

편집 대화 상자에서는 컨텐츠 작성자가 제목 텍스트를 정의하고 제목 수준을 선택할 수 있습니다.

>[!NOTE]
>
>제목이 비어 있는 값으로 인해 페이지 제목이 표시됩니다.

![](/help/assets/chlimage_1-91.png)

즉석 편집기를 사용하여 제목 구성 요소의 텍스트를 편집할 수도 있습니다.

![](/help/assets/chlimage_1-37.png)

## 디자인 대화 상자 {#design-dialog}

디자인 대화 상자에서는 템플릿 작성자가 컨텐츠 작성자가 만들 때 제목 구성 요소가 가질 기본 제목 수준을 정의할 수 있습니다.

![](/help/assets/chlimage_1-92.png)

## 기술 세부 정보 {#technical-details}

제목 구성 요소 [에 대한 최신 기술 설명서는 GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/title/v1/title)에 있습니다.

전체 코어 구성 요소 프로젝트는 GitHub에서 다운로드할 수 있습니다.

코어 구성 요소 개발에 대한 자세한 내용은 [코어 구성 요소 개발자 설명서](/help/developing/overview.md)에서 확인할 수 있습니다.

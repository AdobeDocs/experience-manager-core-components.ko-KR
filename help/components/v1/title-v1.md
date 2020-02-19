---
title: 제목 구성 요소(v1)
description: 핵심 구성 요소 제목 구성 요소는 즉석 편집을 제공하는 섹션 제목 구성 요소입니다.
index: n
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# 제목 구성 요소(v1) {#title-component-v}

핵심 구성 요소 제목 구성 요소는 즉석 편집을 제공하는 섹션 제목 구성 요소입니다.

## 사용량 {#usage}

제목 구성 요소는 컨텐츠 섹션의 제목이나 머리글로 사용됩니다.

사용 가능한 제목 수준은 [디자인 대화](#design-dialog)상자에서 템플릿 작성자가 정의할 수 있습니다. 컨텐츠 편집기는 [편집 대화 상자의](#edit-dialog)사용 가능한 머리글 수준 중에서 선택할 수 있습니다. 편리한 추가 기능을 위해 제목 텍스트를 직접 편집할 수도 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

이 문서에서는 AEM 6.3의 핵심 구성 요소 릴리스 1.0.0에서 처음 소개된 제목 구성 요소의 v1에 대해 설명합니다.

다음 표에는 제목 구성 요소의 v1 호환성이 나와 있습니다.

| AEM 버전 | 제목 구성 요소 v1 |
|--- |--- |
| 6.3 | 호환 가능 |
| 6.4 | 호환 가능 |

>[!CAUTION]
>
>이 문서에서는 제목 구성 요소의 버전 1에 대해 설명합니다.
>
>제목 구성 요소의 현재 버전에 대한 자세한 내용은 제목 구성 요소 [문서를](/help/components/title.md) 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

다음은 We.Retail에서 [가져온 샘플입니다](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

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
>핵심 구성 요소에서 JSON을 내보내려면 핵심 구성 요소 릴리스 1.1.0이 필요합니다. 자세한 내용은 핵심 구성 요소 v1의 [](/help/versions.md) 호환성 정보를 참조하십시오.

## Edit Dialog {#edit-dialog}

편집 대화 상자에서는 컨텐츠 작성자가 제목 텍스트를 정의할 수 있을 뿐만 아니라 제목 수준을 선택할 수 있습니다.

>[!NOTE]
>
>제목에 대한 값이 비어 있으면 페이지 제목이 표시됩니다.

![](/help/assets/chlimage_1-91.png)

즉석 편집기를 사용하여 제목 구성 요소의 텍스트를 편집할 수도 있습니다.

![](/help/assets/chlimage_1-37.png)

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 사용하여 컨텐츠 작성자가 작성할 때 제목 구성 요소가 가질 기본 제목 수준을 정의할 수 있습니다.

![](/help/assets/chlimage_1-92.png)

## 기술 정보 {#technical-details}

제목 구성 요소에 대한 최신 기술 문서는 GitHub에서 [찾을 수 있습니다](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/title/v1/title).

전체 핵심 구성 요소 프로젝트는 GitHub에서 다운로드할 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 핵심 구성 요소 개발자 [설명서를](/help/developing/overview.md)참조하십시오.

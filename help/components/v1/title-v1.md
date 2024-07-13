---
title: 제목 구성 요소 (v1)
description: 핵심 구성 요소의 제목 구성 요소는 바로 편집 기능이 있는 섹션 머리말 구성 요소입니다.
index: n
role: Architect, Developer, Admin, User
exl-id: 79549ac0-82f2-4ea0-9cce-d534d0b47b5c
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 100%

---

# 제목 구성 요소 (v1) {#title-component-v}

핵심 구성 요소의 제목 구성 요소는 바로 편집 기능이 있는 섹션 머리말 구성 요소입니다.

## 사용량 {#usage}

제목 구성 요소는 콘텐츠 섹션의 제목이나 머리글로 사용하기 위한 목적으로 작성되었습니다.

템플릿 작성자는 [디자인 대화 상자](#design-dialog)에서 사용 가능한 머리말 수준을 정의할 수 있습니다. 콘텐츠 편집기는 [편집 대화 상자](#edit-dialog)에서 사용 가능한 머리말 수준 중 하나를 선택할 수 있습니다. 편리성을 추가하기 위해 머리글 텍스트의 간단한 바로 편집 기능을 사용할 수도 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

이 문서에서는 AEM 6.3을 포함하는 핵심 구성 요소 릴리스 1.0.0과 함께 최초 도입된 제목 구성 요소 v1에 대해 설명합니다.

다음 표에서 제목 구성 요소 v1의 호환성을 확인할 수 있습니다.

| AEM 버전 | 제목 구성 요소 v1 |
|--- |--- |
| 6.3 | 호환 가능 |
| 6.4 | 호환 가능 |

>[!CAUTION]
>
>이 문서에서는 제목 구성 요소 v1에 대해 설명합니다.
>
>현재 버전의 제목 구성 요소에 대한 자세한 내용은 [제목 구성 요소](/help/components/title.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

다음은 [We.Retail](https://helpx.adobe.com/kr/experience-manager/6-4/sites/developing/using/we-retail.html)에서 얻은 샘플입니다.

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
>핵심 구성 요소에서 JSON을 내보내는 데 핵심 구성 요소 릴리스 1.1.0이 필요합니다. 자세한 내용은 [핵심 구성 요소 v1에 대한 호환성 정보](/help/versions.md)를 참조하십시오.

## 편집 대화 상자 {#edit-dialog}

콘텐츠 작성자는 편집 대화 상자를 통해 제목 텍스트를 정의하고 머리말 수준을 선택할 수 있습니다.

>[!NOTE]
>
>제목 값이 비어 있으면 페이지 제목이 표시될 수 있습니다.

![](/help/assets/chlimage_1-91.png)

바로 편집 기능을 가진 편집기를 사용하여 제목 구성 요소의 텍스트를 편집합니다.

![](/help/assets/chlimage_1-37.png)

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 통해 콘텐츠 작성자가 제목 구성 요소를 생성할 때 이에 포함될 기본 머리말 수준을 정의할 수 있습니다.

![](/help/assets/chlimage_1-92.png)

## 기술 세부 사항 {#technical-details}

제목 구성 요소에 대한 최신 기술 설명서는[ GitHub에서 확인할 수 있습니다](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/title/v1/title).

GitHub에서 전체 핵심 구성 요소 프로젝트를 다운로드할 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

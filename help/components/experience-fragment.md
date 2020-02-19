---
title: 경험 조각 구성 요소
description: 경험 조각 구성 요소를 사용하면 컨텐츠 작성자가 경험 조각 변형을 페이지에 추가할 수 있습니다.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# 경험 조각 구성 요소{#experience-fragment-component}

핵심 구성 요소 경험 조각 구성 요소를 사용하면 컨텐츠 작성자가 현지화된 사이트 구조를 지원하는 동안 페이지에 경험 조각 변형을 배치할 수 있습니다.

## 사용량 {#usage}

핵심 구성 요소 경험 조각 구성 요소를 사용하면 컨텐츠 작성자가 기존 경험 조각 변형에서 선택하고 컨텐츠 페이지에 배치할 수 있습니다. 경험 조각 구성 요소는 현지화된 사이트 구조도 지원합니다.

* 구성 요소의 속성은 [구성 대화 상자에서](#configure-dialog)정의할 수 있습니다.
* 구성 요소를 페이지에 추가할 때의 기본값은 [디자인 대화 상자에서](#design-dialog)정의할 수 있습니다.

## 현지화된 사이트 구조 지원 {#localized-site-structure}

경험 조각 구성 요소는 현지화된 사이트 구조에 적응성이 있으며 페이지의 현지화를 기반으로 적절한 경험 조각을 렌더링합니다. 이렇게 하려면 경험 조각이 다음 조건을 충족해야 합니다.

* 경험 조각 구성 요소가 템플릿에 추가됩니다.
* 이 템플릿은 아래 현지화된 구조에 속하는 새 컨텐츠 페이지를 만드는 데 사용됩니다 `/content/<site>`.
* 컨텐츠 페이지에서 참조되는 경험 조각은 아래의 현지화된 경험 조각 구조의 일부이며, 동일한 구성 요소 이름 사용을 `/content/experience-fragments` `/content/<site>` 포함하여 아래 사이트와 동일한 패턴을 따릅니다.

이 경우, 현재 페이지와 동일한 현지화(언어, 블루프린트 또는 Live Copy)가 있는 조각은 템플릿의 일부로 렌더링됩니다.

이 동작은 템플릿에 추가된 경험 조각 구성 요소로 제한됩니다. 개별 컨텐츠 페이지에 추가된 경험 조각 구성 요소는 구성 요소 내에 구성된 정확한 경험 조각 변환을 렌더링합니다.

* 경험 조각 구성 요소의 현지화 기능이 작동하는 방법의 예는 아래 [섹션을 참조하십시오](#example).
* 핵심 구성 요소의 현지화 기능이 함께 작동하는 방법에 대한 예는 핵심 구성 요소 [페이지의](/help/get-started/localization.md)현지화 기능을 참조하십시오.

### 예 {#example}

귀하의 컨텐츠는 다음과 같은 모습이라고 가정해 보겠습니다.

```
/content
+-- experience-fragments
   \-- we-retail
      +-- language-masters
      +-- us
         +-- en
            +-- footerTextXf
            \-- headerTextXf
         \-- es
            +-- footerTextXf
            \-- headerTextXf
      \-- ch
         +-- de
            +-- footerTextXf
            \-- headerTextXf
         +-- fr
            +-- footerTextXf
            \-- headerTextXf
         \-- it
            +-- footerTextXf
            \-- headerTextXf
+-- we-retail
   +-- language-masters
   +-- us
      +-- en
      \-- es
   +-- ch
      +-- de
      +-- fr
      \-- it
+-- wknd-events
\-- wknd-shop
```

아래 구조가 `/content/experience-fragments/we-retail` 의 구조를 반영한다는 것을 `/content/we-retail`확인하십시오.

이 경우 경험 조각 구성 요소가 템플릿에 `/content/experience-fragments/we-retail/us/en/footerTextXf` 배치되면 해당 템플릿을 기반으로 작성된 현지화된 페이지가 현지화된 컨텐츠 페이지에 해당하는 현지화된 경험 조각을 자동으로 렌더링합니다.

따라서 동일한 템플릿을 사용하는 컨텐트 페이지로 이동하면 `/content/we-retail/ch/de` 대신 렌더링됩니다 `/content/experience-fragments/we-retail/ch/de/footerTextXf` `/content/experience-fragments/we-retail/us/en/footerTextXf`.

### 폴백 {#fallback}

경험 조각 구성 요소는 다음 순서로 해당 현지화된 구성 요소를 찾으려고 시도합니다.

1. 먼저 언어 루트를 찾으려고 합니다.
1. 찾을 수 없으면 청사진을 찾으려고 합니다.
1. 찾을 수 없으면 Live Copy를 찾으려고 합니다.
1. 찾을 수 없는 경우, 구성 요소에 구성된 경험 조각으로 기본값이 설정됩니다.

## 버전 및 호환성 {#version-and-compatibility}

경험 조각 구성 요소의 현재 버전은 v1이며, 이 버전은 2019년 9월에 릴리스 2.6.0의 핵심 구성 요소에서 도입되었으며 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소 버전이 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.3 | AEM 6.4 | AEM 6.5 | 클라우드 서비스로 AEM 사용 |
|--- |--- |--- |---|---|
| v1 | 호환 가능 | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 핵심 구성 요소 [버전을 참조하십시오](/help/versions.md).

## 샘플 구성 요소 출력 {#sample-component-output}

경험 조각 구성 요소뿐만 아니라 구성 옵션 예와 HTML 및 JSON 출력을 보려면 구성 요소 라이브러리를 [방문하십시오](https://adobe.com/go/aem_cmp_library_xf).

## 기술 정보 {#technical-details}

경험 조각 구성 요소에 대한 최신 기술 문서는 GitHub에서 [찾을 수 있습니다](https://adobe.com/go/aem_cmp_tech_xf_v1).

핵심 구성 요소 개발에 대한 자세한 내용은 핵심 구성 요소 개발자 [설명서를](/help/developing/overview.md)참조하십시오.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자에서는 컨텐츠 작성자가 페이지에서 렌더링해야 하는 경험 조각 변형을 선택할 수 있습니다.

![](/help/assets/screen-shot-2019-08-23-10.49.21.png)

선택 **대화 상자 열기** 단추를 사용하여 구성 요소 선택기를 열어 컨텐츠 페이지에 추가할 경험 조각 구성 요소 변형을 선택합니다.

경험 조각 구성 요소를 템플릿에 추가하는 경우 경험 조각이 지역화되면 자동으로 현지화되므로 페이지에서 렌더링되는 내용은 명시적으로 선택한 구성 요소와 다를 수 있습니다. [자세한 내용은 위의](#example) 예를 참조하십시오.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 사용하여 경험 조각 구성 요소를 사용하는 컨텐츠 작성자가 사용할 수 있는 옵션과 경험 조각 구성 요소를 배치할 때 설정된 기본값을 정의할 수 있습니다.

![](/help/assets/screen-shot-2019-08-23-10.48.36.png)

경험 조각 구성 요소는 AEM 스타일 [시스템을 지원합니다](/help/get-started/authoring.md#component-styling).

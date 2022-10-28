---
title: 이메일 경험 조각 구성 요소
description: 이메일 경험 조각 구성 요소를 사용하면 컨텐츠 작성자가 현지화된 컨텐츠 구조를 지원하는 동안 컨텐츠에 경험 조각 변형을 배치할 수 있습니다.
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: tm+mt
source-wordcount: '927'
ht-degree: 27%

---


# 이메일 경험 조각 구성 요소 {#email-experience-fragment-component}

이메일 경험 조각 구성 요소를 사용하면 컨텐츠 작성자가 현지화된 컨텐츠 구조를 지원하는 동안 컨텐츠에 경험 조각 변형을 배치할 수 있습니다.

## 사용량 {#usage}

이메일 경험 조각 구성 요소를 사용하여 컨텐츠 작성자는 기존 경험 조각 변형에서 선택하고 컨텐츠 내에 배치할 수 있습니다. 경험 조각 은 컨텐츠와 레이아웃을 모두 포함하고 여러 채널에서 재사용할 수 있는 컨텐츠 그룹입니다.

* [구성 대화 상자](#configure-dialog)에서 구성 요소의 속성을 정의할 수 있습니다.
* 컨텐츠에 추가할 때 구성 요소의 기본값은 [디자인 대화 상자](#design-dialog).

이메일 경험 조각 구성 요소는 현지화된 사이트 구조를 지원합니다.

## 버전 및 호환성 {#version-and-compatibility}

이메일 경험 조각 구성 요소의 현재 버전은 v1이며, 2022년 10월에 이메일 코어 구성 요소 릴리스 X에서 도입되었으며 이 문서에 설명되어 있습니다.

다음 표에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | 호환 가능 | 호환 가능 |

이메일 핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 문서를 참조하십시오 [이메일 핵심 구성 요소 버전.](/help/email/versions.md)

## 현지화된 사이트 구조 지원 {#localized-site-structure}

이메일 경험 조각 구성 요소는 현지화된 컨텐츠 구조에 적응형이며 컨텐츠의 현지화를 기반으로 적절한 경험 조각을 렌더링합니다. 이를 수행하려면 경험 조각이 다음 조건을 충족해야 합니다.

* 이메일 경험 조각 구성 요소가 [페이지 템플릿.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/templates.html)
* 해당 템플릿을 사용하여 `/content/<site>` 아래 현지화된 구조의 일부인 새 콘텐츠 페이지를 만듭니다.
* 컨텐츠 페이지에서 참조되는 경험 조각은 아래의 현지화된 경험 조각 구조의 일부입니다 `/content/experience-fragments` 아래와 같은 패턴을 따릅니다 `/content/<site>` 동일한 구성 요소 이름 사용을 포함합니다.

이 경우 동일한 현지화( )가 있는 조각[언어, 블루프린트 또는 live copy](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/administering/reusing-content/msm-and-translation.html))을 클릭하여 현재 페이지가 템플릿의 일부로 렌더링됩니다.

이 동작은 템플릿에 추가된 이메일 경험 조각 구성 요소로 제한됩니다. 개별 컨텐츠 페이지에 추가된 경험 조각 구성 요소는 구성 요소 내에 구성된 정확한 경험 조각 표현물을 렌더링합니다.

* 경험 조각 구성 요소의 현지화 기능이 작동하는 방식에 대한 예는 를 참조하십시오 [아래 섹션](#example).
* 핵심 구성 요소의 현지화 기능이 어떻게 서로 작동하는지 사례를 알고 싶다면 [핵심 구성 요소의 현지화 기능](/help/get-started/localization.md)을 참조하십시오.

### 예 {#example}

콘텐츠의 형태가 다음과 같습니다.

```
/content
+-- experience-fragments
   \-- wknd
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
+-- wknd
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

`/content/experience-fragments/wknd` 아래의 구조는 `/content/wknd`의 구조를 미러링합니다.

이 경우 이메일 경험 조각 구성 요소인 경우 `/content/experience-fragments/wknd/us/en/footerTextXf` 를 템플릿에 배치하면 해당 템플릿을 기반으로 만들어진 현지화된 페이지가 현지화된 컨텐츠 페이지에 해당하는 현지화된 경험 조각을 자동으로 렌더링합니다.

동일한 템플릿을 사용하는 `/content/wknd/ch/de` 아래 콘텐츠 페이지로 이동하면 `/content/experience-fragments/wknd/us/en/footerTextXf` 대신 `/content/experience-fragments/wknd/ch/de/footerTextXf`가 렌더링됩니다.

### 대체 {#fallback}

이메일 경험 조각 구성 요소는 다음 순서로 해당 현지화된 구성 요소를 찾습니다.

1. 먼저 언어 루트 검색을 시도합니다.
1. 검색되지 않는 경우 블루프린트 검색을 시도합니다.
1. 검색되지 않는 경우 라이브 카피 검색을 시도합니다.
1. 찾을 수 없으면 기본적으로 구성 요소에 구성된 경험 조각으로 설정됩니다.

## 샘플 구성 요소 출력 {#sample-component-output}

이메일 경험 조각 구성 요소 와 구성 옵션의 예 및 HTML 및 JSON 출력을 보려면 [구성 요소 라이브러리.](https://adobe.com/go/aem_cmp_library_email_xf)

## 기술 세부 사항 {#technical-details}

경험 조각 구성 요소에 대한 최신 기술 설명서는[ GitHub에서 확인할 수 있습니다.](https://adobe.com/go/aem_cmp_email_tech_xf_v1)

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서입니다.](/help/developing/overview.md)

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자에서는 컨텐츠 작성자가 컨텐츠에서 렌더링해야 하는 경험 조각 변형을 선택할 수 있습니다.

![이메일 경험 조각 구성 요소의 편집 대화 상자](/help/email/assets/email-experience-fragment-edit.png)

를 사용하십시오 **선택 대화 상자 열기** 구성 요소 선택기를 열어 컨텐츠 페이지에 추가할 경험 조각 구성 요소 변형을 선택합니다.

이메일 경험 조각 구성 요소를 템플릿에 추가하는 경우 경험 구성 요소가 현지화된 경우 자동으로 현지화됩니다. 따라서 페이지에서 렌더링되는 내용은 명시적으로 선택한 구성 요소에 따라 달라질 수 있습니다. 자세한 내용은 [위의 예](#example)를 참조하십시오.

**ID**&#x200B;를 정의할 수도 있습니다. 이 옵션을 사용하면 HTM에서 구성 요소의 고유 식별자를 제어할 수 있습니다.

* 비워 두면 고유 ID가 자동으로 생성되며 결과 컨텐츠를 검사하여 찾을 수 있습니다.
* ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
* ID를 변경하면 CSS에 영향을 줄 수 있습니다.

### 스타일 탭 {#styles-tab-edit}

이메일 경험 조각 구성 요소는 AEM을 지원합니다 [스타일 시스템.](/help/get-started/authoring.md#component-styling)

드롭다운을 사용하여 구성 요소에 적용할 스타일을 선택합니다. 편집 대화 상자에서 선택한 항목은 구성 요소 툴바에서 선택한 항목과 동일한 효과를 가집니다.

스타일을 [디자인 대화 상자](#design-dialog) 을 클릭하여 탭을 사용할 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자에서 이메일 경험 조각 구성 요소를 사용하는 컨텐츠 작성자가 사용할 수 있는 옵션과 이메일 경험 조각 구성 요소를 배치할 때 설정된 기본값을 정의할 수 있습니다.

### 스타일 탭 {#styles-tab}

이메일 경험 조각 구성 요소는 AEM을 지원합니다 [스타일 시스템.](/help/get-started/authoring.md#component-styling)

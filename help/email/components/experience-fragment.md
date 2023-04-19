---
title: 이메일 경험 조각 구성 요소
description: 콘텐츠 작성자는 이메일 경험 조각 구성 요소를 통해 콘텐츠에 경험 조각 변형을 배치하면서 현지화된 콘텐츠 구조를 지원할 수 있습니다.
role: Architect, Developer, Admin, User
exl-id: 861c1fd1-6d6d-426c-a338-a558326fe16e
source-git-commit: 3abc29e0c186a84f079d5938b8b716f4c7378d65
workflow-type: tm+mt
source-wordcount: '888'
ht-degree: 100%

---


# 이메일 경험 조각 구성 요소 {#email-experience-fragment-component}

콘텐츠 작성자는 이메일 경험 조각 구성 요소를 통해 콘텐츠에 경험 조각 변형을 배치하면서 현지화된 콘텐츠 구조를 지원할 수 있습니다.

## 사용 {#usage}

콘텐츠 작성자는 이메일 경험 조각 구성 요소를 통해 기존 경험 조각 변형을 선택하여 콘텐츠에 배치할 수 있습니다. 경험 조각은 콘텐츠와 레이아웃을 모두 포함하고 여러 채널에서 재사용할 수 있는 콘텐츠 그룹입니다.

* [구성 대화 상자](#configure-dialog)에서 구성 요소의 속성을 정의할 수 있습니다.
* 구성 요소를 콘텐츠에 추가하는 경우 [디자인 대화 상자](#design-dialog)에서 구성 요소의 기본값을 정의할 수 있습니다.

이메일 경험 조각 구성 요소는 현지화된 사이트 구조를 지원합니다.

## 버전 및 호환성 {#version-and-compatibility}

현재 버전의 이메일 경험 조각 구성 요소는 2022년 10월 이메일 핵심 구성 요소 릴리스 X과(와) 함께 도입된 v1입니다. 이 문서에서는 해당 구성 요소에 대해 설명합니다.

다음 표에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | 호환 가능 | - |

이메일 핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 문서 [이메일 핵심 구성 요소 버전](/help/email/versions.md)을 참조하십시오.

## 현지화된 사이트 구조 지원 {#localized-site-structure}

이메일 경험 조각 구성 요소는 현지화된 콘텐츠 구조에 적응하고 콘텐츠의 현지화에 따라 해당 경험 조각을 렌더링합니다. 이 작업을 수행하려면 경험 조각은 다음 조건을 충족해야 합니다.

* 이메일 경험 조각 구성 요소를 [페이지 템플릿](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/templates.html)에 추가합니다.
* 해당 템플릿을 사용하여 `/content/<site>` 아래 현지화된 구조의 일부인 새 콘텐츠 페이지를 만듭니다.
* 콘텐츠 페이지에서 참조한 경험 조각은 동일한 구성 요소 이름을 사용하는 `/content/<site>` 아래 사이트와 동일한 패턴을 따르는 `/content/experience-fragments` 아래에 있는 현지화된 경험 조각 구조의 일부입니다.

이 경우 현지화 기능([언어, 블루프린트 또는 라이브 카피](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/administering/reusing-content/msm-and-translation.html))이 현재 페이지와 같은 조각은 템플릿의 일부로 렌더링됩니다.

이 비헤이비어는 템플릿에 추가된 이메일 경험 조각 구성 요소로 제한됩니다. 개별 콘텐츠 페이지에 추가된 경험 조각 구성 요소를 사용하여 정확한 경험 조각 렌디션을 렌더링하고 구성 요소 내부에 구성합니다.

* 경험 조각 구성 요소의 현지화 기능이 어떻게 작동하는지 사례를 알고 싶다면 [아래 섹션](#example)을 참조하십시오.
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

이 경우 이메일 경험 조각 구성 요소 `/content/experience-fragments/wknd/us/en/footerTextXf`를 템플릿에 배치하면 해당 템플릿을 기반으로 제작된 현지화된 페이지는 현지화된 콘텐츠 페이지에 해당되는 현지화된 경험 조각을 자동으로 렌더링합니다.

동일한 템플릿을 사용하는 `/content/wknd/ch/de` 아래 콘텐츠 페이지로 이동하면 `/content/experience-fragments/wknd/us/en/footerTextXf` 대신 `/content/experience-fragments/wknd/ch/de/footerTextXf`가 렌더링됩니다.

### 대체 {#fallback}

이메일 경험 조각 구성 요소는 해당 현지화된 구성 요소 검색을 다음 순서로 시도합니다.

1. 먼저 언어 루트 검색을 시도합니다.
1. 검색되지 않는 경우 블루프린트 검색을 시도합니다.
1. 검색되지 않는 경우 라이브 카피 검색을 시도합니다.
1. 검색되지 않는 경우 구성 요소에 구성되는 경험 조각으로 기본 설정됩니다.

## 기술 세부 사항 {#technical-details}

경험 조각 구성 요소에 대한 최신 기술 설명서는 [GitHub에서 확인할 수 있습니다.](https://adobe.com/go/aem_cmp_email_tech_xf_v1_kr)

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

콘텐츠 작성자는 구성 대화 상자를 통해 콘텐츠에 렌더링할 경험 조각 변형을 선택할 수 있습니다.

![이메일 경험 조각 구성 요소의 편집 대화 상자](/help/email/assets/email-experience-fragment-edit.png)

**선택 열기 대화 상자** 버튼을 통해 구성 요소 선택기를 열고 콘텐츠 페이지에 추가할 경험 조각 구성 요소를 선택합니다.

이메일 경험 조각 구성 요소가 템플릿에 추가되어 경험 조각이 현지화되면 경험 조각 구성 요소는 자동으로 현지화됩니다. 이 경우 페이지에 렌더링된 내용은 명시된 구성 요소와 다를 수 있습니다. 자세한 내용은 [위의 예](#example)를 참조하십시오.

**ID**&#x200B;를 정의할 수도 있습니다. 이 옵션을 통해 HTML에서 구성 요소의 고유 식별자를 제어할 수 있습니다.

* 비워 두면 고유 ID는 자동으로 생성되고 결과 콘텐츠 검사를 통해 발견될 수 있습니다.
* ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
* ID를 변경하면 CSS에 영향을 줄 수 있습니다.

### 스타일 탭 {#styles-tab-edit}

이메일 경험 조각 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

드롭다운을 사용하여 구성 요소에 적용할 스타일을 선택합니다. 편집 대화 상자에서 선택한 항목은 구성 요소 툴바에서 선택한 항목과 동일한 효과를 가집니다.

탭을 사용하려면 [디자인 대화 상자](#design-dialog)에서 이 구성 요소에 대한 스타일을 구성해야 합니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 통해 이메일 경험 조각 구성 요소를 사용하는 콘텐츠 작성자에게 제공되는 옵션과 이메일 경험 조각 구성 요소 배치 시 설정된 기본값을 정의할 수 있습니다.

### 스타일 탭 {#styles-tab}

이메일 경험 조각 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

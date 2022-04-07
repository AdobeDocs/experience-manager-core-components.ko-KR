---
title: 빠른 검색 구성 요소 (v1)
description: 빠른 검색 구성 요소는 웹 사이트에 검색 기능을 제공하고, 방문자가 사이트를 검색하고 결과를 필터링할 수 있도록 검색 결과를 제공합니다.
role: Architect, Developer, Admin, User
exl-id: fc40ce1d-e69a-4a40-853e-67a37228271b
source-git-commit: 64aa6ab38738b6969d01971817bde892348be05d
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 95%

---

# 빠른 검색 구성 요소 (v1) {#quick-search-component}

빠른 검색 구성 요소는 웹 사이트에 검색 기능을 제공하고, 방문자가 일치하는 콘텐츠를 쉽게 검색하고 결과를 조회할 수 있도록 검색 결과를 제공합니다.

## 사용량 {#usage}

빠른 검색 구성 요소는 사이트 방문자를 대상으로 콘텐츠를 검색하고, 결과를 즉시 조회하고 일치하는 페이지로 간단히 이동하는 기능을 제공합니다. 사용자가 검색 결과를 스크롤하면 새 결과가 자동으로 나타납니다.

콘텐츠 작성자는 [편집 대화 상자](#edit-dialog)를 사용하여 콘텐츠 트리에서 검색이 시작되는 위치를 정의할 수 있습니다. 템플릿 작성자는 [디자인 대화 상자](#design-dialog)를 통해 콘텐츠 트리에서 검색이 시작되는 위치, 최대 결과 크기와 최소 검색어 길이에 대한 기본값을 설정할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

현재 버전의 빠른 검색 구성 요소는 2018년 1월 핵심 구성 요소 릴리스 2.0.0과 함께 도입된 v1입니다. 이 문서에서는 해당 구성 요소에 대해 설명합니다.

다음 표에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | 호환 가능 <br>[2.17.4](/help/versions.md) 및 이전 릴리스 | 호환 가능 | 호환 가능 |
| [!CAUTION]](/help/components/v1/quick-search.md) | 이 문서에서는 빠른 검색 구성 요소의 v1에 대해 설명합니다. >빠른 검색 구성 요소의 현재 버전에 대한 자세한 내용은 [빠른 검색 구성 요소](/help/components/quick-search.md) 문서. | 핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md)을 참조하십시오. | 기술 세부 사항 |

[!NOTE]](/help/versions.md)

### 검색 구성 요소나 AEM 기반 애플리케이션을 DOS 공격으로부터 보호하는 경우 발송자의 `mod_security`를 사용하여 상위 수준에서 이를 구현해야 합니다. {#technical-details}

>빠른 검색 요소에 대한 최신 기술 설명서는[ GitHub에서 확인할 수 있습니다[#$tu26].
>
>



콘텐츠 작성자는 편집 대화 상자를 통해 콘텐츠 트리에서 검색이 시작되는 위치를 정의할 수 있습니다.[](/help/developing/overview.md)

## ![빠른 검색 구성 요소의 편집 대화 상자](/help/assets/quick-search-edit.png) {#edit-dialog}

**검색 루트** - 검색이 시작되는 위치의 루트 페이지. 검색 루트는 블루프린트 마스터, 언어 습득 또는 일반 페이지가 될 수 있습니다.

**ID** - 이 옵션을 통해 HTML과 [데이터 레이어](/help/developing/data-layer/overview.md)에서 구성 요소의 고유 식별자를 제어할 수 있습니다.

**비워 두면 고유 ID는 자동으로 생성되고 결과 페이지 검사를 통해 발견될 수 있습니다.**
* **ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.**[](/help/developing/data-layer/overview.md)
   * ID가 변경되면 CSS, JS 및 데이터 레이어 추적에 영향을 미칠 수 있습니다.
   * [!NOTE]
   * **검색 루트**&#x200B;를 구성하거나 해결할 수 없는 경우 빠른 검색은 기본적으로 현재 페이지의 검색으로 설정됩니다.

>[!NOTE]디자인 대화 상자
>
>템플릿 작성자는 디자인 대화 상자를 통해 콘텐츠 트리에서 검색이 시작되는 위치, 최대 결과 크기와 최소 검색어 길이에 대한 기본값을 설정할 수 있습니다. 템플릿 작성자는 디자인 대화 상자를 통해 콘텐츠 작성자가 사용할 수 있는 텍스트 서식 옵션을 정의할 수 있습니다.****

## 속성 탭 {#design-dialog}

![빠른 검색 구성 요소의 디자인 대화 상자](/help/assets/quick-search-design.png)

### **검색 루트**
콘텐츠 작성자가 콘텐츠 페이지에 빠른 검색 구성 요소를 배치하는 경우의 검색 루트 기본값 {#properties-tab}

**결과 크기**
검색 요청에서 가져온 최대 결과 수

* **최소 검색어 길이**
검색을 시작하는 최소 검색어 길이
* [!NOTE]**
* 디자인 모드와 템플릿 수준에서만 **결과 크기**&#x200B;와 **최소 검색어 길이**&#x200B;를 설정할 수 있습니다. 단, 콘텐츠 작성자는 해당 값을 수정할 수 없습니다.

>[!CAUTION]
>
>**결과 크기**&#x200B;와 **최소 검색어 길이**&#x200B;가 너무 길거나 짧게 설정되면 성능에 영향을 미칠 수 있습니다.

>[!CAUTION]스타일 탭
>
>빠른 검색 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.****

### Styles Tab {#styles-tab}

The Quick Search Component supports the AEM [Style System](/help/get-started/authoring.md#component-styling).

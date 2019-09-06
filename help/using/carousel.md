---
title: 회전판 구성 요소
seo-title: 회전판 구성 요소
description: 'null'
seo-description: 회전판 구성 요소를 사용하면 컨텐츠 작성자가 회전 회전판에 컨텐츠를 표시할 수 있습니다.
uuid: 34934491-BD 85-4 F 1 E-AE 22-BB 48 ED 4 DBD 5 C
content-type: 참조
topic-tags: 핵심 구성 요소
discoiquuid: 3510812 b -9 d 3 e -40 fe-b 986-0 f 15 d 40 b 42 ad
disttype: dist5
gnavtheme: 밝음
groupsectionnavitems: 아니오
hidemerchandisingbar: 상속
hidepromocomponent: 상속
modalsize: 426x240
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: d37cde072dea612ccb55ad31b4aaf42f17839cb4

---


# 회전판 구성 요소{#carousel-component}

컨텐츠 작성자는 핵심 구성 요소 캐러셀 구성 요소를 사용하여 탐색 가능한 캐러셀에 컨텐츠를 표시할 수 있습니다.

## 사용량 {#usage}

컨텐츠 작성자는 회전식 슬라이드 회전판에서 컨텐츠를 구성할 수 있습니다.

컨텐츠 작성자는 [편집 대화 상자를 사용하여](#edit-dialog) 여러 슬라이드를 만들고 이름을 지정하고 순서를 지정할 수 있을 뿐만 아니라 지연 시 자동 전환을 활성화할 수 있습니다. 템플릿 작성자는 [디자인 대화 상자를](#design-dialog)사용하여 회전판에 추가할 수 있는 구성 요소를 정의하고 자동 전환을 활성화 또는 비활성화하며 스타일을 사용자 정의할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

현재 Carousel 구성 요소 버전은 2018 년 10 월에 핵심 구성 요소의 릴리스 2.2.0에서 처음 소개된 v 1 이며 이 문서에서는 설명합니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서에 대한 링크를 제공합니다.

| 구성 요소 버전 | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 문서 [코어 구성 요소 버전을 참조하십시오](versions.md).

## 샘플 구성 요소 출력 {#sample-component-output}

회전판 구성 요소를 경험하고 HTML 및 JSON 출력뿐만 아니라 구성 옵션의 예를 보려면 [구성 요소 라이브러리를 참조하십시오](http://opensource.adobe.com/aem-core-wcm-components/library/carousel.html).

### 기술 세부 정보 {#technical-details}

회전판 구성 요소에 [대한 최신 기술 문서는 Github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/carousel/v1/carousel)에서 찾을 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서를](developing.md)참조하십시오.

## Edit Dialog {#edit-dialog}

컨텐츠 작성자는 편집 대화 상자를 사용하여 슬라이드를 추가, 이름 변경 및 재배치할 수 있을 뿐만 아니라 자동 전환 설정을 정의할 수 있습니다.

### 항목 탭 {#items-tab}

![](assets/screen-shot-2019-08-29-12.01.39.png)

**추가** 단추를 사용하여 구성 요소 선택기를 열어 탭으로 추가할 구성 요소를 선택합니다. 추가된 항목이 목록에 추가되면 다음 열이 포함됩니다.

* **아이콘** - 목록에서 쉽게 식별할 수 있는 탭의 구성 요소 유형의 아이콘입니다. 마우스를 놓으면 전체 구성 요소 이름이 툴팁으로 표시됩니다.
* **설명** - 탭의 텍스트로 사용된 설명으로서, 탭에 대해 선택된 구성 요소의 이름을 기본값으로 지정합니다.
* **삭제** - 탭 구성 요소에서 탭을 탭하려면 탭하거나 클릭합니다.
* **순서 변경** - 탭하거나 클릭하고 드래그하여 탭합니다.

### 속성 탭 {#properties-tab}

![](assets/screen-shot-2019-08-29-12.01.57.png)

**속성** 탭에서 컨텐츠 작성자는 슬라이드를 자동으로 전환하도록 설정할 수 있습니다.

* **슬라이드 자동 전환** - 활성화된 경우 지정된 지연 후 구성 요소가 다음 슬라이드로 자동 이동합니다.
* **전환 지연** - 슬라이드를 자동으로 전환할 때 이 값은 전환 사이의 지연 (밀리초 단위) 를 정의하는 데 사용됩니다.
* **마우스를 가리키면** 자동 일시 중지 **비활성화 - 슬라이드를** 자동으로 전환할 때 커서가 회전판에 커서로 표시될 때마다 회전식 전환이 자동으로 일시 중단됩니다. 전환이 일시 정지되지 않도록 이 옵션을 선택합니다.

>[!NOTE]
>
>편집 모드에서는 슬라이드 고급 컨트롤이 **활성화되지** 않습니다. 게시된 컨텐츠의 판독기로 회전판과 상호 작용하려면 [**미리 보기** 모드](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html) **[또는 게시됨으로](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html)** 보기를 사용합니다.
>
>편집 모드에서는 자동 완성 기능이 **활성화되지** 않습니다. 게시된 **[컨텐츠로 보기를](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html)** 사용하여 게시된 컨텐츠의 독자로 자동 고급 기능을 확인합니다.

### 액세스 가능성 탭 {#accessibility-tab}

![](assets/screen-shot-2019-08-29-12.02.22.png)

**액세서빌러티** 탭에서 구성 요소의 [ARIA 액세서빌러티](https://www.w3.org/WAI/standards-guidelines/aria/) 레이블에 대해 값을 설정할 수 있습니다.

* **label** - 구성 요소에 대한 aria 레이블 속성의 값

## Select Panel {#select-panel}

컨텐츠 작성자는 구성 요소 도구 모음의 패널 **선택** 옵션을 사용하여 편집을 위해 다른 슬라이드로 변경할 수 있을 뿐만 아니라 슬라이드 순서를 손쉽게 재정렬할 수 있습니다.

![](assets/screenshot_2018-10-11at165417.png)

구성 요소 **도구 모음에서 선택 패널** 옵션을 선택하면 구성된 슬라이드가 드롭다운으로 표시됩니다.

* 목록은 슬라이드의 지정된 배열로 순서가 지정되며 번호 매기기에 반영됩니다.
* 먼저 슬라이드의 구성 요소 유형이 표시되고 그 뒤에 연한 글꼴로 슬라이드의 설명이 표시됩니다.

![](assets/opera_snapshot_2018-11-28141537localhost.png)

* 드롭다운에서 항목을 탭하거나 클릭하면 편집기의 보기를 해당 슬라이드로 전환합니다.
* 드래그하는 핸들을 사용하여 즉석에서 슬라이드를 다시 정렬할 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 사용하여 슬라이드 구성 요소에 슬라이드로 추가할 수 있는 구성 요소를 정의할 수 있을 뿐만 아니라 자동 전환 기본값 및 컨텐츠 작성자가 사용할 수 있는 사용자 지정 스타일을 정의할 수 있습니다.

### 속성 탭 {#properties-tab-1}

**속성** 탭은 컨텐츠 작성자가 페이지에 회전식 구성 요소를 추가할 때 슬라이드 전환에 대한 기본 설정을 정의하는 데 사용됩니다.

![](assets/screenshot_2018-11-28at141824.png)

* **슬라이드 자동 전환** - 컨텐츠 작성자가 회전식 구성 요소를 페이지에 추가할 때 기본적으로 다음 슬라이드로 회전판을 이동하는 옵션을 정의합니다.
* **전환 지연** - 컨텐츠 작성자가 페이지에 회전식 구성 요소를 추가하면 전환 지연 기본값 (밀리초 단위) 를 정의합니다.
* **마우스로 가리킨 자리에서** 일시 중지 비활성화 - 컨텐츠 작성자에 의해 슬라이드를 자동으로 전환할 때 **자동 슬라이드 일시 정지를 비활성화할 수 있는 옵션이 기본적으로** 활성화되어 있는지 정의합니다.

### 허용된 구성 요소 탭 {#allowed-components-tab}

**허용된 구성 요소** 탭은 컨텐츠 작성자가 캐러셀 구성 요소에 슬라이드로 추가할 수 있는 구성 요소를 정의하는 데 사용됩니다.

허용된 구성 요소 탭은 템플릿 편집기에서 레이아웃 컨테이너의 정책 및 속성을 [정의할 때 동일한 이름의 탭과 동일한 방식으로 작동합니다.](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)

### 스타일 탭 {#styles-tab}

회전판 구성 요소는 AEM [스타일 시스템을 지원합니다](authoring.md#component-styling).

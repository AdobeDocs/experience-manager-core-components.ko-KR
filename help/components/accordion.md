---
title: 아코디언 구성 요소
description: 핵심 구성 요소의 아코디언 구성 요소를 통해 페이지에서 아코디언으로 배열되는 패널 컬렉션을 만들 수 있습니다.
role: Architect, Developer, Admin, User
exl-id: 1deb570a-3d8d-409e-805f-8460c49cf9bb
source-git-commit: 888719359f9a1d1c9dccff97fb639b332f2be54c
workflow-type: ht
source-wordcount: '1063'
ht-degree: 100%

---

# 아코디언 구성 요소{#accordion-component}

핵심 구성 요소의 아코디언 구성 요소를 통해 페이지에서 아코디언으로 배열되는 패널 컬렉션을 만들 수 있습니다.

## 사용량 {#usage}

핵심 구성 요소의 아코디언 구성 요소를 통해 패널로 구성되고 페이지에서 아코디언으로 배열되는 구성 요소 컬렉션을 만들 수 있습니다. 이는 [탭 구성 요소](tabs.md)와 유사하지만 패널을 확장 및 축소할 수 있습니다.

* [구성 대화 상자](#configure-dialog)에서 아코디언 구성 요소의 속성을 정의할 수 있습니다.
* 구성 대화 상자와 [패널 선택 팝오버](#select-panel-popover)에서 아코디언의 패널 순서를 정의할 수 있습니다.
* 구성 요소를 페이지에 추가하는 경우 [디자인 대화 상자](#design-dialog)에서 아코디언 구성 요소의 기본값을 정의할 수 있습니다.

## 패널로 딥 링크하기 {#deep-linking}

아코디언 및 [탭 구성 요소](tabs.md)는 구성 요소에서 패널로 직접 링크하기를 지원합니다.

이를 위해 진행되는 작업:

1. 페이지 편집기의 **[게시로 보기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)**&#x200B;옵션을 사용하여 구성 요소와 함께 페이지를 조회합니다.
1. 페이지 콘텐츠를 검사하고 패널의 ID를 식별합니다.
   * 예 `id="accordion-86196c94d3-item-ca319dbb0b"`
1. ID는 해시로 URL에 추가될 수 있는 앵커가 됩니다(`#`).
   * 예 `https://wknd.site/content/wknd/language-masters/en/magazine/western-australia.html#accordion-86196c94d3-item-ca319dbb0b`

패널 ID를 앵커로 사용하여 URL로 이동하면 브라우저는 특정 구성 요소로 바로 스크롤하고 지정 패널을 표시합니다. 패널 확장이 기본 구성되어 있지 않으면 패널은 자동으로 확장됩니다.

## 버전 및 호환성 {#version-and-compatibility}

현재 버전의 아코디언 구성 요소는 2019년 6월 핵심 구성 요소 릴리스 2.5.0과 함께 도입된 v1입니다. 이 문서에서는 해당 구성 요소에 대해 설명합니다.

다음 표에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md)을 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

아코디언 구성 요소를 경험하고 구성 옵션의 샘플뿐만 아니라 HTML 및 JSON 출력을 확인하려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_accordion_kr)를 참조하십시오.

## 기술 세부 사항 {#technical-details}

아코디언 구성 요소에 대한 최신 기술 설명서는[ GitHub에서 확인할 수 있습니다](https://adobe.com/go/aem_cmp_tech_accordion_v1_kr).

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

콘텐츠 작성자는 구성 대화 상자를 통해 아코디언 항목, 패널과 방문자를 위한 페이지 작동 및 표시 방법을 정의할 수 있습니다.

### 항목 탭 {#items-tab}

![아코디언 구성 요소의 편집 대화 상자 항목 탭](/help/assets/accordion-edit-items.png)

**추가** 버튼을 사용하여 패널로 추가할 구성 요소를 선택하는 구성 요소 선택기를 엽니다. 추가되면 다음 열이 포함된 목록에 항목을 추가합니다.

* **아이콘** - 목록에서 간단히 식별할 수 있는 패널 구성 요소 유형의 아이콘. 마우스를 가져가 툴팁으로 전체 구성 요소 이름을 조회합니다.
* **설명** - 패널 텍스트로 사용되는 설명, 패널에 선택된 구성 요소 이름을 기본값으로 설정.
* **삭제** - 탭하거나 클릭하여 아코디언 구성 요소에서 패널을 삭제합니다.
* **재배열** - 탭하거나 클릭하고 드래그하여 패널의 순서를 재배열합니다.

>[!TIP]
>
>페이지 뷰포트가 작아져 편집 대화 상자가 전체 화면이 되면 **추가** 버튼이 표시되지 않습니다. [구성 요소 브라우저를 드래그하여 페이지 편집기의 아코디언 구성 요소에 드롭하여](https://helpx.adobe.com/kr/experience-manager/6-5/sites/authoring/using/editing-content.html#InsertingaComponent) 구성 요소를 아코디언 구성 요소에 추가할 수 있습니다.

### 속성 탭 {#properties-tab}

![아코디언 구성 요소의 편집 대화 상자 속성 탭](/help/assets/accordion-edit-properties.png)

* **단일 항목 확장** - 선택되면 이 옵션은 한 번에 단일 아코디언 항목을 강제 확장시킵니다. 한 개의 항목이 확장되면 다른 모든 항목은 축소됩니다.
* **확장된 항목** -페이지가 로드되면 이 옵션은 기본적으로 확장된 항목을 정의합니다.
   * **단일 항목 확장**&#x200B;이 선택되면 한 개의 패널을 선택해야 합니다. 기본적으로 첫 번째 패널을 선택합니다.
   * **단일 항목 확장** 이 선택되지 않으면 이 옵션을 다중 선택합니다(선택 사항).
* **ID** - 이 옵션을 통해 HTML과 [데이터 레이어](/help/developing/data-layer/overview.md)에서 구성 요소의 고유 식별자를 제어할 수 있습니다.
   * 비워 두면 고유 ID는 자동으로 생성되고 결과 페이지 검사를 통해 발견될 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID가 변경되면 CSS, JS 및 데이터 레이어 추적에 영향을 미칠 수 있습니다.

## 패널 선택 팝오버 {#select-panel-popover}

콘텐츠 작성자는 구성 요소 툴바의 **패널 선택** 옵션을 사용하여 다른 패널 편집을 변경하고 아코디언으로 패널 순서를 간단히 재배열할 수 있습니다.

![패널 선택 아이콘](/help/assets/select-panel-icon.png)

구성 요소 툴바에서 **패널 선택** 옵션을 선택하면 구성된 아코디언 패널이 드롭다운으로 표시됩니다.

![패널 선택 팝오버](/help/assets/select-panel-popover.png)

* 할당된 패널 배열로 목록 순서가 변경되고 번호 매기기에 반영됩니다.
* 먼저 패널의 구성 요소 유형을 표시한 다음 더 밝은 글꼴로 패널에 대한 설명을 표시합니다.
* 드롭다운의 항목을 탭하거나 클릭하여 편집기의 보기를 해당 패널로 전환합니다.
* 드래그 핸들러를 사용하여 패널을 제대로 재배열할 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 통해 아코디언 구성 요소를 사용하는 콘텐츠 작성자에게 제공되는 옵션을 정의할 수 있습니다. 그리고 아코디언 구성 요소가 배치되면 기본값이 설정됩니다.

### 속성 탭 {#properties-tab-design}

![디자인 대화 상자 속성 탭](/help/assets/accordion-design-properties.png)

* **허용된 제목 요소** - 이 다중 선택 드롭다운은 작성자가 선택해야 할 아코디언 항목 제목 HTML 요소를 정의합니다.
* **기본 제목 요소** - 이 다중 선택 드롭다운은 기본 아코디언 항목 제목 HTML 요소를 정의합니다.

### 허용된 구성 요소 탭 {#allowed-components-tab}

콘텐츠 작성자는 **허용된 구성 요소**&#x200B;를 통해 항목으로 아코디언 구성 요소의 패널에 추가 가능한 구성 요소를 정의할 수 있습니다.

[템플릿 편집기의 레이아웃 컨테이너 정책 및 속성을 정의하는 경우](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html#editing-a-template-layout-template-author) 허용된 구성 탭은 동일한 이름의 탭과 동일한 방식으로 작동합니다.

### 스타일 탭 {#styles-tab}

아코디언 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

## Adobe 클라이언트 데이터 레이어 {#data-layer}

아코디언 구성 요소는 [ Adobe 클라이언트 데이터 레이어](/help/developing/data-layer/overview.md)지원합니다.

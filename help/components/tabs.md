---
title: 탭 구성 요소
description: 탭 구성 요소를 사용하여 페이지에서 콘텐츠를 정렬할 수 있는 여러 탭을 만들 수 있습니다.
role: Architect, Developer, Admin, User
exl-id: 0031c5f3-447c-4932-898f-2f453801e492
source-git-commit: 9767a3a10cb9a77f385edc0ac3fb00096c0087af
workflow-type: ht
source-wordcount: '1032'
ht-degree: 100%

---

# 탭 구성 요소 {#tabs-component}

핵심 구성 요소의 탭 구성 요소를 사용하여 콘텐츠를 여러 탭으로 구성할 수 있습니다.

## 사용량 {#usage}

콘텐츠 작성자는 탭 구성 요소를 통해 여러 탭에서 페이지 콘텐츠를 구성할 수 있습니다.

콘텐츠 작성자는 [편집 대화 상자](#edit-dialog)를 통해 여러 탭을 정의하고 활성 탭을 설정할 수 있습니다. 템플릿 작성자는 [디자인 대화 상자](#design-dialog)를 통해 탭에 추가될 수 있는 구성 요소를 정의하고 스타일을 맞춤화할 수 있습니다.

>[!TIP]
>
>중첩된 탭 구성 요소(탭 내부의 탭)를 지원합니다.
>
>[콘텐츠 트리](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html#content-tree)를 통해 간단한(중첩되지 않은) 탭 구성 요소를 배치/선택할 수 있지만 중첩된 탭은 그럴 수 없습니다.

## 버전 및 호환성 {#version-and-compatibility}

현재 버전의 탭 구성 요소는 2019년 10월 핵심 구성 요소 릴리스 2.2.0과 함께 도입된 v1입니다. 이 문서에서는 해당 구성 요소에 대해 설명합니다.

다음 표에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | 호환 가능 <br>[2.17.4](/help/versions.md) 및 이전 릴리스 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md)을 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

탭 구성 요소를 경험하고 구성 옵션의 샘플뿐만 아니라 HTML 및 JSON 출력을 확인하려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_tabs_kr)를 참조하십시오.

### 기술 세부 사항 {#technical-details}

탭 구성 요소에 대한 최신 기술 설명서는[ GitHub에서 확인할 수 있습니다](https://adobe.com/go/aem_cmp_tech_tabs_v1_kr).

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

## 패널로 딥 링크하기 {#deep-linking}

탭 및 [아코디언 구성 요소](accordion.md)는 구성 요소에서 패널로 직접 링크하기를 지원합니다.

이를 위해 진행되는 작업:

1. 페이지 편집기의 **[게시로 보기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)**&#x200B;옵션을 사용하여 구성 요소와 함께 페이지를 조회합니다.
1. 페이지 콘텐츠를 검사하고 패널의 ID를 식별합니다.
   * 예 `id="accordion-86196c94d3-item-ca319dbb0b"`
1. ID는 해시로 URL에 추가될 수 있는 앵커가 됩니다(`#`).
   * 예 `https://wknd.site/content/wknd/language-masters/en/magazine/western-australia.html#accordion-86196c94d3-item-ca319dbb0b`

패널 ID를 앵커로 사용하여 URL로 이동하면 브라우저는 특정 구성 요소로 바로 스크롤하고 지정 패널을 표시합니다. 패널 확장이 기본 구성되어 있지 않으면 패널은 자동으로 확장됩니다.

## 편집 대화 상자 {#edit-dialog}

콘텐츠 작성자는 편집 대화 상자를 통해 탭을 만들고, 이름을 바꾸고 배열할 수 있을 뿐만 아니라 활성 탭을 정의할 수 있습니다.

### 항목 탭 {#items-tab}

![탭 구성 요소의 편집 대화 상자 항목 탭](/help/assets/tabs-edit-items.png)

**추가** 버튼을 사용하여 탭으로 추가할 구성 요소를 선택하는 구성 요소 선택기를 엽니다. 추가되면 다음 열이 포함된 목록에 항목을 추가합니다.

* **아이콘** - 목록에서 간단히 식별할 수 있는 탭 구성 요소 유형의 아이콘. 마우스를 가져가 툴팁으로 전체 구성 요소 이름을 조회합니다.
* **설명** - 탭 텍스트로 사용되는 설명, 탭에 선택된 구성 요소 이름을 기본값으로 설정.
* **삭제** - 탭하거나 클릭하여 탭 구성 요소에서 탭을 삭제합니다.
* **재배열** - 탭하거나 클릭하고 드래그하여 탭의 순서를 재배열합니다.

>[!TIP]
>
>페이지 뷰포트가 작아져 편집 대화 상자가 전체 화면이 되면 **추가** 버튼이 표시되지 않습니다. [구성 요소 브라우저를 드래그하여 페이지 편집기의 탭 구성 요소에 드롭하여](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#inserting-a-component) 구성 요소를 탭 구성 요소에 추가할 수 있습니다.

### 속성 탭 {#properties-tab}

![탭 구성 요소의 편집 대화 상자 속성 탭](/help/assets/tabs-edit-properties.png)

* **활성 항목** - 콘텐츠 작성자는 페이지 로드 시 활성화된 탭을 정의할 수 있습니다.
   * **기본** 옵션을 사용하여 첫 번째 탭을 선택합니다.
* **ID** - 이 옵션을 통해 HTML과 [데이터 레이어](/help/developing/data-layer/overview.md)에서 구성 요소의 고유 식별자를 제어할 수 있습니다.
   * 비워 두면 고유 ID는 자동으로 생성되고 결과 페이지 검사를 통해 발견될 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID가 변경되면 CSS, JS 및 데이터 레이어 추적에 영향을 미칠 수 있습니다.

### 접근성 탭 {#accessibility-tab}

![탭 구성 요소의 편집 대화 상자 접근성 탭](/help/assets/tabs-edit-accessibility.png)

**접근성** 탭에서 구성 요소에 대한 [ARIA 접근성](https://www.w3.org/WAI/standards-guidelines/aria/) 라벨 값을 설정할 수 있습니다.

* **라벨** - 구성 요소에 대한 ARIA 라벨 속성 값

## 패널 선택 {#select-panel}

콘텐츠 작성자는 구성 요소 툴바의 **패널 선택** 옵션을 사용하여 다른 패널 편집을 변경하고 탭 순서를 간단히 재배열할 수 있습니다.

![패널 선택 아이콘](/help/assets/select-panel-icon.png)

구성 요소 툴바에서 **패널 선택** 옵션을 선택하면 구성된 탭이 드롭다운으로 표시됩니다.

* 할당된 탭 배열로 목록 순서가 변경되고 번호 매기기에 반영됩니다.
* 먼저 탭의 구성 요소 유형을 표시한 다음 더 밝은 글꼴로 탭에 대한 설명을 표시합니다.

![패널 선택 팝오버](/help/assets/select-panel-popover.png)

* 드롭다운의 항목을 탭하거나 클릭하여 편집기의 보기를 해당 탭으로 전환합니다.
* 드래그 핸들러를 사용하여 탭을 제대로 재배열할 수 있습니다.

>[!NOTE]
>
>**편집** 모드에서 작성자는 탭을 선택할 수 없습니다. **[미리보기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#preview-mode)** 모드나 **[게시로 보기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html#view-as-published)** 옵션을 사용하여 게시된 콘텐츠 판독기와 마찬가지로 탭과 상호 작용합니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 통해 항목으로 탭 구성 요소에 추가 가능한 구성 요소뿐만 아니라 콘텐츠 작성자가 사용할 수 있는 맞춤형 스타일을 정의할 수 있습니다.

### 허용된 구성 요소 탭 {#allowed-components-tab}

콘텐츠 작성자는 **허용된 구성 요소**&#x200B;를 통해 항목으로 탭 구성 요소에 추가 가능한 구성 요소를 정의할 수 있습니다.

[템플릿 편집기의 레이아웃 컨테이너 정책 및 속성을 정의하는 경우](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html) 허용된 구성 탭은 동일한 이름의 탭과 동일한 방식으로 작동합니다.

### 스타일 탭 {#styles-tab}

탭 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

## Adobe 클라이언트 데이터 레이어 {#data-layer}

탭 구성 요소는 [ Adobe 클라이언트 데이터 레이어](/help/developing/data-layer/overview.md)지원합니다.

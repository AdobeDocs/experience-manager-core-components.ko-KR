---
title: 슬라이드 구성 요소
description: 콘텐츠 작성자는 회전하는 슬라이드 구성 요소를 통해 콘텐츠를 제공할 수 있습니다.
role: Architect, Developer, Admin, User
exl-id: 3331214c-a05c-47e1-b54c-fbfd1045bd60
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: ht
source-wordcount: '1317'
ht-degree: 100%

---


# 슬라이드 구성 요소{#carousel-component}

콘텐츠 작성자는 탐색하는 슬라이드 구성 요소를 통해 콘텐츠를 제공할 수 있습니다.

{{traditional-aem}}

## 사용량 {#usage}

콘텐츠 작성자는 회전하는 슬라이드 구성 요소를 통해 콘텐츠를 구성할 수 있습니다.

콘텐츠 작성자는 [편집 대화 상자](#edit-dialog)를 통해 여러 슬라이드를 만들고, 이름 및 순서를 변경할 수 있을 뿐만 아니라 자동 전환을 지연 활성화할 수 있습니다. 템플릿 작성자는 [디자인 대화 상자](#design-dialog)를 통해 슬라이드에 추가될 수 있는 구성 요소를 정의하고, 자동 전환을 활성화하거나 비활성하고 스타일을 맞춤화할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

현재 버전의 슬라이드 구성 요소는 2018년 10월 핵심 구성 요소 릴리스 2.2.0과 함께 도입된 v1입니다. 이 문서에서는 해당 구성 요소에 대해 설명합니다.

다음 테이블에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v1 | <br>[릴리스 2.17.4](/help/versions.md) 및 이전 버전과 호환 가능 | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md)을 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

슬라이드 구성 요소를 경험하고 구성 옵션의 샘플뿐만 아니라 HTML 및 JSON 출력을 확인하려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_carousel_kr)를 참조하십시오.

### 기술 세부 정보 {#technical-details}

슬라이드 구성 요소에 대한 최신 기술 설명서는 [GitHub에서 확인할 수 있습니다](https://adobe.com/go/aem_cmp_tech_carousel_v1_kr).

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

## 패널로 딥 링크하기 {#deep-linking}

캐러셀, [탭](tabs.md) 및 [아코디언 구성 요소](accordion.md)는 구성 요소 내에서 패널로 직접 링크하는 기능을 지원합니다.

이를 위해 진행되는 작업:

1. 페이지 편집기의 **[게시로 보기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=ko#view-as-published)**&#x200B;옵션을 사용하여 구성 요소와 함께 페이지를 조회합니다.
1. 페이지 콘텐츠를 검사하고 패널의 ID를 식별합니다.
   * 예 `id="carousel-bfe4fa6647-item-47f1a7ca67-tabpanel"`
1. ID는 해시로 URL에 추가될 수 있는 앵커가 됩니다(`#`).
   * 예 `https://wknd.site/content/wknd/language-masters/en/magazine/western-australia.html#carousel-bfe4fa6647-item-47f1a7ca67-tabpanel`

패널 ID를 앵커로 사용하여 URL로 이동하면 브라우저는 특정 구성 요소로 바로 스크롤하고 지정 패널을 표시합니다. 패널이 기본적으로 표시되지 않도록 구성되면 패널은 자동으로 스크롤됩니다.

## 슬라이드 및 반응형 디자인 {#responsive-design}

모든 핵심 구성 요소는 완벽하게 반응하도록 설계되어 여러 장치에서 원활한 경험을 보장합니다.

슬라이드 구성 요소와 같은 일부 고급 구성 요소는 모든 상태에서 응답성을 유지하기 위해 구현 프로젝트의 맥락 내에서 특별한 고려 사항이 필요할 수 있습니다. 자세한 내용은 [핵심 구성 요소의 반응형 디자인](/help/responsive.md) 문서를 참조하십시오.

## 편집 대화 상자 {#edit-dialog}

콘텐츠 작성자는 편집 대화 상자를 통해 슬라이드를 추가하고 이름을 바꿀 수 있을 뿐만 아니라 자동 전환 설정을 정의할 수 있습니다.

### 항목 탭 {#items-tab}

![슬라이드 구성 요소의 편집 대화 상자 항목 탭](/help/assets/carousel-edit-items.png)

**추가** 버튼을 사용하여 탭으로 추가할 구성 요소를 선택하는 구성 요소 선택기를 엽니다. 추가되면 다음 열이 포함된 목록에 항목을 추가합니다.

* **아이콘** - 목록에서 간단히 식별할 수 있는 탭 구성 요소 유형의 아이콘. 마우스를 가져가 툴팁으로 전체 구성 요소 이름을 조회합니다.
* **설명** - 탭 텍스트로 사용되는 설명, 탭에 선택된 구성 요소 이름을 기본값으로 설정.
* **삭제** - 탭하거나 클릭하여 탭 구성 요소에서 탭을 삭제합니다.
* **순서 변경** - 탭하거나 클릭하고 드래그하여 탭 순서를 변경합니다.

>[!TIP]
>
>페이지 뷰포트가 작아져 편집 대화 상자가 전체 화면이 되면 **추가** 버튼이 표시되지 않습니다. [슬라이드 요소 브라우저를 드래그하여 페이지 편집기의 탭 구성 요소에 드롭하여](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=ko#inserting-a-component-from-the-components-browser) 구성 요소를 슬라이드 구성 요소에 추가할 수 있습니다.

### 속성 탭 {#properties-tab}

![슬라이드 구성 요소의 편집 대화 상자 속성 탭](/help/assets/carousel-edit-properties.png)

**속성** 탭에서 콘텐츠 작성자는 슬라이드를 설정하여 자동 전환할 수 있습니다.

* **활성 항목** - 콘텐츠 작성자는 페이지 로드 시 활성화된 탭을 정의할 수 있습니다.
* **자동 전환 슬라이드** - 활성화되면 구성 요소는 지정된 지연 후 자동으로 다음 슬라이드로 이동합니다.
* **전환 지연** - 자동 전환 슬라이드가 선택되면 이 값을 사용하여 전환 간 지연(밀리초)을 정의합니다.
* **마우스 오버 시 자동 일시 중지 비활성화** - **자동 전환 슬라이드**&#x200B;가 선택되면 슬라이드에 커서를 가져다 댈 때마다 슬라이드 전환이 자동으로 일시 중단됩니다. 이 옵션을 선택하면 전환이 일시 중단되지 않습니다.
* **ID** - 이 옵션을 통해 HTML과 [데이터 레이어](/help/developing/data-layer/overview.md)에서 구성 요소의 고유 식별자를 제어할 수 있습니다.
   * 비워 두면 고유 ID는 자동으로 생성되고 결과 페이지 검사를 통해 발견될 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID가 변경되면 CSS, JS 및 데이터 레이어 추적에 영향을 미칠 수 있습니다.

>[!NOTE]
>
>**편집** 모드에 있는 경우 슬라이드 이동 컨트롤은 활성화되지 않습니다. [**미리보기** 모드](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=ko#preview-mode)나 **[게시로 보기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=ko#view-as-published)** 옵션을 사용하여 게시된 콘텐츠 판독기와 마찬가지로 슬라이드와 상호 작용합니다.
>
>**편집** 모드에 있는 경우 자동 이동 기능은 활성화되지 않습니다. **[게시로 보기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=ko#view-as-published)** 옵션을 사용하여 게시된 콘텐츠 판독기와 마찬가지로 자동 이동 기능을 확인합니다.

### 접근성 탭 {#accessibility-tab}

![슬라이드 구성 요소의 편집 대화 상자 접근성 탭](/help/assets/carousel-edit-accessibility.png)

**접근성** 탭에서 구성 요소에 대한 [ARIA 접근성](https://www.w3.org/WAI/standards-guidelines/aria/) 라벨 값을 설정할 수 있습니다.

* **레이블** - 캐러셀 콘텐츠를 설명하는 회전 메뉴의 Aria 레이블 속성 값입니다.
* **이전** - 캐러셀 탐색의 이전 버튼 레이블에 대한 Aria 레이블 속성 값입니다.
* **다음** - 캐러셀 탐색의 다음 버튼 레이블에 대한 Aria 레이블 속성 값입니다.
* **재생** - 캐러셀 탐색의 재생 버튼 레이블에 대한 Aria 레이블 속성 값입니다.
* **일시 정지** - 캐러셀 탐색의 일시 정지 버튼 레이블에 대한 Aria 레이블 속성 값입니다.
* **탭 목록** - 캐러셀 탐색의 항목 목록 버튼 레이블에 대한 Aria 레이블 속성 값입니다.
* **항목의 Aria 레이블을 제목으로 설정** - 이 옵션을 선택하면 캐러셀 항목 제목이 Aria 레이블 설명으로 자동 설정됩니다.

## 패널 선택 {#select-panel}

콘텐츠 작성자는 구성 요소 툴바의 **패널 선택** 옵션을 사용하여 다른 슬라이드 편집을 변경하고 슬라이드 순서를 간단히 재배열할 수 있습니다.

![패널 선택 아이콘](/help/assets/select-panel-icon.png)

구성 요소 툴바에서 **패널 선택** 옵션을 선택하면 구성된 슬라이드가 드롭다운으로 표시됩니다.

* 할당된 슬라이드 배열로 목록 순서가 변경되고 번호 매기기에 반영됩니다.
* 먼저 슬라이드의 구성 요소 유형을 표시한 다음 더 밝은 글꼴로 슬라이드에 대한 설명을 표시합니다.

![패널 선택](/help/assets/select-panel-popover.png)

* 드롭다운의 항목을 탭하거나 클릭하여 편집기의 보기를 해당 슬라이드로 전환합니다.
* 드래그 핸들러를 사용하여 슬라이드를 제대로 재배열할 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 통해 슬라이드로 슬라이드 구성 요소에 추가 가능한 구성 요소뿐만 아니라 자동 전환 기본값과 콘텐츠 작성자가 사용할 수 있는 맞춤형 스타일을 정의할 수 있습니다.

### 속성 탭 {#properties-tab-1}

콘텐츠 작성자가 슬라이드 구성 요소를 페이지에 추가하면 **속성** 탭을 사용하여 슬라이드 전환을 위한 기본 설정을 정의할 수 있습니다.

![슬라이드 구성 요소의 디자인 대화 상자](/help/assets/carousel-design.png)

* **자동 전환 슬라이드** - 콘텐츠 작성자가 슬라이드 구성 요소를 페이지에 추가하여 자동으로 슬라이드를 다음 슬라이드로 이동하는 옵션이 활성화되면 정의합니다.
* **앞에 제어 요소 추가** - 이 옵션을 선택하면 접근성을 개선하기 위해 제어 요소가 캐러셀 항목 앞에 배치됩니다.

### 허용된 구성 요소 탭 {#allowed-components-tab}

콘텐츠 작성자는 **허용된 구성 요소**&#x200B;를 통해 슬라이드로 슬라이드 구성 요소에 추가 가능한 구성 요소를 정의할 수 있습니다.

[템플릿 편집기의 레이아웃 컨테이너 정책 및 속성을 정의하는 경우](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=ko) 허용된 구성 요소 탭은 동일한 이름의 탭과 동일한 방식으로 작동합니다.

### 스타일 탭 {#styles-tab}

슬라이드 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

## Adobe 클라이언트 데이터 레이어 {#data-layer}

슬라이드 구성 요소는 [Adobe 클라이언트 데이터 레이어](/help/developing/data-layer/overview.md)지원합니다.

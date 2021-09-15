---
title: 컨테이너 구성 요소
description: 핵심 구성 요소의 컨테이너 구성 요소를 통해 페이지에서 다중 구성 요소의 컨테이너를 만들 수 있습니다.
role: Architect, Developer, Admin, User
exl-id: 53c7190d-44cb-42ff-bc1a-483c7875bcf8
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: ht
source-wordcount: '792'
ht-degree: 100%

---

# 컨테이너 구성 요소{#container-component}

핵심 구성 요소의 컨테이너 구성 요소를 통해 페이지에서 다중 구성 요소의 컨테이너를 만들 수 있습니다.

## 사용량 {#usage}

핵심 구성 요소의 컨테이너 구성 요소를 통해 페이지에서 다중 구성 요소의 컨테이너를 만들 수 있습니다. 그리고 다른 구성 요소를 그룹화라고 일반 스타일 또는 레이아웃을 적용할 수 있습니다.

* [구성 대화 상자](#configure-dialog)에서 컨테이너의 속성을 선택할 수 있습니다.
* 구성 요소를 페이지에 추가하는 경우 [디자인 대화 상자](#design-dialog)에서 컨테이너 구성 요소의 기본값을 정의할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

현재 버전의 컨테이너 구성 요소는 2019년 6월 핵심 구성 요소 릴리스 2.5.0과 함께 도입된 v1입니다. 이 문서에서는 해당 구성 요소에 대해 설명합니다.

다음 표에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md)을 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

컨테이너 구성 요소를 경험하고 구성 옵션의 샘플뿐만 아니라 HTML 및 JSON 출력을 확인하려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_container_kr)를 참조하십시오.

## 기술 세부 사항 {#technical-details}

컨테이너 구성 요소에 대한 최신 기술 설명서는 [GitHub에서 확인할 수 있습니다](https://adobe.com/go/aem_cmp_tech_container_v1_kr).

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

콘텐츠 작성자는 구성 대화 상자를 통해 컨테이너 항목과 방문자를 위한 페이지 작동 및 표시 방법을 정의할 수 있습니다.

![컨테이너 구성 요소의 편집 대화 상자](/help/assets/container-edit.png)

* **레이아웃** - 이 옵션은 컨테이너 구성 요소의 비헤이비어 또는 레이아웃 비헤이비어를 정의합니다.
   * **간소화된** - 컨테이너를 간소화된 구성 요소 컬렉션으로 정의합니다.
   * **반응형 그리드** - 컨테이너를[ AEM 반응형 레이아웃](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html)으로 정의합니다.
* **배경색** - [구성에 따라](#background-tab) 자유 형식의 RGB 값이나 색상 피커를 사용하여 정의할 수 있습니다.
* **배경 이미지** - [구성에 따라](#background-tab) 컨테이너 배경색을 정의합니다.
* **ID** - 이 옵션을 통해 HTML과 [데이터 레이어](/help/developing/data-layer/overview.md)에서 구성 요소의 고유 식별자를 제어할 수 있습니다.
   * 비워 두면 고유 ID는 자동으로 생성되고 결과 페이지 검사를 통해 발견될 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID가 변경되면 CSS, JS 및 데이터 레이어 추적에 영향을 미칠 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 통해 컨테이너 구성 요소를 사용하는 콘텐츠 작성자에게 제공되는 옵션을 정의할 수 있습니다.

### 허용된 구성 요소 탭 {#allowed-components-tab}

콘텐츠 작성자는 **허용된 구성 요소**&#x200B;를 통해 항목으로 컨테이너 구성 요소에 추가 가능한 구성 요소를 정의할 수 있습니다.

[템플릿 편집기의 레이아웃 컨테이너 정책 및 속성을 정의하는 경우](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) 허용된 구성 탭은 동일한 이름의 탭과 동일한 방식으로 작동합니다.

### 기본 구성 요소 탭 {#default-components-tab}

컨테이너에서 특정 에셋 유형이 삭제되면 기본 구성 요소 탭을 사용하여 구성 요소에 추가된 구성 요소를 정의할 수 있습니다. 이는 [페이지 템플릿에서 기본 구성 요소를 정의하는 방법](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)과 매우 유사합니다.

### 반응형 설정 탭 {#responsive-settings-tab}

![컨테이너 구성 요소의 편집 대화 상자 반응형 설정](/help/assets/container-design-responsive.png)

* **열** - 결과 컨테이너 그리드의 열 수를 정의합니다.

### 배경 탭 {#background-tab}

![컨테이너 구성 요소의 편집 대화 상자 배경 탭](/help/assets/container-design-background.png)

* **배경 이미지**
   * **배경 이미지 활성화** - 이 옵션을 선택하여 콘텐츠 작성자는 컨테이너의 배경 이미지를 정의할 수 있습니다.
* **배경색**
   * **배경색 활성화** - 이 옵션을 선택하여 콘텐츠 작성자는 컨테이너의 배경색을 정의할 수 있습니다.
   * **색상 견본만 해당** - 이 옵션을 선택하여 콘텐츠 작성자는 컨테이너 배경색에 대한 사전 정의된 색상 견본을 선택할 수 있습니다.
      * **배경색 활성화**&#x200B;를 선택하는 경우에만 사용할 수 있습니다.
* **허용된 색상 견본** - 사전 정의된 색상에서 콘텐츠 작성자는 컨테이너 배경색을 선택할 수 있습니다.
   * **추가** 버튼을 사용하여 사전 정의된 색상 견본을 추가합니다. 추가되면 다음 열이 포함된 목록에 항목을 추가합니다.
   * **값** - RGB 값을 통해 색상을 수동으로 정의합니다.
      * 색상 피커를 탭하거나 클릭한 다음 개별 RGB 값을 조정하거나 16진수 값을 정의하여 색상을 보다 쉽게 선택합니다.
   * **삭제** - 탭하거나 클릭하여 색상 견본을 삭제합니다.
   * **재배열** - 탭하거나 클릭하고 드래그하여 색상 견본의 순서를 재배열합니다.

### 스타일 탭 {#styles-tab}

컨테이너 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

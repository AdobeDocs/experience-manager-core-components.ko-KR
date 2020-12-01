---
title: 컨테이너 구성 요소
description: 핵심 구성 요소 컨테이너 구성 요소를 사용하면 한 페이지에서 여러 추가 구성 요소에 대한 컨테이너를 만들 수 있습니다.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 2%

---


# 컨테이너 구성 요소{#container-component}

핵심 구성 요소 컨테이너 구성 요소를 사용하면 한 페이지에서 여러 추가 구성 요소에 대한 컨테이너를 만들 수 있습니다.

## 사용량 {#usage}

핵심 구성 요소 컨테이너 구성 요소를 사용하면 한 페이지에서 여러 추가 구성 요소에 대한 컨테이너를 만들 수 있으며 다른 구성 요소를 그룹화하고 공통 스타일 또는 레이아웃을 적용하는 데 사용할 수 있습니다.

* [구성 대화 상자](#configure-dialog)에서 컨테이너의 속성을 선택할 수 있습니다.
* 페이지에 추가할 때 컨테이너 구성 요소의 기본값은 [디자인 대화 상자](#design-dialog)에서 정의할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

컨테이너 구성 요소의 현재 버전은 v1이며, 2019년 6월에 핵심 구성 요소의 릴리스 2.5.0에서 도입되었으며 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전이 호환되는 AEM 버전 및 이전 버전의 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

HTML 및 JSON 출력뿐만 아니라 컨테이너 구성 요소의 구성 옵션 예를 보려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_container)를 방문하십시오.

## 기술 세부 정보 {#technical-details}

컨테이너 구성 요소 [에 대한 최신 기술 문서는 GitHub](https://adobe.com/go/aem_cmp_tech_container_v1)에서 찾을 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)에서 확인할 수 있습니다.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자에서는 컨텐츠 작성자가 컨테이너 항목 및 페이지 방문자에 대해 어떻게 표시되고 작동하는지 정의할 수 있습니다.

![컨테이너 구성 요소의 편집 대화 상자](/help/assets/container-edit.png)

* **레이아웃**  - 이 옵션은 컨테이너 구성 요소의 동작 또는 레이아웃 동작을 정의합니다.
   * **단순**  - 컨테이너를 구성 요소의 간단한 컬렉션으로 정의합니다.
   * **응답형 격자**  - 컨테이너를  [AEM 응답형 레이아웃으로 정의합니다.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html)
* **배경색**  - 구성에  [따라 자유 형식의 RGB 값이나 색상 피커를 사용하여 정의할 수 있습니다.](#background-tab)
* **배경 이미지**  - 구성에   [따라 컨테이너의 배경색을 정의합니다.](#background-tab)
* **ID**  - 이 옵션을 사용하면 HTML과  [데이터 레이어에서 구성 요소의 고유 식별자를 제어할 수 있습니다](/help/developing/data-layer/overview.md).
   * 비워 두면 자동으로 고유 ID가 생성되어 결과 페이지를 검사하여 찾을 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID를 변경하면 CSS, JS 및 데이터 레이어 추적에 영향을 줄 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 사용하여 컨테이너 구성 요소를 사용하는 컨텐츠 작성자가 사용할 수 있는 옵션을 정의할 수 있습니다.

### 허용된 구성 요소 탭 {#allowed-components-tab}

**허용된 구성 요소** 탭은 컨텐츠 작성자가 컨테이너 구성 요소에 항목으로 추가할 수 있는 구성 요소를 정의하는 데 사용됩니다.

허용된 구성 요소 탭은 템플릿 편집기에서 레이아웃 컨테이너의 정책 및 속성을 정의할 때 동일한 이름의 탭과 동일한 방식으로 작동합니다.[](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)

### 기본 구성 요소 탭 {#default-components-tab}

기본 구성 요소 탭은 페이지 템플릿[에서 기본 구성 요소를 정의하는 방법과 유사하게, 특정 자산 유형이 컨테이너에 드롭될 때 구성 요소에 추가되는 구성 요소를 정의하는 데 사용됩니다.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)

### 응답형 설정 탭 {#responsive-settings-tab}

![컨테이너 구성 요소의 디자인 대화 상자의 반응형 설정 탭](/help/assets/container-design-responsive.png)

* **열**  - 결과 컨테이너의 격자에 있는 열 수를 정의합니다.

### 백그라운드 탭 {#background-tab}

![컨테이너 구성 요소의 디자인 대화 상자의 배경 탭](/help/assets/container-design-background.png)

* **배경 이미지**
   * **배경 이미지**  활성화 - 컨텐츠 작성자가 컨테이너에 대한 배경 이미지를 정의할 수 있도록 하려면 이 옵션을 선택합니다.
* **배경색**
   * **배경색**  활성화 - 컨텐츠 작성자가 컨테이너에 대한 배경색을 정의할 수 있도록 하려면 이 옵션을 선택합니다.
   * **견본만**  해당 - 컨텐츠 작성자가 컨테이너 배경색의 사전 정의된 색상 견본에서 선택할 수 있도록 하려면 이 옵션을 선택합니다.
      * **배경색 활성화**&#x200B;를 선택한 경우에만 사용할 수 있습니다.
* **허용된 색상 견본**  - 컨텐츠 작성자가 컨테이너 배경색을 선택할 수 있는 미리 정의된 색상을 정의합니다.
   * **추가** 단추를 사용하여 미리 정의된 색상 견본을 추가합니다. 추가된 항목은 다음 열을 포함하는 목록에 추가됩니다.
   * **값**  - RGB 값을 통해 색상을 수동으로 정의
      * 개별 RGB 값을 조정하거나 16진수 값을 정의하여 색상을 보다 손쉽게 선택하려면 색상 피커를 누르거나 클릭합니다.
   * **삭제**  - 견본을 삭제하려면 탭하거나 클릭합니다.
   * **재배치**  - 색상 견본의 순서를 재정렬하려면 탭하거나 클릭하고 드래그합니다.

### 스타일 탭 {#styles-tab}

컨테이너 구성 요소는 AEM [Style System](/help/get-started/authoring.md#component-styling)을 지원합니다.

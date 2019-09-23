---
title: 컨테이너 구성 요소
seo-title: 컨테이너 구성 요소
description: 'null'
seo-description: 핵심 구성 요소 컨테이너 구성 요소를 사용하면 페이지에 있는 여러 추가 구성 요소에 대한 컨테이너를 만들 수 있습니다.
uuid: ec807de9-f76c-4850-9ece-c3e439a1d626
contentOwner: 사용자
content-type: 참조
topic-tags: authoring
products: SG_EXPERIENCEMANAGER/CORCOMPONENTS-new
discoiquuid: f093f58e-9755-4a4f-803a-ab93a50e6870
translation-type: tm+mt
source-git-commit: 3e2e7a297c6ee1d6c8d092c619df8febdc900e25

---


# 컨테이너 구성 요소{#container-component}

핵심 구성 요소 컨테이너 구성 요소를 사용하면 페이지에 있는 여러 추가 구성 요소에 대한 컨테이너를 만들 수 있습니다.

## 사용량 {#usage}

핵심 구성 요소 컨테이너 구성 요소를 사용하면 한 페이지에서 여러 추가 구성 요소에 대한 컨테이너를 만들 수 있으며 다른 구성 요소를 그룹화하고 공통 스타일 또는 레이아웃을 적용하는 데 사용할 수 있습니다.

* 컨테이너의 속성은 [구성 대화 상자에서](#configure-dialog)선택할 수 있습니다.
* 페이지에 컨테이너 구성 요소를 추가할 때의 기본값은 [디자인 대화 상자에서](#design-dialog)정의할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

컨테이너 구성 요소의 현재 버전은 v1이며, 이 버전은 2019년 6월 핵심 구성 요소 릴리스 2.5.0에서 도입되었으며 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소 버전이 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |---|
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 핵심 구성 요소 [버전을 참조하십시오](versions.md).

## 샘플 구성 요소 출력 {#sample-component-output}

컨테이너 구성 요소뿐만 아니라 구성 옵션 예와 HTML 및 JSON 출력을 보려면 구성 요소 [라이브러리를 참조하십시오](http://opensource.adobe.com/aem-core-wcm-components/library/container.html).

## 기술 정보 {#technical-details}

컨테이너 구성 요소에 대한 최신 기술 문서는 GitHub에서 [찾을 수 있습니다](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/container/v1/container).

핵심 구성 요소 개발에 대한 자세한 내용은 핵심 구성 요소 개발자 [설명서를](developing.md)참조하십시오.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자에서는 컨텐츠 작성자가 컨테이너 항목 및 방문자가 페이지를 방문자에 대해 동작하고 표시되는 방식을 정의할 수 있습니다.

![](assets/screen-shot-2019-06-21-13.59.26.png)

* **레이아웃** - 이 옵션은 컨테이너 구성 요소의 동작 또는 레이아웃 동작을 정의합니다.
   * **단순** - 컨테이너를 간단한 구성 요소 컬렉션으로 정의합니다.
   * **반응형 격자** - 컨테이너를 AEM [반응형 격자로 정의합니다.](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/responsive-layout.html)
* **ID** - 이 옵션을 사용하여 구성 요소에 적용할 HTML ID 속성을 정의합니다.
* **배경색** - 구성에 [따라 자유 형식 RGB 값으로 정의하거나 색상 피커를 사용하여 정의할 수 있습니다.](#background-tab)
* **배경 이미지** - 구성에 [따라 컨테이너의 배경색을 정의합니다.](#background-tab)

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 사용하여 컨테이너 구성 요소를 사용하는 컨텐츠 작성자가 사용할 수 있는 옵션을 정의할 수 있습니다.

### 허용된 구성 요소 탭 {#allowed-components-tab}

허용된 구성 **요소** 탭은 컨텐츠 작성자가 컨테이너 구성 요소에 항목으로 추가할 수 있는 구성 요소를 정의하는 데 사용됩니다.

템플릿 편집기에서 레이아웃 컨테이너의 정책 및 속성을 [정의할 때 허용된 구성 요소 탭은 동일한 이름의 탭과 동일한 방식으로 작동합니다.](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)

### 기본 구성 요소 탭 {#default-components-tab}

기본 구성 요소 탭은 페이지 템플릿에서 [](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html#EditingTemplatesTemplateAuthors)기본 구성 요소를 정의하는 방법과 유사하게, 특정 자산 유형이 컨테이너에 드롭될 때 구성 요소에 추가되는 구성 요소를 정의하는 데 사용됩니다.

### 반응형 설정 탭 {#responsive-settings-tab}

![](assets/screen-shot-2019-06-21-09.33.03.png)

* **열** - 결과 컨테이너의 격자에 있는 열 수를 정의합니다.

### 배경 탭 {#background-tab}

![](assets/screen-shot-2019-06-21-09.42.42.png)

* **배경 이미지**
   * **배경 이미지** 활성화 - 컨텐츠 작성자가 컨테이너에 대한 배경 이미지를 정의할 수 있도록 하려면 이 옵션을 선택합니다.
* **배경색**
   * **배경색** 활성화 - 컨텐츠 작성자가 컨테이너에 대한 배경색을 정의할 수 있도록 하려면 이 옵션을 선택합니다.
   * **견본만** 해당 - 컨텐츠 작성자가 컨테이너 배경색에 대한 미리 정의된 색상 견본에서만 선택할 수 있도록 하려면 이 옵션을 선택합니다.
      * 배경색 **활성화를** 선택한 경우에만 사용 가능
* **허용된 색상** 견본 - 컨텐츠 작성자가 컨테이너 배경색을 선택할 수 있는 미리 정의된 색상을 정의합니다.
   * 추가 **단추를 사용하여** 미리 정의된 색상 견본을 추가합니다. 항목이 추가되면 다음 열이 포함된 항목이 목록에 추가됩니다.
   * **값** - RGB 값을 통해 수동으로 색상 정의
      * 개별 RGB 값을 조정하거나 16진수 값을 정의하여 색상을 보다 손쉽게 선택하려면 색상 피커를 탭하거나 클릭합니다.
   * **삭제** - 견본을 탭하거나 클릭하여 삭제합니다.
   * **재정렬** - 색상 견본의 순서를 재정렬하려면 탭하거나 클릭하고 드래그합니다.

### 스타일 탭 {#styles-tab}

컨테이너 구성 요소는 AEM 스타일 [시스템을 지원합니다](authoring.md#component-styling).

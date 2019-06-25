---
title: 컨테이너 구성 요소
seo-title: 컨테이너 구성 요소
description: 'null'
seo-description: 핵심 구성 요소 컨테이너 구성 요소를 사용하면 페이지에서 여러 추가 구성 요소에 대한 컨테이너를 만들 수 있습니다.
uuid: EC 807 DE 9-F 76 C -4850-9 ECE-C 3 E 439 A 1 D 626
contentOwner: 사용자
content-type: 참조
topic-tags: 저작
products: sg_ Experiencemanager/Corecomponents-new
discoiquuid: F 093 F 58 E -9755-4 A 4 F -803 A-AB 93 A 50 E 6870
translation-type: tm+mt
source-git-commit: 3e2e7a297c6ee1d6c8d092c619df8febdc900e25

---


# Container Component{#container-component}

핵심 구성 요소 컨테이너 구성 요소를 사용하면 페이지에서 여러 추가 구성 요소에 대한 컨테이너를 만들 수 있습니다.

## 사용량 {#usage}

핵심 구성 요소 컨테이너 구성 요소를 사용하면 페이지에서 여러 추가 구성 요소에 대한 컨테이너를 만들 수 있으며, 다른 구성 요소를 그룹화하고 공통 스타일 또는 레이아웃을 적용하는 데 사용할 수 있습니다.

* The container&#39;s properties can be selected in the [configure dialog](#configure-dialog).
* Defaults for the Container Component when adding it to a page can be defined in the [design dialog](#design-dialog).

## Version and Compatibility {#version-and-compatibility}

현재 컨테이너 구성 요소의 버전은 2019 년 6 월에 핵심 구성 요소의 릴리스 2.5.0에서 처음 소개된 v 1 이며, 이 문서에서는 설명합니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서에 대한 링크를 제공합니다.

| 구성 요소 버전 | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |---|
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |

For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

To experience the Container Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/container.html).

## Technical Details {#technical-details}

The latest technical documentation about the Container Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/container/v1/container).

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md).

## Configure Dialog {#configure-dialog}

구성 대화 상자에서는 컨텐츠 작성자가 컨테이너 항목을 정의하고 방문자에 대해 어떻게 행동하고 나타나는지 지정할 수 있습니다.

![](assets/screen-shot-2019-06-21-13.59.26.png)

* **레이아웃** - 이 옵션은 컨테이너 구성 요소의 동작 또는 레이아웃 동작을 정의합니다.
   * **단순** - 간단한 구성 요소로 컨테이너를 정의합니다.
   * **응답형 격자** - 컨테이너를 [AEM 응답형 격자로 정의](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/responsive-layout.html)
* **ID** - 이 옵션을 사용하여 구성 요소에 적용할 HTML ID 속성을 정의합니다.
* **배경색** - 구성에 [따라 자유형 RGB 값 또는 색상 피커를 사용하여 정의 가능](#background-tab)
* **배경 이미지** - 구성에 [따라 컨테이너의 배경색을 정의합니다.](#background-tab)

## Design Dialog {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 사용하여 컨테이너 구성 요소를 사용하는 컨텐츠 작성자가 사용할 수 있는 옵션을 정의할 수 있습니다.

### Allowed Components Tab {#allowed-components-tab}

**허용된 구성 요소** 탭은 컨텐츠 작성자가 컨테이너 구성 요소에 항목으로 추가할 수 있는 구성 요소를 정의하는 데 사용됩니다.

The Allowed Components tab functions in the same way as the tab of the same name when [defining the policy and properties of a Layout Container in the Template Editor.](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)

### Default Components Tab {#default-components-tab}

The Default Components tab is used to define which component is added to the component when a particular asset type is dropped on the container, similar to [how default components are defined on the page template](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html#EditingTemplatesTemplateAuthors).

### Responsive Settings Tab {#responsive-settings-tab}

![](assets/screen-shot-2019-06-21-09.33.03.png)

* **열** - 결과 컨테이너의 격자에 있는 열 수를 정의합니다.

### Background Tab {#background-tab}

![](assets/screen-shot-2019-06-21-09.42.42.png)

* **배경 이미지**
   * **배경 이미지 사용** - 컨텐츠 작성자가 컨테이너의 배경 이미지를 정의할 수 있도록 하려면 이 옵션을 선택합니다.
* **배경색**
   * **배경색 활성화** - 컨텐츠 작성자가 컨테이너의 배경색을 정의할 수 있도록 하려면 이 옵션을 선택합니다.
   * **색상 견본 전용** - 컨텐츠 작성자만 컨테이너 배경색에 대해 사전 정의된 색상 견본에서 선택하도록 하려면 이 옵션을 선택합니다.
      * Only available when **Enable background color** is selected
* **허용되는 색상 견본** - 컨텐츠 작성자가 컨테이너 배경색을 선택할 수 있는 사전 정의된 색상을 정의합니다.
   * Use the **Add** button to add a pre-defined color swatch. 추가된 항목이 목록에 추가되면 다음 열이 포함됩니다.
   * **값** - RGB 값을 통해 수동으로 색상 정의
      * 색상 피커를 탭하거나 클릭하여 개별 RGB 값을 조정하거나 16 진수 값을 정의하여 색상을 보다 쉽게 선택할 수 있습니다.
   * **삭제** - 견본을 삭제하려면 탭하거나 클릭합니다.
   * **재배치** - 탭하거나 클릭하고 드래그하여 견본 순서를 재정렬합니다.

### Styles Tab {#styles-tab}

The Container Component supports the AEM [Style System](authoring.md#component-styling).

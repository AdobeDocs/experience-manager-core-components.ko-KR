---
title: 응용 Forms 코어 구성 요소 - 헤더
description: 응용 Forms 헤더 코어 구성 요소 사용 또는 사용자 지정
role: Architect, Developer, Admin, User
source-git-commit: 7f680eac1da61b55f9d90db6c0842421d03ac1dc
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 7%

---


# 헤더 {#header-adaptive-forms-core-component}

적응형 양식의 헤더 구성 요소는 일반적으로 양식의 제목, 로고 또는 이름을 포함하는 양식 맨 위에 있는 섹션입니다. 헤더에는 양식의 용도에 대한 간단한 설명, 양식을 만든 조직의 이름 또는 양식에 대한 도움말을 위한 연락처 정보 등의 기타 정보도 포함될 수 있습니다. 헤더는 사용자에게 양식 개요를 제공하고 작성하려는 정보에 대한 컨텍스트를 제공하는 데 사용됩니다. 사용자가 양식의 목적과 양식을 올바르게 채우는 방법을 이해하는 데 도움이 되는 데 사용됩니다.

**예**

![](/help/adaptive-forms/assets/header.png)

## 사용 {#reasons-to-use-header}

* **브랜딩**: 헤더를 사용하여 양식을 만든 조직의 로고나 이름을 표시할 수 있으므로 브랜드 인식과 신뢰성을 확립할 수 있습니다.

* **컨텍스트**: 헤더에서는 양식의 용도에 대한 간단한 설명을 제공할 수 있으므로 사용자가 양식이 사용되는 컨텍스트를 이해할 수 있습니다.

* **탐색**: 헤더에는 사용자가 웹 사이트 또는 애플리케이션의 다른 부분으로 이동할 수 있는 링크나 버튼이 포함될 수 있습니다.

* **정보**: 헤더에는 연락처 정보 또는 도움말 리소스에 대한 링크가 포함될 수 있으므로 사용자가 필요한 경우 쉽게 지원을 받을 수 있습니다.

* **사용자 경험**: 헤더는 사용자가 양식 필드에 액세스하고 채울 수 있는 명확하고 직관적인 방법을 제공하여 사용자에게 친숙한 양식을 만드는 데 사용할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

응용 Forms 헤더 코어 구성 요소는 코어 구성 요소 2.0.4의 일부로 2023년 2월에 출시되었습니다. 다음은 지원되는 모든 버전, AEM 호환성 및 해당 설명서에 대한 링크를 보여주는 표입니다.

| 구성 요소 버전 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | 호환 가능 with<br>[릴리스 2.0.4](/help/versions.md) 나중에 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md) 문서.


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->


## 기술 세부 사항 {#technical-details}

응용 Forms 헤더 핵심 구성 요소에 대한 최신 정보를 다음에 대한 기술 문서에서 얻습니다. [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/pageheader/v1/pageheader). 핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md).

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자에서 방문자의 헤더 경험을 쉽게 사용자 지정할 수 있습니다. 또한 원활한 사용자 경험을 위해 헤더 옵션을 쉽게 정의할 수 있습니다.

### 이미지 탭 {#image-tab}

헤더의 이 부분에는 헤더 제목과 이미지가 포함되어 있습니다.

![Imagetab](/help/adaptive-forms/assets/header_image.png)

* **이미지 자산** - 이 옵션을 사용하면 마우스를 드래그하여 놓는 방식으로 이미지와 같은 자산을 삭제할 수 있습니다. 로컬 파일 시스템에서 **찾아보기** 버튼을 클릭합니다. 이미지를 추가한 후 이미지 하단에 세 개의 버튼이 나타납니다. 이미지를 추가한 후 이미지 하단에 세 개의 버튼이 나타납니다.
   * **편집** - 탭하거나 클릭 **편집** 자산 편집기에서 자산의 렌디션을 관리하기 위해.
   * **지우기** - 탭하거나 클릭 **지우기** 현재 선택한 이미지를 선택 취소하려면 선택합니다.
   * **선택** - 탭하거나 클릭 **선택**  자산 폴더에서 다른 이미지를 선택하는 옵션.

* **제목** - 이 옵션은 헤더에 제목을 추가하는 데 사용됩니다. 사전 정의된 텍스트가 대화 상자에 포함되며 사용자가 수정할 수 있습니다.
* **링크 대상** - 폴더를 사용하여 제목을 폴더에 연결할 수 있습니다 **찾아보기** 아이콘.
* **설명** - 설명은 특정 이미지의 용도에 대한 추가 정보나 설명을 제공하는 간단한 텍스트 설명입니다.
* **크기(px)** - 픽셀을 늘리거나 줄임으로써 이미지의 길이와 너비를 조정하는 데 도움이 됩니다.

![accessibilitytab](/help/adaptive-forms/assets/header_accessibility.png)

* **대체 텍스트** - 이 옵션은 시각 장애가 있는 사용자에게 이미지를 설명하는 이미지에 대한 짧고 설명적인 텍스트 대체 요소를 제공하는 텍스트를 입력하는 데 사용됩니다.

* **장식적 이미지** - 이미지가 보조 기술에서 무시되어 대체 텍스트가 필요한지 확인합니다. 이는 장식적 이미지에만 적용됩니다.

### 텍스트 탭 {#text-tab}

이 섹션에서는 헤더에 포함할 텍스트를 입력할 수 있습니다.

## 디자인 대화 상자 {#design-dialog}



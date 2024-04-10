---
title: 적응형 양식 핵심 구성 요소 - 헤더
description: 적응형 양식 헤더 핵심 구성 요소를 사용 또는 사용자 정의합니다.
role: Architect, Developer, Admin, User
exl-id: aa18def9-0bec-4475-8dde-213860621ef5
source-git-commit: e4274194026c3370b52be17171776847374a86b5
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 100%

---

# 헤더 {#header-adaptive-forms-core-component}

적응형 양식의 헤더 구성 요소는 일반적으로 양식의 제목, 로고 또는 이름을 포함하는 양식 상단에 있는 섹션입니다. 헤더에는 양식의 용도에 대한 간략한 설명, 양식을 만든 조직의 이름 또는 양식에 대한 도움을 받을 수 있는 연락처 정보와 같은 기타 정보도 포함될 수 있습니다. 헤더는 사용자에게 양식의 개요를 제공하고 작성하고자 하는 정보에 대한 컨텍스트를 제공하는 데 사용됩니다. 사용자가 양식의 용도와 양식을 올바르게 작성하는 방법을 이해하는 데 도움을 주기 위해 사용됩니다.

**예**

![예](/help/adaptive-forms/assets/header.png)

## 사용 {#reasons-to-use-header}

- **브랜딩**: 헤더를 사용하여 양식을 만든 조직의 로고나 이름을 표시할 수 있으므로 브랜드 인지도와 신뢰성을 확립하는 데 도움이 됩니다.

- **컨텍스트**: 헤더는 양식의 용도에 대한 간략한 설명을 제공하여 사용자가 양식이 사용되는 컨텍스트를 이해하는 데 도움을 줍니다.

- **탐색**: 헤더에는 사용자가 웹 사이트 또는 애플리케이션의 다른 부분으로 이동할 수 있는 링크 또는 버튼이 포함될 수 있습니다.

- **정보**: 헤더에는 연락처 정보 또는 도움말 리소스에 대한 링크가 포함되어 사용자가 필요한 경우 도움을 쉽게 받을 수 있습니다.

- **사용자 경험**: 헤더를 사용하면 사용자가 명확하고 직관적으로 양식 필드에 액세스하고 채울 수 있으므로 양식을 보다 사용자 친화적으로 만들 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

적응형 양식 아코디언 핵심 구성 요소는 Cloud Service의 핵심 구성 요소 2.0.4 및 AEM 6.5.16.0 Forms 이상의 핵심 구성 요소 1.1.12 일부로 2023년 2월에 릴리스되었습니다. 다음 표에서는 지원되는 모든 버전, AEM 호환성 및 해당 문서에 대한 링크를 보여 줍니다.

| 구성 요소 버전 | AEM as a Cloud Service | AEM 6.5.16.0 Forms 이상 |
|---|---|---|
| v1 | <br>[릴리스 2.0.4](/help/adaptive-forms/version.md) 이상 버전과 호환 가능 | <br>[릴리스 1.1.12](/help/adaptive-forms/version.md) 이상과 호환합니다(2.0.0 이전 버전). |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/adaptive-forms/version.md) 문서를 참조하십시오.


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## 기술 세부 정보 {#technical-details}

적응형 양식 헤더 핵심 구성 요소에 대한 최신 정보는 [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/pageheader/v1/pageheader)의 기술 설명서에서 확인할 수 있습니다. 핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 확인하십시오.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자를 사용하여 방문자를 위한 헤더 경험을 손쉽게 사용자 정의할 수 있습니다. 헤더 옵션을 간편하게 정의하여 원활한 사용자 경험을 제공할 수도 있습니다.

### 이미지 탭 {#image-tab}

헤더의 이 부분에는 헤더 제목과 이미지가 포함됩니다.

![이미지 탭](/help/adaptive-forms/assets/header_image.png)

- **이미지 자산** - 이 옵션을 사용하면 마우스 드래그 앤 드롭으로 이미지와 같은 자산을 놓을 수 있습니다. **검색** 버튼을 사용하여 로컬 파일 시스템에서 파일을 업로드할 수도 있습니다. 이미지를 추가하면 이미지 하단에 세 개의 버튼이 나타납니다. 이미지를 추가하면 이미지 하단에 세 개의 버튼이 나타납니다.
   - **편집** - 자산 편집기에서 자산 렌디션을 관리하려면 **편집**&#x200B;을 탭하거나 클릭합니다.
   - **지우기** - 현재 선택된 이미지의 선택을 해제하려면 **지우기**&#x200B;를 탭하거나 클릭합니다.
   - **선택** - 자산 폴더에서 다른 이미지를 선택하려면 **선택**&#x200B;을 탭하거나 클릭합니다.

- **제목** - 이 옵션은 헤더에 제목을 추가하는 데 사용됩니다. 대화 상자에는 사전 정의된 텍스트가 포함되며 사용자는 이를 수정할 수 있습니다.
- **연결 대상** - **검색** 아이콘을 사용하여 제목을 폴더에 연결할 수 있습니다.
- **설명** - 설명은 특정 이미지의 용도에 대한 추가 정보 또는 설명을 제공하는 간단한 텍스트 설명입니다.
- **크기(px)** - 픽셀을 늘리거나 줄여 이미지의 길이와 폭을 조정하는 데 도움이 됩니다.

![접근성 탭](/help/adaptive-forms/assets/header_accessibility.png)

- **대체 텍스트** - 이 옵션은 시각 장애가 있는 사용자에게 이미지를 설명해 주는 이미지에 대한 간단한 대체 텍스트를 제공하는 텍스트를 입력하는 데 사용됩니다.

- **장식적 이미지** - 이미지가 보조 기술에서 무시되어 대체 텍스트가 필요한지 확인합니다. 이는 장식적 이미지에만 적용됩니다.

### 텍스트 탭 {#text-tab}

이 섹션에서는 헤더에 포함할 텍스트를 입력할 수 있습니다.

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## 관련 문서 {#related-articles}

{{more-like-this}}

## 추가 참조 {#see-also}

{{see-also}}

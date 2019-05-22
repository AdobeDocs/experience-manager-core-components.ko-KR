---
title: 핵심 구성 요소로 작성
seo-title: 핵심 구성 요소로 작성
description: AEM에서 구성 요소는 작성되는 페이지의 컨텐츠를 구성하는 구조적 요소입니다. 핵심 구성 요소는 유연하고 기능이 풍부한 작성 기능을 제공합니다.
seo-description: AEM에서 구성 요소는 작성되는 페이지의 컨텐츠를 구성하는 구조적 요소입니다. 핵심 구성 요소는 유연하고 기능이 풍부한 작성 기능을 제공합니다.
uuid: 4 A 54 CD 4 C -3 D 89-4683-8301-BF 1 E 634736 E 3
content-type: 참조
topic-tags: 저작
discoiquuid: 8751 E 490-D 427-44 F 2-B 767-51935 AFDA 988
translation-type: tm+mt
source-git-commit: 632d6abb1f13667cc0457152268d50af3bfabfc4

---


# 핵심 구성 요소를 사용한 저작

Adobe Experience Manager에서 구성 요소는 작성 중인 페이지의 컨텐츠를 구성하는 구조적 요소입니다. 이 섹션에서는 페이지를 만들 때 반드시 필요한 컨텐츠 유형을 제공하는 핵심 구성 요소를 다룹니다.

핵심 구성 요소는 유연하고 기능이 풍부한 작성 기능을 제공합니다. [We. Retail 참조 사이트는](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html) 핵심 구성 요소를 사용할 수 있는 방법을 보여줍니다.

핵심 구성 요소를 경험하고 HTML 및 JSON 출력뿐만 아니라 구성 옵션의 예를 보려면 [구성 요소 라이브러리를 참조하십시오](http://opensource.adobe.com/aem-core-wcm-components/library/content-fragment.html).

>[!NOTE]
>
>작성자는 핵심 구성 요소를 즉시 사용할 수 없으며 [, 개발 팀은 먼저 이러한 구성 요소를 환경에 통합해야](using.md)합니다. 통합되면 [템플릿 편집기를 통해 사용 가능하고 미리 구성할](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)수 있습니다.

>[!CAUTION]
>
>핵심 구성 요소는 [AEM 6.3 이상을 필요로 하며](versions.md) [편집 가능한 템플릿을 사용해야](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)합니다. 클래식 UI와 정적 템플릿에서는 작동하지 않습니다.

## 핵심 구성 요소로 작성 {#authoring-with-core-components}

작성자는 다음과 같은 핵심 구성 요소의 몇 가지 이점을 알 수 있습니다.

* 페이지 편집기와 간편하게 통합 [및 통합](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html)

* We. Retail와 구성 요소 라이브러리에서와 같이 [다양한 사용 사례를 수용할 수](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html) 있는 [기능이 풍부한 기능](http://opensource.adobe.com/aem-core-wcm-components/library/content-fragment.html)

* [템플릿 편집기를](#pre-configuring-core-components) 통해 페이지 작성자가 사용할 수 있는 기능을 정의하는 [사전 구성 가능](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)

* 접근성 가이드라인을 중심으로 [구축](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html)

* [반응형 레이아웃을 지원하도록 구축](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/responsive-layout.html)

구성 요소는 페이지를 편집할 때 페이지 편집기의 사이드 패널의 **구성 요소** 탭에서 사용할 수 [](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html)있습니다.

구성 요소는 구성 요소 그룹이라는 카테고리에 따라 그룹화되어 구성 요소를 쉽게 구성하고 필터링합니다. 구성 요소 그룹 이름은 [구성 요소 브라우저에서](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/editing-content.html) 구성 요소와 함께 표시되며 그룹별로 필터링하여 올바른 구성 요소를 쉽게 찾을 수도 있습니다.

>[!NOTE]
>
>핵심 구성 요소는 기본적으로 숨겨진 그룹의 일부이며 구성 요소 브라우저 내에 표시되지 않습니다.
>
>표시되는 그룹에 필요한 구성 요소를 추가하거나 작성자가 사용할 수 있도록 사용자 정의할 수 있습니다.

## 핵심 구성 요소 사전 구성 {#pre-configuring-core-components}

기본 구성 요소 구성은 개발자의 작업이었습니다. 그러나 템플릿 작성자는 코어 구성 요소를 사용하여 템플릿 편집기를 통해 다양한 기능을 구성할 수 있습니다.

예를 들어 이미지 구성 요소가 파일 시스템에서 이미지 업로드를 허용하지 않거나 텍스트 구성 요소가 특정 단락 포맷만 허용해야 하는 경우 간단한 클릭으로 이러한 기능을 활성화하거나 비활성화할 수 있습니다.

자세한 내용은 [페이지 템플릿](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) 만들기를 참조하십시오.

### 편집 및 디자인 대화 상자 {#edit-and-design-dialogs}

템플릿 작성자는 핵심 구성 요소를 미리 구성하여 템플릿의 일부로 허용된 옵션을 정의하고, 페이지 작성자가 실제 페이지 컨텐츠를 정의하기 위해 추가로 구성할 수 있으므로, 각 구성 요소는 두 개의 서로 다른 대화 상자에서 옵션을 가질 수 있습니다.

|  | 설명 | 컨트롤 기능 | examples |
|--- |--- |--- |--- |
| **편집 대화 상자** | **페이지 작성자가** 배치된 구성 요소에 대한 일반적인 페이지 편집 중에 수정할 수 있는 옵션 | 구성 요소에 의해 표시되는 컨텐츠 및 궁극적으로 페이지에 표시되는 방법. | 컨텐츠 텍스트 서식 지정, 페이지에서 이미지 회전 |
| **디자인 대화 상자** | 템플릿 **작성자가** 페이지 템플릿을 구성할 때 수정할 수 있는 옵션. | 구성 요소를 편집할 때 페이지 작성자가 사용할 수 있는 옵션 | 사용 가능한 텍스트 서식 옵션을 사용할 수 있으며, 어떤 이미지를 즉석 옵션을 사용할 수 있습니다. |

### 구성 요소 스타일 {#component-styling}

대부분의 핵심 구성 요소의 스타일은 AEM 스타일 시스템을 사용하여 정의할 수 있습니다.

* 템플릿 작성자는 해당 구성 요소의 디자인 대화 상자에서 특정 구성 요소에 사용할 수 있는 스타일을 정의할 수 있습니다.
* 컨텐츠 작성자는 구성 요소를 추가하고 컨텐츠를 만들 때 적용할 스타일을 선택할 수 있습니다.

자세한 내용은 [스타일 시스템](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/style-system.html) 설명서를 참조하십시오.

>[!NOTE]
>
>스타일 시스템 기능을 활성화하려면 AEM 6.3, 서비스 팩 2 (6.3.2.0) 이상 버전이 필요합니다.

## 사용 가능한 핵심 구성 요소 목록 {#list-of-core-components-available}

다음은 편집 및 디자인 대화 상자 기능을 자세히 설명하는 페이지에 연결된 사용 가능한 핵심 구성 요소 목록입니다.

핵심 구성 요소의 최신 버전은 다음 구성 요소를 제공합니다.

* [탐색 표시](breadcrumb.md)
* [양식 단추](form-button.md)
* [회전판](carousel.md)
* [양식 컨테이너](form-container.md)
* [컨텐츠 조각](content-fragment-component.md)
* [컨텐츠 조각 목록](content-fragment-list.md)
* [숨겨진 양식](form-hidden.md)
* [양식 옵션](form-options.md)
* [양식 텍스트](form-text.md)
* [이미지](image.md)
* [언어 탐색](language-navigation.md)
* [목록](list.md)
* [탐색](navigation.md)
* [페이지](page.md)
* [빠른 검색](quick-search.md)
* [분리자](separator.md)
* [소셜 미디어 공유](sharing.md)
* [티저](teaser.md)
* [텍스트](text.md)
* [제목](title.md)

>[!CAUTION]
>
>일부 버전의 개별 핵심 구성 요소는 특정 버전의 AEM 와만 호환할 수 있습니다.
>
>자세한 내용은 호환성 정보에 대한 개별 도움말 페이지 (이전 목록에 연결) 를 참조하거나 [핵심 구성 요소 버전](versions.md) 문서를 참조해 보십시오.

>[!NOTE]
>
>사용자 인스턴스에 따라 사용자 요구 사항에 맞게 명시적으로 개발된 구성 요소를 사용자 지정했을 수 있습니다. 이러한 구성 요소는 여기서 설명한 구성 요소 중 일부와 이름이 같을 수도 있습니다.
>양식 코어 구성 요소는 AEM Forms와 관련이 없습니다.

## 개발자 리소스 {#developer-resources}

핵심 [구성 요소에 대한 기술 정보는 핵심 구성 요소](developing.md) 개발자 개발 설명서를 참조하십시오.

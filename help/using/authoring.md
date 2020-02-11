---
title: 핵심 구성 요소로 작성
description: AEM에서 구성 요소는 작성 중인 페이지의 컨텐츠를 구성하는 구조적 요소입니다. 핵심 구성 요소는 유연하고 기능이 풍부한 작성 기능을 제공합니다.
translation-type: tm+mt
source-git-commit: 5439f90faef28c72367419bb7429a3a880b65229

---


# 핵심 구성 요소로 작성

Adobe Experience Manager에서 구성 요소는 작성 중인 페이지의 콘텐츠를 구성하는 구조적 요소입니다.

핵심 구성 요소는 유연하고 기능이 풍부한 작성 기능을 제공합니다. WKND [참조 사이트](https://wknd.site) 및 이 사이트에서는 핵심 구성 요소를 사용하여 리치 웹 사이트 경험을 구현하는 방법을 보여 줍니다.

핵심 구성 요소를 살펴보고 구성 옵션 예와 HTML 및 JSON 출력을 보려면 구성 요소 [라이브러리를 참조하십시오](https://adobe.com/go/aem_cmp_library).

AEM 프로젝트 원형형을 사용하여 AEM 프로젝트에서 핵심 구성 요소를 구현하기 위한 개발자 중심의 심층 소개를 살펴보려면 [WKND](overview.md) 자습서를 [참조하십시오.](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)

>[!NOTE]
>
>작성자는 핵심 구성 요소를 즉시 사용할 수 없습니다. [개발 팀에서 먼저 핵심 구성 요소를 환경에 통합해야 합니다](using.md). Once integrated, they may be made available and pre-configured via the [template editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

>[!CAUTION]
>
>핵심 구성 요소는 [AEM 6.3 이상을](versions.md) 필요로 하며 [편집 가능한 템플릿을](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)사용해야 합니다. 클래식 UI와 정적 템플릿에서는 작동하지 않습니다.

## 핵심 구성 요소로 작성 {#authoring-with-core-components}

작성자는 핵심 구성 요소의 다음과 같은 몇 가지 이점을 알 수 있습니다.

* Simple to use and well-integrated with the [page editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html)

* WKND 참조 사이트 [및 구성 요소 라이브러리에서 설명한 것처럼 다양한](https://wknd.site) 사용 사례를 [수용할 수있는 다양한 기능](https://adobe.com/go/aem_cmp_library)

* [페이지 작성자가](#pre-configuring-core-components) [템플릿 편집기를 통해 사용할 수 있는 기능을 정의하기 위한 사전 구성 가능](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)

* Built around [accessibility guidelines](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html)

* Built to support [responsive layout](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html)

* 간편한 [로컬라이제이션 지원](localization.md)

Components are available on the **Components** tab of the side panel of the page editor when [editing a page](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html).

구성 요소는 구성 요소를 쉽게 구성하고 필터링하기 위해 구성 요소 그룹이라는 범주에 따라 그룹화됩니다. 구성 요소 그룹 이름은 [구성 요소 브라우저의](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html) 구성 요소와 함께 표시되며, 올바른 구성 요소를 쉽게 찾기 위해 그룹별로 필터링할 수도 있습니다.

>[!NOTE]
>
>핵심 구성 요소는 기본적으로 숨겨진 그룹의 일부이며 구성 요소 브라우저 내에 표시되지 않습니다.
>
>보이는 그룹에 필요한 구성 요소를 추가하거나 작성자가 사용할 수 있도록 구성 요소를 사용자 정의합니다.

## 코어 구성 요소 사전 구성 {#pre-configuring-core-components}

기본 구성 요소 구성은 개발자의 작업이었습니다. 하지만 핵심 구성 요소를 사용하면 템플릿 작성자가 템플릿 편집기를 통해 다양한 기능을 구성할 수 있습니다.

예를 들어 이미지 구성 요소가 파일 시스템에서 이미지 업로드를 허용하지 않아야 하거나 텍스트 구성 요소가 특정 단락 서식만 허용해야 하는 경우 간단한 클릭으로 이러한 기능을 활성화하거나 비활성화할 수 있습니다.

자세한 [내용은 페이지 템플릿](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) 만들기를 참조하십시오.

### 편집 및 디자인 대화 상자 {#edit-and-design-dialogs}

템플릿 작성자가 핵심 구성 요소를 미리 구성하여 템플릿의 일부로 허용되는 옵션을 정의한 다음 페이지 작성자가 실제 페이지 컨텐츠를 정의하도록 추가로 구성할 수 있으므로 각 구성 요소에는 서로 다른 두 대화 상자에 옵션이 있을 수 있습니다.

|  | 설명 | 컨트롤 | 예 |
|--- |--- |--- |--- |
| **편집 대화 상자** | 배치된 구성 요소에 대한 일반 페이지 편집 중에 **페이지 작성자가** 수정할 수 있는 옵션 | 구성 요소에 의해 표시되는 컨텐츠와 페이지가 페이지에 표시되는 방식. | 컨텐츠 텍스트의 서식을 지정하고 페이지에서 이미지를 회전할 수 있습니다. |
| **디자인 대화 상자** | 페이지 템플릿을 구성할 때 **템플릿 작성자가** 수정할 수 있는 옵션입니다. | 구성 요소를 편집할 때 페이지 작성자가 사용할 수 있는 옵션 | 사용할 수 있는 텍스트 서식 옵션, 사용할 수 있는 이미지 즉석 옵션 |

### 구성 요소 스타일 {#component-styling}

대부분의 핵심 구성 요소의 스타일은 AEM 스타일 시스템을 사용하여 정의할 수 있습니다.

* 템플릿 작성자는 해당 구성 요소의 디자인 대화 상자에서 특정 구성 요소에 사용할 수 있는 스타일을 정의할 수 있습니다.
* 그런 다음 컨텐츠 작성자는 구성 요소를 추가하고 컨텐츠를 만들 때 적용할 스타일을 선택할 수 있습니다.

자세한 내용은 스타일 시스템 [설명서를](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/style-system.html) 참조하십시오.

>[!NOTE]
>
>스타일 시스템 기능을 활성화하려면 AEM 6.3에서 서비스 팩 2(6.3.2.0) 이상이 필요합니다.

## 사용 가능한 핵심 구성 요소 목록 {#list-of-core-components-available}

다음은 편집 및 디자인 대화 상자 기능을 자세히 설명하는 페이지에 연결된 사용 가능한 핵심 구성 요소 목록입니다.

핵심 구성 요소의 현재 버전은 다음 구성 요소 기능이 있습니다.

* [어코디언](accordion.md)
* [탐색 표시](breadcrumb.md)
* [단추](button.md)
* [컨테이너](container.md)
* [회전판](carousel.md)
* [콘텐츠 조각](content-fragment-component.md)
* [콘텐츠 조각 목록](content-fragment-list.md)
* [다운로드](download.md)
* [포함](embed.md)
* [경험 조각](experience-fragment.md)
* [양식 단추](form-button.md)
* [양식 컨테이너](form-container.md)
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
* [탭](tabs.md)
* [텍스트](text.md)
* [제목](title.md)

>[!CAUTION]
>
>개별 핵심 구성 요소의 일부 버전은 특정 AEM 버전과 호환될 수 있습니다.
>
>특정 구성 요소에 대한 개별 도움말 페이지(이전 목록에 연결됨)에서 호환성 정보를 참조하거나 [핵심 구성 요소 버전](versions.md) 문서에서 자세한 내용을 참조하십시오.

>[!NOTE]
>
>사용자 인스턴스에 따라 사용자 요구 사항에 맞게 명시적으로 개발된 구성 요소를 사용자 지정했을 수 있습니다. 이러한 구성 요소는 여기서 설명한 구성 요소 중 일부와 이름이 같을 수도 있습니다.
>양식 핵심 구성 요소는 AEM Forms와 관련이 없습니다.

## 개발자 리소스 {#developer-resources}

핵심 구성 [요소에 대한](developing.md) 기술 정보는 핵심 구성 요소 개발 개발자 설명서를 참조하십시오.

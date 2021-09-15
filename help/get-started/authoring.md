---
title: 핵심 구성 요소로 작성
description: AEM에서 구성 요소는 작성 중인 페이지의 콘텐츠를 구성하는 구조적 요소이며, 핵심 구성 요소는 유연하고 다양한 작성 기능을 제공합니다.
role: Architect, Developer, Admin, User
exl-id: 56e58303-a178-45ab-b59d-e374c9cf90cf
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: ht
source-wordcount: '764'
ht-degree: 100%

---

# 핵심 구성 요소로 작성합니다.

Adobe Experience Manager에서 구성 요소는 작성 중인 페이지의 콘텐츠를 구성하는 구조적 요소입니다.

핵심 구성 요소는 유연하고 다양한 작성 기능을 제공합니다. [WKND 참조 사이트](https://wknd.site)는 핵심 구성 요소를 사용하여 다양한 웹 사이트 경험을 구현하는 방법을 보여 줍니다.

핵심 구성 요소를 경험하고 구성 옵션의 샘플뿐만 아니라 HTML 및 JSON 출력을 확인하려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_kr)를 참조하십시오.

[AEM Project Archetype](/help/developing/archetype/overview.md)을 사용하여 AEM 프로젝트에서 개발자 중심의 핵심 구성 요소를 구현하려면 [WKND 튜토리얼](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)을 확인하십시오.

>[!NOTE]
>
>작성자는 핵심 구성 요소를 즉시 사용할 수 없습니다. [개발 팀에서 먼저 핵심 구성 요소를 환경에 통합해야 합니다](/help/get-started/using.md). 통합되면 [템플릿 편집기](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)를 통해 사용 및 사전 구성할 수 있습니다.

>[!CAUTION]
>
>구성 요소에는 [AEM 6.4 이상](/help/versions.md) 버전이 필요하고 [편집 가능한 템플릿](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)을 사용해야 합니다. 클래식 UI와 정적 템플릿에서는 작동하지 않습니다.

## 핵심 구성 요소로 작성 {#authoring-with-core-components}

작성자는 다음을 포함하여 핵심 구성 요소의 몇 가지 이점을 알 수 있습니다.

* 간편한 사용 및 [페이지 편집기](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html)와 효율적인 통합

* [WKND 참조 사이트](https://wknd.site)와 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_kr) 설명과 같이 여러 사용 사례에 맞게 구성된 다양한 기능

* 페이지 작성자가 [템플릿 편집기](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)를 통해 사용할 수 있는 기능을 정의하는 [사전에 구성 가능한 옵션](#pre-configuring-core-components)

* [액세스 가능성 가이드라인](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html)을 중심으로 구축

* [응답형 레이아웃](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html)을 지원하도록 구축

* [간단한 현지화](localization.md)을 지원하도록 구축

구성 요소는 [페이지를 편집할 때](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html) 페이지 편집기의 측면 패널에 있는 **구성 요소** 탭에서 사용할 수 있습니다.

구성 요소는 구성 요소 그룹이라는 범주에 따라 그룹화되어 구성 요소를 간단하게 구성하고 필터링할 수 있습니다. 구성 요소 그룹은 [구성 요소 브라우저](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html)의 구성 요소와 함께 표시됩니다. 또한 그룹별로 적합한 구성 요소를 간단히 검색할 수 있습니다.

>[!NOTE]
>
>기본적으로 핵심 구성은 숨겨진 그룹의 일부이며 구성 요소 브라우저에는 표시되지 않습니다.
>
>필수 구성 요소를 시각화 그룹에 추가하거나 작성자가 구성 요소를 사용할 수 있도록 사용자 정의합니다.

## 사전 구성하는 핵심 구성 요소 {#pre-configuring-core-components}

기초 구성 요소 구성은 개발자의 업무입니다. 하지만, 이제 템플릿 작성자는 템플릿 편집기를 통해 핵심 구성 요소로 여러 기능을 구성할 수 있습니다.

예를 들어 이미지 구성 요소를 통해 파일 시스템에서 이미지를 업로드하거나 텍스트 구성 요소를 통해 특정 단락을 지정하는 경우 클릭 한 번으로 이러한 기능을 활성화하거나 비활성화할 수 있습니다.

자세한 내용은 [페이지 템플릿 제작](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)을 참조하십시오.

### 편집 대화 상자 및 디자인 대화 상자 {#edit-and-design-dialogs}

템플릿 작성자가 핵심 구성 요소를 사전 구성하여 템플릿의 일부로 허용된 옵션을 정의한 다음 페이지 작성자가 핵심 구성 요소를 구성하여 실제 페이지 콘텐츠를 정의할 수 있기 때문에 각 구성 요소에는 서로 다른 두 개의 대화 상자 옵션이 있을 수 있습니다.

|  | 설명 | 제어 항목 | 예 |
|--- |--- |--- |--- |
| **편집 대화 상자** | 배치된 구성 요소에 대한 일반 페이지 편집 도중 **페이지 작성자**&#x200B;가 수정할 수 있는 옵션 | 구성 요소에 표시되는 콘텐츠 및 페이지에 최종 표시되는 방법. | 콘텐츠 텍스트 서식을 지정하면서 페이지의 이미지를 회전합니다. |
| **디자인 대화 상자** | 페이지 템플릿 구성 시 **템플릿 작성자**&#x200B;가 수정할 수 있는 옵션 | 구성 요소 편집 시 페이지 작성자가 사용할 수 있는 옵션 | 텍스트 서식 지정 옵션 및 이미지 위치 고정 옵션 사용 가능 |

### 구성 요소 스타일링 {#component-styling}

AEM 스타일 시스템을 통해 추가 핵심 구성 요소의 스타일을 정의합니다.

* 템플릿 작성자는 구성 요소의 디자인 대화 상자에서 특정 구성 요소가 사용할 수 있는 스타일을 정의할 수 있습니다.
* 그런 다음 콘텐츠 작성자는 구성 요소 추가 및 콘텐츠 제작 시 적용되는 스타일을 선택할 수 있습니다.

자세한 내용은 [스타일 시스템](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/style-system.html) 설명서를 참조하십시오.

## 개발자 리소스 {#developer-resources}

핵심 구성 요소에 대한 기술 정보를 보려면 [핵심 구성 요소 개발](/help/developing/overview.md)의 개발자 설명서를 참조하십시오.

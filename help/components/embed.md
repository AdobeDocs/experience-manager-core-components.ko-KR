---
title: 구성 요소 포함
description: 포함 구성 요소를 사용하면 AEM 컨텐츠 페이지에 외부 컨텐츠를 포함할 수 있습니다.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '944'
ht-degree: 2%

---


# 구성 요소 포함{#embed-component}

핵심 구성 요소 포함 구성 요소를 사용하면 AEM 컨텐츠 페이지에 외부 컨텐츠를 포함할 수 있습니다.

## 사용량 {#usage}

핵심 구성 요소 포함 구성 요소를 사용하면 컨텐츠 작성자가 AEM 컨텐츠 페이지에 포함할 선택한 외부 컨텐츠를 정의할 수 있습니다. 또한 포함할 자유형 HTML을 정의하는 옵션이 있습니다.

* 구성 요소의 속성은 [구성 대화 상자](#configure-dialog)에서 정의할 수 있습니다.
* 구성 요소를 페이지에 추가할 때의 기본값은 [디자인 대화 상자](#design-dialog)에서 정의할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

포함 구성 요소의 현재 버전은 v1이며, 2019년 9월 핵심 구성 요소 릴리스 2.7.0에 도입되었으며 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소 버전이 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

구성 옵션과 HTML 및 JSON 출력의 예를 보고 포함 구성 요소를 경험하려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_embed)를 방문하십시오.

## 기술 세부 정보 {#technical-details}

포함 구성 요소 [에 대한 최신 기술 문서는 GitHub](https://adobe.com/go/aem_cmp_tech_embed_v1)에서 찾을 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)에서 확인할 수 있습니다.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자를 사용하면 컨텐츠 작성자가 페이지에 포함할 외부 리소스를 정의할 수 있습니다. 먼저 포함할 리소스 유형을 선택합니다.

* [URL](#url)
* [포함 가능](#embeddable)
* [HTML](#html)

임베드 가능한 각 유형에 대해 광고 **ID**&#x200B;를 정의할 수 있습니다. 이 옵션을 사용하면 HTML 및 [데이터 레이어](/help/developing/data-layer/overview.md)에서 구성 요소의 고유 식별자를 제어할 수 있습니다.

* 비워 두면 자동으로 고유 ID가 생성되며 결과 페이지를 검사하여 찾을 수 있습니다.
* ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
* ID를 변경하면 CSS, JS 및 데이터 레이어 추적에 영향을 줄 수 있습니다.

### URL {#url}

가장 간단한 임베드 방법은 URL입니다. **URL** 필드에 포함할 리소스의 URL을 붙여넣으면 됩니다. 구성 요소가 리소스에 액세스하려고 하며 프로세서 중 하나에서 렌더링할 수 있는 경우 **URL** 필드 아래에 확인 메시지가 표시됩니다. 그렇지 않으면 필드가 오류로 표시됩니다.

포함 구성 요소는 다음 유형의 리소스에 대해 프로세서와 함께 제공됩니다.

* Facebook 게시물, Instagram, SoundCloud, Twitter 및 YouTube를 포함한 [Embed 표준](https://oembed.com/)을 준수하는 리소스
* Pinterest

개발자는 포함 구성 요소의 개발자 설명서에 따라 [에 의해 추가 URL 프로세서를 추가할 수 있습니다.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![URL에 대한 구성 요소의 편집 대화 상자 포함](/help/assets/embed-url.png)

### 포함 가능 {#embeddable}

포함 가능 항목을 사용하면 포함된 리소스를 보다 사용자 지정할 수 있으며, 매개 변수화할 수 있고 추가 정보를 포함할 수 있습니다. 작성자는 미리 구성된 신뢰할 수 있는 포함 가능 항목 중에서 선택할 수 있으며 구성 요소는 기본 제공 가능한 Youtube와 함께 제공됩니다.

**포함 가능** 필드는 사용할 프로세서 유형을 정의합니다. YouTube 임베드 가능한 경우 다음을 정의할 수 있습니다.

* **비디오 ID**  - 포함할 리소스의 YouTube에서 고유한 비디오 ID
* **너비**  - 포함된 비디오의 폭입니다.
* **높이**  - 포함된 비디오의 높이입니다.

다른 포함 파일은 유사한 필드를 제공하며 포함 구성 요소의 개발자 설명서에 따라 [개발자가 정의할 수 있습니다.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![포함 파일에 대한 구성 요소의 편집 대화 상자 포함](/help/assets/embed-embeddable.png)

>[!NOTE]
>페이지 작성자가 사용할 수 있도록 [디자인 대화 상자](#design-dialog)를 통해 템플릿 수준에서 임베드 파일을 활성화해야 합니다.

### HTML {#html}

포함 구성 요소를 사용하여 페이지에 자유 형식 HTML을 추가할 수 있습니다.

![HTML에 대한 구성 요소의 편집 대화 상자 포함](/help/assets/embed-html.png)

>[!NOTE]
>스크립트와 같은 안전하지 않은 태그는 입력한 HTML에서 필터링되며 결과 페이지에서 렌더링되지 않습니다.

#### 보안 {#security}

작성자가 입력할 수 있는 HTML 마크업은 작성자가 관리 권한을 얻을 수 있는 크로스 사이트 스크립팅 공격을 방지하기 위해 보안 목적으로 필터링됩니다.

*일반적으로* 모든 스크립트 및  `style` 요소뿐만 아니라 모든  `on*` 및  `style` 속성이 출력에서 제거됩니다.

그러나 포함 구성 요소는 `/libs/cq/xssprotection/config.xml`에서 찾을 수 있는 AEM 전역 HTML AntiSamy Furishing 프레임워크 필터링 규칙 세트를 따르기 때문에 규칙은 더 복잡합니다. 필요한 경우 개발자가 프로젝트 특정 구성을 위해 이를 오버레이할 수 있습니다.

추가 보안 정보는 Cloud Service 설치로서 ](https://docs.adobe.com/content/help/en/experience-manager-65/developing/introduction/security.html)AEM뿐만 아니라 온-프레미스 설치[AEM 개발자 문서에서 찾을 수 있습니다.[](https://docs.adobe.com/content/help/ko-KR/experience-manager-cloud-service/security/home.html)

>[!NOTE]
>`/libs/cq/xssprotection/config.xml`을(를) 오버레이하여 AntiSamy 위생 프레임워크 규칙을 구성할 수 있지만 이러한 변경 사항은 내장 코어 구성 요소만이 아니라 모든 HTL 및 JSP 동작에 영향을 줍니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 통해 포함 구성 요소를 사용할 때 기본 설정값과 포함 구성 요소를 사용할 컨텐츠 작성자가 사용할 수 있는 옵션을 정의할 수 있습니다.

![구성 요소의 디자인 대화 상자 포함](/help/assets/embed-design.png)

* **URL**  비활성화 - 선택 시 컨텐츠 작성자에  **** 대한 URL 옵션을 비활성화합니다.
* **포함 가능**  비활성화 - 임베드 가능한  **** 프로세서에 상관없이 선택한 경우 컨텐츠 작성자에 대한 포함 가능 옵션을 비활성화합니다.
* **HTML**  비활성화 - 선택 시 컨텐츠 작성자에  **** 대한 HTML 옵션을 비활성화합니다.
* **임베드 가능**  - 임베드 가능 옵션이 활성 상태인 경우 컨텐츠 작성자가 사용할 수 있는 임베드 가능한 프로세서를 정의하는  **** 다중 선택 기능입니다.

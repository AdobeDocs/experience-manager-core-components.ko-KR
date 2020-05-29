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

핵심 구성 요소 포함 구성 요소를 사용하면 컨텐츠 작성자가 AEM 컨텐츠 페이지에 포함할 선택한 외부 컨텐츠를 정의할 수 있습니다. 또한 포함할 자유 형식 HTML을 정의하는 옵션이 있습니다.

* 구성 요소의 속성은 [구성 대화 상자에서 정의할 수 있습니다](#configure-dialog).
* 페이지에 구성 요소를 추가할 때의 구성 요소의 기본값은 [디자인 대화 상자에서 정의할 수 있습니다](#design-dialog).

## 버전 및 호환성 {#version-and-compatibility}

포함 구성 요소의 현재 버전은 v1이며, 2019년 9월에 핵심 구성 요소의 릴리스 2.7.0에서 도입되었으며 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전이 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | 클라우드 서비스로서의 AEM |
|--- |--- |---|---|
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전을 참조하십시오](/help/versions.md).

## 샘플 구성 요소 출력 {#sample-component-output}

구성 옵션과 HTML 및 JSON 출력 예제를 보려면 [구성 요소 라이브러리를 방문하십시오](https://adobe.com/go/aem_cmp_library_embed).

## 기술 세부 정보 {#technical-details}

포함 구성 요소에 대한 최신 기술 문서는 GitHub에서 확인할 [수 있습니다](https://adobe.com/go/aem_cmp_tech_embed_v1).

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서를 참조하십시오](/help/developing/overview.md).

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자에서는 컨텐츠 작성자가 페이지에 포함할 외부 리소스를 정의할 수 있습니다. 먼저 포함할 리소스 유형을 선택합니다.

* [URL](#url)
* [포함 가능](#embeddable)
* [HTML](#html)

임베드 가능한 각 유형에 대해 광고 **ID를 정의할 수 있습니다**. 이 옵션을 사용하면 HTML 및 [데이터 레이어에서 구성 요소의 고유 식별자를 제어할 수 있습니다](/help/developing/data-layer/overview.md).

* 비워 두면 자동으로 고유 ID가 생성되어 결과 페이지를 검사하여 찾을 수 있습니다.
* ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
* ID를 변경하면 CSS, JS 및 데이터 레이어 추적에 영향을 줄 수 있습니다.

### URL {#url}

가장 간단한 임베드는 URL입니다. URL 필드에 포함할 리소스의 URL을 **붙여넣으면 됩니다** . 구성 요소는 리소스에 액세스하려고 하며, 프로세서 중 하나에서 렌더링할 수 있는 경우 **URL** 필드 아래에 확인 메시지가 표시됩니다. 그렇지 않으면 필드가 오류로 표시됩니다.

포함 구성 요소는 다음과 같은 유형의 리소스에 대해 프로세서와 함께 제공됩니다.

* Facebook 게시물, Instagram, [SoundCloud, Twitter 및 YouTube를 비롯한](https://oembed.com/) 내장 표준을 준수하는 리소스
* Pinterest

개발자는 내장 구성 요소의 개발자 설명서를 [따라 추가 URL 프로세서를 추가할 수 있습니다.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![URL에 대한 구성 요소 편집 대화 상자 포함](/help/assets/embed-url.png)

### 포함 가능 {#embeddable}

임베드 가능한 경우 포함된 리소스를 보다 맞춤화하여 매개 변수화할 수 있으며 추가 정보를 포함할 수 있습니다. 작성자는 미리 구성된 신뢰할 수 있는 포함 가능 항목 중에서 선택할 수 있으며 구성 요소는 기본적으로 Youtube 임베드 가능한 구성 요소와 함께 제공됩니다.

임베드 **가능한** 필드는 사용할 프로세서 유형을 정의합니다. YouTube 임베드 가능한 경우 다음을 정의할 수 있습니다.

* **비디오 ID** - 포함할 리소스의 YouTube의 고유 비디오 ID
* **너비** - 포함된 비디오의 너비
* **높이** - 포함된 비디오의 높이

기타 임베드 파일은 유사한 필드를 제공하며 내장 구성 요소의 개발자 설명서를 [따라 개발자가 정의할 수 있습니다.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![포함 가능 파일에 대한 구성 요소 편집 대화 상자 포함](/help/assets/embed-embeddable.png)

>[!NOTE]
>페이지 작성자가 사용할 수 있도록 [ [디자인] 대화 상자를](#design-dialog) 통해 템플릿 수준에서 임베드 파일을 활성화해야 합니다.

### HTML {#html}

포함 구성 요소를 사용하여 페이지에 자유 형식의 HTML을 추가할 수 있습니다.

![HTML용 구성 요소 편집 대화 상자 포함](/help/assets/embed-html.png)

>[!NOTE]
>스크립트와 같은 안전하지 않은 태그는 입력된 HTML에서 필터링되며 결과 페이지에서 렌더링되지 않습니다.

#### 보안 {#security}

작성자가 입력할 수 있는 HTML 마크업은 예를 들어 작성자가 관리 권한을 얻을 수 있는 크로스 사이트 스크립팅 공격을 방지하기 위해 보안 목적으로 필터링됩니다.

*일반적으로* 모든 스크립트 및 `style` 요소뿐만 아니라 모든 `on*` 및 `style` 속성이 출력에서 제거됩니다.

하지만 포함 구성 요소는 AEM의 전역 HTML AntiSamey 위생 프레임워크 필터링 규칙 세트를 따르기 때문에 규칙은 더 복잡합니다. 이 규칙은 다음에 찾을 수 있습니다 `/libs/cq/xssprotection/config.xml`. 필요한 경우 개발자가 프로젝트별 구성에 대해 오버레이할 수 있습니다.

추가 보안 정보는 [AEM 개발자 문서에서 온-프레미스 설치](https://docs.adobe.com/content/help/en/experience-manager-65/developing/introduction/security.html) 및 [AEM과 클라우드 서비스 설치에 대해 참조할 수 있습니다.](https://docs.adobe.com/content/help/ko-KR/experience-manager-cloud-service/security/home.html)

>[!NOTE]
>AntiSamy Furishing 프레임워크 규칙을 오버레이로 구성할 수 있지만 이러한 변경 사항은 내장 코어 구성 요소만이 아니라 모든 HTL 및 JSP 동작에 영향을 줍니다. `/libs/cq/xssprotection/config.xml`

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 사용하여 포함 구성 요소를 사용하는 컨텐츠 작성자에게 사용 가능한 옵션과 내장 구성 요소를 배치할 때 기본값 세트를 정의할 수 있습니다.

![구성 요소의 디자인 대화 상자 포함](/help/assets/embed-design.png)

* **URL** 비활성화 - 선택한 경우 컨텐츠 작성자에 대한 **URL** 옵션을 비활성화합니다.
* **임베드 가능한 프로세서** 비활성화 - 임베드 가능한 **프로세서에 상관없이 선택한 경우 컨텐츠 작성자에 대한 임베드 가능한** 옵션을 비활성화합니다.
* **HTML** 비활성화 - 선택한 경우 컨텐츠 작성자에 **대한** HTML옵션을 비활성화합니다.
* **임베드 가능한 임베드 가능** - 임베드 가능한 **옵션이 활성화된 경우 컨텐츠 작성자가 사용할 수 있는 임베드 가능한 프로세서를 정의하는 다중** 세그먼트입니다.

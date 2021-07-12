---
title: 포함 구성 요소
description: 포함 구성 요소를 사용하면 AEM 컨텐츠 페이지에 외부 컨텐츠를 포함할 수 있습니다.
role: Architect, Developer, Admin, User
exl-id: 985fa304-70a3-4329-957e-76d1832a06f1
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '1341'
ht-degree: 2%

---

# 포함 구성 요소{#embed-component}

핵심 구성 요소 포함 구성 요소를 사용하면 AEM 컨텐츠 페이지에 외부 컨텐츠를 포함할 수 있습니다.

## 사용량 {#usage}

컨텐츠 작성자는 핵심 구성 요소 포함 구성 요소를 사용하여 AEM 컨텐츠 페이지 내에 포함할 선택한 외부 컨텐츠를 정의할 수 있습니다. 또한 포함할 자유 양식 HTML을 정의하는 옵션이 있습니다.

* 구성 요소의 속성은 [구성 대화 상자](#configure-dialog)에서 정의할 수 있습니다.
* 페이지에 구성 요소를 추가할 때 구성 요소의 기본값은 [디자인 대화 상자](#design-dialog)에서 정의할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

포함 구성 요소의 현재 버전은 v1이며, 2019년 9월에 핵심 구성 요소 릴리스 2.7.0에서 도입되었으며, 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전이 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

HTML 및 JSON 출력뿐만 아니라 포함 구성 요소의 구성 옵션에 대한 예를 보려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_embed)를 방문하십시오.

## 기술 세부 정보 {#technical-details}

포함 구성 요소 [에 대한 최신 기술 설명서는 GitHub](https://adobe.com/go/aem_cmp_tech_embed_v1)에 있습니다.

코어 구성 요소 개발에 대한 자세한 내용은 [코어 구성 요소 개발자 설명서](/help/developing/overview.md)에서 확인할 수 있습니다.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자에서는 컨텐츠 작성자가 페이지에 포함할 외부 리소스를 정의할 수 있습니다. 먼저 포함할 리소스 유형을 선택합니다.

* [URL](#url)
* [포함 가능](#embeddable)
* [HTML](#html)

포함 가능한 각 유형에 대해 광고 **ID**&#x200B;를 정의할 수 있습니다. 이 옵션을 사용하면 HTML과 [데이터 레이어](/help/developing/data-layer/overview.md)에서 구성 요소의 고유 식별자를 제어할 수 있습니다.

* 비워 두면 고유 ID가 자동으로 생성되며 결과 페이지를 검사하여 찾을 수 있습니다.
* ID가 지정된 경우 ID가 고유한지 확인하는 것은 작성자의 책임입니다.
* ID를 변경하면 CSS, JS 및 데이터 레이어 추적에 영향을 줄 수 있습니다.

### URL {#url}

가장 간단한 포함 은 URL입니다. **URL** 필드에 포함할 리소스의 URL을 붙여넣으면 됩니다. 구성 요소는 리소스에 액세스를 시도합니다. 이 구성 요소가 프로세서 중 하나에서 렌더링될 수 있는 경우 **URL** 필드 아래에 확인 메시지가 표시됩니다. 그렇지 않으면 필드에 오류가 표시됩니다.

포함 구성 요소는 다음 유형의 리소스에 대해 프로세서와 함께 제공됩니다.

* facebook Post, Instagram, SoundCloud, Twitter 및 YouTube을 포함하여 [Embed standard](https://oembed.com/)을 준수하는 리소스
* Pinterest

개발자는 포함 구성 요소의 개발자 설명서에 따라 [에서 추가 URL 프로세서를 추가할 수 있습니다.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![URL에 대한 포함 구성 요소의 편집 대화 상자](/help/assets/embed-url.png)

### 포함 가능 {#embeddable}

포함 가능 항목을 사용하면 매개 변수화 및 추가 정보를 포함할 수 있는 포함된 리소스를 더 사용자 지정할 수 있습니다. 작성자는 사전 구성된 신뢰할 수 있는 포함 가능 파일에서 선택할 수 있으며 구성 요소는 YouTube 포함 가능 기본 제공 상태로 제공됩니다.

**포함 가능** 필드는 사용할 프로세서 유형을 정의합니다. YouTube 포함 가능한 경우 다음을 정의할 수 있습니다.

* **비디오 ID**  - 포함할 리소스의 YouTube의 고유 비디오 ID입니다
* **너비**  - 포함된 비디오의 폭입니다
* **높이**  - 포함된 비디오의 높이입니다
* **음소거 활성화**  - 이 매개 변수는 기본적으로 비디오가 음소거되어 재생되는지 여부를 지정합니다. 이를 활성화하면 자동 재생이 최신 브라우저에서 작동할 가능성이 높아집니다.
* **자동 재생 활성화**  - 이 매개 변수는 플레이어가 로드될 때 초기 비디오가 자동으로 재생되는지 여부를 지정합니다. 이 옵션은 게시 인스턴스에서만 또는 작성 인스턴스에서 **게시됨으로 보기** 옵션을 사용하는 경우에만 적용됩니다.
* **루프 활성화**  - 단일 비디오의 경우 이 매개 변수는 플레이어가 초기 비디오를 반복적으로 재생해야 하는지 여부를 지정합니다. 재생 목록의 경우 플레이어가 전체 재생 목록을 재생한 다음 첫 번째 비디오에서 다시 시작합니다.
* **인라인 재생 활성화(iOS)**  - 이 매개 변수는 iOS에서 비디오가 HTML5 플레이어에서 인라인(온) 또는 전체 화면(오프)을 재생하는지 여부를 제어합니다.
* **무제한 관련 비디오**  - 이 옵션을 비활성화하면 관련 비디오가 방금 재생된 비디오와 동일한 채널에서 나옵니다. 그렇지 않으면 모든 채널에서 나옵니다.

&quot;enable&quot; 옵션은 [디자인 대화 상자](#design-dialog)를 통해 활성화해야 하며 기본값으로 설정할 수 있습니다.

다른 포함 가능 변수는 유사한 필드를 제공하며 포함 구성 요소의 개발자 설명서에 따라 [개발자가 정의할 수 있습니다.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![포함 구성 요소의 편집 대화 상자 - 포함 가능](/help/assets/embed-embeddable.png)

>[!NOTE]
>포함 가능 항목은 페이지 작성자가 사용할 수 있도록 [디자인 대화 상자](#design-dialog)를 통해 템플릿 수준에서 활성화되어야 합니다.

### HTML {#html}

포함 구성 요소를 사용하여 페이지에 자유 형식 HTML을 추가할 수 있습니다.

![HTML에 대한 포함 구성 요소의 편집 대화 상자](/help/assets/embed-html.png)

>[!NOTE]
>스크립트와 같이 안전하지 않은 태그는 입력한 HTML에서 필터링되며 결과 페이지에서 렌더링되지 않습니다.

#### 보안 {#security}

작성자가 입력할 수 있는 HTML 마크업은 보안 목적으로 필터링되므로 작성자가 관리 권한을 얻을 수 있는 크로스 사이트 스크립팅 공격을 방지할 수 있습니다.

*일반적으로* 모든 스크립트 및  `style` 요소와 모든  `on*` 및  `style` 속성이 출력에서 제거됩니다.

그러나 포함 구성 요소가 AEM 전역 HTML AntiSamy 위생상 프레임워크 필터링 규칙 세트를 따르므로 규칙은 더 복잡합니다. 이러한 규칙은 `/libs/cq/xssprotection/config.xml`에 있습니다. 필요한 경우 개발자가 프로젝트별 구성에 대해 오버레이할 수 있습니다.

추가 보안 정보는 [AEM Developer Documentation for on-premise 설치](https://docs.adobe.com/content/help/en/experience-manager-65/developing/introduction/security.html) 및 [AEM as a Cloud Service 설치에서 찾을 수 있습니다.](https://docs.adobe.com/content/help/ko-KR/experience-manager-cloud-service/security/home.html)

>[!NOTE]
>AntiSamy 위생 프레임워크 규칙은 `/libs/cq/xssprotection/config.xml`을 오버레이하여 구성할 수 있지만 이러한 변경 사항은 포함 코어 구성 요소뿐만 아니라 모든 HTL 및 JSP 동작에 영향을 줍니다.

## 디자인 대화 상자 {#design-dialog}

디자인 대화 상자에서는 템플릿 작성자가 포함 구성 요소를 배치할 때 포함 구성 요소를 사용하고 기본 설정을 사용하는 컨텐츠 작성자가 사용할 수 있는 옵션을 정의할 수 있습니다.

### 포함 가능한 유형 탭 {#embeddable-types-tab}

![구성 요소의 디자인 대화 상자 포함](/help/assets/embed-design.png)

* **URL 비활성화**  - 선택 시 컨텐츠 작성자에  **** 대한 URL 옵션을 비활성화합니다
* **포함 가능 테이블 비활성화**  -  **** 임베디드 가능한 프로세서가 허용되는지의 여부에 관계없이 선택한 경우 컨텐츠 작성자에 대한 Embeddableoption을 비활성화합니다.
* **HTML 비활성화**  -  **** 선택한 경우 컨텐츠 작성자에 대한 HTML 옵션을 비활성화합니다.
* **허용되는 포함 가능**  - Embeddableoption이 활성 상태인 경우, 컨텐츠 작성자가 사용할 수 있는 포함 가능한 프로세서를 정의하는  **** 다중 선택.

### YouTube 탭 {#youtube-tab}

![포함 구성 요소의 디자인 대화 상자의 YouTube 탭](/help/assets/embed-design-youtube.png)

* **음소거 동작 구성 허용**  - YouTube 포함 유형을  **선택한** 경우 컨텐츠 작성자가 구성 요소에서 뮤테이트 활성화 옵션을 구성할 수 있습니다
   * **음소거의 기본값**  - YouTube 포함  **유형** 을 선택한 경우 Enable Muteoption을 자동으로 설정합니다
* **자동 재생 동작 구성 허용**  - YouTube 포함 유형을  **선택한** 경우 컨텐츠 작성자가 구성 요소에서 자동 레이아웃 활성화 를 구성할 수 있습니다
   * **자동 재생 기본값**  - YouTube 포함  **유형** 을 선택하면 자동 레이아웃 사용 을 자동으로 설정합니다.
* **루프 동작 구성 허용**  - YouTube 포함 유형을  **선택한** 경우 컨텐츠 작성자가 구성 요소에서 루프 활성화 옵션을 구성할 수 있습니다
   * **루프**  기본값 - YouTube 포함  **유형을 선택한** 경우 자동으로 루프 활성화 옵션을 설정합니다
* **인라인 재생 구성 허용(iOS)**  - YouTube 포함 유형을 선택한 경우 컨텐츠 작성자가 구성 요소에서  **인라인 재생 활성화(iOS)**  옵션을 구성할 수 있습니다
   * **인라인 재생 기본값(iOS)**  - YouTube 포함 유형을 선택한 경우  **인라인 재생 활성화(iOS)**  옵션을 자동으로 설정합니다
* **인라인 비디오 구성 허용**  - YouTube 포함 유형을 선택한 경우 컨텐츠 작성자가 구성  **요소** 에서 무제한 관련 비디오 옵션을 구성할 수 있습니다
   * **무제한 관련 비디오의 기본값**  - YouTube 포함  **유형을 선택한** 경우 무제한 관련 비디오 옵션을 자동으로 설정합니다.

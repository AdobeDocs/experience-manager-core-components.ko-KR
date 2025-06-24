---
title: 임베드 구성 요소
description: 임베디드 구성 요소를 통해 AEM 콘텐츠 페이지에서 외부 콘텐츠 임베드를 활성화합니다.
role: Architect, Developer, Admin, User
exl-id: 985fa304-70a3-4329-957e-76d1832a06f1
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: tm+mt
source-wordcount: '1343'
ht-degree: 100%

---


# 임베드 구성 요소 {#embed-component}

핵심 구성 요소의 임베디드 구성 요소를 통해 AEM 콘텐츠 페이지에서 외부 콘텐츠를 임베드할 수 있습니다.

{{traditional-aem}}

## 사용량 {#usage}

콘텐츠 작성자는 핵심 구성 요소의 임베디드 구성 요소를 통해 AEM 콘텐츠 페이지 내에 임베드할 외부 콘텐츠를 선택하고 정의할 수 있습니다. 또한, 임베드할 자유 형식의 HTML을 정의하는 옵션이 있습니다.

* [구성 대화 상자](#configure-dialog)에서 구성 요소의 속성을 정의할 수 있습니다.
* 구성 요소를 페이지에 추가하는 경우 [디자인 대화 상자](#design-dialog)에서 구성 요소의 기본값을 정의할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

현재 버전의 임베드 구성 요소는 2022년 2월 핵심 구성 요소 릴리스 2.18.0과 함께 도입된 v2입니다. 이 문서에서는 해당 구성 요소에 대해 설명합니다.

다음 테이블에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |---|---|---|
| v2 | - | 호환 가능 | 호환 가능 | 호환 가능 |
| [v1](v1/embed.md) | 호환 가능 | 호환 가능 | - | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md)을 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

임베드 구성 요소를 경험하고 구성 옵션의 샘플뿐만 아니라 HTML 및 JSON 출력을 확인하려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_embed_kr)를 참조하십시오.

## 기술 세부 정보 {#technical-details}

임베드 구성 요소에 대한 최신 기술 설명서는[ GitHub에서 확인할 수 있습니다](https://adobe.com/go/aem_cmp_tech_embed_v2).

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

콘텐츠 작성자는 구성 대화 상자를 통해 페이지에 임베드할 외부 리소스를 정의할 수 있습니다.

### 속성 탭 {#properties-tab}

우선 임베드해야 할 리소스 유형을 선택합니다.

* [URL](#url)
* [임베드 가능](#embeddable)
* [HTML](#html)

임베드가 가능한 유형의 경우 **ID**&#x200B;를 정의할 수 있습니다. 이 옵션을 통해 HTML과 [데이터 레이어](/help/developing/data-layer/overview.md)에서 구성 요소의 고유 식별자를 제어할 수 있습니다.

* 비워 두면 고유 ID는 자동으로 생성되고 결과 페이지 검사를 통해 발견될 수 있습니다.
* ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
* ID가 변경되면 CSS, JS 및 데이터 레이어 추적에 영향을 미칠 수 있습니다.

#### URL {#url}

가장 단순한 임베드는 URL입니다. 간단히 **URL** 필드에서 임베드하려는 리소스의 URL을 붙여넣습니다. 구성 요소가 리소스 액세스를 시도하고, 프로세서 중 하나에서 구성 요소를 렌더링하는 경우 아래 **URL** 필드에 확인 메시지가 표시됩니다. 그렇지 않으면 필드에 오류가 표시됩니다.

임베드 구성 요소에는 다음 유형의 리소스를 위한 프로세서가 포함됩니다.

* Facebook Post, Instagram, SoundCloud, Twitter 및 YouTube 등 [표준 임베드](https://oembed.com/)를 준수하는 리소스
* Pinterest

개발자는 [임베드 구성 요소의 개발자 설명서에 따라](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component) URL 프로세서를 추가할 수 있습니다.

![URL용 임베드 구성 요소의 편집 대화 상자](/help/assets/embed-url.png)

#### 임베드 가능 {#embeddable}

임베드 가능 항목을 사용하여 임베드된 리소스를 추가로 사용자 정의할 수 있습니다. 해당 리소스는 매개 변수화되고 리소스에 추가 정보가 포함될 수 있습니다. 작성자는 사전 구성된 임베드 가능 항목 중 하나를 선택할 수 있으며, 구성 요소에는 즉시 사용 가능한 YouTube 임베드 가능 항목이 포함됩니다.

**임베드 가능 항목** 필드는 사용하려는 프로세스 유형을 정의합니다. YouTube 임베드 가능 항목의 경우 다음을 정의할 수 있습니다.

* **비디오 ID** - 임베드하려는 리소스의 YouTube 고유 비디오 ID
* **폭** - 임베드된 비디오 폭
* **높이** - 임베드된 비디오 높이
* **음소거 활성화** - 이 매개 변수는 기본적으로 비디오가 음소거를 재생할지 여부를 지정합니다. 음소거가 활성화되면 최신 브라우저의 자동 재생이 작동할 확률이 높아집니다.
* **자동 재생 활성화** - 이 매개 변수는 플레이어가 로드될 때 초기 비디오를 자동으로 재생할지 여부를 지정합니다. 게시 인스턴스 또는 작성 인스턴스의 **게시로 보기** 옵션을 사용하는 경우에만 적용됩니다.
* **루프 활성화** - 단일 비디오의 경우 이 매개 변수는 플레이어가 초기 비디오를 반복적으로 재생할지 여부를 지정합니다. 재생 목록의 경우 플레이어는 전체 재생 목록을 재생한 다음 최초 비디오에서 다시 시작합니다.
* **인라인 재생(iOS) 활성화** - 이 매개 변수는 iOS의 HTML5 플레이어에서 비디오가 인라인(켜짐) 또는 전체 화면(꺼짐)으로 재생될지를 제어합니다.
* **무제한 관련 비디오** - 이 옵션이 비활성화되면 비디오가 바로 재생되기 때문에 관련 비디오는 동일한 채널에서 가져옵니다. 그렇지 않으면 모든 채널에서 가져옵니다.

다른 임베드 가능 항목도 유사 필드를 제공하고 [임베드 구성 요소 개발자 설명서에 따라](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component) 개발자에 의해 정의될 수 있습니다.

![임베드 가능 항목을 위한 임베드 구성 요소의 편집 대화 상자](/help/assets/embed-embeddable.png)

>[!NOTE]
>
>페이지 작성자가 사용할 수 있는 [디자인 대화 상자](#design-dialog)를 통해 템플릿 수준에서 임베드 가능 항목을 활성화해야 합니다.

#### HTML {#html}

임베드 구성 요소를 사용하여 자유 형식의 HTML을 페이지에 추가할 수 있습니다.

![HTML용 임베드 구성 요소의 편집 대화 상자](/help/assets/embed-html.png)

>[!NOTE]
>스크립트와 같은 불안전한 태그는 입력한 HTML에서 필터링되고 결과 페이지에서는 렌더링되지 않습니다.

##### 보안 {#security}

(예로 작성자에게 관리 권한을 부여할 수 있는) 크로스 사이트 스크립팅 공격을 방지하려면 작성자가 보안용으로 입력할 수 있는 HTML 마크업을 필터링합니다.

일반적으로 출력에서 모든 스크립트와 `style` 요소뿐 아니라 모든 `on*` 및 `style` 속성을 제거합니다.

임베드 구성 요소는 AEM의 HTML AntiSamy 정리 프레임워크 필터링 규칙 세트를 준수하기 때문에 전역 규칙은 더 복잡합니다. 해당 규칙 세트는 `/libs/cq/xssprotection/config.xml`에서 확인할 수 있습니다. 필요한 경우 개발자에 의해 프로젝트별 구성에 오버레이될 수 있습니다.

추가 보안 정보는 [AEM 개발자 설명서(온프레미스 설치](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/security.html) 및 [AEM as a Cloud Service 설치](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/security/home.html)용)에서 확인할 수 있습니다.

>[!NOTE]
>
>`/libs/cq/xssprotection/config.xml` 오버레이를 통해 HTML AntiSamy 정리 프레임워크 규칙을 구성할 수 있지만 해당 변경 사항은 핵심 임베드 구성 요소뿐 만 아니라 모든 HTL 및 JSP 비헤이비어에 영향을 줄 수 있습니다.

### 스타일 탭 {#styles-tab-edit}

![임베드 구성 요소의 디자인 대화 상자 스타일 탭](/help/assets/embed-styles.png)

임베드 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

드롭다운을 사용하여 구성 요소에 적용할 스타일을 선택합니다. 편집 대화 상자에서 선택한 항목은 구성 요소 툴바에서 선택한 항목과 동일한 효과를 가집니다.

드롭다운 메뉴를 사용하려면 [디자인 대화 상자](#design-dialog)에서 이 구성 요소에 대한 스타일을 구성해야 합니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 통해 임베드 구성 요소를 사용하는 콘텐츠 작성자에게 제공되는 옵션을 정의할 수 있습니다. 그리고 임베드 구성 요소가 배치되면 기본값이 설정됩니다.

### 임베드 가능 항목 유형 탭 {#embeddable-types-tab}

![임베드 구성 요소의 디자인 대화 상자](/help/assets/embed-design.png)

* **URL 비활성화** - 선택한 경우 콘텐츠 작성자의 **URL** 옵션을 비활성화합니다.
* **임베드 가능 항목 비활성화** - 선택한 경우 허용된 임베드 가능 프로세서에 상관없이 콘텐츠 작성자의 **임베드 가능 항목** 옵션을 비활성화합니다.
* **HTML 비활성화** - 선택한 경우 콘텐츠 작성자의 **HTML** 옵션을 비활성화합니다.
* **허용된 임베드 가능 항목** - **임베드 가능 항목** 옵션이 활성화될 경우 다중 선택으로 콘텐츠 작성자가 사용할 수 있는 임베드 가능 프로세서를 정의합니다.

### YouTube 탭 {#youtube-tab}

![임베드 구성 요소 디자인 대화 상자의 YouTube 탭](/help/assets/embed-design-youtube.png)

* **음소거 비헤이비어 구성 허용** - YouTube 임베드 유형 선택 시 콘텐츠 작성자는 구성 요소에서 **음소거 활성화** 옵션을 구성할 수 있습니다.
   * **음소거의 기본값** - YouTube 임베드 유형 선택 시 **음소거 활성화** 옵션을 자동으로 설정합니다.
* **자동 재생 비헤이비어 구성 허용** - YouTube 임베드 유형 선택 시 콘텐츠 작성자는 구성 요소에서 **자동 재생 활성화** 옵션을 구성할 수 있습니다.
   * **자동 재생의 기본값** - YouTube 임베드 유형 선택 시 **자동 재생 활성화** 옵션을 자동으로 설정합니다.
* **루프 비헤이비어 구성 허용** - YouTube 임베드 유형 선택 시 콘텐츠 작성자는 구성 요소에서 **루프 활성화** 옵션을 구성할 수 있습니다.
   * **루프의 기본값** - YouTube 임베드 유형 선택 시 **루프 활성화** 옵션을 자동으로 설정합니다.
* **인라인 재생(iOS) 구성 허용** - YouTube 임베드 유형 선택 시 콘텐츠 작성자는 구성 요소에서 **인라인 재생(iOS) 활성화** 옵션을 구성할 수 있습니다.
   * **인라인 재생(iOS)의 기본값** - YouTube 임베드 유형 선택 시 **인라인 재생(iOS) 활성화** 옵션을 자동으로 설정합니다.
* **인라인 비디오 구성 허용** - YouTube 임베드 유형 선택 시 콘텐츠 작성자는 구성 요소에서 **무제한 관련 비디오** 옵션을 구성할 수 있습니다.
   * **무제한 관련 비디오의 기본값** - YouTube 임베드 유형 선택 시 **무제한 관련 비디오** 옵션을 자동으로 설정합니다.

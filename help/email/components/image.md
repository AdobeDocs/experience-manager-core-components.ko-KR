---
title: 이메일 이미지 구성 요소
description: 이메일 이미지 구성 요소는 바로 편집 기능이 있는 적응형 이미지 구성 요소입니다.
role: Architect, Developer, Admin, User
exl-id: f5d40047-3082-4edd-a5f6-6ab3e33997f9
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# 이메일 이미지 구성 요소 {#email-image-component}

이메일 이미지 구성 요소는 바로 편집 기능이 있는 적응형 이미지 구성 요소입니다.

## 사용 {#usage}

이메일 이미지 구성 요소에는 페이지 방문자의 소극적 로드와 콘텐츠 작성자의 간단한 드래그 앤 드롭 이미지 배치 및 구성 옵션이 있는 적응형 이미지 선택 기능과 반응형 비헤이비어가 포함됩니다.

* 템플릿 작성자는 [디자인 대화 상자](#design-dialog)에서 이미지 폭 및 추가 설정 옵션을 정의할 수 있습니다.
* 콘텐츠 편집기는 [구성 대화 상자](#configure-dialog)에서 에셋을 업로드하거나 선택할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

현재 버전의 이메일 이미지 구성 요소는 2022년 10월 이메일 핵심 구성 요소 릴리스 x과(와) 함께 도입된 v1입니다. 이 문서에서는 해당 구성 요소에 대해 설명합니다.

다음 표에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 문서 [이메일 핵심 구성 요소 버전](/help/email/versions.md)을 참조하십시오.

## 반응형 기능 {#responsive-features}

이메일 이미지 구성 요소에는 즉시 사용 가능한 강력한 반응형 기능이 제공됩니다. 페이지 템플릿 수준에서 [디자인 대화 상자](#design-dialog)를 사용하여 이미지 에셋의 기본 폭을 정의할 수 있습니다. 브라우저 창의 크기에 따라 이메일 이미지 구성 요소는 올바른 폭을 자동으로 로드하여 표시합니다. 창의 크기가 조정되면 이메일 이미지 구성 요소는 즉시 올바른 이미지 크기를 자동으로 로드합니다. 이메일 이미지 구성 요소가 이미 콘텐츠 로드에 최적화되었기 때문에 구성 요소 개발자는 사용자 정의 미디어 쿼리를 정의하는 데 걱정할 필요가 없습니다.

또한, 이메일 이미지 구성 요소는 소극적 로드를 지원하여 브라우저에 표시될 때까지 실제 이미지 에셋 로드를 지연합니다. 이로써 콘텐츠의 응답성이 향상될 수 있습니다.

>[!TIP]
>
>기본적으로 이메일 이미지 구성 요소는 적응형 이미지 서블릿에 의해 제공됩니다. 작동 방식에 대한 자세한 내용은 [적응형 이미지 서블릿](#adaptive-image-servlet) 문서를 참조하십시오.

## Dynamic Media 지원 {#dynamic-media}

이메일 이미지 구성 요소는 [Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/dynamic-media.html#dynamicmedia) 에셋을 지원합니다. [활성화되면](#design-dialog) 다른 이미지에서와 마찬가지로 이 기능의 간단한 드래그 앤 드롭이나 에셋 브라우저를 통해 Dynamic Media 이미지 에셋을 추가할 수 있습니다. 또한 이미지 수정자, 이미지 사전 설정 및 스마트 자르기를 지원합니다.

이메일 핵심 구성 요소가 내장된 이메일 경험에는 Sensei에서 지원하는 강력한 고성능 크로스 플랫폼 Dynamic Media 이미지 기능이 포함될 수 있습니다.

## SVG 지원 {#svg-support}

이메일 이미지 구성 요소는 확장 가능한 벡터 그래픽(SVG)을 지원합니다.

* DAM에서의 SVG 에셋 드래그 앤 드롭과 로컬 파일 시스템에서의 SVG 파일 업로드를 모두 지원합니다.
* 원본 SVG 파일이 스트리밍됩니다(변환은 건너뜀).
* SVG 이미지의 경우 “스마트 이미지”와 “스마트 크기”를 이미지 모델에서 빈 배열로 설정합니다.

### 보안 {#security}

보안상 이유로 이미지 편집기에서 바로 최초 SVG를 호출하지 않습니다. `<img src=“path-to-component”>`를 통해 호출됩니다. 이렇게 하면 브라우저는 SVG 파일에 임베드된 스크립트를 실행할 수 없습니다.

## 샘플 구성 요소 출력 {#sample-component-output}

이메일 이미지 구성 요소를 경험하고 구성 옵션의 샘플뿐만 아니라 HTML 및 JSON 출력을 확인하려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_email_image_kr)를 참조하십시오.

### 기술 세부 사항 {#technical-details}

이메일 이미지 구성 요소에 대한 최신 기술 설명서는 [GitHub에서 확인할 수 있습니다.](https://adobe.com/go/aem_cmp_tech_email_image_v1_kr)

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

이미지 구성 요소는 [schema.org microdata](https://schema.org)를 지원합니다.

## 구성 대화 상자 {#configure-dialog}

이메일 이미지 구성 요소는 설명 및 기본 속성과 함께 이미지 자체를 정의하는 구성 대화 상자를 제공합니다.

### 에셋 탭 {#asset-tab}

![이메일 이미지 구성 요소의 구성 대화 상자 에셋 탭](/help/email/assets/email-image-configure-asset.png)

* **페이지에서 추천 이미지 상속** 옵션은 [링크된 페이지의 추천 이미지](page.md)를 사용하거나 이미지가 링크되지 않은 경우 현재 페이지의 추천 이미지를 사용합니다.

* **접근성을 위한 그림 설명** 필드에서는 시각 장애인 독자를 위한 이미지 설명을 정의할 수 있습니다.

   * **페이지에서 그림 설명 상속** 옵션은 DAM에 있는 `dc:description` 메타데이터 또는 연결된 에셋이 없는 경우 현재 페이지의 연결된 에셋 값에 대한 대체 설명을 사용합니다.

* **이미지 에셋**
   * [에셋 브라우저](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html)에서 에셋을 삭제하거나 **검색** 옵션을 탭하여 로컬 파일 시스템에서 로드합니다.
   * **지우기**&#x200B;를 탭하거나 클릭하여 현재 선택된 이미지 선택을 해제합니다.
   * **편집**&#x200B;을 탭하거나 클릭하여 에셋 편집기에서 [에셋 렌디션을 관리합니다](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html).

* **그림 설명을 제공하지 않음** 옵션은 이미지가 단순히 장식용이거나 페이지에 추가 정보를 전달하지 않는 경우 화면 판독기와 같은 보조 기술에서 무시되도록 이미지를 표시합니다.

* **소극적 로드 활성화** - 이 옵션은 필요에 따라 로드 없이 모든 이미지 구성 요소를 미리 로드합니다.

### 메타데이터 탭 {#metadata-tab}

![이미지 구성 요소의 구성 대화 상자 메타데이터 탭](/help/email/assets/email-image-configure-metadata.png)

* **사전 설정 유형** - 이는 사용 가능한 이미지 사전 설정 유형, **이미지 사전 설정** 또는 **스마트 자르기** 중 하나를 정의하고, [Dynamic Media 기능](#dynamic-meida)이 활성화되는 경우에만 사용할 수 있습니다.
   * **이미지 사전 설정** - **이미지 사전 설정**&#x200B;의 **사전 설정 유형**&#x200B;이 설정되면 사용 가능한 Dynamic Media 사전 설정을 선택하면서 드롭다운 **이미지 사전 설정**&#x200B;을 사용할 수 있습니다. 선택한 에셋에 대한 사전 설정이 정의되는 경우에만 사용할 수 있습니다.
   * **스마트 자르기** - **스마트 자르기**&#x200B;의 **사전 설정 유형**&#x200B;이 설정되면 선택한 에셋에 대해 사용 가능한 렌디션을 선택하면서 드롭다운 **렌디션**&#x200B;을 사용할 수 있습니다. 선택한 에셋에 대해 렌디션이 정의되는 경우에만 사용할 수 있습니다.
   * **이미지 수정자** - **사전 설정 유형** 선택에 관계없이 명령을 제공하는 추가 Dynamic Media 이미지를 `&`로 구분하여 정의할 수 있습니다.
* **캡션** - 기본적으로 이미지에 대한 추가 정보가 이미지 아래에 표시됩니다.
   * **DAM에서 캡션 다운로드** - 확인 표시가 되어 있으면 이미지의 캡션 텍스트가 DAM의 `dc:title` 메타데이터 값으로 채워집니다. DAM에서 에셋을 선택한 경우에만 사용할 수 있습니다.
   * **팝업으로 캡션 표시** - 확인 표시가 되어 있으면 캡션은 이미지 아래에 표시되지 않고 마우스로 이미지를 가리키면 일부 브라우저에서 팝업으로 표시됩니다.
* **링크** - 이미지를 다른 리소스에 연결합니다.
   * 선택 대화 상자를 통해 다른 AEM 리소스에 연결합니다.
   * AEM 리소스에 연결되지 않은 경우 절대 URL을 입력합니다. 절대 URL이 아닌 URL은 AEM의 상대 URL로 해석됩니다.
   * **새 탭에서 링크 열기** 옵션을 통해 새 브라우저 창에서 링크를 열 수 있습니다.
* **ID** - 이 옵션을 통해 HTML에서 구성 요소의 고유 식별자를 제어할 수 있습니다.
   * 비워 두면 고유 ID는 자동으로 생성되고 결과 페이지 검사를 통해 발견될 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID를 변경하면 CSS에 영향을 줄 수 있습니다.
* **고정 값** - 이 옵션은 이미지의 폭을 픽셀 단위로 정의합니다.
* **사용 가능한 폭으로 이미지 크기 조정** - 이 옵션은 `"width":"100%"` 이미지 스타일 속성에 적용됩니다.

>[!TIP]
>
>**스마트 자르기**&#x200B;와 **이미지 사전 설정**&#x200B;은 함께 수행할 수 없는 옵션입니다. 작성자가 스마트 자르기 렌디션과 함께 이미지 사전 설정을 사용해야 한다면 **이미지 수정자**&#x200B;를 사용해야 합니다.

### 스타일 탭 {#styles-tab-edit}

![이메일 이미지 구성 요소의 편집 대화 상자 스타일 탭](/help/assets/image-configure-styles.png)

이메일 이미지 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

드롭다운을 사용하여 구성 요소에 적용할 스타일을 선택합니다. 편집 대화 상자에서 선택한 항목은 구성 요소 툴바에서 선택한 항목과 동일한 효과를 가집니다.

탭을 사용하려면 [디자인 대화 상자](#design-dialog)에서 이 구성 요소에 대한 스타일을 구성해야 합니다.

## 디자인 대화 상자 {#design-dialog}

### 메인 탭 {#main-tab}

![이미지 구성 요소의 디자인 대화 상자 메인 탭](/help/email/assets/email-image-design-main.png)

* **DM 기능 활성화** - 확인 표시가 되어 있으면 [Dynamic Media 기능](#dynamic-media)을 사용할 수 있습니다.
   * 이 옵션은 환경에서 Dynamic Media가 활성화된 경우에만 표시됩니다.
* **웹 최적화 이미지 활성화** - 선택하면 [웹에 최적화된 이미지 제공 서비스](/help/developing/web-optimized-image-delivery.md)는 WebP 형식으로 이미지를 전달하여 이미지 크기를 평균 25% 줄일 수 있습니다.
   * 이 옵션은 AEMaaCS에서만 사용할 수 있습니다.
   * 선택하지 않거나 웹 최적화된 이미지 제공 서비스를 사용할 수 없는 경우 [적응형 이미지 서블릿](/help/developing/adaptive-image-servlet.md)이 사용됩니다.
* **장식적 이미지** - 페이지에 이미지 구성 요소를 추가할 때 장식적 이미지 옵션이 자동으로 활성화되면 정의합니다.
* **DAM에서 그림 설명 다운로드** - 페이지에 이미지 구성 요소를 추가할 때 DAM에서 그림 설명을 검색하는 옵션이 자동으로 활성화되면 정의합니다.
* **DAM에서 캡션 다운로드** - 페이지에 이미지 구성 요소를 추가할 때 DAM에서 캡션을 검색하는 옵션이 자동으로 활성화되면 정의합니다.
* **팝업으로 캡션 표** - 페이지에 이미지 구성 요소를 추가할 때 팝업으로 이미지 캡션을 표시하는 옵션이 자동으로 활성화되면 정의합니다.
* **폭 조정** - 이 값은 DAM 에셋인 베이스 이미지의 폭을 조정하는 데 사용됩니다.
   * 이미지의 종횡비가 유지됩니다.
   * 값이 이미지의 실제 폭보다 크면 이 값은 효과가 없습니다.
   * 이 값은 SVG 이미지에 영향을 주지 않습니다.

이미지에 대해 허용된 폭 목록을 픽셀 단위로 정의하면 구성 요소는 브라우저 크기에 따라 가장 적절한 폭을 자동으로 로드합니다. 이는 이메일 이미지 구성 요소 [반응형 기능](#responsive-features)의 주요 부분입니다.

* **폭** - 이미지에 대해 폭 목록을 픽셀 단위로 정의하면 구성 요소는 브라우저 크기에 따라 가장 적절한 폭을 자동으로 로드합니다.
   * **추가** 버튼을 탭하거나 클릭하여 다른 크기를 추가합니다.
      * 그랩 드래그 핸들을 사용하여 크기의 순서를 재배열합니다.
      * **삭제** 아이콘을 사용하여 폭을 제거합니다.
   * 기본적으로 이미지가 표시될 때까지 이미지 로드를 연기합니다.
      * **소극적 로드 활성화** 옵션을 사용하여 페이지 로드에서 이미지를 로드합니다.
* **JPEG 품질** - 변환된(예: 크기 조정된 또는 잘린) JPEG 이미지의 품질 인수(0~100 사이의 백분율)입니다
* **기본 폭** - 디자인 대화 상자에서 사용될 이미지 기본 폭(픽셀)

>[!TIP]
>
>폭을 정의함으로써 렌디션 선택을 최적화하기 위한 팁과 관련된 자세한 내용은 [적응형 이미지 서블릿](/help/developing/adaptive-image-servlet.md) 문서를 참조하십시오.

### 스타일 탭 {#styles-tab}

이메일 이미지 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.
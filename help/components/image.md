---
title: 이미지 구성 요소
description: 코어 구성 요소 이미지 구성 요소 는 즉석 편집 중인 응용 이미지 구성 요소 기능입니다.
role: Architect, Developer, Administrator, Business Practitioner
exl-id: c5e57f4b-139f-40e7-8d79-be9a74360b63
source-git-commit: 8ff36ca143af9496f988b1ca65475497181def1d
workflow-type: tm+mt
source-wordcount: '2170'
ht-degree: 2%

---

# 이미지 구성 요소{#image-component}

코어 구성 요소 이미지 구성 요소는 즉석 편집 기능을 하는 응용 이미지 구성 요소입니다.

## 사용량 {#usage}

이미지 구성 요소는 페이지 방문자를 위해 레이지 로드를 사용하는 적응형 이미지 선택 및 응답형 동작과 컨텐츠 작성자를 위한 쉬운 이미지 배치 및 자르기를 제공합니다.

자르기와 추가 설정은 물론 이미지 너비는 [디자인 대화 상자](#design-dialog)에서 템플릿 작성자가 정의할 수 있습니다. 컨텐츠 편집기는 [구성 대화 상자](#configure-dialog)에서 자산을 업로드하거나 선택하고 [편집 대화 상자](#edit-dialog)에서 이미지를 자를 수 있습니다. 편의상 간단한 이미지 즉석 수정 작업도 가능합니다.

## 응답형 기능 {#responsive-features}

이미지 구성 요소에는 즉시 사용할 수 있는 강력한 응답형 기능이 포함되어 있습니다. 페이지 템플릿 수준에서 [디자인 대화 상자](#design-dialog)를 사용하여 이미지 자산의 기본 너비를 정의할 수 있습니다. 그러면 이미지 구성 요소가 브라우저 창의 크기에 따라 표시할 올바른 너비를 자동으로 로드합니다. 창 크기가 조정되면 이미지 구성 요소는 즉시 올바른 이미지 크기를 동적으로 로드합니다. 이미지 구성 요소는 이미 콘텐츠를 로드하도록 최적화되었으므로 구성 요소 개발자가 사용자 지정 미디어 쿼리 정의에 대해 걱정할 필요가 없습니다.

또한 이미지 구성 요소는 브라우저가 표시될 때까지 실제 이미지 자산 로드를 지연하여 페이지의 응답성을 높입니다.

## Dynamic Media 지원 {#dynamic-media}

이미지 구성 요소(예: [릴리스 2.13.0](/help/versions.md))는 [Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/dynamic-media.html?lang=en#dynamicmedia) 자산을 지원합니다. [활성화된 경우 ](#design-dialog) 이러한 기능을 사용하면 다른 이미지와 마찬가지로 간단한 드래그 앤 드롭으로 또는 자산 브라우저를 통해 Dynamic Media 이미지 자산을 추가할 수 있습니다. 또한 이미지 수정자, 이미지 사전 설정 및 스마트 자르기도 지원됩니다.

핵심 구성 요소로 구축된 웹 환경에서는 풍부한 기능을 갖춘 Sensei 기반의 강력한 고성능 교차 플랫폼 Dynamic Media 이미지 기능을 사용할 수 없습니다.

## 버전 및 호환성 {#version-and-compatibility}

이미지 구성 요소의 현재 버전은 v2이며, 2018년 1월에 핵심 구성 요소 릴리스 2.0.0에서 도입되었으며, 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전이 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | 호환 가능 | 호환 가능 | 호환 가능 |
| [v1](v1/image-v1.md) | 호환 가능 | 호환 가능 | - |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md) 문서를 참조하십시오.

## SVG 지원 {#svg-support}

SVG(Scalable Vector Graphics)는 이미지 구성 요소에서 지원됩니다.

* DAM에서 SVG 자산을 드래그 앤 드롭하고 로컬 파일 시스템에서 SVG 파일 업로드를 모두 지원합니다.
* 응용 이미지 서블릿은 원래 SVG 파일이 스트리밍되도록 스트리밍됩니다(변환은 생략됨).
* SVG 이미지의 경우 &quot;스마트 이미지&quot; 및 &quot;스마트 크기&quot;가 이미지 모델에서 빈 배열로 설정됩니다.

### 보안 {#security}

보안상의 이유로 원본 SVG는 이미지 편집기에서 직접 호출되지 않습니다. `<img src=“path-to-component”>`을 통해 호출됩니다. 따라서 브라우저가 SVG 파일에 포함된 스크립트를 실행할 수 없습니다.

>[!CAUTION]
>
>SVG 지원을 사용하려면 AEM 내에서 [이미지 편집기 기능](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/components-templates/image-editor.html)을 지원하기 위해 AEM 6.4 이상의 서비스 팩 2](https://docs.adobe.com/content/help/ko-KR/experience-manager-64/release-notes/sp-release-notes.html)과 함께 코어 구성 요소 이상의 릴리스 2.1.0이 필요합니다.[

## 샘플 구성 요소 출력 {#sample-component-output}

이미지 구성 요소를 경험하고 구성 옵션의 예와 HTML 및 JSON 출력을 보려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_image)를 방문하십시오.

### 기술 세부 정보 {#technical-details}

이미지 구성 요소 [에 대한 최신 기술 설명서는 GitHub](https://adobe.com/go/aem_cmp_tech_image_v2)에 있습니다.

코어 구성 요소 개발에 대한 자세한 내용은 [코어 구성 요소 개발자 설명서](/help/developing/overview.md)에서 확인할 수 있습니다.

이미지 구성 요소는 [schema.org microdata](https://schema.org)을 지원합니다.

## 구성 대화 상자 {#configure-dialog}

표준 [편집 대화 상자](#edit-dialog) 및 [디자인 대화 상자](#design-dialog) 외에도 이미지 구성 요소는 설명 및 기본 속성과 함께 이미지 자체가 정의된 구성 대화 상자를 제공합니다.

### 자산 탭 {#asset-tab}

![이미지 구성 요소의 구성 대화 상자에 있는 자산 탭](/help/assets/image-configure-asset.png)

* **이미지 자산**
   * [자산 브라우저](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html)에서 자산을 끌어 놓거나 **찾아보기** 옵션을 탭하여 로컬 파일 시스템에서 업로드합니다.
   * **지우기**&#x200B;를 탭하거나 클릭하여 현재 선택한 이미지를 선택 취소합니다.
   * **편집**&#x200B;을 탭하거나 클릭하여 [자산 편집기에서 자산](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/manage/manage-digital-assets.html)의 변환을 관리합니다.

### 메타데이터 탭 {#metadata-tab}

![이미지 구성 요소의 구성 대화 상자에 있는 메타데이터 탭](/help/assets/image-configure-metadata.png)

* **사전 설정 유형**  - 사용 가능한 이미지 사전 설정 유형( **이미지** 사전 설정 또는  **스마트 자르기**)을 정의하며  [Dynamic Media ](#dynamic-meida) 기능을 사용하는 경우에만 사용할 수 있습니다.
   * **이미지 사전 설정**  - [ **사전** 설정  **이미지 사전 설정]** 유형을 선택한 경우 사용 가능한 Dynamic Media 사전 설정 **에서 선택할 수 있는 드롭다운** 이미지 사전 설정을 사용할 수 있습니다. 선택한 자산에 대해 사전 설정이 정의된 경우에만 사용할 수 있습니다.
   * **스마트 자르기**  -  **[** 스마트  **카탈로그] 유형** 을 선택한 경우 드롭다운  **** 표현물을 사용할 수 있으므로 선택한 자산의 사용 가능한 표현물 중에서 선택할 수 있습니다. 선택한 자산에 대해 표현물이 정의된 경우에만 사용할 수 있습니다.
   * **이미지 수정자**  - 선택한 사전 설정 유형에 관계없이 추가 Dynamic Media 이미지 제공 명령 `&`을  **로 구분하여** 정의할 수 있습니다.
* **이미지가 장식용임**  - 보조 기술에 의해 이미지가 무시되어야 하므로 대체 텍스트가 필요 없는지 확인합니다. 이것은 장식 이미지만 적용됩니다.
* **대체 텍스트**  - 시각 장애가 있는 독자를 위한 이미지의 의미 또는 기능의 텍스트 대체 요소입니다.
   * **DAM에서 대체 텍스트 가져오기**  - 이 확인란을 선택하면 이미지의 대체 텍스트가 DAM에 있는  `dc:description` 메타데이터 값으로 채워집니다.
* **캡션**  - 기본적으로 이미지 아래에 표시되는 이미지에 대한 추가 정보입니다.
   * **DAM에서 캡션 가져오기**  - 이 확인란을 선택하면 이미지의 캡션 텍스트가 DAM에 있는  `dc:title` 메타데이터 값으로 채워집니다.
   * **캡션을 팝업으로 표시**  - 이 확인란을 선택하면 캡션이 이미지 아래에 표시되지 않고 이미지를 마우스로 가리키면 일부 브라우저에서 표시하는 팝업입니다.
* **링크**  - 이미지를 다른 리소스에 연결합니다.
   * 선택 대화 상자를 사용하여 다른 AEM 리소스에 연결합니다.
   * AEM 리소스에 연결하지 않을 경우 절대 URL을 입력합니다. 비솔루션 URL은 AEM을 기준으로 해석됩니다.
* **ID**  - 이 옵션을 사용하면 HTML과  [데이터 레이어에서 구성 요소의 고유 식별자를 제어할 수 있습니다](/help/developing/data-layer/overview.md).
   * 비워 두면 고유 ID가 자동으로 생성되며 결과 페이지를 검사하여 찾을 수 있습니다.
   * ID가 지정된 경우 ID가 고유한지 확인하는 것은 작성자의 책임입니다.
   * ID를 변경하면 CSS, JS 및 데이터 레이어 추적에 영향을 줄 수 있습니다.

>[!TIP]
>
>**스마트** 코어  **이미지 사전 설정** 은 함께 사용할 수 없는 옵션입니다. 작성자가 스마트 자르기 렌디션과 함께 이미지 사전 설정을 사용해야 하는 경우 작성자는 **이미지 수정자**&#x200B;를 사용하여 수동으로 사전 설정을 추가해야 합니다.

## 편집 대화 상자 {#edit-dialog}

편집 대화 상자에서는 컨텐츠 작성자가 이미지를 자르거나, 론치 맵을 수정하고, 확대/축소할 수 있습니다.

>[!NOTE]
>
>자르기, 회전 및 확대/축소 기능은 Dynamic Media 자산에 적용되지 않습니다. [Dynamic Media 기능](#dynamic-media)이 활성화되어 있으면 [구성 대화 상자를 통해 Dynamic Media 자산에 대한 모든 편집 작업을 수행해야 합니다.](#configure-dialog)

![이미지 구성 요소의 편집 대화 상자](/help/assets/image-edit.png)

* 자르기 시작

   ![자르기 시작 아이콘](/help/assets/image-start-crop.png)

   이 옵션을 선택하면 사전 정의된 자르기 비율에 대한 드롭다운이 열립니다.

   * 직접 자르기를 정의하려면 **자유 손** 옵션을 선택합니다.
   * **자르기 제거** 옵션을 선택하여 원래 자산을 표시합니다.

   자르기 옵션을 선택하면 파란색 핸들을 사용하여 이미지에서 자르기 크기를 지정합니다.

   ![자르기 옵션](/help/assets/image-crop-options.png)

* 오른쪽으로 회전

   ![오른쪽으로 회전 아이콘](/help/assets/image-rotate-right.png)

   이미지 90°을 오른쪽(시계 방향)으로 회전하려면 이 옵션을 사용합니다.

* 가로로 뒤집기

   ![가로 대칭 이동 아이콘](/help/assets/image-flip-horizontal.png)

   이미지를 가로로 뒤집거나 y축을 따라 이미지 180°을 회전하려면 이 옵션을 사용합니다.

* 세로로 뒤집기

   ![세로로 뒤집기 아이콘](/help/assets/image-flip-vertical.png)

   이미지를 세로로 뒤집거나 이미지를 x축을 따라 180° 피벗하려면 이 옵션을 사용합니다.

* 확대/축소 재설정

   ![확대/축소 재설정 아이콘](/help/assets/image-reset-zoom.png)

   이미지가 이미 확대/축소된 경우 이 옵션을 사용하여 확대/축소 수준을 재설정합니다.

* 확대/축소 슬라이더 열기

   ![확대/축소 슬라이더 아이콘 열기](/help/assets/image-zoom.png)

   이 옵션을 사용하여 슬라이더를 표시하여 이미지의 확대/축소 수준을 제어합니다.

   ![확대/축소 슬라이더 컨트롤](/help/assets/image-zoom-slider.png)

즉석 편집기를 사용하여 이미지를 수정할 수도 있습니다. 공간 제한 때문에 기본적인 옵션만 온라인으로 사용할 수 있습니다. 전체 편집 옵션의 경우 전체 화면 모드를 사용합니다.

![이미지 즉석 편집 옵션](/help/assets/image-in-place-edit.png)

>[!NOTE]
>
>GIF 이미지에는 이미지 편집 작업(자르기, 뒤집기, 회전)이 지원되지 않습니다. 편집 모드에서 GIF로 수행된 모든 변경 사항은 지속되지 않습니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자에서 이 구성 요소를 사용할 때 컨텐츠 작성자가 가지고 있는 자르기, 업로드, 회전 및 업로드 옵션을 정의할 수 있습니다.

### 기본 탭 {#main-tab}

**주** 탭에서 이미지에 대한 너비 목록을 픽셀 단위로 정의할 수 있으며, 구성 요소는 브라우저 크기에 따라 가장 적절한 너비를 자동으로 로드합니다. 이는 이미지 구성 요소의 [응답형 기능](#responsive-features)에서 중요한 부분입니다.

또한 작성자가 페이지에 구성 요소를 추가할 때 자동으로 또는 비활성화되는 일반 구성 요소 옵션을 정의할 수 있습니다.

![이미지 구성 요소의 디자인 대화 상자 기본 탭](/help/assets/image-design-main.png)

* **DM 기능 활성화**  - 이 확인란을 선택하면  [Dynamic Media 활성화 ](#dynamic-media) 기능을 사용할 수 있습니다.
* **레이지 로드 활성화**  - 페이지에 이미지 구성 요소를 추가할 때 레이지 로드 옵션이 자동으로 활성화되는지 여부를 정의합니다.
* **이미지가 장식용임**  - 페이지에 이미지 구성 요소를 추가할 때 장식 이미지 옵션이 자동으로 활성화되는지 여부를 정의합니다.
* **DAM에서 대체 텍스트 가져오기** - 페이지에 이미지 구성 요소를 추가할 때 DAM에서 대체 텍스트를 검색하는 옵션이 자동으로 활성화되어 있는지 정의합니다.
* **DAM에서 캡션 가져오기**  - 페이지에 이미지 구성 요소를 추가할 때 DAM에서 캡션을 검색하는 옵션이 자동으로 활성화되는지 여부를 정의합니다.
* **캡션을 팝업으로 표시**  - 페이지에 이미지 구성 요소를 추가할 때 이미지 캡션을 팝업으로 표시하는 옵션이 자동으로 활성화되어 있는지 여부를 정의합니다.
* **UUID 추적 비활성화**  - 이미지 자산의 UUID 추적을 비활성화하려면 을 선택합니다.
* **폭**  - 이미지의 너비 목록을 픽셀 단위로 정의하며 구성 요소는 브라우저 크기에 따라 가장 적합한 너비를 자동으로 로드합니다.
   * **추가** 단추를 탭하거나 클릭하여 다른 크기를 추가합니다.
      * 탭 핸들을 사용하여 크기 순서를 다시 정렬합니다.
      * **삭제** 아이콘을 사용하여 너비를 제거합니다.
   * 기본적으로 이미지 로드가 표시될 때까지 지연됩니다.
      * 페이지 로드 시 이미지를 로드하려면 **레이지 로드 비활성화** 옵션을 선택합니다.
* **JPEG 품질**  - 변형된(예: 크기 조절 또는 잘림) JPEG 이미지의 품질 요소(0에서 100까지의 백분율)입니다.

### 기능 탭 {#features-tab}

**기능** 탭에서 업로드 옵션, 방향 및 자르기 옵션을 포함한 구성 요소를 사용할 때 컨텐츠 작성자가 사용할 수 있는 옵션을 정의할 수 있습니다.

* 소스

   ![이미지 구성 요소의 디자인 대화 상자 기능 탭](/help/assets/image-design-features-source.png)

   컨텐츠 작성자가 로컬 컴퓨터의 이미지를 업로드할 수 있도록 하려면 **파일 시스템에서 자산 업로드 허용 옵션을 선택합니다.** 컨텐츠 작성자가 AEM에서 자산만 선택하도록 하려면 이 옵션을 선택 취소합니다.

* 방향

   ![이미지 구성 요소의 디자인 대화 상자 기능 탭](/help/assets/image-design-features-orientation.png)

* ****
회전이 옵션을 사용하여 컨텐츠 작성자가 
**오른쪽으로** 회전 선택 사항입니다.
* ****
뒤집기이 옵션을 사용하여 컨텐츠 작성자가 
**수평** 대칭 이동 및  **수직** 대칭 이동 옵션.

   >[!CAUTION]
   >
   >기본적으로 **Flip** 옵션이 비활성화됩니다. 이 기능을 활성화하면 이미지 구성 요소의 편집 대화 상자에 **세로로 뒤집기** 및 **가로로 뒤집기** 단추가 표시되지만, 이 기능은 현재 AEM에서 지원하지 않으며, 이러한 옵션을 사용하여 변경한 사항은 유지되지 않습니다.

* 자르기

   ![이미지 구성 요소의 디자인 대화 상자 기능 탭](/help/assets/image-design-features-cropping.png)

   컨텐츠 작성자가 편집 대화 상자의 구성 요소에서 이미지를 자르도록 하려면 **자르기 허용** 옵션을 선택합니다.
   * 사전 정의된 자르기 종횡비를 추가하려면 **추가**&#x200B;를 클릭하십시오.
   * **자르기 시작** 드롭다운에 표시되는 수사적 이름을 입력합니다.
   * 종횡비의 숫자 비율을 입력합니다.
   * 드래그 핸들을 사용하여 종횡비의 순서를 다시 정렬합니다
   * 종횡비를 삭제하려면 휴지통 아이콘을 사용하십시오.

   >[!CAUTION]
   >
   >AEM에서 자르기 종횡비는 **height/width**&#x200B;로 정의됩니다. 이것은 종래의 폭/높이 정의와 다르며, 레거시 호환성을 위해 수행됩니다. 비율이 비율 자체가 아니라 UI에 이름이 표시되므로 콘텐츠 작성자는 명확한 이름을 제공하면 차이를 알지 못합니다.

### 스타일 탭 {#styles-tab-1}

이미지 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

## 응용 이미지 서블릿 {#adaptive-image-servlet}

이미지 구성 요소는 코어 구성 요소의 응용 이미지 서블릿을 사용합니다. [응용 이미지 ](https://github.com/adobe/aem-core-wcm-components/wiki/The-Adaptive-Image-Servlet) 서비스는 이미지 처리 및 스트리밍을 담당하며 개발자가 핵심 구성 요소의 사용자 지정 [에서 활용할 수 있습니다](/help/developing/customizing.md).

>[!NOTE]
>
>`Last-Modified` 헤더를 통한 조건부 요청은 응용 이미지 서블릿에서 지원되지만 `Last-Modified` 헤더 [의 캐싱은 Dispatcher](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html?lang=en#caching-http-response-headers)에서 활성화해야 합니다.
>
>[AEM 프로젝트 원형](/help/developing/archetype/overview.md) 의 샘플 Dispatcher 구성에 이미 이 구성이 포함되어 있습니다.

## Adobe 클라이언트 데이터 계층 {#data-layer}

이미지 구성 요소는 [Adobe 클라이언트 데이터 계층을 지원합니다.](/help/developing/data-layer/overview.md)

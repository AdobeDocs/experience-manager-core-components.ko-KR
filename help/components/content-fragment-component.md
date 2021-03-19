---
title: 컨텐츠 조각 구성 요소
description: 핵심 구성 요소 컨텐츠 조각 구성 요소를 사용하면 컨텐츠 조각을 표시할 수 있습니다.
role: 건축가, 개발자, 관리자, 비즈니스 전문가
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 9%

---


# 컨텐츠 조각 구성 요소{#content-fragment-component}

핵심 구성 요소 컨텐츠 조각 구성 요소를 사용하면 [컨텐츠 조각](https://docs.adobe.com/content/help/ko-KR/experience-manager-cloud-service/assets/content-fragments/content-fragments.html)을 표시할 수 있습니다.

>[!NOTE]
>
>핵심 구성 요소의 릴리스 2.4.0 이전에는 컨텐츠 조각 구성 요소를 핵심 구성 요소의 익스텐션으로 사용할 수 있었으며 별도로 다운로드하여 명시적으로 활성화해야 했습니다.

## 사용량 {#usage}

핵심 구성 요소 컨텐츠 조각 구성 요소를 사용하면 페이지에 [컨텐츠 조각](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments.html)을 포함할 수 있습니다.

* 조각 및 해당 속성은 [구성 대화 상자](#configure-dialog)에서 선택할 수 있습니다.
* 특정 이미지 및 그리드를 처리하는 리소스 유형은 [디자인 대화 상자](#design-dialog)에서 정의할 수 있습니다.
* 편집 옵션은 [컨텐츠 조각 편집기](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments-variations.html) 내에서 선택한 조각을 엽니다.

## 버전 및 호환성 {#version-and-compatibility}

컨텐츠 조각 구성 요소의 현재 버전은 v1이며, 2017년 10월 핵심 구성 요소 릴리스 1.1.0에서 도입되었으며 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소 버전이 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |

>[!NOTE]
>
>2.4.0 출시 전에 컨텐츠 조각 구성 요소가 extensions 폴더에 있었습니다.
>
> `apps/core/wcm/extension/components/contentfragment/v1/contentfragment`
> 
>2.4.0부터 다음 위치로 이동되었습니다.
>
>`apps/core/wcm/components/contentfragment/v1/contentfragment`
>
>둘 다 v1이지만, 확장 폴더에서 사용된 컨텐츠 조각 구성 요소는 핵심 구성 요소의 릴리스 2.4.0 이상으로 업그레이드할 때 새 리소스 유형을 사용하기 위해 관련 프록시 구성 요소를 마이그레이션해야 합니다.

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

컨텐츠 조각 구성 요소와 구성 옵션 예 및 HTML 및 JSON 출력을 보려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_cf)를 방문하십시오.

## 기술 세부 정보 {#technical-details}

컨텐츠 조각 구성 요소 [에 대한 최신 기술 문서는 GitHub](https://adobe.com/go/aem_cmp_tech_cf_v1)에서 찾을 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)에서 확인할 수 있습니다.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자를 사용하면 컨텐츠 작성자가 포함시킬 컨텐츠 조각 및 해당 조각의 요소를 정의할 수 있습니다.

### 속성 탭 {#properties-tab}

![컨텐츠 조각 구성 요소](/help/assets/content-fragment-edit-properties.png)

* **콘텐츠 조각**

   * 원하는 컨텐츠 조각의 경로
   * **선택 대화 상자**&#x200B;를 사용하여 조각을 찾을 수 있습니다.

* **표시 모드**
   * **단일 텍스트 요소**  - 여러 줄로 된 텍스트 요소를 선택할 수 있고 단락 컨트롤 옵션을 사용할 수 있습니다.
   * **여러 요소**  - 선택한 컨텐츠 조각의 하나 이상의 요소를 선택할 수 있습니다.
* **요소**  - 포함할 컨텐츠 조각의 요소 또는 요소입니다.
* **변형**  - 사용할 컨텐츠 조각의 변형(기본값:  **기본**)

* **단락**

   * **모두**  - 모든 단락 표시
   * **범위**

      * 세미콜론으로 구분하여 표시해야 하는 단락 범위를 지정합니다.
      * 예를 들어 1일, 3일~5일, 7일, 9일~9일 단락을 포함하는 `1;3-5;7;9-*`
* **ID**  - 이 옵션을 사용하면 HTML 및 데이터 레이어에서 구성 요소의 고유 식별자를 제어할  [수 있습니다](/help/developing/data-layer/overview.md).
   * 비워 두면 자동으로 고유 ID가 생성되며 결과 페이지를 검사하여 찾을 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID를 변경하면 CSS, JS 및 데이터 레이어 추적에 영향을 줄 수 있습니다.

### 단락 컨트롤 탭 {#paragraph-control-tab}

**여러 요소** 모드를 선택한 경우에는 이 탭을 사용할 수 없습니다.

![컨텐츠 조각 구성 요소](/help/assets/content-fragment-edit-paragraph.png)

* **단락**  - 모든 단락 또는 범위를 선택할 수 있습니다.
* **머리글을 원하는 단락으로 처리**

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 사용하여 혼합된 미디어 이미지와 응답형 그리드를 처리하는 데 사용되는 리소스 유형을 정의할 수 있습니다.

![컨텐츠 조각 구성 요소의 디자인 대화 상자](/help/assets/content-fragment-design.png)

* **내부 응답형 격자**

   * 내부 응답형 격자에 사용된 Sling 리소스 유형입니다

## Adobe 클라이언트 데이터 레이어 {#data-layer}

컨텐츠 조각 구성 요소는 [Adobe 클라이언트 데이터 레이어를 지원합니다.](/help/developing/data-layer/overview.md)

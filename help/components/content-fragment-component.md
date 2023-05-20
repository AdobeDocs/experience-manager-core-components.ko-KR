---
title: 콘텐츠 조각 구성 요소
description: 핵심 구성 요소의 콘텐츠 조각 구성 요소를 사용하여 버튼을 생성하고 표시할 수 있습니다.
role: Architect, Developer, Admin, User
exl-id: 551ff2a1-f8db-490c-84a3-4255b364fc83
source-git-commit: 9767a3a10cb9a77f385edc0ac3fb00096c0087af
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 100%

---

# 콘텐츠 조각 구성 요소{#content-fragment-component}

핵심 구성 요소의 [콘텐츠 조각 구성 요소](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html)를 사용하여 버튼을 생성하고 표시할 수 있습니다.

>[!NOTE]
>
>핵심 구성 요소 릴리스 2.4.0 이전의 콘텐츠 조각 구성 요소는 핵심 구성 요소의 확장 기능으로 사용되고, 별도로 다운로드되고 명시적으로 활성화되어야 합니다.

## 사용량 {#usage}

핵심 구성 요소의 콘텐츠 조각 구성 요소를 사용하여 페이지에 [콘텐츠 조각](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html)을 포함할 수 있습니다.

* [구성 대화 상자](#configure-dialog)에서 조각과 조각의 속성을 선택할 수 있습니다.
* [디자인 대화 상자](#design-dialog)에서 특정 이미지와 그리드를 처리하는 리소스 유형을 정의할 수 있습니다.
* 편집 옵션은 [콘텐츠 조각 편집기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments-variations.html) 내에서 선택한 조각을 열 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

현재 버전의 콘텐츠 조각 구성 요소는 2017년 10월 핵심 구성 요소 릴리스 1.1.0과 함께 도입된 v1입니다. 이 문서에서는 해당 구성 요소에 대해 설명합니다.

다음 표에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | 호환 가능 <br>[2.17.4](/help/versions.md) 및 이전 릴리스 | 호환 가능 | 호환 가능 |

>[!NOTE]
>
>릴리스 2.4.0 이전의 콘텐츠 조각 구성 요소는 확장 폴더에 있습니다.
>
> `apps/core/wcm/extension/components/contentfragment/v1/contentfragment`
> 
>릴리스 2.4.0에서 다음 위치로 이동합니다.
>
>`apps/core/wcm/components/contentfragment/v1/contentfragment`
>
>둘 다 v1이지만 릴리스 2.4.0 이상의 핵심 구성 요소 업그레이드 시 확장 폴더에서 콘텐츠 조각 구성 요소를 사용하려면 관련 프록시 구성 요소를 마이그레이션하여 새 리소스 유형을 사용해야 합니다.

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md)을 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

콘텐츠 조각 구성 요소를 경험하고 구성 옵션의 샘플뿐만 아니라 HTML 및 JSON 출력을 확인하려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_cf_kr)를 참조하십시오.

## 기술 세부 사항 {#technical-details}

콘텐츠 조각 구성 요소에 대한 최신 기술 설명서는[ GitHub에서 확인할 수 있습니다](https://adobe.com/go/aem_cmp_tech_cf_v1_kr).

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

콘텐츠 작성자는 구성 대화 상자를 통해 포함해야 할 콘텐츠 조각과 해당 조각의 요소를 정의할 수 있습니다.

### 속성 탭 {#properties-tab}

![콘텐츠 조각 구성 요소](/help/assets/content-fragment-edit-properties.png)

* **콘텐츠 조각**

   * 원하는 콘텐츠 조각의 경로
   * **선택 대화 상자**&#x200B;를 선택하여 조각을 찾을 수 있습니다.

* **표시 모드**
   * **단일 텍스트 요소** - 하나의 여러 줄 텍스트 요소 선택을 활성화하고 단락 제어 옵션을 활성화합니다.
   * **다중 요소** - 선택한 콘텐츠 조각에서 하나 이상의 요소를 선택할 수 있습니다.
* **요소** - 포함될 콘텐츠 조각의 요소
* **변형** - 사용될 콘텐츠 조각의 변형(기본적으로 **마스터**&#x200B;로 설정)

* **단락**

   * **전체** - 모든 문단이 표시됩니다.
   * **범위**

      * 세미콜론으로 구분되어야 하는 단락의 범위를 지정합니다.
      * 예: 최종 단락에 1번째, 3번쨰, 5번쨰, 7번째, 9번째 단락이 포함될 `1;3-5;7;9-*`
* **ID** - 이 옵션을 통해 HTML과 [데이터 레이어](/help/developing/data-layer/overview.md)에서 구성 요소의 고유 식별자를 제어할 수 있습니다.
   * 비워 두면 고유 ID는 자동으로 생성되고 결과 페이지 검사를 통해 발견될 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID가 변경되면 CSS, JS 및 데이터 레이어 추적에 영향을 미칠 수 있습니다.

### 단락 제어 탭 {#paragraph-control-tab}

**다중 요소** 모드 선택 시 이 탭을 사용할 수 없습니다.

![콘텐츠 조각 구성 요소](/help/assets/content-fragment-edit-paragraph.png)

* **단락** - 모든 단락 또는 범위를 선택할 수 있습니다.
* **제목을 소유자의 단락으로 처리**

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 통해 혼합 미디어 이미지 처리에 사용되는 리소스 유형을 정의할 수 있습니다.

![콘텐츠 조각 구성 요소의 디자인 대화 상자](/help/assets/content-fragment-design.png)

* **내부 응답형 격자**

   * 내부 응답형 격자에 사용된 슬링 리소스 유형입니다

## Adobe 클라이언트 데이터 레이어 {#data-layer}

콘텐츠 조각 구성 요소는 [Adobe 클라이언트 데이터 레이어](/help/developing/data-layer/overview.md)를 지원합니다.

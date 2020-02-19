---
title: 컨텐츠 조각 구성 요소
description: 핵심 구성 요소 컨텐츠 조각 구성 요소를 사용하면 컨텐츠 조각을 표시할 수 있습니다.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# 컨텐츠 조각 구성 요소{#content-fragment-component}

핵심 구성 요소 컨텐츠 조각 구성 요소를 사용하면 [컨텐츠 조각을](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments.html)표시할 수 있습니다.

>[!NOTE]
>
>핵심 구성 요소의 릴리스 2.4.0 이전에 컨텐츠 조각 구성 요소는 핵심 구성 요소의 익스텐션으로 사용할 수 있었으며 별도로 다운로드되어 명시적으로 활성화해야 했습니다.

## 사용량 {#usage}

핵심 구성 요소 컨텐츠 조각 구성 요소를 사용하면 페이지에 [컨텐츠 조각을](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) 포함할 수 있습니다.

* 조각 및 해당 속성은 [구성 대화 상자에서](#configure-dialog)선택할 수 있습니다.
* 특정 이미지 및 격자를 처리하는 리소스 유형은 [디자인 대화 상자에서](#design-dialog)정의할 수 있습니다.
* 편집 옵션은 [컨텐츠 조각 편집기](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments-variations.html)내에서 선택한 조각을 엽니다.

## 버전 및 호환성 {#version-and-compatibility}

컨텐츠 조각 구성 요소의 현재 버전은 v1이며, 이 버전은 2017년 10월 핵심 구성 요소 릴리스 1.1.0과 함께 도입되었으며 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소 버전이 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.3 | AEM 6.4 | AEM 6.5 | 클라우드 서비스로 AEM 사용 |
|--- |--- |--- |---|---|
| v1 | 호환 가능 | 호환 가능 | 호환 가능 | 호환 가능 |

>[!NOTE]
>
>릴리스 2.4.0 이전에는 컨텐츠 조각 구성 요소가 확장 폴더에 있었습니다.
>
> `apps/core/wcm/extension/components/contentfragment/v1/contentfragment`
> 
>2.4.0에서 다음 위치로 이동되었습니다.
>
>`apps/core/wcm/components/contentfragment/v1/contentfragment`
>
>둘 다 v1이지만, 확장 폴더에서 사용된 컨텐츠 조각 구성 요소는 핵심 구성 요소의 릴리스 2.4.0 이상으로 업그레이드할 때 새 리소스 유형을 사용하기 위해 관련 프록시 구성 요소를 마이그레이션해야 합니다.

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 핵심 구성 요소 [버전을 참조하십시오](/help/versions.md).

## 샘플 구성 요소 출력 {#sample-component-output}

컨텐츠 조각 구성 요소뿐만 아니라 구성 옵션 예와 HTML 및 JSON 출력을 보려면 구성 요소 [라이브러리를 참조하십시오](https://adobe.com/go/aem_cmp_library_cf).

## 기술 정보 {#technical-details}

컨텐츠 조각 구성 요소에 대한 최신 기술 문서는 GitHub에서 [찾을 수 있습니다](https://adobe.com/go/aem_cmp_tech_cf_v1).

핵심 구성 요소 개발에 대한 자세한 내용은 핵심 구성 요소 개발자 [설명서를](/help/developing/overview.md)참조하십시오.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자에서는 컨텐츠 작성자가 포함할 컨텐츠 조각 및 해당 조각의 요소를 정의할 수 있습니다.

![](/help/assets/chlimage_1-87.png)

* **콘텐츠 조각**

   * 원하는 컨텐츠 조각의 경로
   * 선택 **대화 상자를** 사용하여 조각을 찾을 수 있습니다.

* **요소** - 포함할 컨텐츠 조각의 요소
* **변형** - 사용할 컨텐츠 조각의 변형(기본값: **마스터**)

* **단락**

   * **모두** - 모든 단락 표시
   * **범위**

      * 세미콜론으로 구분하여 표시해야 하는 단락 범위를 지정합니다.
      * 예를 `1;3-5;7;9-*` 들어 1일, 3일 ~ 5일, 7일 및 9일 대 최종 단락을 포함시킵니다.

* **머리글을 단락으로 처리**

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 사용하여 혼합 미디어 이미지 및 반응형 그리드를 처리하는 데 사용되는 리소스 유형을 정의할 수 있습니다.

![](/help/assets/chlimage_1-88.png)

* **혼합된 미디어 이미지 유형**

   * 혼합된 미디어 이미지 렌더링에 사용되는 Sling 리소스 유형

* **내부 응답형 격자**

   * 내부 응답형 격자에 사용된 Sling 리소스 유형입니다


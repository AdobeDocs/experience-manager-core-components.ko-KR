---
title: 컨텐츠 조각 목록 구성 요소
description: 핵심 구성 요소 컨텐츠 조각 목록 구성 요소를 사용하면 컨텐츠 조각 목록을 표시할 수 있습니다.
role: Architect, Developer, Admin, User
exl-id: 0f2295b1-d287-4f72-8ee4-fa98c4850e53
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '762'
ht-degree: 5%

---

# 컨텐츠 조각 목록 구성 요소{#content-fragment-list-component}

코어 구성 요소 컨텐츠 조각 목록 구성 요소를 사용하면 [컨텐츠 조각](https://docs.adobe.com/content/help/ko/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) 목록을 표시할 수 있습니다.

## 사용량 {#usage}

코어 구성 요소 컨텐츠 조각 목록 구성 요소를 사용하면 컨텐츠 조각 모델을 기반으로 페이지에 [컨텐츠 조각](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) 목록을 포함할 수 있습니다. 이 기능은 다른 응용 프로그램에서 쉽게 사용할 수 있는 [헤드리스 컨텐츠](https://helpx.adobe.com/kr/experience-manager/6-5/sites/developing/user-guide.html?topic=/experience-manager/6-5/sites/developing/morehelp/headless.ug.js)를 만드는 데 특히 유용합니다.

* 목록 및 속성은 [구성 대화 상자](#configure-dialog)에서 선택할 수 있습니다.
* [디자인 대화 상자](#design-dialog)에서 스타일을 구성 요소에 적용할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

컨텐츠 조각 구성 요소의 현재 버전은 v1이며, 2019년 5월에 핵심 구성 요소 릴리스 2.4.0에서 도입되었으며, 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전이 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

컨텐츠 조각 목록 구성 요소 와 구성 옵션의 예 및 HTML 및 JSON 출력을 보려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_cflist)를 방문하십시오.

## 기술 세부 정보 {#technical-details}

컨텐츠 조각 목록 구성 요소 [에 대한 최신 기술 설명서는 GitHub](https://adobe.com/go/aem_cmp_tech_cflist_v1)에 있습니다.

코어 구성 요소 개발에 대한 자세한 내용은 [코어 구성 요소 개발자 설명서](/help/developing/overview.md)에서 확인할 수 있습니다.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자에서는 컨텐츠 작성자가 목록을 구성하는 컨텐츠 조각과 포함할 해당 조각의 요소를 정의할 수 있습니다.

### 속성 탭

**속성** 탭은 목록에 포함된 컨텐츠 조각을 정의합니다. 기본적으로 선택된 컨텐츠 조각 모델을 기반으로 하지만 다른 필터 옵션을 사용할 수 있습니다.

![컨텐츠 조각 목록 구성 요소의 편집 대화 상자에 있는 속성 탭](/help/assets/content-fragment-list-properties.png)

* **모델**  - 목록이 기반으로 하는 컨텐츠 조각 모델의 경로입니다.
   * 기본적으로 **모델 경로**&#x200B;로 정의된 모델의 모든 컨텐츠 조각이 목록에 포함됩니다.
* **상위 경로**  - 목록을 작성할 상위 경로입니다.
   * 선택한 **모델 경로**&#x200B;를 기반으로 하는 컨텐츠 조각은 지정된 **상위 경로**&#x200B;에 있는 조각으로 필터링됩니다.
      * 필드의 오른쪽에 있는 **선택 대화 상자 열기** 단추를 클릭하거나 탭하여 경로를 지정합니다.
* **태그**  - 지정된 태그가 있는 컨텐츠 조각만 목록에 포함됩니다.
   * 필드의 오른쪽에 있는 **선택 대화 상자 열기** 단추를 클릭하거나 탭하여 태그를 지정합니다.
   * 선택한 태그 옆에 있는 X 를 클릭하거나 탭하여 제거합니다.
* **정렬 기준**  - 목록이 정렬될 컨텐츠 조각 모델의 필드입니다
   * 텍스트 필드(숫자, 날짜 및 시간 포함)만 선택할 수 있습니다.
* **정렬 순서**  - 목록을 정렬 기준 필드 **로 정렬하는** 방법
   * 오름차순 또는 내림차순
* **최대 항목**  - 목록에 표시할 최대 항목 수입니다
   * 값이 모든 항목을 반환하지 않습니다.
* **ID**  - 이 옵션을 사용하면 HTML과  [데이터 레이어에서 구성 요소의 고유 식별자를 제어할 수 있습니다](/help/developing/data-layer/overview.md).
   * 비워 두면 고유 ID가 자동으로 생성되며 결과 페이지를 검사하여 찾을 수 있습니다.
   * ID가 지정된 경우 ID가 고유한지 확인하는 것은 작성자의 책임입니다.
   * ID를 변경하면 CSS, JS 및 데이터 레이어 추적에 영향을 줄 수 있습니다.

>[!NOTE]
>**Order By**, **정렬 순서** 및 **최대 항목** 옵션은 코어 구성 요소 릴리스 2.7.0과 함께 도입되었습니다.

### 요소 탭

기본적으로 컨텐츠 조각 모델의 모든 요소가 목록에 포함됩니다(**최대 항목** 필드로 제한되지 않는 경우). **Elements** 탭에서는 포함할 특정 요소만 지정할 수 있습니다.

![컨텐츠 조각 목록 구성 요소의 편집 대화 상자에 있는 요소 탭](/help/assets/content-fragment-list-elements.png)

* **요소**  - 지정된 목록에 있는 컨텐츠 조각의 요소만 표시됩니다.
   * **추가** 단추를 클릭하거나 탭하여 새 요소를 추가합니다.
   * **삭제** 단추를 클릭하거나 탭하여 선택한 요소를 제거합니다.
   * **Order** 핸들을 드래그하여 요소의 순서를 재정렬합니다.

## 디자인 대화 상자 {#design-dialog}

디자인 대화 상자에서는 템플릿 작성자가 컨텐츠 조각 목록 구성 요소에 적용된 스타일을 정의할 수 있습니다.

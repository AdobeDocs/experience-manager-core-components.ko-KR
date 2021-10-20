---
title: 콘텐츠 조각 목록 구성 요소
description: 핵심 구성 요소의 콘텐츠 조각 목록 구성 요소를 사용하여 콘텐츠 조각 목록을 표시할 수 있습니다.
role: Architect, Developer, Admin, User
exl-id: 0f2295b1-d287-4f72-8ee4-fa98c4850e53
source-git-commit: 888719359f9a1d1c9dccff97fb639b332f2be54c
workflow-type: ht
source-wordcount: '758'
ht-degree: 100%

---

# 콘텐츠 조각 목록 구성 요소{#content-fragment-list-component}

핵심 구성 요소의 콘텐츠 조각 목록 구성 요소를 사용하여 [콘텐츠 조각](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) 목록을 표시할 수 있습니다.

## 사용량 {#usage}

핵심 구성 요소의 콘텐츠 조각 목록 구성 요소를 사용하여 콘텐츠 조각 모델에 따라 페이지에 [콘텐츠 조각](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) 목록을 포함할 수 있습니다. 다른 애플리케이션에서 간단히 사용할 수 있는 [헤드리스 콘텐츠](https://helpx.adobe.com/kr/experience-manager/6-5/sites/developing/user-guide.html?topic=/experience-manager/6-5/sites/developing/morehelp/headless.ug.js)를 제작하는 경우 특히 유용합니다.

* [구성 대화 상자](#configure-dialog)에서 목록과 목록의 속성을 선택할 수 있습니다.
* [디자인 대화 상자](#design-dialog)에서 스타일을 구성 요소에 적용할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

현재 버전의 콘텐츠 조각 구성 요소는 2019년 5월 핵심 구성 요소 릴리스 2.4.0과 함께 도입된 v1입니다. 이 문서에서는 해당 구성 요소에 대해 설명합니다.

다음 표에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md)을 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

콘텐츠 조각 목록 구성 요소를 경험하고 구성 옵션의 샘플뿐만 아니라 HTML 및 JSON 출력을 확인하려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_cflist_kr)를 참조하십시오.

## 기술 세부 사항 {#technical-details}

콘텐츠 조각 목록 구성 요소에 대한 최신 기술 설명서는[ GitHub에서 확인할 수 있습니다](https://adobe.com/go/aem_cmp_tech_cflist_v1_kr).

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

콘텐츠 작성자는 구성 대화 상자를 통해 포함될 목록과 해당 조각의 요소를 구성하는 콘텐츠 조각을 정의할 수 있습니다.

### 속성 탭

**속성** 탭은 목록에 포함된 콘텐츠 조각을 정의합니다. 주로 선택한 콘텐츠 조각 모델을 기반으로 하지만 다른 필터 옵션을 선택할 수 있습니다.

![콘텐츠 조각 목록 구성 요소의 편집 대화 상자 속성 탭](/help/assets/content-fragment-list-properties.png)

* **모델** - 목록의 기반이 되는 콘텐츠 조각 모델의 경로.
   * 기본적으로 **모델 경로**&#x200B;로 정의된 모델의 모든 콘텐츠 조각이 목록에 포함됩니다.
* **상위 경로** - 목록을 빌드해야 하는 상위 경로
   * 선택한 **모델 경로**&#x200B;를 기반으로 콘텐츠 조각을 지정된 **상위 경로**&#x200B;의 조각으로 필터링할 수 있습니다.
      * 필드의 오른쪽 **선택 열기 대화 상자** 버튼을 클릭하거나 탭하여 경로를 지정합니다.
* **태그** - 지정된 태그가 있는 콘텐츠 조각만 표시됩니다.
   * 필드의 오른쪽 **선택 열기 대화 상자** 버튼을 클릭하거나 탭하여 태그를 지정합니다.
   * 선택한 태그 옆의 x를 클릭하거나 탭하여 태그를 제거합니다.
* **항목별 순서** - 목록의 순서를 정하는 콘텐츠 조각 모델의 필드
   * 텍스트 필드(숫자, 날짜 및 시간)만 선택할 수 있습니다.
* **정렬 순서** - **항목별 순서**&#x200B;로 목록을 정렬하는 방법
   * 오름차순 또는 내림차순
* **최대 항목** - 목록에 표시될 최대 항목 수
   * 값은 모든 항목을 반환하지 않습니다.
* **ID** - 이 옵션을 통해 HTML과 [데이터 레이어](/help/developing/data-layer/overview.md)에서 구성 요소의 고유 식별자를 제어할 수 있습니다.
   * 비워 두면 고유 ID는 자동으로 생성되고 결과 페이지 검사를 통해 발견될 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID가 변경되면 CSS, JS 및 데이터 레이어 추적에 영향을 미칠 수 있습니다.

>[!NOTE]
>**항목별 순서**, **정렬 순서** 및 **최대 항목** 옵션은 핵심 구성 요소 릴리스 2.7.0과 함께 도입되었습니다.

### 요소 탭

기본적으로 목록에 콘텐츠 조각 모델의 모든 요소가 포함될 수 있습니다(**최대 항목** 필드에서 제한하지 않는 경우). **요소** 탭을 통해 포함될 특정 요소만 지정할 수 있습니다.

![콘텐츠 조각 목록 구성 요소의 편집 대화 상자 요소 탭](/help/assets/content-fragment-list-elements.png)

* **요소** - 지정된 목록의 콘텐츠 조각 요소만 표시됩니다.
   * **추가** 버튼을 클릭하거나 탭하여 새 요소를 추가합니다.
   * **삭제** 버튼을 클릭하거나 탭하여 선택한 요소를 삭제합니다.
   * 요소의 순서를 재배열하려면 **순서** 핸들을 드래그합니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 통해 콘텐츠 조각 목록 구성 요소에 적용되는 스타일을 정의할 수 있습니다.

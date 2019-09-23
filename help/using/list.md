---
title: 구성 요소 나열
seo-title: 구성 요소 나열
description: 'null'
seo-description: 핵심 구성 요소 목록 구성 요소를 사용하면 정적 목록뿐만 아니라 동적 목록을 쉽게 만들 수 있습니다.
uuid: 50a572e8-b444-4f7d-82bc-5a93seb4be95
contentOwner: 사용자
content-type: 참조
topic-tags: authoring
products: SG_EXPERIENCEMANAGER/CORCOMPONENTS-new
discoiquuid: 89053323-6221-46ed-896a-31a42c55282e
disttype: dist5
gnavtheme: 밝음
groupsectionnavitems: 아니오
hidemerchandisingbar: 상속
hidepromocomponent: 상속
modalsize: 426x240
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: eef608fb06001485aa2c2c0b574af412ed7f15a4

---


# 구성 요소 나열{#list-component}

핵심 구성 요소 목록 구성 요소를 사용하면 정적 목록뿐만 아니라 동적 목록을 쉽게 만들 수 있습니다.

## 사용량 {#usage}

목록 구성 요소를 사용하여 하위 페이지의 동적 목록 또는 임의의 정의된 항목의 정적 목록을 만들 수 있습니다. 사용 가능한 목록 유형 및 서식 지정 옵션은 [디자인 대화 상자에서](#design-dialog)템플릿 작성자가 정의할 수 있습니다. 컨텐츠 편집기는 사용 가능한 목록 유형 및 [편집 대화](#edit-dialog)상자에서 목록 요소의 서식을 지정하는 방법을 선택할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

목록 구성 요소의 현재 버전은 v2이며, 이 버전은 2018년 1월에 릴리스 2.0.0의 핵심 구성 요소에 소개되었으며 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소 버전이 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | 호환 가능 | 호환 가능 | 호환 가능 |
| [v1](list-v1.md) | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 핵심 구성 요소 [버전을 참조하십시오](versions.md).

## 샘플 구성 요소 출력 {#sample-component-output}

목록 구성 요소뿐만 아니라 구성 옵션의 예와 HTML 및 JSON 출력을 보려면 구성 요소 [라이브러리를 참조하십시오](http://opensource.adobe.com/aem-core-wcm-components/library/list.html).

### 기술 정보 {#technical-details}

목록 구성 요소에 대한 최신 기술 문서는 GitHub에서 [찾을 수 있습니다](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/list/v2/list).

핵심 구성 요소 개발에 대한 자세한 내용은 핵심 구성 요소 개발자 [설명서를](developing.md)참조하십시오.

## Edit Dialog {#edit-dialog}

편집 대화 상자에서는 컨텐츠 작성자가 목록 및 목록 항목을 구성할 수 있습니다.

### 목록 설정 탭 {#list-settings-tab}

목록은 다양한 방법으로 작성할 수 있습니다.

* [하위 페이지](#child-pages)
* [고정 목록](#fixed-list)
* [검색](#search-options)
* [태그](#tags)

목록이 작성되는 방식에 관계없이 항상 [구성할 수 있는](#sort-options) 정렬 옵션이 있습니다.

![](assets/chlimage_1-38.png)

컨텐츠 작성자가 목록 작성을 선택하는 방법에 따라 추가 구성 옵션이 변경됩니다.

#### 하위 페이지 {#child-pages}

목록은 현재 페이지나 다른 페이지의 하위 페이지로 구성됩니다.

![](assets/chlimage_1-39.png)

* **상위 페이지**
   * 하위 페이지가 목록을 만들어야 하는 페이지
   * 현재 페이지를 사용하려면 비워 둡니다.

* **하위 수준**&#x200B;계층 구조에서 하위 수준 사용

#### Fixed List {#fixed-list}

고정된 항목 목록을 사용하여 목록을 작성할 수 있습니다.

![](assets/chlimage_1-40.png)

추가 단추를 탭하거나 **클릭하여** 목록에 새 항목을 삽입합니다.

* 목록에 있는 항목의 텍스트를 입력하거나 선택 **대화 상자를** 사용하여 AEM에서 항목을 선택합니다.
* 드래그 핸들을 사용하여 목록의 항목을 다시 정렬합니다.
* 휴지통 아이콘을 사용하여 목록에서 항목을 삭제합니다.

#### 검색 {#search-options}

AEM 컨텐츠 검색 결과를 사용하여 목록을 작성할 수 있습니다.

![](assets/chlimage_1-41.png)

* **검색**&#x200B;쿼리전체 텍스트 검색을 실행하여 목록 요소를 생성하는 문자열
* **검색**&#x200B;위치 검색을 실행해야 하는 위치
   * 선택 **대화 상자를** 사용하여 AEM에서 위치 선택
   * 비워 둔 경우 현재 페이지 사용

#### 태그 {#tags}

특정 위치 아래의 특정 태그와 일치하는 페이지를 사용하여 목록을 작성할 수 있습니다.

![](assets/chlimage_1-42.png)

* **상위 페이지태그**&#x200B;일치를 시작해야 하는 위치
   * 선택 **대화 상자를** 사용하여 AEM에서 위치 선택
   * 비워 둔 경우 현재 페이지 사용
* **태그**&#x200B;일치해야 하는 태그
   * 찾아보기 **대화 상자를** 사용하여 태그 선택
* **일치목록에**&#x200B;포함할 페이지의 자격을 규정하는 일치 유형을 정의합니다.
   * **임의의 태그**
   * **모든 태그**

#### 정렬 옵션 {#sort-options}

목록 작성 방법에 관계없이 항상 정의할 수 있는 특정 정렬 옵션이 있습니다.

![](assets/chlimage_1-43.png)

* **정렬 기준요소를**&#x200B;정렬하는 방법
   * **제목**
   * **마지막으로 수정한 날짜**
* **정렬**&#x200B;순서항목을 주문해야 하는 순서
   * **오름차순**
   * **내림차순**
* **최대**&#x200B;항목 목록에 표시되는 최대 항목 수입니다.
   * 모든 항목을 반환하려면 비워 둡니다.

### 항목 설정 탭 {#item-settings-tab}

항목 설정 탭을 사용하여 목록 요소의 서식을 구성할 수 있습니다.

![](assets/chlimage_1-44.png)

* **항목**&#x200B;연결 항목을 해당 페이지에 연결
* **설명**&#x200B;표시링크 항목의 설명 표시
* **날짜**&#x200B;표시링크 항목의 수정 날짜 표시

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 사용하여 컨텐츠 작성자가 사용할 수 있는 항목 설정뿐만 아니라 사용할 수 있는 목록 유형을 정의할 수 있습니다.

### 목록 설정 {#list-settings}

목록 **설정** 탭에서 날짜 형식을 정의할 수 있을 뿐만 아니라 컨텐츠 작성자에게 구성 요소에서 사용할 수 있는 목록 유형을 정의할 수 있습니다.

![](assets/chlimage_1-45.png)

* **날짜**&#x200B;형식 마지막 수정 날짜 표시에 사용할 형식
* **하위**&#x200B;비활성화 구성 요소에서 하위 목록 유형 비활성화
* **정적**&#x200B;비활성화 구성 요소에서 정적 목록 유형 비활성화
* **검색**&#x200B;비활성화 구성 요소에서 검색 목록 유형 비활성화
* **태그**&#x200B;비활성화 구성 요소에서 태그 목록 유형 비활성화

### 항목 설정 {#item-settings}

항목 **설정** 탭에서 컨텐츠 작성자에 대한 구성 요소에서 사용할 수 있어야 하는 개별 목록 요소에 대한 서식 옵션을 정의할 수 있습니다.

![](assets/chlimage_1-46.png)

* **링크**&#x200B;항목 [편집 대화 상자의 링크 항목 활성화 옵션](#edit-dialog)
* **설명**&#x200B;표시 [편집 대화 상자에서 설명 표시 옵션 사용](#edit-dialog)
* **편집**&#x200B;대화 상자에서 날짜 표시 [활성화 옵션 표시](#edit-dialog)

### 스타일 탭 {#styles-tab}

이미지 구성 요소는 AEM 스타일 [시스템을 지원합니다](authoring.md#component-styling).
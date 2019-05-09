---
title: 구성 요소 나열
seo-title: 구성 요소 나열
description: 'null'
seo-description: 핵심 구성 요소 목록 구성 요소를 사용하면 정적 목록과 동적 목록을 쉽게 만들 수 있습니다.
uuid: 50 a 572 e 8-b 444-4 f 7 d -82 bc -5 a 93 ebb 4 be 95
contentOwner: 사용자
content-type: 참조
topic-tags: 저작
products: sg_ Experiencemanager/Corecomponents-new
discoiquuid: 89053323-6221-46 ED -896 A -31 A 42 C 55282 E
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
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# 구성 요소 나열{#list-component}

핵심 구성 요소 목록 구성 요소를 사용하면 정적 목록과 동적 목록을 쉽게 만들 수 있습니다.

## 사용량 {#usage}

목록 구성 요소는 하위 페이지의 동적 목록 또는 임의 정의된 임의 항목의 정적 목록을 만드는 데 사용할 수 있습니다. 사용 가능한 목록 유형 및 서식 옵션은 [디자인 대화 상자의 템플릿 작성자가 정의할](#design-dialog)수 있습니다. 컨텐츠 편집기에서는 사용 가능한 목록 유형과 [편집 대화 상자에서 목록 요소의 형식을 지정하는 방법을](#edit-dialog)선택할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

목록 구성 요소의 현재 버전은 2018 년 1 월에 핵심 구성 요소의 릴리스 2.0.0에 도입된 v 2 이며, 이 문서에서는 설명합니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서에 대한 링크를 제공합니다.

| 구성 요소 버전 | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | 호환 가능 | 호환 가능 | 호환 가능 |
| [v1](list-v1.md) | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 문서 [코어 구성 요소 버전을 참조하십시오](versions.md).

## 샘플 구성 요소 출력 {#sample-component-output}

[다음은 We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html)에서 가져온 샘플입니다.

### 스크린샷 {#screenshot}

![](assets/screen_shot_2018-01-12at105924.png)

### 구성 요소 라이브러리

목록 구성 요소를 경험하고 HTML 및 JSON 출력뿐만 아니라 구성 옵션의 예를 보려면 [구성 요소 라이브러리를 참조하십시오](http://opensource.adobe.com/aem-core-wcm-components/library/list.html).

### 기술 세부 정보 {#technical-details}

목록 구성 요소에 [대한 최신 기술 설명서는 Github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/list/v2/list)에서 찾을 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서를](developing.md)참조하십시오.

## 편집 대화 상자 {#edit-dialog}

컨텐츠 작성자는 편집 대화 상자를 사용하여 목록 및 목록 항목을 구성할 수 있습니다.

### 목록 설정 탭 {#list-settings-tab}

목록은 다른 방식으로 빌드할 수 있습니다.

* [하위 페이지](#child-pages)
* [고정 목록](#fixed-list)
* [검색](#search-options)
* [태그](#tags)

목록이 구성되는 방식에 관계없이 항상 구성할 수 있는 [정렬 옵션이](#sort-options) 있습니다.

![](assets/chlimage_1-38.png)

컨텐츠 작성자가 목록을 작성하는 방법에 따라 추가 구성 옵션이 변경됩니다.

#### 하위 페이지 {#child-pages}

현재 페이지 또는 다른 페이지의 하위 페이지로 목록을 작성할 수 있습니다.

![](assets/chlimage_1-39.png)

* **상위 페이지**
   * 하위 페이지가 목록을 만들어야 하는 페이지
   * 현재 페이지를 사용하려면 비워 두십시오.

* **하위 깊이**계층 구조에서 아래쪽으로 얼마나 많이 사용해야 합니까?

#### 고정 목록 {#fixed-list}

목록은 고정된 항목 목록을 사용하여 작성할 수 있습니다.

![](assets/chlimage_1-40.png)

**추가** 단추를 탭하거나 클릭하여 목록에 새 항목을 삽입합니다.

* 목록에 있는 항목에 대한 텍스트를 입력하거나 **선택 대화 상자를** 사용하여 AEM에서 항목을 선택합니다.
* 드래그 핸들을 사용하여 목록의 항목을 다시 정렬합니다.
* 휴지통 아이콘을 사용하여 목록에서 항목을 삭제합니다.

#### 검색 {#search-options}

AEM 컨텐츠 검색 결과를 사용하여 목록을 작성할 수 있습니다.

![](assets/chlimage_1-41.png)

* **검색 쿼리를**
사용하여 전체 텍스트 검색이 실행될 문자열을 검색합니다.
* **검색을 실행해야**하는 위치 검색
   * **선택 대화 상자를** 사용하여 AEM에서 위치를 선택합니다.
   * 비워 두면 현재 페이지 사용

#### 태그 {#tags}

특정 위치 아래의 특정 태그와 일치하는 페이지를 사용하여 목록을 작성할 수 있습니다.

![](assets/chlimage_1-42.png)

* **태그 일치를**시작해야 하는 상위 페이지
   * **선택 대화 상자를** 사용하여 AEM에서 위치를 선택합니다.
   * 비워 두면 현재 페이지 사용
* **태그가**일치해야 하는 태그
   * **탐색** 대화 상자를 사용하여 태그를 선택합니다.
* **일치 -**
목록에 포함할 페이지 자격이 있는 일치 항목을 정의합니다.
   * **임의의 태그**
   * **모든 태그**

#### 정렬 옵션 {#sort-options}

목록을 작성하는 방법에 관계없이 항상 정의할 수 있는 특정 정렬 옵션이 있습니다.

![](assets/chlimage_1-43.png)

* **요소의 순서 지정**방법
   * **제목**
   * **마지막으로 수정한 날짜**
* **정렬 순서**
항목을 주문해야 하는 순서
   * **오름차순**
   * **내림차순**
* **최대 항목**
목록에 표시되는 최대 항목 수입니다.
   * 모든 항목을 반환하려면 비워 둡니다.

### 항목 설정 탭 {#item-settings-tab}

항목 설정 탭을 사용하여 목록 요소의 서식을 구성할 수 있습니다.

![](assets/chlimage_1-44.png)

* **항목을**해당 페이지에 링크 항목
연결
* **설명**
표시 링크 항목에 대한 설명 표시
* **날짜**항목의 수정 날짜 표시 날짜
표시

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 사용하여 컨텐츠 작성자가 사용할 수 있는 목록과 사용 가능한 항목 설정을 정의할 수 있습니다.

### 목록 설정 {#list-settings}

**목록 설정** 탭에서는 컨텐츠 작성자에게 구성 요소에서 사용할 수 있어야 하는 목록과 날짜 형식을 정의할 수 있습니다.

![](assets/chlimage_1-45.png)

* **마지막 수정 날짜 표시에 사용할 날짜 형식**
형식
* **하위**
비활성화 구성 요소에서 하위 목록 유형을 비활성화합니다.
* **정적**
비활성화 구성 요소의 정적 목록 유형 비활성화
* **검색**
비활성화 구성 요소에서 검색 목록 유형을 비활성화합니다.
* **구성 요소에서 태그**
비활성화 태그 목록 유형 비활성화

### 항목 설정 {#item-settings}

**[항목 설정** ] 탭에서 컨텐츠 작성자에 대해 구성 요소에서 사용할 수 있어야 하는 개별 목록 요소에 대한 서식 지정 옵션을 정의할 수 있습니다.

![](assets/chlimage_1-46.png)

* **항목**
연결 [편집 대화 상자에서 항목 연결 옵션](#edit-dialog)
* **설명**
표시 편집 대화 상자에 설명 표시 [옵션](#edit-dialog)
* **편집 대화 상자에서 날짜**표시 활성화 [날짜
표시](#edit-dialog)

### 스타일 탭 {#styles-tab}

이미지 구성 요소는 AEM [스타일 시스템을 지원합니다](authoring.md#component-styling).
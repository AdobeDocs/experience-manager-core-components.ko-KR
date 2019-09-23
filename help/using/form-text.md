---
title: 양식 텍스트 구성 요소
seo-title: 양식 텍스트 구성 요소
description: 'null'
seo-description: 핵심 구성 요소 양식 텍스트 구성 요소를 사용하면 양식 텍스트를 입력하여 제출할 수 있습니다.
uuid: f2418d55-0b59-4c7c-a541-d12dda4db4cf
contentOwner: 사용자
content-type: 참조
topic-tags: authoring
products: SG_EXPERIENCEMANAGER/CORCOMPONENTS-new
discoiquuid: 3a970c4b-806b-4a0a-b6b8-b3dca4e9f136
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
source-git-commit: 1243d6cc1b0b015ee2f37ae89d0e2e42d366cc02

---


# 양식 텍스트 구성 요소{#form-text-component}

핵심 구성 요소 양식 텍스트 구성 요소를 사용하면 양식 텍스트를 입력하여 제출할 수 있습니다.

## 사용량 {#usage}

양식 텍스트 구성 요소를 사용하면 다양한 유형의 텍스트를 제출할 수 있으며 [양식 컨테이너 구성 요소와](form-container.md)함께 사용할 수 있습니다. 텍스트 유효성 검사, 레이블 및 도움말 메시지 유형은 [구성 대화 상자의](#configure-dialog)컨텐츠 편집기에서 정의할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

양식 텍스트 구성 요소의 현재 버전은 v2이며, 이 버전은 2018년 1월 핵심 구성 요소 릴리스 2.0.0과 함께 도입되었으며 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소 버전이 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | 호환 가능 | 호환 가능 | 호환 가능 |
| [v1](form-text-v1.md) | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 핵심 구성 요소 [버전을 참조하십시오](versions.md).

## 샘플 구성 요소 출력 {#sample-component-output}

다음은 We.Retail에서 [가져온 샘플입니다](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### 스크린샷 {#screenshot}

![](assets/chlimage_1-22.png)

### HTML {#html}

```
<div class="text aem-GridColumn aem-GridColumn--default--12">
   <div class="cmp-form-text">
      <label for="form-text-2146967">How many pieces of toast would you like?
      </label>
   <input class="cmp-form-text__text" type="number" id="form-text-2146967" name="pieces">
   </div>
</div>
```

### JSON {#json}

```
"text":{  
                     "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                     "id":"form-text-2146967",
                     "title":"How many pieces of toast would you like?",
                     "name":"pieces",
                     "value":"",
                     "helpMessage":"",
                     "type":"number",
                     "readOnly":false,
                     "required":false,
                     "requiredMessage":"",
                     "constraintMessage":"",
                     "rows":2,
                     "defaultValue":"",
                     ":type":"core/wcm/components/form/text/v2/text"
                  }
```

### 기술 정보 {#technical-details}

양식 텍스트 구성 요소에 대한 최신 기술 문서는 GitHub에서 [찾을 수 있습니다](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v2/text).

핵심 구성 요소 개발에 대한 자세한 내용은 핵심 구성 요소 개발자 [설명서를](developing.md)참조하십시오.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자에서는 컨텐츠 작성자가 입력할 텍스트 유형과 기본값 및 레이블을 정의할 수 있습니다.

### 기본 탭 {#main-tab}

![](assets/chlimage_1-23.png)

* **제한**&#x200B;입력할 텍스트 유형이며
   * **텍스트**
   * **텍스트 영역**
   * **이메일**
   * **전화**
   * **날짜**
   * **번호**
   * **암호**
* **텍스트**&#x200B;라인텍스트 영역에 표시할 줄 수(제한 **조건이 텍스트 영역으로** 설정된 경우에만 **표시됨**)
* **레이블필드에**&#x200B;표시할 레이블입니다.
* **레이블이 표시되지**&#x200B;않도록 숨기기레이블은 액세서빌러티 용도로만 필요하고 필드에 대한 추가 시각적 정보를 포함하지 않는 경우 필요합니다.
* **요소**&#x200B;이름양식 데이터로 제출된 필드의 이름입니다.
* **값**&#x200B;필드에 미리 채워지는 기본값

### 탭 정보 {#about-tab}

![](assets/chlimage_1-24.png)

* **도움말**&#x200B;메시지필드에 입력할 수 있는 항목에 대한 힌트
* **도움말 메시지를 자리 표시자로**&#x200B;표시양식 입력에 초점이 맞지 않고 비어 있는 경우 도움말 메시지를 표시하려면

### 제한 탭 {#constraints-tab}

![](assets/chlimage_1-25.png)

* **제한 메시지**
   * 값이 선택된 유형에 대한 유효성을 검사하지 못할 경우 양식을 제출할 때 도구 설명으로 표시되는 메시지
   * 텍스트 및 텍스트 **영역** 제한 **유형에 대해** 표시되지 않음
* **필수**&#x200B;선택한 경우 양식을 제출하기 전에 값을 입력해야 합니다.
* **읽기 전용**&#x200B;이 옵션을 선택하면 사용자가 필드의 값을 수정할 수 없습니다

## 디자인 대화 상자 {#design-dialog}

양식 텍스트 구성 요소에 대한 디자인 대화 상자가 없습니다.
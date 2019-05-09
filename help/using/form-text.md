---
title: 양식 텍스트 구성 요소
seo-title: 양식 텍스트 구성 요소
description: 'null'
seo-description: 핵심 구성 요소 양식 텍스트 구성 요소를 사용하면 양식 텍스트를 제출할 수 있습니다.
uuid: F 2418 D 55-0 B 59-4 C 7 C-A 541-D 12 DDA 4 DB 4 CF
contentOwner: 사용자
content-type: 참조
topic-tags: 저작
products: sg_ Experiencemanager/Corecomponents-new
discoiquuid: 3 A 970 C 4 B -806 B -4 A 0 A-B 6 B 8-B 3 DCA 4 E 9 F 136
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


# 양식 텍스트 구성 요소{#form-text-component}

핵심 구성 요소 양식 텍스트 구성 요소를 사용하면 양식 텍스트를 제출할 수 있습니다.

## 사용량 {#usage}

양식 텍스트 구성 요소는 서로 다른 유형의 텍스트를 제출할 수 있도록 하며 [양식 컨테이너 구성 요소와 함께 사용됩니다](form-container.md). 텍스트 유효성 검사, 레이블 및 도움말 메시지의 유형은 [구성 대화 상자의 컨텐츠 편집기에서 정의할](#configure-dialog)수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

양식 텍스트 구성 요소의 현재 버전은 2018 년 1 월에 핵심 구성 요소의 릴리스 2.0.0에 도입된 v 2 이며, 이 문서에서는 설명합니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서에 대한 링크를 제공합니다.

| 구성 요소 버전 | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | 호환 가능 | 호환 가능 | 호환 가능 |
| [v1](form-text-v1.md) | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 문서 [코어 구성 요소 버전을 참조하십시오](versions.md).

## 샘플 구성 요소 출력 {#sample-component-output}

[다음은 We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html)에서 가져온 샘플입니다.

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

### 기술 세부 정보 {#technical-details}

양식 텍스트 구성 요소에 [대한 최신 기술 설명서는 Github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v2/text)에서 찾을 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서를](developing.md)참조하십시오.

## 구성 대화 상자 {#configure-dialog}

컨텐츠 작성자는 구성 대화 상자를 사용하여 입력할 텍스트 유형 및 기본값 및 레이블을 정의할 수 있습니다.

### 기본 탭 {#main-tab}

![](assets/chlimage_1-23.png)

* **제한입력할**텍스트 유형을 제한하고
   * **텍스트**
   * **텍스트 영역**
   * **이메일**
   * **전화**
   * **날짜**
   * **번호**
   * **암호**
* **텍스트 줄**
텍스트 영역에 표시할 줄 수 ( **제한이** **텍스트 영역으로 설정된 경우에만 표시됨**)
* **레이블필드에**표시할 레이블입니다.
* **액세서빌러티 목적이**액세서빌러티 목적으로만 필요한 경우 레이블을 표시하고 필드에 대한 추가 시각적 정보를 부여하지 않습니다.
* **요소 이름**
양식 데이터와 함께 제출된 필드 이름
* **필드에 미리 채워진 값**
기본값

### 탭 정보 {#about-tab}

![](assets/chlimage_1-24.png)

* **필드에 입력할**수 있는 내용을 사용자에게 알려주는 도움말 메시지
* **비어 있고 초점이 아닌 양식 입력 내부에 도움말 메시지를**표시하는 자리 표시자로 도움말 메시지를 표시할 수
있습니다.

### 제한 탭 {#constraints-tab}

![](assets/chlimage_1-25.png)

* **제한 메시지**
   * 값이 선택된 유형에 대한 유효성을 검사하지 못할 경우 양식을 제출할 때 도구 설명으로 표시되는 메시지
   * **텍스트** 및 **텍스트 영역** 제한 유형에 표시되지 않음
* **필수**사용자는 양식을 제출하기 전에 값을 입력해야 합니다.
* **읽기 전용 사용자가 필드 값을 수정할 수 없는**경우

## 디자인 대화 상자 {#design-dialog}

양식 텍스트 구성 요소에 대한 디자인 대화 상자는 없습니다.
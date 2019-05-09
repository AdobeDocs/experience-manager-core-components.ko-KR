---
title: 양식 텍스트 구성 요소 (v 1)
seo-title: 양식 텍스트 구성 요소 (v 1)
description: 'null'
seo-description: 핵심 구성 요소 양식 텍스트 구성 요소를 사용하면 양식 텍스트를 제출할 수 있습니다.
uuid: 30123 ABA -57 A 8-4 ED 4-93 CB -6 A 3 D 2 EDFF 9 A 7
content-type: 참조
products: sg_ Experiencemanager/Corecomponents-new
discoiquuid: BD 4 E 9930-4 D 81-49 AE-A 3 D 1-9 A 8740418 DAE
index: n
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# 양식 텍스트 구성 요소 (v 1){#form-text-component-v}

핵심 구성 요소 양식 텍스트 구성 요소를 사용하면 양식 텍스트를 제출할 수 있습니다.

## 사용량 {#usage}

양식 텍스트 구성 요소는 서로 다른 유형의 텍스트를 제출할 수 있도록 하며 [양식 컨테이너 구성 요소와 함께 사용됩니다](form-container.md).

텍스트 유효성 검사, 레이블 및 도움말 메시지의 유형은 [구성 대화 상자의 컨텐츠 편집기에서 정의할](form-text-v1.md#main-pars_title)수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

이 문서에서는 원래 AEM 6.3 이 있는 핵심 구성 요소의 릴리스 1.0.0에 도입된 양식 텍스트 구성 요소의 v 1에 대해 설명합니다.

다음 표에는 양식 텍스트 구성 요소의 v 1 호환성이 나와 있습니다.

| AEM 버전 | 양식 텍스트 구성 요소 v 1 |
|--- |--- |
| 6.3 | 호환 가능 |
| 6.4 | 호환 가능 |

>[!CAUTION]
>
>이 문서에서는 양식 텍스트 구성 요소의 v 1를 설명합니다.
>
>양식 텍스트 구성 요소의 현재 버전에 대한 자세한 내용은 [양식 텍스트 구성 요소](form-text.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

[다음은 We. Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html)에서 가져온 샘플입니다.

### 스크린샷 {#screenshot}

![](assets/chlimage_1-22.png)

### HTML {#html}

```
<div class="cmp cmp-form aem-GridColumn aem-GridColumn--default--12">
 <form method="POST" action="/content/we-retail/us/en/experience.html" id="new_form" name="new_form" enctype="multipart/form-data" class="aem-Grid aem-Grid--12 aem-Grid--default--12 ">
     <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container">
     <div class="cmp cmp-form-field aem-GridColumn aem-GridColumn--default--12">
   <div class="form-group">
       <label for="form-text-978484744">How many pieces of toast would you like?</label>
          <input type="number" id="form-text-978484744" name="pieces">
   </div>
  </div>
 </form>
</div>
```

### JSON {#json}

```
"container": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "columnCount": 12,
              "gridClassNames": "aem-Grid aem-Grid--12 aem-Grid--default--12",
              ":items": {
                "text": {
                  "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
                  ":type": "weretail/components/form/text",
                  "name": "piecesOfToast",
                  "jcr:title": "How many pieces of toast would you like?",
                  "type": "number",
                  "rows": "2"
                }
              },
              ":itemsOrder": [
                "text"
              ],
              ":type": "weretail/components/form/container"
            }
```

>[!NOTE]
>
>핵심 구성 요소에서 JSON 내보내기를 사용하려면 핵심 구성 요소의 릴리스 1.1.0 이 필요합니다. 자세한 내용은 [핵심 구성 요소 v 1](versions.md#main-pars_title_236368006) 의 호환성 정보를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

컨텐츠 작성자는 구성 대화 상자를 사용하여 입력할 텍스트 유형 및 기본값 및 레이블을 정의할 수 있습니다.

### 기본 {#main}

![](assets/chlimage_1-23.png)

* **제한** - 입력할 텍스트 유형 및

   * **텍스트**
   * **텍스트 영역**
   * **이메일**
   * **전화**
   * **날짜**
   * **번호**
   * **암호**

* **텍스트 줄** - 텍스트 영역에 표시할 줄 수 ( **제한이** **텍스트 영역으로 설정된 경우에만 표시됨**)

* **레이블** - 필드에 대해 표시되는 레이블입니다.
* **레이블이 표시되는** 것을 숨깁니다. 레이블은 액세서빌러티 목적으로만 필요한 경우 필요하며 필드에 대한 추가 시각적 정보를 부여하지 않습니다.
* **요소 이름** - 양식 데이터와 함께 제출된 필드 이름
* **값** - 필드에 미리 채워진 기본값

### 정보 {#about}

![](assets/chlimage_1-24.png)

* **도움말 메시지** - 필드에 입력할 수 있는 사용자의 힌트입니다.
* **도움말 메시지를 자리 표시자로** 표시 - 비어 있고 초점이 아닌 양식 입력 내부에 도움말 메시지를 표시하려면

### 제한 {#constraints}

![](assets/chlimage_1-25.png)

* **제한 메시지**

   * 값이 선택된 유형에 대한 유효성을 검사하지 못할 경우 양식을 제출할 때 도구 설명으로 표시되는 메시지
   * **텍스트** 및 **텍스트 영역** 제한 유형에 표시되지 않음

* **필수** - 선택한 경우 양식을 제출하기 전에 값을 입력해야 합니다.
* **읽기 전용** - 선택한 경우 해당 필드의 값을 수정할 수 없습니다.

## 디자인 대화 상자 {#design-dialog}

양식 텍스트 구성 요소에 대한 디자인 대화 상자는 없습니다.

## 기술 세부 정보 {#technical-details}

양식 텍스트 구성 요소에 [대한 최신 기술 설명서는 Github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v1/text)에서 찾을 수 있습니다.

Github에서 전체 핵심 구성 요소 프로젝트를 다운로드할 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서를](developing.md)참조하십시오.

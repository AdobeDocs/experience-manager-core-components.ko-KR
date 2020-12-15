---
title: 양식 텍스트 구성 요소(v1)
description: 핵심 구성 요소 양식 텍스트 구성 요소를 사용하면 양식 텍스트를 입력하여 제출할 수 있습니다.
index: n
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 8%

---


# 양식 텍스트 구성 요소(v1) {#form-text-component-v}

핵심 구성 요소 양식 텍스트 구성 요소를 사용하면 양식 텍스트를 입력하여 제출할 수 있습니다.

## 사용량 {#usage}

양식 텍스트 구성 요소는 다양한 유형의 텍스트를 제출할 수 있으며, 이 구성 요소는 [양식 컨테이너 구성 요소](form-container-v1.md)와 함께 사용하기 위한 것입니다.

텍스트 유효성 검사, 레이블 및 도움말 메시지의 유형은 [구성 대화 상자](#configure-dialog)에서 내용 편집기에서 정의할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

이 문서에서는 AEM 6.3의 핵심 구성 요소 릴리스 1.0.0에 처음 소개된 양식 텍스트 구성 요소의 v1에 대해 설명합니다.

다음 표는 양식 텍스트 구성 요소의 v1 호환성을 보여줍니다.

| AEM 버전 | 양식 텍스트 구성 요소 v1 |
|--- |--- |
| 6.3 | 호환 가능 |
| 6.4 | 호환 가능 |

>[!CAUTION]
>
>이 문서에서는 양식 텍스트 구성 요소의 v1에 대해 설명합니다.
>
>양식 텍스트 구성 요소의 현재 버전에 대한 자세한 내용은 [양식 텍스트 구성 요소](/help/components/forms/form-text.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

다음은 [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html)에서 가져온 샘플입니다.

### 스크린샷 {#screenshot}

![](/help/assets/chlimage_1-22.png)

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
>핵심 구성 요소에서 JSON 내보내기를 사용하려면 핵심 구성 요소의 릴리스 1.1.0이 필요합니다. 자세한 내용은 핵심 구성 요소 v1[에 대한 호환성 정보를 참조하십시오.](/help/versions.md)

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자를 사용하면 컨텐츠 작성자가 입력할 텍스트 유형과 기본값 및 레이블을 정의할 수 있습니다.

### 기본 {#main}

![](/help/assets/chlimage_1-23.png)

* **제한**  - 입력할 텍스트 유형이며 다음에 대해 유효성 검사가 수행됩니다

   * **텍스트**
   * **텍스트 영역**
   * **이메일**
   * **전화**
   * **날짜**
   * **번호**
   * **암호**

* **텍스트 행**  - 텍스트 영역에 표시할 행 수입니다( **** 제한이  **텍스트 영역으로 설정된 경우에만 표시됨**).

* **레이블**  - 필드에 표시할 레이블입니다.
* **레이블 표시**  안 함 - 액세스 가능성 목적으로만 레이블이 필요하고 필드에 대한 추가적인 시각적 정보를 포함하지 않는 경우에 필요합니다.
* **요소 이름**  - 양식 데이터와 함께 제출한 필드의 이름입니다.
* **값**  - 필드에 미리 채워지는 기본값

### 정보 {#about}

![](/help/assets/chlimage_1-24.png)

* **도움말 메시지**  - 필드에 입력할 수 있는 항목의 힌트입니다.
* **도움말 메시지를 자리**  표시자로 표시 - 비어 있고 초점이 맞지 않을 때 양식 입력 내에 도움말 메시지를 표시하려면

### 제한 {#constraints}

![](/help/assets/chlimage_1-25.png)

* **제한 메시지**

   * 값이 선택된 유형에 대한 유효성을 검사하지 못할 경우 양식을 제출할 때 도구 설명으로 표시되는 메시지
   * **텍스트** 및 **텍스트 영역** 제약 조건 유형에 표시되지 않음

* **필수**  - 선택한 경우 양식을 제출하기 전에 사용자가 값을 입력해야 합니다.
* **읽기 전용**  만들기 - 선택한 경우 사용자가 필드의 값을 수정할 수 없습니다.

## 디자인 대화 상자 {#design-dialog}

양식 텍스트 구성 요소에 대한 디자인 대화 상자가 없습니다.

## 기술 세부 정보 {#technical-details}

양식 텍스트 구성 요소 [에 대한 최신 기술 문서는 GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v1/text)에서 찾을 수 있습니다.

전체 핵심 구성 요소 프로젝트를 GitHub에서 다운로드할 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)에서 확인할 수 있습니다.

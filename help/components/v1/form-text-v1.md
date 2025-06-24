---
title: 양식 텍스트 구성 요소 (v1)
description: 핵심 구성 요소의 양식 텍스트 구성 요소를 사용하여 제출용 양식 텍스트를 입력합니다.
index: n
role: Architect, Developer, Admin, User
exl-id: d6fbc596-cb42-4478-8a3c-aa5aead3be0a
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 100%

---


# 양식 텍스트 구성 요소 (v1) {#form-text-component-v}

핵심 구성 요소의 양식 텍스트 구성 요소를 사용하여 제출용 양식 텍스트를 입력합니다.

## 사용량 {#usage}

양식 텍스트 구성 요소를 사용하여 다양한 유형의 텍스트를 제출하고, [양식 컨테이너 구성 요소](form-container-v1.md)와 함께 이 구성 요소를 사용할 수 있습니다.

콘텐츠 편집기는 [구성 대화 상자](#configure-dialog)에서 텍스트 유효성 검사 유형, 라벨 및 도움말 메시지를 정의할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

이 문서에서는 AEM 6.3을 포함하는 핵심 구성 요소 릴리스 1.0.0과 함께 최초 도입된 양식 텍스트 구성 요소 v1에 대해 설명합니다.

다음 테이블에서 양식 텍스트 구성 요소 v1의 호환성을 확인할 수 있습니다.

| AEM 버전 | 양식 텍스트 구성 요소 v1 |
|--- |--- |
| 6.3 | 호환 가능 |
| 6.4 | 호환 가능 |

>[!CAUTION]
>
>이 문서에서는 양식 텍스트 구성 요소 v1에 대해 설명합니다.
>
>현재 버전의 양식 텍스트 구성 요소에 대한 자세한 내용은 [양식 텍스트 구성 요소](/help/components/forms/form-text.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

다음은 [We.Retail](https://helpx.adobe.com/kr/experience-manager/6-4/sites/developing/using/we-retail.html)에서 얻은 샘플입니다.

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
>핵심 구성 요소에서 JSON을 내보내는 데 핵심 구성 요소 릴리스 1.1.0이 필요합니다. 자세한 내용은 [핵심 구성 요소 v1에 대한 호환성 정보](/help/versions.md)를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

콘텐츠 작성자는 구성 대화 상자를 통해 입력할 텍스트 유형뿐만 아니라 기본값 및 라벨을 정의할 수 있습니다.

### 메인 {#main}

![](/help/assets/chlimage_1-23.png)

* **제한** - 입력할 텍스트 유형은 다음을 통해 유효성이 확인됩니다.

   * **텍스트**
   * **텍스트 영역**
   * **이메일**
   * **전화**
   * **날짜**
   * **번호**
   * **암호**

* **텍스트 라인** - 텍스트 영역에 표시될 라인 수(**제한**&#x200B;이 **텍스트 영역**&#x200B;으로 설정될 경우에만 표시)

* **라벨** - 필드에 표시될 라벨
* **라벨이 표시되지 않도록 숨기기** - 손쉬운 사용을 위해 라벨이 필요한 경우. 필드에 대해 시각적 정보를 추가로 제공하지 않음
* **요소 이름** - 양식 데이터로 제출된 필드의 이름
* **값** - 필드에 미리 채워진 기본값

### 정보 {#about}

![](/help/assets/chlimage_1-24.png)

* **도움말 메시지** - 필드에 입력할 수 있는 것에 대한 사용자용 힌트
* **도움말 메시지를 자리 표시자로 표시** - 양식이 비어 있고 포커스를 두지 않았을 때 양식 입력 내부에 도움말 메시지를 표시할지 여부

### 제한 {#constraints}

![](/help/assets/chlimage_1-25.png)

* **제한 메시지**

   * 값이 선택된 유형에 대한 유효성을 검사하지 못할 경우 양식을 제출할 때 도구 설명으로 표시되는 메시지
   * **텍스트** 및 **텍스트 영역** 제한 유형에 표시되지 않음

* **필수** - 이 옵션을 선택하면 사용자는 양식을 제출하기 전에 값을 채워야 함
* **읽기 전용** - 이 옵션을 선택하면 사용자는 필드 값을 수정할 수 없음

## 디자인 대화 상자 {#design-dialog}

양식 텍스트 구성 요소용 디자인 대화 상자는 없습니다.

## 기술 세부 사항 {#technical-details}

양식 텍스트 구성 요소에 대한 최신 기술 설명서는[ GitHub에서 확인할 수 있습니다](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v1/text).

GitHub에서 전체 핵심 구성 요소 프로젝트를 다운로드할 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

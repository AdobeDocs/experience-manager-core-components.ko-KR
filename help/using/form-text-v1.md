---
title: 양식 텍스트 구성 요소(v1)
seo-title: 양식 텍스트 구성 요소(v1)
description: 'null'
seo-description: 핵심 구성 요소 양식 텍스트 구성 요소를 사용하면 양식 텍스트를 입력하여 제출할 수 있습니다.
uuid: 30123aba-57a8-4ed4-93cb-6a3d2edff9a7
content-type: 참조
products: SG_EXPERIENCEMANAGER/CORCOMPONENTS-new
discoiquuid: bd4e9930-4d81-49ae-a3d1-9a8740418dae
index: n
translation-type: tm+mt
source-git-commit: 4e74f10e2a4119484a597178dc4577b399833dbf

---


# Form Text Component (v1){#form-text-component-v}

핵심 구성 요소 양식 텍스트 구성 요소를 사용하면 양식 텍스트를 입력하여 제출할 수 있습니다.

## 사용량 {#usage}

양식 텍스트 구성 요소를 사용하면 다양한 유형의 텍스트를 제출할 수 있으며 [양식 컨테이너 구성 요소와](form-container.md)함께 사용할 수 있습니다.

텍스트 유효성 검사, 레이블 및 도움말 메시지 유형은 [구성 대화 상자의](form-text-v1.md#main-pars_title)컨텐츠 편집기에서 정의할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

이 문서에서는 AEM 6.3의 핵심 구성 요소 릴리스 1.0.0에서 처음 소개된 양식 텍스트 구성 요소의 v1에 대해 설명합니다.

다음 표에는 양식 텍스트 구성 요소의 v1 호환성이 나와 있습니다.

| AEM 버전 | 양식 텍스트 구성 요소 v1 |
|--- |--- |
| 6.3 | 호환 가능 |
| 6.4 | 호환 가능 |

>[!CAUTION]
>
>이 문서에서는 양식 텍스트 구성 요소의 v1에 대해 설명합니다.
>
>양식 텍스트 구성 요소의 현재 버전에 대한 자세한 내용은 양식 텍스트 구성 [요소](form-text.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

다음은 We.Retail에서 [가져온 샘플입니다](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

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
>핵심 구성 요소에서 JSON을 내보내려면 핵심 구성 요소 릴리스 1.1.0이 필요합니다. 자세한 내용은 핵심 구성 요소 v1의 [](versions.md#main-pars_title_236368006) 호환성 정보를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자에서는 컨텐츠 작성자가 입력할 텍스트 유형과 기본값 및 레이블을 정의할 수 있습니다.

### 기본 {#main}

![](assets/chlimage_1-23.png)

* **제한** - 입력할 텍스트 유형이며

   * **텍스트**
   * **텍스트 영역**
   * **이메일**
   * **전화**
   * **날짜**
   * **번호**
   * **암호**

* **텍스트 줄** - 텍스트 영역에 표시할 줄 수(제한 조건이 텍스트 **영역으로** 설정된 경우에만 **표시됨**)

* **레이블** - 필드에 표시할 레이블입니다.
* **레이블 표시** 안 함 - 레이블을 액세서빌러티 용도로만 사용하고 필드에 대한 추가 시각적 정보를 포함하지 않는 경우 필요합니다.
* **요소** 이름 - 양식 데이터로 제출된 필드의 이름
* **값** - 필드에 미리 채워진 기본값

### 정보 {#about}

![](assets/chlimage_1-24.png)

* **도움말 메시지** - 필드에 입력할 수 있는 항목에 대한 힌트
* **도움말 메시지를 자리 표시자로** 표시 - 양식 입력에 초점이 맞지 않고 비어 있는 경우 도움말 메시지를 표시하려면

### 제한 {#constraints}

![](assets/chlimage_1-25.png)

* **제한 메시지**

   * 값이 선택된 유형에 대한 유효성을 검사하지 못할 경우 양식을 제출할 때 도구 설명으로 표시되는 메시지
   * 텍스트 및 텍스트 **영역** 제한 **유형에 대해** 표시되지 않음

* **필수** - 선택한 경우 사용자가 양식을 제출하기 전에 값을 입력해야 합니다.
* **읽기 전용** 만들기 - 선택한 경우 사용자가 필드의 값을 수정할 수 없습니다.

## 디자인 대화 상자 {#design-dialog}

양식 텍스트 구성 요소에 대한 디자인 대화 상자가 없습니다.

## 기술 정보 {#technical-details}

양식 텍스트 구성 요소에 대한 최신 기술 문서는 GitHub에서 [찾을 수 있습니다](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v1/text).

전체 핵심 구성 요소 프로젝트는 GitHub에서 다운로드할 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 핵심 구성 요소 개발자 [설명서를](developing.md)참조하십시오.

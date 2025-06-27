---
title: 양식 옵션 구성 요소 (v1)
description: 핵심 구성 요소의 양식 옵션 구성 요소를 통해 다양한 포맷으로 사전 정의된 옵션을 선택할 수 있습니다.
index: n
role: Architect, Developer, Admin, User
exl-id: a5e8656b-eddd-48ec-876b-39bbaa70edf6
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: ht
source-wordcount: '459'
ht-degree: 100%

---


# 양식 옵션 구성 요소 (v1) {#form-options-component-v}

핵심 구성 요소의 양식 옵션 구성 요소를 통해 다양한 포맷으로 사전 정의된 옵션을 선택할 수 있습니다.

## 사용량 {#usage}

핵심 구성 요소의 옵션 구성 요소를 사용하여 다양한 방식으로 제공되는 여러 유형의 옵션을 제출하고, [양식 컨테이너 구성 요소](form-container-v1.md)와 함께 이 구성 요소를 사용할 수 있습니다.

콘텐츠 편집기는 [구성 대화 상자](#configure-dialog)에서 옵션, 라벨 및 개별 옵션 제공을 정의할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

이 문서에서는 AEM 6.3을 포함하는 핵심 구성 요소 릴리스 1.0.0과 함께 최초 도입된 양식 옵션 구성 요소 v1에 대해 설명합니다.

다음 테이블에서 양식 옵션 구성 요소 v1의 호환성을 확인할 수 있습니다.

| 구성 요소 버전 | AEM 6.3 | AEM 6.4 |
|--- |--- |--- |
| v2 | 호환 가능 | 호환 가능 |
| v1 | 호환 가능 | 호환 가능 |

>[!CAUTION]
>
>이 문서에서는 양식 옵션 구성 요소 v1에 대해 설명합니다.
>
>현재 버전의 양식 옵션 구성 요소에 대한 자세한 내용은 [양식 옵션 구성 요소](/help/components/forms/form-options.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

다음은 [We.Retail](https://helpx.adobe.com/kr/experience-manager/6-4/sites/developing/using/we-retail.html)에서 얻은 샘플입니다.

### 스크린샷 {#screenshot}

![](/help/assets/chlimage_1-89.png)

### HTML {#html}

```
<div class="cmp cmp-form aem-GridColumn aem-GridColumn--default--12">
<form method="POST" action="/content/we-retail/us/en/experience.html" id="new_form" name="new_form" enctype="multipart/form-data" class="aem-Grid aem-Grid--12 aem-Grid--default--12 ">
    <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container">
    
    <div class="cmp cmp-options aem-GridColumn aem-GridColumn--default--12">

    <fieldset class="form-group checkbox">
        <legend>What is your favorite type of toast?</legend>
        
        <div class="checkbox-item">
            <label>
              <input type="checkbox" name="toasttypes" value="dry">
              Plain dry toast
            </label>
        </div>
<div class="checkbox-item">
            <label>
              <input type="checkbox" name="toasttypes" value="french">
              French toast
            </label>
        </div>
<div class="checkbox-item">
            <label>
              <input type="checkbox" name="toasttypes" value="texas">
              Texas toast
            </label>
        </div>

    </fieldset>
    
</div>
    
</form></div>
```

### JSON {#json}

```
"container": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "columnCount": 12,
              "gridClassNames": "aem-Grid aem-Grid--12 aem-Grid--default--12",
              ":items": {
                "options": {
                  "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
                  ":type": "weretail/components/form/options",
                  "name": "toastTypes",
                  "jcr:title": "What is your favorite type of toast?",
                  "source": "local",
                  "type": "checkbox"
                }
              },
              ":itemsOrder": [
                "options"
              ],
              ":type": "weretail/components/form/container"
            }
```

>[!NOTE]
>
>핵심 구성 요소에서 JSON을 내보내는 데 핵심 구성 요소 릴리스 1.1.0이 필요합니다. 자세한 내용은 [핵심 구성 요소 v1에 대한 호환성 정보](/help/versions.md)를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

콘텐츠 작성자는 구성 대화 상자를 통해 제공할 옵션 유형, 라벨과 사용 가능한 옵션을 정의할 수 있습니다.

![](/help/assets/chlimage_1-90.png)

* **유형**
옵션을 제공하는 방법

   * **확인란**
   * **라디오 버튼**
   * **드롭다운**
   * **다중 선택 드롭다운**

* **제목** - 옵션용 라벨로 표시되는 제목
* **이름** - 양식 데이터로 제출된 필드의 이름
* **소스** - 옵션을 정의하는 위치

   * **로컬** - 구성 요소 내에서 정의합니다.
      * **추가** 버튼을 탭하거나 클릭하여 값을 추가하고, **삭제**&#x200B;를 탭하거나 클릭하여 값을 삭제합니다.
      * **값** - 양식 제출 시 해당 옵션이 선택되면 저장되는 값
      * **텍스트** - 양식에 표시되는 옵션용 라벨
      * **활성** - 양식 로드 시 옵션이 선택된 상태로 표시됩니다.
      * **비활성** - 옵션은 선택할 수 없지만 계속 표시됩니다.
      * **목록** - AEM의 다른 곳에서 정의된 정적 목록을 옵션용으로 사용합니다.
         * **목록** - AEM 내 정적 목록의 경로
            * 검색 버튼을 사용하여 목록 리소스를 찾습니다.
      * **데이터 소스** - 데이터 소스를 옵션용으로 사용합니다.
         * **데이터 소스** - 데이터 소스의 리소스 유형
* **도움말 메시지** - 필드에 입력할 수 있는 것에 대한 사용자용 힌트

## 디자인 대화 상자 {#design-dialog}

양식 옵션 구성 요소용 디자인 대화 상자가 없습니다.

## 기술 세부 사항 {#technical-details}

양식 옵션 구성 요소에 대한 최신 기술 설명서는[ GitHub에서 확인할 수 있습니다](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/options/v1/options).

GitHub에서 전체 핵심 구성 요소 프로젝트를 다운로드할 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

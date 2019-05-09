---
title: 양식 숨김 구성 요소
seo-title: 양식 숨김 구성 요소
description: 'null'
seo-description: 핵심 구성 요소 양식 숨김 구성 요소는 숨김 필드를 표시할 수 있습니다.
uuid: 63 A 1 B 381-F 45 C -4241-B 743-DEA 8 ABD 45 E 11
contentOwner: 사용자
content-type: 참조
topic-tags: 핵심 구성 요소
discoiquuid: 36 E 49035-7641-4 BAD -8 A 61-723060032903
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


# 양식 숨김 구성 요소{#form-hidden-component}

핵심 구성 요소 양식 숨김 구성 요소는 숨김 필드를 표시할 수 있습니다.

## 사용량 {#usage}

핵심 구성 요소 양식 숨김 구성 요소는 숨김 필드를 만들어 현재 페이지에 대한 정보를 다시 AEM로 전달하며 [양식 컨테이너 구성 요소와 함께 사용할 수 있도록 만들어졌습니다](form-container.md).

필드 속성은 [구성 대화 상자의 컨텐츠 편집기에서 정의할](form-hidden.md)수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

양식 숨김 구성 요소의 현재 버전은 v 2 입니다. 이 버전은 2018 년 1 월에 핵심 구성 요소의 릴리스 2.0.0에서 처음 소개되었으며 이 문서에서는 설명합니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서에 대한 링크를 제공합니다.

| 구성 요소 버전 | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | 호환 가능 | 호환 가능 | 호환 가능 |
| [v1](form-hidden-v1.md) | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 문서 [코어 구성 요소 버전을 참조하십시오](versions.md).

## 샘플 구성 요소 출력 {#sample-component-output}

[다음은 We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html)에서 가져온 샘플입니다.

### HTML {#html}

```
<div class="cmp cmp-form aem-GridColumn aem-GridColumn--default--12">
 <form method="POST" action="/content/we-retail/us/en/experience.html" id="new_form" name="new_form" enctype="multipart/form-data" class="aem-Grid aem-Grid--12 aem-Grid--default--12 ">
  <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container">
   <div class="visible aem-GridColumn aem-GridColumn--default--12">
    <input type="hidden" id="ghostToast" name="Invisible Toast" value="ghostToast">
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
                "hidden": {
                  "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
                  ":type": "weretail/components/form/hidden",
                  "name": "Invisible Toast",
                  "id": "ghostToast",
                  "value": "ghostToast"
                }
              },
              ":itemsOrder": [
                "hidden"
              ],
              ":type": "weretail/components/form/container"
            }
```

### 기술 세부 정보 {#technical-details}

양식 숨김 구성 [요소에 대한 최신 기술 설명서는 Github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/form/hidden/v2/hidden)에서 찾을 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서를](developing.md)참조하십시오.

## 구성 대화 상자 {#configure-dialog}

컨텐츠 작성자는 구성 대화 상자를 사용하여 숨김 필드의 매개 변수를 정의할 수 있습니다.

![](assets/chlimage_1-26.png)

* **이름**
양식 데이터와 함께 제출된 필드 이름
* **값양식**
데이터와 함께 제출된 필드 값
* **식별자**
식별자는 페이지에서 고유해야 하며 이 양식 필드에 스크립트를 바인딩하는 데 사용할 수 있습니다.

양식 숨김 구성 요소에는 일반적으로 표시되는 속성이 없으므로 편집기에 있는 구성 요소의 자리 표시자는 작성자가 해당 양식 숨김 구성 요소를 식별할 수 있도록 지정된 경우 **이름** 및 **값** 필드 값을 표시합니다.

![](assets/screenshot_2018-10-19at094927.png)

## 디자인 대화 상자 {#design-dialog}

양식 숨김 구성 요소에 대한 디자인 대화 상자는 없습니다.
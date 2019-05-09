---
title: 양식 숨겨진 구성 요소 (v 1)
seo-title: 양식 숨겨진 구성 요소 (v 1)
description: 핵심 구성 요소 양식 숨김 구성 요소는 숨김 필드를 표시할 수 있습니다.
seo-description: 핵심 구성 요소 양식 숨김 구성 요소는 숨김 필드를 표시할 수 있습니다.
uuid: F 5005346-DEF 5-4 E 1 F -8 F 93-E 4 CFC 67 A 9329
content-type: 참조
products: sg_ Experiencemanager/Corecomponents-new
discoiquuid: D 35 F 4 E 71-EC 7 F -4128-9123-B 997 DBB 5 F 0 CF
index: n
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# 양식 숨겨진 구성 요소 (v 1){#form-hidden-component-v}

핵심 구성 요소 양식 숨김 구성 요소는 숨김 필드를 표시할 수 있습니다.

## 사용량 {#usage}

핵심 구성 요소 양식 숨김 구성 요소는 숨김 필드를 만들어 현재 페이지에 대한 정보를 다시 AEM로 전달하며 [양식 컨테이너 구성 요소와 함께 사용할 수 있도록 만들어졌습니다](form-container.md).

필드 속성은 [구성 대화 상자의 컨텐츠 편집기에서 정의할](#configure-dialog)수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

이 문서에서는 원래 AEM 6.3 이 있는 핵심 구성 요소의 릴리스 1.0.0에 도입된 양식 숨겨진 구성 요소의 v 1를 설명합니다.

다음 표에는 숨겨진 구성 요소의 v 1 호환성이 나와 있습니다.

| AEM 버전 | 양식 숨겨진 구성 요소 v 1 |
|--- |--- |
| 6.3 | 호환 가능 |
| 6.4 | 호환 가능 |

>[!CAUTION]
>
>이 문서에서는 양식 숨김 구성 요소의 v 1에 대해 설명합니다.
>
>양식 숨김 구성 요소의 현재 버전에 대한 자세한 내용은 숨겨진 [구성 요소](form-hidden.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

[다음은 We. Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html)에서 가져온 샘플입니다.

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

>[!NOTE]
>
>핵심 구성 요소에서 JSON 내보내기를 사용하려면 핵심 구성 요소의 릴리스 1.1.0 이 필요합니다. 자세한 내용은 [핵심 구성 요소 v 1](versions.md#release-history-and-compatibility) 의 호환성 정보를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

컨텐츠 작성자는 구성 대화 상자를 사용하여 숨김 필드의 매개 변수를 정의할 수 있습니다.

![](assets/chlimage_1-26.png)

* **이름** - 양식 데이터와 함께 제출된 필드 이름
* **값** - 양식 데이터와 함께 제출된 필드 값입니다.
* **식별자** - 식별자는 페이지에서 고유해야 하며 이 양식 필드에 스크립트를 바인딩하는 데 사용할 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

양식 숨김 구성 요소에 대한 디자인 대화 상자는 없습니다.

## 기술 세부 정보 {#technical-details}

양식 숨김 구성 [요소에 대한 최신 기술 설명서는 Github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/hidden/v1/hidden)에서 찾을 수 있습니다.

Github에서 전체 핵심 구성 요소 프로젝트를 다운로드할 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서를](developing.md)참조하십시오.

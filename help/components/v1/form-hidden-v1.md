---
title: 숨겨진 구성 요소(v1)
description: 코어 구성 요소 양식 숨김 구성 요소로 숨김 필드를 표시할 수 있습니다.
index: n
role: Architect, Developer, Admin, User
exl-id: 8e30dac0-5b4b-4fc7-af99-5791c98c90bf
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 2%

---

# 숨겨진 구성 요소(v1) {#form-hidden-component-v}

코어 구성 요소 양식 숨김 구성 요소로 숨김 필드를 표시할 수 있습니다.

## 사용량 {#usage}

코어 구성 요소 양식 숨김 구성 요소 를 사용하면 숨겨진 필드를 만들어 현재 페이지에 대한 정보를 다시 AEM에 전달할 수 있습니다. 이 필드는 [양식 컨테이너 구성 요소](form-container-v1.md)와 함께 사용하기 위한 것입니다.

필드 속성은 [구성 대화 상자](#configure-dialog)에서 컨텐츠 편집기에서 정의할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

이 문서에서는 원래 AEM 6.3과 함께 코어 구성 요소 릴리스 1.0.0에 소개된 양식 숨김 구성 요소의 v1에 대해 설명합니다.

다음 표에는 Form Hidden 구성 요소의 v1과의 호환성이 나와 있습니다.

| AEM 버전 | 양식 숨김 구성 요소 v1 |
|--- |--- |
| 6.3 | 호환 가능 |
| 6.4 | 호환 가능 |

>[!CAUTION]
>
>이 문서에서는 양식 숨김 구성 요소의 v1에 대해 설명합니다.
>
>양식 숨김 구성 요소의 현재 버전에 대한 자세한 내용은 [양식 숨김 구성 요소](/help/components/forms/form-hidden.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

다음은 [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html)에서 가져온 샘플입니다.

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
>코어 구성 요소에서 JSON 내보내기를 사용하려면 핵심 구성 요소 릴리스 1.1.0이 필요합니다. 자세한 내용은 코어 구성 요소 v1](/help/versions.md#release-history-and-compatibility)에 대한 호환성 정보를 참조하십시오.[

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자에서는 컨텐츠 작성자가 숨김 필드의 매개 변수를 정의할 수 있습니다.

![](/help/assets/chlimage_1-26.png)

* **이름**  - 양식 데이터와 함께 제출되는 필드의 이름입니다
* **값**  - 양식 데이터와 함께 제출되는 필드의 값입니다
* **식별자**  - 식별자는 페이지에서 고유해야 하며 스크립트를 이 양식 필드에 바인딩하는 데 사용할 수 있습니다

## 디자인 대화 상자 {#design-dialog}

양식 숨김 구성 요소에 대한 디자인 대화 상자가 없습니다.

## 기술 세부 정보 {#technical-details}

양식 숨김 구성 요소 [에 대한 최신 기술 설명서는 GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/hidden/v1/hidden)에 있습니다.

전체 코어 구성 요소 프로젝트는 GitHub에서 다운로드할 수 있습니다.

코어 구성 요소 개발에 대한 자세한 내용은 [코어 구성 요소 개발자 설명서](/help/developing/overview.md)에서 확인할 수 있습니다.

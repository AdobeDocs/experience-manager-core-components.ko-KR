---
title: 양식 숨김 구성 요소(v1)
description: 핵심 구성 요소 양식 숨김 구성 요소를 사용하면 숨김 필드를 표시할 수 있습니다.
index: n
translation-type: tm+mt
source-git-commit: fe8a121520000ffd56ae3347469590e89121eaf0

---


# Form Hidden Component (v1) {#form-hidden-component-v}

핵심 구성 요소 양식 숨김 구성 요소를 사용하면 숨김 필드를 표시할 수 있습니다.

## 사용량 {#usage}

핵심 구성 요소 양식 숨김 구성 요소를 사용하면 숨김 필드를 만들어 현재 페이지에 대한 정보를 AEM으로 다시 전달할 수 있으며 [양식 컨테이너 구성 요소와](form-container-v1.md)함께 사용할 수 있습니다.

필드 속성은 [구성 대화 상자의](#configure-dialog)컨텐츠 편집기에서 정의할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

이 문서에서는 AEM 6.3의 핵심 구성 요소 릴리스 1.0.0에서 처음 소개된 양식 숨김 구성 요소의 v1에 대해 설명합니다.

다음 표에는 양식 숨김 구성 요소의 v1 호환성이 나와 있습니다.

| AEM 버전 | 양식 숨김 구성 요소 v1 |
|--- |--- |
| 6.3 | 호환 가능 |
| 6.4 | 호환 가능 |

>[!CAUTION]
>
>이 문서에서는 양식 숨김 구성 요소의 v1에 대해 설명합니다.
>
>양식 숨김 구성 요소의 현재 버전에 대한 자세한 내용은 양식 숨겨진 구성 [요소 문서를](/help/components/forms/form-hidden.md) 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

다음은 We.Retail에서 [가져온 샘플입니다](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

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
>핵심 구성 요소에서 JSON을 내보내려면 핵심 구성 요소 릴리스 1.1.0이 필요합니다. 자세한 내용은 핵심 구성 요소 v1의 [](/help/versions.md#release-history-and-compatibility) 호환성 정보를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자에서는 컨텐츠 작성자가 숨김 필드의 매개 변수를 정의할 수 있습니다.

![](/help/assets/chlimage_1-26.png)

* **이름** - 양식 데이터와 함께 제출하는 필드의 이름입니다.
* **값** - 양식 데이터와 함께 제출하는 필드의 값
* **식별자** - 식별자는 페이지에서 고유해야 하며 이 양식 필드에 스크립트를 바인딩하는 데 사용할 수 있습니다

## 디자인 대화 상자 {#design-dialog}

양식 숨김 구성 요소에 대한 디자인 대화 상자가 없습니다.

## 기술 정보 {#technical-details}

양식 숨김 구성 요소에 대한 최신 기술 문서는 GitHub에서 [찾을 수 있습니다](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/hidden/v1/hidden).

전체 핵심 구성 요소 프로젝트는 GitHub에서 다운로드할 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 핵심 구성 요소 개발자 [설명서를](/help/developing/overview.md)참조하십시오.

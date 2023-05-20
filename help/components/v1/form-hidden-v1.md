---
title: 양식 숨김 구성 요소 (v1)
description: 핵심 구성 요소의 양식 숨기기 구성 요소를 사용하여 숨겨진 필드를 표시할 수 있습니다.
index: n
role: Architect, Developer, Admin, User
exl-id: 8e30dac0-5b4b-4fc7-af99-5791c98c90bf
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 100%

---

# 양식 숨김 구성 요소 (v1) {#form-hidden-component-v}

핵심 구성 요소의 양식 숨기기 구성 요소를 사용하여 숨겨진 필드를 표시할 수 있습니다.

## 사용량 {#usage}

핵심 구성 요소의 양식 숨김 구성 요소를 통해 숨겨진 필드를 만들어 AEM에 다시 현재 페이지에 대한 정보를 전달하고 [양식 컨테이너 구성 요소](form-container-v1.md)와 함께 이 구성 요소를 사용할 수 있습니다.

콘텐츠 작성자는 [구성 대화 상자](#configure-dialog)에서 필드 속성을 정의할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

이 문서에서는 AEM 6.3을 포함하는 핵심 구성 요소 릴리스 1.0.0과 함께 최초 도입된 양식 숨김 구성 요소 v1에 대해 설명합니다.

다음 표에서 양식 숨김 구성 요소 v1의 호환성을 확인할 수 있습니다.

| AEM 버전 | 양식 숨김 구성 요소 v1 |
|--- |--- |
| 6.3 | 호환 가능 |
| 6.4 | 호환 가능 |

>[!CAUTION]
>
>이 문서에서는 양식 숨김 구성 요소 v1에 대해 설명합니다.
>
>현재 버전의 양식 숨김 구성 요소에 대한 자세한 내용은 [양식 숨김 구성 요소](/help/components/forms/form-hidden.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

다음은 [We.Retail](https://helpx.adobe.com/kr/experience-manager/6-4/sites/developing/using/we-retail.html)에서 얻은 샘플입니다.

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
>핵심 구성 요소에서 JSON을 내보내는 데 핵심 구성 요소 릴리스 1.1.0이 필요합니다. 자세한 내용은 [핵심 구성 요소 v1에 대한 호환성 정보](/help/versions.md#release-history-and-compatibility)를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

콘텐츠 작성자는 구성 대화 상자를 통해 숨겨진 필드의 매개 변수를 정의할 수 있습니다.

![](/help/assets/chlimage_1-26.png)

* **이름** - 양식 데이터로 제출된 필드의 이름
* **값** - 양식 데이터로 제출된 필드의 값
* **식별자** - 식별자는 페이지에서 고유해야 하며, 스크립트를 이 양식 필드에 바인딩하는 데 사용할 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

양식 숨김 구성 요소용 디자인 대화 상자가 없습니다.

## 기술 세부 사항 {#technical-details}

양식 숨김 구성 요소에 대한 최신 기술 설명서는 [GitHub에서 확인할 수 있습니다](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/hidden/v1/hidden).

GitHub에서 전체 핵심 구성 요소 프로젝트를 다운로드할 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

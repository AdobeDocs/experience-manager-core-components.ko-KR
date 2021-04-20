---
title: 양식 단추 구성 요소(v1)
description: 핵심 구성 요소 양식 숨김 구성 요소를 사용하면 숨겨진 필드를 양식에 포함할 수 있습니다.
index: n
role: Architect, Developer, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 3%

---


# 양식 단추 구성 요소(v1) {#form-button-component-v}

핵심 구성 요소 양식 단추 구성 요소를 사용하면 단추 필드를 양식에 포함하여 작업을 트리거할 수 있습니다.

## 사용량 {#usage}

핵심 구성 요소 양식 단추 구성 요소를 사용하면 종종 양식 제출을 트리거하는 단추 필드를 만들 수 있으며 [양식 컨테이너 구성 요소](form-container-v1.md)와 함께 사용할 수 있습니다.

단추 속성은 [구성 대화 상자](#configure-dialog)에서 내용 편집기에서 정의할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

이 문서에서는 AEM 6.3의 핵심 구성 요소 릴리스 1.0.0에 처음 소개된 양식 단추 구성 요소의 v1에 대해 설명합니다.

다음 표는 양식 단추 구성 요소의 v1 호환성을 보여줍니다.

| AEM 버전 | 양식 단추 구성 요소 v1 |
|--- |--- |
| 6.3 | 호환 가능 |
| 6.4 | 호환 가능 |

>[!CAUTION]
>
>이 문서에서는 양식 단추 구성 요소의 v1에 대해 설명합니다.
>
>양식 단추 구성 요소의 현재 버전에 대한 자세한 내용은 [양식 단추 구성 요소](/help/components/forms/form-button.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

다음은 [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html)에서 가져온 샘플입니다.

### 스크린샷 {#screenshot}

![](/help/assets/chlimage_1-48.png)

### HTML {#html}

```
<div class="cmp cmp-button aem-GridColumn aem-GridColumn--default--12">
    <div class="cmp cmp-button">
        <button type="BUTTON" class="btn btn-action btn-primary" name="loveToast" value="ILoveToast">
            Click here if you love toast!
        </button>
    </div>
</div>
```

### JSON {#json}

```
"container": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "columnCount": 12,
              "gridClassNames": "aem-Grid aem-Grid--12 aem-Grid--default--12",
              ":items": {
                "button": {
                  "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
                  ":type": "weretail/components/form/button",
                  "name": "loveToast",
                  "jcr:title": "Click here if you love toast!",
                  "type": "submit",
                  "value": "ILoveToast"
                }
              },
              ":itemsOrder": [
                "button"
              ],
              ":type": "weretail/components/form/container"
            }
```

>[!NOTE]
>
>핵심 구성 요소에서 JSON 내보내기를 사용하려면 핵심 구성 요소의 릴리스 1.1.0이 필요합니다. 자세한 내용은 핵심 구성 요소 v1](/help/versions.md)에 대한 호환성 정보를 참조하십시오.[

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자를 사용하면 컨텐츠 작성자가 단추의 매개 변수를 정의할 수 있습니다.

![](/help/assets/chlimage_1-49.png)

* **유형**
   * **단추**
   * **전송**

* **제목**  - 단추에 표시되는 텍스트입니다.
   * 아무 것도 제공하지 않으면 기본적으로 단추 유형이 됩니다

* **이름**  - 양식 데이터와 함께 제출하는 단추의 이름입니다.
* **값**  - 양식 데이터와 함께 제출하는 단추의 값

## 디자인 대화 상자 {#design-dialog}

양식 단추 구성 요소에 대한 디자인 대화 상자가 없습니다.

## 기술 세부 정보 {#technical-details}

양식 단추 구성 요소 [에 대한 최신 기술 문서는 GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/button/v1/button)에서 찾을 수 있습니다.

전체 핵심 구성 요소 프로젝트를 GitHub에서 다운로드할 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)에서 확인할 수 있습니다.

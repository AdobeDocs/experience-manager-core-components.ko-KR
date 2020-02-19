---
title: 양식 단추 구성 요소(v1)
description: 핵심 구성 요소 양식 숨김 구성 요소를 사용하면 양식에 숨김 필드를 포함할 수 있습니다.
index: n
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Form Button Component (v1) {#form-button-component-v}

핵심 구성 요소 양식 단추 구성 요소를 사용하면 양식에 단추 필드를 포함하여 작업을 트리거할 수 있습니다.

## 사용량 {#usage}

핵심 구성 요소 양식 단추 구성 요소를 사용하면 종종 양식 제출을 트리거할 수 있으며 [양식 컨테이너 구성 요소와](form-container-v1.md)함께 사용할 수 있습니다.

단추 속성은 [구성 대화 상자의](#configure-dialog)컨텐츠 편집기에서 정의할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

이 문서에서는 AEM 6.3의 핵심 구성 요소 릴리스 1.0.0에서 처음 소개된 양식 단추 구성 요소의 v1에 대해 설명합니다.

다음 표에는 양식 단추 구성 요소의 v1 호환성이 나와 있습니다.

| AEM 버전 | 양식 단추 구성 요소 v1 |
|--- |--- |
| 6.3 | 호환 가능 |
| 6.4 | 호환 가능 |

>[!CAUTION]
>
>이 문서에서는 양식 단추 구성 요소의 v1에 대해 설명합니다.
>
>양식 단추 구성 요소의 현재 버전에 대한 자세한 내용은 양식 단추 구성 [요소 문서를](/help/components/forms/form-button.md) 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

다음은 We.Retail에서 [가져온 샘플입니다](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

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
>핵심 구성 요소에서 JSON을 내보내려면 핵심 구성 요소 릴리스 1.1.0이 필요합니다. 자세한 내용은 핵심 구성 요소 v1의 [](/help/versions.md) 호환성 정보를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자에서는 컨텐츠 작성자가 단추의 매개 변수를 정의할 수 있습니다.

![](/help/assets/chlimage_1-49.png)

* **유형**
   * **단추**
   * **전송**

* **제목** - 단추에 표시된 텍스트
   * 제공된 것이 없으면 기본적으로 단추 유형이 됩니다

* **이름** - 양식 데이터와 함께 제출하는 단추의 이름
* **값** - 양식 데이터와 함께 제출하는 단추의 값

## 디자인 대화 상자 {#design-dialog}

양식 단추 구성 요소에 대한 디자인 대화 상자가 없습니다.

## 기술 정보 {#technical-details}

양식 단추 구성 요소에 대한 최신 기술 문서는 GitHub에서 [찾을 수 있습니다](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/button/v1/button).

전체 핵심 구성 요소 프로젝트는 GitHub에서 다운로드할 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 핵심 구성 요소 개발자 [설명서를](/help/developing/overview.md)참조하십시오.

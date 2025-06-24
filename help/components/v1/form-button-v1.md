---
title: 양식 버튼 구성 요소 (v1)
description: 핵심 구성 요소의 양식 숨기기 구성 요소를 사용하여 양식에 숨겨진 필드를 포함할 수 있습니다.
index: n
role: Architect, Developer, Admin, User
exl-id: 2c06a942-7ac5-4847-9d11-7bbcd0ea51bd
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 100%

---


# 양식 버튼 구성 요소 (v1) {#form-button-component-v}

핵심 구성 요소의 양식 버튼 요소 다운로드를 사용하여 작업을 양식에 트리거할 버튼 필드를 포함할 수 있습니다.

## 사용량 {#usage}

핵심 구성 요소의 양식 버튼 구성 요소를 사용하여 버튼 필드를 생성하고, 종종 양식 제출을 트리거하고 [양식 컨테이너 구성 요소](form-container-v1.md)와 함께 이 구성 요소를 사용할 수 있습니다.

콘텐츠 편집기는 [구성 대화 상자](#configure-dialog)에서 버튼의 속성을 정의할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

이 문서에서는 AEM 6.3을 포함하는 핵심 구성 요소 릴리스 1.0.0과 함께 최초 도입된 양식 버튼 구성 요소 v1에 대해 설명합니다.

다음 테이블에서 양식 버튼 구성 요소 v1의 호환성을 확인할 수 있습니다.

| AEM 버전 | 양식 버튼 구성 요소 v1 |
|--- |--- |
| 6.3 | 호환 가능 |
| 6.4 | 호환 가능 |

>[!CAUTION]
>
>이 문서에서는 양식 버튼 구성 요소 v1에 대해 설명합니다.
>
>현재 버전의 양식 버튼 구성 요소에 대한 자세한 내용은 [양식 버튼 구성 요소](/help/components/forms/form-button.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

다음은 [We.Retail](https://helpx.adobe.com/kr/experience-manager/6-4/sites/developing/using/we-retail.html)에서 얻은 샘플입니다.

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
>핵심 구성 요소에서 JSON을 내보내는 데 핵심 구성 요소 릴리스 1.1.0이 필요합니다. 자세한 내용은 [핵심 구성 요소 v1에 대한 호환성 정보](/help/versions.md)를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

콘텐츠 작성자는 구성 대화 상자를 통해 버튼의 매개 변수를 정의할 수 있습니다.

![](/help/assets/chlimage_1-49.png)

* **유형**
   * **버튼**
   * **제출**

* **제목** - 버튼에 표시된 텍스트
   * 제공되지 않은 경우 기본값은 버튼 유형으로 설정됩니다.

* **이름** - 양식 데이터로 제출된 버튼의 이름
* **값** - 양식 데이터로 제출된 버튼의 값

## 디자인 대화 상자 {#design-dialog}

양식 버튼 구성 요소용 디자인 대화 상자는 없습니다.

## 기술 세부 사항 {#technical-details}

양식 버튼 구성 요소에 대한 최신 기술 설명서는 [GitHub에서 확인할 수 있습니다](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/button/v1/button).

GitHub에서 전체 핵심 구성 요소 프로젝트를 다운로드할 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

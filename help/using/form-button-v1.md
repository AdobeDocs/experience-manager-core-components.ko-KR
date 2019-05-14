---
title: 양식 단추 구성 요소 (v 1)
seo-title: 양식 단추 구성 요소 (v 1)
description: 'null'
seo-description: 핵심 구성 요소 양식 숨김 구성 요소를 사용하면 양식에 숨김 필드를 포함할 수 있습니다.
uuid: 0525 E 70 F -294 F -4 D 35-BF 96-FC 0 E 4 EC 225 E 9
content-type: 참조
products: sg_ Experiencemanager/Corecomponents-new
discoiquuid: EA 06 ACC 0-38 E 2-4252-AC 29-07332835 B 7 C 4
disttype: dist5
gnavtheme: 밝음
groupsectionnavitems: 아니오
hidemerchandisingbar: 상속
hidepromocomponent: 상속
modalsize: 426x240
index: n
translation-type: tm+mt
source-git-commit: 4e74f10e2a4119484a597178dc4577b399833dbf

---


# 양식 단추 구성 요소 (v 1){#form-button-component-v}

핵심 구성 요소 양식 단추 구성 요소를 사용하면 양식에 단추 필드를 포함시켜 작업을 트리거할 수 있습니다.

## 사용량 {#usage}

핵심 구성 요소 양식 단추 구성 요소는 단추 필드를 만들어 양식 제출 작업을 트리거하는 경우가 있으며 [양식 컨테이너 구성 요소와 함께 사용하기 위한 것입니다](form-container.md).

단추 속성은 [구성 대화 상자의 컨텐츠 편집기에서 정의할](form-button-v1.md#main-pars_title)수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

이 문서에서는 원래 AEM 6.3 이 있는 핵심 구성 요소의 릴리스 1.0.0에 도입된 양식 단추 구성 요소의 v 1에 대해 설명합니다.

다음 표에는 양식 단추 구성 요소의 v 1 호환성이 나와 있습니다.

| AEM 버전 | 양식 단추 구성 요소 v 1 |
|--- |--- |
| 6.3 | 호환 가능 |
| 6.4 | 호환 가능 |

>[!CAUTION]
>
>이 문서에서는 양식 단추 구성 요소의 v 1에 대해 설명합니다.
>
>양식 단추 구성 요소의 현재 버전에 대한 자세한 내용은 [양식 단추 구성 요소](form-button.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

[다음은 We. Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html)에서 가져온 샘플입니다.

### 스크린샷 {#screenshot}

![](assets/chlimage_1-48.png)

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
>핵심 구성 요소에서 JSON 내보내기를 사용하려면 핵심 구성 요소의 릴리스 1.1.0 이 필요합니다. 자세한 내용은 [핵심 구성 요소 v 1](versions.md#main-pars_title_236368006) 의 호환성 정보를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

컨텐츠 작성자는 구성 대화 상자를 사용하여 버튼의 매개 변수를 정의할 수 있습니다.

![](assets/chlimage_1-49.png)

* **유형**
   * **단추**
   * **전송**

* **제목** - 단추에 표시되는 텍스트입니다.
   * if none provided it default to the button type

* **이름** - 양식 데이터와 함께 제출된 단추 이름
* **값** - 양식 데이터와 함께 제출된 단추 값입니다.

## 디자인 대화 상자 {#design-dialog}

양식 단추 구성 요소에는 디자인 대화 상자가 없습니다.

## 기술 세부 정보 {#technical-details}

양식 단추 구성 요소에 [대한 최신 기술 설명서는 Github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/button/v1/button)에서 찾을 수 있습니다.

Github에서 전체 핵심 구성 요소 프로젝트를 다운로드할 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서를](developing.md)참조하십시오.

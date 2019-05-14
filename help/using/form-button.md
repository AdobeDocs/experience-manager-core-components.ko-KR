---
title: 양식 단추 구성 요소
seo-title: 양식 단추 구성 요소
description: 'null'
seo-description: 핵심 구성 요소 양식 숨김 구성 요소를 사용하면 양식에 숨김 필드를 포함할 수 있습니다.
uuid: 22 C 53 CD 0-D 0 BC -4 E 5 D -89 F 3-5 AC 4 F 61 A 9100
contentOwner: 사용자
content-type: 참조
topic-tags: 저작
products: sg_ Experiencemanager/Corecomponents-new
discoiquuid: A 6 E 2974 A -243 F -40 AB -903 C-C 7 D 3 E 8615 BCC
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
source-git-commit: 1243d6cc1b0b015ee2f37ae89d0e2e42d366cc02

---


# 양식 단추 구성 요소{#form-button-component}

핵심 구성 요소 양식 단추 구성 요소를 사용하면 단추를 포함할 수 있습니다.

## 사용량 {#usage}

핵심 구성 요소 양식 단추 구성 요소는 단추 필드를 만들어 양식 제출 작업을 트리거하는 경우가 있으며 [양식 컨테이너 구성 요소와 함께 사용하기 위한 것입니다](form-container.md).

단추 속성은 [구성 대화 상자의 컨텐츠 편집기에서 정의할](form-button.md)수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

양식 단추 구성 요소의 현재 버전은 2018 년 1 월에 핵심 구성 요소의 릴리스 2.0.0에 도입된 v 2 이며, 이 문서에서는 설명합니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서에 대한 링크를 제공합니다.

| 구성 요소 버전 | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | 호환 가능 | 호환 가능 | 호환 가능 |
| [v1](form-button-v1.md) | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 문서 [코어 구성 요소 버전을 참조하십시오](versions.md).

## 샘플 구성 요소 출력 {#sample-component-output}

[다음은 We. Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html)에서 가져온 샘플입니다.

### 스크린샷 {#screenshot}

![](assets/screen_shot_2018-01-12at120021.png)

### HTML {#html}

```
<div class="container responsivegrid aem-GridColumn aem-GridColumn--default--12">
<form method="POST" action="/content/we-retail/us/en/experience.html" id="new_form" name="new_form" enctype="multipart/form-data" class="cmp-form aem-Grid aem-Grid--12 aem-Grid--default--12">
    <input type="hidden" name=":formstart" value="/content/we-retail/us/en/experience/jcr:content/root/responsivegrid/container">
    
    <div class="button aem-GridColumn aem-GridColumn--default--12">
<button type="BUTTON" class="cmp-form-button" name="loveToast" value="ILoveToast">Click here if you love toast!</button>
</div>

</form>
</div>
```

### JSON {#json}

```
"button":{  
                           "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                           ":type":"core/wcm/sandbox/components/form/button/v2/button",
                           "name":"loveToast",
                           "jcr:title":"Click here if you love toast!",
                           "type":"button",
                           "value":"ILoveToast"
                        }
```

### 기술 세부 정보 {#technical-details}

양식 단추 구성 요소에 [대한 최신 기술 설명서는 Github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/form/button/v2/button)에서 찾을 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서를](developing.md)참조하십시오.

## 구성 대화 상자 {#configure-dialog}

컨텐츠 작성자는 구성 대화 상자를 사용하여 버튼의 매개 변수를 정의할 수 있습니다.

### 속성 탭 {#properties-tab}

![](assets/screen_shot_2018-01-12at120433.png)

* **유형**

   * **단추**
   * **전송**

* **제목** - 단추에 표시되는 텍스트입니다.

   * if none provided it default to the button type

* **이름** - 양식 데이터와 함께 제출된 단추 이름
* **값** - 양식 데이터와 함께 제출된 단추 값입니다.

## 디자인 대화 상자 {#design-dialog}

### 스타일 탭 {#styles-tab}

양식 단추 구성 요소는 AEM [스타일 시스템을 지원합니다](authoring.md#component-styling).
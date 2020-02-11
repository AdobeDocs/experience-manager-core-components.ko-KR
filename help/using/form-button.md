---
title: 양식 단추 구성 요소
description: 핵심 구성 요소 양식 숨김 구성 요소를 사용하면 양식에 숨김 필드를 포함할 수 있습니다.
translation-type: tm+mt
source-git-commit: 60df01ca9efe59b67bad57610d04496a2cdded9e

---


# 양식 단추 구성 요소{#form-button-component}

핵심 구성 요소 양식 단추 구성 요소를 사용하면 페이지에 동작을 트리거하는 단추를 포함할 수 있습니다.

## 사용량 {#usage}

핵심 구성 요소 양식 단추 구성 요소를 사용하면 종종 양식 제출을 트리거할 수 있으며 양식 컨테이너 구성 요소와 [함께 사용할 수](form-container.md)있습니다.

단추 속성은 [구성 대화 상자의](form-button.md)컨텐츠 편집기에서 정의할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

양식 단추 구성 요소의 현재 버전은 v2이며, 이 버전은 2018년 1월 핵심 구성 요소 릴리스 2.0.0과 함께 도입되었으며 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소 버전이 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.3 | AEM 6.4 | AEM 6.5 | 클라우드 서비스로 AEM 사용 |
|--- |--- |--- |--- |---|
| v2 | 호환 가능 | 호환 가능 | 호환 가능 | 호환 가능 |
| [v1](form-button-v1.md) | 호환 가능 | 호환 가능 | 호환 가능 | - |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 핵심 구성 요소 [버전을 참조하십시오](versions.md).

## 샘플 구성 요소 출력 {#sample-component-output}

다음은 We.Retail에서 [가져온 샘플입니다](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

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

### 기술 정보 {#technical-details}

양식 단추 구성 요소에 대한 최신 기술 문서는 GitHub에서 [찾을 수 있습니다](https://adobe.com/go/aem_cmp_tech_form_button_v2).

핵심 구성 요소 개발에 대한 자세한 내용은 핵심 구성 요소 개발자 [설명서를](developing.md)참조하십시오.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자에서는 컨텐츠 작성자가 단추의 매개 변수를 정의할 수 있습니다.

### 속성 탭 {#properties-tab}

![](assets/screen_shot_2018-01-12at120433.png)

* **유형**

   * **단추**
   * **전송**

* **제목** - 단추에 표시된 텍스트

   * 제공된 것이 없으면 기본적으로 단추 유형이 됩니다

* **이름** - 양식 데이터와 함께 제출하는 단추의 이름
* **값** - 양식 데이터와 함께 제출하는 단추의 값

## 디자인 대화 상자 {#design-dialog}

### 스타일 탭 {#styles-tab}

양식 단추 구성 요소는 AEM 스타일 시스템을 [지원합니다](authoring.md#component-styling).

---
title: 컨텐츠 조각 목록 구성 요소
seo-title: 컨텐츠 조각 목록 구성 요소
description: 'null'
seo-description: 핵심 구성 요소 조각 목록 구성 요소는 컨텐츠 조각 목록을 표시할 수 있습니다.
contentOwner: Bohnert
content-type: 참조
topic-tags: 저작
products: sg_ Experiencemanager/Corecomponents-new
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# 컨텐츠 조각 목록 구성 요소{#content-fragment-list-component}

핵심 구성 요소 조각 목록 구성 요소는 [컨텐츠 조각 목록을 표시할 수 있습니다](https://helpx.adobe.com/experience-manager/6-5/assets/using/content-fragments.html).

## 사용량 {#usage}

핵심 구성 요소 조각 목록 구성 요소를 사용하면 컨텐츠 조각 모델을 기반으로 페이지에 [컨텐츠 조각](https://helpx.adobe.com/experience-manager/6-5/assets/using/content-fragments.html) 목록을 포함시킬 수 있습니다. 이 기능은 다른 애플리케이션에서 쉽게 사용할 수 있는 [헤드리스 컨텐츠를](https://helpx.adobe.com/experience-manager/6-5/sites/developing/user-guide.html?topic=/experience-manager/6-5/sites/developing/morehelp/headless.ug.js) 만드는 데 특히 유용합니다.

* 목록 및 해당 속성은 [구성 대화 상자에서 선택할](#configure-dialog)수 있습니다.
* 스타일은 [디자인 대화 상자의 구성 요소에 적용할](#design-dialog)수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

컨텐츠 조각 구성 요소의 현재 버전은 2019 년 5 월에 핵심 구성 요소의 릴리스 2.4.0에 도입된 v 1 이며, 이 문서에서는 설명합니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서에 대한 링크를 제공합니다.

| 구성 요소 버전 | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |---|
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 문서 [코어 구성 요소 버전을 참조하십시오](versions.md).

## 샘플 구성 요소 출력 {#sample-component-output}

컨텐츠 조각 목록 구성 요소를 경험하고 HTML 및 JSON 출력뿐만 아니라 구성 옵션의 예를 보려면 [구성 요소 라이브러리를 참조하십시오](http://opensource.adobe.com/aem-core-wcm-components/library/content-fragment-list.html).

## 기술 세부 정보 {#technical-details}

컨텐츠 조각 목록 구성 요소에 [대한 최신 기술 설명서는 Github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/contentfragmentlist/v1/contentfragmentlist)에서 찾을 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서를](developing.md)참조하십시오.

## 구성 대화 상자 {#configure-dialog}

컨텐츠 작성자는 구성 대화 상자를 사용하여 포함할 컨텐츠 조각과 포함할 조각의 요소를 정의할 수 있습니다.

### 속성 탭

**속성** 탭은 목록에 포함된 컨텐츠 조각을 정의합니다. 이것은 주로 선택된 컨텐츠 조각 모델을 기반으로 하지만 사용할 수 있는 다른 필터 옵션이 있습니다.

![](assets/screen-shot-2019-05-08-10.47.19.png)

* **모델** - 목록이 기반으로 하는 컨텐츠 조각 모델의 경로입니다.
   * 기본적으로 **모델 경로로** 정의된 모델의 모든 컨텐츠 조각이 목록에 포함됩니다.
* **상위 경로** - 목록을 작성해야 하는 상위 경로입니다.
   * 선택한 **모델 경로를** 기반으로 하는 컨텐츠 조각은 지정된 **상위 경로의 컨텐츠**조각으로 필터링됩니다.
   * 필드의 오른쪽에 있는 선택 대화 **상자 열기** 단추를 클릭하거나 탭하여 경로를 지정합니다.
* **태그** - 지정된 태그가 있는 컨텐츠 조각만 목록에 포함됩니다.
   * 필드의 오른쪽에 있는 선택 대화 **상자 열기** 단추를 클릭하거나 탭하여 태그를 지정합니다.
   * 선택한 태그 옆에 있는 X를 클릭하거나 탭하여 제거합니다.


### 요소 탭

기본적으로 컨텐츠 조각 모델의 모든 요소는 목록에 포함됩니다. 요소를 사용하면 **포함할** 특정 요소만 지정할 수 있습니다.

![](assets/screen-shot-2019-05-08-10.47.34.png)

* **요소** - 지정된 목록에 있는 컨텐츠 조각의 요소만 표시됩니다.
   * **추가** 단추를 클릭하거나 탭하여 새 요소를 추가합니다.
   * **삭제** 단추를 클릭하거나 탭하여 선택한 요소를 제거합니다.
   * **주문** 핸들을 드래그하여 요소의 순서를 재정렬합니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 사용하여 컨텐츠 조각 목록 구성 요소에 적용된 스타일을 정의할 수 있습니다.
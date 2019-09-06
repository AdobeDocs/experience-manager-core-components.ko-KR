---
title: 단추 구성 요소
seo-title: 단추 구성 요소
description: 'null'
seo-description: 핵심 구성 요소 단추 구성 요소를 사용하면 단추를 만들고 표시할 수 있습니다.
uuid: EC 807 DE 9-F 76 C -4850-9 ECE-C 3 E 439 A 1 D 626
contentOwner: 사용자
content-type: 참조
topic-tags: 저작
products: sg_ Experiencemanager/Corecomponents-new
discoiquuid: F 093 F 58 E -9755-4 A 4 F -803 A-AB 93 A 50 E 6870
translation-type: tm+mt
source-git-commit: d37cde072dea612ccb55ad31b4aaf42f17839cb4

---


# 단추 구성 요소{#button-component}

핵심 구성 요소 단추 구성 요소를 사용하면 페이지에 단추 항목을 구성하고 표시할 수 있습니다.

## 사용량 {#usage}

핵심 구성 요소 단추 구성 요소를 사용하면 페이지에 단추를 포함할 수 있습니다.

* 구성 대화 상자에서 단추의 속성을 선택할 [](#configure-dialog)수 있습니다.
* 단추 구성 요소에 대한 스타일은 [디자인 대화 상자에서 정의할](#design-dialog)수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

버튼 구성 요소의 현재 버전은 2019 년 6 월에 핵심 구성 요소의 릴리스 2.5.0에서 처음 소개된 v 1 이며, 이 문서에서는 설명합니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서에 대한 링크를 제공합니다.

| 구성 요소 버전 | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |---|
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 문서 [코어 구성 요소 버전을 참조하십시오](versions.md).

## 샘플 구성 요소 출력 {#sample-component-output}

단추 구성 요소를 경험하고 HTML 및 JSON 출력을 비롯하여 구성 옵션의 예를 보려면 [구성 요소 라이브러리를 참조하십시오](http://opensource.adobe.com/aem-core-wcm-components/library/button.html).

## 기술 세부 정보 {#technical-details}

단추 구성 요소에 [대한 최신 기술 설명서는 Github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/button/v1/button)에서 찾을 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서를](developing.md)참조하십시오.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자에서 컨텐츠 작성자가 단추를 정의할 수 있으며 방문자가 페이지에 대해 어떻게 행동하고 나타날지 지정할 수 있습니다.

### 속성 탭 {#properties-tab}

![](assets/screen-shot-2019-08-29-12.19.32.png)

* **텍스트** - 단추에 표시할 텍스트입니다.
* **링크** - AEM 내의 컨텐츠 페이지, 외부 리소스 또는 앵커에 연결
   * **선택 대화 상자를** 사용하여 AEM 내의 경로를 선택합니다.
* **아이콘** - 단추에 아이콘을 표시하기 위한 식별자

### 액세스 가능성 탭 {#accessibility-tab}

![](assets/screen-shot-2019-08-29-12.19.43.png)

**액세서빌러티** 탭에서 구성 요소의 [ARIA 액세서빌러티](https://www.w3.org/WAI/standards-guidelines/aria/) 레이블에 대해 값을 설정할 수 있습니다.

* **label** - 구성 요소에 대한 aria 레이블 속성의 값

## 디자인 대화 상자 {#design-dialog}

### 스타일 탭 {#styles-tab}

이미지 구성 요소는 AEM [스타일 시스템을 지원합니다](authoring.md#component-styling).

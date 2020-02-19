---
title: 양식 컨테이너 구성 요소(v1)
description: 핵심 구성 요소 양식 컨테이너 구성 요소를 사용하면 간단한 제출 양식을 만들 수 있습니다.
index: n
translation-type: tm+mt
source-git-commit: 68472ab548fb6ebb443a06c12e7b37797a0c1302

---


# Form Container Component (v1) {#form-container-component-v1}

핵심 구성 요소 양식 컨테이너 구성 요소를 사용하면 간단한 제출 양식을 만들 수 있습니다.

## 사용량 {#usage}

양식 컨테이너 구성 요소는 간단한 WCM 양식을 지원하고 중첩된 구조를 사용하여 추가 양식 구성 요소를 허용함으로써 간단한 정보 제출 양식 및 기능을 작성할 수 있도록 했습니다.

컨텐츠 편집자는 [설정 대화](#settings-dialog) 상자를 사용하여 어떤 유형의 작업 양식 제출 트리거, 제출된 컨텐츠를 저장할 위치, 그리고 워크플로우를 실행해야 하는지를 정의할 수 있습니다. 템플릿 작성자는 [디자인 대화 상자를](#design-dialog) 사용하여 템플릿 편집기의 [](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/templates.html)표준 레이아웃 컨테이너에 대한 디자인 대화 상자와 유사한 구성 요소 및 해당 매핑을 정의할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

이 문서에서는 AEM 6.3의 핵심 구성 요소 릴리스 1.0.0에서 처음 소개된 양식 컨테이너 구성 요소의 v1에 대해 설명합니다.

다음 표에는 양식 컨테이너 구성 요소의 v1 호환성이 나와 있습니다.

| AEM 버전 | 양식 컨테이너 구성 요소 v1 |
|--- |--- |
| 6.3 | 호환 가능 |
| 6.4 | 호환 가능 |

>[!CAUTION]
>
>이 문서에서는 양식 컨테이너 구성 요소의 v1에 대해 설명합니다.
>
>양식 컨테이너 구성 요소의 현재 버전에 대한 자세한 내용은 양식 컨테이너 구성 [요소 문서를](/help/components/forms/form-container.md) 참조하십시오.

## 설정 대화 상자 {#settings-dialog}

설정 대화 상자에서는 컨텐츠 작성자가 구성 요소를 제출할 때 수행되는 작업을 정의할 수 있습니다.

![](/help/assets/chlimage_1.png)

선택한 작업 **유형에**&#x200B;따라 컨테이너 내에서 사용할 수 있는 옵션이 변경됩니다. 사용 가능한 작업 유형은 다음과 같습니다.

* [메일](#mail)
* [컨텐츠 저장](#store-content)
* [주문 제출](#submit-order)
* [주문 업데이트](#update-order)

유형에 관계없이 각 동작에 적용되는 [일반 설정이](#general-settings) 있습니다.

### 메일 {#mail}

양식이 제출되면 메일 작업 유형은 지정된 받는 사람에게 이메일을 보냅니다.

![](/help/assets/chlimage_1-1.png)

* **제목** - 양식 제출 시 전송되는 이메일의 제목
* **보낸 사람** - 양식 제출 시 보낼 이메일의 보낸 사람 이메일 주소입니다.
* **받는 사람** - 양식 제출 시 이메일을 받을 수신자의 주소
   * 추가 단추를 탭하거나 클릭하여 **추가** 주소 추가
   * 삭제 **단추를 탭하거나 클릭하여** 이메일 주소를 제거합니다.
* **CC** - 양식 제출 시 발송된 카본 사본을 수신자의 주소
   * 추가 단추를 탭하거나 클릭하여 **추가** 주소 추가
   * 삭제 **단추를 탭하거나 클릭하여** 이메일 주소를 제거합니다.

### 컨텐츠 저장 {#store-content}

양식이 제출되면 양식의 컨텐츠가 지정된 저장소 위치에 저장됩니다.

![](/help/assets/chlimage_1-2.png)

* **컨텐츠 경로** - 제출된 컨텐츠가 저장되는 컨텐츠 저장소 경로
* **데이터** 보기 - 저장된 제출 데이터를 JSON으로 보려면 탭하거나 클릭합니다.
* **워크플로우** 시작 - 양식 제출 시 저장된 컨텐츠를 페이로드로 사용하여 워크플로우를 시작하도록 구성

### 주문 제출 {#submit-order}

양식이 제출되면 주문이 제출됩니다.

![](/help/assets/chlimage_1-3.png)

### 주문 업데이트 {#update-order}

양식이 제출되면 주문이 업데이트됩니다.

![](/help/assets/chlimage_1-4.png)

### 일반 설정 {#general-settings}

선택한 작업 유형에 관계없이 감사 페이지를 항상 정의할 수 있습니다.

![](/help/assets/chlimage_1-5.png)

양식 제출 완료 후 사용자가 지정된 페이지로 리디렉션됩니다.

* 선택 대화 상자를 사용하여 AEM 내의 리소스를 선택합니다.
* 감사 인사 페이지가 AEM에 없는 경우 절대 URL을 지정합니다. 절대 URL이 아닌 URL은 AEM을 기준으로 해석됩니다.
* 양식을 제출한 후 다시 표시하려면 비워 둡니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 사용하여 템플릿 편집기에서 [](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/templates.html#main-pars_title_1754153843)표준 레이아웃 컨테이너에 대한 디자인 대화 상자와 유사한 컨테이너에 대해 허용된 구성 요소 및 해당 매핑을 정의할 수 있습니다.

## 기술 정보 {#technical-details}

양식 컨테이너 구성 요소에 대한 최신 기술 문서는 GitHub에서 [찾을 수 있습니다](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/container/v1/container).

전체 핵심 구성 요소 프로젝트는 GitHub에서 다운로드할 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 핵심 구성 요소 개발자 [설명서를](/help/developing/overview.md)참조하십시오.

---
title: 양식 컨테이너 구성 요소
seo-title: 양식 컨테이너 구성 요소
description: 'null'
seo-description: 핵심 구성 요소 양식 컨테이너 구성 요소를 사용하면 간단한 제출 양식을 작성할 수 있습니다.
uuid: 9 d 556 daf -3 fe 7-4 b 2 a-b 5 ae -6926 acb 267 a 9
contentOwner: 사용자
content-type: 참조
topic-tags: 저작
products: sg_ Experiencemanager/Corecomponents-new
discoiquuid: 3 D 33 FE 60-A 0 AC -4 FF 2-A 865-D 600 B 5448 AEB
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
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# 양식 컨테이너 구성 요소{#form-container-component}

핵심 구성 요소 양식 컨테이너 구성 요소를 사용하면 간단한 제출 양식을 작성할 수 있습니다.

## 사용량 {#usage}

양식 컨테이너 구성 요소를 사용하면 간단한 WCM 양식을 지원하고 중첩된 구조를 사용하여 추가 양식 구성 요소를 제공함으로써 간단한 정보 제출 양식 및 기능을 구축할 수 있습니다.

[컨텐츠 편집기로 구성 대화 상자를](#configure-dialog) 사용하면 양식 제출 시 트리거되는 작업, 제출된 컨텐츠를 저장할 위치, 워크플로우가 트리거되어야 하는지 여부를 정의할 수 있습니다. 템플릿 작성자는 [디자인 대화 상자를](#design-dialog) 사용하여 템플릿 편집기의 [표준 레이아웃 컨테이너에 대한 디자인 대화 상자와 유사한 허용된 구성 요소 및 해당 매핑을 정의할](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)수 있습니다.

>[!NOTE]
>
>핵심 구성 요소 양식 컨테이너 구성 요소는 핵심 구성 요소 양식 구성 요소 (단추, 텍스트, 숨김 등) 의 사용을 지원합니다. 핵심 구성 요소 양식 컨테이너 (및 그 반대) 내에서 [기본 구성 요소](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-foundation.html) 양식 구성 요소를 사용하는 것은 지원되지 않습니다.

## 버전 및 호환성 {#version-and-compatibility}

양식 컨테이너 구성 요소의 현재 버전은 2018 년 1 월에 핵심 구성 요소의 릴리스 2.0.0에 도입된 v 2 이며, 이 문서에서는 설명합니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서에 대한 링크를 제공합니다.

| 구성 요소 버전 | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | 호환 가능 | 호환 가능 | 호환 가능 |
| [v1](form-container-v1.md) | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 문서 [코어 구성 요소 버전을 참조하십시오](versions.md).

## 기술 세부 정보 {#technical-details}

양식 컨테이너 구성 요소에 [대한 최신 기술 설명서는 Github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/form/container/v2/container)에서 찾을 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서를](developing.md)참조하십시오.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자에서는 컨텐츠 작성자가 구성 요소를 제출할 때 수행되는 작업을 정의할 수 있습니다.

![](assets/screen_shot_2018-01-12at122046.png)

선택한 **작업 유형에**따라 컨테이너 내의 사용 가능한 옵션이 변경됩니다. 사용 가능한 작업 유형은 다음과 같습니다.

* [메일](#mail)
* [컨텐츠 저장](#store-content)
* [주문 제출](#submit-order)
* [주문 업데이트](#update-order)

유형에 관계없이 각 작업에 적용되는 [일반 설정이](#general-settings) 있습니다.

### 메일 {#mail}

양식을 제출하면 메일 작업 유형이 지정된 수신자에게 이메일을 전송합니다.

![](assets/screen_shot_2018-01-12at122554.png)

* **양식**제출 시 전송할 이메일 제목 제목
* **양식**제출 시 전송할 이메일의 이메일 주소 From
* **양식**제출 시 이메일을 받을 수신자의 주소

   * 추가 주소를 **추가하려면** 추가 단추를 탭하거나 클릭합니다.
   * **삭제** 단추를 탭하거나 클릭하여 이메일 주소를 제거합니다.
* **참조양식**
제출 시 전송된 이메일을 받을 받는 사람의 주소
   * 추가 주소를 **추가하려면** 추가 단추를 탭하거나 클릭합니다.
   * **삭제** 단추를 탭하거나 클릭하여 이메일 주소를 제거합니다.

### 컨텐츠 저장 {#store-content}

양식을 제출하면 양식의 컨텐츠가 지정된 저장소 위치에 저장됩니다.

![](assets/screen_shot_2018-01-12at122538.png)

* **제출된 컨텐츠가 저장되는 컨텐츠 경로**
컨텐츠 저장소 경로
* **데이터**
탭하거나 클릭하여 제출된 제출된 데이터를 JSON로 보기
* **양식 제출 시 저장된 컨텐츠를 페이로드로 사용하여 워크플로우를 시작하려면 워크플로우**
구성을 시작합니다.

### 주문 제출 {#submit-order}

양식을 제출하면 주문이 제출됩니다.

![](assets/chlimage_1-3.png)

### 주문 업데이트 {#update-order}

양식을 제출하면 주문이 업데이트됩니다.

![](assets/chlimage_1-4.png)

### 일반 설정 {#general-settings}

선택한 작업 유형에 관계없이 감사 인사 페이지를 항상 정의할 수 있습니다.

![](assets/chlimage_1-5.png)

양식 제출 완료 후 사용자가 지정된 페이지로 리디렉션됩니다.

* 선택 대화 상자를 사용하여 AEM 내의 리소스를 선택합니다.
* 감사 페이지가 AEM에 없는 경우 절대 URL를 지정합니다. 절대 URL 이 아닌 URL는 AEM를 기준으로 해석됩니다.
* 제출 후 양식을 다시 표시하려면 비워 두십시오.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 사용하여 템플릿 편집기의 [표준 레이아웃 컨테이너에 대한 디자인 대화 상자와 유사한 컨테이너에 대한 허용된 구성 요소 및 해당 매핑을 정의할](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)수 있습니다.
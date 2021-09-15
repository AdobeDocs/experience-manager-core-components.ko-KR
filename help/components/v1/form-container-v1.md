---
title: 양식 컨테이너 구성 요소 (v1)
description: 핵심 구성 요소의 양식 컨테이너 구성 요소를 사용하여 간단한 제출용 양식을 작성할 수 있습니다.
index: n
role: Architect, Developer, Admin, User
exl-id: 1e34219f-fa82-494e-82e2-1b4d63d37fea
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: ht
source-wordcount: '638'
ht-degree: 100%

---

# 양식 컨테이너 구성 요소 (v1) {#form-container-component-v1}

핵심 구성 요소의 양식 컨테이너 구성 요소를 사용하여 간단한 제출용 양식을 작성할 수 있습니다.

## 사용량 {#usage}

양식 컨테이너 구성 요소를 통해 간소화된 WCM 양식을 지원하고 추가 양식 구성 요소를 허용하는 중첩된 구조를 사용하여 정보 제출용 양식 및 기능 빌드를 간단하게 활성화합니다.

콘텐츠 편집기는 [설정 대화 상자](#settings-dialog)를 통해 양식 제출로 트리거된 작업 유형, 제출한 다음 저장된 콘텐츠 위치와 워크플로의 트리거 여부를 정의할 수 있습니다. 템플릿 작성자는 [디자인 대화 상자](#design-dialog)를 통해 허용된 구성 요소와 매핑을 정의할 수 있습니다. 이는 [템플릿 편집기의 표준 레이아웃 컨테이너](https://helpx.adobe.com/kr/experience-manager/6-4/sites/authoring/using/templates.html)용 디자인 대화 상자와 매우 유사합니다.

## 버전 및 호환성 {#version-and-compatibility}

이 문서에서는 AEM 6.3을 포함하는 핵심 구성 요소 릴리스 1.0.0과 함께 최초 도입된 양식 컨테이너 구성 요소 v1에 대해 설명합니다.

다음 표에서 양식 컨테이너 구성 요소 v1의 호환성을 확인할 수 있습니다.

| AEM 버전 | 양식 컨테이너 구성 요소 v1 |
|--- |--- |
| 6.3 | 호환 가능 |
| 6.4 | 호환 가능 |

>[!CAUTION]
>
>이 문서에서는 양식 컨테이너 구성 요소 v1에 대해 설명합니다.
>
>현재 버전의 양식 컨테이너 구성 요소에 대한 자세한 내용은 [양식 컨테이너 구성 요소](/help/components/forms/form-container.md) 문서를 참조하십시오.

## 설정 대화 상자 {#settings-dialog}

콘텐츠 작성자는 설정 대화 상자를 통해 구성 요소 제출 시 수행한 작업을 정의할 수 있습니다.

![](/help/assets/chlimage_1.png)

선택한 **작업 유형**&#x200B;에 따라 컨테이너에서 사용 가능한 옵션이 달라집니다. 사용 가능한 작업 유형은 다음과 같습니다.

* [메일](#mail)
* [콘텐츠 저장](#store-content)
* [주문 제출](#submit-order)
* [주문 업데이트](#update-order)

유형에 관계없이 각 작업에 적용되는 [일반 설정](#general-settings)이 있습니다.

### 메일 {#mail}

양식 제출 시 메일 작업 유형은 지정된 수신자에게 이메일을 전송합니다.

![](/help/assets/chlimage_1-1.png)

* **주제** - 양식 제출 시 전송되는 이메일 주제
* **발신자** - 양식 제출 시 전송되는 발신자 이메일 주소
* **수신자** - 양식 제출 시 이메일을 받는 수신자 이메일 주소
   * **추가** 버튼을 탭하거나 클릭하여 주소를 추가합니다.
   * **삭제** 버튼을 탭하거나 클릭하여 이메일 주소를 삭제합니다.
* **CC** - 양식 제출 시 전송된 이메일 복사본을 받는 수신자 이메일 주소
   * **추가** 버튼을 탭하거나 클릭하여 주소를 추가합니다.
   * **삭제** 버튼을 탭하거나 클릭하여 이메일 주소를 삭제합니다.

### 콘텐츠 저장 {#store-content}

양식 제출 시 양식의 콘텐츠는 저장소 위치에 저장됩니다.

![](/help/assets/chlimage_1-2.png)

* **콘텐츠 경로** - 제출된 콘텐츠가 저장되는 콘텐츠 저장소 경로
* **데이터 보기** - 탭하거나 클릭하여 JSON으로 제출되고 나서 저장된 데이터를 조회합니다.
* **워크플로 시작** - 양식 제출 시 페이로드로 저장된 콘텐츠로 워크플로를 시작합니다.

### 주문 제출 {#submit-order}

양식 제출시 주문이 제출됩니다.

![](/help/assets/chlimage_1-3.png)

### 주문 업데이트 {#update-order}

양식 제출 시 주문이 업로드됩니다.

![](/help/assets/chlimage_1-4.png)

### 일반 설정 {#general-settings}

선택한 작업 유형에 관계없이 언제든지 감사 페이지를 정의할 수 있습니다.

![](/help/assets/chlimage_1-5.png)

양식 제출이 완료되면 사용자는 지정된 페이지로 리디렉션됩니다.

* 선택 대화 상자를 통해 AEM 내에서 리소스를 선택합니다.
* 감사 페이지가 AEM에 없는 경우 절대 URL을 지정합니다. 절대 URL이 아닌 URL은 AEM의 상대 URL로 해석될 수 있습니다.
* 제출 후 양식을 다시 표시하려면 비워 둡니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 통해 허용된 구성 요소와 컨테이너에 대한 매핑을 정의할 수 있습니다. 이는 [템플릿 편집기의 표준 레이아웃 컨테이너](https://helpx.adobe.com/kr/experience-manager/6-4/sites/authoring/using/templates.html#main-pars_title_1754153843)용 디자인 대화 상자와 매우 유사합니다.

## 기술 세부 사항 {#technical-details}

양식 컨테이너 구성 요소에 대한 최신 기술 설명서는 [GitHub에서 확인할 수 있습니다](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/container/v1/container).

GitHub에서 전체 핵심 구성 요소 프로젝트를 다운로드할 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

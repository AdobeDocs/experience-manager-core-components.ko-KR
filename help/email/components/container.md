---
title: 이메일 컨테이너 구성 요소
description: 이메일 컨테이너 구성 요소를 통해 이메일 콘텐츠에서 다중 추가 구성 요소의 컨테이너를 만들 수 있습니다.
role: Architect, Developer, Admin, User
exl-id: 3b271e95-0093-4cb1-bb83-8446ba12a821
index: false
source-git-commit: eb77567dc32cccb81a9fc131493d11fb55b7e93b
workflow-type: ht
source-wordcount: '780'
ht-degree: 100%

---


# 이메일 컨테이너 구성 요소 {#email-container-component}

이메일 컨테이너 구성 요소를 통해 이메일 콘텐츠에서 다중 추가 구성 요소의 컨테이너를 만들 수 있습니다.

## 사용 {#usage}

이메일 컨테이너 구성 요소의 컨테이너 구성 요소를 통해 이메일 콘텐츠에서 다중 추가 구성 요소의 컨테이너를 만들 수 있습니다. 그리고 다른 구성 요소를 그룹화하고 일반 스타일 또는 레이아웃을 적용할 수 있습니다.

* [구성 대화 상자](#configure-dialog)에서 컨테이너의 속성을 선택할 수 있습니다.
* 구성 요소를 페이지에 추가하는 경우 [디자인 대화 상자](#design-dialog)에서 이메일 컨테이너 구성 요소의 기본값을 정의할 수 있습니다.

이메일 컨테이너 구성 요소가 페이지에 추가되면 콘텐츠 작성자는 추가 구성 요소를 페이지에 끌어다 놓을 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

현재 버전의 이메일 컨테이너 구성 요소는 2022년 10월 이메일 핵심 구성 요소 릴리스 X과(와) 함께 도입된 v1입니다. 이 문서에서는 해당 구성 요소에 대해 설명합니다.

다음 테이블에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| v1 | 호환 가능 | - | - |

이메일 핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 문서 [이메일 핵심 구성 요소 버전](/help/email/versions.md)을 참조하십시오.

## 기술 세부 정보 {#technical-details}

컨테이너 구성 요소에 대한 최신 기술 설명서는 [GitHub에서 확인할 수 있습니다.](https://adobe.com/go/aem_cmp_tech_email_container_v1_kr)

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

콘텐츠 작성자는 구성 대화 상자를 통해 컨테이너 항목과 이 항목이 콘텐츠에서 작동 및 표시되는 방법을 정의할 수 있습니다.

![이메일 컨테이너 구성 요소의 편집 대화 상자](/help/email/assets/email-container-configure.png)

* **레이아웃** - 이 옵션은 이메일 컨테이너 구성 요소의 비헤이비어 또는 레이아웃 비헤이비어를 정의합니다.
   * **전체 폭**
   * **반|반**
   * **1/3|2/3**
   * **2/3|1/3**
   * **1/3|1/3|1/3**
* **배경색** - [구성에 따라](#container-settings-tab) 자유 형식의 RGB 값이나 색상 피커를 사용하여 정의할 수 있습니다.
* **배경 이미지** - [구성에 따라](#container-settings-tab) 컨테이너 배경 이미지를 정의합니다.
* **ID** - 이 옵션을 통해 HTML에서 구성 요소의 고유 식별자를 제어할 수 있습니다.
   * 비워 두면 고유 ID는 자동으로 생성되고 결과 콘텐츠 검사를 통해 발견될 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID를 변경하면 CSS에 영향을 줄 수 있습니다.

### 스타일 탭 {#styles-tab-edit}

이메일 컨테이너 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

드롭다운을 사용하여 구성 요소에 적용할 스타일을 선택합니다. 편집 대화 상자에서 선택한 항목은 구성 요소 툴바에서 선택한 항목과 동일한 효과를 가집니다.

탭을 사용하려면 [디자인 대화 상자](#design-dialog)에서 이 구성 요소에 대한 스타일을 구성해야 합니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 통해 이메일 컨테이너 구성 요소를 사용하는 콘텐츠 작성자에게 제공되는 옵션을 정의할 수 있습니다.

### 허용된 구성 요소 탭 {#allowed-components-tab}

콘텐츠 작성자는 **허용된 구성 요소**&#x200B;를 통해 항목으로 이메일 컨테이너 구성 요소에 추가 가능한 구성 요소를 정의할 수 있습니다.

[템플릿 편집기의 레이아웃 컨테이너 정책 및 속성을 정의하는 경우](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=ko) **허용된 구성 요소** 탭은 동일한 이름의 탭과 동일한 방식으로 작동합니다.

### 기본 구성 요소 탭 {#default-components-tab}

컨테이너에서 특정 자산 유형이 삭제되면 **기본 구성 요소** 탭을 사용하여 구성 요소에 추가된 구성 요소를 정의할 수 있습니다. 이는 [페이지 템플릿에서 기본 구성 요소를 정의하는 방법](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=ko)과 매우 유사합니다.

### 컨테이너 설정 탭 {#container-settings-tab}

**컨테이너 설정** 탭은 작성자가 배경 이미지 또는 색상을 정의할 수 있는지 정의합니다.

![이메일 컨테이너 구성 요소의 디자인 대화 상자 컨테이너 설정 탭](/help/email/assets/email-container-design-container-settings.png)

* **배경 이미지**
   * **배경 이미지 활성화** - 이 옵션을 선택하여 콘텐츠 작성자는 컨테이너의 배경 이미지를 정의할 수 있습니다.
* **배경색**
   * **배경색 활성화** - 이 옵션을 선택하여 콘텐츠 작성자는 컨테이너의 배경색을 정의할 수 있습니다.
   * **색상 견본만 해당** - 이 옵션을 선택하여 콘텐츠 작성자는 컨테이너 배경색에 대한 사전 정의된 색상 견본을 선택할 수 있습니다.
      * **배경색 활성화**&#x200B;를 선택하는 경우에만 사용할 수 있습니다.
* **허용된 색상 견본** - 사전 정의된 색상에서 콘텐츠 작성자는 컨테이너 배경색을 선택할 수 있습니다.
   * **추가** 버튼을 사용하여 사전 정의된 색상 견본을 추가합니다. 추가되면 다음 열이 포함된 목록에 항목을 추가합니다.
   * **값** - RGB 값을 통해 색상을 수동으로 정의합니다.
      * 색상 피커를 탭하거나 클릭한 다음 개별 RGB 값을 조정하거나 16진수 값을 정의하여 색상을 보다 쉽게 선택합니다.
   * **삭제** - 탭하거나 클릭하여 색상 견본을 삭제합니다.
   * **재배열** - 탭하거나 클릭하고 드래그하여 색상 견본의 순서를 변경합니다.

### 스타일 탭 {#styles-tab}

이메일 컨테이너 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

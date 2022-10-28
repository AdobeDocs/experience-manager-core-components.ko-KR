---
title: 이메일 컨테이너 구성 요소
description: 이메일 컨테이너 구성 요소를 사용하면 이메일 콘텐츠에서 여러 추가 구성 요소를 위한 컨테이너를 만들 수 있습니다.
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 37%

---


# 이메일 컨테이너 구성 요소 {#email-container-component}

이메일 컨테이너 구성 요소를 사용하면 이메일 콘텐츠에서 여러 추가 구성 요소를 위한 컨테이너를 만들 수 있습니다.

## 사용량 {#usage}

이메일 컨테이너 구성 요소를 사용하면 이메일 콘텐츠에서 여러 추가 구성 요소를 위한 컨테이너를 만들 수 있으며, 다른 구성 요소를 그룹화하고 공통 스타일 또는 레이아웃을 적용하는 데 사용할 수 있습니다.

* 컨테이너에서 속성을 선택할 수 있습니다 [구성 대화 상자.](#configure-dialog)
* 페이지에 추가할 때 이메일 컨테이너 구성 요소의 기본값은 [디자인 대화 상자](#design-dialog)

이메일 컨테이너 구성 요소가 페이지에 추가되면 컨텐츠 작성자는 추가 구성 요소를 페이지에 드래그하여 놓을 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

전자 메일 컨테이너 구성 요소의 현재 버전은 v1이며, 2022년 10월에 이메일 핵심 구성 요소의 릴리스 X에서 도입되었으며 이 문서에 설명되어 있습니다.

다음 표에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | 호환 가능 | 호환 가능 |

이메일 핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 문서를 참조하십시오 [이메일 핵심 구성 요소 버전.](/help/email/versions.md)

## 샘플 구성 요소 출력 {#sample-component-output}

구성 옵션과 HTML 및 JSON 출력에 대한 예를 볼 수 있을 뿐만 아니라 이메일 컨테이너 구성 요소를 경험하려면 [구성 요소 라이브러리.](https://adobe.com/go/aem_cmp_library_email_container)

## 기술 세부 사항 {#technical-details}

컨테이너 구성 요소에 대한 최신 기술 설명서는 [GitHub에서 확인할 수 있습니다.](https://adobe.com/go/aem_cmp_tech_email_container_v1)

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서입니다.](/help/developing/overview.md)

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자에서는 컨텐츠 작성자가 컨테이너 항목과 이 항목이 컨텐츠에 어떻게 동작하고 표시되는지를 정의할 수 있습니다.

![전자 메일 컨테이너 구성 요소의 편집 대화 상자](/help/email/assets/email-container-configure.png)

* **레이아웃** - 이 옵션은 전자 메일 컨테이너 구성 요소의 동작 또는 레이아웃 동작을 정의합니다.
   * **전체 너비**
   * **절반**
   * **1/3|2/3**
   * **2/3|1/3**
   * **third|third|third**
* **배경색** - [구성에 따라](#container-settings-tab) 자유 형식의 RGB 값이나 색상 피커를 사용하여 정의할 수 있습니다.
* **배경 이미지** - 컨테이너의 배경 이미지를 정의합니다. [구성에 따라](#container-settings-tab)
* **ID** - 이 옵션을 사용하면 HTML에서 구성 요소의 고유 식별자를 제어할 수 있습니다.
   * 비워 두면 고유 ID가 자동으로 생성되며 결과 컨텐츠를 검사하여 찾을 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID를 변경하면 CSS에 영향을 줄 수 있습니다.

### 스타일 탭 {#styles-tab-edit}

이메일 컨테이너 구성 요소는 AEM을 지원합니다 [스타일 시스템.](/help/get-started/authoring.md#component-styling)

드롭다운을 사용하여 구성 요소에 적용할 스타일을 선택합니다. 편집 대화 상자에서 선택한 항목은 구성 요소 툴바에서 선택한 항목과 동일한 효과를 가집니다.

스타일을 [디자인 대화 상자](#design-dialog) 을 클릭하여 탭을 사용할 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

디자인 대화 상자에서는 템플릿 작성자가 이메일 컨테이너 구성 요소를 사용하는 컨텐츠 작성자가 사용할 수 있는 옵션을 정의할 수 있습니다.

### 허용된 구성 요소 탭 {#allowed-components-tab}

다음 **허용된 구성 요소** 탭은 컨텐츠 작성자가 전자 메일 컨테이너 구성 요소에 항목으로 추가할 수 있는 구성 요소를 정의하는 데 사용됩니다.

다음 **허용된 구성 요소** 탭은 동일한 이름의 탭과 동일한 방식으로 작동합니다. [템플릿 편집기에서 레이아웃 컨테이너의 정책 및 속성 정의.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html)

### 기본 구성 요소 탭 {#default-components-tab}

다음 **기본 구성 요소** 탭에서는 특정 자산 유형이 컨테이너에 삭제될 때 구성 요소에 추가되는 구성 요소를 정의하는 데 사용됩니다. 이는 다음과 같습니다 [페이지 템플릿에서 기본 구성 요소를 정의하는 방법.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html)

### 컨테이너 설정 탭 {#container-settings-tab}

다음 **컨테이너 설정** 탭에는 작성자가 배경 이미지나 색상을 정의할 수 있는지 여부가 정의됩니다.

![전자 메일 컨테이너 구성 요소의 디자인 대화 상자에 있는 컨테이너 설정 탭](/help/email/assets/email-container-design-container-settings.png)

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
   * **다시 정렬** - 색상 견본 순서를 변경하려면 탭하거나 클릭하고 드래그합니다.

### 스타일 탭 {#styles-tab}

이메일 컨테이너 구성 요소는 AEM을 지원합니다 [스타일 시스템.](/help/get-started/authoring.md#component-styling)
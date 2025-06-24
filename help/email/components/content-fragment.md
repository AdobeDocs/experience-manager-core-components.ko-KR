---
title: 이메일 콘텐츠 조각 구성 요소
description: 이메일 콘텐츠 조각 구성 요소를 사용하여 콘텐츠에 콘텐츠 조각을 표시할 수 있습니다.
role: Architect, Developer, Admin, User
exl-id: 9bc6b730-0d2a-4e5b-891c-d2f67f600bcc
index: false
source-git-commit: eb77567dc32cccb81a9fc131493d11fb55b7e93b
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# 이메일 콘텐츠 조각 구성 요소 {#email-content-fragment-component}

이메일 콘텐츠 조각 구성 요소를 사용하여 콘텐츠에 [콘텐츠 조각](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html)을 표시할 수 있습니다.

## 사용 {#usage}

이메일 콘텐츠 조각 구성 요소를 사용하여 이메일 콘텐츠에 [콘텐츠 조각](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html)을 포함할 수 있습니다. 콘텐츠 조각은 중앙에서 작성하고 쉽게 재사용할 수 있는 멀티채널 구조화 콘텐츠입니다.

* [구성 대화 상자](#configure-dialog)에서 조각과 조각의 속성을 선택할 수 있습니다.
* [디자인 대화 상자](#design-dialog)에서 특정 이미지와 그리드를 처리하는 리소스 유형을 정의할 수 있습니다.
* 편집 옵션은 [콘텐츠 조각 편집기](#edit-dialog)내에서 선택한 조각을 엽니다. 이는 이메일 핵심 구성 요소와 함께 사용하도록 사용자 정의됩니다.

## 버전 및 호환성 {#version-and-compatibility}

현재 버전의 이메일 콘텐츠 조각 구성 요소는 2022년 10월 이메일 핵심 구성 요소 릴리스 X과(와) 함께 도입된 v1입니다. 이 문서에서는 해당 구성 요소에 대해 설명합니다.

다음 테이블에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| v1 | 호환 가능 | - | - |

이메일 핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 문서 [이메일 핵심 구성 요소 버전](/help/email/versions.md)을 참조하십시오.

## 기술 세부 정보 {#technical-details}

이메일 콘텐츠 조각 구성 요소에 대한 최신 기술 설명서는 [GitHub에서 확인할 수 있습니다.](https://adobe.com/go/aem_cmp_tech_email_cf_v1_kr)

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

콘텐츠 작성자는 구성 대화 상자를 통해 포함해야 할 콘텐츠 조각과 해당 조각의 요소를 정의할 수 있습니다.

### 속성 탭 {#properties-tab}

![이메일 콘텐츠 조각 구성 요소](/help/email/assets/email-content-fragment-edit-properties.png)

* **콘텐츠 조각**

   * 원하는 콘텐츠 조각의 경로
   * **선택 대화 상자**&#x200B;를 선택하여 조각을 찾을 수 있습니다.

* **표시 모드**
   * **단일 텍스트 요소** - 하나의 여러 줄 텍스트 요소 선택을 활성화하고 단락 제어 옵션을 활성화합니다.
* **변형** - 사용될 콘텐츠 조각의 변형(기본적으로 **마스터**&#x200B;로 설정)

* **ID** - 이 옵션을 통해 HTML에서 구성 요소의 고유 식별자를 제어할 수 있습니다.
   * 비워 두면 고유 ID는 자동으로 생성되고 결과 콘텐츠 검사를 통해 발견될 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID를 변경하면 CSS에 영향을 줄 수 있습니다.

### 단락 제어 탭 {#paragraph-control-tab}

![이메일 콘텐츠 조각 구성 요소](/help/assets/content-fragment-edit-paragraph.png)

* **단락** - 모든 단락 또는 범위를 선택할 수 있습니다.
   * **전체** - 모든 문단이 표시됩니다.
   * **범위**
      * 세미콜론으로 구분되어야 하는 단락의 범위를 지정합니다.
      * 예: 최종 단락에 첫 번째, 세 번째~다섯 번째, 일곱 번째, 아홉 번째 단락이 포함될 `1;3-5;7;9-*`
* **제목을 소유자의 단락으로 처리**

## 편집 대화 상자 {#edit-dialog}

이메일 콘텐츠 조각 구성 요소를 사용하여 콘텐츠 조각을 구성하면 콘텐츠 편집기에서 구성 요소를 선택했을 때 **편집** 옵션으로 표시됩니다.

![이메일 콘텐츠 조각 구성 요소의 도구 모음](/help/email/assets/email-content-fragment-edit-toolbar.png)

**편집** 버튼을 탭하거나 클릭하면 콘텐츠 조각 편집기가 열립니다. 콘텐츠 조각 편집기가 확장되어 Adobe Campaign 변수를 콘텐츠 조각에 삽입하기 위한 **Adobe Campaign 변수 선택** 버튼이 포함되었습니다.

![이메일용 콘텐츠 조각 편집기](/help/email/assets/email-content-fragment-editor.png)

콘텐츠 조각 편집 및 작성에 대한 자세한 내용은 문서 [조각 콘텐츠 작성](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/content-fragments/content-fragments-variations.html)을 참조하십시오.

## 디자인 대화 상자 {#design-dialog}

이메일 콘텐츠 조각 구성 요소가 콘텐츠 조각으로 구성된 경우 콘텐츠 편집기에서 이를 선택하면 도구 모음에 콘텐츠 조각 편집기를 여는 버튼이 표시됩니다.


### 메인 탭 {#main-tab}

![이메일 콘텐츠 조각 구성 요소의 디자인 대화 상자](/help/email/assets/email-content-fragment-design.png)

* **내부 응답형 격자**

   * 내부 응답형 격자에 사용된 슬링 리소스 유형입니다

### 스타일 탭 {#styles-tab}

이메일 경험 조각 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

---
title: 이메일 컨텐츠 조각 구성 요소
description: 이메일 컨텐츠 조각 구성 요소를 사용하면 컨텐츠에 컨텐츠 조각을 표시할 수 있습니다.
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: tm+mt
source-wordcount: '668'
ht-degree: 28%

---


# 이메일 컨텐츠 조각 구성 요소 {#email-content-fragment-component}

이메일 컨텐츠 조각 구성 요소를 사용하면 [콘텐츠 조각](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) 참조하십시오.

## 사용량 {#usage}

이메일 컨텐츠 조각 구성 요소를 사용하면 [콘텐츠 조각](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) 이메일 콘텐츠에서 확인하십시오. 컨텐츠 조각은 중앙에서 작성 및 쉽게 재사용할 수 있는 다중 채널 구조 컨텐츠입니다.

* 조각과 해당 속성은 [구성 대화 상자.](#configure-dialog)
* 특정 이미지와 그리드를 처리하는 리소스 유형은 [디자인 대화 상자](#design-dialog)
* 편집 옵션은 선택한 조각을 [컨텐츠 조각 편집기,](#edit-dialog) 이메일 핵심 구성 요소에 사용할 사용자 지정됨.

## 버전 및 호환성 {#version-and-compatibility}

이메일 컨텐츠 조각 구성 요소의 현재 버전은 v1이며, 이 버전은 2022년 10월에 이메일 핵심 구성 요소의 릴리스 X에서 도입되었으며, 이 문서에 설명되어 있습니다.

다음 표에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | 호환 가능 | 호환 가능 |

이메일 핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 문서를 참조하십시오 [이메일 핵심 구성 요소 버전.](/help/email/versions.md)

## 샘플 구성 요소 출력 {#sample-component-output}

이메일 컨텐츠 조각 구성 요소와 구성 옵션의 예 및 HTML 및 JSON 출력을 보려면 [구성 요소 라이브러리.](https://adobe.com/go/aem_cmp_library_email_cf)

## 기술 세부 사항 {#technical-details}

이메일 컨텐츠 조각 구성 요소에 대한 최신 기술 문서입니다 [GitHub에서 찾을 수 있습니다.](https://adobe.com/go/aem_cmp_tech_email_cf_v1)

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서입니다.](/help/developing/overview.md)

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자에서는 컨텐츠 작성자가 포함할 컨텐츠 조각 및 해당 조각의 요소를 정의할 수 있습니다.

### 속성 탭 {#properties-tab}

![이메일 컨텐츠 조각 구성 요소](/help/email/assets/email-content-fragment-edit-properties.png)

* **콘텐츠 조각**

   * 원하는 콘텐츠 조각의 경로
   * **선택 대화 상자**&#x200B;를 선택하여 조각을 찾을 수 있습니다.

* **표시 모드**
   * **단일 텍스트 요소** - 하나의 여러 줄 텍스트 요소 선택을 활성화하고 단락 제어 옵션을 활성화합니다.
* **변형** - 사용될 콘텐츠 조각의 변형(기본적으로 **마스터**&#x200B;로 설정)

* **ID** - 이 옵션을 사용하면 HTML에서 구성 요소의 고유 식별자를 제어할 수 있습니다.
   * 비워 두면 고유 ID가 자동으로 생성되며 결과 컨텐츠를 검사하여 찾을 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID를 변경하면 CSS에 영향을 줄 수 있습니다.

### 단락 제어 탭 {#paragraph-control-tab}

![이메일 컨텐츠 조각 구성 요소](/help/assets/content-fragment-edit-paragraph.png)

* **단락** - 모든 단락 또는 범위를 선택할 수 있습니다.
   * **전체** - 모든 문단이 표시됩니다.
   * **범위**
      * 세미콜론으로 구분되어야 하는 단락의 범위를 지정합니다.
      * 예 `1;3-5;7;9-*` 첫 번째와 세 번째와 다섯 번째와, 일곱 번째와, 아홉 번째 부분과, 마지막 단락을 함께 묶어서,
* **제목을 소유자의 단락으로 처리**

## 편집 대화 상자 {#edit-dialog}

이메일 컨텐츠 조각 구성 요소를 사용하여 컨텐츠 조각을 구성했으면 컨텐츠 편집기에서 구성 요소를 선택하면 컨텐츠 조각에 **편집** 선택 사항입니다.

![이메일 컨텐츠 조각 구성 요소의 도구 모음](/help/email/assets/email-content-fragment-edit-toolbar.png)

을 탭하거나 클릭합니다. **편집** 버튼을 클릭하면 컨텐츠 조각 편집기가 열립니다. 컨텐츠 조각 편집기가 을 위한 단추를 포함하도록 확장되었습니다 **Adobe Campaign 변수 선택** 컨텐츠 조각에 Adobe Campaign 변수를 삽입하려면 다음을 수행하십시오.

![이메일용 컨텐츠 조각 편집기](/help/email/assets/email-content-fragment-editor.png)

컨텐츠 조각 편집 및 작성에 대한 자세한 내용은 문서를 참조하십시오 [조각 컨텐츠 작성.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/content-fragments/content-fragments-variations.html)

## 디자인 대화 상자 {#design-dialog}

이메일 컨텐츠 조각 구성 요소가 컨텐츠 조각으로 구성되면 컨텐츠 편집기에서 선택하면 도구 모음에 컨텐츠 조각 편집기를 여는 단추가 표시됩니다.


### 메인 탭 {#main-tab}

![이메일 컨텐츠 조각 구성 요소의 디자인 대화 상자](/help/email/assets/email-content-fragment-design.png)

* **내부 응답형 격자**

   * 내부 응답형 격자에 사용된 슬링 리소스 유형입니다

### 스타일 탭 {#styles-tab}

이메일 경험 조각 구성 요소는 AEM을 지원합니다 [스타일 시스템.](/help/get-started/authoring.md#component-styling)

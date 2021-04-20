---
title: 양식 컨테이너 구성 요소
description: 핵심 구성 요소 양식 컨테이너 구성 요소를 사용하면 간단한 제출 양식을 만들 수 있습니다.
role: Architect, Developer, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '961'
ht-degree: 2%

---


# 양식 컨테이너 구성 요소 {#form-container-component}

핵심 구성 요소 양식 컨테이너 구성 요소를 사용하면 간단한 제출 양식을 만들 수 있습니다.

## 사용량 {#usage}

양식 컨테이너 구성 요소를 사용하면 간단한 WCM 양식을 지원하고 중첩된 구조를 사용하여 추가 양식 구성 요소를 허용하도록 간단한 정보 제출 양식 및 기능을 작성할 수 있습니다.

[구성 대화 상자](#configure-dialog)를 사용하면 내용 편집자는 양식 제출 시 트리거되는 작업, 제출을 처리해야 하는 URL 및 워크플로우를 트리거해야 하는지 여부를 정의할 수 있습니다. 템플릿 작성자는 [디자인 대화 상자](#design-dialog)를 사용하여 템플릿 편집기](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)의 [표준 레이아웃 컨테이너에 대한 디자인 대화 상자와 유사한 허용되는 구성 요소 및 해당 매핑을 정의할 수 있습니다.

>[!NOTE]
>
>핵심 구성 요소 양식 컨테이너 구성 요소는 핵심 구성 요소(단추, 텍스트, 숨김 등)의 사용만 지원합니다. 핵심 구성 요소 양식 컨테이너 내에 있는 [기본 구성 요소](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/default-components-foundation.html) 양식 구성 요소를 사용하는 것은 지원되지 않습니다(그 반대의 경우).

## 버전 및 호환성 {#version-and-compatibility}

양식 컨테이너 구성 요소의 현재 버전은 v2로, 2018년 1월에 핵심 구성 요소 릴리스 2.0.0에 도입되었으며 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소 버전이 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | 호환 가능 | 호환 가능 | 호환 가능 |
| [v1](/help/components/v1/form-container-v1.md) | 호환 가능 | 호환 가능 | - |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

양식 컨테이너 구성 요소와 구성 옵션의 예 및 HTML 및 JSON 출력을 보려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_form_container)를 방문하십시오.

## 기술 세부 정보 {#technical-details}

양식 컨테이너 구성 요소 [에 대한 최신 기술 문서는 GitHub](https://adobe.com/go/aem_cmp_tech_form_container_v2)에서 찾을 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)에서 확인할 수 있습니다.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자를 사용하면 컨텐츠 작성자가 구성 요소를 제출할 때 수행되는 작업을 정의할 수 있습니다.

선택한 **작업 유형**&#x200B;에 따라 컨테이너 내의 사용 가능한 옵션이 변경됩니다. 사용 가능한 작업 유형은 다음과 같습니다.

* [게시물 양식 데이터](#post-data)
* [메일](#mail)
* [컨텐츠 저장](#store-content)

유형에 관계없이 각 작업에 적용되는 [일반 설정](#general-settings)이 있습니다.

### 게시물 양식 데이터 {#post-data}

양식이 제출되면, 양식 데이터 작업 유형은 제출된 데이터를 처리를 위해 제3자에게 JSON으로 전달합니다.

![양식 컨테이너 구성 요소의 편집 대화 상자에서 양식 데이터 게시 옵션](/help/assets/form-container-edit-post.png)

* **끝점**  - 데이터를 처리할 정규화된 HTTPS 서비스
* **오류 메시지**  - 제출이 실패할 경우 표시할 메시지입니다.

>[!TIP]
>시스템 관리자가 전달된 양식 데이터의 처리를 처리하도록 조정할 수 있는 추가 시간 제한 옵션이 있습니다. [자세한 내용은 GitHub에 대한 기술 설명서를 참조하십시오.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/actions/rpc)

### 메일 {#mail}

양식이 제출되면 메일 작업 유형은 지정된 수신자에게 이메일을 보냅니다.

![양식 컨테이너 구성 요소의 편집 대화 상자의 메일 옵션](/help/assets/form-container-edit-mail.png)

* **제목**  - 양식 제출 시 보내는 이메일의 제목
* **보낸 사람**  - 양식 제출 시 보낼 이메일의 보낸 사람 이메일 주소입니다.
* **받는 사람**  - 양식 제출 시 이메일을 받을 받는 받는 사람의 주소
   * 추가 주소를 추가하려면 **추가** 단추를 탭하거나 클릭합니다.
   * **삭제** 단추를 탭하거나 클릭하여 이메일 주소를 제거합니다.
* **CC**  - 양식 제출 시 보낸 전자 메일을 받을 수신자의 주소
   * 추가 주소를 추가하려면 **추가** 단추를 탭하거나 클릭합니다.
   * **삭제** 단추를 탭하거나 클릭하여 이메일 주소를 제거합니다.

### 컨텐츠 저장 {#store-content}

양식이 제출되면 양식의 컨텐츠가 지정된 저장소 위치에 저장됩니다.

![양식 컨테이너의 편집 대화 상자에 컨텐츠 옵션 저장](/help/assets/form-container-edit-store.png)

* **컨텐츠 경로**  - 제출된 컨텐츠가 저장되는 컨텐츠 저장소 경로
* **데이터**  보기 - 제출한 저장된 데이터를 JSON으로 보려면 탭하거나 클릭합니다.
* **워크플로우**  시작 - 양식 제출 시 저장된 컨텐츠를 페이로드로 사용하여 워크플로우를 시작하도록 구성합니다.

>[!NOTE]
>
>사용자 데이터 관리를 간소화하고 문제 분리를 적용하기 위해 일반적으로 저장소 내에 사용자 생성 컨텐츠를 저장하지 않는 것이 좋습니다.
>
>대신 [게시물 양식 데이터](#post-data) 작업 유형을 사용하여 전용 서비스 공급자에게 사용자 컨텐츠를 전달합니다.

### 일반 설정 {#general-settings}

선택한 작업 유형에 관계없이 감사 인사 페이지를 항상 정의할 수 있습니다.

![양식 컨테이너 구성 요소의 편집 대화 상자의 일반 옵션](/help/assets/form-container-edit-general.png)

* **감사 인사 페이지**  - 양식 제출 완료 후 사용자가 지정된 페이지로 리디렉션됩니다.
   * [선택] 대화 상자를 사용하여 AEM 내의 리소스를 선택합니다.
   * 감사 인사 페이지가 AEM에 없는 경우 절대 URL을 지정합니다. 절대 URL이 아닌 URL은 AEM에 대해 해석됩니다.
   * 양식을 제출한 후 다시 표시하려면 비워 둡니다.
* **ID**  - 이 옵션을 사용하면 HTML 및 데이터 레이어에서 구성 요소의 고유 식별자를 제어할  [수 있습니다](/help/developing/data-layer/overview.md).
   * 비워 두면 자동으로 고유 ID가 생성되며 결과 페이지를 검사하여 찾을 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID를 변경하면 CSS, JS 및 데이터 레이어 추적에 영향을 줄 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 사용하여 템플릿 편집기](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)에 있는 [표준 레이아웃 컨테이너에 대한 디자인 대화 상자와 유사한 컨테이너에 대해 허용된 구성 요소 및 해당 매핑을 정의할 수 있습니다.

### 스타일 탭 {#styles-tab}

양식 컨테이너 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

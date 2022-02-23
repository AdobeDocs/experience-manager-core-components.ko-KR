---
title: 양식 컨테이너 구성 요소
description: 핵심 구성 요소의 양식 컨테이너 구성 요소를 사용하여 간단한 제출용 양식을 작성할 수 있습니다.
role: Architect, Developer, Admin, User
exl-id: 552f9dd5-6a3a-42d9-9969-e62a1f36e811
source-git-commit: 9767a3a10cb9a77f385edc0ac3fb00096c0087af
workflow-type: ht
source-wordcount: '954'
ht-degree: 100%

---

# 양식 컨테이너 구성 요소 {#form-container-component}

핵심 구성 요소의 양식 컨테이너 구성 요소를 사용하여 간단한 제출용 양식을 작성할 수 있습니다.

## 사용량 {#usage}

양식 컨테이너 구성 요소를 통해 간소화된 WCM 양식을 지원하고 추가 양식 구성 요소를 허용하는 중첩된 구조를 사용하여 정보 제출용 양식 및 기능 빌드를 간단하게 활성화합니다.

콘텐츠 편집기는 [구성 대화 상자](#configure-dialog)를 통해 양식 제출로 트리거된 작업, 제출을 처리하는 URL과 워크플로의 트리거 여부를 정의할 수 있습니다. 템플릿 작성자는 [디자인 대화 상자](#design-dialog)를 통해 허용된 구성 요소와 매핑을 정의할 수 있습니다. 이는 [템플릿 편집기의 표준 레이아웃 컨테이너](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html)용 디자인 대화 상자와 매우 유사합니다.

>[!NOTE]
>
>핵심 구성 요소의 양식 컨테이너 구성 요소는 핵심 구성 요소의 양식 구성 요소(예: 버튼, 텍스트, 숨김 등) 사용만 지원합니다. 핵심 구성 요소의 양식 컨테이너 구성 요소 내 [기초 구성 요소](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/siteandpage/default-components-foundation.html)의 양식 구성 요소 사용(그 반대의 경우도 가능)은 지원되지 않습니다.

## 버전 및 호환성 {#version-and-compatibility}

현재 버전의 양식 컨테이너 구성 요소는 2018년 1월 핵심 구성 요소 릴리스 2.0.0과 함께 도입된 v2입니다. 이 문서에서는 해당 구성 요소에 대해 설명합니다.

다음 표에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | 호환 가능 <br>[2.17.4](/help/versions.md) 및 이전 릴리스 | 호환 가능 | 호환 가능 |
| [v1](/help/components/v1/form-container-v1.md) | 호환 가능 | 호환 가능 | - |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md)을 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

양식 컨테이너 구성 요소를 경험하고 구성 옵션의 샘플뿐만 아니라 HTML 및 JSON 출력을 확인하려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_form_container_kr)를 참조하십시오.

## 기술 세부 사항 {#technical-details}

양식 컨테이너 구성 요소에 대한 최신 기술 설명서는 [GitHub에서 확인할 수 있습니다](https://adobe.com/go/aem_cmp_tech_form_container_v2_kr).

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

콘텐츠 작성자는 구성 대화 상자를 통해 구성 요소 제출 시 수행한 작업을 정의할 수 있습니다.

선택한 **작업 유형**&#x200B;에 따라 컨테이너에서 사용 가능한 옵션이 달라집니다. 사용 가능한 작업 유형은 다음과 같습니다.

* [게시물 양식 데이터](#post-data)
* [메일](#mail)
* [콘텐츠 저장](#store-content)

유형에 관계없이 각 작업에 적용되는 [일반 설정](#general-settings)이 있습니다.

### 게시물 양식 데이터 {#post-data}

양식 제출 시 게시물 양식 데이터 작업 유형을 JSON으로 제출된 데이터를 서드파티에 전달하여 처리합니다.

![양식 컨테이너 구성 요소 편집 대화 상자의 게시물 양식 데이터 옵션](/help/assets/form-container-edit-post.png)

* **끝점** - 데이터를 처리하는 정규화된 HTTPS 서비스
* **오류 메시지** - 제출 실패 시 표시되는 메시지

>[!TIP]
>전송된 형식 데이터 처리를 위해 시스템 관리자가 조정할 수 있는 추가 제한 시간 옵션이 있습니다. 자세한 내용은 [GitHub에 대한 기술 설명서](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/actions/rpc)를 참조하십시오.

### 메일 {#mail}

양식 제출 시 메일 작업 유형은 지정된 수신자에게 이메일을 전송합니다.

![양식 컨테이너 구성 요소 편집 대화 상자의 메일 옵션](/help/assets/form-container-edit-mail.png)

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

![양식 컨테이너 구성 요소 편집 대화 상자의 콘텐츠 저장 옵션](/help/assets/form-container-edit-store.png)

* **콘텐츠 경로** - 제출된 콘텐츠가 저장되는 콘텐츠 저장소 경로
* **데이터 보기** - 탭하거나 클릭하여 JSON으로 제출되고 나서 저장된 데이터를 조회합니다.
* **워크플로 시작** - 양식 제출 시 페이로드로 저장된 콘텐츠로 워크플로를 시작합니다.

>[!NOTE]
>
>사용자 데이터를 보다 간편하게 관리하고 문제를 분리하려면 사용자 생성 콘텐츠를 저장소에 저장하지 않는 것이 좋습니다.
>
>대신 [게시물 양식 데이터](#post-data) 작업 유형을 사용하여 전용 서비스 공급자에게 사용자 콘텐츠를 전달합니다.

### 일반 설정 {#general-settings}

선택한 작업 유형에 관계없이 언제든지 감사 페이지를 정의할 수 있습니다.

![양식 컨테이너 구성 요소 편집 대화 상자의 일반 옵션](/help/assets/form-container-edit-general.png)

* **감사 페이지** - 양식 제출이 완료되면 사용자는 지정된 페이지로 리디렉션됩니다.
   * 선택 대화 상자를 통해 AEM 내에서 리소스를 선택합니다.
   * 감사 페이지가 AEM에 없는 경우 절대 URL을 지정합니다. 절대 URL이 아닌 URL은 AEM의 상대 URL로 해석될 수 있습니다.
   * 제출 후 양식을 다시 표시하려면 비워 둡니다.
* **ID** - 이 옵션을 통해 HTML과 [데이터 레이어](/help/developing/data-layer/overview.md)에서 구성 요소의 고유 식별자를 제어할 수 있습니다.
   * 비워 두면 고유 ID는 자동으로 생성되고 결과 페이지 검사를 통해 발견될 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID가 변경되면 CSS, JS 및 데이터 레이어 추적에 영향을 미칠 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 통해 허용된 구성 요소와 컨테이너에 대한 매핑을 정의할 수 있습니다. 이는 [템플릿 편집기의 표준 레이아웃 컨테이너](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html)용 디자인 대화 상자와 매우 유사합니다.

### 스타일 탭 {#styles-tab}

형식 컨테이너 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

---
title: 양식 텍스트 구성 요소
description: 핵심 구성 요소의 양식 텍스트 구성 요소를 사용하여 제출용 양식 텍스트를 입력합니다.
role: Architect, Developer, Admin, User
exl-id: e8fa3881-51fb-4726-9654-8f93acfb7464
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: ht
source-wordcount: '578'
ht-degree: 100%

---

# 양식 텍스트 구성 요소{#form-text-component}

핵심 구성 요소의 양식 텍스트 구성 요소를 사용하여 제출용 양식 텍스트를 입력합니다.

## 사용량 {#usage}

양식 텍스트 구성 요소를 사용하여 다양한 유형의 텍스트를 제출하고, [양식 컨테이너 구성 요소](form-container.md)와 함께 이 구성 요소를 사용할 수 있습니다. 콘텐츠 편집기는 [구성 대화 상자](#configure-dialog)에서 텍스트 유효성 검사 유형, 라벨 및 도움말 메시지를 정의할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

현재 버전의 양식 텍스트 구성 요소는 2018년 1월 핵심 구성 요소 릴리스 2.0.0과 함께 도입된 v2입니다. 이 문서에서는 해당 구성 요소에 대해 설명합니다.

다음 테이블에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|---|
| v2 | <br>[릴리스 2.17.4](/help/versions.md) 및 이전 버전과 호환 가능 | 호환 가능 | 호환 가능 | 호환 가능 |
| [v1](/help/components/v1/form-text-v1.md) | 호환 가능 | 호환 가능 | - | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md)을 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

양식 텍스트 구성 요소를 경험하고 구성 옵션의 샘플뿐만 아니라 HTML 및 JSON 출력을 확인하려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_form_text_kr)를 참조하십시오.

### 기술 세부 정보 {#technical-details}

양식 텍스트 구성 요소에 대한 최신 기술 설명서는[ GitHub에서 확인할 수 있습니다](https://adobe.com/go/aem_cmp_tech_form_text_v2_kr).

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

콘텐츠 작성자는 구성 대화 상자를 통해 입력할 텍스트 유형뿐만 아니라 기본값 및 라벨을 정의할 수 있습니다.

### 속성 탭 {#properties-tab}

![속성 탭](/help/assets/form-text-edit-properties.png)

* **제한** - 입력할 텍스트 유형은 다음을 통해 유효성이 확인됩니다.
   * **텍스트**
   * **텍스트 영역**
   * **이메일**
   * **전화**
   * **날짜**
   * **번호**
   * **암호**
* **텍스트 라인** - 텍스트 영역에 표시될 라인 수(**제한**&#x200B;이 **텍스트 영역**&#x200B;으로 설정될 경우에만 표시)
* **라벨** - 필드에 표시될 라벨
* **라벨이 표시되지 않도록 숨기기** - 손쉬운 사용을 위해 라벨이 필요한 경우. 필드에 대해 시각적 정보를 추가로 제공하지 않음
* **요소 이름** - 양식 데이터로 제출된 필드의 이름
* **값** - 필드에 미리 채워진 기본값
* **ID** - 이 옵션을 통해 HTML과 [데이터 레이어](/help/developing/data-layer/overview.md)에서 구성 요소의 고유 식별자를 제어할 수 있습니다.
   * 비워 두면 고유 ID는 자동으로 생성되고 결과 페이지 검사를 통해 발견될 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID가 변경되면 CSS, JS 및 데이터 레이어 추적에 영향을 미칠 수 있습니다.

### 탭 정보 {#about-tab}

![탭 정보](/help/assets/form-text-edit-about.png)

* **도움말 메시지** - 필드에 입력할 수 있는 것에 대한 사용자용 힌트
* **도움말 메시지를 플레이스홀더로 표시** - 양식이 비어 있고 포커스를 두지 않았을 때 양식 입력 내부에 도움말 메시지를 표시할지 여부

### 제한 탭 {#constraints-tab}

![제한 탭](/help/assets/form-text-edit-constraints.png)

* **제한 메시지**
   * 값이 선택된 유형에 대한 유효성을 검사하지 못할 경우 양식을 제출할 때 도구 설명으로 표시되는 메시지
   * **텍스트** 및 **텍스트 영역** 제한 유형에 표시되지 않음
* **필수** - 이 옵션을 선택하면 사용자는 양식을 제출하기 전에 값을 채워야 함
   * **필수 메시지** - 필드를 비워 두면 툴팁으로 표시되는 메시지
* **읽기 전용** - 이 옵션을 선택하면 사용자는 필드 값을 수정할 수 없음

## 디자인 대화 상자 {#design-dialog}

### 스타일 탭 {#styles-tab}

양식 텍스트 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

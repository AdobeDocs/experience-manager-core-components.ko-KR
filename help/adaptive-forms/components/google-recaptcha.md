---
title: 적응형 양식 핵심 구성 요소 - 양식 컨테이너
description: 웹 페이지에 적응형 양식을 추가합니다.
role: Architect, Developer, Admin, User
hide: true
hidefromtoc: true
source-git-commit: 9a80b453d6a6cf7b347128654d3b5e673a063505
workflow-type: ht
source-wordcount: '723'
ht-degree: 100%

---


# Google reCAPTCHA {#google-recaptcha}

CAPTCHA(컴퓨터와 인간을 구분하기 위해 완전히 자동화된 공공 튜링 테스트)는 인간과 자동화된 프로그램 또는 봇을 구별하기 위해 온라인 거래에서 일반적으로 사용되는 프로그램입니다. 문제를 제기하고 사용자 응답을 평가하여 사이트와 상호 작용하는 것이 인간인지 봇인지 판단합니다. 테스트가 실패할 경우 사용자가 진행하지 못하도록 차단하고 봇이 스팸을 게시하거나 악의적인 목적으로 상호 작용하는 것을 방지하여 온라인 거래를 안전하게 할 수 있도록 도와줍니다.

AEM Forms as a Cloud Service는 적응형 양식에서 Google reCAPTCHA v2를 지원합니다. 양식 제출 시 CAPTCHA 문제를 표시하는 데 사용할 수 있습니다.

## 사용 {#reasons-to-use-google-recaptcha}


- **스팸 및 봇 방지**: reCAPTCHA를 사용하는 주요 이유 중 하나는 스팸 제출을 방지하고 악성 봇이 양식을 넘치게 하도록 방지하기 위함입니다. reCAPTCHA의 고급 알고리즘은 양식을 제출하려는 자동화된 시도를 감지할 수 있으므로 적합한 사용자만 양식과 상호 작용할 수 있습니다.

- **개선된 보안**: reCAPTCHA를 구현하면 적응형 양식에 추가 보안 계층을 추가할 수 있습니다. 이를 통해 중요한 정보를 보호하고 악의적인 사용자가 취약점을 악용하지 못하도록 방지할 수 있습니다.

- **사용자 경험**: CAPTCHA는 때때로 불편하게 보일 수 있지만 reCAPTCHA의 적응형 접근 방식은 대부분의 사용자에게 최소한의 상호 작용을 요구하는 능률적이고 사용자 친화적인 환경을 제공합니다. 이를 통해 봇을 억제하면서 긍정적인 사용자 경험을 유지할 수 있습니다.

- **적응성**: reCAPTCHA의 적응 메커니즘은 사용자 행동과 상호 작용을 분석하여 사람인지 아닌지를 판단합니다. 즉, 사용자에게 제시되는 문제의 수준은 사용자가 봇일 가능성에 따라 달라질 수 있습니다. 이러한 적응성은 강력한 보안을 유지함과 동시에 실제 사용자의 마찰을 줄입니다.

- **수동 관리 감소**: reCAPTCHA는 스팸 제출 및 봇이 생성하는 콘텐츠의 수를 크게 줄임으로써 수동 관리 및 정리에 소요되는 시간과 리소스를 절약할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

적응형 양식 Google reCAPTCHA 핵심 구성 요소는 핵심 구성 요소 “버전”의 일부로 2023년 8월에 출시되었습니다. 다음 표에서는 지원되는 모든 버전, AEM 호환성 및 해당 문서에 대한 링크를 보여 줍니다.

|  |  |
|---|---|
| 구성 요소 버전 | AEM as a Cloud Service |
| --- | --- |
| v1 | 호환 가능 <br>[2.0.4](/help/versions.md) 및 이후 릴리스 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md) 문서를 참조하십시오.

## 기술 세부 정보 {#technical-details}

적응형 양식 Google reCAPTCHA 핵심 구성 요소에 대한 최신 정보는 [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/recaptcha/v1/recaptcha)의 기술 설명서에서 확인할 수 있습니다. 핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 확인하십시오.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자를 사용하여 방문자를 위한 Google reCAPTCHA 경험을 손쉽게 사용자 정의할 수 있습니다. Google reCAPTCHA 옵션을 간편하게 정의하여 원활한 사용자 경험을 제공할 수도 있습니다.

### 기본 탭 {#basic-tab}

- **이름** - 양식과 규칙 편집기 모두에서 고유한 이름으로 양식 구성 요소를 쉽게 식별할 수 있습니다. 단, 이름에는 공백이나 특수 문자가 포함되어서는 안 됩니다.

- **제목** - 제목을 사용하면 양식에서 구성 요소를 쉽게 식별할 수 있으며, 기본적으로 제목은 구성 요소 상단에 나타납니다. 제목을 추가하지 않으면 제목 텍스트 대신 구성 요소의 이름이 표시됩니다.

- **제목 숨기기** - 구성 요소의 제목을 숨기려면 이 옵션을 선택합니다.

- **구성** -

- **유형** -

- **구성 요소 숨기기** - 양식에서 구성 요소를 숨기려면 이 옵션을 선택합니다. 구성 요소는 다른 용도로(예: 규칙 편집기에서 계산에 사용) 계속 액세스할 수 있습니다. 구성 요소 숨기기는 사용자가 보거나 직접 변경할 필요가 없는 정보를 저장해야 할 때 유용합니다.

- **구성 요소 비활성화** - 구성 요소를 비활성화하려면 이 옵션을 선택합니다. 비활성화된 구성 요소는 활성 상태가 아니므로 최종 사용자가 편집할 수 없습니다. 비활성화된 구성 요소의 데이터는 제출되지 않습니다. 사용자는 필드의 값을 볼 수 있지만 수정할 수는 없습니다. 구성 요소는 다른 용도로(예: 규칙 편집기에서 계산에 사용) 계속 액세스할 수 있습니다.

- **읽기 전용** - 구성 요소를 편집할 수 없도록 만들려면 이 옵션을 선택합니다. 사용자는 필드 값을 볼 수 있지만 수정할 수는 없습니다. 구성 요소는 다른 용도로(예: 규칙 편집기에서 계산에 사용) 계속 액세스할 수 있습니다.

### 유효성 검사 탭 {#validation-tab}

- **오류 메시지** - 이 옵션을 사용하면 **필수** 확인란이 선택되어 있고 양식 필드가 비어 있는 경우 표시되는 메시지를 입력할 수 있습니다.


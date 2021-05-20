---
title: 핵심 구성 요소에 대한 AMP 지원
description: 핵심 구성 요소 지원 AMP - 가속 모바일 페이지
role: Architect, Developer, Administrator
exl-id: 1fd9b6b5-0e4d-48c7-8faa-42e0d4a6bbd0
source-git-commit: 8ff36ca143af9496f988b1ca65475497181def1d
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 1%

---

# 코어 구성 요소 {#amp-support}에 대한 AMP 지원

코어 구성 요소 중 [릴리스 2.11.0](/help/versions.md)AMP - 가속 모바일 페이지](https://developers.google.com/amp) 는 완전히 지원됩니다.[

이 문서에서는 AMP가 지원되는 방법과 사이트에 대해 AMP를 활성화하는 방법에 대한 개요를 제공합니다. 그러나 기술적인 세부 사항은 [GitHub 개발자 설명서를 참조하십시오.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)

## AMP란 무엇입니까?{#what-is-amp}

가속 모바일 페이지 또는 AMP는 본래 Google이 모바일 탐색을 위해 페이지를 최적화하기 위해 설계한 오픈 소스 프레임워크입니다. AMP 페이지는 일반적으로 표준 웹 페이지보다 훨씬 더 빠르게 로드되므로 더 나은 모바일 경험을 제공합니다.

## 코어 구성 요소 {#amp-in-core-components}의 AMP

코어 구성 요소에서 AMP에 대한 지원은 [완전히 구성할 수 있습니다.](#enabling-amp) AMP 버전의 페이지는 표준 HTML 버전과 함께 독점적으로 제공되거나 전혀 제공되지 않을 수 있습니다.

코어 구성 요소는 `amp` 을 Sling 선택기로 사용하여 AMP 페이지를 렌더링합니다. 예를 들어 `example.html`은 일반 페이지를 렌더링하고 `example.amp.html`은 AMP 버전입니다.

개별 프로젝트는 AMP를 활용할지 여부를 결정할 수 있습니다. 실제로 AMP와 표준 HTML 페이지를 동시에 전달할 수 있으므로 프로젝트는 프로젝트의 특정 페이지에서만 AMP를 사용하도록 선택할 수 있습니다.

## 프로젝트에서 AMP 지원 시작하기 {#getting-started}

AMP 지원은 매우 많은 유연성을 제공하지만 빠르게 시작하려면 몇 가지 간단한 단계만 필요합니다.

1. 필요한 경우 AMP 지원 확장을 설치합니다.
   * AEM as a Cloud Service 프로젝트의 경우 코어 구성 요소에서 확장을 자동으로 사용할 수 있으며 설치할 필요가 없습니다.
   * 온-프레미스 및 AMS 프로젝트의 경우 코어 구성 요소를 설치할 때 확장을 명시적으로 설치해야 합니다.
1. AMP 확장이 설치되면 구성 요소 작성자는 구성 요소 슈퍼 유형을 확장의 구성 요소 수퍼 유형만 가리켜야 합니다.
1. [템플릿 ](#enabling-amp) 수준 또는 개별 페이지에서 AMP 지원을 활성화합니다.
1. [필요에 ](#css-requirements) 따라 인라인 CSS를 배포합니다.

### 페이지용 AMP {#enabling-amp} 활성화

페이지에 대해 AMP를 활성화하려면 **AMP 모드**&#x200B;를 [페이지 정책에서 선택해야 합니다.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html#editing-a-template-page-policy-template-author-developer)

![AMP 페이지 정책 옵션](/help/assets/amp-policy.png)

* **AMP 없음**  - 페이지가 표준 HTML로만 전달됩니다.
* **연결된 AMP**  - 페이지가 HTML뿐만 아니라 AMP로 전달됩니다.
* **AMP만**  - 페이지가 AMP로만 전달됩니다.

페이지에 대한 AMP 설정은 개별 페이지의 [페이지 속성](https://docs.adobe.com/content/help/ko-KR/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html)에서도 무시할 수 있습니다.

![AMP 페이지 속성](/help/assets/amp-page-properties.png)

* **페이지 템플릿에서 상속**  - 기본 값으로서 페이지 템플릿의 정책에서 설정을 가져올 수 있습니다.
* **AMP 없음**  - 페이지가 표준 HTML로만 전달됩니다.
* **연결된 AMP**  - 페이지가 HTML뿐만 아니라 AMP로 전달됩니다.
* **AMP만**  - 페이지가 AMP로만 전달됩니다.

### CSS 요구 사항 {#css-requirements}

핵심 구성 요소로 AMP를 사용하는 경우, 주요 차이점은 AMP를 사용하려면 모든 [CSS가 최적화되었을 뿐만 아니라 `<head>` 요소에 삽입되어야 한다는 것입니다.](including-clientlibs.md#inlining)

이 기능을 지원하기 위해 사용자 지정된 페이지 구성 요소가 사용되며 이 구성 요소는 페이지에 있는 구성 요소에 대해 AMP별 CSS만 로드합니다.

>[!NOTE]
>
>AMP 디자인 제한 사항으로 인해 Adobe은 페이지의 AMP 버전에서 응답형 그리드의 사용을 지원하지 않습니다.

추가적인 요구 사항 및 기술 세부 사항은 [GitHub 개발자 설명서를 참조하십시오.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)

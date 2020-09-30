---
title: 핵심 구성 요소에 대한 AMP 지원
description: 핵심 구성 요소 지원 AMP - 가속 모바일 페이지
translation-type: tm+mt
source-git-commit: 2926c51c2ab97b50b9ec4942cd5415c15a1411b6
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---


# 핵심 구성 요소에 대한 AMP 지원 {#amp-support}

핵심 구성 요소 [의 릴리스 2.11.0](/help/versions.md) 현재 [AMP - 가속 모바일 페이지](https://developers.google.com/amp) 가 완벽하게 지원됩니다.

이 문서에서는 AMP가 지원되는 방법과 사이트에 대해 AMP를 활성화하는 방법에 대해 간략하게 설명합니다. 그러나 자세한 기술 정보는 [GitHub 개발자 설명서를 참조하십시오.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)

## AMP란? {#what-is-amp}

가속화된 모바일 페이지 또는 AMP는 Google이 모바일 검색에 맞게 페이지를 최적화하기 위해 원래 디자인한 오픈 소스 프레임워크입니다. AMP 페이지는 일반적으로 표준 웹 페이지보다 훨씬 빠르게 로드되므로 모바일 경험을 향상시킬 수 있습니다.

## 핵심 구성 요소의 AMP {#amp-in-core-components}

핵심 구성 요소의 AMP에 대한 지원은 [완전히 구성할 수 있습니다.](#enabling-amp) AMP 버전의 페이지는 표준 HTML 버전과 함께 단독으로 제공되거나 전혀 제공되지는 않습니다.

코어 구성 요소는 스링 선택기 `amp` 로 사용하여 AMP 페이지를 렌더링합니다. 예를 `example.html` 들어 일반 페이지를 렌더링하고 AMP 버전 `example.amp.html` 이 됩니다.

개별 프로젝트는 AMP를 활용할지 여부를 결정할 수 있습니다. 실제로 AMP와 표준 HTML 페이지를 동시에 전달할 수 있으므로 프로젝트의 특정 페이지만 AMP를 사용하도록 선택할 수 있습니다.

## 프로젝트에서 AMP 지원 시작 {#getting-started}

AMP 지원에서는 상당한 유연성을 제공하지만 AMP를 빠르게 시작하려면 간단한 몇 단계만 있으면 됩니다.

1. 필요한 경우 AMP 지원 확장 프로그램을 설치합니다.
   * AEM의 Cloud Service 프로젝트의 경우 확장 기능은 핵심 구성 요소에서 자동으로 사용할 수 있으며 설치할 필요가 없습니다.
   * 온-프레미스 및 AMS 프로젝트의 경우 핵심 구성 요소를 설치할 때 익스텐션을 명시적으로 설치해야 합니다.
1. AMP 확장이 설치되면 구성 요소 작성자는 구성 요소 슈퍼 유형을 확장자에 가리켜야 합니다.
1. [템플릿 수준 또는 개별 페이지에서 AMP 지원을](#enabling-amp) 활성화합니다.
1. [필요에 따라 인라인 CSS를](#css-requirements) 배포합니다.

### 페이지에 대해 AMP 활성화 {#enabling-amp}

페이지에 대해 AMP를 활성화하려면 **페이지 정책** 에서 AMP 모드를 선택해야 [합니다.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html#editing-a-template-page-policy-template-author-developer)

![AMP 페이지 정책 옵션](/help/assets/amp-policy.png)

* **AMP** 없음 - 페이지가 표준 HTML로만 제공됩니다.
* **AMP** - 페이지가 HTML과 AMP로 제공됩니다.
* **AMP만** - 페이지가 AMP로만 제공됩니다.

페이지의 AMP 설정은 개별 페이지의 [페이지 속성에서](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html) 재정의할 수도 있습니다.

![AMP 페이지 속성](/help/assets/amp-page-properties.png)

* **페이지 템플릿에서** 상속 - 페이지 템플릿의 정책에서 설정을 가져올 수 있는 기본값입니다.
* **AMP** 없음 - 페이지가 표준 HTML로만 제공됩니다.
* **AMP** - 페이지가 HTML과 AMP로 제공됩니다.
* **AMP만** - 페이지가 AMP로만 제공됩니다.

### CSS 요구 사항 {#css-requirements}

핵심 구성 요소에서 AMP를 사용하는 경우 AMP가 모든 [CSS를 최적화했을 뿐만 아니라 요소에 삽입해야](including-clientlibs.md#inlining) 한다는 점이 주요 차이점입니다 `<head>` .

이를 지원하기 위해 사용자 지정된 페이지 구성 요소가 사용됩니다. 이 구성 요소는 페이지에 있는 구성 요소에 대해 AMP별 CSS만 로드합니다.

자세한 요구 사항 및 기술 정보는 [GitHub 개발자 설명서를 참조하십시오.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)

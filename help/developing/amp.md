---
title: 핵심 구성 요소에 대한 AMP 지원
description: 핵심 구성 요소에 대한 AMP(Accelerated Mobile Pages) 지원
role: Developer, Admin
exl-id: 1fd9b6b5-0e4d-48c7-8faa-42e0d4a6bbd0
TQID: https://experienceleague.adobe.com/5v1tXLzHNRvAxy6-aJipN-ZYzsPJ1xFNc1hKmz73wic
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: c18d9e03-ac7d-4811-9c92-3e92ddc70ade
source-git-commit: 59ca85e0f0b99ba46bb2b85f383f1fefd2b1c5fd
workflow-type: tm+mt
source-wordcount: 680
ht-degree: 76%

---


# 핵심 구성 요소에 대한 AMP 지원 {#amp-support}

핵심 구성 요소 [릴리스 2.11.0](/help/versions.md)부터 [AMP(Accelerated Mobile Pages)](https://developers.google.com/amp)를 전폭 지원합니다.

이 문서는 AMP를 지원하는 방법과 사이트에서 활성화하는 방법에 대한 개요를 제공합니다. 단, 전체 기술 정보의 경우 [GitHub 개발자 설명서](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)를 참조하십시오.

## AMP란 무엇입니까? {#what-is-amp}

AMP(Accelerated Mobile Pages)는 Google에서 페이지를 최적화하기 위해 모바일 검색용으로 최초 설계한 오픈 소스 프레임워크입니다. 일반적으로 AMP 페이지는 표준 웹 페이지를 휠씬 더 빠르게 로드하여 보다 나은 모바일 경험을 제공합니다.

## 핵심 구성 요소의 AMP {#amp-in-core-components}

핵심 구성 요소에 대한 AMP 지원을 [전체 구성할 수 있습니다.](#enabling-amp) 표준 HTML 버전과 함께 AMP 버전의 페이지가 독점 제공되거나 전혀 제공되지 않을 수 있습니다.

핵심 구성 요소는 `amp`를 슬링 선택기로 사용하여 AMP 페이지를 렌더링합니다. 예를 들어 `example.html`는 일반 페이지를 렌더링하고 `example.amp.html`는 AMP 버전이 됩니다.

개별 프로젝트는 AMP 활용 여부를 결정할 수 있습니다. 실제로 AMP와 표준 HTML 페이지는 동시에 제공될 수 있기 때문에 프로젝트는 자체 특정 페이지에서만 AMP를 사용할 수 있습니다.

## 프로젝트에서 AMP 지원 시작하기 {#getting-started}

AMP 지원을 통해 다양한 유연성이 제공되지만 지원을 빠르게 시작하는 데에는 몇 가지 간단한 단계들이 필요합니다.

1. [핵심 구성 요소 설치](/help/get-started/using.md#download-and-install)
   * AEM as a Cloud Service 프로젝트의 경우 핵심 구성 요소는 기본적으로 사용할 수 있으며 추가 설치가 필요하지 않습니다.
   * 온-프레미스 및 AMS 프로젝트의 경우 [GitHub에서 핵심 구성 요소에 대한 최신 콘텐츠 패키지를 다운로드](https://github.com/adobe/aem-core-wcm-components/releases/latest)하여 AEM 환경에 설치할 수 있습니다.
   * 온-프레미스 또는 AMS 프로젝트에서 2.14.0 이전의 핵심 구성 요소 릴리스를 사용하는 경우 GitHub에 릴리스의 일부로 사용할 수 있는 AMP 확장 을 설치해야 합니다.
1. 구성 요소 `resourceSuperType`을(를) `core/wcm/extensions/amp/components/page/v1/page`(으)로 지정합니다.
   * 권장 모범 사례로 프로젝트에 [AEM Project Archetype](/help/developing/archetype/using.md)을(를) 사용하고 [AMP 지원을 활성화하는 옵션을 선택한 경우](https://github.com/adobe/aem-project-archetype/tree/develop) 자동으로 이 작업을 수행했습니다.
1. 템플릿 수준 또는 개별 페이지에서 [AMP 지원 활성화](#enabling-amp).
1. 필요에 따라 [인라인 CSS 배포](#css-requirements).

### 페이지의 AMP 활성화 {#enabling-amp}

페이지의 AMP를 활성화하려면 [페이지 정책](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html#editing-a-template-page-policy-template-author-developer)에서 **AMP 모드**&#x200B;를 선택해야 합니다.

![AMP 페이지 정책 옵션](/help/assets/amp-policy.png)

* **AMP 없음** - 페이지는 표준 HTML로만 제공됩니다.
* **페어링된 AMP** - 페이지는 AMP와 HTML로 제공됩니다.
* **AMP만 해당** - 페이지는 AMP로만 제공됩니다.

개별 페이지의 [페이지 속성](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html)에서 페이지의 AMP 설정이 재정의될 수도 있습니다.

![AMP 페이지 속성](/help/assets/amp-page-properties.png)

* **페이지 템플릿에서 상속** - 이 값은 페이지 템플릿의 정책에서 설정값을 얻을 수 있는 기본값입니다.
* **AMP 없음** - 페이지는 표준 HTML로만 제공됩니다.
* **페어링된 AMP** - 페이지는 AMP와 HTML로 제공됩니다.
* **AMP만 해당** - 페이지는 AMP로만 제공됩니다.

`resourceSuperType`이(가) AMP 지원을 위해 올바르게 설정된 경우에만 UI에 이러한 옵션이 표시됩니다. 기본 WKND 샘플 콘텐츠에는 `resourceSuperType` 설정이 없으므로 AMP에 대한 옵션이 UI에 표시되지 않습니다.

### CSS 요구 사항 {#css-requirements}

AMP를 핵심 구성 요소와 함께 사용하는 경우 주요 차이점은 AMP를 통해 [모든 CSS가 `<head>` 요소에서 인라인](including-clientlibs.md#inlining)되고 최적화될 수 있다는 것입니다.

이를 지원하기 위해 맞춤화된 페이지 구성 요소를 사용하여, 페이지에 표시된 구성 요소의 AMP별 CSS만 로드합니다.

>[!NOTE]
>
>AMP 디자인 제한으로 인해 Adobe는 AMP 버전의 페이지와 함께 반응형 그리드 사용을 지원하지 않습니다.

추가 요구 사항 및 기술에 대한 자세한 내용은 [GitHub 개발자 설명서를 참조하십시오.](https://github.com/adobe/aem-core-wcm-components/tree/master/extensions/amp)

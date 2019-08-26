---
title: 핵심 구성 요소 버전
seo-title: 핵심 구성 요소 버전
description: 핵심 구성 요소는 여러 버전의 동일한 핵심 구성 요소를 포함할 수 있는 릴리스로 게시됩니다. 이 문서에서는 릴리스 및 버전과 핵심 구성 요소 및 AEM 과의 호환성을 이해하는 방법에 대해 설명합니다.
seo-description: 핵심 구성 요소는 여러 버전의 동일한 핵심 구성 요소를 포함할 수 있는 릴리스로 게시됩니다. 이 문서에서는 릴리스 및 버전과 핵심 구성 요소 및 AEM 과의 호환성을 이해하는 방법에 대해 설명합니다.
uuid: A 916 A 923-8 C 5 E -456 A -84 B 5-B 52228 E 21434
contentOwner: 사용자
content-type: 참조
topic-tags: 소개
products: sg_ Experiencemanager/Corecomponents-new
discoiquuid: A 3 A 98 B 2 F -65 BF -4493-82 AD -01717938 FDBC
translation-type: tm+mt
source-git-commit: d1708bef323e2cdb071ebea5b15a1ebc6f683e9d

---


# 핵심 구성 요소 버전{#core-components-versions}

핵심 구성 요소의 현재 릴리스는 2.4.0 이며 AEM 6.5와 호환됩니다. 2019 년 5 월 릴리스 2.0.0에 대한 경미한 업데이트로 출시되었습니다. 릴리스 2.0.0는 기존 구성 요소의 v 2 업데이트와 함께 새 구성 요소를 도입했습니다.

자세한 내용은 이 문서의 섹션 [릴리스 내역 및 호환성을](#versions-and-releases) 참조하십시오.

핵심 구성 요소의 현재 릴리스를 표시하고 사용 예를 제공하는 [구성 요소 라이브러리를](http://opensource.adobe.com/aem-core-wcm-components/library.html)확인할 수도 있습니다.

## 버전 및 릴리스 {#versions-and-releases}

핵심 구성 요소는 Github를 통해 배포됩니다. 이를 통해 Adobe는 구성 요소에 기능을 보다 신속하게 추가할 수 있으며 AEM 릴리스 주기의 외부에 커뮤니티 의견을 입력할 수 있습니다.

핵심 구성 요소는 호환되는 AEM 버전과 함께 사용할 수 있습니다. 즉, 하나의 AEM 버전에서 핵심 구성 요소의 여러 버전 또는 릴리스를 지원할 수 있습니다. 이렇게 하면 특정 버전의 AEM에 연결되어 있는 이전의 기초 구성 요소보다 유연성이 더 높아집니다.

### 버전 {#versions}

핵심 구성 요소의 주요 반복은 **버전입니다**. 각 구성 요소에는 버전이 있습니다. 버전은 **v 1 및 v 2와 같이 0 이 아닌 양의 정수를 가진 v** 로 표시됩니다. 버전은 역호환이 아닌 변경 사항에만 증가하며, 이는 일반적으로 새로운 특징의 도입에 대한 대소문자입니다.

개발자와 관리자는 핵심 구성 요소 버전을 리소스 유형 경로 및 구현의 정규화된 Java 클래스 이름에서 숫자로 인식할 수 있습니다. 이 버전 번호는 Semantic 버전 관리 가이드라인에 의해 [정의된 주요 버전을 나타냅니다](https://semver.org/).

핵심 구성 요소 버전에 대한 자세한 내용은 핵심 구성 요소의 [개발자 설명서를 참조하십시오](guidelines.md).

### 릴리스 {#releases}

핵심 구성 요소는 **릴리스를 통해** 사용할 수 있으며 Github에서 사용할 수 있는 실제 게시된 결함을 [나타냅니다](https://github.com/adobe/aem-core-wcm-components/releases). 릴리스는 x. y. z 형식의 십진수 형식으로 표시되고 모든 핵심 구성 요소를 배달 패키지로 취합합니다.

* **주요 릴리스는** 새로운 버전의 기존 구성 요소와 완전히 새로운 구성 요소 및 표준 버그 수정을 제공합니다. 이것은 릴리스 번호의 x 구성 요소에서 증분으로 표시됩니다.

* **중요 릴리스는** 버그 수정과 함께 기존 버전의 구성 요소에 새로운 기능을 추가할 수 있습니다. 이것은 릴리스 번호의 Y 구성 요소에서 증분으로 표시됩니다.

* **보조 릴리스에는** 버그 수정만 포함됩니다. 이것은 릴리스 번호의 Z 구성 요소에서 증분으로 표시됩니다.

>[!NOTE]
>
>릴리스에는 동일한 구성 요소의 여러 버전이 포함될 수 있습니다.
>
>동일한 버전의 구성 요소가 여러 릴리스에서 나타날 수 있습니다.

## 릴리스 내역 및 호환성 {#release-history-and-compatibility}

핵심 구성 요소는 AEM 6.3에서 처음 릴리스되었으며, 지원되는 모든 AEM 버전과 호환되고 호환되도록 설계되었습니다. 이 때문에 구성 요소 릴리스에는 동일한 구성 요소의 여러 버전이 포함될 수 있습니다.

다음 표에서는 릴리스 버전과 함께 핵심 구성 요소 버전과 함께 핵심 구성 요소 버전과 호환성을 보여줍니다.

### 릴리스 내역 및 지원되는 AEM 버전 {#release-history-supported-aem-versions}

전체 릴리스 세부 사항과 함께 Github에서 사용할 [수 있는 다음 표는](https://github.com/adobe/aem-core-wcm-components/releases)핵심 구성 요소의 릴리스 및 AEM 릴리스 및 Java 버전과의 호환성에 대한 개요를 제공합니다.

| 릴리스 | 설명 | AEM 6.3 | AEM 6.4 | AEM 6.5 | Java |
|---|---|---|---|---|---|
| [2.5.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.5.0) | 이번 릴리스에서는 새로운 아코디언, 단추, 컨테이너 및 다운로드 구성 요소를 도입했습니다. | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | 8, 11 |
| [2.4.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.4.0) | 이 릴리스에서는 컨텐츠 조각 목록 구성 요소를 도입했습니다. | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | 8, 11 |
| [2.3.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.2) | 이 릴리스는 구성 요소 라이브러리에 대한 세부 사항에 중점을 두지만, separator 구성 요소에 대한 기능 개선 사항도 포함합니다. | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | 8 |
| [2.3.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.0) | 이 릴리스는 구성 요소 라이브러리와 새 분리 기호 구성 요소를 중점적으로 다루지만 이미지 구성 요소에 대한 향상된 일부 기능을 포함합니다. | 6.3.3.0+ | 6.4.2.0+ | - | 8 |
| [2.2.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.2) | 이 릴리스에는 주로 버그 수정에 중점을 두지만 회전식 구성 요소에 대한 향상된 기능 또한 포함되어 있습니다. | 6.3.3.0+ | 6.4.2.0+ | - | 8 |
| [2.2.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.0) | 추가된 탭 및 회전식 구성 요소, 향상된 이미지, 페이지 및 제목 구성 요소 및 향상된 추적 | 6.3.3.0+ | 6.4.2.0+ | - | 8 |
| [2.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.1.0) | 티저 구성 요소가 소개되었고, 향상된 이미지 구성 요소 및 많은 버그 수정 | 6.3.3.0+ | 6.4.2.0+ | - | 8 |
| [2.0.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.8) | 버그 수정 릴리스 | 6.3.2.0+ | 6.4.0.0+ | - | 8 |
| [2.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.6) | 백그라운드에서 향상된 추가 기능, 버그 수정, 이미지 뒤집기 지원 등 향상된 기능이 추가되었습니다. | 6.3.2.0+ | 6.4.0.0+ | - | 8 |
| [2.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.4) | 백그라운드에서 향상된 기능, 버그 수정, 이미지, 페이지 및 컨텐츠 조각 구성 요소에 대한 사소한 개선 사항 | 6.3.2.0+ | 6.4.0.0+ | - | 8 |
| [2.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.0) | 탐색, 언어 탐색 및 빠른 검색 구성 요소가 도입되었습니다. 스타일 시스템은 모든 구성 요소에 대해 구현되었습니다. | 6.3.2.0+ | 6.4.0.0+ | - | 8 |
| [1.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.1.0) | 모든 구성 요소에 JSON 내보내기 구현, 컨텐츠 조각 구성 요소 소개 | 6.3.1.0 | 6.4.0.0+ | - | 8 |
| [1.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.6) | 이미지 구성 요소에 대한 몇 가지 수정 사항 | 6.3.0.0+ | 6.4.0.0+ | - | 8 |
| [1.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.4) | 페이지 구성 요소 수정, 이미지 구성 요소, 다양한 전역 수정 사항 및 개선 사항 | 6.3.0.0+ | 6.4.0.0+ | - | 8 |
| [1.0.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.all-1.0.2) | 이미지 구성 요소의 애니메이션 GIF 이미지에 대한 수정 사항 | 6.3.0.0+ | 6.4.0.0+ | - | 7 |
| [1.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.0) | 핵심 구성 요소의 초기 릴리스 | 6.3.0.0+ | 6.4.0.0+ | - | 7 |

>[!NOTE]
>
>AEM와 마찬가지로, Adobe 에서는 개발자가 최신 수정 [버전과 기능을 사용할](https://github.com/adobe/aem-core-wcm-components/releases/latest) 수 있도록 AEM 버전과 호환되는 최신 버전의 핵심 구성 요소를 사용할 것을 권장합니다. 이 구성 요소는 최신 수정 사항 및 기능을 활용할 수 있습니다.

### 구성 요소 버전 및 릴리스 {#component-versions-and-releases}

다음 표에서는 핵심 구성 요소의 릴리스에서 어떤 구성 요소가 포함되어 있는지 자세히 설명합니다.

|  | 릴리스 1.0.0 - 1.0.6 | 릴리스 1.1.0 | 릴리스 2.0.0 - 2.0.8 | 릴리스 2.1.0 | 릴리스 2.2.-2.2.0 | 2.3.0 |
|---|---|---|---|---|---|---|
| **[page](page.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[제목](title.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[이미지](image.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[목록](list.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[브레드크럼](breadcrumb.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[소셜 미디어 공유](sharing.md)** | v1 | v1 | v1 | v1 | v1 | v1 |
| **[양식 컨테이너](form-container.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[양식 텍스트](form-text.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[양식 옵션](form-options.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[숨겨진 양식](form-hidden.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[양식 단추](form-button.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[컨텐츠 조각](content-fragment-component.md)** |  | 샌드박스 | v1 | v1 | v1 | v1 |
| **[탐색](navigation.md)** |  |  | v1 | v1 | v1 | v1 |
| **[언어 탐색](language-navigation.md)** |  |  | v1 | v1 | v1 | v1 |
| **[빠른 검색](quick-search.md)** |  |  | v1 | v1 | v1 | v1 |
| **[티저](teaser.md)** |  |  |  | v1 | v1 | v1 |
| **[탭](tabs.md)** |  |  |  |  | v1 | v1 |
| **[회전판](carousel.md)** |  |  |  |  | v1 | v1 |
| **[separator](separator.md)** |  |  |  |  |  | v1 |

## 설명서 {#documentation}

[핵심 구성](authoring.md) 요소로 작성하면 컨텐츠 작성자 및 템플릿 작성자에게 노출되는 핵심 구성 요소 및 기능의 사용에 대해 설명합니다. 각 구성 요소는 자세히 설명되어 있습니다.

[구성 요소 라이브러리는](http://opensource.adobe.com/aem-core-wcm-components/library.html) 사용 방법을 보여주는 최신 버전의 핵심 구성 요소입니다.

[핵심 구성 요소](developing.md) 개발 시 핵심 구성 요소의 기술적 기능, 프로젝트에서 이러한 구성 요소를 사용하는 방법, 사용자 지정 방법 및 우수 사례를 설명합니다.

[핵심 구성 요소 소개에서는](introduction.md) 버전, 사용 사례 및 지원의 핵심 구성 요소 호환성에 대한 개요를 제공합니다.

---
title: 핵심 구성 요소 소개
description: '핵심 구성 요소는 최신 기술과 우수 사례를 기반으로 구축된 강력하고 확장 가능한 기본 구성 요소를 제공하기 위해 도입되었습니다. '
translation-type: tm+mt
source-git-commit: 5439f90faef28c72367419bb7429a3a880b65229

---


# 핵심 구성 요소 소개{#core-components-introduction}

Adobe Experience Manager에서 구성 요소는 작성 중인 페이지의 콘텐츠를 구성하는 구조적 요소입니다. 구성 요소는 항상 AEM 경험의 기본 요소로, 이를 통해 작성자는 간단하지만 강력한 페이지를 만들 수 있고 개발자는 유연하고 확장 가능한 구성 요소를 개발할 수 있습니다.

핵심 구성 요소는 최신 기술과 모범 사례를 기반으로 하여 구축되었고 액세스 가능성 지침을 준수하고 WCAG 2.0 AA 표준과 호환되는 강력하고 확장 가능한 기본 구성 요소를 제공하기 위해 도입되었습니다. 핵심 구성 요소를 통해 페이지를 보다 유연하게 작성하고 사용자 지정할 수 있으며, 핵심 구성 요소를 확장하여 개발자에게 사용자 지정 기능을 간단하게 제공할 수 있습니다.

## 핵심 구성 요소 시도

핵심 구성 요소를 바로 사용해 보려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library)로 이동하십시오. 구성 요소 라이브러리는 대부분의 핵심 구성 요소의 현재 버전을 온라인으로 표시한 것으로, 구성 요소의 변형과 상호 작용하고 샘플 HTML 및 JSON 출력을 볼 수 있습니다.

WKND [자습서에서는](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/getting-started.html) 핵심 구성 요소를 사용하는 방법도 설명합니다.

## 핵심 구성 요소 - 핵심 기능 {#core-components-core-features}

핵심 구성 요소의 기능은 다음과 같습니다.

|  |  |
|--- |--- |
| 사전 구성 가능 | 템플릿은 페이지 작성자가 핵심 구성 요소 사용 방법을 정의할 수 있습니다. |
| 유연성 | 작성자가 대부분의 콘텐츠 종류를 만들 수 있습니다. |
| 사용하기 쉬움 | 작성자가 콘텐츠를 효율적으로 작성하고 관리할 수 있습니다. |
| 프로덕션 준비 | 바로 사용 가능합니다! 강력하고 충분히 테스트되어 원활하게 수행됩니다. |
| 액세스 가능 | WCAG 2.0 표준을 준수하고 ARIA 레이블을 제공하며 키보드 탐색을 지원합니다. |
| 스타일을 쉽게 지정 | 이 구성 요소는 스타일 시스템을 구현하고 마크업이 BEM CSS 명명을 따릅니다. |
| SEO에 친숙함 | HTML 출력은 의미가 있으며 schema.org 마이크로 데이터 주석을 제공합니다. |
| PWA/SPA/앱 사용 가능 | 간소화된 JSON 출력을 클라이언트측 렌더링에 사용할 수도 있습니다. |
| 확장 가능 | 사용자 지정 요구 사항을 다루지만 처음부터 시작하지 않도록 모든 것을 확장할 수 있습니다. |
| 공개 소스 | 필요한 어떤 기능이 없다면 GitHub(Apache 라이센스)에서 개선해 주십시오. |
| 버전이 지정됨 | 핵심 구성 요소는 영향을 줄 수 있는 요소를 개선할 때 사이트를 손상시키지 않습니다. |
| [지역화됨](localization.md) | 스마트 참조 해상도를 사용하면 특정 구성 요소에서 해당 지역화된 컨텐츠를 자동으로 찾아 렌더링할 수 있습니다 |

## 사용 가능한 구성 요소 {#available-components}

핵심 구성 요소의 현재 버전은 다음 구성 요소 기능이 있습니다.

* [어코디언](accordion.md)
* [탐색 표시](breadcrumb.md)
* [단추](button.md)
* [컨테이너](container.md)
* [회전판](carousel.md)
* [콘텐츠 조각](content-fragment-component.md)
* [콘텐츠 조각 목록](content-fragment-list.md)
* [다운로드](download.md)
* [포함](embed.md)
* [경험 조각](experience-fragment.md)
* [양식 단추](form-button.md)
* [양식 컨테이너](form-container.md)
* [숨겨진 양식](form-hidden.md)
* [양식 옵션](form-options.md)
* [양식 텍스트](form-text.md)
* [이미지](image.md)
* [언어 탐색](language-navigation.md)
* [목록](list.md)
* [탐색](navigation.md)
* [페이지](page.md)
* [빠른 검색](quick-search.md)
* [분리자](separator.md)
* [소셜 미디어 공유](sharing.md)
* [탭](tabs.md)
* [텍스트](text.md)
* [제목](title.md)

>[!NOTE]
>
>작성자는 핵심 구성 요소를 즉시 사용할 수 없습니다. [개발 팀에서 먼저 핵심 구성 요소를 환경에 통합해야 합니다](using.md). Once integrated, they may be made available and pre-configured via the [template editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

>[!CAUTION]
>
>개별 핵심 구성 요소의 일부 버전은 특정 AEM 버전과 호환될 수 있습니다.
>
>특정 구성 요소에 대한 개별 도움말 페이지(이전 목록에 연결됨)에서 호환성 정보를 참조하거나 [핵심 구성 요소 버전](versions.md) 문서에서 자세한 내용을 참조하십시오.

## 핵심 구성 요소를 사용해야 하는 경우 {#when-to-use-core-components}

핵심 구성 요소가 새로워졌고 여러 이점을 제공하므로 새 AEM 프로젝트에서 이러한 구성 요소를 사용하는 것이 좋습니다. 기존 프로젝트의 경우 마이그레이션은 리브랜딩 또는 전체 리팩터링 등 대규모 프로젝트 작업에 포함되었습니다.

특정 사용 권장 사항에 대해서는 [핵심 구성 요소를 사용해야 하는 경우](developing.md)([핵심 구성 요소 개발](developing.md) 문서)를 참조하십시오.

## Gems 세션 개요 {#gems-session-overview}

핵심 구성 요소, 구성 요소가 제공하는 기능 및 AEM에서 이러한 구성 요소를 활용하는 방법에 대한 소개는 AEM Gems 세션 [AEM 핵심 구성 요소](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)

[Adobe Experience Manager의](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/aem-index.html) Gems는 Adobe 전문가가 전달하는 일련의 기술 심층 정보입니다. 이 시리즈는 제품 설명서 및 기타 모든 기술 채널을 보완했기 때문에 개발자가 특정 주제를 선택하여 자세히 알아볼 수 있습니다.

## 핵심 구성 요소를 사용한 개발 {#developing-core-components}

핵심 구성 요소는 간단한 스타일링에서 고급 기능 재사용에 이르기까지 사용자 정의가 간편한 여러 패턴을 구현하는 강력하고 확장 가능한 기본 구성 요소를 제공합니다. 자세한 내용은 [핵심 구성 요소 개발 설명서를](developing.md) 참조하십시오.

WKND 자습서를 따라 핵심 구성 요소를 사용하여 AEM [사이트 개발을 시작하십시오.](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/getting-started.html)

AEM Project Tranype을 활용하는 자체 AEM 프로젝트를 [시작하는](overview.md) 것을 잊지 마십시오.

## 핵심 구성 요소 지원 {#core-components-support}

핵심 구성 요소는 AEM의 필수적인 부분으로, 빠른 시작의 일부로 전달된 것처럼 동일한 이용 약관에 따라 지원됩니다.

다른 제품 기능과 마찬가지로 수명 종료에 대한 일반적인 규칙은 다음과 같습니다.

* 구성 요소는 제거되기 전에 먼저 사용을 중단한다고 발표했습니다.
* 공지 후 가장 빠른 시일 내에 AEM 릴리스에서 제거됩니다.

따라서 지원이 종료되기 전에 고객에게 구성 요소의 새 버전으로 이동할 수 있는 릴리스 주기를 1개 이상 제공합니다.

각 구성 요소의 버전은 지원되는 AEM 버전을 명확하게 설명합니다. AEM 버전에 대한 지원이 중단되면 해당 버전의 AEM에 대한 핵심 구성 요소에 대한 지원도 중단됩니다.

구성 요소 사용자 정의에 대한 자세한 내용은 관련 핵심 구성 요소 버전의 [핵심 구성 요소 사용자 정의](customizing.md)를 참조하십시오.

## 기초 구성 요소 지원 {#foundation-component-support}

기초 구성 요소는 많은 버전에 대해 프로젝트 개발 기준 역할을 했기 때문에 가까운 미래에도 계속 지원됩니다.

However, Adobe&#39;s development emphasis has shifted to the Core Components and new features will be added to them, whereas [nearly all Foundation Components have been deprecated with AEM 6.5](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/default-components-foundation.html) and only bug fixes will be made to the Foundation Components going forward.

---
title: 핵심 구성 요소 개발
seo-title: 핵심 구성 요소 개발
description: 핵심 구성 요소는 풍부한 기능, 지속적인 전달, 구성 요소 버전 관리, 최신 구현, 강력한 마크업 및 컨텐츠 JSON 내보내기를 제공하는 강력하고 확장 가능한 기본 구성 요소를 제공합니다.
seo-description: 핵심 구성 요소는 풍부한 기능, 지속적인 전달, 구성 요소 버전 관리, 최신 구현, 강력한 마크업 및 컨텐츠 JSON 내보내기를 제공하는 강력하고 확장 가능한 기본 구성 요소를 제공합니다.
uuid: 68569da2-9bc8-4e20-9a71-e5816ace51ce
contentOwner: 사용자
content-type: 참조
topic-tags: 개발
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: 157a2ec3-9fca-4fad-977a-d93013eeb218
translation-type: tm+mt
source-git-commit: 683b4f4705c226275439a408423cbf1b23bea66f

---


# 핵심 구성 요소 개발{#developing-core-components}

## 개요 {#overview}

핵심 구성 요소는 강력하고 확장 가능한 기본 구성 요소를 제공하며, 주요 내용은 다음과 같습니다.

* 다양한 기능
   * [다양한 사용 사례를 수용할 수 있는 유연한 구성 옵션](authoring.md)
   * [페이지 작성자가 사용할 수 있는 기능을 정의하는 사전 구성 가능한 기능](authoring.md#pre-configuring-core-components)
* 지속적인 전달
   * 잦은 증분 기능 개선
   * 개발자 커뮤니티에서 피드백을 제공하고 [증여할](https://github.com/adobe/aem-core-wcm-components) 수 있는 GitHub의 소스 코드 사용 가능
   * AEM 업그레이드와 독립적으로 구성 요소 업그레이드를 위한 [별도로 릴리스된 컨텐츠 패키지를](https://github.com/adobe/aem-core-wcm-components/releases) 통한 설치
* [구성 요소 버전 관리](guidelines.md#component-versioning)
   * [한 버전](#upgrade-of-core-components)내의 호환성을 보장하면서 구성 요소가 진화하도록 허용
   * 한 구성 요소의 여러 버전이 동일한 환경에서 함께 사용 가능
* 최신 구현
   * HTML 템플릿 [언어](https://helpx.adobe.com/experience-manager/htl/using/overview.html) (HTL)에 정의된 마크업
   * Sling Models를 사용하여 구현된 [컨텐츠 모델 로직](https://sling.apache.org/documentation/bundles/models.html)
* 마크업
   * 릴리스 [2.0.0의 BEM](https://getbem.com/) (블록 요소 수정자) 표기법
      * 이전 릴리스 이후 [Bootstrap](https://getbootstrap.com/css/) 이름 지정 규칙
   * Built around [accessibility guidelines](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html)
   * 반응형 및 모바일 사이트에 사용 가능
* 헤드리스 CMS 사용 사례를 위한 컨텐츠 모델을 JSON으로 일련화할 수 있는 기능
* 액세스 가능
   * WCAG [2.0 AA 표준 준수](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html)

>[!CAUTION]
>
>핵심 구성 요소는 AEM 6.3 이상 및 Java 8이 필요하며 [편집 가능한 템플릿을 사용해야 합니다](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)
>
>핵심 구성 요소는 클래식 UI와 정적 템플릿에서는 작동하지 않습니다.

## Gems 세션 개요 {#gems-session-overview}

핵심 구성 요소, 구성 요소가 제공하는 기능 및 AEM에서 이러한 구성 요소를 활용하는 방법에 대한 소개는 AEM Gems 세션 [AEM 핵심 구성 요소](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)

[Adobe Experience Manager의](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/aem-index.html) Gems는 Adobe 전문가가 전달하는 일련의 기술 심층 정보입니다. 이 시리즈는 제품 설명서 및 기타 모든 기술 채널을 보완했기 때문에 개발자가 특정 주제를 선택하여 자세히 알아볼 수 있습니다.

## WKND 개발자 자습서 {#wknd-developer-tutorial}

Get started developing AEM Sites with Core Components by following [this step-by-step tutorial.](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/getting-started.html)

## AEM 프로젝트 원형 {#aem-project-archetype}

[AEM Project Tranype](overview.md) 은 권장 프록시 패턴을 사용하는 핵심 구성 요소의 로직과 적절한 구현을 위해 SlingModels가 포함된 사용자 지정 HTL 구성 요소의 도움말 예제를 비롯하여 최소한의 Adobe Experience Manager 프로젝트를 고유한 프로젝트의 시작점으로 만듭니다.

## GitHub를 통해 제공 {#delivered-over-github}

핵심 구성 요소는 GitHub에서 개발되어 전달됩니다.

GITHUB에 대한 코드

GitHub에서 이 페이지의 코드를 찾을 수 있습니다

* [GitHub에서 aem-core-wcm-components 프로젝트 열기](https://github.com/adobe/aem-core-wcm-components)
* 프로젝트를 ZIP [파일로 다운로드](https://github.com/adobe/aem-core-wcm-components/archive/master.zip)

프로젝트에서 [핵심 구성 요소](using.md) 사용을 시작하는 방법에 대한 자세한 내용은 핵심 구성 요소 사용 설명서 페이지를 참조하십시오.

GitHub에 핵심 구성 요소를 추가하면 자주 업데이트되고 AEM 개발자 커뮤니티의 의견을 들을 수 있습니다. 또한 사용자 지정 구성 요소를 빌드할 때 고객과 파트너가 유사한 패턴을 따를 수 있도록 도와줍니다.

>[!NOTE]
>
>핵심 구성 요소에 대한 최신 변경 사항을 최신 상태로 유지하려면 GitHub에서 [핵심 구성 요소 저장소를](https://github.com/adobe/aem-core-wcm-components) 볼 수 있습니다.

## 구성 요소 라이브러리

핵심 구성 [요소의](http://opensource.adobe.com/aem-core-wcm-components/library.html)현재 릴리스를 보여주고 사용 예를 제공하는 구성 요소 라이브러리를 확인하십시오.

### 샘플 컨텐츠 실행 모드 {#sample-content-run-mode}

핵심 구성 요소는 We.Retail 참조 사이트에서 [사용하기 때문에 샘플 컨텐츠가 있으면 빠른](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html) 시작에서볼 수 있습니다. 그러나 프로덕션( `nosamplecontent` 런타임 모드에서 샘플 컨텐츠가 활성화되지 않은 상태로)에서 실행할 때 핵심 구성 요소는 더 이상 표시되지 않으며 개발 및/또는 작업 팀에서 AEM 인스턴스에 설치해야 합니다.

>[!NOTE]
>
>프로덕션 환경에서는 항상 `nosamplecontent` 실행 모드에서 빠른 시작을 실행합니다. 런타임 모드에서 핵심 구성 요소를 사용하려면 핵심 구성 요소 사용 `nosamplecontent` 설명서 [](using.md) 페이지의 지침을 따르십시오.

## 기술 기능 {#technical-capabilities}

다음 표는 핵심 구성 요소와 기본 구성 요소 간의 차이점을 대략적으로 설명합니다.

작성 기능과 사전 구성 가능한 옵션에 대한 자세한 [내용은 작성 페이지를 참조하십시오](authoring.md).

| **기능** | **핵심 구성 요소** | **기본 구성 요소** |
|-----|---|---|
| 논리 구현 | Sling 모델 [주석이 있는 Java POJO](https://sling.apache.org/documentation/bundles/models.html) | JSP 코드 |
| 마크업 정의 | [HTML 템플릿 언어](https://helpx.adobe.com/experience-manager/htl/user-guide.html) (HTL) 구문 | JSP 코드 |
| XSS 기밀 정보 가리기 | HTL로 자동화 | 대부분 수동 |
| CSS 클래스 이름 지정 | 블록 요소 수정자( [BEM](https://getbem.com/) ) 표기법을 기반으로 하는 표준 이름 지정 규칙(릴리스 2.0.0 기준) | 사용자 지정 구성표 |
| 대화 상자 정의 | [Coral 3](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/reference-materials/coral-ui/coralui3/index.html) | Coral 2 + 클래식 UI |
| JSON 출력 | [Sling Models Exporter with Jackson serialization](https://sling.apache.org/documentation/bundles/models.html#exporter-framework-since-130) | 기본 Sling 서블릿 |
| 버전 관리 | [모델 및 HTL의 경우](guidelines.md) | 없음 |
| 테스트 | 단위 테스트 + 통합 테스트 | 통합 테스트 |
| 배달 | [공개 GitHub를 통해](https://github.com/adobe/aem-core-wcm-components) | 빠른 시작을 통해 |
| 라이센스 | [Apache License](https://www.apache.org/licenses/LICENSE-2.0) | Adobe 독점 제품 |
| 기여도 | 가져오기 요청 사용 | 불가능 |
| 액세스 가능성 | WCAG 2. [0 AA 표준 준수](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html) | WCAG 2.0 [AA 표준을 일부 준수하는 경우에만](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html) |

## 구성 요소 목록 {#component-list}

다음 표에는 사용 가능한 핵심 구성 요소(API에 연결)가 나열되며, 이 구성 요소가 대체할 기본 구성 요소를 나타냅니다.

| 핵심 구성 요소 | 설명 | 기본 구성 요소 대체 |
|---|---|---|
| [페이지](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/page/v2/page) | 템플릿 편집기를 사용한 반응형 페이지 | `/libs/foundation/components/page /libs/wcm/foundation/components/page` |
| [탐색 표시](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb) | 페이지 계층 구조 탐색 | `/libs/foundation/components/breadcrumb` |
| [제목](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/title/v2/title) | H1-H6 제목 | `/libs/foundation/components/title /libs/wcm/foundation/components/title` |
| [텍스트](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v2/text) | 리치 텍스트 | `/libs/foundation/components/text /libs/foundation/components/table /libs/wcm/foundation/components/text` |
| [이미지](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/image/v2/image) | 최적의 변환 크기의 지능적이고 레이지 로딩 | `/libs/foundation/components/image /libs/foundation/components/adaptiveimage /libs/foundation/components/logo /libs/foundation/components/mobileimage  /libs/foundation/components/mobilelogo /libs/wcm/foundation/components/image` |
| [목록](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/list/v2/list) | 페이지 목록 | `/libs/foundation/components/list /libs/foundation/components/mobilelist /libs/wcm/foundation/components/list` |
| [소셜 미디어 공유](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/sharing/v1/sharing) | Facebook 및 Pinterest 공유 위젯 | `-` |
| [양식 컨테이너](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/container/v2/container) | 반응형 양식 단락 시스템 | `/libs/foundation/components/form/start /libs/foundation/components/form/end` |
| [양식 텍스트](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v2/text) | 텍스트 입력 필드 | `/libs/foundation/components/form/text /libs/foundation/components/form/password` |
| [양식 옵션](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/options/v2/options) | 여러 옵션 입력 필드 | `/libs/foundation/components/form/checkbox /libs/foundation/components/form/radio /libs/foundation/components/form/dropdown` |
| [숨겨진 양식](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/hidden/v2/hidden) | 숨겨진 입력 필드 | `/libs/foundation/components/form/hidden` |
| [양식 단추](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/button/v2/button) | 전송 또는 사용자 정의 단추 | `/libs/foundation/components/form/submit` |
| [탐색](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/navigation/v1/navigation) | 중첩된 페이지 계층 구조를 나열하는 사이트 탐색 구성 요소 | `/libs/foundation/components/topnav /libs/foundation/components/mobiletopnav` |
| [언어 탐색](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/languagenavigation/v1/languagenavigation) | 글로벌 언어 구조를 나열하는 언어 및 국가 전환기 | `-` |
| [빠른 검색](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/search/v1/search) | 드롭다운 메뉴에서 결과를 즉석 제안으로 표시하는 검색 구성 요소 | `/libs/foundation/components/search` |
| [티저](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/teaser/v1/teaser) | 컨텐츠 작성자는 이미지, 제목 또는 리치 텍스트를 사용하여 추가 컨텐츠에 Teaser를 쉽게 만들고 추가 컨텐츠 또는 기타 작업에 연결할 수 있습니다 | `-` |
| [탭](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/tabs/v1/tabs) | 컨텐츠 작성자가 여러 탭 내에서 페이지 컨텐츠를 구성할 수 있도록 허용 | `-` |
| [회전판](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/carousel/v1/carousel) | 컨텐츠 작성자가 슬라이드 회전 슬라이드로 컨텐츠를 구성할 수 있습니다. | `/libs/foundation/components/carousel` |
| [컨텐츠 관리](https://github.com/adobe/aem-core-wcm-components/tree/master/extension/contentfragment/content/src/content/jcr_root/apps/core/wcm/extension/components/contentfragment/v1/contentfragment) | 컨텐츠 조각을 표시할 수 있습니다. | `-` |
| [콘텐츠 관리 목록](https://github.com/adobe/aem-core-wcm-components/tree/master/extension/contentfragment/content/src/content/jcr_root/apps/core/wcm/extension/components/contentfragmentlist/v1/contentfragmentlist) | 컨텐츠 조각 목록을 표시할 수 있습니다. | `-` |
| [분리자](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/separator/v1/separator) | 페이지에서 컨텐츠 분리 | `-` |
| [어코디언](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/accordion/v1/accordion) | 콘텐츠 패널을 축소 가능한 아코디언 구성 | `-` |
| [컨테이너](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/container/v1/container) | 컨테이너 내 구성 요소 구성 | `-` |
| [단추](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/button/v1/button) | 페이지에서 단추 만들기 | `-` |
| [다운로드](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/download/v1/download) | 페이지에 다운로드 가능한 자산 추가 | `-` |
| [경험 조각](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/experience-fragment/v1/experience-fragment) | 페이지에 경험 조각 추가 | `/libs/cq/experience-fragments/editor/components/experiencefragment` |
| [포함](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed) | 페이지 내에 외부 리소스 포함 | - |

### 예정된 구성 요소 {#upcoming-components}

예정된 핵심 구성 요소 로드맵에 대한 개요는 GitHub의 [프로젝트 위키를 참조하십시오](https://github.com/adobe/aem-core-wcm-components/wiki/home).

## 핵심 구성 요소 업그레이드 {#upgrade-of-core-components}

버전 관리 구성 요소의 이점 중 하나는 새 AEM 버전으로의 마이그레이션을 새 구성 요소 버전으로의 마이그레이션으로부터 분리할 수 있다는 것입니다. 또한 새 구성 요소 버전을 사용할 수 있는 경우 각 구성 요소를 새 버전으로 개별적으로 마이그레이션할 수 있습니다.

새 AEM 버전으로 마이그레이션은 핵심 구성 요소가 작동하는 방식에 영향을 주지 않습니다. 단, 해당 버전은 마이그레이션되는 새 AEM 버전도 지원합니다. 핵심 구성 요소에 대한 사용자 지정은 [더 이상 사용되지 않거나 제거된](https://helpx.adobe.com/experience-manager/6-5/release-notes/deprecated-removed-features.html)API를 사용하지 않는 한 영향을 받지 않아야 합니다.

핵심 구성 요소의 새 버전으로 마이그레이션해도 구성 요소의 작동 방식에는 영향을 주지 않지만, 기본 동작을 원하지 않는 경우 템플릿 편집기의 일부 구성이 필요할 수 있는 새로운 기능이 페이지 작성자에게 소개될 수 있습니다. 하지만 사용자 지정을 수정해야 할 수도 있습니다. 자세한 내용은 핵심 구성 요소 [사용자 지정 페이지를 참조하십시오](customizing.md#upgrade-compatibility-of-customizations) .

## When to Use the Core Components? {#when-to-use-the-core-components}

핵심 구성 요소가 새로워졌고 여러 이점을 제공하므로 새 AEM 프로젝트에서 이러한 구성 요소를 사용하는 것이 좋습니다. 기존 프로젝트의 경우 마이그레이션은 리브랜딩 또는 전체 리팩터링 등 대규모 프로젝트 작업에 포함되었습니다.

따라서 Adobe는 다음과 같은 권장 사항을 제공합니다.

* **새**&#x200B;프로젝트새 프로젝트는 항상 핵심 구성 요소를 사용하려고 시도합니다. 핵심 구성 요소를 프로젝트 요구 사항을 충족하기 위해 직접 또는 [확장할](customizing.md) 수 없는 경우 핵심 구성 요소에 지정된 구성 요소 아키텍처 다음에 사용자 지정 구성 요소를 만듭니다. 달리 가능하지 않은 경우를 제외하고는 [기본 구성 요소를](developing.md)사용하지 마십시오.
* **사이트나 구성**&#x200B;요소 리팩토링이 계획되지 않은 경우 기존 프로젝트 권장 사항은 [기초 구성 요소를](developing.md)계속 사용합니다.\
   대부분의 기존 프로젝트에서 매우 널리 사용되고 있으므로 기본 구성 요소는 계속 [지원됩니다.](developing.md)
* **새 사용자 지정 구성**&#x200B;요소기존 [핵심 구성 요소를 사용자](customizing.md)지정할 수 있는지 여부를 평가합니다.\
   그렇지 않은 경우, 권장 사항은 구성 요소 지침에 따라 새 사용자 지정 구성 요소를 [만드는 것입니다](guidelines.md).
* **기존 사용자**&#x200B;지정 구성 요소구성 요소가 예상대로 작동하면 구성 요소를 그대로 유지합니다.\
   그렇지 않은 경우 위의 "새 사용자 지정 구성 요소"를 참조하십시오.

## 핵심 구성 요소로 마이그레이션

모든 새 프로젝트는 핵심 구성 요소를 사용하여 구현해야 합니다. 그러나 기존 프로젝트에는 일반적으로 Foundation 구성 요소의 광범위한 구현이 있습니다.

기존 프로젝트(예: 리브랜딩 또는 전체 리팩토링)에서 더 많은 노력을 기울이면 종종 핵심 구성 요소로 마이그레이션할 수 있습니다. Adobe는 이러한 마이그레이션을 촉진하기 위해 핵심 구성 요소 및 최신 AEM 기술의 채택을 장려하는 여러 마이그레이션 도구를 제공했습니다.

[AEM 현대화 도구를](http://opensource.adobe.com/aem-modernize-tools/) 사용하여 다음을 쉽게 변환할 수 있습니다.

* 정적 템플릿을 편집 가능한 템플릿으로 변환
* 정책으로 구성 디자인
* 기본 구성 요소를 핵심 구성 요소로
* 클래식 UI에서 터치 지원 UI

이러한 도구의 사용에 대한 자세한 내용은 설명서를 [참조하십시오](http://opensource.adobe.com/aem-modernize-tools/).

>[!NOTE]
>
>AEM 현대화 도구는 커뮤니티 활동이며 Adobe에서 지원하거나 보증하지 않습니다.

## 핵심 구성 요소 지원 {#core-component-support}

핵심 구성 요소는 AEM의 필수적인 부분으로, 빠른 시작의 일부로 전달된 것처럼 동일한 이용 약관에 따라 지원됩니다.

다른 AEM 제품 기능과 마찬가지로 일반 규칙은 다음과 같습니다.구성 요소는 먼저 더 이상 사용되지 않는다고 발표되고 다음 AEM 릴리스에 대해 가장 빨리 제거됩니다. 따라서 고객이 지원을 중단하기 전에 하나 이상의 릴리스 주기를 구성 요소의 새 버전으로 전환할 수 있습니다.

각 구성 요소의 버전은 지원되는 AEM 버전을 명확하게 설명합니다. AEM 버전에 대한 지원이 중단되면 해당 버전의 AEM에 대한 핵심 구성 요소에 대한 지원도 중단됩니다.

구성 요소 사용자 지정 지원에 대한 자세한 내용은 핵심 구성 요소 [사용자 지정 페이지를](customizing.md) 참조하십시오.

## 기초 구성 요소 지원 {#foundation-component-support}

기본 구성 요소는 많은 AEM 버전에 걸쳐 많은 프로젝트 개발의 기반으로 사용되기 때문에 앞으로도 계속 지원될 것입니다.

However, Adobe's development emphasis has shifted to the Core Components and new features will be added to them, whereas [nearly all Foundation Components have been deprecated with AEM 6.5](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-foundation.html) and only bug fixes will be made to the Foundation Components going forward.

**다음 참조:**

* [핵심 구성 요소](using.md) 사용 - 프로젝트에서 핵심 구성 요소를 사용하여 바로 시작할 수 있습니다.
* [구성 요소](guidelines.md) 지침 - 핵심 구성 요소의 구현 패턴을 학습합니다.

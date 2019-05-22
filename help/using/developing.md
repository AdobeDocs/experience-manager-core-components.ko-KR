---
title: 핵심 구성 요소 개발
seo-title: 핵심 구성 요소 개발
description: 핵심 구성 요소는 기능이 풍부한 기능, 지속적인 전달, 구성 요소 버전 관리, 최신 구현, Lean Markup 및 JSON 내보내기를 제공하는 강력하고 확장 가능한 기본 구성 요소를 제공합니다.
seo-description: 핵심 구성 요소는 기능이 풍부한 기능, 지속적인 전달, 구성 요소 버전 관리, 최신 구현, Lean Markup 및 JSON 내보내기를 제공하는 강력하고 확장 가능한 기본 구성 요소를 제공합니다.
uuid: 68569 da 2-9 bc 8-4 e 20-9 a 71-e 5816 ace 51 ce
contentOwner: 사용자
content-type: 참조
topic-tags: developing
products: sg_ Experiencemanager/Corecomponents-new
discoiquuid: 157 A 2 EC 3-9 FCA -4 FAD -977 A-D 93013 EEB 218
translation-type: tm+mt
source-git-commit: 632d6abb1f13667cc0457152268d50af3bfabfc4

---


# 핵심 구성 요소 개발{#developing-core-components}

## 개요 {#overview}

핵심 구성 요소는 강력하고 확장 가능한 기본 구성 요소를 제공하며 다음과 같습니다.

* 기능이 풍부한 기능
   * [Flexible configuration options](authoring.md) to accommodate many use cases
   * [페이지 작성자가 사용할 수 있는 기능을 정의하기](authoring.md#pre-configuring-core-components) 위한 사전 구성 가능 기능
* 지속적인 전달
   * 향상된 증분 기능
   * 개발자 커뮤니티에서 [피드백 및 Contribute를 제공할 수](https://github.com/adobe/aem-core-wcm-components) 있도록 Github에서 소스 코드를 사용할 수 있음
   * 별도로 릴리스된 [컨텐츠 패키지를](https://github.com/adobe/aem-core-wcm-components/releases) 통해 설치해서 AEM 업그레이드와는 독립적으로 구성 요소 업그레이드 수행
* [구성 요소 버전 관리](guidelines.md#component-versioning)
   * [구성 요소 간에 호환성이 보장되는 버전](#upgrade-of-core-components)내 호환성 보장
   * 한 구성 요소의 여러 버전이 동일한 환경에서 공존하도록 허용
* 최신 구현
   * HTML 템플릿 언어 (HTL) 로 [정의된](https://helpx.adobe.com/experience-manager/htl/using/overview.html) 마크업
   * Sling 모델로 구현된 컨텐츠 [모델 로직](https://sling.apache.org/documentation/bundles/models.html)
* Lean Markup
   * 릴리스 2.0.0 부터 BEM ( [Block Element Modifier](https://getbem.com/) ) 표기법
      * 이전 릴리스 [Bootstrap](https://getbootstrap.com/css/) 이름 지정 규칙 준수
   * 접근성 가이드라인을 중심으로 [구축](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html)
   * 반응형 및 모바일 사이트에 사용 가능
* 헤드리스 CMS 사용 사례를 위한 컨텐츠 모델로 JSON 직렬화 기능
* 액세스 가능
   * [WCAG 2.0 AA 표준을 준수하는 표준](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html)

>[!CAUTION]
>
>핵심 구성 요소는 AEM 6.3 이상과 Java 8를 필요로 하며 [편집 가능한 템플릿을 사용해야 합니다.](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)
>
>핵심 구성 요소는 클래식 UI 또는 정적 템플릿과 함께 작동하지 않습니다.

## Gems 세션 개요 {#gems-session-overview}

핵심 구성 요소, 고객이 제공하는 기능 및 AEM에서 사용하는 방법에 대한 소개를 보려면 AEM GEMS 세션 [AEM 코어 구성 요소를 확인하십시오.](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)

[Adobe Experience Manager](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/aem-index.html) 의 Gems는 Adobe 전문가가 제공하는 일련의 기술 심층 선봉입니다. 이 시리즈는 제품 설명서와 기타 모든 기술 채널을 보완해 주므로 개발자는 특정 주제를 자세히 살펴볼 수 있습니다.

## WKND 개발자 자습서 {#wknd-developer-tutorial}

이 단계별 튜토리얼을 따라 [핵심 구성 요소를 사용하여 AEM 사이트를 개발하는 방법을 살펴보십시오.](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/getting-started.html)

## Github를 통해 제공 {#delivered-over-github}

핵심 구성 요소는 Github를 통해 개발되고 제공됩니다.

Github의 코드

Github에서 이 페이지의 코드를 찾을 수 있습니다.

* [Github에서 AEM-core-wcm-components 프로젝트 열기](https://github.com/adobe/aem-core-wcm-components)
* 프로젝트를 ZIP 파일로 [다운로드](https://github.com/adobe/aem-core-wcm-components/archive/master.zip)

프로젝트에서 [사용할 수 있는 방법은 핵심 구성 요소](using.md) 설명서 사용 페이지를 참조하십시오.

Github의 핵심 구성 요소를 사용하면 자주 업데이트를 수행하고 AEM 개발자 커뮤니티의 피드백을 수렴할 수 있습니다. 또한 사용자 지정 구성 요소를 빌드할 때 이와 유사한 패턴을 따라야 합니다.

>[!NOTE]
>
>핵심 구성 요소의 최신 변경 내용을 최신 상태로 유지하기 위해 Github의 [핵심 구성 요소 저장소를](https://github.com/adobe/aem-core-wcm-components) 볼 수 있습니다.

## 구성 요소 라이브러리

핵심 구성 요소의 현재 릴리스를 표시하고 사용 방법의 예를 제공하는 [구성 요소 라이브러리를](http://opensource.adobe.com/aem-core-wcm-components/library.html)확인합니다.

### 샘플 컨텐츠 실행 모드 {#sample-content-run-mode}

We. Retail 참조 사이트에서 해당 [컨텐츠를](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html) 사용하므로, 샘플 컨텐츠가 있을 때 핵심 구성 요소가 빠른 속도로 표시됩니다. 하지만 프로덕션 실행 시 (샘플 컨텐츠 사용 없이 `nosamplecontent` 런타임 모드) 핵심 구성 요소는 더 이상 존재하지 않으며 개발 및/또는 작업 팀에서 AEM 인스턴스에 설치해야 합니다.

>[!NOTE]
>
>프로덕션 환경에서는 항상 Runmode에서 `nosamplecontent` Quickstart를 실행합니다. Runmode에서 `nosamplecontent` 핵심 구성 요소를 사용하려면 핵심 [구성 요소](using.md) 설명서 페이지 사용 지침을 따릅니다.

## 기술 기능 {#technical-capabilities}

다음 표에서는 핵심 구성 요소와 기본 구성 요소 간의 차이점을 대략적으로 설명합니다.

작성 기능과 사전 구성 가능한 옵션에 대한 자세한 내용은 해당 구성 요소에 대한 작성 페이지를 [참조하십시오](authoring.md).

| **기능** | **핵심 구성 요소** | **Foundation 구성 요소** |
|-----|---|---|
| 논리 구현 | [Sling Models](https://sling.apache.org/documentation/bundles/models.html) 주석이 있는 Java Pojos | JSP 코드 |
| 마크업 정의 | [HTML (HTML Template Language)](https://helpx.adobe.com/experience-manager/htl/user-guide.html) 구문 | JSP 코드 |
| XSS 기밀 정보 가리기 | HTL에서 자동화 | 대부분의 수동 설명서 |
| CSS 클래스 이름 지정 | 블록 요소 수정자 (BEM) 표기법을 기반으로 [한 표준화된](https://getbem.com/) 이름 지정 규칙 (릴리스 2.0.0) | 맞춤형 구성 |
| 대화 상자 정의 | [Coral 3](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/reference-materials/coral-ui/coralui3/index.html) | Coral 2 + Classic UI |
| JSON 출력 | [Jackson 일련화 관련 Sling Models Exporter](https://sling.apache.org/documentation/bundles/models.html#exporter-framework-since-130) | 기본 Sling 서블릿 |
| 버전 관리 | [The Model and the HTL](guidelines.md) | 없음 |
| 테스트 | 유닛 테스트 + 통합 테스트 | 통합 테스트 |
| 배달 | [공용 Github를 통해](https://github.com/adobe/aem-core-wcm-components) | 빠른 시작 |
| 라이센스 | [Apache License](https://www.apache.org/licenses/LICENSE-2.0) | Adobe 독점 |
| 기여도 | 가져오기 요청 | 가능하지 않음 |
| 액세스 가능성 | WCAG 2.0 AA 표준을 [완벽하게 준수](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html) | WCAG 2.0 AA 표준과 [부분적으로 호환](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html) |

## 구성 요소 목록 {#component-list}

다음 표에는 API에 연결하는 사용 가능한 핵심 구성 요소가 나와 있으며 해당 구성 요소가 대체할 기본 구성 요소가 나와 있습니다.

| 핵심 구성 요소 | 설명 | Foundation 구성 요소 대체 |
|---|---|---|
| [페이지](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/page/v2/page) | 템플릿 편집기를 사용한 반응형 페이지 | `/libs/foundation/components/page /libs/wcm/foundation/components/page` |
| [탐색 표시](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb) | 페이지 계층 탐색 | `/libs/foundation/components/breadcrumb` |
| [제목](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/title/v2/title) | H 1-H 6 제목 | `/libs/foundation/components/title /libs/wcm/foundation/components/title` |
| [텍스트](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v2/text) | 리치 텍스트 | `/libs/foundation/components/text /libs/foundation/components/table /libs/wcm/foundation/components/text` |
| [이미지](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/image/v2/image) | 최적의 변환 크기 스마트 및 지연 로딩 | `/libs/foundation/components/image /libs/foundation/components/adaptiveimage /libs/foundation/components/logo /libs/foundation/components/mobileimage  /libs/foundation/components/mobilelogo /libs/wcm/foundation/components/image` |
| [목록](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/list/v2/list) | 페이지 목록 | `/libs/foundation/components/list /libs/foundation/components/mobilelist /libs/wcm/foundation/components/list` |
| [소셜 미디어 공유](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/sharing/v1/sharing) | Facebook 및 Pinterest 공유 위젯 | `-` |
| [양식 컨테이너](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/container/v2/container) | 반응형 양식 단락 시스템 | `/libs/foundation/components/form/start /libs/foundation/components/form/end` |
| [양식 텍스트](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v2/text) | 텍스트 입력 필드 | `/libs/foundation/components/form/text /libs/foundation/components/form/password` |
| [양식 옵션](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/options/v2/options) | 다중 옵션 입력 필드 | `/libs/foundation/components/form/checkbox /libs/foundation/components/form/radio /libs/foundation/components/form/dropdown` |
| [숨겨진 양식](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/hidden/v2/hidden) | 숨겨진 입력 필드 | `/libs/foundation/components/form/hidden` |
| [양식 단추](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/button/v2/button) | 제출 또는 사용자 지정 단추 | `/libs/foundation/components/form/submit` |
| [탐색](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/navigation/v1/navigation) | 중첩된 페이지 계층 구조를 나열하는 사이트 탐색 구성 요소 | `/libs/foundation/components/topnav /libs/foundation/components/mobiletopnav` |
| [언어 탐색](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/languagenavigation/v1/languagenavigation) | 글로벌 언어 구조를 나열하는 언어 및 국가 전환기 | `-` |
| [빠른 검색](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/search/v1/search) | 드롭다운 메뉴에서 결과를 즉석 제안 사항으로 표시하는 검색 구성 요소 | `/libs/foundation/components/search` |
| [티저](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/teaser/v1/teaser) | 컨텐츠 작성자가 이미지, 제목 또는 리치 텍스트를 사용하여 추가 컨텐츠에 대한 티저를 쉽게 만들고 추가 컨텐츠 또는 기타 작업을 연결할 수 있도록 합니다. | `-` |
| [탭](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/tabs/v1/tabs) | 컨텐츠 작성자가 여러 탭 내에서 페이지 컨텐츠를 구성할 수 있도록 설정 | `-` |
| [회전판](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/carousel/v1/carousel) | 컨텐츠 작성자가 회전 슬라이드 회전판에서 컨텐츠를 구성할 수 있도록 합니다. | `/libs/foundation/components/carousel` |
| [컨텐츠 조각](https://github.com/adobe/aem-core-wcm-components/tree/master/extension/contentfragment/content/src/content/jcr_root/apps/core/wcm/extension/components/contentfragment/v1/contentfragment) | 컨텐츠 조각을 표시할 수 있습니다. | `-` |
| [컨텐츠 조각 목록](https://github.com/adobe/aem-core-wcm-components/tree/master/extension/contentfragment/content/src/content/jcr_root/apps/core/wcm/extension/components/contentfragmentlist/v1/contentfragmentlist) | 컨텐츠 조각 목록 표시를 허용합니다. | `-` |
| [분리자](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/separator/v1/separator) | 페이지의 컨텐츠 분리 | `-` |

### 예정된 구성 요소 {#upcoming-components}

다음 핵심 구성 요소가 활발히 작동되고 있습니다. 아직 릴리스되지는 않았지만 [개발 분기에서 미리 볼](https://github.com/adobe/aem-core-wcm-components/tree/development)수 있습니다.

* 비디오
* 다운로드

## 핵심 구성 요소 업그레이드 {#upgrade-of-core-components}

버전 구성 요소의 한 가지 이점은 새 AEM 버전으로 마이그레이션과 새 구성 요소 버전으로 마이그레이션을 분리할 수 있다는 것입니다. 또한 새 구성 요소 버전을 사용할 수 있는 경우 각 구성 요소를 새 버전으로 개별 마이그레이션할 수 있습니다.

새 AEM 버전으로 마이그레이션하면 핵심 구성 요소가 작동하는 방식에는 영향을 주지 않습니다. 단, 해당 버전은 마이그레이션되는 새 AEM 버전도 지원합니다. 핵심 구성 요소에 대한 맞춤화는 [중단되거나 제거된 API를 사용하지 않는 한 영향을 받지 않습니다](https://helpx.adobe.com/experience-manager/6-5/release-notes/deprecated-removed-features.html).

새 버전의 핵심 구성 요소로 마이그레이션해도 구성 요소가 작동하는 방식에는 영향을 주지 않지만, 새 기능이 페이지 작성자에게 소개될 수 있는데, 이 기능은 기본 비헤이비어가 원하지 않는 경우에 템플릿 편집기에 의한 일부 구성이 필요할 수 있습니다. 그러나 사용자 지정을 수정해야 할 수도 있습니다. 자세한 내용은 핵심 구성 요소 [페이지 사용자 지정을](customizing.md#upgrade-compatibility-of-customizations) 참조하십시오.

## 핵심 구성 요소를 사용해야 하는 경우 {#when-to-use-the-core-components}

핵심 구성 요소가 완전히 새로워지고 여러 이점을 제공하므로 새로운 AEM 프로젝트를 사용하는 것이 좋습니다. 기존 프로젝트의 경우 마이그레이션은 다시 브랜딩이나 전체 리팩토링과 같은 대규모 프로젝트 작업의 일부여야 합니다.

따라서 Adobe는 다음 권장 사항을 제공합니다.

* **새 프로젝트**새 프로젝트는
항상 핵심 구성 요소를 사용하려고 합니다. 핵심 구성 요소를 직접 또는 [확장할](customizing.md) 수 없는 경우 프로젝트 요구 사항을 충족시킨 다음 핵심 구성 요소에 설명된 구성 요소 아키텍처를 따라 사용자 지정 구성 요소를 만드십시오. 불가능한 경우를 제외하고는 [기본 구성 요소를 사용하지 마십시오](developing.md).
* **사이트 또는 구성 요소 리팩토링이 계획되지 않은 한 기존 프로젝트**
권장 사항은 [기본 구성 요소를](developing.md)계속 사용합니다.\
   대부분의 기존 프로젝트에서 매우 널리 사용되고 있으므로 기본 구성 요소는 [계속 지원됩니다.](developing.md)
* **새로운 맞춤형 구성 요소는**
기존의 [핵심 구성 요소를 맞춤화할](customizing.md)수 있는지 여부를 평가합니다.\
   그렇지 않은 경우, 권장 사항은 [구성 요소 지침 다음에 새 사용자 지정 구성 요소를 구축하는 것입니다](guidelines.md).
* **기존 사용자 지정 구성**
요소가 예상대로 작동하면 그대로 유지합니다.\
   그렇지 않은 경우 위의 &quot;새로운 사용자 지정 구성 요소&quot; 를 참조하십시오.

## 핵심 구성 요소로 마이그레이션

모든 새 프로젝트는 핵심 구성 요소로 구현해야 합니다. 그러나 기존 프로젝트에는 일반적으로 기본 구성 요소가 광범위하게 구현되어 있습니다.

기존 프로젝트 (예: 리브랜딩 또는 전체 리팩토링) 에 대한 큰 노력은 종종 핵심 구성 요소로 마이그레이션할 기회를 제공합니다. Adobe는 이 마이그레이션을 용이하게 하기 위해 핵심 구성 요소 및 최신 AEM 기술의 채택을 장려하기 위한 다양한 마이그레이션 도구를 제공했습니다.

[AEM Modernify Tools Suite](https://github.com/adobe/aem-modernize-tools) 에서는 다음 사항을 쉽게 변환할 수 있습니다.

* 편집 툴이다. 이제는 실시간 미리보기를 통해 더
* 정책에 대한 디자인 구성
* 핵심 구성 요소에 대한 기본 구성 요소
* 터치 활성화 UI에 대한 클래식 UI

이러한 도구의 사용에 대한 자세한 내용은 해당 [설명서를](https://www.adobe.com/go/aem_modernize_tools_en)참조하십시오.

## 핵심 구성 요소 지원 {#core-component-support}

핵심 구성 요소는 AEM의 핵심적인 부분으로, Quickstart의 일부로 제공된 것과 동일한 조건에서 동일한 조건에서 지원됩니다.

다른 AEM 제품 기능과 마찬가지로 일반 규칙은 다음과 같습니다. 구성 요소는 처음 발표될 것으로 발표되며 다음 AEM 릴리스에 대해 가장 일찍 제거되었습니다. 지원 놓기 전에 고객에게 최소 1 개의 릴리스 주기가 새로운 버전의 구성 요소로 이동하도록 합니다.

각 구성 요소의 버전은 지원되는 AEM 버전을 명시합니다. 지원이 AEM 버전에 대해 중지되면 해당 버전의 AEM에 대한 핵심 구성 요소가 지원됩니다.

구성 요소 사용자 정의 지원에 대한 자세한 내용은 핵심 구성 요소 [페이지 사용자 지정을](customizing.md) 참조하십시오.

## 기본 구성 요소 지원 {#foundation-component-support}

Foundation 구성 요소는 많은 AEM 버전에 대한 많은 프로젝트 개발의 기초로 제공되기 때문에 향후 계속 지원될 것입니다.

그러나 Adobe의 개발 강조는 핵심 구성 요소로 옮겨졌고 새로운 기능은 추가되지만 [거의 모든 기본 구성 요소는 AEM 6.5에서 더 이상 사용되지](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-foundation.html) 않으며 앞으로 기본 구성 요소에서만 버그 수정이 수행됩니다.

**다음을 참조하십시오.**

* [핵심 구성 요소 사용](using.md) - 프로젝트에 핵심 구성 요소를 사용할 수 있습니다.
* [구성 요소 지침](guidelines.md) - 핵심 구성 요소의 구현 패턴을 학습합니다.

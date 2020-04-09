---
title: 핵심 구성 요소 개발
description: 핵심 구성 요소는 풍부한 기능, 지속적인 전달, 구성 요소 버전 관리, 최신 구현, 강력한 마크업 및 컨텐츠 JSON 내보내기를 제공하는 강력하고 확장 가능한 기본 구성 요소를 제공합니다.
translation-type: tm+mt
source-git-commit: c338428a681f652d17bb972fb6a2abf216a338c3

---


# 핵심 구성 요소 개발 {#developing-core-components}

## When to Use the Core Components? {#when-to-use-the-core-components}

핵심 구성 요소가 새로워졌고 여러 이점을 제공하므로 새 AEM 프로젝트에서 이러한 구성 요소를 사용하는 것이 좋습니다. 기존 프로젝트의 경우 마이그레이션은 리브랜딩 또는 전체 리팩터링 등 대규모 프로젝트 작업에 포함되었습니다.

따라서 Adobe는 다음과 같은 권장 사항을 제공합니다.

* **새**&#x200B;프로젝트새 프로젝트는 항상 핵심 구성 요소를 사용하려고 시도합니다. 핵심 구성 요소를 프로젝트 요구 사항을 충족하기 위해 직접 또는 [확장할](customizing.md) 수 없는 경우 핵심 구성 요소에 지정된 구성 요소 아키텍처 다음에 사용자 지정 구성 요소를 만듭니다. 달리 가능하지 않은 경우를 제외하고는 [기본 구성 요소를](#foundation-component-support)사용하지 마십시오.
* **사이트나 구성**&#x200B;요소 리팩토링이 계획되지 않은 경우 기존 프로젝트 권장 사항은 [기초 구성 요소를](#foundation-component-support)계속 사용합니다.\
   대부분의 기존 프로젝트에서 매우 널리 사용되고 있으므로 기본 구성 요소는 계속 [지원됩니다.](#foundation-component-support)
* **새 사용자 지정 구성**&#x200B;요소기존 [핵심 구성 요소를 사용자](customizing.md)지정할 수 있는지 여부를 평가합니다.\
   그렇지 않은 경우, 권장 사항은 구성 요소 지침에 따라 새 사용자 지정 구성 요소를 [만드는 것입니다](guidelines.md).
* **기존 사용자**&#x200B;지정 구성 요소구성 요소가 예상대로 작동하면 구성 요소를 그대로 유지합니다.\
   그렇지 않은 경우 위의 &quot;새 사용자 지정 구성 요소&quot;를 참조하십시오.

## 핵심 구성 요소 성공 방법 {#how-to-succeed}

핵심 구성 요소는 강력하고 유연하며 사용하기 쉽고 사용자 정의할 수 있습니다. [몇 가지 주요 지침을](success.md) 따르면 핵심 구성 요소가 있는 프로젝트가 성공했는지 확인할 수 있습니다.

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


## 기술 기능 {#technical-capabilities}

다음 표는 핵심 구성 요소와 기본 구성 요소 간의 차이점을 대략적으로 설명합니다.

작성 기능과 사전 구성 가능한 옵션에 대한 자세한 [내용은 작성 페이지를 참조하십시오](/help/get-started/authoring.md).

| **기능** | **핵심 구성 요소** | **기본 구성 요소** |
|-----|---|---|
| 논리 구현 | Sling 모델 [주석이 있는 Java POJO](https://sling.apache.org/documentation/bundles/models.html) | JSP 코드 |
| 마크업 정의 | [HTML 템플릿 언어](https://docs.adobe.com/content/help/ko-KR/experience-manager-htl/using/overview.html) (HTL) 구문 | JSP 코드 |
| XSS 기밀 정보 가리기 | HTL로 자동화 | 대부분 수동 |
| CSS 클래스 이름 지정 | 블록 요소 수정자( [BEM](https://getbem.com/) ) 표기법을 기반으로 하는 표준 이름 지정 규칙(릴리스 2.0.0 기준) | 사용자 지정 구성표 |
| 대화 상자 정의 | [Coral 3](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/reference-materials/coral-ui/coralui3/index.html) | Coral 2 + 클래식 UI |
| JSON 출력 | [Sling Models Exporter with Jackson serialization](https://sling.apache.org/documentation/bundles/models.html#exporter-framework-since-130) | 기본 Sling 서블릿 |
| 버전 관리 | [모델 및 HTL의 경우](guidelines.md) | 없음 |
| 테스트 | 단위 테스트 + 통합 테스트 | 통합 테스트 |
| 배달 | [공개 GitHub를 통해](https://github.com/adobe/aem-core-wcm-components) | 빠른 시작을 통해 |
| 라이센스 | [Apache License](https://www.apache.org/licenses/LICENSE-2.0) | Adobe 독점 제품 |
| 기여도 | 가져오기 요청 사용 | 불가능 |
| 액세스 가능성 | WCAG 2.0 [AA 표준을]완벽하게 준수(https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html | WCAG 2.0 [AA 표준을 일부 준수하는 경우에만](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html) |

## 구성 요소 목록 {#component-list}

다음 표에는 사용 가능한 핵심 구성 요소(API에 연결)가 나열되며, 이 구성 요소가 대체할 기본 구성 요소를 나타냅니다.

| 핵심 구성 요소 | 설명 | 기본 구성 요소 대체 |
|---|---|---|
| [페이지](https://adobe.com/go/aem_cmp_tech_page_v2) | 템플릿 편집기를 사용한 반응형 페이지 | `/libs/foundation/components/page /libs/wcm/foundation/components/page` |
| [탐색 표시](https://adobe.com/go/aem_cmp_tech_breadcrumb_v2) | 페이지 계층 구조 탐색 | `/libs/foundation/components/breadcrumb` |
| [제목](https://adobe.com/go/aem_cmp_tech_title_v2) | H1-H6 제목 | `/libs/foundation/components/title /libs/wcm/foundation/components/title` |
| [텍스트](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v2/text) | 리치 텍스트 | `/libs/foundation/components/text /libs/foundation/components/table /libs/wcm/foundation/components/text` |
| [이미지](https://adobe.com/go/aem_cmp_tech_image_v2) | 최적의 변환 크기의 지능적이고 레이지 로딩 | `/libs/foundation/components/image /libs/foundation/components/adaptiveimage /libs/foundation/components/logo /libs/foundation/components/mobileimage  /libs/foundation/components/mobilelogo /libs/wcm/foundation/components/image` |
| [목록](https://adobe.com/go/aem_cmp_tech_list_v2) | 페이지 목록 | `/libs/foundation/components/list /libs/foundation/components/mobilelist /libs/wcm/foundation/components/list` |
| [소셜 미디어 공유](https://adobe.com/go/aem_cmp_tech_sharing_v1) | Facebook 및 Pinterest 공유 위젯 | `-` |
| [양식 컨테이너](https://adobe.com/go/aem_cmp_tech_form_container_v2) | 반응형 양식 단락 시스템 | `/libs/foundation/components/form/start /libs/foundation/components/form/end` |
| [양식 텍스트](https://adobe.com/go/aem_cmp_tech_form_text_v2) | 텍스트 입력 필드 | `/libs/foundation/components/form/text /libs/foundation/components/form/password` |
| [양식 옵션](https://adobe.com/go/aem_cmp_tech_form_options_v2) | 여러 옵션 입력 필드 | `/libs/foundation/components/form/checkbox /libs/foundation/components/form/radio /libs/foundation/components/form/dropdown` |
| [숨겨진 양식](https://adobe.com/go/aem_cmp_tech_form_hidden_v2) | 숨겨진 입력 필드 | `/libs/foundation/components/form/hidden` |
| [양식 단추](https://adobe.com/go/aem_cmp_tech_form_button_v2) | 전송 또는 사용자 정의 단추 | `/libs/foundation/components/form/submit` |
| [탐색](https://adobe.com/go/aem_cmp_tech_navigation_v1) | 중첩된 페이지 계층 구조를 나열하는 사이트 탐색 구성 요소 | `/libs/foundation/components/topnav /libs/foundation/components/mobiletopnav` |
| [언어 탐색](https://adobe.com/go/aem_cmp_tech_langnav_v1) | 글로벌 언어 구조를 나열하는 언어 및 국가 전환기 | `-` |
| [빠른 검색](https://adobe.com/go/aem_cmp_tech_search_v1) | 드롭다운 메뉴에서 결과를 즉석 제안으로 표시하는 검색 구성 요소 | `/libs/foundation/components/search` |
| [티저](https://adobe.com/go/aem_cmp_tech_teaser_v1) | 컨텐츠 작성자는 이미지, 제목 또는 리치 텍스트를 사용하여 추가 컨텐츠에 Teaser를 쉽게 만들고 추가 컨텐츠 또는 기타 작업에 연결할 수 있습니다 | `-` |
| [탭](https://adobe.com/go/aem_cmp_tech_tabs_v1) | 컨텐츠 작성자가 여러 탭 내에서 페이지 컨텐츠를 구성할 수 있도록 허용 | `-` |
| [회전판](https://adobe.com/go/aem_cmp_tech_carousel_v1) | 컨텐츠 작성자가 슬라이드 회전 슬라이드로 컨텐츠를 구성할 수 있습니다. | `/libs/foundation/components/carousel` |
| [콘텐츠 조각](https://adobe.com/go/aem_cmp_tech_cf_v1) | 컨텐츠 조각을 표시할 수 있습니다. | `-` |
| [콘텐츠 조각 목록](https://adobe.com/go/aem_cmp_tech_cflist_v1) | 컨텐츠 조각 목록을 표시할 수 있습니다. | `-` |
| [분리자](https://adobe.com/go/aem_cmp_tech_separator_v1) | 페이지에서 컨텐츠 분리 | `-` |
| [어코디언](https://adobe.com/go/aem_cmp_tech_accordion_v1) | 콘텐츠 패널을 축소 가능한 아코디언 구성 | `-` |
| [컨테이너](https://adobe.com/go/aem_cmp_tech_container_v1) | 컨테이너 내 구성 요소 구성 | `-` |
| [단추](https://adobe.com/go/aem_cmp_tech_button_v1) | 페이지에서 단추 만들기 | `-` |
| [다운로드](https://adobe.com/go/aem_cmp_tech_download_v1) | 페이지에 다운로드 가능한 자산 추가 | `-` |
| [경험 조각](https://adobe.com/go/aem_cmp_tech_xf_v1) | 페이지에 경험 조각 추가 | `/libs/cq/experience-fragments/editor/components/experiencefragment` |
| [포함](https://adobe.com/go/aem_cmp_tech_embed_v1) | 페이지 내에 외부 리소스 포함 | - |

### 예정된 구성 요소 {#upcoming-components}

예정된 핵심 구성 요소 로드맵에 대한 개요는 GitHub의 [프로젝트 Wiki를 참조하십시오](https://github.com/adobe/aem-core-wcm-components/wiki/home).

## 핵심 구성 요소 업그레이드 {#upgrade-of-core-components}

버전 관리 구성 요소의 이점 중 하나는 새 AEM 버전으로의 마이그레이션을 새 구성 요소 버전으로의 마이그레이션으로부터 분리할 수 있다는 것입니다. 또한 새 구성 요소 버전을 사용할 수 있는 경우 각 구성 요소를 새 버전으로 개별적으로 마이그레이션할 수 있습니다.

새 AEM 버전으로 마이그레이션은 핵심 구성 요소가 작동하는 방식에 영향을 주지 않습니다. 단, 해당 버전은 마이그레이션되는 새 AEM 버전도 지원합니다. 핵심 구성 요소에 대한 사용자 지정은 [더 이상 사용되지 않거나 제거된](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/release-notes/deprecated-removed-features.html)API를 사용하지 않는 한 영향을 받지 않아야 합니다.

핵심 구성 요소의 새 버전으로 마이그레이션해도 구성 요소의 작동 방식에는 영향을 주지 않지만, 기본 동작을 원하지 않는 경우 템플릿 편집기의 일부 구성이 필요할 수 있는 새로운 기능이 페이지 작성자에게 소개될 수 있습니다. 하지만 사용자 지정을 수정해야 할 수도 있습니다. 자세한 내용은 핵심 구성 요소 [사용자 지정 페이지를 참조하십시오](customizing.md#upgrade-compatibility-of-customizations) .

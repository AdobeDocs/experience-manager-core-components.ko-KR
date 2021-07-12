---
title: 핵심 구성 요소 개발
description: 핵심 구성 요소는 다양한 기능, 지속적인 게재, 구성 요소 버전 관리, 최신 구현, 마크업 및 컨텐츠 JSON 내보내기를 제공하는 강력하고 확장 가능한 기본 구성 요소를 제공합니다.
role: Architect, Developer, Admin
exl-id: 0f79cac1-a3b0-487e-90be-0bd8263d3912
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '1591'
ht-degree: 14%

---

# 핵심 구성 요소 개발 {#developing-core-components}

## 핵심 구성 요소를 사용해야 하는 경우 {#when-to-use-the-core-components}

핵심 구성 요소가 새로워졌고 여러 이점을 제공하므로 새 AEM 프로젝트에서 이러한 구성 요소를 사용하는 것이 좋습니다. 기존 프로젝트의 경우 마이그레이션은 리브랜딩 또는 전체 리팩터링 등 대규모 프로젝트 작업에 포함되었습니다.

따라서 Adobe은 다음 권장 사항을 제공합니다.

* **새**
프로젝트새 프로젝트는 항상 코어 구성 요소를 사용하려고 해야 합니다. 코어 구성 요소를 직접 사용하거나 [extended](customizing.md)를 사용하여 프로젝트 요구 사항을 충족할 수 없는 경우, 핵심 구성 요소에 지정된 구성 요소 아키텍처에 따라 사용자 지정 구성 요소를 만드십시오. 달리 가능한 경우를 제외하고 [기초 구성 요소](/help/versions.md#foundation-component-support)를 사용하지 마십시오.
* **사이트 또**
는 구성 요소 리팩터링을 계획하지 않는 한, 기존 ProjectsRecommendations는  [기초 구성 요소를 계속 사용합니다](/help/versions.md#foundation-component-support).\
   대부분의 기존 프로젝트에서 매우 광범위하게 사용되므로 기초 구성 요소 [은(는) 계속 지원됩니다.](/help/versions.md#foundation-component-support)
* **새 사용자 지정**
구성 요소기존  [핵심 구성 요소를 사용자 지정할 수 있는지 평가합니다](customizing.md).\
   그렇지 않은 경우 [구성 요소 지침](guidelines.md)에 따라 새 사용자 지정 구성 요소를 만드는 것이 좋습니다.
* **기존 사용자 지정**
구성 요소구성 요소가 예상대로 작동하면 그대로 유지합니다.
\
   없는 경우 위의 &quot;새 사용자 지정 구성 요소&quot;를 참조하십시오.

## 핵심 구성 요소를 사용하여 성공하는 방법 {#how-to-succeed}

핵심 구성 요소는 강력하고 유연하며 사용이 편리하고 사용자 지정할 수 있습니다. [몇 가지 주요 ](success.md) 지침에 따라 핵심 구성 요소를 사용하는 프로젝트가 성공했는지 확인합니다.

## 핵심 구성 요소로 마이그레이션

새 프로젝트는 코어 구성 요소를 사용하여 구현해야 합니다. 그러나 기존 프로젝트에는 일반적으로 기초 구성 요소의 광범위한 구현이 있습니다.

### Foundation 구성 요소에서 마이그레이션 {#from-foundation}

기존 프로젝트(예: 리브랜딩 또는 전체 리팩터링)에 대한 더 많은 노력이 종종 핵심 구성 요소로 마이그레이션할 수 있는 기회를 제공합니다. 이러한 마이그레이션을 용이하게 하기 위해 Adobe은 핵심 구성 요소 및 최신 AEM 기술을 채택할 수 있도록 많은 마이그레이션 도구를 제공했습니다.

[AEM 현대화 ](http://opensource.adobe.com/aem-modernize-tools/) 도구 모음으로 쉽게 변환할 수 있습니다.

* 정적 템플릿을 편집 가능한 템플릿
* 디자인 구성을 정책
* 기초 구성 요소를 코어 구성 요소
* 클래식 UI를 터치 사용 UI

이러한 도구의 사용에 대한 자세한 내용은 설명서](http://opensource.adobe.com/aem-modernize-tools/)를 참조하십시오.[

>[!NOTE]
>
>AEM 현대화 도구는 커뮤니티 활동으로, Adobe에서 지원하거나 보증하지 않습니다.

## AEM으로 Cloud Service으로 이동을 통한 마이그레이션 {#via-aemaacs}

Cloud Service로서의 AEM은 자동으로 최신 버전의 핵심 구성 요소를 제공하므로, 온프레미스 AEM 설치에서 이동할 때 프로젝트 `pom.xml` 파일에서 핵심 구성 요소에 대한 종속성을 제거해야 합니다.

프록시 구성 요소는 이전과 동일하게 작동합니다.   프록시는 필요한 슈퍼유형을 가리키며 슈퍼타입 패스에 버전이 있습니다. 이러한 방식으로 종속성을 제거하기만 하면 온프레미스처럼 코어 구성 요소가 AEMaaCS에서 작동할 수 있습니다.

다른 AEMaaCS 프로젝트와 마찬가지로 AEM SDK jar에도 종속성을 추가해야 합니다. 이것은 핵심 구성 요소에만 국한되지 않지만 필요합니다.

```xml
<dependency>
   <groupId>com.adobe.aem</groupId>
   <artifactId>aem-sdk-api</artifactId>
</dependency>
```

AEMaaCS 프로젝트에 대한 자세한 내용은 [AEM 프로젝트 구조](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html) 문서를 참조하십시오.

## 핵심 구성 요소 지원 {#core-component-support}

핵심 구성 요소는 AEM의 필수적인 부분으로, 빠른 시작의 일부로 전달된 것처럼 동일한 이용 약관에 따라 지원됩니다.

다른 AEM 제품 기능과 마찬가지로 일반적인 규칙은 다음과 같습니다. 구성 요소는 먼저 사용을 중단한다고 발표되고, 다음 AEM 릴리스에 대해 가장 빨리 제거됩니다. 이 경우 지원을 중단하기 전에 고객에게 구성 요소의 새 버전으로 이동할 수 있는 릴리스 주기를 1개 이상 제공합니다.

각 구성 요소의 버전은 지원되는 AEM 버전을 명확하게 설명합니다. AEM 버전에 대한 지원이 중단되면 해당 버전의 AEM에 대한 핵심 구성 요소에 대한 지원도 중단됩니다.

구성 요소 사용자 정의에 대한 자세한 내용은 [핵심 구성 요소 사용자 정의](customizing.md) 페이지를 참조하십시오.


## 기술 기능 {#technical-capabilities}

다음 표에서는 핵심 구성 요소와 기초 구성 요소의 차이점에 대해 설명합니다.

작성 기능 및 사전 구성 가능한 옵션에 대한 자세한 내용은 [작성 페이지에 대한 정보](/help/get-started/authoring.md)를 참조하십시오.

| **기능** | **핵심 구성 요소** | **기초 구성 요소** |
|-----|---|---|
| 논리 구현 | [Sling 모델](https://sling.apache.org/documentation/bundles/models.html) 주석이 있는 Java POJO | JSP 코드 |
| 마크업 정의 | [HTL(HTML Template Language](https://docs.adobe.com/content/help/ko/experience-manager-htl/using/overview.html) ) 구문 | JSP 코드 |
| XSS 기밀 정보 가리기 | HTL로 자동화 | 대부분 수동 |
| CSS 클래스 이름 지정 | [블록 요소 수정자](https://getbem.com/) (BEM) 표기법(릴리스 2.0.0부터)을 기반으로 표준화된 명명 규칙 | 사용자 지정 구성표 |
| 대화 상자 정의 | [Coral 3](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/reference-materials/coral-ui/coralui3/index.html) | Coral 2 + 클래식 UI |
| JSON 출력 | [Sling 모델 Exporter with Jackson serialization](https://sling.apache.org/documentation/bundles/models.html#exporter-framework-since-130) | 기본 Sling 서블릿 |
| 버전 관리 | [모델 및 HTL의 경우](guidelines.md) | 없음 |
| 테스트 | 단위 테스트 + 통합 테스트 | 통합 테스트 |
| 배달 | [공용 GitHub를 통해](https://github.com/adobe/aem-core-wcm-components) | Quickstart를 통해 |
| 라이센스 | [Apache 라이센스](https://www.apache.org/licenses/LICENSE-2.0) | Adobe 독점 |
| 기여도 | 가져오기 요청을 통해 | 가능하지 않음 |
| 접근성 | [WCAG 2.0 AA 표준](https://docs.adobe.com/content/help/ko/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html)과 완벽하게 호환됩니다 | [WCAG 2.0 AA 표준](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html)만 부분적으로 준수합니다. |

## 구성 요소 목록 {#component-list}

다음 표에는 사용 가능한 핵심 구성 요소가 나열되며, 해당 API에 연결되며, 해당 구성 요소가 대체되는 기초 구성 요소를 나타냅니다.

| 핵심 구성 요소 | 설명 | 대체된 기초 구성 요소 |
|---|---|---|
| [페이지](https://adobe.com/go/aem_cmp_tech_page_v2) | 템플릿 편집기를 사용한 응답형 페이지 | `/libs/foundation/components/page /libs/wcm/foundation/components/page` |
| [탐색 표시](https://adobe.com/go/aem_cmp_tech_breadcrumb_v2) | 페이지 계층 탐색 | `/libs/foundation/components/breadcrumb` |
| [제목](https://adobe.com/go/aem_cmp_tech_title_v2) | H1-H6 제목 | `/libs/foundation/components/title /libs/wcm/foundation/components/title` |
| [텍스트](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v2/text) | 리치 텍스트 | `/libs/foundation/components/text /libs/foundation/components/table /libs/wcm/foundation/components/text` |
| [이미지](https://adobe.com/go/aem_cmp_tech_image_v2) | 최적의 표현물 크기의 지능적이고 지연 로딩 | `/libs/foundation/components/image /libs/foundation/components/adaptiveimage /libs/foundation/components/logo /libs/foundation/components/mobileimage  /libs/foundation/components/mobilelogo /libs/wcm/foundation/components/image` |
| [목록](https://adobe.com/go/aem_cmp_tech_list_v2) | 페이지 목록 | `/libs/foundation/components/list /libs/foundation/components/mobilelist /libs/wcm/foundation/components/list` |
| [소셜 미디어 공유](https://adobe.com/go/aem_cmp_tech_sharing_v1) | Facebook 및 Pinterest 공유 위젯 | `-` |
| [양식 컨테이너](https://adobe.com/go/aem_cmp_tech_form_container_v2) | 응답형 양식 단락 시스템 | `/libs/foundation/components/form/start /libs/foundation/components/form/end` |
| [양식 텍스트](https://adobe.com/go/aem_cmp_tech_form_text_v2) | 텍스트 입력 필드 | `/libs/foundation/components/form/text /libs/foundation/components/form/password` |
| [양식 옵션](https://adobe.com/go/aem_cmp_tech_form_options_v2) | 여러 옵션 입력 필드 | `/libs/foundation/components/form/checkbox /libs/foundation/components/form/radio /libs/foundation/components/form/dropdown` |
| [숨겨진 양식](https://adobe.com/go/aem_cmp_tech_form_hidden_v2) | 숨겨진 입력 필드 | `/libs/foundation/components/form/hidden` |
| [양식 단추](https://adobe.com/go/aem_cmp_tech_form_button_v2) | 제출 또는 사용자 지정 단추 | `/libs/foundation/components/form/submit` |
| [탐색](https://adobe.com/go/aem_cmp_tech_navigation_v1) | 중첩된 페이지 계층 구조를 나열하는 사이트 탐색 구성 요소입니다 | `/libs/foundation/components/topnav /libs/foundation/components/mobiletopnav` |
| [언어 탐색](https://adobe.com/go/aem_cmp_tech_langnav_v1) | 전역 언어 구조를 나열하는 언어 및 국가 전환기 | `-` |
| [빠른 검색](https://adobe.com/go/aem_cmp_tech_search_v1) | 드롭다운 메뉴에 결과를 즉석 제안으로 표시하는 검색 구성 요소입니다 | `/libs/foundation/components/search` |
| [티저](https://adobe.com/go/aem_cmp_tech_teaser_v1) | 컨텐츠 작성자는 이미지, 제목 또는 리치 텍스트를 사용하여 추가 컨텐츠에 Teaser를 쉽게 만들고 추가 컨텐츠 또는 기타 작업에 연결할 수 있습니다 | `-` |
| [탭](https://adobe.com/go/aem_cmp_tech_tabs_v1) | 컨텐츠 작성자가 여러 탭 내에서 페이지 컨텐츠를 구성할 수 있습니다 | `-` |
| [회전판](https://adobe.com/go/aem_cmp_tech_carousel_v1) | 컨텐츠 작성자가 회전하는 슬라이드 회전판에서 컨텐츠를 구성할 수 있도록 해줍니다 | `/libs/foundation/components/carousel` |
| [콘텐츠 조각](https://adobe.com/go/aem_cmp_tech_cf_v1) | 컨텐츠 조각을 표시할 수 있습니다 | `-` |
| [콘텐츠 조각 목록](https://adobe.com/go/aem_cmp_tech_cflist_v1) | 컨텐츠 조각 목록을 표시할 수 있습니다 | `-` |
| [분리자](https://adobe.com/go/aem_cmp_tech_separator_v1) | 페이지에서 컨텐츠 분리 | `-` |
| [어코디언](https://adobe.com/go/aem_cmp_tech_accordion_v1) | 축소 가능한 아코디언으로 컨텐츠 패널 구성 | `-` |
| [컨테이너](https://adobe.com/go/aem_cmp_tech_container_v1) | 컨테이너 내에서 구성 요소 구성 | `-` |
| [단추](https://adobe.com/go/aem_cmp_tech_button_v1) | 페이지에서 단추 만들기 | `-` |
| [다운로드](https://adobe.com/go/aem_cmp_tech_download_v1) | 페이지에 다운로드 가능한 자산 추가 | `-` |
| [경험 조각](https://adobe.com/go/aem_cmp_tech_xf_v1) | 페이지에 경험 조각 추가 | `/libs/cq/experience-fragments/editor/components/experiencefragment` |
| [포함](https://adobe.com/go/aem_cmp_tech_embed_v1) | 페이지 내에 외부 리소스 포함 | - |
| [진행률 표시줄](https://adobe.com/go/aem_cmp_tech_progress_v1) | 목표를 향해 진행 상황을 시각적으로 표시 | - |
| [PDF 뷰어](https://adobe.com/go/aem_cmp_tech_pdfviewer_v1) | 페이지에 PDF 문서를 보여 줍니다 | - |

### 예정된 구성 요소 {#upcoming-components}

예정된 코어 구성 요소 로드 맵에 대한 개요는 GitHub](https://github.com/adobe/aem-core-wcm-components/wiki/home)에서 [프로젝트 wiki를 참조하십시오.

## 핵심 구성 요소 업그레이드 {#upgrade-of-core-components}

버전이 지정된 구성 요소의 한 가지 이점은 새 구성 요소 버전으로의 마이그레이션과 새 AEM 버전으로의 마이그레이션을 구분할 수 있다는 것입니다. 또한 새 구성 요소 버전을 사용할 수 있는 경우 각 구성 요소를 새 버전으로 개별 마이그레이션할 수 있습니다.

새 AEM 버전으로 마이그레이션해도 핵심 구성 요소가 작동하는 방식에는 영향을 주지 않습니다. 단, 해당 버전도 마이그레이션되는 새 AEM 버전을 지원합니다. 핵심 구성 요소에 대한 사용자 지정은 [더 이상 사용되지 않거나 제거된 API를 사용하지 않는 한 영향을 받지 않아야 합니다](https://docs.adobe.com/content/help/ko-KR/experience-manager-cloud-service/release-notes/deprecated-removed-features.html).

핵심 구성 요소의 새 버전으로 마이그레이션해도 구성 요소의 작동 방식에는 영향을 주지 않지만, 기본 동작을 원하지 않는 경우 템플릿 편집기에 의해 일부 구성이 필요할 수 있는 페이지 작성자에게 새 기능이 도입될 수 있습니다. 그러나 사용자 지정을 수정해야 할 수 있습니다. 자세한 내용은 [코어 구성 요소 사용자 지정](customizing.md#upgrade-compatibility-of-customizations) 페이지를 참조하십시오.

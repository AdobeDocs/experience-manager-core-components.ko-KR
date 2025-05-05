---
title: 핵심 구성 요소 개발
description: 핵심 구성 요소는 강력하고 확장 가능한 기본 구성 요소를 제공합니다. 이 기본 구성 요소에는 다양한 기능의 연속 제공, 구성 요소 버전 관리, 최신 구현, 린 마크업 및 JSON 포맷의 콘텐츠 내보내기 등이 있습니다.
role: Architect, Developer, Admin
exl-id: 0f79cac1-a3b0-487e-90be-0bd8263d3912
source-git-commit: 614bc5fd01a76a6888606faa4576e1695b77ba58
workflow-type: tm+mt
source-wordcount: '1287'
ht-degree: 100%

---

# 핵심 구성 요소 개발 {#developing-core-components}

## 핵심 구성 요소는 언제 사용합니까? {#when-to-use-the-core-components}

핵심 구성 요소가 새로워졌고 여러 이점을 제공하므로 새 AEM 프로젝트에서 이러한 구성 요소를 사용하는 것이 좋습니다. 기존 프로젝트의 경우 마이그레이션은 리브랜딩 또는 전체 리팩터링 등 대규모 프로젝트 작업에 포함되었습니다.

이에 Adobe에서 제공하는 권장 사항은 다음과 같습니다.

* **새 프로젝트**
새 프로젝트는 항상 핵심 구성 요소 사용을 시도해야 합니다. 프로젝트 요구 사항에 부합하는 핵심 구성 요소를 바로 사용하거나 [확장](customizing.md)할 수 없을 경우 핵심 구성 요소에 명시된 구성 요소 아키텍처에 따라 맞춤형 구성 요소를 만듭니다. 불가능한 경우를 제외하고 [기초 구성 요소](/help/versions.md#foundation-component-support)를 사용하지 마십시오.
* **기존 프로젝트**
사이트 또는 구성 요소 리팩터링이 예정되는 경우가 아니라면 [기초 구성 요소](/help/versions.md#foundation-component-support)를 지속적으로 사용하는 것이 좋습니다.\
  기존 프로젝트에서 널리 사용되기 때문에 기초 구성 요소를 [지속적으로 지원할 수 있습니다](/help/versions.md#foundation-component-support).
* **새 맞춤형 구성 요소**
기존 [핵심 구성 요소를 사용자 정의할 수 있는지 평가합니다.](customizing.md)\
  그렇지 않으면 [구성 요소 가이드라인](guidelines.md)에 따라 새 맞춤형 구성 요소를 빌드하는 것이 좋습니다.
* **기존 맞춤형 구성 요소**
구성 요소가 정상적으로 작동하면 그대로 유지합니다.\
  그렇지 않으면 상기 “새 맞춤형 구성 요소”를 참조하십시오.

## 핵심 구성 요소로 성공하는 방법은? {#how-to-succeed}

핵심 구성 요소는 강력하고 유연하며 사용 및 맞춤화가 매우 간편합니다. [몇 군데 주요 가이드라인에 따라](success.md) 핵심 구성 요소를 사용하면 프로젝트를 성공적으로 완료할 수 있습니다.

## 핵심 구성 요소로 마이그레이션

핵심 구성 요소를 사용하여 새 프로젝트를 구현해야 합니다. 단, 일반적으로 기존 프로젝트에서 기초 구성 요소를 확장하고 구현할 수 있습니다.

### 기초 구성 요소로의 마이그레이션 {#from-foundation}

기존 프로젝트(예: 리브랜딩 또는 전체 리팩터링)에 더 많은 노력을 투자하면서 핵심 구성 요소로 마이그레이션할 수 있는 가능성이 높아집니다. 원활한 마이그레이션을 위해 Adobe는 다양한 마이그레이션 도구를 제공함으로써 핵심 구성 요소 및 최신 AEM 기술 도입을 유도하고 있습니다.

[AEM 현대화 도구](https://opensource.adobe.com/aem-modernize-tools/)를 사용하여 다음과 같이 쉽게 변환할 수 있습니다.

* 정적 템플릿을 편집 가능한 템플릿
* 디자인 구성을 정책
* 기초 구성 요소를 핵심 구성 요소
* 클래식 UI를 터치 사용 UI

이 도구 사용에 대한 자세한 내용은 [도구 설명서를 참조하십시오](https://opensource.adobe.com/aem-modernize-tools/).

>[!NOTE]
>
>AEM 현대화 도구는 커뮤니티 활동으로, Adobe에서 지원하거나 보증하지 않습니다.

## 이동을 통해 AEM as a Cloud Service로 마이그레이션 {#via-aemaacs}

AEM as a Cloud Service에는 최신 버전의 핵심 구성 요소가 자동으로 제공되므로, 온프레미스 AEM 설치에서 이동할 경우 프로젝트 `pom.xml` 파일의 핵심 구성 요소에 대한 종속성을 제거해야 합니다.

프록시가 필수 슈퍼타입을 지정하고 슈퍼타입 경로에 버전이 있기 때문에 프록시 구성 요소는 이전과 동일하게 작동합니다. 이러한 방식으로 종속성이 간단히 제거되면 핵심 구성 요소는 AEMaaCS에서 이전과 동일하게 온프레미스로 작동합니다.

다른 AEMaaCS 프로젝트와 마찬가지로 또한 종속성을 AEM SDK jar에 추가해야 합니다. 이는 핵심 구성 요소와 관련이 없지만 필요합니다.

```xml
<dependency>
   <groupId>com.adobe.aem</groupId>
   <artifactId>aem-sdk-api</artifactId>
</dependency>
```

AEMaaCS 프로젝트에 대한 자세한 내용은 [AEM 프로젝트 구조](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=ko)를 참조하십시오.

## 핵심 구성 요소 지원 {#core-component-support}

핵심 구성 요소는 AEM의 필수적인 부분으로, 빠른 시작의 일부로 전달된 것처럼 동일한 이용 약관에 따라 지원됩니다.

다른 AEM 제품 기능과 마찬가지로 일반적인 규칙은 다음과 같습니다. 최초 발표에 따르면 구성 요소는 더 이상 사용될 수 없으며 우선적으로 제거될 수 있다는 점입니다. 이에 지원이 종료되기 전에 고객에게 구성 요소의 새 버전으로 이동할 수 있는 릴리스 주기를 1개 이상 제공합니다.

각 구성 요소의 버전은 지원되는 AEM 버전을 명확하게 설명합니다. AEM 버전에 대한 지원이 중단되면 해당 버전의 AEM에 대한 핵심 구성 요소에 대한 지원도 중단됩니다.

맞춤형 구성 요소 지원에 대한 자세한 내용은 [핵심 구성 요소 맞춤화](customizing.md)를 참조하십시오.


## 기술적 기능 {#technical-capabilities}

다음 표는 핵심 구성 요소와 기초 구성 요소의 차이점에 대한 개요를 제공합니다.

작성 기능 및 사전에 구성 가능한 옵션에 대한 자세한 내용은 [해당 기능 및 옵션에 대한 작성 페이지를 참조하십시오](/help/get-started/authoring.md).

| **기능** | **핵심 구성 요소** | **기초 구성 요소** |
|-----|---|---|
| 논리 구현 | [슬링 모드](https://sling.apache.org/documentation/bundles/models.html) 주석이 포함된 Java POJO | JSP 코드 |
| 마크업 정의 | [HTML 템플릿 언어](https://experienceleague.adobe.com/docs/experience-manager-htl/using/overview.html?lang=ko)(HTL) 구문 | JSP 코드 |
| XSS 정리 | HTL로 자동화 | 대부분의 경우 수동 |
| CSS 클래스 명명 | [블록 요소 수정자](https://getbem.com/)(BEM) 표기법에 따라 표준화된 명명 규칙(릴리스 2.9.0부터) | 맞춤형 스키마 |
| 대화 상자 정의 | [코랄 3](https://helpx.adobe.com/kr/experience-manager/6-5/sites/developing/using/reference-materials/coral-ui/coralui3/index.html) | 코랄 2 + 클래식 UI |
| JSON 출력 | [Jackson 일련화가 적용된 슬링 모드 내보내기](https://sling.apache.org/documentation/bundles/models.html#exporter-framework-since-130) | 기본 슬링 서블릿 |
| 버전 관리 | [모델 및 HTL 용](guidelines.md) | 없음 |
| 테스트 | 단위 테스트 + 통합 테스트 | 통합 테스트 |
| 제공 | [공용 GitHub 통과](https://github.com/adobe/aem-core-wcm-components) | 빠른 시작 통과 |
| 라이선스 | [Apache 라이선스](https://www.apache.org/licenses/LICENSE-2.0) | Adobe 소유 |
| 기여도 | 끌어오기 요청 통과 | 불가능 |
| 접근성 | [WCAG 2.0 AA 표준](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html?lang=ko)을 완벽히 준수 | [WCAG 2.0 AA 표준](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html?lang=ko)을 일부만 준수 |

## 구성 요소 목록 {#component-list}

다음 표에서 사용 가능한 API 연결 핵심 구성 요소와 대체 중인 기초 구성 요소를 확인할 수 있습니다.

| 핵심 구성 요소 | 설명 | 기초 구성 요소 대체 |
|---|---|---|
| [페이지](https://adobe.com/go/aem_cmp_tech_page_v2_kr) | 템플릿 편집기로 작동하는 반응형 페이지 | `/libs/foundation/components/page /libs/wcm/foundation/components/page` |
| [이동 경로](https://adobe.com/go/aem_cmp_tech_breadcrumb_v2_kr) | 페이지 계층 구조 탐색 | `/libs/foundation/components/breadcrumb` |
| [제목](https://adobe.com/go/aem_cmp_tech_title_v2_kr) | H1-H6 제목 | `/libs/foundation/components/title /libs/wcm/foundation/components/title` |
| [텍스트](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v2/text) | 서식 있는 텍스트 | `/libs/foundation/components/text /libs/foundation/components/table /libs/wcm/foundation/components/text` |
| [이미지](https://adobe.com/go/aem_cmp_tech_image_v2_kr) | 최적의 크기를 위한 렌디션의 스마트 및 소극적 로드 | `/libs/foundation/components/image /libs/foundation/components/adaptiveimage /libs/foundation/components/logo /libs/foundation/components/mobileimage  /libs/foundation/components/mobilelogo /libs/wcm/foundation/components/image` |
| [목록](https://adobe.com/go/aem_cmp_tech_list_v2_kr) | 페이지 목록 | `/libs/foundation/components/list /libs/foundation/components/mobilelist /libs/wcm/foundation/components/list` |
| [소셜 미디어 공유](https://adobe.com/go/aem_cmp_tech_sharing_v1_kr) | Facebook 및 Pinterest 공유 위젯 | `-` |
| [양식 컨테이너](https://adobe.com/go/aem_cmp_tech_form_container_v2_kr) | 반응형 양식 단락 시스템 | `/libs/foundation/components/form/start /libs/foundation/components/form/end` |
| [양식 텍스트](https://adobe.com/go/aem_cmp_tech_form_text_v2_kr) | 텍스트 입력 필드 | `/libs/foundation/components/form/text /libs/foundation/components/form/password` |
| [양식 옵션](https://adobe.com/go/aem_cmp_tech_form_options_v2_kr) | 여러 옵션 입력 필드 | `/libs/foundation/components/form/checkbox /libs/foundation/components/form/radio /libs/foundation/components/form/dropdown` |
| [양식 숨김](https://adobe.com/go/aem_cmp_tech_form_hidden_v2_kr) | 숨겨진 입력 필드 | `/libs/foundation/components/form/hidden` |
| [양식 버튼](https://adobe.com/go/aem_cmp_tech_form_button_v2_kr) | 제출 또는 맞춤형 버튼 | `/libs/foundation/components/form/submit` |
| [탐색](https://adobe.com/go/aem_cmp_tech_navigation_v1_kr) | 중첩된 페이지 계층 구조를 보여 주는 사이트 탐색 구성 요소 | `/libs/foundation/components/topnav /libs/foundation/components/mobiletopnav` |
| [언어 탐색](https://adobe.com/go/aem_cmp_tech_langnav_v1_kr) | 전역 언어 구조를 보여 주는 언어 및 지역 전환기 | `-` |
| [빠른 검색](https://adobe.com/go/aem_cmp_tech_search_v1_kr) | 추천 사항으로 드롭다운 메뉴의 결과를 보여 주는 검색 구성 요소 | `/libs/foundation/components/search` |
| [티저](https://adobe.com/go/aem_cmp_tech_teaser_v1_kr) | 콘텐츠 작성자는 이미지, 제목이나 서식 있는 텍스트와 추가 콘텐트 링크 또는 기타 작업을 통해 티저를 손쉽게 제작할 수 있습니다. | `-` |
| [탭](https://adobe.com/go/aem_cmp_tech_tabs_v1_kr) | 콘텐츠 작성자는 여러 탭에서 페이지 콘텐츠를 구성할 수 있습니다. | `-` |
| [슬라이드](https://adobe.com/go/aem_cmp_tech_carousel_v1_kr) | 콘텐츠 작성자는 회전하는 슬라이드를 통해 페이지 콘텐츠를 구성할 수 있습니다. | `/libs/foundation/components/carousel` |
| [콘텐츠 조각](https://adobe.com/go/aem_cmp_tech_cf_v1_kr) | 콘텐츠 조각을 표시할 수 있습니다. | `-` |
| [콘텐츠 조각 목록](https://adobe.com/go/aem_cmp_tech_cflist_v1_kr) | 콘텐츠 조각 목록을 표시할 수 있습니다. | `-` |
| [분리자](https://adobe.com/go/aem_cmp_tech_separator_v1_kr) | 페이지의 콘텐츠를 분리합니다. | `-` |
| [아코디언](https://adobe.com/go/aem_cmp_tech_accordion_v1_kr) | 축소 가능한 아코디언으로 콘텐츠 패널을 구성합니다. | `-` |
| [컨테이너](https://adobe.com/go/aem_cmp_tech_container_v1_kr) | 컨테이너 내부 구성 요소를 구성합니다. | `-` |
| [버튼](https://adobe.com/go/aem_cmp_tech_button_v1_kr) | 페이지의 버튼을 만듭니다. | `-` |
| [다운로드](https://adobe.com/go/aem_cmp_tech_download_v1_kr) | 다운로드 가능한 에셋을 페이지에 추가합니다. | `-` |
| [경험 조각](https://adobe.com/go/aem_cmp_tech_xf_v1_kr) | 경험 조각을 페이지에 추가합니다. | `/libs/cq/experience-fragments/editor/components/experiencefragment` |
| [임베드](https://adobe.com/go/aem_cmp_tech_embed_v1_kr) | 페이지 내부 외부 리소스를 임베드합니다. | - |
| [진행률 표시줄](https://adobe.com/go/aem_cmp_tech_progress_v1_kr) | 목표에 대한 진행률을 시각적으로 표시합니다. | - |
| [PDF 뷰어](https://adobe.com/go/aem_cmp_tech_pdfviewer_v1_kr) | 페이지의 PDF 문서를 제공합니다. | - |

## 핵심 구성 요소 업그레이드 {#upgrade-of-core-components}

버전 관리된 구성 요소의 이점은 새 AEM 버전으로의 마이그레이션과 새 구성 요소 버전으로의 마이그레이션을 구분할 수 있다는 점입니다. 또한, 새 구성 요소 버전을 사용할 경우 각 구성 요소를 새 버전으로 개별 마이그레이션할 수 있습니다.

구성 요소 버전이 마이그레이션 중인 새 AEM 버전을 지원하는 경우 새 AEM 버전으로 마이그레이션해도 핵심 구성 요소가 작동하는 방식에는 영향을 미치지 않습니다. 핵심 구성 요소가 맞춤화되어도 [더 이상 사용되지 않거나 제거된](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/deprecated-removed-features.html?lang=ko) API를 사용하지 않으면 아무런 영향을 받지 않습니다.

핵심 구성 요소의 새 버전으로 마이그레이션해도 구성 요소가 작동하는 방식에는 영향을 미치지 않습니다. 하지만, 기본 비헤이비어가 필요하지 않은 경우 페이지 작성자는 템플릿 편집기에서 일부 구성할 수 있는 새로운 기능을 적용할 수도 있습니다. 하지만 맞춤화는 조정할 수도 있습니다. 자세한 내용은 [핵심 구성 요소 맞춤화](customizing.md#upgrade-compatibility-of-customizations)를 참조하십시오.

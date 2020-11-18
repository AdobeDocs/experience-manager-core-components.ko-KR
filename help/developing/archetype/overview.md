---
title: AEM 프로젝트 전형
description: AEM 기반 응용 프로그램용 프로젝트 템플릿
translation-type: tm+mt
source-git-commit: c9ec069a9eb12b8625be09d1c38dcaaf437bd5cb
workflow-type: tm+mt
source-wordcount: '1280'
ht-degree: 6%

---


# AEM 프로젝트 전형 {#aem-project-archetype}

AEM Project Tranype은 최소한의 모범 사례 기반 Adobe Experience Manager(AEM) 프로젝트를 웹 사이트의 시작점으로 만드는 Maven 템플릿입니다.

>[!TIP]
>
>최신 AEM 프로젝트 원형은 GitHub에서 찾을 [수 있습니다](https://github.com/adobe/aem-project-archetype).

## 리소스 {#resources}

* **원형 문서(이 문서):** 원형 아키텍처 및 서로 다른 모듈에 대한 개요.
   * **[원형 사용:](using.md)** 원형 및 사용 가능한 모듈 사용에 대한 자세한 내용
   * **[ui.frontends:](uifrontend.md)** 프런트 엔드 빌드 모듈을 사용하는 방법
* 다음 자습서는 이 기본 유형을 기반으로 합니다.
   * **[WKND 사이트:](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)** 새로운 웹 사이트를 시작하는 방법을 살펴보십시오.
   * **[WKND 단일 페이지 앱:](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)** AEM에서 완전히 저작할 수 있는 반응형 또는 각도 웹 앱을 제작하는 방법을 살펴봅니다.

## 기능 {#features}

* **모범 사례:** 모든 Adobe의 최신 권장 사례를 사용하여 사이트를 Bootstrap할 수 있습니다.
* **낮은 코드:** 템플릿을 편집하고 컨텐츠를 제작하며 CSS를 배포할 수 있으며 사이트를 바로 라이브할 수 있습니다.
* **클라우드 지원:** 원하는 경우 며칠 안에 [AEM을 Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html) 로 사용하여 라이브하고 손쉽게 확장 및 유지 관리할 수 있습니다.
* **발송자:** 프로젝트는 속도와 보안을 보장하는 [Dispatcher 구성만](https://docs.adobe.com/content/help/ko-KR/experience-manager-dispatcher/using/dispatcher.html) 사용하여 완료됩니다.
* **다중 사이트:** 필요한 경우 원형은 [다중 언어 및 다중 영역 설정에 대한 컨텐츠 구조를 생성합니다](https://docs.adobe.com/content/help/en/experience-manager-65/administering/introduction/msm.html).
* **핵심 구성 요소:** 작성자는 다양한 표준화된 구성 요소 [세트를 사용하여 거의 모든 레이아웃을 만들 수 있습니다](/help/introduction.md).
* **편집 가능한 템플릿:** 코드 [없이 거의 모든](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html)템플릿을 취합하고 작성자가 편집할 수 있는 항목을 정의할 수 있습니다.
* **응답형 레이아웃:** 템플릿 또는 개별 페이지에서 정의된 중단점에 대해 요소가 리플로우되는 [방식을](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html) 정의합니다.
* **머리글 및 바닥글:** 구성 요소의 [로컬라이제이션 기능을 사용하여 코드 없이 구성 및 현지화할 수 있습니다](https://docs.adobe.com/content/help/ko-KR/experience-manager-core-components/using/get-started/localization.html).
* **스타일 시스템:** 작성자가 다른 스타일을 [적용할 수 있도록 하여 사용자 지정 구성 요소를](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/style-system.html) 작성하지 마십시오.
* **프런트 엔드 빌드:** 프런트 엔드 개발자는 [웹 팩, TypeScript](uifrontend.md#webpack-dev-server) 및 SASS를 사용하여 AEM 페이지 [를 만들고 클라이언트 라이브러리를](uifrontend.md) 구축할 수 있습니다.
* **WebApp-Ready:** React [또는 Angular](uifrontend-react.md) 를 사용하는 사이트에서는 [SPA SDK](uifrontend-angular.md)를 [사용하여](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/headless/spa/developing.html) 앱 [의 컨텍스트](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)내 저작을 유지할 수 있습니다.
* **상거래 활성화:** 커머스 코어 구성 요소를 사용하여 [Magento과](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/commerce/home.html) 같은 상거래 솔루션과 [AEM](https://magento.com/) 커머스 [를 통합하려는](https://github.com/adobe/aem-core-cif-components)프로젝트의경우.
* **예제 코드:** HelloWorld 구성 요소와 샘플 모델, 서블릿, 필터 및 스케줄러를 체크 아웃합니다.
* **오픈 소스:** 만약 어떤 것이 제대로 되어 있지 않다면, [여러분의 개선점을](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) 기부하라!

## 사용량

프로젝트를 생성하려면 다음 명령줄을 필요에 맞게 조정합니다.

```
mvn -B archetype:generate \
 -D archetypeGroupId=com.adobe.aem \
 -D archetypeArtifactId=aem-project-archetype \
 -D archetypeVersion=24 \
 -D appTitle="My Site" \
 -D appId="mysite" \
 -D groupId="com.mysite" \
```

* Set `aemVersion=cloud` for [AEM as a Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html);\
   `aemVersion=6.5.0` Adobe Managed Services [](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams)또는 온프레미스 설정
핵심 구성 요소는 AEM용 OOTB를 Cloud Service으로 제공하므로 비 클라우드 aem 버전에 대해서만 코어 구성 요소 종속성이 추가됩니다.
* 웹 사이트 제목 및 구성 요소 그룹 `appTitle="My Site"` 을 정의하려면 조정합니다.
* 클라이언트 라이브러리 이름 `appId="mysite"` 은 물론 구성 요소, 구성 요소, 구성 및 컨텐츠 폴더 이름을 정의하기 위해 조정합니다.
* Maven groupId `groupId="com.mysite"` 와 Java 소스 패키지를 정의하도록 조정합니다.
* 사용 가능한 속성 목록을 조회하여 조정할 추가 사항이 있는지 확인합니다.

## 사용 가능한 속성

| 이름 | 기본값 | 설명 |
--------------------------|----------------|--------------------
| `appTitle` |  | 애플리케이션 제목은 웹 사이트 제목 및 구성 요소 그룹(예: `"My Site"`). |
| `appId` |  | 기술 이름은 클라이언트 라이브러리 이름(예: `"mysite"`). |
| `artifactId` | *`${appId}`* | 기본 마비안 아티팩트 ID(예: `"mysite"`). |
| `groupId` |  | 기본 마비안 그룹 ID(예: `"com.mysite"`). |
| `package` | *`${groupId}`* | Java 소스 패키지(예: `"com.mysite"`). |
| `version` | `1.0-SNAPSHOT` | 프로젝트 버전(예: `1.0-SNAPSHOT`). |
| `aemVersion` | `cloud` | Target AEM 버전(Cloud Service `cloud` 로 [AEM용으로 사용할 수 있음](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html))또는 `6.5.0`Adobe `6.4.4` Managed Services [](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) 또는 온프레미스)를 사용할 수 있습니다. |
| `sdkVersion` | `latest` | SDK `aemVersion=cloud` 버전 [을 지정할](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html) 수 있는 경우(예: `2020.02.2265.20200217T222518Z-200130`). |
| `includeDispatcherConfig` | `y` | 값(또는 `aemVersion` )에 따라 클라우드 또는 AMS/on-premise용 디스패처 구성을 `y` `n`포함합니다. |
| `frontendModule` | `general` | 클라이언트 라이브러리를 생성하는 Webpack 프런트 엔드 빌드 모듈(일반 사이트일 수도 `general` 또는 `none` 에 사용할 수 있음)을 포함합니다.spa 편집기 `angular` 를 구현하는 단일 페이지 앱에 대해 `react` 또는 [사용할 수 있습니다](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/headless/spa/editor-overview.html). |
| `language` | `en` | 언어 코드(예: `en`, `deu`). |
| `country` | `us` | 국가 번호(ISO 3166-1)를 사용하여 콘텐츠 구조를 만드는 방법(예: `US`). |
| `singleCountry` | `y` | 언어 마스터 컨텐츠 구조를 포함합니다( `y`또는 `n`). |
| `includeExamples` | `n` | 구성 요소 [라이브러리](https://www.aemcomponents.dev/) 예제 사이트( `y`또는 `n`)를 포함합니다. |
| `includeErrorHandler` | `n` | 전체 인스턴스( `y` 또는 `n`)에 대해 글로벌할 사용자 지정 404 응답 페이지를 포함합니다. |
| `includeCommerce` | `n` | CIF [핵심 구성 요소](https://github.com/adobe/aem-core-cif-components) 종속성을 포함하고 해당 객체를 생성합니다. |
| `commerceEndpoint` |  | CIF에만 필요합니다. 사용할 상거래 시스템 GraphQL 서비스의 선택 끝점(예: `https://hostname.com/grapql`). |
| `datalayer` | `y` | Adobe 클라이언트 [데이터 레이어와의 통합을 활성화합니다](/help/developing/data-layer/overview.md). |
| `amp` | `n` | 생성된 [프로젝트 템플릿에](/help/developing/amp.md) 대한 AMP 지원을 활성화합니다. |

## 분석기 모듈 {#analyzer-module}

AEM analyzer Maven 플러그인은 다양한 컨텐츠 패키지 프로젝트의 구조를 분석합니다.

AEM [마스터 프로젝트에 이를 포함하는 방법에 대한 자세한 내용은 AEM Analyzer Maven 플러그인 설명서를](https://github.com/adobe/aemanalyser-maven-plugin/blob/main/aemanalyser-maven-plugin/README.md) 참조하십시오. 이 플러그인은 AEM Maven 원형형 버전 25 이상에 포함되어 있습니다.

다음은 이 단계의 일부로 실행되는 분석기를 설명하는 표입니다. 일부는 로컬 SDK에서 실행되는 반면 다른 일부는 Cloud Manager 파이프라인 배포 중에만 실행됩니다.

| 모듈 | 함수, 예 및 문제 해결 | 로컬 SDK | Cloud Manager |
|---|---|---|---|
| `api-regions-exportsimports` | 모든 OSGI 번들이 Maven 프로젝트에 포함된 다른 번들의 Export-package 선언에서 충족한 Import-Package 선언이 있는지 확인합니다. <p> </p> 문제를 해결하려면 잘못된 이름 또는 잘못된 버전이 사용되었는지 확인하기 위해 내보낼 번들의 매니페스트를 확인하십시오. | 예 | 예 |
| `requirements-capabilities` | OSGI 번들에서 수행된 모든 요구 사항 선언이 Maven 프로젝트에 포함된 다른 번들의 기능 선언에 만족하는지 확인합니다. <p> </p> 문제를 해결하려면 누락된 이유를 확인하는 기능을 선언해야 할 번들의 매니페스트를 확인하십시오. | 예 | 예 |
| `bundle-content` | 번들에 Sling-Initial-Content로 지정된 초기 컨텐츠가 포함되어 있는 경우 Cloud Service 클러스터된 환경으로서 AEM에서 문제가 되는 경고 메시지가 표시됩니다. | 예 | 예 |
| `api-regions-crossfeature-dups` | 고객 OSGI 번들에 AEM을 Cloud Service의 공용 API로 재정의하는 내보내기 패키지 선언이 없는지 확인합니다. | 예 | 예 |

## 시스템 요구 사항

| 원형 | AEM as a Cloud Service | AEM 6.5 | AEM 6.4 | Java SE | 마벤 |
|---------|---------|---------|---------|---------|---------|
| [24](https://github.com/adobe/aem-project-archetype/releases/tag/aem-project-archetype-24) | 지속적인 | 6.5.5.0+ | 6.4.8.1+ | 8, 11 | 3.3.9+ |

AEM용 로컬 개발 환경을 Cloud Service SDK [또는](https://docs.adobe.com/content/help/en/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html) 이전 버전의 AEM으로 [](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html)설정하십시오.

### 알려진 문제

Windows에서 실행하고 디스패처 구성을 생성하는 경우 관리자 권한 명령 프롬프트 또는 Linux용 Windows 하위 시스템에서 실행해야 합니다( [#329](https://github.com/adobe/aem-project-archetype/issues/329)참조).

매개 변수 없이 대화형 모드에서 원형 유형을 실행할 때 최종 확인을 취소하면 기본값이 있는 속성을 변경할 수 없으며 질문의 기본값이 있는 속성을 포함하여 질문을 반복합니다(자세한 내용은 `-B` TRANYPE-308[](https://issues.apache.org/jira/browse/ARCHETYPE-308) 참조).

## Further Reading {#further-reading}

장점, 옵션, 모듈 작동 방식 등 원형형을 사용하는 방법에 대한 자세한 내용은 [원형 [사용] 문서를 참조하십시오.](using.md)

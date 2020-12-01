---
title: AEM 프로젝트 전형
description: AEM 기반 응용 프로그램용 프로젝트 템플릿
translation-type: tm+mt
source-git-commit: e32521f35f33897cd72892de393073b01ad963f1
workflow-type: tm+mt
source-wordcount: '1035'
ht-degree: 7%

---


# AEM 프로젝트 전형 {#aem-project-archetype}

AEM Project Tranype은 최소한의 모범 사례 기반 Adobe Experience Manager(AEM) 프로젝트를 웹 사이트의 시작점으로 만드는 Maven 템플릿입니다.

>[!TIP]
>
>최신 AEM 프로젝트 원형 [은 GitHub](https://github.com/adobe/aem-project-archetype)에서 찾을 수 있습니다.

## 리소스 {#resources}

* **원형 문서(이 문서):** 원형 아키텍처 및 다양한 모듈에 대한 개요입니다.
   * **[원형 사용: 원형 및 사용 가능한 모듈 사용에 대한](using.md)** 자세한 내용
   * **[ui.frontend:](uifrontend.md)** 프런트 엔드 빌드 모듈을 사용하는 방법
* 다음 자습서는 이 기본 유형을 기반으로 합니다.
   * **[WKND 사이트: ](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)** 새로운 웹 사이트를 시작하는 방법을 학습합니다.
   * **[WKND 단일 페이지 앱: ](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)** AEM에서 완전히 저작할 수 있는 반응형 또는 각도 웹 앱을 빌드하는 방법을 알아봅니다.

## 기능 {#features}

* **모범 사례: 모든 Adobe의 최신 권장 사례를 사용하여 사이트를** Bootstrap할 수 있습니다.
* **낮은 코드:** 템플릿을 편집하고 컨텐츠를 제작하며 CSS를 배포하며 사이트를 바로 라이브할 수 있습니다.
* **클라우드** 준비: 원하는 경우  [AEM을 클라우드 ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html) 서비스로 사용하여 며칠 만에 라이브하고 손쉽게 확장 및 유지 관리를 수행할 수 있습니다.
* **발송자:** 프로젝트는 속도와 보안을 보장하는  [발송자 ](https://docs.adobe.com/content/help/ko-KR/experience-manager-dispatcher/using/dispatcher.html) 구성만 사용하여 완료됩니다.
* **다중 사이트:** 필요한 경우 원형에서는  [다중 언어 및 다중 영역 설정에 대한 컨텐츠 구조를 생성합니다](https://docs.adobe.com/content/help/en/experience-manager-65/administering/introduction/msm.html).
* **핵심 구성 요소:** 작성자는 다양한 표준화된 구성 요소 [를 사용하여 거의 모든 레이아웃을 만들 수 있습니다](/help/introduction.md).
* **편집 가능한 템플릿:** 코드 [ 없이 거의 모든 ](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html)템플릿을 취합하고 작성자가 편집할 수 있는 항목을 정의합니다.
* **응답형 레이아웃: 템플릿** 또는 개별 페이지에서,  [요소가 정의된 중단점에 대해 리플로우 방식을 ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html) 정의합니다.
* **머리글 및 바닥글:** 구성 요소의  [로컬라이제이션 기능을 사용하여 코드 없이 구성 요소를 조합하고 현지화합니다](https://docs.adobe.com/content/help/ko-KR/experience-manager-core-components/using/get-started/localization.html).
* **스타일 시스템:** 작성자가 다른 스타일을 적용할 수 있도록 하여 사용자 지정 구성 요소를  [](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/style-system.html) 작성하지 마십시오.
* **프런트 엔드 빌드:** 프런트 엔드 개발자는 웹 팩, TypeScript 및 SASS를 사용하여  [AEM ](uifrontend.md#webpack-dev-server) 페이지 [를 만들고 클라이언트 ](uifrontend.md) 라이브러리를구축할 수 있습니다.
* **WebApp-Ready:** Reactor Angular [](uifrontend-react.md) 를 사용하는 사이트 [의 경우 ](uifrontend-angular.md)SPA  [SDK를 사용하여 앱](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/headless/spa/developing.html) 의 컨텍스트 작성 [ ](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)에 보관하십시오.
* **상거래 활성화:** 커머스 코어 구성 요소 [와 같은 상거래 솔루션](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/commerce/home.html) 과  [](https://magento.com/) AEM  [Commerce를 통합하려는 ](https://github.com/adobe/aem-core-cif-components)프로젝트의경우
* **예제 코드:** HelloWorld 구성 요소와 샘플 모델, 서블릿, 필터 및 스케줄러를 체크 아웃합니다.
* **오픈 소스:** 제대로 된 솔루션이 아닌 경우  [](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) 향상된 기능을 제공할 수 있습니다.

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

* [AEM에 대해 `aemVersion=cloud`을 Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html)으로 설정합니다.\
   [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) 또는 온-프레미스에 대해 `aemVersion=6.5.0`을 설정합니다.
핵심 구성 요소는 AEM용 OOTB를 Cloud Service으로 제공하므로 비 클라우드 aem 버전에 대해서만 코어 구성 요소 종속성이 추가됩니다.
* 웹 사이트 제목 및 구성 요소 그룹을 정의하려면 `appTitle="My Site"`을 조정합니다.
* `appId="mysite"`을 조정하여 클라이언트 라이브러리 이름은 물론 구성 요소, 구성 및 컨텐츠 폴더 이름을 정의합니다.
* `groupId="com.mysite"`을 조정하여 Maven groupId 및 Java 소스 패키지를 정의합니다.
* 사용 가능한 속성 목록을 조회하여 조정할 추가 사항이 있는지 확인합니다.

## 사용 가능한 속성

| 이름 | 기본값 | 설명 |
--------------------------|----------------|--------------------
| `appTitle` |  | 애플리케이션 제목은 웹 사이트 제목 및 구성 요소 그룹(예:`"My Site"`). |
| `appId` |  | 기술 이름은 클라이언트 라이브러리 이름(예:`"mysite"`). |
| `artifactId` | *`${appId}`* | 기본 마비안 아티팩트 ID(예:`"mysite"`). |
| `groupId` |  | 기본 마비안 그룹 ID(예:`"com.mysite"`). |
| `package` | *`${groupId}`* | Java 소스 패키지(예:`"com.mysite"`). |
| `version` | `1.0-SNAPSHOT` | 프로젝트 버전(예:`1.0-SNAPSHOT`). |
| `aemVersion` | `cloud` | Target AEM 버전(Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html);으로 [AEM의 경우 `cloud`일 수 있음)또는 `6.5.0`, [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) 또는 온-프레미스)용 `6.4.4`. |
| `sdkVersion` | `latest` | `aemVersion=cloud`SDK](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html) 버전을 지정할 수 있는 경우(예:`2020.02.2265.20200217T222518Z-200130`).[ |
| `includeDispatcherConfig` | `y` | `aemVersion` 값(`y` 또는 `n`일 수 있음)에 따라 클라우드 또는 AMS/on-premise용 디스패처 구성을 포함합니다. |
| `frontendModule` | `general` | 클라이언트 라이브러리를 생성하는 Webpack 프런트 엔드 빌드 모듈을 포함합니다(일반 사이트에 대해 `general` 또는 `none`일 수 있음).[SPA 편집기](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/headless/spa/editor-overview.html)를 구현하는 단일 페이지 앱의 경우 `angular` 또는 `react`일 수 있습니다. |
| `language` | `en` | 언어 코드(예:`en`, `deu`). |
| `country` | `us` | 국가 번호(ISO 3166-1)를 사용하여 콘텐츠 구조를 만드는 방법(예:`US`). |
| `singleCountry` | `y` | 언어 마스터 콘텐츠 구조를 포함합니다(`y` 또는 `n` 가능). |
| `includeExamples` | `n` | [구성 요소 라이브러리](https://www.aemcomponents.dev/) 예제 사이트(`y` 또는 `n`일 수 있음)를 포함합니다. |
| `includeErrorHandler` | `n` | 전체 인스턴스(`y` 또는 `n`일 수 있음)로 글로벌할 사용자 지정 404 응답 페이지를 포함합니다. |
| `includeCommerce` | `n` | [CIF 핵심 구성 요소](https://github.com/adobe/aem-core-cif-components) 종속성을 포함하고 해당 객체를 생성합니다. |
| `commerceEndpoint` |  | CIF에만 필요합니다. 사용할 상거래 시스템 GraphQL 서비스의 선택 끝점(예:`https://hostname.com/grapql`). |
| `datalayer` | `y` | [Adobe 클라이언트 데이터 레이어](/help/developing/data-layer/overview.md)와의 통합을 활성화합니다. |
| `amp` | `n` | 생성된 프로젝트 템플릿에 대해 [AMP](/help/developing/amp.md) 지원을 활성화합니다. |

## 시스템 요구 사항

| 원형 | AEM as a Cloud Service | AEM 6.5 | AEM 6.4 | Java SE | 마벤 |
|---------|---------|---------|---------|---------|---------|
| [24](https://github.com/adobe/aem-project-archetype/releases/tag/aem-project-archetype-24) | 지속적인 | 6.5.5.0+ | 6.4.8.1+ | 8, 11 | 3.3.9+ |

[AEM의 로컬 개발 환경을 Cloud Service SDK](https://docs.adobe.com/content/help/en/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html) 또는 이전 버전의 AEM](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html)에 대해 설정합니다.[

### 알려진 문제

Windows에서 실행하고 디스패처 구성을 생성하는 경우 관리자 권한 명령 프롬프트 또는 Linux용 Windows 하위 시스템에서 실행 중이어야 합니다([#329](https://github.com/adobe/aem-project-archetype/issues/329) 참조).

대화형 모드에서 원형 유형을 실행할 때(`-B` 매개 변수 없이) 기본값이 있는 속성은 변경할 수 없습니다. 단, 최종 확인을 취소할 때까지 마지막 값을 갖는 속성은 변경할 수 없습니다. 그런 다음 질문에 기본값이 있는 속성을 포함하는 질문을 반복합니다(
[TRANYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308)에 대한 자세한 내용을 살펴보십시오.

## {#further-reading} 추가 읽기

장점, 옵션 및 그 모듈의 작동 방식을 포함하여 원형 유형을 사용하는 방법에 대한 자세한 내용은 [Using the Tranype document.](using.md)

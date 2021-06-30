---
title: AEM 프로젝트 전형
description: AEM 기반 응용 프로그램용 프로젝트 템플릿
feature: 핵심 구성 요소, AEM 프로젝트 원형
role: Architect, Developer, Administrator
exl-id: 58994726-9b65-4035-9d45-60b745d577bb
source-git-commit: 8b3f98d5087ddca6928950daf2db1eb7728fa44e
workflow-type: tm+mt
source-wordcount: '1111'
ht-degree: 6%

---

# AEM 프로젝트 전형 {#aem-project-archetype}

AEM 프로젝트 원형 은 웹 사이트의 시작점으로 최소한의 우수 사례 기반 Adobe Experience Manager(AEM) 프로젝트를 만드는 Maven 템플릿입니다.

>[!TIP]
>
>최신 AEM 프로젝트 원형 [은 GitHub에서 찾을 수 있습니다.](https://github.com/adobe/aem-project-archetype)

## 리소스 {#resources}

* **Archetype 설명서(이 문서):** 원형 아키텍처 및 다른 모듈에 대한 개요.
   * **[Archetype 사용:](using.md)** 원형 및 사용 가능한 모듈 사용에 대한 자세한 내용
   * **[ui.frontend:](uifrontend.md)** 프런트 엔드 빌드 모듈을 사용하는 방법
* 다음 자습서는 이 기본 자습서를 기반으로 합니다.
   * **[WKND 사이트: ](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)** 새 웹 사이트를 시작하는 방법을 알아봅니다.
   * **[WKND 단일 페이지 앱: ](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)** AEM에서 완전히 권한이 부여된 React 또는 Angular 웹 앱을 빌드하는 방법을 알아봅니다.

## 기능 {#features}

* **우수 사례:** Adobe의 모든 최신 권장 지침으로 사이트를 Bootstrap합니다.
* **낮은 코드:** 템플릿을 편집하고, 콘텐츠를 만들고, CSS를 배포하며, 사이트가 라이브로 전환될 준비가 됩니다.
* **클라우드 준비:** 원하는 경우  [AEM as a Cloud ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html) Service를 사용하여 며칠 안에 라이브로 전환하고 확장성 및 유지 관리를 간소화할 수 있습니다.
* **Dispatcher:** 프로젝트는 속도 및 보안을  [ ](https://docs.adobe.com/content/help/ko-KR/experience-manager-dispatcher/using/dispatcher.html) 보장하는 Dispatcher 구성만 사용하여 완료됩니다.
* **다중 사이트:** 필요한 경우 원형 은  [다국어 및 다중 영역 설정에 대한 컨텐츠 구조를 생성합니다](https://docs.adobe.com/content/help/en/experience-manager-65/administering/introduction/msm.html).
* **핵심 구성 요소:** 작성자는 다양한 표준화된 구성 요소  [세트를 사용하여 거의 모든 레이아웃을 만들 수 있습니다](/help/introduction.md).
* **편집 가능한 템플릿:** 코드  [없이 거의 모든 템플릿을 어셈블하고 작성자가 편집할 수 있는 사항을 정의합니다](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html).
* **응답형 레이아웃:** 템플릿 또는 개별 페이지에서  [정의된 중단점에 대해 요소가 ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/responsive-layout.html) 리플로우되는 방식을 정의합니다.
* **머리글 및 바닥글:** 구성 요소의  [로컬라이제이션 기능을 사용하여 코드 없이 어셈블하고 현지화합니다](https://docs.adobe.com/content/help/ko-KR/experience-manager-core-components/using/get-started/localization.html).
* **스타일 시스템:** 작성자가 다른 스타일을  [적용할 수 있도록 하여 사용자 지정 구성 ](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/style-system.html) 요소를 빌드하지 마십시오.
* **프런트 엔드 빌드:** 프런트 엔드 개발자는 AEM 페이지 [를 ](uifrontend.md#webpack-dev-server) 조롱하고 Webpack, TypeScript 및 SASS를 사용하여 클라이언트 라이브러리 [ ](uifrontend.md) 를 빌드할 수 있습니다.
* **WebApp-Ready:** Reactor  [](uifrontend-react.md)  [Angular](uifrontend-angular.md)를 사용하는 사이트의 경우  [SPA ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/headless/spa/developing.html) SDK를 사용하여  [앱](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html) 컨텍스트 내 작성을 유지합니다.
* **상거래 활성화:**  [AEM Commerce를 ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/commerce/home.html) Magento와 같은 상거래 솔루션 [](https://magento.com/) 과 통합하려는  [프로젝트의 경우](https://github.com/adobe/aem-core-cif-components).
* **예제 코드:** HelloWorld 구성 요소와 샘플 모델, 서블릿, 필터 및 스케줄러를 체크아웃합니다.
* **오픈 소싱됨:** 필요한 내용이 아닌 경우 개선  [](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) 사항에 기여합니다.

## 사용량 {#usage}

프로젝트를 생성하려면 다음 명령줄을 필요에 따라 조정합니다.

```shell
mvn -B archetype:generate \
 -D archetypeGroupId=com.adobe.aem \
 -D archetypeArtifactId=aem-project-archetype \
 -D archetypeVersion=27 \
 -D appTitle="My Site" \
 -D appId="mysite" \
 -D groupId="com.mysite" \
```

* [AEM에 대해 `aemVersion=cloud`을 Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html)로 설정합니다.\
   [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) 또는 온-프레미스용으로 `aemVersion=6.5.0` 을 설정합니다.
핵심 구성 요소 종속성은 AEM용 OOTB를 Cloud Service으로 제공하므로 비 클라우드 aem 버전에 대해서만 추가됩니다.
* 웹 사이트 제목 및 구성 요소 그룹을 정의하려면 `appTitle="My Site"` 을 조정합니다.
* `appId="mysite"`을 조정하여 Maven artifactId, 구성 요소, 구성 및 콘텐츠 폴더 이름과 클라이언트 라이브러리 이름을 정의합니다.
* `groupId="com.mysite"` 을 조정하여 Maven groupId 및 Java 소스 패키지를 정의합니다.
* 사용 가능한 속성 목록을 조회하여 조정할 추가 정보가 있는지 확인합니다.

## 사용 가능한 속성 {#available-properties}

| 이름 | 기본값 | 설명 |
|---------------------------|----------------|--------------------|
| `appTitle` |  | 애플리케이션 제목 은 웹 사이트 제목 및 구성 요소 그룹(예:`"My Site"`) |
| `appId` |  | 기술 이름은 클라이언트 라이브러리 이름(예:`"mysite"`) |
| `artifactId` | *`${appId}`* | Base Maven 아티팩트 ID(예:`"mysite"`) |
| `groupId` |  | 기본 Maven 그룹 ID(예:`"com.mysite"`) |
| `package` | *`${groupId}`* | Java 소스 패키지(예:`"com.mysite"`) |
| `version` | `1.0-SNAPSHOT` | 프로젝트 버전(예:`1.0-SNAPSHOT`) |
| `aemVersion` | `cloud` | Target AEM 버전([AEM as a Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html)에 대해 `cloud`일 수 있음);또는 `6.5.0`, [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) 또는 온-프레미스용 `6.4.4`)입니다. |
| `sdkVersion` | `latest` | `aemVersion=cloud`[SDK](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html) 버전을 지정할 수 있으면(예: )`2020.02.2265.20200217T222518Z-200130`). |
| `includeDispatcherConfig` | `y` | `aemVersion` 값(`y` 또는 `n`일 수 있음)에 따라 클라우드 또는 AMS/on-premise에 대한 디스패처 구성을 포함합니다. |
| `frontendModule` | `general` | 일반 사이트의 클라이언트 라이브러리(`general` 또는 `none`일 수 있음)를 생성하는 Webpack 프런트 엔드 빌드 모듈이 포함되어 있습니다.[SPA Editor](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/headless/spa/editor-overview.html))를 구현하는 단일 페이지 앱의 경우 `angular` 또는 `react`일 수 있습니다. |
| `language` | `en` | 에서 컨텐츠 구조를 만들 언어 코드(ISO 639-1).`en`, `deu`). |
| `country` | `us` | 에서 컨텐츠 구조를 만들 국가 코드(ISO 3166-1).`US`) |
| `singleCountry` | `y` | 언어 마스터 컨텐츠 구조(`y` 또는 `n`일 수 있음)를 포함합니다. |
| `includeExamples` | `n` | [구성 요소 라이브러리](https://www.aemcomponents.dev/) 예제 사이트(`y` 또는 `n`일 수 있음)를 포함합니다. |
| `includeErrorHandler` | `n` | 전체 인스턴스(`y` 또는 `n`일 수 있음)에 전역되는 사용자 지정 404 응답 페이지를 포함합니다. |
| `includeCommerce` | `n` | [CIF 코어 구성 요소](https://github.com/adobe/aem-core-cif-components) 종속성을 포함하고 해당 아티팩트를 생성합니다. |
| `commerceEndpoint` |  | CIF에만 필요합니다. 사용할 상거래 시스템 GraphQL 서비스의 선택적 끝점(예:`https://hostname.com/grapql`) |
| `datalayer` | `y` | [Adobe 클라이언트 데이터 레이어](/help/developing/data-layer/overview.md)와의 통합을 활성화합니다. |
| `amp` | `n` | 생성된 프로젝트 템플릿에 대해 [AMP](/help/developing/amp.md) 지원을 사용하도록 설정합니다. |
| `enableDynamicMedia` | `n` | 프로젝트 정책 설정에서 기본 Dynamic Media 구성 요소를 활성화하고 핵심 이미지 구성 요소의 정책에서 Dynamic Media 기능을 활성화합니다. |
| `enableSSR` | `n` | 프런트엔드 프로젝트에 대해 SSR을 활성화하는 옵션 |

## 시스템 요구 사항 {#requirements}

| 원형 | AEM as a Cloud Service | AEM 6.5 | Java SE | Maven |
|---------|---------|---------|---------|---------|
| [28년](https://github.com/adobe/aem-project-archetype/releases/tag/aem-project-archetype-28) | 계속 | 6.5.7.0+ | 8,11 | 3.3.9+ |

[AEM as a Cloud Service SDK](https://docs.adobe.com/content/help/en/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html) 또는 이전 버전의 AEM](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html)에 대한 로컬 개발 환경을 설정합니다.[

### 알려진 문제 {#known-issues}

Windows에서 실행하고 디스패처 구성을 생성하는 경우 관리자 권한 명령 프롬프트 또는 Linux용 Windows 하위 시스템에서 실행해야 합니다( [#329](https://github.com/adobe/aem-project-archetype/issues/329) 참조).

대화형 모드(`-B` 매개 변수 없이)에서 원형 을 실행할 때 최종 확인이 취소되지 않는 한 기본값이 있는 속성을 변경할 수 없습니다. 그러면 질문에 기본값이 있는 속성을 포함하여 질문을 반복합니다( 참조)
[ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) 자세한 내용)

[Eclipse 문제로 인해 생성 스크립트 `archetype-post-generate.groovy`이 실행되지 않으므로 `File -> New -> Maven Project`으로 새 프로젝트를 시작할 때 Eclipse에서 이 원형 을 사용할 수 없습니다.](https://bugs.eclipse.org/bugs/show_bug.cgi?id=514993) 해결 방법은 위의 명령줄을 사용한 다음 Eclipse를 사용하는 것입니다  `File -> Import -> Existing Maven Project`.

## 추가 읽기 {#further-reading}

Archetype의 이점, 옵션 및 모듈 작동 방식 등 원형 사용에 대한 자세한 내용은 [Using the Archetype 문서](using.md)를 참조하십시오.

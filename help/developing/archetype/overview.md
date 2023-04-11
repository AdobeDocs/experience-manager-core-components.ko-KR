---
title: AEM Project Archetype
description: AEM 기반 애플리케이션용 프로젝트 템플릿
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 58994726-9b65-4035-9d45-60b745d577bb
source-git-commit: fac7c40919d2c31a8004bd1f47500ac44f99fb61
workflow-type: tm+mt
source-wordcount: '1192'
ht-degree: 100%

---

# AEM Project Archetype {#aem-project-archetype}

AEM Project Archetype은 Adobe Experience Manager(AEM) 프로젝트를 웹 사이트 시작 지점으로 만드는 최소한의 모범 사례 기반 Maven 템플릿입니다.

>[!TIP]
>
>최신 AEM Project Archetype은 [GitHub에서 확인할 수 있습니다.](https://github.com/adobe/aem-project-archetype)

## 리소스 {#resources}

* **Archetype 설명서(본 문서):** Archetype 아키텍처와 서로 다른 모듈을 대해 살펴봅니다.
   * **[Archetype 사용:](using.md)** Archetype 및 모듈 사용에 대해 자세히 알아보기
   * **[ui.frontend:](uifrontend.md)** 프론트엔드 빌드 모듈을 사용하는 방법
* **다음 튜토리얼은 이 Archetype에 따라 작성됩니다.**
   * **[WKND Site:](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)** 완전히 새로운 웹 사이트를 시작하는 방법에 대해 알아봅니다.
   * **[WKND Single Page App:](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)** AEM에서 전체 작성할 수 있는 대화형 또는 방사형 WebApp을 빌드하는 방법에 알아봅니다.

## 기능 {#features}

* **모범 관행:** Adobe 권장 최신 모범 사례를 사용하여 Bootstrap으로 사이트를 제작합니다.
* **로우 코드:** 템플릿을 편집하고, 콘텐츠를 제작하고 CSS를 배포하면 사이트 실행이 준비됩니다.
* **클라우드 기반:** 필요한 경우 [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html)를 사용하여 며칠 내에 사이트를 실행하고 간단히 확장 및 관리할 수 있습니다.
* **발송자:** 속도와 보안을 보장하는 [발송자 구성](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/dispatcher.html)만으로 프로젝트를 완료합니다.
* **다중 사이트:** 필요한 경우 Archetype은 [다국어 및 다중 지역 설정](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/msm/overview.html)용 콘텐츠 구조를 생성합니다.
* **핵심 구성 요소:** 작성자는 다목적 [세트의 표준화된 구성 요소](/help/introduction.md)를 사용하여 거의 모든 레이아웃을 제작할 수 있습니다.
* **편집 가능한 템플릿:** 코드 없이 거의 모든 [템플릿을 조합하고](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html) 작성자가 편집할 내용을 정의합니다.
* **반응형 레이아웃:** 템플릿 또는 개별 페이지에서 [정의된 중단점에 대한 요소를 재배치하는 방법](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/get-started/localization.html)을 정의합니다.
* **머리글 및 바닥글:** [구성 요소의 현지화 기능](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/get-started/localization.html)을 사용하여 코드 없이 이를 조합하고 현지화합니다.
* **스타일 시스템:** 작성자가 [다른 스타일을 적용](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/project-archetype/style-system.html)하면 사용자 정의 구성 요소를 빌드하지 마십시오.
* **프론트엔드 빌드:** 프론트엔드 개발자는 Webpack, TypeScript 및 SASS를 사용하여 [AEM을 복제](uifrontend.md#webpack-dev-server)하고 [클라이언트 라이브러리를 빌드](uifrontend.md)할 수 있습니다.
* **WebApp 기반:** 사이트에서 [반응형](uifrontend-react.md) 또는 [방사형 WebApp](uifrontend-angular.md)을 사용하는 경우 [SPA SDK](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/hybrid/developing.html)로 [상황에 맞게 앱 제작](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)을 유지할 수 있습니다.
* **Commerce 활성화됨:** 프로젝트에서 [상거래 핵심 구성 요소](https://github.com/adobe/aem-core-cif-components)를 사용하여 [AEM Commerce](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/home.html)와 상거래 솔루션(예: [Magento](https://magento.com/))을 통합하는 경우.
* **예제 코드:** HelloWorld 구성 요소와 샘플 모드, 서블릿, 필터 및 스케줄러 체크아웃.
* **오픈 소스:** 매출이 평소와 같지 않다면 자신의 성과를 [공개](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md)하십시오.

## 사용 {#usage}

프로젝트를 생성하려면 필요에 맞게 다음 명령줄을 조정해야 합니다.

```shell
mvn -B org.apache.maven.plugins:maven-archetype-plugin:3.2.1:generate \
 -D archetypeGroupId=com.adobe.aem \
 -D archetypeArtifactId=aem-project-archetype \
 -D archetypeVersion=XX \
 -D appTitle="My Site" \
 -D appId="mysite" \
 -D groupId="com.mysite" \
```

* `XX`를 최신 [Archetype 버전 번호로 대체합니다.](#requirements)
* [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html)에 대해 `aemVersion=cloud`를 설정합니다.\
   [Adobe 관리 서비스](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) 또는 온프레미스를 위한 `aemVersion=6.5.0`를 설정합니다.
AEM as a Cloud Service용 OOTB에 핵심 구성 요소가 제공되므로 AEM이 아닌 버전에는 핵심 구성 요소 종속성만 추가됩니다.
* `appTitle="My Site"`를 조정하여 웹 사이트 제목과 구성 요소 그룹을 정의합니다.
* `appId="mysite"`를 조정하여 Maven artifactId, 구성 요소 config 및 콘텐츠 폴더 이름과 클라이언트 라이브러리 이름을 정의합니다.
* `groupId="com.mysite"`를 조정하여 Maven groupId 및 Java 소스 패키지를 정의합니다.
* 조정할 추가 속성이 있는지 확인하려면 사용 가능한 속성 목록을 조회합니다.

## 사용 가능한 속성 {#available-properties}

| 이름 | 기본값 | 설명 |
|---------------------------|----------------|--------------------|
| `appTitle` |  | 웹 사이트 제목과 구성 요소 그룹(예: `"My Site"`)에 애플리케이션 제목을 사용합니다. |
| `appId` |  | 구성 요소, config 및 콘텐츠 폴더 이름과 클라이언트 라이브러리 이름(예: `"mysite"`)에 기술적 용어가 사용됩니다. |
| `artifactId` | *`${appId}`* | 기본 Maven 아티팩트 ID (예: `"mysite"`) |
| `groupId` |  | 기본 Maven 그룹 ID (예: `"com.mysite"`) 이 값은 [유효한 Java 패키지 이름](https://docs.oracle.com/javase/specs/jls/se6/html/packages.html#7.7)이어야 합니다. |
| `package` | *`${groupId}`* | Java 소스 패키지 (예: `"com.mysite"`) |
| `version` | `1.0-SNAPSHOT` | 프로젝트 버전 (예: `1.0-SNAPSHOT`) |
| `aemVersion` | `cloud` | 대상 AEM 버전 ([AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html?lang=ko-KR)나 `6.5.0`용 `cloud` 또는 [Adobe 관리 서비스](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams)나 온프레미스용 `6.4.4`일 수 있음) |
| `sdkVersion` | `latest` | `aemVersion=cloud` 한 개의 [SDK](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html) 버전이 지정될 경우 (예: `2020.02.2265.20200217T222518Z-200130`) |
| `includeDispatcherConfig` | `y` | `aemVersion`(`y` 또는 `n`일 수 있음)의 값에 따라 Cloud 또는 AMS/온프레미스용 발송자 구성을 포함합니다. |
| `frontendModule` | `general` | 클라이언트 라이브러리를 생성하는 Webpack 프론트엔드 빌드 모듈(일반 사이트용 `general` 또는 `none`일 수 있고, [SPA 편집기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/hybrid/editor-overview.html)를 구현하는 단일 페이지 앱용 `angular` 또는 `react`일 수 있음)을 포함합니다. |
| `language` | `en` | 다음 코드(예: `en`, `deu`)에서 콘텐츠 구조를 만드는 언어 코드(ISO 639-1). |
| `country` | `us` | 다음 코드(예: `US`)에서 콘텐츠 구조를 만드는 국가 코드(ISO 3166-1). |
| `singleCountry` | `y` | 언어 습득 콘텐츠 구조(`y` 또는 `n`일 수 있음)를 포함합니다. |
| `includeExamples` | `n` | [구성 요소 라이브러리](https://www.aemcomponents.dev/) 예시 사이트(`y` 또는 `n`일 수 있음)를 포함합니다. |
| `includeErrorHandler` | `n` | 전체 인스턴스 전역의 사용자 정의 404 반응형 페이지(`y` 또는 `n`일 수 있음)를 포함합니다. |
| `includeCommerce` | `n` | [CIF 핵심 구성 요소](https://github.com/adobe/aem-core-cif-components) 종속성을 포함하고 해당 아티팩트를 생성합니다. |
| `commerceEndpoint` |  | CIF에만 필요합니다. 옵션: 아직 사용하지 않은 상거래 시스템 GraphQ 서비스 엔드포인트(예: `https://hostname.com/grapql`). |
| `includeFormscommunications` | `n` | [Forms 핵심 구성 요소](https://github.com/adobe/aem-core-forms-components) 종속성, 템플릿, 양식 데이터 모델, 테마를 포함하며 Forms 커뮤니케이션 프로그램에 해당하는 아티팩트를 생성합니다. |
| `includeFormsenrollment` | `n` | [Forms 핵심 구성 요소](https://github.com/adobe/aem-core-forms-components) 종속성, 템플릿, 양식 데이터 모델, 테마를 포함하며 Forms 등록 프로그램에 해당하는 아티팩트를 생성합니다. |
| `sdkFormsVersion` | `latest` | `aemVersion=cloud` 및 `includeFormsenrollment=y` 또는 `includeFormscommunications=y` 중 하나이면 Forms SDK 버전을 지정할 수 있습니다(예: `2020.12.17.02`). |
| `datalayer` | `y` | [Adobe 클라이언트 데이터 레이어](/help/developing/data-layer/overview.md)와의 통합 기능을 활성화합니다. |
| `amp` | `n` | 생성된 프로젝트 템플릿에 대한 [AMP](/help/developing/amp.md) 지원을 활성화합니다. |
| `enableDynamicMedia` | `n` | 프로젝트 정책 설정으로 기초 Dynamic Media 구성 요소를 활성화하고 핵심 이미지 구성 요소 정책으로 Dynamic Media 기능을 작동합니다. |
| `enableSSR` | `n` | 프론트엔드 프로젝트용 SSR을 활성화하는 옵션 |
| `precompiledScripts` | `n` | `ui.apps`의 서버측 스크립트를 [미리 컴파일](/help/developing/archetype/precompiled-bundled-scripts.md)하고 `ui.apps` 프로젝트에서 빌드에 보조 번들 아티팩트로 스크립트를 첨부하는 옵션. `aemVersion`을 `cloud`로 설정해야 합니다. |
| `includeFormsheadless` | `n` | [Forms 핵심 구성 요소](https://github.com/adobe/aem-core-forms-components) 종속성, `ui.frontend.react.forms.af` 및 헤드리스 아티팩트를 포함합니다. |

## 시스템 요구 사항 {#requirements}

| Archetype | AEM as a Cloud Service | AEM 6.5 | Java SE | Maven |
|---------|---------|---------|---------|---------|
| [41](https://github.com/adobe/aem-project-archetype/releases/tag/aem-project-archetype-41) | Continual | 6.5.7.0+ | 8, 11 | 3.3.9+ |

[AEM as a Cloud Service SDK](https://experienceleague.adobe.com/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html?lang=ko-KR) 또는 [기존 버전의 AEM](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html)용 로컬 개발 환경을 설정합니다.

### 알려진 문제 {#known-issues}

Windows에서 실행하고 발송자 구성을 생성하는 경우 상위 명령 프롬프트나 Linux용 Windows 하위 시스템에서 실행해야 합니다([#329](https://github.com/adobe/aem-project-archetype/issues/329) 참조).

대화형 모드로 Archetype을 실행할 때(`-B` 매개변수가 없음), 최종 확인이 종료되지 않으면 기본값이 포함된 속성을 변경할 수 없습니다. 그런 다음 기본값이 포함된 속성이 질문에 기재되면 질문이 반복됩니다(자세한 내용은 [ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) 참조).

`File -> New -> Maven Project`로 새 프로젝트를 시작할 때 [Eclipse 문제로 사후 생성 스크립트`archetype-post-generate.groovy`를 실행할 수 없기 때문에 Eclipse에서 이 Archetype을 사용할 수 없습니다.](https://bugs.eclipse.org/bugs/show_bug.cgi?id=514993) 문제를 해결하려면 상기 명령줄을 사용한 다음 Eclipse에서 `File -> Import -> Existing Maven Project`를 사용합니다.

## 추가 참조 {#further-reading}

Archetype의 혜택, 옵션 및 모듈이 작동하는 방식 등 Archetype 사용에 대한 자세한 내용은 [Archetype 문서 사용](using.md)을 참조하십시오.

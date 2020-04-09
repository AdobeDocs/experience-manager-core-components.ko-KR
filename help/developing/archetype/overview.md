---
title: AEM 프로젝트 전형
description: AEM 기반 응용 프로그램용 프로젝트 템플릿
translation-type: tm+mt
source-git-commit: 2faa092a075ab0512e9bd5654884534936c0ad53

---


# AEM 프로젝트 전형 {#aem-project-archetype}

AEM Project Tranype은 최소한의 우수 사례 기반 AEM(Adobe Experience Manager) 프로젝트를 웹 사이트의 시작점으로 만드는 Maven 템플릿입니다.

>[!TIP]
>
>최신 AEM Project Tranype [은 GitHub에서 찾을 수 있습니다](https://github.com/adobe/aem-project-archetype).

## 리소스 {#resources}

* **원형 문서(이 문서):** 원형형 아키텍처 및 다른 모듈에 대한 개요.
   * **[원형 사용:](using.md)**사용 가능한 원형과 모듈 사용에 대한 자세한 내용
   * **[ui.front:](uifrontend.md)**프런트 엔드 빌드 모듈을 사용하는 방법
* 다음 자습서는 이 기본 유형을 기반으로 합니다.
   * **[WKND 사이트:](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)**새로운 웹 사이트를 시작하는 방법을 살펴보십시오.
   * **[WKND 단일 페이지 앱:](https://helpx.adobe.com/experience-manager/kt/sites/using/getting-started-spa-wknd-tutorial-develop.html)**AEM 파섹

## 기능 {#features}

* **모범 사례:** Bootstrap your site with all of Adobe&#39;s latest recommended practices.
* **낮은 코드:** 템플릿을 편집하고 컨텐츠를 제작하며 CSS를 배포할 수 있으며 사이트를 바로 라이브할 수 있습니다.
* **클라우드 지원:** 원하는 경우 AEM을 [클라우드 서비스로](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html) 사용하여 며칠 만에 라이브하고 손쉽게 확장 및 유지 관리할 수 있습니다.
* **발송자:** 프로젝트는 속도와 보안을 보장하는 [Dispatcher 구성을](https://docs.adobe.com/content/help/en/experience-manager-dispatcher/using/dispatcher.html) 통해서만 완료됩니다.
* **다중 사이트:** 필요한 경우 원형에서는 [다중 언어 및 다중 영역 설정에](https://docs.adobe.com/content/help/en/experience-manager-65/administering/introduction/msm.html)대한 컨텐츠 구조를 생성합니다.
* **핵심 구성 요소:** 작성자는 다용도의 표준 구성 요소 [세트를 사용하여 거의 모든 레이아웃을 만들 수 있습니다](/help/introduction.md).
* **편집 가능한 템플릿:** 코드 [없이 거의 모든](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html)템플릿을 취합하고 작성자가 편집할 수 있는 항목을 정의할 수 있습니다.
* **반응형 레이아웃:** 템플릿 또는 개별 페이지에서 정의된 중단점에 대해 요소가 리플로우되는 [방식을](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/responsive-layout.html) 정의합니다.
* **머리글 및 바닥글:** 구성 요소의 [로컬라이제이션 기능을 사용하여 코드를 작성하지 않고도 구성 요소를 취합하고 현지화할 수 있습니다](https://docs.adobe.com/content/help/ko-KR/experience-manager-core-components/using/get-started/localization.html).
* **스타일 시스템:** 작성자가 다른 스타일을 [](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/style-system.html) 적용할 수 있도록 허용하여 사용자 정의 구성 요소를 만들지 마십시오.
* **프런트 엔드 빌드:** 프런트 엔드 디바이스는 [웹 팩, TypeScript 및 SASS를 사용하여 AEM 페이지를](uifrontend.md#webpack-dev-server) 만들고 클라이언트 라이브러리를 [](uifrontend.md) 만들 수 있습니다.
* **WebApp-Ready:** React 또는 Angular를 [사용하는](uifrontend-react.md) 사이트의 [경우](uifrontend-angular.md)SPA SDK [를](https://docs.adobe.com/content/help/en/experience-manager-64/developing/headless/spas/spa-architecture.html) 사용하여 앱의 컨텍스트 [](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)작성에서 유지할 수 있습니다.
* **예제 코드:** HelloWorld 구성 요소와 샘플 모델, 서버, 필터 및 스케줄러를 체크아웃합니다.
* **오픈 소스:** 만약 어떤 것이 그렇게 될 수 없다면, [여러분의 개선점을](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) 기부하세요!

## 사용량

프로젝트를 생성하려면 필요에 따라 다음 명령줄을 조정합니다.

```
mvn -B archetype:generate \
 -D archetypeGroupId=com.adobe.granite.archetypes \
 -D archetypeArtifactId=aem-project-archetype \
 -D archetypeVersion=23 \
 -D aemVersion=cloud \
 -D appTitle="My Site" \
 -D appId="mysite" \
 -D groupId="com.mysite" \
 -D frontendModule=general \
 -D includeExamples=n
```

* Set `aemVersion=cloud` for [AEM as a Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html);\
   Adobe Managed `aemVersion=6.5.0` Services [](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams)또는 온프레미스 설정
핵심 구성 요소는 CloudService로 AEM용 OOTB가 제공되므로 비 클라우드 aem 버전에 대해서만 추가됩니다.
* 웹 사이트 제목 및 구성 요소 그룹을 `appTitle="My Site"` 정의하려면 조정합니다.
* Maven artifactId, 구성 요소, 구성 및 콘텐트 폴더 이름, 클라이언트 라이브러리 이름을 정의하려면 `appId="mysite"` 조정합니다.
* Maven groupId 및 Java 소스 패키지를 `groupId="com.mysite"` 정의하기 위해 조정합니다.
* 사용 가능한 속성 목록을 조회하여 조정할 추가 사항이 있는지 확인합니다.

## 사용 가능한 속성

| 이름 | 기본값 | 설명 |
--------------------------|----------------|--------------------
| `appTitle` |  | 애플리케이션 제목은 웹 사이트 제목 및 구성 요소 그룹(예: `"My Site"`). |
| `appId` |  | 기술 이름은 클라이언트 라이브러리 이름(예: `"mysite"`). |
| `artifactId` | *`${appId}`* | 기본 Maven 아티팩트 ID(예: `"mysite"`). |
| `groupId` |  | 기본 Maven 그룹 ID(예: `"com.mysite"`). |
| `package` | *`${groupId}`* | Java 소스 패키지(예: `"com.mysite"`). |
| `version` | `1.0-SNAPSHOT` | 프로젝트 버전(예: `1.0-SNAPSHOT`). |
| `aemVersion` | `6.5.0` | Target AEM 버전(클라우드 서비스로 AEM `cloud` 에 [사용할 수 있음](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html);또는 `6.5.0`Adobe Managed `6.4.4`Services `6.3.3` 또는 [온프레미스](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) )를 사용할 수 있습니다. |
| `sdkVersion` | `latest` | SDK `aemVersion=cloud` 버전을 [](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html) 지정할 수 있는 경우(예: `2020.02.2265.20200217T222518Z-200130`). |
| `includeDispatcherConfig` | `y` | 값(또는 일 수 있음)에 따라 클라우드 또는 AMS/on-premise용 디스패처 구성을 `aemVersion``y` `n`포함합니다. |
| `frontendModule` | `none` | 클라이언트 라이브러리를 생성하는 Webpack 프런트 엔드 빌드 모듈이 포함되어 있습니다(일반 사이트일 수도 `general` 있고 `none` 사이트용일 수도 있음).은 SPA 편집기를 구현하는 단일 페이지 `angular` 앱이거나 `react` 단일 페이지 [앱일 수 있습니다](https://docs.adobe.com/content/help/en/experience-manager-65/developing/headless/spas/spa-overview.html). |
| `languageCountry` | `en_us` | 컨텐츠 구조를 만드는 언어 및 국가 코드(예: `en_us`). |
| `singleCountry` | `y` | 언어 마스터 컨텐츠 구조( `y`또는 `n`일 수 있음)를 포함합니다. |
| `includeExamples` | `y` | 구성 요소 [라이브러리](https://www.aemcomponents.dev/) 예제 사이트( `y`또는 `n`)를 포함합니다. |
| `includeErrorHandler` | `n` | 전체 인스턴스( `y` 또는 `n`일 수 있음)에 대해 글로벌할 사용자 지정 404 응답 페이지를 포함합니다. |

## 시스템 요구 사항

| 원형 | 클라우드 서비스로서의 AEM | AEM 6.5 | AEM 6.4 | AEM 6.3 | Java SE | Maven |
---------|---------|---------|---------|---------|---------|---------
| [23](https://github.com/adobe/aem-project-archetype/releases/tag/aem-project-archetype-23) | 연속 | 6.5.0.0+ | 6.4.4.0+ | 6.3.3.4+ | 8, 11 | 3.3.9+ |

AEM에 대한 로컬 개발 환경을 클라우드 서비스 [SDK](https://docs.adobe.com/content/help/en/experience-manager-learn/cloud-service/local-development-environment-set-up/overview.html) 또는 [이전 버전의 AEM용으로 설정하십시오](https://docs.adobe.com/content/help/en/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html).

### 알려진 문제

Windows에서 실행하고 디스패처 구성을 생성할 때는 관리자 권한 명령 프롬프트 또는 Linux용 Windows 하위 시스템에서 실행해야 합니다( [#329 참조](https://github.com/adobe/aem-project-archetype/issues/329)).

매개 변수 없이 대화형 모드에서 원형형을 실행할 때 최종 확인을 무시하지 않으면 기본값이 있는 속성을 변경할 수 없습니다. 그러면 질문에 기본값이 있는 속성을 포함하여 질문을 반복하게 됩니다(자세한 내용은 `-B` TRANYPE-308[참조](https://issues.apache.org/jira/browse/ARCHETYPE-308) ).

## 추가 읽기 {#further-reading}

장점, 옵션, 모듈 작동 방식 등 전형 사용에 대한 자세한 내용은 Using the Tranype [문서를 참조하십시오.](using.md)
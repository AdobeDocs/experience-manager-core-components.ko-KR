---
title: AEM Project Archetype 사용
description: AEM Project Archetype에 대한 자세한 사용량 지침
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: a3978d8b-4904-42aa-9ee2-9c1f884327bb
source-git-commit: 017790c5a0e53ba6203a5c3d5ddebcce9c00cb01
workflow-type: tm+mt
source-wordcount: '2193'
ht-degree: 93%

---

# AEM Project Archetype {#aem-project-archetype}

AEM Project Archetype은 사용자 자신의 AEM 프로젝트의 시작점으로서 모범 사례 기반 Adobe Experience Manager 프로젝트를 생성합니다. 이 Archetype 사용 시 제공되는 속성을 사용하여 이 프로젝트의 전체 이름을 지정하고 특정 옵션 기능을 제어할 수 있습니다.

## 이 Archetype을 사용하는 이유 {#why-use-the-archetype}

AEM Project Archetype을 사용하여 몇 번의 키 입력만으로 모범 사례 기반 AEM 프로젝트를 빌드할 수 있습니다. Archetype을 사용하여, 결과 프로젝트가 최소화되도록 모든 콘텐츠를 활용하고 맨 위에서 프로젝트를 빌드하고 확장하도록 AEM의 [주요 기능](#what-you-get)을 모두 구현합니다.

여러 요소들이 성공적인 AEM 프로젝트에 투입되지만 AEM Project Archetype 사용은 AEM 프로젝트에서 적극 권장되는 매우 기초적인 방법입니다.

## 시작하기 {#getting-started}

Project Archetype을 통해 AEM에서 개발 시작하기가 수월해집니다. 여러 방식으로 첫 단계를 수행할 수 있습니다.

* WKND 튜토리얼 - Archetype을 활용하는 방법 등 도입된 AEM 개발에 대한 실용적인 예제(Archetype 사용을 통한 간단한 프로젝트 구현하기에 대한 안내)를 알아보려면 [AEM Sites 시작하기](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html) - WKND 튜토리얼을 참조하십시오.
* WKND 이벤트 튜토리얼 - AEM에서 단일 페이지 애플리케이션(SPA) 개발에 관심이 있다면 전용 [WKND 이벤트 튜토리얼](https://helpx.adobe.com/kr/experience-manager/kt/sites/using/getting-started-spa-wknd-tutorial-develop.html)에 대해 자세히 알아보십시오.
* 다운로드 후 바로 시작해 보십시오. - GitHub에 제공하는 현재 Project Archetype을 간편하게 다운로드하고 [아래의 간소한 단계에 따라](#how-to-use-the-archetype) 첫 번째 프로젝트를 제작할 수 있습니다.

## Archetype을 통해 누릴 수 있는 혜택 {#what-you-get}

AEM Project Archetype은 모듈로 구성됩니다.

* **[core](core.md)**: 모든 핵심 기능(OSGi 서비스, 리스너 및 스케줄러 등)과 구성 요소 관련 Java 코드(서블릿 및 요청 필터 등)가 포함된 Java 번들입니다.
* **[it.tests](ittests.md)**: Java 기반 통합 테스트입니다.
* **[ui.apps](uiapps.md)**: 일부 프로젝트 `/apps` 및 `/etc`(예: JS 및 CSS Clientlib, 구성 요소 및 템플릿)가 포함됩니다.
* **[ui.content](uicontent.md)**: ui.apps 모듈에서 구성 요소를 사용하는 샘플 콘텐츠가 포함됩니다.
* **ui.config**: 프로젝트의 실행 모드별 OSGi configs가 포함됩니다.
* **[ui.frontend.general](uifrontend.md)**: **(선택 사항)** 일반 Webpack 기반 프론트엔드 빌드 모드 사용에 필요한 아티팩트가 포함됩니다.
* **[ui.frontend.react](uifrontend-react.md)**: **(선택 사항)** React에 따라 Archetype을 사용하여 SPA 프로젝트를 만들 때 필요한 아티팩트가 포함됩니다.
* **[ui.frontend.react](uifrontend-angular.md)**: **(선택 사항)** Angular에 따라 Archetype을 사용하여 SPA 프로젝트를 만들 때 필요한 아티팩트가 포함됩니다.
* **[ui.tests](uitests.md)**: Selenium 기반 UI 테스트가 포함됩니다.
* **all**: 공급업체 종속성 등 컴파일된 모든 모듈(번들 및 콘텐츠 패키지)을 임베드하는 단일 콘텐츠 패키지입니다.
* **analyse**: 프로젝트에서 AEM as a Cloud Service 배포를 다시 확인하는 분석을 실행합니다.

![](/help/assets/archetype-structure.png)

애플리케이션, 콘텐츠와 필요한 OSGi 번들을 표시하는 콘텐츠 패키지로서 Maven에 표시된 AEM Archetype 모듈을 AEM으로 배포합니다.

## Archetype을 사용하는 방법 {#how-to-use-the-archetype}

Archetype을 사용하려면 먼저 [이전에 설명한](#what-you-get) 로컬 파일의 모듈을 생성하는 프로젝트를 만들어야 합니다. 프로젝트 생성의 일부로 프로젝트 이름, 버전 등 다수의 프로젝트 속성을 정의할 수 있습니다.

Maven과 함께 프로젝트를 빌드하면 AEM으로 배포 가능한 아티팩트(패키지 및 OSGi 번들)를 제작할 수 있습니다. 추가 Maven 명령 및 프로필을 사용하여 프로젝트 아티팩트를 AEM으로 배포할 수 있습니다.

### 프로젝트 제작 {#create-project}

시작하려면 [AEM Eclipse 확장 기능](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developer-tools/eclipse.html)을 최대한 활용하고, 새 프로젝트 마법사를 따라 **AEM 샘플 멀티 모듈 프로젝트를 선택하여** 릴리스된 Archetype 버전을 사용할 수 있습니다.

Maven을 바로 호출할 수도 있습니다.

```shell
mvn -B archetype:generate \
 -D archetypeGroupId=com.adobe.aem \
 -D archetypeArtifactId=aem-project-archetype \
 -D archetypeVersion=XX \
 -D aemVersion=cloud \
 -D appTitle="My Site" \
 -D appId="mysite" \
 -D groupId="com.mysite" \
 -D frontendModule=general \
 -D includeExamples=n
```

* `XX`를 [최신 AEM Project Archetype의 버전 번호](https://github.com/adobe/aem-project-archetype/blob/master/VERSIONS.md)로 설정합니다.
* [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html)에 대해 `aemVersion=cloud`를 설정합니다.\
   [Adobe 관리 서비스](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) 또는 온프레미스를 위한 `aemVersion=6.5.0`를 설정합니다.
AEM as a Cloud Service용 OOTB에 핵심 구성 요소가 제공되므로 AEM이 아닌 버전에는 핵심 구성 요소 종속성만 추가됩니다.
* `appTitle="My Site"`를 조정하여 웹 사이트 제목과 구성 요소 그룹을 정의합니다.
* `appId="mysite"`를 조정하여 Maven artifactId, 구성 요소 config 및 콘텐츠 폴더 이름과 클라이언트 라이브러리 이름을 정의합니다.
* `groupId="com.mysite"`를 조정하여 Maven groupId 및 Java 소스 패키지를 정의합니다.
* 조정할 추가 속성이 있는지 확인하려면 사용 가능한 속성 목록을 조회합니다.

>[!NOTE]
>
>repo.adobe.com을 maven build process로 자동 추가하려면 `adobe-public`프로필을 Maven`settings.xml` 파일로 추가하는 것이 좋습니다.
>
>예제 POM은 [여기에서 찾을 수 있습니다](https://helpx.adobe.com/kr/experience-manager/kb/SetUpTheAdobeMavenRepository.html).

### 속성 {#properties}

Archetype을 사용하여 프로젝트를 제작할 때 다음 속성을 사용할 수 있습니다.

| 이름 | 기본값 | 설명 |
|---------------------------|----------------|--------------------|
| `appTitle` |  | 웹 사이트 제목과 구성 요소 그룹(예: `"My Site"`)에 애플리케이션 제목을 사용합니다. |
| `appId` |  | 구성 요소, config 및 콘텐츠 폴더 이름과 클라이언트 라이브러리 이름(예: `"mysite"`)에 기술적 용어가 사용됩니다. |
| `artifactId` | *`${appId}`* | 기본 Maven 아티팩트 ID(예: `"mysite"`). |
| `groupId` |  | 기본 Maven 그룹 ID(예: `"com.mysite"`). |
| `package` | *`${groupId}`* | Java 소스 패키지(예: `"com.mysite"`). |
| `version` | `1.0-SNAPSHOT` | 프로젝트 버전(예: `1.0-SNAPSHOT`) |
| `aemVersion` | `cloud` | 대상 AEM 버전([AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html)나 `6.5.0`용 `cloud` 또는 [Adobe 관리 서비스](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams)나 온프레미스용 `6.4.4`일 수 있음) |
| `sdkVersion` | `latest` | `aemVersion=cloud` 한 개의 [SDK](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html) 버전이 지정될 경우(예: `2020.02.2265.20200217T222518Z-200130`) |
| `includeDispatcherConfig` | `y` | `aemVersion`(`y` 또는 `n`일 수 있음)의 값에 따라 Cloud 또는 AMS/온프레미스용 발송자 구성을 포함합니다. |
| `frontendModule` | `general` | 클라이언트 라이브러리를 생성하는 Webpack 프론트엔드 빌드 모듈(일반 사이트용 `general` 또는 `none`일 수 있고, [SPA 편집기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/headless/spa/editor-overview.html)를 구현하는 단일 페이지 앱용 `angular` 또는 `react`일 수 있음)을 포함합니다. |
| `language` | `en` | 다음 코드(예: `en`, `deu`)에서 콘텐츠 구조를 만드는 언어 코드(ISO 639-1). |
| `country` | `us` | 다음 코드(예: `US`)에서 콘텐츠 구조를 만드는 국가 코드(ISO 3166-1). |
| `singleCountry` | `y` | 언어 습득 콘텐츠 구조(`y` 또는 `n`일 수 있음)를 포함합니다. |
| `includeExamples` | `n` | [구성 요소 라이브러리](https://www.aemcomponents.dev/) 예시 사이트(`y` 또는 `n`일 수 있음)를 포함합니다. |
| `includeErrorHandler` | `n` | 전체 인스턴스 전역의 맞춤형 404 반응형 페이지(`y` 또는 `n`일 수 있음)를 포함합니다. |
| `includeCommerce` | `n` | [CIF 핵심 구성 요소](https://github.com/adobe/aem-core-cif-components) 종속성을 포함하고 해당 아티팩트를 생성합니다. |
| `commerceEndpoint` |  | CIF에만 필요합니다. 옵션: 아직 사용하지 않은 상거래 시스템 GraphQ 서비스 끝점(예: `https://hostname.com/grapql`). |
| `datalayer` | `y` | [Adobe 클라이언트 데이터 레이어](/help/developing/data-layer/overview.md)와의 통합 기능을 활성화합니다. |
| `amp` | `n` | 생성된 프로젝트 템플릿에 대한 [AMP](/help/developing/amp.md) 지원을 활성화합니다. |
| `enableDynamicMedia` | `n` | 프로젝트 정책 설정으로 기초 Dynamic Media 구성 요소를 활성화하고 핵심 이미지 구성 요소 정책으로 Dynamic Media 기능을 작동합니다. |
| `enableSSR` | `n` | 프론트엔드 프로젝트용 SSR을 활성화하는 옵션 |
| `precompiledScripts` | `n` | [서버측 스크립트를 `ui.apps`에서 미리 컴파일하고 `ui.apps` 프로젝트에서 두 번째 번들 아티팩트로 빌드에 첨부하는 옵션입니다. ](/help/developing/archetype/precompiled-bundled-scripts.md) `aemVersion` 를 로 설정해야  `cloud`합니다. |

>[!NOTE]
>
> 대화형 모드에서 Archetype을 처음 실행하면 기본값을 가진 속성을 변경할 수 없습니다(자세한 내용은 [ARCHETYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) 참조). 끝부분의 속성 확인이 거부되고 질문이 반복되거나 명령줄의 매개 변수를 전달하면 값이 변경될 수 있습니다(예: `-DoptionIncludeExamples=n`).

>[!NOTE]
>
>Windows에서 실행하고 발송자 구성을 생성하는 경우 상위 명령 프롬프트나 Linux용 Windows 하위 시스템에서 실행해야 합니다([문제 329](https://github.com/adobe/aem-project-archetype/issues/329) 참조).

### 프로필 {#profiles}

`mvn install` 실행 시 생성된 Maven 프로젝트는 서로 다른 배포 프로필을 지원합니다.

| 프로필 ID | 설명 |
| --------------------------|------------------------------|
| `autoInstallBundle` | maven-sling-plugin이 포함된 핵심 번들을 Felix 콘솔에 설치합니다. |
| `autoInstallPackage` | content-package-maven-plugin이 포함된 ui.content 및 ui.apps 콘텐츠 패키지를 패키지 매니저에 설치하여 localhost, port 4502에 작성자 인스턴스를 기본 설정합니다. `aem.host` 및 `aem.port` 사용자 정의 속성으로 된 호스트 이름과 포트를 변경할 수 있습니다. |
| `autoInstallPackagePublish` | content-package-maven-plugin이 포함된 ui.content 및 ui.apps 콘텐츠 패키지를 패키지 매니저에 설치하여 localhost, port 4503에 게시 인스턴스를 기본 설정합니다. `aem.host` 및 `aem.port` 사용자 정의 속성으로 된 호스트 이름과 포트를 변경할 수 있습니다. |
| `autoInstallSinglePackage` | content-package-maven-plugin이 포함된 `all` 콘텐츠 패키지를 패키지 매니저에 설치하여 localhost, port 4502에 작성자 인스턴스를 기본 설정합니다. `aem.host` 및 `aem.port` 사용자 정의 속성으로 된 호스트 이름과 포트를 변경할 수 있습니다. |
| `autoInstallSinglePackagePublish` | content-package-maven-plugin이 포함된 `all` 콘텐츠 패키지를 패키지 매니저에 설치하여 localhost, port 4503에 게시 인스턴스를 기본 설정합니다. `aem.host` 및 `aem.port` 사용자 정의 속성으로 된 호스트 이름과 포트를 변경할 수 있습니다. |
| `integrationTests` | AEM 인스턴스에 제공된 통합 테스트를 실행합니다(`verify` 단계만 해당). |
| `precompiledScripts` | `precompiledScripts` 속성이 `y`로 설정된 상태에서 프로젝트가 생성될 때 자동으로 정의됩니다. 이 프로필은 기본적으로 활성화되어 있으며 `ui.apps` 내에 OSGi 번들을 생성하며 이 번들은 사전 컴파일된 스크립트가 `all` 컨텐츠 패키지에 포함됩니다. 이 프로필은 `-DskipScriptPrecompilation=true`으로 비활성화할 수 있습니다. |

### 빌드 및 설치 {#building-and-installing}

모든 모듈을 빌드하려면 프로젝트 루트 디렉터리를 실행하고 다음 Maven 명령을 따릅니다.

```shell
mvn clean install
```

AEM 인스턴스가 실행 중인 경우 다음 Maven 명령을 사용하여 전체 프로젝트를 빌드 및 패키징하고 AEM에 배포할 수 있습니다.

```shell
mvn clean install -PautoInstallPackage
```

게시 인스턴스로 배포하려면 이 명령을 실행합니다.

```shell
mvn clean install -PautoInstallPackagePublish
```

또는 게시 인스턴스로 배포하려면 이 명령을 실행합니다.

```shell
mvn clean install -PautoInstallPackage -Daem.port=4503
```

또는 번들만 작성자로 배포하려면 이 명령을 실행합니다.

```shell
mvn clean install -PautoInstallBundle
```

## 상위 POM {#parent-pom}

프로젝트 루트(`<src-directory>/<project>/pom.xml`)의 `pom.xml`는 상위 POM이라고 합니다. 이는 프로젝트 구조를 유도하고 프로젝트에 대한 종속성 및 특정 전역 속성을 관리합니다.

### 전역 프로젝트 속성 {#global-properties}

상위 POM의 `<properties>` 섹션은 AEM 인스턴스에서 프로젝트를 구현하는 데 중요한 몇 가지 전역 속성(예: 사용자 이름/암호, 호스트 이름/포트 등)을 정의합니다.

이 속성을 설정하여 로컬 AEM 인스턴스로 배포합니다. 이는 개발자가 수행할 수 있는 가장 일반적인 빌드입니다. 작성자 인스턴스와 게시 인스턴스에 배포되는 속성이 있습니다. 여기서 자격 증명을 설정하여 AEM 인스턴스를 인증합니다. 기본 admin:admin 자격 증명을 사용합니다.

상위 수준의 환경에 배포할 때 이러한 속성이 재정의될 수 있도록 설정합니다. 이러한 방식으로 POM 파일은 변경될 수 없지만 `aem.host` 및 `sling.password`와 같은 변수는 다음 명령줄 인수를 통해 재정의될 수 있습니다.

```shell
mvn -PautoInstallPackage clean install -Daem.host=production.hostname -Dsling.password=productionpasswd
```

### 모듈 구조 {#module-structure}

상위 POM의 `<modules>` 섹션은 프로젝트가 빌드할 모듈을 정의합니다. 기본적으로 프로젝트는 [이전에 정의된 표준 모듈](#what-you-get)(ore, ui.apps, ui.content, ui.tests 및 it.launcher 등)을 빌드합니다. 프로젝트가 커지면 언제든지 모듈을 추가할 수 있습니다.

### 종속성 {#dependencies}

상위 POM의 `<dependencyManagement>` 섹션은 프로젝트에 사용되는 종속성과 API 버전을 모두 정의합니다. 상위 POM에서 버전을 관리해야 합니다. core 및 ui.apps 등 하위 모듈에는 버전 정보가 제외되어야 합니다.

#### Uber-Jar {#uber-jar}

주요 종속성 중 하나는 [AEM Java API Jar](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html)입니다. AEM 버전용 단일 종속성 목록이 있는 모든 AEM API가 여기에 포함됩니다.

>[!NOTE]
>
>AEM의 대상 버전에 일치하는 uber-jar 버전을 업데이트하는 것이 좋습니다. 예를 들어 AEM 6.4에 배포하려면 uber-jar 버전을 6.4.0으로 업데이트하는 것이 좋습니다.

#### 핵심 구성 요소 {#core-components}

AEM Project Archetype은 핵심 구성 요소를 활용합니다.

기본 실행 모드에서 AEM에 핵심 구성 요소를 자동으로 설치하고 샘플 WKND 사이트에서 사용합니다. [제작 실행 모드](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#runmodes)(`nosamplecontent`)에서는 핵심 구성 요소를 사용할 수 없습니다.

따라서 모든 배포에서 핵심 구성 요소를 활용하려면 Maven 프로젝트의 일부로 포함시키는 것이 좋습니다.

>[!NOTE]
>
>각 핵심 구성 요소 릴리스 다음에 AEM Project Archetype 릴리스가 제공되면 최신 Archetype이 최신 버전의 핵심 구성 요소를 사용합니다.
>
>하지만 새 버전의 Archetype 다음에 새 버전의 핵심 구성 요소가 바로 제공되지 않으면 핵심 구성 요소의 종속성을 최신 버전으로 업데이트할 수 있습니다.

>[!NOTE]
>
>core.wcm.components.예제는 핵심 구성 요소의 예제를 나타내는 샘플 페이지 세트입니다. 제작용 프로젝트를 배포할 때 이 종속성과 하위 패키지 포함을 제거하는 것이 좋습니다.

## 테스트 {#testing}

세 가지 수준의 테스트가 프로젝트에 포함되어 있습니다. 테스트의 유형이 서로 다르기 때문에 실행 방법 및 위치가 각각 다릅니다.

* core의 단위 테스트: 번들에 포함된 코드에 대한 클래식 단위 테스트를 보여 줍니다. 테스트를 하려면 다음을 실행합니다.
   * `mvn clean test`
* 서버측 통합 테스트: AEM 환경(AEM 서버)에서 유사 단위 테스트를 실행할 수 있습니다. 테스트를 하려면 다음을 실행합니다.
   * `mvn clean verify -PintegrationTests`
* 클라이언트측 Hobbes.js 테스트: 브라우저측 비헤이비어를 확인하는 JavaScript 기반 브라우저측 테스트입니다. 테스트를 수행하려면
   1. 페이지를 작성하는 경우 AEM을 브라우저에 로드합니다.
   1. 페이지를 [개발자 모드](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developer-tools/developer-mode.html)에서 엽니다
   1. 왼쪽 패널을 열고 **테스트** 탭으로 전환합니다.
   1. 생성된 **MyName 테스트**&#x200B;를 검색하고 실행합니다.

## 다음 단계 {#next-steps}

AEM Project Archetype을 빌드하고 설치했습니다. 이제 무엇을 합니까? Archetype의 규모는 작지만 권장 모범 사례에 따라 강력한 AEM 기능에 대한 여러 예제들로 구성됩니다. 이를 통해 이러한 기능이 프로젝트에서 어떻게 활용되는지 나타냅니다. 프로젝트의 경우 다음 작업을 수행해야 합니다.

* [기본 핵심 구성 요소를 확장하여 구성 요소를 사용자 정의합니다.](/help/developing/customizing.md)
* [템플릿 추가](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html)
* [현지화 구조 조정](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/translation/preparation.html)
* [프론트엔드 빌드 모듈에 대해 알아보기](uifrontend.md)

---
title: AEM 프로젝트 원형 사용
description: AEM 프로젝트 원형형에 대한 자세한 사용 지침
translation-type: tm+mt
source-git-commit: 477a1774a856725f52b9db7a978c534de4700661

---


# AEM 프로젝트 전형 {#aem-project-archetype}

AEM Project Tranype은 AEM 프로젝트의 시작점으로 최소한으로 우수 사례 기반 Adobe Experience Manager 프로젝트를 만듭니다. 이 전형 사용 시 제공해야 하는 속성을 사용하면 이 프로젝트의 모든 부분에 대한 이름을 지정할 수 있을 뿐만 아니라 특정 선택적 기능을 제어할 수 있습니다.

## 원형형을 사용하는 이유 {#why-use-the-archetype}

AEM 프로젝트 전형 사용을 사용하면 몇 번의 키 입력만으로 모범 사례 기반 AEM 프로젝트를 빌드하는 경로를 설정할 수 있습니다. 전형(tranype)을 사용하면 모든 조각이 이미 제자리에 배치되므로 결과 프로젝트가 최소한으로 수행되지만 AEM의 모든 [주요 기능이](#features) 이미 구현되어 우선 순위를 설정하고 확장할 수 있습니다.

물론 성공적인 AEM 프로젝트로 들어가는 많은 요소들이 있지만, AEM 프로젝트 전형 사용은 건전한 기반이며 모든 AEM 프로젝트에 적극 권장됩니다.

## 시작하기 {#getting-started}

프로젝트 원형에서는 AEM에서 개발을 쉽게 시작할 수 있습니다. 다양한 방법으로 첫 단계를 수행할 수 있습니다.

* WKND 튜토리얼 - AEM Sites를 활용하는 방법 등 AEM [에서 개발하는 방법에 대한 자세한 내용은 AEM Sites 시작하기 - WKND 튜토리얼을](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html) 참조하십시오. 이 자습서는 간단한 프로젝트를 구현하기 위해 원형형을 사용하는 방법을 안내합니다.
* WKND 이벤트 자습서 - AEM에서 단일 페이지 애플리케이션(SPA) 개발에 특히 관심이 있는 경우 전용 WKND 이벤트 [자습서를](https://helpx.adobe.com/experience-manager/kt/sites/using/getting-started-spa-wknd-tutorial-develop.html)확인하십시오.
* 직접 다운로드하여 시작해 보세요! - GitHub에서 제공되는 최신 프로젝트 전형 버전을 손쉽게 다운로드할 수 있으며 아래 [간단한 단계를](#how-to-use-the-archetype)수행하여 첫 번째 프로젝트를 제작할 수 있습니다.

## 원형형을 통해 얻을 수 있는 이점 {#what-you-get}

AEM Tranype은 다음 모듈로 구성됩니다.

* **[코어](core.md)**:는 OSGi 서비스, 리스너 및 스케줄러와 같은 모든 핵심 기능뿐만 아니라 서블릿 및 요청 필터와 같은 구성 요소 관련 Java 코드를 포함하는 Java 번들입니다.
* **[ui.apps](uiapps.md)**:에는 프로젝트의`/apps`부분과`/etc`부분(예: JS 및 CSS 클라이언트, 구성 요소, 템플릿, 런타임 모드 특정 구성 및 Hobbes 테스트 포함)
* **[ui.content](uicontent.md)**:에는 ui.apps 모듈의 구성 요소를 사용하는 샘플 컨텐츠가 포함되어 있습니다.
* **[ui.tests](uitests.md)**:는 서버측에서 실행되는 JUnit 테스트가 들어 있는 Java 번들입니다. 이 번들은 프로덕션에 배포되지 않습니다.
* **ui.launcher**:에는 ui.tests 번들(및 종속 번들)을 서버에 배포하고 원격 JUnit 실행을 트리거하는 접착제가 포함되어 있습니다.
* **[ui.front.general](uifrontend.md)**:(선택 사항)****에는 일반 Webpack 기반 프런트 엔드 빌드 모듈을 사용하는 데 필요한 결함이 포함되어 있습니다.
* **[ui.frontend.response](uifrontend-react.md)**:(선택 사항)****에는 원형 툴을 사용하여 반응(React)을 기반으로 SPA 프로젝트를 만들 때 필요한 가공물이 포함되어 있습니다.
* **[ui.front.angular](uifrontend-angular.md)**:(선택 사항)****에는 원형(Angular)을 사용하여 Angular를 기반으로 SPA 프로젝트를 만들 때 필요한 가공물이 포함되어 있습니다.

![](/help/assets/archetype-structure.png)

Maven에 표시되는 AEM Tranype 모듈은 애플리케이션, 컨텐츠 및 필요한 OSGi 번들을 나타내는 컨텐츠 패키지로 AEM에 배포됩니다.

## 원형형을 사용하는 방법 {#how-to-use-the-archetype}

원형형을 사용하려면 먼저 프로젝트를 만들어야 합니다. 이 프로젝트는 [이전에 설명한](#what-you-get)대로 로컬 파일 구조로 모듈을 생성합니다. 프로젝트 생성의 일부로 프로젝트 이름, 버전 등과 같이 프로젝트에 대한 많은 속성을 정의할 수 있습니다.

Maven을 사용하여 프로젝트를 빌드하면 AEM에 배포할 객체(패키지 및 OSGi 번들)가 만들어집니다. 추가 Maven 명령 및 프로필을 사용하여 프로젝트 객체를 AEM 인스턴스에 배포할 수 있습니다.

### 프로젝트 만들기 {#create-project}

먼저 AEM Eclipse 확장 기능을 [사용하고 새 프로젝트](https://docs.adobe.com/content/help/en/experience-manager-65/developing/devtools/aem-eclipse.html) 마법사를 **따라 AEM 샘플 다중 모듈** 프로젝트를선택하여 릴리스된 버전의 전형을 사용할 수 있습니다.

물론 마벤을 직접 불러오셔도 됩니다

```
mvn -B archetype:generate \
 -D archetypeGroupId=com.adobe.granite.archetypes \
 -D archetypeArtifactId=aem-project-archetype \
 -D archetypeVersion=XX \
 -D aemVersion=cloud \
 -D appTitle="My Site" \
 -D appId="mysite" \
 -D groupId="com.mysite" \
 -D frontendModule=general \
 -D includeExamples=n
```

* 최신 `XX` AEM Project Tranype의 [버전 번호로](https://github.com/adobe/aem-project-archetype/blob/master/VERSIONS.md) 설정합니다.
* Set `aemVersion=cloud` for [AEM as a Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html);\
   Adobe Managed `aemVersion=6.5.0` Services [](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams)또는 온프레미스 설정
핵심 구성 요소는 CloudService로 AEM용 OOTB가 제공되므로 비 클라우드 aem 버전에 대해서만 추가됩니다.
* 웹 사이트 제목 및 구성 요소 그룹을 `appTitle="My Site"` 정의하려면 조정합니다.
* Maven artifactId, 구성 요소, 구성 및 콘텐트 폴더 이름, 클라이언트 라이브러리 이름을 정의하려면 `appId="mysite"` 조정합니다.
* Maven groupId 및 Java 소스 패키지를 `groupId="com.mysite"` 정의하기 위해 조정합니다.
* 사용 가능한 속성 목록을 조회하여 조정할 추가 사항이 있는지 확인합니다.

>[!NOTE]
>
>Maven 파일에 `adobe-public` 프로필을 추가하면 `settings.xml` maven 빌드 프로세스에 repo.adobe.com이 자동으로 추가됩니다.
>
>POM 예는 여기에서 [찾을 수 있습니다](https://helpx.adobe.com/experience-manager/kb/SetUpTheAdobeMavenRepository.html).

### 속성 {#properties}

원형형을 사용하여 프로젝트를 만들 때 다음 속성을 사용할 수 있습니다.

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

>[!NOTE]
> 원형형이 처음 대화형 모드에서 실행되는 경우 기본값을 갖는 속성을 변경할 수 없습니다(자세한 내용은 [RCEYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) 참조). 끝 부분의 속성 확인이 거부되고 질문서가 반복되거나 명령줄의 매개 변수(예: `-DoptionIncludeExamples=n`).

>[!NOTE]
>Windows에서 실행하고 디스패처 구성을 생성할 때는 관리자 권한 명령 프롬프트 또는 Linux용 Windows 하위 시스템에서 실행해야 합니다( [문제 329 참조](https://github.com/adobe/aem-project-archetype/issues/329)).

### 프로파일 {#profiles}

생성된 maven 프로젝트는 실행 시 다른 배포 프로필을 지원합니다 `mvn install`.

| 프로필 ID | 설명 |
--------------------------|------------------------------
| `autoInstallBundle` | felix 콘솔에 대한 maven-sling-plugin을 사용하여 핵심 번들 설치 |
| `autoInstallPackage` | localhost, port 4502에서 기본 작성 인스턴스를 설정하려면 패키지 관리자에 content-package-maven-plugin을 사용하여 ui.content 및 ui.apps 컨텐츠 패키지를 설치합니다. 호스트 이름 및 포트는 `aem.host` 및 `aem.port` 사용자 정의 속성으로 변경할 수 있습니다. |
| `autoInstallPackagePublish` | localhost, port 4503에서 기본 게시 인스턴스를 설정하려면 content-package-maven-plugin을 패키지 관리자에 사용하여 ui.content 및 ui.apps 컨텐츠 패키지를 설치합니다. 호스트 이름 및 포트는 `aem.host` 및 `aem.port` 사용자 정의 속성으로 변경할 수 있습니다. |
| `autoInstallSinglePackage` | content-package-maven-plugin과 함께 `all` 콘텐트 패키지를 패키지 관리자에 설치하여 localhost, port 4502에서 기본 작성자 인스턴스를 설치합니다. 호스트 이름 및 포트는 `aem.host` 및 `aem.port` 사용자 정의 속성으로 변경할 수 있습니다. |
| `autoInstallSinglePackagePublish` | content-package-maven-plugin과 함께 `all` 콘텐트 패키지를 패키지 관리자에 설치하여 localhost, port 4503에서 기본 게시 인스턴스를 설치합니다. 호스트 이름 및 포트는 `aem.host` 및 `aem.port` 사용자 정의 속성으로 변경할 수 있습니다. |
| `integrationTests` | AEM 인스턴스에서 제공된 통합 테스트를 실행합니다( `verify` 단계에 대해서만). |

### 작성 및 설치 {#building-and-installing}

프로젝트 루트 디렉토리에서 실행되는 모든 모듈을 빌드하려면 다음 Maven 명령을 사용합니다.

```
mvn clean install
```

실행 중인 AEM 인스턴스가 있는 경우 다음 Maven 명령을 사용하여 전체 프로젝트를 작성하고 패키지하여 AEM에 배포할 수 있습니다.

```
mvn clean install -PautoInstallPackage
```

게시 인스턴스에 배포하려면 이 명령을 실행합니다.

```
mvn clean install -PautoInstallPackagePublish
```

또는 게시 인스턴스에 배포하려면 이 명령을 실행합니다.

```
mvn clean install -PautoInstallPackage -Daem.port=4503
```

또는 번들만 작성자에게 배포하려면 이 명령을 실행합니다.

```
mvn clean install -PautoInstallBundle
```

## 상위 POM {#parent-pom}

프로젝트 `pom.xml` 루트의 위치(`<src-directory>/<project>/pom.xml`)를 상위 POM이라고 하며 프로젝트의 구조를 구동할 수 있을 뿐만 아니라 프로젝트의 종속성 및 특정 전역 속성을 관리합니다.

### 전역 프로젝트 속성 {#global-properties}

상위 POM의 `<properties>` 섹션에서는 사용자 이름/암호, 호스트 이름/포트 등과 같은 AEM 인스턴스에서 프로젝트를 배포하는 데 중요한 몇 가지 전역 속성을 정의합니다.

이러한 속성은 개발자가 수행하는 가장 일반적인 빌드이므로 로컬 AEM 인스턴스에 배포하도록 설정됩니다. 게시 인스턴스와 작성자 인스턴스에 배포할 속성이 있습니다. 또한 자격 증명이 AEM 인스턴스로 인증되도록 설정되어 있습니다. 기본 admin:admin 자격 증명이 사용됩니다.

이러한 속성은 상위 수준 환경에 배포할 때 재정의할 수 있도록 설정됩니다. 이러한 방식으로 POM 파일은 변경할 필요가 없지만 다음과 같은 변수를 명령줄 인수를 통해 재정의할 `aem.host` 수 `sling.password` 있습니다.

````
mvn -PautoInstallPackage clean install -Daem.host=production.hostname -Dsling.password=productionpasswd
````

### 모듈 구조 {#module-structure}

상위 POM의 `<modules>` 섹션에서는 프로젝트가 빌드할 모듈을 정의합니다. 기본적으로 프로젝트는 [이전에 정의된](#what-you-get)표준 모듈을 작성합니다.핵심, ui.apps, ui.content, ui.tests 및 it.launcher. 프로젝트의 진화에 따라 더 많은 모듈을 추가할 수 있습니다.

### 종속성 {#dependencies}

상위 POM의 `<dependencyManagement>` 섹션에서는 프로젝트에 사용되는 API의 모든 종속성 및 버전을 정의합니다. 버전은 상위 POM에서 관리해야 합니다. 코어 및 ui.apps와 같은 하위 모듈에는 버전 정보가 포함되지 않아야 합니다.

#### Uber-Jar {#uber-jar}

주요 종속성 중 하나는 AEM [uber-jar](https://docs.adobe.com/content/help/en/experience-manager-65/developing/devtools/ht-projects-maven.html#ExperienceManagerAPIDependencies). 여기에는 AEM 버전에 대한 단일 종속성 항목만 포함된 모든 AEM API가 포함됩니다.

>[!NOTE]
>
>우수 사례로 uber-jar 버전을 업데이트하여 AEM의 대상 버전과 일치시켜야 합니다. 예를 들어 AEM 6.4에 배포하려는 경우 uber-jar 버전을 6.4.0으로 업데이트해야 합니다.

#### 코어 구성 요소 {#core-components}

AEM 프로젝트 원형에서는 물론 핵심 구성 요소를 활용합니다.

코어 구성 요소는 기본 런타임 모드에서 자동으로 설치되고 샘플 We.Retail 사이트에서 사용됩니다. 프로덕션 [런타임](https://docs.adobe.com/content/help/en/experience-manager-65/administering/security/production-ready.html) (`nosamplecontent`)에서는 핵심 구성 요소를 사용할 수 없습니다.

따라서 모든 배포에서 핵심 구성 요소를 활용하려면 이를 Maven 프로젝트의 일부로 포함하는 것이 좋습니다.

>[!NOTE]
>
>핵심 구성 요소의 각 릴리스에는 일반적으로 AEM 프로젝트 원형형이 릴리스되어 최신 버전의 핵심 구성 요소가 사용됩니다.
>
>그러나 새 버전의 원형 구성 요소는 새 버전의 핵심 구성 요소를 직접 따르지 않으므로 핵심 구성 요소에 대한 종속성을 최신 버전으로 업데이트할 수 있습니다.

>[!NOTE]
>
>core.wcm.components.examples는 핵심 구성 요소의 예를 보여주는 샘플 페이지 세트입니다. 프로덕션 프로젝트를 배포할 때는 이 종속성을 제거하고 하위 패키지 포함을 제거하는 것이 좋습니다.

## 테스트 {#testing}

프로젝트에는 세 가지 수준의 테스트가 포함되어 있으며 테스트 유형은 서로 다르기 때문에 다른 방법이나 다른 위치에서 실행됩니다.

* 핵심 단위 테스트:번들에 포함된 코드의 클래식 단위 테스트가 표시됩니다. 테스트하려면 다음을 실행합니다.
   * `mvn clean test`
* 서버측 통합 테스트:이러한 테스트는 AEM 환경에서(예: AEM 서버에서) 단위 관련 테스트를 실행합니다. 테스트하려면 다음을 실행합니다.
   * `mvn clean verify -PintegrationTests`
* 클라이언트측 Hobbes.js 테스트:브라우저 측 동작을 확인하는 JavaScript 기반 브라우저 측 테스트입니다. 테스트하려면:
   1. 페이지를 작성하는 것처럼 브라우저에서 AEM을 로드합니다.
   1. Open the page in [Developer mode](https://docs.adobe.com/content/help/en/experience-manager-65/developing/components/developer-mode.html)
   1. 왼쪽 패널을 열고 테스트 **탭으로** 전환합니다.
   1. 생성된 MyName **테스트를** 찾아 실행합니다.

## 다음 단계 {#next-steps}

AEM 프로젝트 원형형을 만들고 설치했습니다. 지금 뭐? 전형은 작지만 권장 우수 사례에 따라 구성된 강력한 AEM 기능의 많은 예제로 구성되어 있습니다. 이러한 기능은 프로젝트에서 이러한 기능을 활용할 수 있는 방법을 보여 줍니다. 모든 프로젝트의 경우 다음을 수행해야 합니다.

* [기존 핵심 구성 요소를 확장하여 구성 요소 사용자 정의](/help/developing/customizing.md)
* [추가 템플릿 추가](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)
* [현지화 구조 조정](https://docs.adobe.com/content/help/en/experience-manager-65/administering/introduction/tc-prep.html)
* [프런트 엔드 빌드 모듈에 대한 자세한 내용](uifrontend.md)

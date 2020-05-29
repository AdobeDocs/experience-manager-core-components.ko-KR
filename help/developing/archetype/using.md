---
title: AEM 프로젝트 원형 사용
description: AEM 프로젝트 원형 유형에 대한 자세한 사용 지침
translation-type: tm+mt
source-git-commit: 6f7166c46940ed451721e0760d565d58efe412ab
workflow-type: tm+mt
source-wordcount: '2057'
ht-degree: 1%

---


# AEM 프로젝트 전형 {#aem-project-archetype}

AEM Project Tranype은 AEM 프로젝트의 시작점으로 최소의 우수 사례 기반 Adobe Experience Manager 프로젝트를 만듭니다. 이 원형 유형을 사용할 때 제공해야 하는 속성을 사용하면 이 프로젝트의 모든 부분에 대한 이름을 지정할 수 있을 뿐만 아니라 특정 선택적 기능을 제어할 수 있습니다.

## 원형을 사용하는 이유 {#why-use-the-archetype}

AEM 프로젝트 원형 유형을 사용하면 몇 번의 키 입력만으로 모범 사례 기반 AEM 프로젝트를 빌드하는 경로에 사용자를 설정할 수 있습니다. 원형 사용을 통해 모든 조각이 이미 제자리에 배치되므로, 결과 프로젝트는 최소이지만, AEM의 모든 [주요 기능을](#what-you-get) 이미 구현하므로 위에서 빌드하고 확장하기만 하면 됩니다.

물론 성공적인 AEM 프로젝트로 들어가는 많은 요소들이 있지만, AEM 프로젝트 전형 사용은 건전한 기반이며, 모든 AEM 프로젝트에 적극 권장됩니다.

## 시작하기 {#getting-started}

프로젝트 원형을 사용하면 AEM에서 개발을 쉽게 시작할 수 있습니다. 다양한 방법으로 첫 단계를 진행할 수 있습니다.

* WKND 자습서 - 원형율을 활용하는 방법 등 AEM에서 개발하는 방법에 대한 자세한 내용은 AEM Sites 시작하기 - WKND 자습서를 [](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html) 참조하십시오. 기본 유형을 사용하여 간단한 프로젝트를 구현할 수 있는 실용적인 예는 AEM Sites를 참조하십시오.
* WKND 이벤트 자습서 - AEM에서 단일 페이지 애플리케이션(SPA) 개발에 특히 관심이 있는 경우 전용 WKND 이벤트 자습서를 [확인하십시오](https://helpx.adobe.com/experience-manager/kt/sites/using/getting-started-spa-wknd-tutorial-develop.html).
* 직접 다운로드하여 시작해 보세요! - GitHub에서 제공되는 최신 프로젝트 원형 유형을 손쉽게 다운로드할 수 있으며 아래 [의 간단한 단계를 통해 첫 번째 프로젝트를 제작할 수 있습니다](#how-to-use-the-archetype).

## 원형을 통해 얻을 수 있는 이점 {#what-you-get}

AEM Tranype은 다음과 같은 모듈로 구성됩니다.

* **[코어](core.md)**: 는 OSGi 서비스, 청취자 및 일정기와 같은 모든 핵심 기능뿐만 아니라 서블릿 및 요청 필터와 같은 구성 요소 관련 Java 코드가 포함된 Java 번들입니다.
* **[ui.apps](uiapps.md)**: 에는 프로젝트의`/apps`부분과`/etc`부분, 즉 JS 및 CSS clientlibs, components, templates, runmode-specific configs and as Hobes tests.
* **[ui.content](uicontent.md)**: ui.apps 모듈의 구성 요소를 사용하는 샘플 컨텐츠를 포함합니다.
* **[ui.tests](uitests.md)**: 은 서버측에서 실행되는 JUnit 테스트가 들어 있는 Java 번들입니다. 이 번들은 프로덕션에 배포되지 않습니다.
* **ui.launcher**: ui.tests 번들(및 종속 번들)을 서버에 배포하고 원격 JUnit 실행을 트리거하는 링크 코드를 포함합니다.
* **[ui.frontend.general](uifrontend.md)**:**(선택 사항)**일반 웹 팩 기반 프런트 엔드 빌드 모듈을 사용하는 데 필요한 결함이 포함되어 있습니다.
* **[ui.frontend.response](uifrontend-react.md)**:**(선택 사항)**원형형을 사용하여 React를 기반으로 SPA 프로젝트를 만들 때 필요한 가공물이 포함되어 있습니다.
* **[ui.frontend.angular](uifrontend-angular.md)**:**(선택 사항)**원형(Angun)을 사용하여 SPA 프로젝트를 생성할 때 필요한 가공물이 포함되어 있습니다.

![](/help/assets/archetype-structure.png)

Maven에 대표되는 AEM Tranype 모듈은 애플리케이션, 컨텐츠 및 필요한 OSGi 번들을 나타내는 컨텐츠 패키지로 AEM에 배포됩니다.

## 원형 사용 방법 {#how-to-use-the-archetype}

원형을 사용하려면 먼저 프로젝트를 만들어야 하며, 이 경우 [이전에 설명한 대로 로컬 파일 구조에 모듈을 생성합니다](#what-you-get). 프로젝트 생성의 일부로 프로젝트 이름, 버전 등과 같이 프로젝트에 대한 많은 속성을 정의할 수 있습니다.

Maven을 사용하여 프로젝트를 빌드하면 AEM에 배포할 수 있는 객체(패키지 및 OSGi 번들)가 만들어집니다. 추가적인 Maven 명령과 프로필을 사용하여 프로젝트 객체를 AEM 인스턴스에 배포할 수 있습니다.

### 프로젝트 만들기 {#create-project}

AEM Eclipse 확장 [을](https://docs.adobe.com/content/help/en/experience-manager-65/developing/devtools/aem-eclipse.html) 간단히 사용하고 새 프로젝트 마법사를 따라 AEM Sample Multi-Module Project를 선택하여 **AEM Sample Multi-Module Project** 에서 출시된 원형 버전을 사용할 수 있습니다.

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

* 최신 AEM Project Tranype `XX` 의 [버전 번호로](https://github.com/adobe/aem-project-archetype/blob/master/VERSIONS.md) 설정합니다.
* Set `aemVersion=cloud` for [AEM as a Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html);\
   `aemVersion=6.5.0` Adobe Managed Services [](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams)또는 온프레미스 설정
핵심 구성 요소는 CloudService로서 AEM용 OOTB를 제공함에 따라 비 클라우드 aem 버전에 대해서만 추가됩니다.
* 웹 사이트 제목 및 구성 요소 그룹 `appTitle="My Site"` 을 정의하려면 조정합니다.
* 클라이언트 라이브러리 이름 `appId="mysite"` 은 물론 구성 요소, 구성 요소, 구성 및 컨텐츠 폴더 이름을 정의하기 위해 조정합니다.
* Maven groupId `groupId="com.mysite"` 와 Java 소스 패키지를 정의하도록 조정합니다.
* 사용 가능한 속성 목록을 조회하여 조정할 추가 사항이 있는지 확인합니다.

>[!NOTE]
>
>전문적인 빌드 프로세스에 repo.adobe.com을 자동으로 추가하려면 Maven `adobe-public` `settings.xml` 파일에 프로필을 추가하는 것이 좋습니다.
>
>예제 POM은 여기에서 찾을 [수 있습니다](https://helpx.adobe.com/experience-manager/kb/SetUpTheAdobeMavenRepository.html).

### 속성 {#properties}

원형형을 사용하여 프로젝트를 만들 때는 다음 속성을 사용할 수 있습니다.

| 이름 | 기본값 | 설명 |
--------------------------|----------------|--------------------
| `appTitle` |  | 애플리케이션 제목은 웹 사이트 제목 및 구성 요소 그룹(예: `"My Site"`). |
| `appId` |  | 기술 이름은 클라이언트 라이브러리 이름(예: `"mysite"`). |
| `artifactId` | *`${appId}`* | 기본 마비안 아티팩트 ID(예: `"mysite"`). |
| `groupId` |  | 기본 마비안 그룹 ID(예: `"com.mysite"`). |
| `package` | *`${groupId}`* | Java 소스 패키지(예: `"com.mysite"`). |
| `version` | `1.0-SNAPSHOT` | 프로젝트 버전(예: `1.0-SNAPSHOT`). |
| `aemVersion` | `6.5.0` | 타겟 AEM 버전(클라우드 서비스로 `cloud` AEM용으로 사용할 수 있음 [](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html)) 또는 `6.5.0``6.4.4`Adobe Managed Services `6.3.3` 또는 [온프레미스](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) )를 사용할 수 있습니다. |
| `sdkVersion` | `latest` | SDK `aemVersion=cloud` 버전 [을 지정할](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html) 수 있는 경우(예: `2020.02.2265.20200217T222518Z-200130`). |
| `includeDispatcherConfig` | `y` | 값(또는 `aemVersion` )에 따라 클라우드 또는 AMS/on-premise용 디스패처 구성을 `y` `n`포함합니다. |
| `frontendModule` | `none` | 클라이언트 라이브러리를 생성하는 Webpack 프런트 엔드 빌드 모듈(일반 사이트일 수도 `general` 또는 `none` 에 사용할 수 있음)을 포함합니다. SPA 편집기 `angular` 를 구현하는 단일 페이지 앱에 대해 `react` 또는 [사용할 수 있습니다](https://docs.adobe.com/content/help/en/experience-manager-65/developing/headless/spas/spa-overview.html). |
| `languageCountry` | `en_us` | 컨텐츠 구조를 만드는 언어 및 국가 코드(예: `en_us`). |
| `singleCountry` | `y` | 언어 마스터 컨텐츠 구조를 포함합니다( `y`또는 `n`). |
| `includeExamples` | `y` | 구성 요소 [라이브러리](https://www.aemcomponents.dev/) 예제 사이트( `y`또는 `n`될 수 있음)를 포함합니다. |
| `includeErrorHandler` | `n` | 전체 인스턴스( `y` 또는 `n`)에 대해 글로벌할 사용자 지정 404 응답 페이지를 포함합니다. |

>[!NOTE]
> 원형이 처음 대화형 모드에서 실행되는 경우, 기본값이 있는 속성은 변경할 수 없습니다(자세한 내용은 [TRANYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) 참조). 마지막 속성 확인이 거부되고 질문서가 반복되거나 명령줄의 매개 변수(예: `-DoptionIncludeExamples=n`).

>[!NOTE]
>Windows에서 실행하고 디스패처 구성을 생성하는 경우 관리자 권한 명령 프롬프트 또는 Linux용 Windows 하위 시스템에서 실행해야 합니다( [문제 329](https://github.com/adobe/aem-project-archetype/issues/329)참조).

### 프로파일 {#profiles}

생성된 마스터 프로젝트는 실행 시 다른 배포 프로필을 지원합니다 `mvn install`.

| 프로필 ID | 설명 |
--------------------------|------------------------------
| `autoInstallBundle` | felix console에 maven-sling-plugin을 사용하여 코어 번들 설치 |
| `autoInstallPackage` | localhost, port 4502에서 기본 작성 인스턴스를 설정하려면 패키지 관리자에 content-package-maven-plugin을 사용하여 ui.content 및 ui.apps 컨텐츠 패키지를 설치합니다. 호스트 이름 및 포트는 `aem.host` 및 `aem.port` 사용자 정의 속성으로 변경할 수 있습니다. |
| `autoInstallPackagePublish` | localhost, port 4503에서 기본적으로 게시 인스턴스를 게시하려면 content-package-maven-plugin이 포함된 ui.content 및 ui.apps 컨텐츠 패키지를 패키지 관리자에게 설치합니다. 호스트 이름 및 포트는 `aem.host` 및 `aem.port` 사용자 정의 속성으로 변경할 수 있습니다. |
| `autoInstallSinglePackage` | localhost, port 4502에서 기본 작성 인스턴스를 설정하려면 패키지 관리자에 content-package-maven-plugin을 사용하여 `all` 컨텐츠 패키지를 설치합니다. 호스트 이름 및 포트는 `aem.host` 및 `aem.port` 사용자 정의 속성으로 변경할 수 있습니다. |
| `autoInstallSinglePackagePublish` | localhost, port 4503에서 기본 게시 인스턴스를 설정하려면 패키지 관리자에 content-package-maven-plugin을 사용하여 `all` 컨텐츠 패키지를 설치합니다. 호스트 이름 및 포트는 `aem.host` 및 `aem.port` 사용자 정의 속성으로 변경할 수 있습니다. |
| `integrationTests` | AEM 인스턴스에서 제공된 통합 테스트를 `verify` 실행합니다(단계에만 해당). |

### 빌드 및 설치 {#building-and-installing}

프로젝트 루트 디렉토리에서 실행되는 모든 모듈을 빌드하려면 다음 마웬 명령을 사용합니다.

```
mvn clean install
```

실행 중인 AEM 인스턴스가 있는 경우 다음 Maven 명령을 사용하여 전체 프로젝트를 빌드하고 패키지하여 AEM에 배포할 수 있습니다.

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

프로젝트 루트 `pom.xml` (`<src-directory>/<project>/pom.xml`)에 있는 POM을 상위 POM이라고 하며 프로젝트의 구조를 만들고 프로젝트의 종속성 및 특정 전역 속성을 관리합니다.

### 전역 프로젝트 속성 {#global-properties}

상위 POM의 `<properties>` 섹션은 사용자 이름/암호, 호스트 이름/포트 등과 같은 AEM 인스턴스에 프로젝트를 배포하는 데 중요한 몇 가지 전역 속성을 정의합니다.

이러한 속성은 개발자가 수행하는 가장 일반적인 빌드이므로 로컬 AEM 인스턴스에 배포하도록 설정됩니다. 게시 인스턴스와 작성자 인스턴스에 배포할 속성이 있습니다. 또한 자격 증명이 AEM 인스턴스로 인증되도록 설정되어 있습니다. 기본 admin:admin 자격 증명이 사용됩니다.

이러한 속성은 상위 수준 환경에 배포할 때 재정의할 수 있도록 설정됩니다. 이러한 방식으로 POM 파일은 변경할 필요가 없지만 명령줄 인수를 통해 다음과 같은 변수 `aem.host` 를 재정의할 `sling.password` 수 있습니다.

```
mvn -PautoInstallPackage clean install -Daem.host=production.hostname -Dsling.password=productionpasswd
```

### 모듈 구조 {#module-structure}

상위 POM의 `<modules>` 섹션은 프로젝트가 빌드할 모듈을 정의합니다. 기본적으로 프로젝트는 이전에 정의된 표준 모듈 [을 빌드합니다](#what-you-get). core, ui.apps, ui.content, ui.tests 및 it.launcher. 프로젝트의 진화에 따라 더 많은 모듈을 추가할 수 있습니다.

### 종속성 {#dependencies}

상위 POM의 `<dependencyManagement>` 섹션은 프로젝트에서 사용되는 API의 모든 종속성 및 버전을 정의합니다. 버전은 상위 POM에서 관리해야 합니다. 코어 및 ui.apps와 같은 하위 모듈에는 버전 정보가 포함되지 않아야 합니다.

#### 우버항아리 {#uber-jar}

주요 종속성 중 하나는 [AEM uber-jar입니다](https://docs.adobe.com/content/help/en/experience-manager-65/developing/devtools/ht-projects-maven.html#ExperienceManagerAPIDependencies). 여기에는 AEM 버전에 대한 단일 종속성 항목이 포함된 모든 AEM API가 포함됩니다.

>[!NOTE]
>
>가장 좋은 방법은 우버-jar 버전을 업데이트하여 AEM의 대상 버전과 일치시키는 것입니다. 예를 들어 AEM 6.4에 배포할 계획인 경우 uber-jar 버전을 6.4.0으로 업데이트해야 합니다.

#### 코어 구성 요소 {#core-components}

물론 AEM 프로젝트 원형에서는 핵심 구성 요소를 활용합니다.

핵심 구성 요소는 기본 실행 모드에서 자동으로 AEM에 설치되며 샘플 We.Retail 사이트에서 사용됩니다. 프로덕션 [실행 모드](https://docs.adobe.com/content/help/en/experience-manager-65/administering/security/production-ready.html) (`nosamplecontent`)에서는 핵심 구성 요소를 사용할 수 없습니다.

따라서 모든 배포에서 핵심 구성 요소를 활용하려면 이를 Maven 프로젝트의 일부로 포함하는 것이 좋습니다.

>[!NOTE]
>
>핵심 구성 요소의 각 릴리스에는 일반적으로 AEM 프로젝트 원형 버전이 릴리스되므로 최신 원형에서는 핵심 구성 요소의 최신 버전이 사용됩니다.
>
>단, 원형형의 새 버전은 핵심 구성 요소의 새 버전을 직접 따르지 않을 수 있으므로 핵심 구성 요소에 대한 종속성을 최신 버전으로 업데이트할 수 있습니다.

>[!NOTE]
>
>core.wcm.components.examples는 핵심 구성 요소의 예를 보여주는 샘플 페이지 세트입니다. 프로덕션 프로젝트를 배포할 때는 이 종속성 및 하위 패키지 포함을 제거해야 합니다.

## 테스트 {#testing}

프로젝트에는 세 가지 수준의 테스트가 포함되어 있으며 테스트 유형은 서로 다르기 때문에 다른 방법이나 다른 위치에서 실행됩니다.

* 핵심 단위 테스트: 번들에 포함된 코드의 클래식 단위 테스트가 표시됩니다. 테스트하려면 다음을 실행하십시오.
   * `mvn clean test`
* 서버측 통합 테스트: 이러한 실행 단위 테스트는 AEM 환경에서 실행됩니다(예: AEM 서버). 테스트하려면 다음을 실행하십시오.
   * `mvn clean verify -PintegrationTests`
* 클라이언트측 Hobes.js 테스트: 브라우저 측 동작을 확인하는 JavaScript 기반 브라우저 측 테스트입니다. 테스트하려면:
   1. 페이지를 작성하는 것처럼 브라우저에서 AEM을 로드합니다.
   1. Open the page in [Developer mode](https://docs.adobe.com/content/help/en/experience-manager-65/developing/components/developer-mode.html)
   1. 왼쪽 패널을 열고 테스트 **탭으로** 전환합니다.
   1. 생성된 MyName **테스트를** 찾아 실행합니다.

## 다음 단계 {#next-steps}

AEM 프로젝트 원형형을 만들고 설치했습니다. 이제 어쩌죠? 음전형적인 유형은 작지만 권장 우수 사례에 따라 구성된 강력한 AEM 기능의 많은 예제로 구성되어 있습니다. 프로젝트에서 이러한 기능을 활용할 수 있는 방법에 대한 설명입니다. 모든 프로젝트의 경우 다음을 수행해야 합니다.

* [기존 핵심 구성 요소를 확장하여 구성 요소 사용자 정의](/help/developing/customizing.md)
* [추가 템플릿 추가](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)
* [로컬라이제이션 구조 조정](https://docs.adobe.com/content/help/en/experience-manager-65/administering/introduction/tc-prep.html)
* [프런트 엔드 빌드 모듈에 대한 자세한 내용](uifrontend.md)

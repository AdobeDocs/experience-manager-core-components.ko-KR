---
title: AEM 프로젝트 원형 사용
description: AEM 프로젝트 원형을 위한 자세한 사용 지침
feature: 핵심 구성 요소, AEM 프로젝트 원형
role: 건축가, 개발자, 관리자
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '2072'
ht-degree: 1%

---


# AEM 프로젝트 전형 {#aem-project-archetype}

AEM Project Tranype은 AEM 프로젝트를 위한 시작점으로 최소의 모범 사례 기반 Adobe Experience Manager 프로젝트를 만듭니다. 이 원형 유형을 사용할 때 제공해야 하는 속성을 사용하여 이 프로젝트의 모든 부분에 대한 이름을 지정하고 특정 선택적 기능을 제어할 수 있습니다.

## 원형 {#why-use-the-archetype}을 사용하는 이유

AEM 프로젝트 원형을 사용하면 몇 번의 키 입력만으로 모범 사례 기반의 AEM 프로젝트를 구축하는 방법을 선택할 수 있습니다. 원형형을 사용하면 모든 조각들이 이미 제자리에 배치되므로 결과 프로젝트는 최소한으로 수행되지만 AEM의 [주요 기능](#what-you-get)을 모두 이미 구현하므로 필요한 작업은 맨 위에 쌓고 확장만 하면 됩니다.

물론 성공적인 AEM 프로젝트에 참여하는 많은 요소들이 있지만 AEM 프로젝트 원형형을 사용하는 것은 건전한 기반이며 모든 AEM 프로젝트에 적극 권장됩니다.

## 시작하기 {#getting-started}

프로젝트 원형을 사용하면 AEM을 기반으로 개발 작업을 손쉽게 시작할 수 있습니다. 다양한 방법으로 첫 단계를 수행할 수 있습니다.

* WKND 튜토리얼 - 원형 기능을 활용하는 방법을 포함하여 AEM에서 개발하는 방법에 대한 자세한 내용은 원형 유형을 사용하여 간단한 프로젝트를 구현할 수 있는 실용적인 예제에 대한 자세한 내용은 [AEM Sites 시작하기 - WKND 자습서](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)를 참조하십시오.
* WKND 이벤트 자습서 - AEM에서 단일 페이지 애플리케이션(SPA) 개발에 특히 관심이 있는 경우 전용 [WKND 이벤트 자습서](https://helpx.adobe.com/experience-manager/kt/sites/using/getting-started-spa-wknd-tutorial-develop.html)를 확인하십시오.
* 직접 다운로드하여 시작해 보십시오. - GitHub에서 사용할 수 있는 현재 프로젝트 원형 유형을 쉽게 다운로드할 수 있으며 ](#how-to-use-the-archetype) 아래의 간단한 단계를 따라 [이(가) 첫 번째 프로젝트를 만들 수 있습니다.

## 원형 {#what-you-get}을(를) 사용하여 얻는 내용

AEM Lianype은 다음과 같은 모듈로 구성됩니다.

* **[코어](core.md)**:는 OSGi 서비스, 리스너 및 스케줄러와 같은 모든 핵심 기능뿐만 아니라 서블릿 및 요청 필터와 같은 구성 요소 관련 Java 코드가 포함된 Java 번들입니다.
* **[it.tests](ittests.md)**:은 Java 기반 통합 테스트입니다.
* **[ui.apps](uiapps.md)**:에는 프로젝트 `/apps` 의  `/etc` 및 부분, 즉 JS 및 CSS clientlibs, 구성 요소 및 템플릿이 포함되어 있습니다.
* **[ui.content](uicontent.md)**:은 ui.apps 모듈의 구성 요소를 사용하는 샘플 컨텐츠를 포함합니다.
* **ui.config**:프로젝트에 대한 런타임 모드 특정 OSGi 구성을 포함합니다.
* **[ui.frontend.general](uifrontend.md)**: **(선택 사항)** 에는 일반적인 웹 팩 기반 프런트 엔드 빌드 모듈을 사용하는 데 필요한 아티팩트가 포함되어 있습니다.
* **[ui.frontend.react](uifrontend-react.md)**: **(선택 사항)** 에는 원형 유형을 사용하여 [반응]을 기반으로 SPA 프로젝트를 만들 때 필요한 가공물이 포함되어 있습니다.
* **[ui.frontend.angular](uifrontend-angular.md)**: **(선택 사항)** 에는 Angular 기반의 SPA 프로젝트를 만들기 위해 원형 유형을 사용할 때 필요한 가공물이 포함되어 있습니다.
* **[ui.tests](uitests.md)**:는 Selenium 기반 UI 테스트를 포함합니다.
* **모두**:은 공급업체 종속성을 포함하여 컴파일된 모든 모듈(번들 및 컨텐츠 패키지)을 포함하는 단일 컨텐츠 패키지입니다.
* **분석**:프로젝트에서 분석을 실행합니다. 이 분석은 Cloud Service으로 AEM에 배포하기 위한 추가 유효성 검사를 제공합니다.

![](/help/assets/archetype-structure.png)

Maven에 대표되는 AEM Tranype 모듈은 애플리케이션, 컨텐츠 및 필요한 OSGi 번들을 나타내는 컨텐츠 패키지로 AEM에 배포됩니다.

## 원형 유형 {#how-to-use-the-archetype}을 사용하는 방법

전형적인 유형을 사용하려면 먼저 프로젝트를 만들어야 합니다. 이 경우 로컬 파일 구조에 모듈을 [이전에 설명한 ](#what-you-get)으로 생성합니다. 프로젝트 생성의 일부로 프로젝트 이름, 버전 등과 같이 프로젝트에 대한 많은 속성을 정의할 수 있습니다.

Maven을 사용하여 프로젝트를 빌드하면 AEM에 배포할 객체(패키지 및 OSGi 번들)가 만들어집니다. 추가 Maven 명령과 프로필을 사용하여 프로젝트 객체를 AEM 인스턴스에 배포할 수 있습니다.

### 프로젝트 만들기 {#create-project}

시작하려면 대부분 [AEM Eclipse 확장](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developer-tools/eclipse.html)을 사용하고 새 프로젝트 마법사를 따라 **AEM Sample Multi-Module Project**&#x200B;를 선택하여 릴리스된 버전의 원형 버전을 사용할 수 있습니다.

물론 마벤을 직접 불러오셔도 됩니다

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

* `XX`을(를) 최신 AEM Project Pretype의 [버전 번호](https://github.com/adobe/aem-project-archetype/blob/master/VERSIONS.md)로 설정합니다.
* [AEM에 대해 `aemVersion=cloud`을 Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html);\
   [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) 또는 온-프레미스에 대해 `aemVersion=6.5.0`을 설정합니다.
핵심 구성 요소가 AEM용 OTB를 클라우드로 제공하므로 핵심 구성 요소 종속성은 비 클라우드 aem 버전에 대해서만 추가됩니다.
서비스.
* `appTitle="My Site"`을(를) 조정하여 웹 사이트 제목과 구성 요소 그룹을 정의합니다.
* `appId="mysite"`을 조정하여 클라이언트 라이브러리 이름은 물론 구성 요소, 구성 요소, 구성 및 컨텐츠 폴더 이름을 정의합니다.
* `groupId="com.mysite"`을(를) 조정하여 Maven groupId 및 Java 소스 패키지를 정의합니다.
* 사용 가능한 속성 목록을 조회하여 조정할 추가 정보가 있는지 확인합니다.

>[!NOTE]
>
>maven 빌드 프로세스에 repo.adobe.com을 자동으로 추가하려면 `adobe-public` 프로필을 Maven `settings.xml` 파일에 추가하는 것이 좋습니다.
>
>POM [의 예제는 ](https://helpx.adobe.com/experience-manager/kb/SetUpTheAdobeMavenRepository.html)에서 찾을 수 있습니다.

### 속성 {#properties}

원형 유형을 사용하여 프로젝트를 만들 때 다음 속성을 사용할 수 있습니다.

| 이름 | 기본값 | 설명 |
--------------------------|----------------|--------------------
| `appTitle` |  | 애플리케이션 제목은 웹 사이트 제목 및 구성 요소 그룹(예:`"My Site"`). |
| `appId` |  | 기술 이름은 클라이언트 라이브러리 이름(예:`"mysite"`). |
| `artifactId` | *`${appId}`* | Base Maven 아티팩트 ID(예:`"mysite"`). |
| `groupId` |  | 기본 마벤 그룹 ID(예:`"com.mysite"`). |
| `package` | *`${groupId}`* | Java 소스 패키지(예:`"com.mysite"`). |
| `version` | `1.0-SNAPSHOT` | 프로젝트 버전(예:`1.0-SNAPSHOT`). |
| `aemVersion` | `6.5.0` | Target AEM 버전(Cloud Service](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html), [AEM의 경우 `cloud`일 수 있음)또는 `6.5.0`, [Adobe Managed Services](https://github.com/adobe/aem-project-archetype/tree/master/src/main/archetype/dispatcher.ams) 또는 온-프레미스)의 경우 `6.4.4`. |
| `sdkVersion` | `latest` | `aemVersion=cloud`SDK](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html) 버전을 지정할 수 있는 경우(예:`2020.02.2265.20200217T222518Z-200130`).[ |
| `includeDispatcherConfig` | `y` | `aemVersion` 값(`y` 또는 `n`일 수 있음)에 따라 클라우드 또는 AMS/on-premise용 디스패처 구성을 포함합니다. |
| `frontendModule` | `none` | 클라이언트 라이브러리를 생성하는 Webpack 프런트 엔드 빌드 모듈을 포함합니다(일반 사이트의 경우 `general` 또는 `none`일 수 있음).[SPA 편집기](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/headless/spa/introduction.html)를 구현하는 단일 페이지 앱의 경우 `angular` 또는 `react`일 수 있습니다. |
| `languageCountry` | `en_us` | 컨텐츠 구조를 만드는 언어 및 국가 코드(예:`en_us`). |
| `singleCountry` | `y` | 언어 마스터 콘텐츠 구조를 포함합니다(`y` 또는 `n` 가능). |
| `includeExamples` | `y` | [구성 요소 라이브러리](https://www.aemcomponents.dev/) 예제 사이트(`y` 또는 `n`일 수 있음)를 포함합니다. |
| `includeErrorHandler` | `n` | 전체 인스턴스(`y` 또는 `n`일 수 있음)에 대해 글로벌할 사용자 지정 404 응답 페이지를 포함합니다. |

>[!NOTE]
>
> 원형이 처음 대화형 모드에서 실행되는 경우 기본값을 가진 속성을 변경할 수 없습니다(자세한 내용은 [TRANYPE-308](https://issues.apache.org/jira/browse/ARCHETYPE-308) 참조). 끝 부분의 속성 확인이 거부되고 질문서가 반복되거나 명령줄에서 매개 변수를 전달하면(예:`-DoptionIncludeExamples=n`).

>[!NOTE]
>
>Windows에서 실행하고 디스패처 구성을 생성하는 경우 상위 명령 프롬프트 또는 Linux용 Windows 하위 시스템에서 실행 중이어야 합니다([문제 329](https://github.com/adobe/aem-project-archetype/issues/329) 참조).

### 프로파일 {#profiles}

생성된 maven 프로젝트는 `mvn install`을(를) 실행할 때 다른 배포 프로필을 지원합니다.

| 프로필 ID | 설명 |
--------------------------|------------------------------
| `autoInstallBundle` | felix 콘솔에 대한 maven-sling-plugin을 사용하여 핵심 번들 설치 |
| `autoInstallPackage` | localhost, 포트 4502에서 기본 작성 인스턴스를 작성하도록 패키지 관리자에 content-package-maven-plugin을 사용하여 ui.content 및 ui.apps 컨텐츠 패키지를 설치합니다. 호스트 이름 및 포트는 `aem.host` 및 `aem.port` 사용자 정의 속성으로 변경할 수 있습니다. |
| `autoInstallPackagePublish` | localhost, 포트 4503에서 기본 게시 인스턴스를 설정하려면 패키지 관리자에 content-package-maven-plugin을 사용하여 ui.content 및 ui.apps 컨텐츠 패키지를 설치합니다. 호스트 이름 및 포트는 `aem.host` 및 `aem.port` 사용자 정의 속성으로 변경할 수 있습니다. |
| `autoInstallSinglePackage` | localhost, 포트 4502에서 기본 작성 인스턴스를 작성하도록 패키지 관리자에 content-package-maven-plugin이 포함된 `all` 컨텐츠 패키지를 설치합니다. 호스트 이름 및 포트는 `aem.host` 및 `aem.port` 사용자 정의 속성으로 변경할 수 있습니다. |
| `autoInstallSinglePackagePublish` | localhost, 포트 4503에서 게시 인스턴스를 기본값으로 설정하려면 패키지 관리자에 content-package-maven-plugin이 포함된 `all` 내용 패키지를 설치합니다. 호스트 이름 및 포트는 `aem.host` 및 `aem.port` 사용자 정의 속성으로 변경할 수 있습니다. |
| `integrationTests` | AEM 인스턴스에서 제공된 통합 테스트를 실행합니다(`verify` 단계에만 해당). |

### {#building-and-installing} 작성 및 설치

프로젝트 루트 디렉토리에서 실행되는 모든 모듈을 빌드하려면 다음 마웬 명령을 사용합니다.

```shell
mvn clean install
```

실행 중인 AEM 인스턴스가 있는 경우 다음 Maven 명령을 사용하여 전체 프로젝트를 작성하고 패키지하여 AEM에 배포할 수 있습니다.

```shell
mvn clean install -PautoInstallPackage
```

게시 인스턴스에 배포하려면 이 명령을 실행합니다.

```shell
mvn clean install -PautoInstallPackagePublish
```

또는 게시 인스턴스에 배포하려면 이 명령을 실행합니다.

```shell
mvn clean install -PautoInstallPackage -Daem.port=4503
```

또는 번들만 작성자에게 배포하려면 이 명령을 실행합니다.

```shell
mvn clean install -PautoInstallBundle
```

## 상위 POM {#parent-pom}

프로젝트 루트(`<src-directory>/<project>/pom.xml`)에 있는 `pom.xml`은 상위 POM이라고 하며 프로젝트의 구조를 유도하고 프로젝트의 종속성 및 특정 전역 속성을 관리합니다.

### 전역 프로젝트 속성 {#global-properties}

상위 POM의 `<properties>` 섹션에서는 사용자 이름/암호, 호스트 이름/포트 등과 같이 AEM 인스턴스에서 프로젝트를 배포하는 데 중요한 몇 가지 전역 속성을 정의합니다.

이러한 속성은 개발자가 수행하는 가장 일반적인 빌드이므로 로컬 AEM 인스턴스에 배포하도록 설정됩니다. 게시 인스턴스와 작성자 인스턴스에 배포할 속성이 있습니다. 또한 자격 증명이 AEM 인스턴스로 인증하도록 설정되어 있는 경우도 있습니다. 기본 admin:admin 자격 증명이 사용됩니다.

이러한 속성은 상위 수준 환경에 배포할 때 재정의할 수 있도록 설정됩니다. 이러한 방식으로 POM 파일은 변경할 필요가 없지만 `aem.host` 및 `sling.password` 같은 변수는 명령줄 인수를 통해 재정의할 수 있습니다.

```shell
mvn -PautoInstallPackage clean install -Daem.host=production.hostname -Dsling.password=productionpasswd
```

### 모듈 구조 {#module-structure}

상위 POM의 `<modules>` 섹션에서는 프로젝트가 빌드할 모듈을 정의합니다. 기본적으로 프로젝트는 [이전에 정의한 표준 모듈을 만듭니다](#what-you-get):코어, ui.apps, ui.content, ui.tests 및 it.launcher. 프로젝트의 진화에 따라 모듈을 더 추가할 수 있습니다.

### 종속성 {#dependencies}

상위 POM의 `<dependencyManagement>` 섹션에서는 프로젝트에 사용되는 API의 모든 종속성 및 버전을 정의합니다. 버전은 상위 POM에서 관리해야 합니다. 코어 및 ui.apps와 같은 하위 모듈에는 버전 정보가 포함되지 않아야 합니다.

#### Uber-Jar {#uber-jar}

주요 종속성 중 하나는 [AEM uber-jar](https://docs.adobe.com/content/help/en/experience-manager-65/developing/devtools/ht-projects-maven.html#ExperienceManagerAPIDependencies)입니다. 여기에는 AEM 버전에 대한 단일 종속성 항목이 포함된 모든 AEM API가 포함됩니다.

>[!NOTE]
>
>가장 좋은 방법은 AEM의 대상 버전과 일치하도록 uber-jar 버전을 업데이트하는 것입니다. 예를 들어 AEM 6.4에 배포할 계획인 경우 uber-jar 버전을 6.4.0 버전으로 업데이트해야 합니다.

#### 코어 구성 요소 {#core-components}

물론 AEM 프로젝트 원형을 활용합니다.

핵심 구성 요소는 기본 런타임 모드에서 자동으로 AEM에 설치되고 샘플 WKND 사이트에서 사용됩니다. [프로덕션 실행 모드](https://docs.adobe.com/content/help/en/experience-manager-65/administering/security/production-ready.html)(`nosamplecontent`)에서는 핵심 구성 요소를 사용할 수 없습니다.

따라서 모든 배포에서 핵심 구성 요소를 활용하려면 마스터 프로젝트의 일부로 해당 구성 요소를 포함하는 것이 좋습니다.

>[!NOTE]
>
>핵심 구성 요소의 각 릴리스에는 일반적으로 AEM 프로젝트 원형 릴리스가 따르므로 최신 원형에서는 핵심 구성 요소의 최신 버전이 사용됩니다.
>
>그러나 새 버전의 기본 유형은 새 버전의 핵심 구성 요소를 직접 따르지 않을 수 있으므로 핵심 구성 요소에 대한 종속성을 최신 버전으로 업데이트할 수 있습니다.

>[!NOTE]
>
>core.wcm.components.examples는 핵심 구성 요소의 예를 보여주는 샘플 페이지 세트입니다. 프로덕션 프로젝트를 배포할 때 이 종속성 및 하위 패키지 포함을 제거하는 것이 좋습니다.

## 테스트 {#testing}

프로젝트에 포함된 3가지 테스트 수준이 있으며 테스트 유형은 서로 다르므로 서로 다른 방법이나 다른 위치에서 실행됩니다.

* 핵심 단위 테스트:번들에 포함된 코드의 클래식 단위 테스트가 표시됩니다. 테스트하려면 다음을 실행합니다.
   * `mvn clean test`
* 서버측 통합 테스트:이러한 테스트는 AEM 환경에서(예: AEM 서버)와 같이 실행되며, 테스트하려면 다음을 실행합니다.
   * `mvn clean verify -PintegrationTests`
* 클라이언트측 Hobes.js 테스트:브라우저 측 동작을 확인하는 JavaScript 기반 브라우저 측 테스트입니다. 테스트하려면:
   1. 페이지를 작성하는 것처럼 브라우저에서 AEM을 로드합니다.
   1. [개발자 모드](https://docs.adobe.com/content/help/en/experience-manager-65/developing/components/developer-mode.html)에서 페이지를 엽니다.
   1. 왼쪽 패널을 열고 **테스트** 탭으로 전환합니다.
   1. 생성된 **MyName 테스트**&#x200B;를 찾아 실행합니다.

## 다음 단계 {#next-steps}

AEM 프로젝트 원형을 만들고 설치했습니다. 지금 뭐? 전형은 작지만, 권장 우수 사례에 따라 구성된 강력한 AEM 기능의 많은 예제로 구성되어 있습니다. 프로젝트에서 이러한 기능을 활용할 수 있는 방법에 대한 설명입니다. 모든 프로젝트의 경우 다음을 수행해야 합니다.

* [기존 핵심 구성 요소를 확장하여 구성 요소 사용자 정의](/help/developing/customizing.md)
* [추가 템플릿 추가](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)
* [현지화 구조 조정](https://docs.adobe.com/content/help/en/experience-manager-65/administering/introduction/tc-prep.html)
* [프런트 엔드 빌드 모듈에 대한 자세한 내용](uifrontend.md)

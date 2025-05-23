---
title: AEM Project Archetype 사용
description: AEM Project Archetype을 사용하여 사용자 자신의 AEM 프로젝트의 시작점으로서 모범 사례 기반 Adobe Experience Manager 프로젝트를 생성하는 방법에 대해 알아봅니다.
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: a3978d8b-4904-42aa-9ee2-9c1f884327bb
source-git-commit: bd92a5d1884056ca7b44ea28e5817d8bde10a4d9
workflow-type: tm+mt
source-wordcount: '1092'
ht-degree: 100%

---


# AEM Project Archetype 사용 {#using-the-archetype}

이 문서에서는 AEM Project Archetype을 사용하여 사용자 자신의 AEM 프로젝트의 시작점으로서 모범 사례 기반 Adobe Experience Manager 프로젝트를 생성하는 방법에 대해 설명합니다.

여기에서는 일반적인 사용 패턴과 Archetype이 사용자에게 미치는 영향에 중점을 둡니다. 자세한 빌드 옵션 및 기술 지침은 해당 Archetype의 GitHub 저장소에 있는 설명서를 참조하십시오.

>[!TIP]
>
>최신 AEM Project Archetype 및 관련 기술 문서는 [GitHub에서 찾을 수 있습니다.](https://github.com/adobe/aem-project-archetype)

## 시작하기 {#getting-started}

Project Archetype을 통해 AEM에서 개발 시작하기가 수월해집니다. Archetype을 사용하여 여러 방식으로 첫 단계를 수행할 수 있습니다.

* **WKND 튜토리얼** - Archetype을 활용하는 방법 등 도입된 AEM 개발에 대한 실용적인 예제(Archetype 사용을 통한 간단한 프로젝트 구현하기에 대한 안내)를 알아보려면 [AEM Sites 시작하기 - WKND 튜토리얼](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html?lang=ko)을 참조하십시오.
* **WKND 이벤트 튜토리얼** - AEM에서 단일 페이지 애플리케이션(SPA) 개발에 관심이 있다면 전용 [WKND 이벤트 튜토리얼](https://helpx.adobe.com/kr/experience-manager/kt/sites/using/getting-started-spa-wknd-tutorial-develop.html)에 대해 자세히 알아보십시오.
* **스스로 시작해 보십시오.** - [GitHub에서 사용 가능한 최신 프로젝트 Archetype](https://github.com/adobe/aem-project-archetype)을 손쉽게 다운로드하고 직접 첫 번째 프로젝트를 만들 수 있습니다.

## Archetype을 사용하는 방법 {#how-to-use-the-archetype}

Archetype을 사용하는 첫 번째 단계는 로컬 파일 구조에 [모듈](#what-you-get)을 생성하는 프로젝트를 만드는 것입니다. 프로젝트 생성의 일부로 프로젝트 이름, 버전, 다양한 옵션 활성화 등 다수의 프로젝트 속성을 정의할 수 있습니다.

>[!TIP]
>
>Archetype을 빌드할 때마다 [아래에 링크된](#what-you-get) 각 모듈의 기술 세부 사항과 사용법을 제공하는 일련의 추가 정보도 생성됩니다.

Maven과 함께 프로젝트를 빌드하면 AEM으로 배포 가능한 아티팩트(패키지 및 OSGi 번들)를 제작할 수 있습니다. 추가 Maven 명령 및 프로필을 사용하여 프로젝트 아티팩트를 AEM으로 배포할 수 있습니다.

## Archetype을 통해 누릴 수 있는 혜택 {#what-you-get}

Archetype은 모듈로 구성되며, 이 모듈은 모두 Archetype을 사용할 때 자동으로 생성됩니다.

* **[core](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/core)**&#x200B;는 모든 핵심 기능(OSGi 서비스, 리스너 및 스케줄러 등)과 구성 요소 관련 Java 코드(서블릿 및 요청 필터 등)가 포함된 Java 번들입니다.
* **[it.tests](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/it.tests)**&#x200B;는 Java 기반 통합 테스트입니다.
* **[ui.apps](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.apps)**&#x200B;에는 일부 프로젝트 `/apps` 및 `/etc`(예: JS 및 CSS Clientlib, 구성 요소 및 템플릿)가 포함됩니다.
* **[ui.content](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.content)**&#x200B;에는 ui.apps 모듈에서 구성 요소를 사용하는 샘플 콘텐츠가 포함됩니다.
* **[ui.config](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.config)**&#x200B;에는 프로젝트의 실행 모드별 OSGi configs가 포함됩니다.
* **[ui.frontend.general](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.frontend.general)**&#x200B;에는 일반 Webpack 기반 프론트엔드 빌드 모듈 사용에 필요한 아티팩트가 포함됩니다(선택 사항).
* **[ui.frontend.react](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.frontend.react)****(선택 사항)**&#x200B;에는 React에 따라 Archetype을 사용하여 SPA 프로젝트를 만들 때 필요한 아티팩트가 포함됩니다(선택 사항, 빌드 매개 변수에 따라 다름).
* **[ui.frontend.angular](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.frontend.angular)****(선택 사항)**&#x200B;에는 Angular에 따라 Archetype을 사용하여 SPA 프로젝트를 만들 때 필요한 아티팩트가 포함됩니다(선택 사항, 빌드 매개 변수에 따라 다름).
* **[ui.tests](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.tests)**&#x200B;에는 Selenium 기반 UI 테스트가 포함됩니다.
* **[all](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/all)**&#x200B;에는 공급업체 종속성 등 컴파일된 모든 모듈(번들 및 콘텐츠 패키지)을 임베드하는 단일 콘텐츠 패키지입니다.
* **[dispatcher.ams](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/dispatcher.ams)**&#x200B;에는 AMS/온프레미스 프로젝트에 대한 기본 Dispatcher 구성이 포함되어 있습니다(선택 사항, 빌드 매개 변수에 따라 다름).
* **[dispatcher.cloud](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/dispatcher.cloud)**&#x200B;에는 AEMaaCS 프로젝트에 대한 기본 Dispatcher 구성이 포함됩니다(선택 사항, 빌드 매개 변수에 따라 다름).

![콘텐츠 패키지 구성](/help/assets/content-package-organization.png)

애플리케이션, 콘텐츠와 필요한 OSGi 번들을 표시하는 콘텐츠 패키지로서 Maven에 표시된 Archetype의 모듈을 AEM으로 배포합니다.

## 상위 POM {#parent-pom}

프로젝트 루트(`<src-directory>/<project>/pom.xml`)의 `pom.xml`는 상위 POM이라고 합니다. 이는 프로젝트 구조를 유도하고 프로젝트에 대한 종속성 및 특정 전역 속성을 관리합니다.

### 전역 프로젝트 속성 {#global-properties}

상위 POM의 `<properties>` 섹션은 AEM 인스턴스에서 프로젝트를 구현하는 데 중요한 몇 가지 전역 속성(예: 사용자 이름/암호, 호스트 이름/포트 등)을 정의합니다.

이 속성을 설정하여 로컬 AEM 인스턴스로 배포합니다. 이는 개발자가 수행할 수 있는 가장 일반적인 빌드입니다. 작성자 인스턴스와 게시 인스턴스에 배포되는 속성이 있습니다. 여기서 자격 증명을 설정하여 AEM 인스턴스를 인증합니다. 기본 `admin:admin` 자격 증명이 사용됩니다.

상위 수준의 환경에 배포할 때 이러한 속성이 재정의될 수 있도록 설정합니다. 이러한 방식으로 POM 파일은 변경될 수 없지만 `aem.host` 및 `sling.password`와 같은 변수는 다음 명령줄 인수를 통해 재정의될 수 있습니다.

```shell
mvn -PautoInstallPackage clean install -Daem.host=production.hostname -Dsling.password=productionpasswd
```

### 모듈 구조 {#module-structure}

상위 POM의 `<modules>` 섹션은 프로젝트가 빌드할 모듈을 정의합니다. 기본적으로 프로젝트는 [이전에 정의된 표준 모듈을 빌드합니다.](#what-you-get) 프로젝트가 커지면 언제든지 모듈을 추가할 수 있습니다.

### 종속성 {#dependencies}

상위 POM의 `<dependencyManagement>` 섹션은 프로젝트에 사용되는 종속성과 API 버전을 모두 정의합니다. 상위 POM에서 버전을 관리해야 합니다. 하위 모듈에는 버전 정보가 포함되어서는 안 됩니다.

#### Uber-Jar {#uber-jar}

주요 종속성 중 하나는 [AEM Java API Jar입니다.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-as-a-cloud-service-sdk.html?lang=ko) AEM 버전용 단일 종속성 목록이 있는 모든 AEM API가 여기에 포함됩니다.

>[!NOTE]
>
>AEM의 대상 버전에 일치하는 uber-jar 버전을 업데이트하는 것이 좋습니다. 예를 들어 AEM 6.5에 배포하려는 경우 uber-jar 버전을 6.5.X로 업데이트해야 합니다(`X`는 최신 서비스 팩).

#### 핵심 구성 요소 {#core-components}

Archetype은 [핵심 구성 요소를 활용합니다.](/help/introduction.md) 따라서 모든 배포에서 핵심 구성 요소를 활용하려면 Maven 프로젝트의 일부로 포함시키는 것이 좋습니다.

core.wcm.components.예제는 핵심 구성 요소의 예제를 나타내는 샘플 페이지 세트입니다. 제작용 프로젝트를 배포할 때 이 종속성과 하위 패키지 포함을 제거하는 것이 좋습니다.

>[!NOTE]
>
>핵심 구성 요소와 Archetype은 별도의 GitHub 프로젝트로 유지 관리되므로 각각의 릴리스가 다릅니다.
>
>각 Archetype의 릴리스는 릴리스 당시 사용 가능한 핵심 구성 요소의 최신 릴리스를 활용합니다. 단, 핵심 구성 요소에 대한 종속성을 수동으로 업데이트할 수도 있습니다.

## 테스트 {#testing}

세 가지 수준의 테스트가 프로젝트에 포함되어 있습니다. 테스트의 유형이 서로 다르기 때문에 실행 방법 및 위치가 각각 다릅니다.

* **[단위 테스트](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/core)** - 번들에 포함된 코드의 클래식 단위 테스트
* **[통합 테스트](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/it.tests)** - AEM 환경(AEM 서버)에서 유사 단위 테스트를 실행하는 서버측 통합 테스트
* **[UI 테스트](https://github.com/adobe/aem-project-archetype/tree/develop/src/main/archetype/ui.tests)** - 브라우저측 동작을 확인하는 Selenium 기반 브라우저측 테스트

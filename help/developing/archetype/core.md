---
title: AEM 프로젝트 원형의 핵심 모듈
description: AEM 프로젝트 원형의 핵심 모듈
translation-type: tm+mt
source-git-commit: 9d737b31efc8c346775ea5296f7599295af07cf1
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 0%

---


# AEM 프로젝트 원형의 핵심 모듈 {#core-module}

핵심 마스터 모듈(`<src-directory>/<project>/core`)에는 구현에 필요한 모든 Java 코드가 포함되어 있습니다. 이 모듈은 모든 Java 코드를 패키징하고 AEM 인스턴스에 OSGi 번들로 배포합니다.

`<src-directory>/<project>/core/pom.xml`에 정의된 Maven Bundle 플러그인은 AEM OSGi 컨테이너에서 인식할 수 있는 OSGi 번들에 Java 코드를 컴파일합니다. Sling Models의 위치가 정의된 위치에 유의하십시오.

핵심 번들을 상위 수준 환경의 ui.apps 모듈과 독립적으로 배포해야 하는 것은 드물지만, 핵심 번들을 직접 배포하는 것은 로컬 개발/테스트 중에 유용합니다. Maven Sling 플러그인을 사용하면 [부모 POM](/help/developing/archetype/using.md#parent-pom)에 정의된 대로 `autoInstallBundle` 프로파일을 직접 활용하여 핵심 번들을 AEM에 직접 배포할 수 있습니다.

```shell
mvn -PautoInstallBundle clean install
```

성공적으로 실행되면 `http://<host>:<port>/system/console/bundles`에 있는 번들 콘솔을 볼 수 있습니다.

##  단위 테스트 {#unit-tests}

핵심 모듈의 단위 테스트는 번들에 포함된 코드의 클래식 단위 테스트를 보여줍니다. 테스트하려면 다음을 실행합니다.

```shell
mvn clean test
```

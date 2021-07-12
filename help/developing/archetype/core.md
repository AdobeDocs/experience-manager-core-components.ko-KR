---
title: AEM 프로젝트 원형 코어 모듈
description: AEM 프로젝트 원형 코어 모듈
feature: 핵심 구성 요소, AEM 프로젝트 원형
role: Architect, Developer, Admin
exl-id: 49e80d8c-2b41-4c42-b45e-c2e3b4b16a59
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# AEM 프로젝트 원형 코어 모듈 {#core-module}

코어 maven 모듈(`<src-directory>/<project>/core`)에는 구현에 필요한 모든 Java 코드가 포함되어 있습니다. 이 모듈은 모든 Java 코드를 패키징하고 OSGi 번들로 AEM 인스턴스에 배포합니다.

`<src-directory>/<project>/core/pom.xml`에 정의된 Maven 번들 플러그인은 AEM OSGi 컨테이너에서 인식할 수 있는 OSGi 번들로 Java 코드를 컴파일합니다. 여기서 Sling 모델의 위치가 정의됩니다.

코어 번들을 상위 수준 환경에서 ui.apps 모듈과 독립적으로 배포해야 하는 경우는 거의 없지만, 코어 번들을 직접 배포하는 것은 로컬 개발/테스트 중에 유용합니다. Maven Sling 플러그인을 사용하면 [상위 POM](/help/developing/archetype/using.md#parent-pom)에 정의된 대로 `autoInstallBundle` 프로필을 직접 활용하여 코어 번들을 AEM에 배포할 수 있습니다.

```shell
mvn -PautoInstallBundle clean install
```

성공적으로 실행되면 `http://<host>:<port>/system/console/bundles`에 번들 콘솔을 볼 수 있습니다.

##  단위 테스트 {#unit-tests}

코어 모듈의 단위 테스트는 번들에 포함된 코드의 클래식 단위 테스트를 보여줍니다. 테스트하려면 다음을 실행합니다.

```shell
mvn clean test
```

---
title: AEM 프로젝트 원형형의 핵심 모듈
description: AEM 프로젝트 원형형의 핵심 모듈
translation-type: tm+mt
source-git-commit: 6f7166c46940ed451721e0760d565d58efe412ab
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 0%

---


# AEM 프로젝트 원형형의 핵심 모듈 {#core-module}

핵심 마스터 모듈(`<src-directory>/<project>/core`)에는 구현에 필요한 모든 Java 코드가 포함되어 있습니다. 이 모듈은 모든 Java 코드를 패키지하고 AEM 인스턴스에 OSGi 번들로 배포합니다.

에 정의된 Maven 번들 플러그인 `<src-directory>/<project>/core/pom.xml` 은 AEM의 OSGi 컨테이너에서 인식할 수 있는 OSGi 번들에 Java 코드를 컴파일할 책임이 있습니다. 여기서 슬링 모델의 위치가 정의됩니다.

핵심 번들을 상위 수준 환경에서 ui.apps 모듈과 독립적으로 배포해야 하는 경우는 드물지만, 로컬 개발/테스트 중에 바로 핵심 번들을 배포하는 것이 유용합니다. Maven Sling 플러그인을 사용하면 `autoInstallBundle` 상위 POM에 정의된 대로 프로파일을 활용하여 코어 번들을 AEM에 직접 배포할 수 있습니다 [](/help/developing/archetype/using.md#parent-pom).

```
mvn -PautoInstallBundle clean install
```

번들 콘솔이 성공적으로 실행되면 을 참조하십시오 `http://<host>:<port>/system/console/bundles`.

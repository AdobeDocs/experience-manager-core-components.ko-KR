---
title: AEM 프로젝트 원형형의 핵심 모듈
description: AEM 프로젝트 원형형의 핵심 모듈
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# AEM 프로젝트 원형형의 핵심 모듈 {#core-module}

핵심 마스터 모듈(`<src-directory>/<project>/core`)에는 구현에 필요한 모든 Java 코드가 포함되어 있습니다. 이 모듈은 모든 Java 코드를 패키지하여 AEM 인스턴스에 OSGi 번들로 배포합니다.

에 정의된 Maven 번들 플러그인은 AEM의 OSGi 컨테이너에서 인식할 수 있는 OSGi 번들로 Java 코드를 컴파일할 책임이 `<src-directory>/<project>/core/pom.xml` 있습니다. Sling Models의 위치는 여기에서 정의됩니다.

코어 번들을 상위 수준 환경에서 ui.apps 모듈과 독립적으로 배포해야 하는 것은 드문 일이지만, 핵심 번들을 직접 배포하는 것은 로컬 개발/테스트 중에 유용합니다. Maven Sling 플러그인을 사용하면 핵심 번들을 `autoInstallBundle` 상위 POM에 정의된 대로 프로파일을 직접 활용하여 AEM에 배포할 수 있습니다 [](overview.md#parent-pom).

```
mvn -PautoInstallBundle clean install
```

성공적으로 실행되면, 에서 번들 콘솔을 볼 수 있습니다 `http://<host>:<port>/system/console/bundles`.

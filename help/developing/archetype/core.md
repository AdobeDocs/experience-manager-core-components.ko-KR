---
title: AEM Project Archetype의 핵심 모듈
description: AEM Project Archetype의 핵심 모듈
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 49e80d8c-2b41-4c42-b45e-c2e3b4b16a59
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: ht
source-wordcount: '182'
ht-degree: 100%

---

# AEM Project Archetype의 핵심 모듈 {#core-module}

핵심 Maven 모듈(`<src-directory>/<project>/core`)에는 구현에 필요한 모든 Java 코드가 포함됩니다. 모듈은 모든 Java 코드를 패키징하고 OSGi 번들로 AEM 인스턴스에 배포합니다.

`<src-directory>/<project>/core/pom.xml`에 정의된 Maven 번들 플러그인은 AEM의 OSGi 컨테이너가 인식할 수 있는 OSGi 번들로 Java 코드를 컴파일합니다. 여기서 슬링 모델 위치를 정의할 수 있습니다.

상위 수준의 환경에서 ui.apps 모듈과 별개로 핵심 번들을 배포하는 경우는 드물지만 로컬 개발/테스트 진행 과정에서 핵심 번들을 직접 배포하는 경우 유용합니다. Maven 번들 플러그인을 통해 핵심 번들을 [상위 POM](/help/developing/archetype/using.md#parent-pom)에서 정의한 `autoInstallBundle` 프로필을 활용하는 AEM에 직접 배포할 수 있습니다.

```shell
mvn -PautoInstallBundle clean install
```

실행이 완료되면 `http://<host>:<port>/system/console/bundles`에서 번들 콘솔을 확인할 수 있습니다.

## 단위 테스트 {#unit-tests}

핵심 모듈의 단위 테스트는 번들에 포함된 코드에 대한 클래식 단위 테스트를 보여 줍니다. 테스트를 하려면 다음을 실행합니다.

```shell
mvn clean test
```

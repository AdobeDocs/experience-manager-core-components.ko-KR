---
title: 사전 컴파일된 번들 스크립트
description: OSGi 번들을 통해 Adobe Experience Manager Cloud Service에 구성 요소 스크립트를 배포하는 방법을 알아봅니다.
source-git-commit: 56464decc8d6ae3cef68d62bfe459bceda0539ef
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 0%

---

# 사전 컴파일된 번들 스크립트

AEM as a Cloud Service은 [`ui.apps`](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#code-packages-%2F-osgi-bundles) 구성 요소 스크립트를 사전 컴파일된 번들 스크립트로 배포하도록 지원합니다. 이렇게 하면 개발자가 빌드 시 스크립트를 미리 컴파일하고 OSGi 번들로 패키지할 수 있습니다.

## OSGi 번들을 통해 미리 컴파일된 스크립트를 배포하는 것의 이점

스크립트를 사전 컴파일된 번들 스크립트로 배포하면 다음과 같은 이점이 있습니다.

+ 빌드 시 스크립트를 컴파일하면 개발자가 개발 프로세스 초기에 오류를 발견할 수 있습니다
+ Java API 스크립트 종속성은 `Import-Package` 및 `Export-Package` 번들 헤더를 통해 명시적으로 정의됩니다
+ 상속(`sling:resourceSuperType`)과 다른 리소스 유형(예: HTL의 `data-sly-resource` 블록 요소 또는 `sling:include` JSP 태그를 통해)에 대한 위임을 번들의 메타 데이터를 통해 매핑할 수 있습니다
+ 리소스 유형 버전 관리는 Java API와 유사한 방식으로 적용할 수 있습니다

## 미리 컴파일 및 패키지 가져오기

[`htl-maven-plugin`](https://sling.apache.org/components/htl-maven-plugin/index.html)은 HTL 스크립트의 구문을 확인할 수 있지만 HTL 스크립트를 Java 클래스로 전달하는 데 사용할 수도 있습니다. 그런 다음 Maven 프로젝트의 `generated-sources` 폴더에 추가되고 `maven-compiler-plugin`에 의해 선택됩니다.

[`bnd-maven-plugin`](https://github.com/bndtools/bnd/tree/master/maven/bnd-maven-plugin)을 추가하여 Java API 가져오기에 대한 OSGi 번들의 메타데이터를 생성할 수 있습니다.

## 상속 및 위임

OSGi 프레임워크는 [요구 사항 및 기능](https://docs.osgi.org/specification/osgi.core/7.0.0/framework.module.html#framework.module.dependencies)을 정의하여 다양한 구성 요소 간의 계약을 표현하는 강력한 방법을 제공합니다. 이러한 내용은 메타 데이터를 통해 설명되며 런타임 시 적용됩니다. 번들 스크립트는 이 메커니즘을 사용하여 상속 관계(`sling:resourceSuperType`)와 위임(렌더링 프로세스의 다른 리소스 유형 포함)을 모두 나타냅니다.

[scriptingbundle-maven-plugin](https://sling.apache.org/components/scriptingbundle-maven-plugin/bnd.html) 프로젝트의 `bnd` 플러그인은 [`ui.apps`](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#code-packages-%2F-osgi-bundles) 컨텐츠 패키지에서 제공하는 스크립트에 해당하는 요구 사항 및 기능을 추출하는 데 사용할 수 있습니다.

## AEM 프로젝트 원형 지원

버전 31부터 [AEM Project Archetype](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/developing/archetype/using.html)을 사용하여 사전 컴파일된 번들 스크립트를 사용하도록 AEM을 Cloud Service 프로젝트로 올바르게 설정할 수 있습니다. 또한 AEM 프로젝트 원형 은 [AEM as a Cloud Service SDK Build Analyzer Maven 플러그인](/help/developing/archetype/build-analyzer-maven-plugin.md)을 구성하여 Java 패키지 레벨과 스크립트 수준 종속성을 확인합니다.

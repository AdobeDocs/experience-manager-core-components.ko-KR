---
title: 미리 컴파일된 번들형 스크립트
description: OSGi 번들을 통해 구성 요소 스크립트를 Adobe Experience Manager Cloud Service로 배포하는 방법을 살펴보십시오.
exl-id: 3edc388f-01b2-45cc-bd56-f22e5a5a8624
source-git-commit: 767f83fbad11a108aab25be2b77759af3c08b864
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 100%

---

# 미리 컴파일된 번들형 스크립트

AEM as a Cloud Service는 미리 컴파일된 번들형 스크립트로 [`ui.apps` 구성 요소 스크립트](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#code-packages-%2F-osgi-bundles)를 지원합니다. 이렇게 하면 개발자는 작성 시간에 스크립트를 미리 컴파일하고 OSGi 번들로 패키징할 수 있습니다.

## OSGi 번들을 통해 미리 컴파일된 스크립트 배포의 장점

미리 컴파일된 번들형 스크립트로 스크립트를 배포하면 다음과 같은 혜택을 누릴 수 있습니다.

+ 작성 시간에 스크립트를 컴파일하면 개발자는 개발 프로세스에서 오류를 조기에 탐색할 수 있음
+ Java API 스크립트 종속 항목은 `Import-Package` 및 `Export-Package` 번들 헤더를 통해 명시적으로 정의됨
+ 상속(`sling:resourceSuperType`을 통해) 및 기타 리소스 유형(예: HTL의 `data-sly-resource` 블록 요소나 `sling:include`JSP 태그를 통해)으로의 전달이 번들의 메타데이터를 통해 매핑될 수 있음
+ 리소스 유형 버전 관리는 이와 유사한 방식으로 Java API에 적용될 수 있음

## 사전 컴파일링 및 패키지 가져오기

[`htl-maven-plugin`](https://sling.apache.org/components/htl-maven-plugin/index.html)는 HTL 스크립트의 구문을 확인할 수 있지만, HTL 스크립트를 Java 클래스로 변환 컴파일하는 데 사용할 수도 있습니다. 그리고 나서 Maven 프로젝트의 `generated-sources` 폴더에 이를 추가하고 `maven-compiler-plugin`에서 선택합니다.

[`bnd-maven-plugin`](https://github.com/bndtools/bnd/tree/master/maven/bnd-maven-plugin)을 추가하여 OSGi 번들의 메타데이터를 생성하고 Java API를 가져올 수 있습니다.

## 상속 및 전달

OSGi 프레임워크를 통해 여러 구성 요소 간 약정을 표현할 수 있는 [요구 사항 및 기능](https://docs.osgi.org/specification/osgi.core/7.0.0/framework.module.html#framework.module.dependencies)을 정의하는 강력한 방법이 제공됩니다. 이는 메타데이터를 통해 설명되고 런타임 시 적용됩니다. 번들형 스크립트는 이 메커니즘을 사용하여 상속 관계(`sling:resourceSuperType`)와 전달을 모두 표현합니다(렌더링 프로세스에 기타 리소스 유형 포함됨).

`bnd`[scriptingbundle-maven-plugin](https://sling.apache.org/components/scriptingbundle-maven-plugin/bnd.html) 프로젝트의 플러그인을 사용하여 [`ui.apps`](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#code-packages-%2F-osgi-bundles) 콘텐츠 패키지에서 제공하는 스크립트에 해당되는 요구 사항 및 기능을 추출할 수 있습니다.

## AEM Project Archetype 지원

버전 31부터는 [AEM Project Archetype](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/developing/archetype/using.html)를 통해 미리 컴파일된 번들형 스크립트를 사용하는 AEM as a Cloud Service 프로젝트를 제대로 설정할 수 있습니다. 또한, AEM Project Archetype는 [AEM as a Cloud Service SDK Build Analyzer Maven 플러그인](/help/developing/archetype/build-analyzer-maven-plugin.md)을 구성하여 Java 패키지 수준 및 스크립트 수준 종속 항목을 확인할 수 있습니다.

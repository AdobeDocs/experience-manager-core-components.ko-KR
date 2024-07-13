---
title: AEM as a Cloud Service SDK Build Analyzer Maven Plugin
description: 로컬 Maven Build Analyzer Plugin 설명서
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: de26b310-a294-42d6-a0db-91f6036a328c
source-git-commit: 554be9539428cd75462a38fc45f1bece04baf066
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 100%

---

# AEM as a Cloud Service SDK Build Analyzer Maven Plugin {#maven-analyzer-plugin}

AEM as a Cloud Service SDK Build Analyzer Maven Plugin은 다양한 콘텐츠 패키지 프로젝트의 구조를 분석합니다.

AEM Maven 프로젝트에 이 옵션을 포함시키는 방법에 대한 자세한 내용은 [Maven Plugin 설명서](https://github.com/adobe/aemanalyser-maven-plugin/blob/main/aemanalyser-maven-plugin/README.md)를 참조하십시오.

>[!NOTE]
>
>[Maven 중앙 저장소](https://repo1.maven.org/maven2/com/adobe/aem/aemanalyser-maven-plugin/)에 있는 최신 버전의 플러그인을 참조하기 위해 Maven 프로젝트를 업데이트하는 것이 좋습니다.

플러그인은 프로젝트에서 구성한 SDK가 아닌 사용 가능한 최신 SDK를 사용합니다.

다음 표에서는 이 단계의 일부로 실행되는 분석기를 설명합니다. <!-- Note that some are executed in the local SDK, while others are only executed during the Cloud Manager pipeline deployment. -->

| 모듈 | 기능, 예제 및 문제 해결 | 로컬 SDK | Cloud Manager |
|---|---|---|---|
| `api-regions-exportsimports` | Maven 프로젝트에 포함된 다른 번들의 패키지 내보내기 선언이 충족하는 패키지 가져오기 선언이 모든 OSGi 번들에 있는지 확인합니다. 오류의 형태는 다음과 같습니다. <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Bundle org.acme:mybundle:0.0.1-SNAPSHOT is importing package(s) org.acme.foo in start level 20 but no bundle is exporting these for that start level.`<p> </p>문제를 해결하려면 배포에 패키지를 제공하는 번들이 포함되어 있는지 확인합니다. 아니면 내보내려는 번들의 매니페스트를 살펴봄으로써 잘못된 이름 또는 잘못된 버전이 사용되었는지를 확인할 수 있습니다. | 예 | 예 |
| `bundle-unversioned-packages` | OSGi 번들이 Export-Package 선언이 있는 버전과 Import-Package 선언이 있는 버전 범위를 지정하는지 확인하십시오. 오류의 형태는 다음과 같습니다. <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Bundle org.acme:mybundle:0.0.1-SNAPSHOT is exporting package org.acme.foo without a version.`<p> </p>문제를 해결하려면 내보낼 버전을 지정하는 해당 패키지에 `package-info.java`를 추가하십시오. | 예 | 예 |
| `requirements-capabilities` | Maven 프로젝트에 포함된 다른 번들의 기능 선언이 OSGi 번들로 제작된 요구 사항 선언을 모두 충족하는지 확인합니다. 오류의 형태는 다음과 같습니다. <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Artifact org.acme:mybundle:0.0.1-SNAPSHOT requires org.foo.bar in start level 20 but no artifact is providing a matching capability in this start level.`<p> </p> 문제를 해결하려면 기능을 선언하려는 번들의 매니페스트를 살펴봄으로써 누락된 이유를 확인하거나, 필요한 번들의 매니페스트를 체크인하여 해당 요구 사항이 정확한지 확인합니다. | 예 | 예 |
| `bundle-content` | 번들에 포함된 최초 콘텐츠가 AEM as a Cloud Service 클러스터된 환경에 문제가 되는 최초 콘텐츠 슬링으로 지정되는 경우 경고 메시지가 나타납니다. 경고 형태는 다음과 같습니다. <p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found initial content : [/]` <p> </p>문제를 해결하려면 최초 콘텐츠를 Repoinit 선언으로 변환하고 Repoinit 설명서를 참조하십시오. | 예 | 예 |
| `bundle-resources` | 번들에 포함된 리소스가 AEM as a Cloud Service 클러스터된 환경에 문제가 되는 번들 리소스 슬링으로 지정되는 경우 경고 메시지가 나타납니다. 경고 형태는 다음과 같습니다.<p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found bundle resources : [/libs/sling/explorer!/resources/explorer]`<p> </p> 문제를 해결하려면 리소스를 Repoinit 선언으로 변환하고 [Repoinit 설명서](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=ko#repo-init)를 참조하십시오. | 예 | 예 |
| `api-regions`<p> </p>`api-regions-check-order`<p> </p>`api-regions-dependencies`<p> </p>`api-regions-duplicates` | 이 분석기를 사용하여 기능 슬링 모드에 따라 아티팩트를 만드는 [모델 변환 프로세스](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html?lang=ko#deploying)를 보여 주는 콘텐츠 패키지 관련 세부 정보를 확인합니다. 오류가 발생하면 Adobe 고객 지원 센터에 보고해야 합니다. | 예 | 예 |
| `api-regions-crossfeature-dups` | 고객 OSGi 번들에 AEM as a Cloud Service의 공개 API를 오버라이드하는 패키지 내보내기 선언이 없는지 확인합니다.<p> </p>`[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Package overlap found between region global and bundle org.acme:mybundle:0.0.1.SNAPSHOT which comes from feature: [org.acme:myproject.analyse:slingosgifeature:0.0.1-SNAPSHOT]. Both export package: com.day.util`<p> </p>문제를 해결하려면 AEM 공개 API의 일부인 패키지 내보내기를 중단합니다. | 예 | 예 |
| `repoinit` | Repoinit 섹션의 구문을 모두 확인합니다. | 예 | 예 |
| `bundle-nativecode` | OSGi 번들이 기존 코드를 설치하지 않은지 확인합니다. | 예 | 예 |
| `configuration-api` | 중요 OSGi 구성을 확인합니다. <p> </p> `Configuration org.apache.felix.webconsole.internal.servlet.OsgiManager: Configuration is not allowed (com.mysite:mysite.all:1.0.0-SNAPSHOT\|com.mysite:mysite.ui.config:1.0.0-SNAPSHOT)` | 예 | 예 |
| `region-deprecated-api` | [더 이상 사용되지 않는 API](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/deprecated-apis.html?lang=ko)가 사용되고 있는지 확인합니다. <p> </p>`[WARNING] com.mysite:mysite.core:1.0.0-SNAPSHOT: Usage of deprecated package found : org.apache.sling.settings : Avoid these features at runtime: run modes, file system access (com.mysite:mysite.all:1.0.0-SNAPSHOT)` | 예 | 예 |
| `artifact-rules` | 아티팩트의 알려진 문제를 사전에 방지하기 위해 번들 및 패키지와 같은 종속 항목을 확인합니다.<p> </p>`[WARNING] [artifact-rules] com.adobe.acs:acs-aem-commons-bundle:5.0.4: Use at least version 5.0.10 (com.mysite:mysite.all:1.0.0-SNAPSHOT)` | 예 | 예 |
| `aem-env-var` | [변수 이름 지정 가이드](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html#variable-naming)에 따라 env vars의 사용을 확인합니다.<p> </p>`[ERROR] Configuration org.apache.felix.webconsole.internal.servlet.OsgiManager: Value for property 'port' must not use env vars prefixed with INTERNAL_ or ADOBE_ (com.mysite1:my-site-1.all:1.0.0-SNAPSHOT\|com.mysite1:my-site-1.ui.config:1.0.0-SNAPSHOT)` | 예 | 예 |
| `content-package-validation` | FileVault 유효성 검사기를 실행합니다. 기본적으로 jackrabbit-docviewparser가 활성화되며 배포 도중 설치될 내부 패키지의 xml에 대한 올바른 형식의 콘텐츠 구문을 검사합니다.<p> </p>`[main] WARN org.apache.sling.feature.analyser.task.impl.CheckContentPackages - ValidationViolation: "jackrabbit-docviewparser: Invalid XML found: The reference to entity "se" must end with the ';' delimiter.", filePath=jcr_root/apps/somename/configs/com.adobe.test.Invalid.xml, nodePath=/apps/somename/configs/com.adobe.test.Invalid`<p> </p>이를 해결하려면 분석기에서 지정한 파일에 xml 문제가 있는지 확인하십시오. | 예 | 예 |

{style="table-layout:auto"}

## 알려진 문제

다음은 Build Analyzer Maven 플러그인 사용 시 잘 알려진 문제의 목록입니다.

### Build Analyzer Maven 플러그인은 로컬 SDK에서 실행되지 않음

`1.1.2` 미만의 Build Analyzer Maven 플러그인으로 로컬 SDK를 사용하는 경우 플러그인을 실행하면 아래의 오류가 발생할 수 있습니다. 이 경우 프로젝트를 최신 버전의 플러그인으로 업데이트합니다.

```txt
[ERROR] Failed to execute goal com.adobe.aem:aemanalyser-maven-plugin:1.1.0:analyse (default-analyse) on project mysite.analyse: Execution default-analyse of goal com.adobe.aem:aemanalyser-maven-plugin:1.1.0:analyse failed: arraycopy: source index -1 out of bounds for char[65536] -> [Help 1]
```

AEM Project Archetype을 사용하여 프로젝트를 설정한 경우 다음과 같이 루트 Maven `pom.xml`에서 속성을 조정하십시오.

```xml
   ...
   <properties>
      ...
      <aemanalyser.version>1.1.2</aemanalyser.version> <!-- Make sure to use the latest release -->
      ...
   </properties>
```

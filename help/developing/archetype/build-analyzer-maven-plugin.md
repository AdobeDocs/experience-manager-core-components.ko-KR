---
title: AEM as Cloud Service SDK Build Analyzer Maven Plugin
description: 로컬 Maven 빌드 분석기 플러그인에 대한 설명서
translation-type: tm+mt
source-git-commit: e32521f35f33897cd72892de393073b01ad963f1
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 3%

---


# AEM as Cloud Service SDK Build Analyzer Maven Plugin {#maven-analyzer-plugin}

AEM analyzer Maven 플러그인은 다양한 컨텐츠 패키지 프로젝트의 구조를 분석합니다.

AEM [마스터 프로젝트에 이를 포함하는 방법에 대한 자세한 내용은 AEM Analyzer Maven 플러그인 설명서를](https://github.com/adobe/aemanalyser-maven-plugin/blob/main/aemanalyser-maven-plugin/README.md) 참조하십시오. 이 플러그인은 AEM Maven 원형형 버전 25 이상에 포함되어 있습니다.

다음은 이 단계의 일부로 실행되는 분석기를 설명하는 표입니다. 일부는 로컬 SDK에서 실행되는 반면 다른 일부는 Cloud Manager 파이프라인 배포 중에만 실행됩니다.

| 모듈 | 함수, 예 및 문제 해결 | 로컬 SDK | Cloud Manager |
|---|---|---|---|
| `api-regions-exportsimports` | 모든 OSGI 번들이 Maven 프로젝트에 포함된 다른 번들의 Export-package 선언에서 충족한 Import-Package 선언이 있는지 확인합니다. 다음과 같은 오류가 발생합니다. <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Bundle org.acme:mybundle:0.0.1-SNAPSHOT is importing package(s) org.acme.foo in start level 20 but no bundle is exporting these for that start level.`<p> </p>문제를 해결하려면 패키지를 제공하는 번들이 배포에 포함되어 있는지 확인하거나, 잘못된 이름 또는 잘못된 버전이 사용되었는지 확인하기 위해 내보낼 번들의 매니페스트를 확인하십시오. | 예 | 예 |
| `requirements-capabilities` | OSGI 번들에서 수행된 모든 요구 사항 선언이 Maven 프로젝트에 포함된 다른 번들의 기능 선언에 만족하는지 확인합니다. 다음과 같은 오류가 발생합니다. <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Artifact org.acme:mybundle:0.0.1-SNAPSHOT requires org.foo.bar in start level 20 but no artifact is providing a matching capability in this start level.`<p> </p> 문제를 해결하려면, 누락된 이유를 확인하는 기능을 선언하거나 필요한 번들의 매니페스트를 확인하여 요구 사항이 올바른지 확인하십시오. | 예 | 예 |
| `bundle-content` | 번들에 Sling-Initial-Content로 지정된 초기 컨텐츠가 포함되어 있는 경우 Cloud Service 클러스터된 환경으로서 AEM에서 문제가 되는 경고 메시지가 표시됩니다. 경고는 다음과 같습니다. <p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found initial content : [/]` <p> </p>초기 컨텐츠를 추천 문으로 변환하는 문제를 해결하려면 참조 설명서를 참조하십시오. | 예 | 예 |
| `bundle-resources` | 번들에 Sling-Bundle-Resources 헤더로 지정된 리소스가 포함되어 있는 경우 AEM에서 Cloud Service 클러스터된 환경으로 문제가 발생할 수 있습니다. 경고는 다음과 같습니다.<p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found bundle resources : [/libs/sling/explorer!/resources/explorer]`<p> </p> 리소스를 추천 문으로 변환하는 문제를 해결하려면 [설명서 수정을 참조하십시오](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=en#repo-init). | 예 | 예 |
| `api-regions`<p> </p>`api-regions-check-order`<p> </p>`api-regions-dependencies`<p> </p>`api-regions-duplicates` | 이러한 분석자는 기능의 API 영역 설정에 대한 몇 가지 세부 사항을 확인합니다. API 지역 구성이 생성되어 직접 지정되지 않은 고객의 경우 이러한 분석기는 AEMACS에서도 활성화되므로 활성화됩니다. 그러나 이러한 오류로 인해 컨텐트 패키지에 포함된 기능 모델 변환 프로세스의 버그가 발생하지는 않습니다. | 예 | 예 |
| `api-regions-crossfeature-dups` | 고객 OSGI 번들에 AEM을 Cloud Service의 공개 API로 재정의하는 Export-package 선언이 없는지 확인합니다.<p> </p>`[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Package overlap found between region global and bundle org.acme:mybundle:0.0.1.SNAPSHOT which comes from feature: [org.acme:myproject.analyse:slingosgifeature:0.0.1-SNAPSHOT]. Both export package: com.day.util`<p> </p>수정하려면 AEM 공개 API에 포함된 패키지 내보내기를 중지합니다. | 예 | 예 |
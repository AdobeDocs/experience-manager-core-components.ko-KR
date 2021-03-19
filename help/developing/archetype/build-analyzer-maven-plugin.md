---
title: AEM as Cloud Service SDK Build Analyzer Maven Plugin
description: 로컬 Maven 빌드 분석기 플러그인에 대한 설명서
feature: 핵심 구성 요소, AEM 프로젝트 원형
role: 건축가, 개발자, 관리자
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 3%

---


# AEM as Cloud Service SDK Build Analyzer Maben Plugin {#maven-analyzer-plugin}

Cloud Service SDK Build Analyzer Maven 플러그인으로 AEM은 다양한 콘텐츠 패키지 프로젝트의 구조를 분석합니다.

AEM 마스터 프로젝트에 포함하는 방법에 대한 자세한 내용은 [Maven 플러그인 설명서](https://github.com/adobe/aemanalyser-maven-plugin/blob/main/aemanalyser-maven-plugin/README.md)를 참조하십시오.

>[!NOTE]
>
>다음 위치의 Maven 중앙 저장소에 있는 플러그인의 최신 버전을 참조하도록 Maven 프로젝트를 업데이트하는 것이 좋습니다.https://repo1.maven.org/maven2/com/adobe/aem/aemanalyser-maven-plugin/

다음은 이 단계의 일부로 실행되는 분석기를 설명하는 표입니다.<!-- Note that some are executed in the local SDK, while others are only executed during the Cloud Manager pipeline deployment. -->

| 모듈 | 함수, 예 및 문제 해결 | 로컬 SDK | Cloud Manager |
|---|---|---|---|
| `api-regions-exportsimports` | 모든 OSGI 번들에 Maven 프로젝트에 포함된 다른 번들의 내보내기 패키지 선언에 만족한 Import-Package 선언이 있는지 확인합니다. 다음과 같은 오류가 발생합니다. <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Bundle org.acme:mybundle:0.0.1-SNAPSHOT is importing package(s) org.acme.foo in start level 20 but no bundle is exporting these for that start level.`<p> </p>문제를 해결하려면 패키지를 제공하는 번들이 배포에 포함되어 있는지 확인하거나, 또는 잘못된 이름 또는 잘못된 버전이 사용되었는지 확인하기 위해 내보낼 번들의 매니페스트를 확인하십시오. | 예 | 예 |
| `requirements-capabilities` | OSGI 번들에서 선언된 모든 요구 사항이 Maven 프로젝트에 포함된 다른 번들의 기능 선언에 만족하는지 확인합니다. 다음과 같은 오류가 발생합니다. <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Artifact org.acme:mybundle:0.0.1-SNAPSHOT requires org.foo.bar in start level 20 but no artifact is providing a matching capability in this start level.`<p> </p> 문제를 해결하려면, 누락된 이유를 확인하는 기능을 선언할 것으로 예상되는 번들의 매니페스트를 살펴보거나, 필요한 번들의 매니페스트에서 요구 사항이 올바른지 확인하십시오. | 예 | 예 |
| `bundle-content` | 번들에 Sling-Initial-Content로 지정된 초기 컨텐츠가 포함되어 있는 경우 Cloud Service 클러스터 환경으로 AEM에서 문제가 됩니다. 경고는 다음과 같습니다. <p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found initial content : [/]` <p> </p>초기 내용을 추천 문으로 변환하는 문제를 해결하려면 참조 설명서를 참조하십시오. | 예 | 예 |
| `bundle-resources` | 번들에 Sling-Bundle-Resources 헤더로 지정된 리소스가 포함되어 있는 경우 AEM에서 Cloud Service 클러스터 환경으로 문제가 발생합니다. 경고는 다음과 같습니다.<p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found bundle resources : [/libs/sling/explorer!/resources/explorer]`<p> </p> 리소스를 추천 문으로 변환하는 문제를 해결하려면 [참조 설명서](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=en#repo-init)를 참조하십시오. | 예 | 예 |
| `api-regions`<p> </p>`api-regions-check-order`<p> </p>`api-regions-dependencies`<p> </p>`api-regions-duplicates` | 이러한 분석기는 Sling 기능 모델에 따라 가공물을 만드는 [컨텐트 패키지에서 기능 모델 변환 프로세스](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html?lang=en#deploying)에 대한 일부 세부 사항을 확인합니다. 모든 오류는 Adobe 고객 지원에 보고해야 합니다. | 예 | 예 |
| `api-regions-crossfeature-dups` | 고객 OSGI 번들에 AEM을 Cloud Service의 공개 API로 재정의하는 Export-package 선언이 없는지 확인합니다.<p> </p>`[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Package overlap found between region global and bundle org.acme:mybundle:0.0.1.SNAPSHOT which comes from feature: [org.acme:myproject.analyse:slingosgifeature:0.0.1-SNAPSHOT]. Both export package: com.day.util`<p> </p>수정하려면 AEM 공개 API에 포함된 패키지 내보내기를 중지합니다. | 예 | 예 |
| `repoinit` | 모든 참조 섹션의 구문을 검사합니다. | 예 | 예 |
| `bundle-nativecode` | OSGI 번들이 기본 코드를 설치하지 않는지 확인합니다. | 예 | 예 |
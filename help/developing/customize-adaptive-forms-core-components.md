---
title: 적응형 Forms 핵심 구성 요소 맞춤화
description: 적응형 Forms 핵심 구성 요소를 확장하거나 만들어 조직에 맞게 조정된 기능을 구현하는 방법에 대해 알아봅니다.
role: Architect, Developer, Admin
source-git-commit: 9a80b453d6a6cf7b347128654d3b5e673a063505
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 4%

---


# 적응형 Forms 핵심 구성 요소 맞춤화

적응형 Forms 핵심 구성 요소를 사용자 지정하면 특정 요구 사항에 맞게 기본 기능을 맞춤화할 수 있습니다. 이 안내서에서는 보다 개인화된 환경을 만들기 위해 이러한 구성 요소를 맞춤화하는 프로세스를 안내합니다.

## 전제 조건

적응형 Forms 핵심 구성 요소 맞춤화에 들어가기 전에

* 에 대해 알아보기 [핵심 구성 요소의 아키텍처](customizing.md#customizing-the-markup-customizing-the-markup) 다음을 수행합니다. [공식 Adobe Experience Manager 핵심 구성 요소 설명서](customizing.md). 이러한 포괄적인 리소스는 맞춤화 프로세스 전반에 걸쳐 가이드 역할을 합니다.
* 개발 환경 설정 핵심 구성 요소를 변경할 수 있는 원활한 워크플로를 보장합니다. 개발 환경을 설정하는 동안 최신 AEM Archetype 프로젝트를 기반으로 AEM Archetype 프로젝트를 사용합니다. 환경에 따라 다음을 수행할 수 있습니다.

   * [Forms as a Cloud Service을 위한 로컬 개발 환경 설정](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/setup-local-development-environment.html).
   * [AEM 6.5 Forms에 대한 로컬 개발 환경 설정](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html)

## 적응형 Forms 핵심 구성 요소 맞춤화

적응형 Forms 핵심 구성 요소의 모양, 동작 및 기능을 수정하려면 아래 단계를 따르십시오.

1. **핵심 구성 요소 식별 및 복제**

   개발 환경을 구성하는 동안 Archetype 기반 프로젝트를 만들었습니다. AEM Archetype 프로젝트에서 사용자 정의하려는 특정 핵심 구성 요소를 식별합니다. 식별되면 AEM Archetype 기반 프로젝트 내에서 구성 요소의 복제본을 생성합니다. 다른 적응형 Forms 핵심 구성 요소와 병행합니다. 이 단계에서는 사용자 지정 작업이 원래 구성 요소에 영향을 주지 않도록 하여 자유롭게 실험할 수 있습니다.

1. **복사된 구성 요소 사용자 정의**

   복제된 구성 요소를 열고 요구 사항에 따라 필요한 수정을 시작합니다.

   * **HTML 구조 사용자 지정**: 을 준수하면서 디자인 요구에 맞게 HTML 구조를 맞춤화합니다. [BEM(블록 요소 수정자)](https://github.com/adobe/aem-core-wcm-components/wiki/css-coding-conventions) 유지 관리 및 확장 가능한 코드에 대한 스타일링 모범 사례입니다.
   * **레이블 업데이트**: 구성 요소의 레이블을 업데이트하여 사용자 지정된 버전에 대한 명확하고 설명적인 이름을 제공합니다. 제공된 을 참조하십시오 [OOTB(기본 제공) 레이블 템플릿](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/af-commons/v1/fieldTemplates/label.html) 일관성을 위해
   * **위젯 사용자 정의**: 구성 요소 내에서 사용되는 위젯(드롭다운, 확인란)을 조정하여 특정 사용 사례에 맞게 조정합니다. 다음을 참조하십시오. [샘플 위젯 구현](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput/textinput.html) 참조하십시오.
   * **도움말 텍스트 및 툴팁**: 구성 요소와 관련된 도움말 텍스트나 도구 설명을 개인화하여 사용자에게 컨텍스트와 지침을 제공합니다. 사용 [OOTB 도움말 텍스트 템플릿](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/af-commons/v1/fieldTemplates/questionMark.html) 를 시작점으로 사용하십시오.
   * **데이터 속성**: 구성 요소의 HTML 요소 내에 필요한 모든 데이터 속성을 통합합니다. 이러한 속성은 런타임 시 구성 요소가 제대로 작동하는 데 매우 중요합니다. 다음을 참조하십시오. [설명서](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput) 를 사용하여 적응형 Forms 핵심 구성 요소에서 데이터 속성의 역할을 이해할 수 있습니다.

1. **백엔드 논리 구현**

   맞춤화에 백엔드 로직이 필요한 경우 기존 슬링 모델을 확장할 수 있습니다. 제공된 을 참조하십시오 [예](https://github.com/adobe/aem-core-forms-components/blob/master/bundles/af-core/src/main/java/com/adobe/cq/forms/core/components/internal/models/v1/form/TextInputImpl.java) 원하는 기능을 맞춤화된 구성 요소에 완벽하게 통합합니다.

1. **구성 요소의 대화 상자 구성**

   맞춤화된 구성 요소와 연관된 대화 상자를 구성합니다. 예제 사용 [구성 요소 대화 상자](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput/_cq_dialog/.content.xml) 사용자 상호 작용 및 설정이 적절하게 관리되도록 설명서에 제공됩니다.

1. **로컬 개발 환경에서 구성 요소 배포 및 테스트**

   사용 [maven을 사용하여 구성 요소 빌드 및 배포](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/developing/archetype/using.html#building-and-installing) 로컬 개발 환경에서. 구성 요소가 배포되면 적응형 양식을 만들어 사용자 지정 구성 요소를 테스트합니다.

1. **프로덕션 환경에 사용자 정의 구성 요소 배포**

   로컬 개발 환경에서 구성 요소를 테스트한 후 프로덕션 환경에 구성 요소를 배포합니다.


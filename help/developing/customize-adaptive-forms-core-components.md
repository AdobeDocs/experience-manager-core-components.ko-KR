---
title: 적응형 양식 핵심 구성 요소 사용자 정의
description: 조직에 맞는 기능을 구현하기 위해 적응형 양식 핵심 구성 요소를 확장하거나 생성하는 방법에 대해 알아봅니다.
role: Architect, Developer, Admin
exl-id: f3ab12aa-d48d-47e9-a965-15052cac6f18
source-git-commit: 5994133947ff697f7c866fe61598c58e37e77008
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 100%

---

# 적응형 양식 핵심 구성 요소 사용자 정의

적응형 양식 핵심 구성 요소를 사용자 정의하면 특정 요구 사항에 맞게 즉시 사용 가능한 기능을 조정할 수 있습니다. 이 안내서는 이러한 구성 요소를 사용자 정의하여 보다 개인화된 경험을 만드는 과정을 안내합니다.

{{traditional-aem}}

## 전제 조건

적응형 양식 핵심 구성 요소를 사용자 정의하기 전에

* [핵심 구성 요소 아키텍처](customizing.md#customizing-the-markup-customizing-the-markup)에 대해 알아보고 [공식 Adobe Experience Manager 핵심 구성 요소 설명서](customizing.md)를 확인하십시오. 이러한 포괄적인 리소스는 사용자 정의 프로세스 전체에서 안내서 역할을 합니다.
* 개발 환경을 설정합니다. 이렇게 하면 핵심 구성 요소를 변경하기 위한 워크플로를 원활하게 할 수 있습니다. 개발 환경을 설정하는 동안에는 최신 AEM Archetype 프로젝트를 기반으로 하는 AEM Archetype 프로젝트를 사용합니다. 사용 중인 환경에 따라 다음을 수행할 수 있습니다.

   * [Forms as a Cloud Service용 로컬 개발 환경 설정](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/setup-configure-migrate/setup-local-development-environment.html)
   * [AEM 6.5 Forms용 로컬 개발 환경 설정](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/development/set-up-a-local-aem-development-environment.html?lang=ko-KR)

## 적응형 양식 핵심 구성 요소 사용자 정의

적응형 양식 핵심 구성 요소의 모양, 동작 및 기능을 수정하려면 아래 단계를 따르십시오.

1. **핵심 구성 요소 식별 및 복제**

   개발 환경을 구성하는 동안 Archetype 기반 프로젝트를 생성했습니다. 이제 AEM Archetype 프로젝트에서 사용자 정의하려는 특정 핵심 구성 요소를 식별합니다. 식별한 다음 AEM Archetype 기반 프로젝트 내에서 구성 요소의 복제본을 만듭니다. 이 복제본은 다른 적응형 양식 핵심 구성 요소와 병렬로 유지합니다. 이 단계를 통해 사용자 정의 작업이 원래 구성 요소에 영향을 미치지 않도록 하여 자유롭게 실험할 수 있습니다.

1. **복사된 구성 요소 사용자 정의**

   복제된 구성 요소를 열고 요구 사항에 따라 필요한 수정을 시작합니다.

   * **HTML 구조 사용자 정의**: [BEM(블록 요소 수정자)](https://github.com/adobe/aem-core-wcm-components/wiki/css-coding-conventions) 관리 및 확장 가능한 코드를 위한 스타일 지정 사례를 준수하여 디자인 요구 사항에 맞게 HTML 구조를 조정합니다.
   * **레이블 업데이트**: 구성 요소의 레이블을 업데이트하여 사용자 정의 버전에 대한 명확하고 설명적인 이름을 제공합니다. 일관성을 위해 제공된 [OOTB(기본 제공) 레이블 템플릿](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/af-commons/v1/fieldTemplates/label.html)을 참조하십시오.
   * **위젯 사용자 정의**: 특정 사용 사례에 맞게 구성 요소(드롭다운, 확인란) 내에서 사용되는 위젯을 조정합니다. [샘플 위젯 구현](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput/textinput.html)을 참조하십시오.
   * **도움말 텍스트 및 도구 설명**: 구성 요소와 관련된 도움말 텍스트 또는 도구 설명을 개인화하여 사용자에게 컨텍스트 및 지침을 제공합니다. [OOTB 도움말 텍스트 템플릿](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/af-commons/v1/fieldTemplates/questionMark.html)을 출발점으로 사용하십시오.
   * **데이터 속성**: 구성 요소의 HTML 요소 내에 필요한 모든 데이터 속성을 통합합니다. 이러한 특성은 런타임에 구성 요소가 제대로 작동하는 데 매우 중요합니다. [설명서](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput)를 참조하면 적응형 양식 핵심 구성 요소에서 데이터 속성의 역할을 이해할 수 있습니다.

1. **백엔드 논리 구현**

   사용자 정의에 백엔드 논리가 필요한 경우 기존 Sling 모델을 확장할 수 있습니다. 제공된 [예제](https://github.com/adobe/aem-core-forms-components/blob/master/bundles/af-core/src/main/java/com/adobe/cq/forms/core/components/internal/models/v1/form/TextInputImpl.java)를 참조하여 원하는 기능을 사용자 정의 구성 요소에 원활하게 통합하십시오.

1. **구성 요소의 대화 상자 구성**

   사용자 정의 구성 요소와 관련된 대화 상자를 구성합니다. 설명서에 제공된 [구성 요소 대화 상자](https://github.com/adobe/aem-core-forms-components/blob/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput/_cq_dialog/.content.xml) 예제를 사용하여 사용자 상호 작용과 설정을 적절하게 관리하십시오.

1. **로컬 개발 환경에서 구성 요소 배포 및 테스트**

   [Maven을 사용하여 로컬 개발 환경에서 구성 요소를 빌드하고 배포](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/developing/archetype/using.html#building-and-installing)합니다. 구성 요소를 배포한 후 적응형 양식을 만들어 사용자 정의 구성 요소를 테스트합니다.

1. **프로덕션 환경에 사용자 정의 구성 요소 배포**

   로컬 개발 환경에서 구성 요소를 테스트한 후 프로덕션 환경에 구성 요소를 배포합니다.

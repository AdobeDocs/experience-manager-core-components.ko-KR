---
title: 구성 요소 가이드라인
description: 핵심 구성 요소는 기초 구성 요소와 전혀 다른 최신 구현 패턴을 따릅니다.
role: Architect, Developer, Admin
exl-id: e8c58fa5-c991-433c-8d38-575dacfc3433
source-git-commit: ee18626280f74a51a799f16d6bf3f5b0be9cd6b9
workflow-type: tm+mt
source-wordcount: '1267'
ht-degree: 100%

---

# 구성 요소 가이드라인 {#component-guidelines}

[핵심 구성 요소](overview.md)는 기초 구성 요소와 전혀 다른 최신 구현 패턴을 따릅니다.

이 페이지에서는 이러한 패턴과, 패턴을 통해 작성 가능한 구성 요소를 빌드하는 시기에 대해 설명합니다. 첫 번째 섹션 [일반 구성 요소 패턴](#general-component-patterns)은 모든 유형의 구성 요소에 적용되지만 두 번째 섹션 [재사용 가능한 구성 요소 패턴](#reusable-component-patterns)은 핵심 구성 요소와 같이 사이트나 프로젝트에서 재사용이 가능한 구성 요소에 적용됩니다.

## 일반 구성 요소 패턴 {#general-component-patterns}

단일 프로젝트에 대한 구성 요소의 적합성 여부 및 사이트나 프로젝트에서 구성 요소의 재사용 여부와 관계없이 이 섹션의 가이드라인은 모든 유형의 패턴에 권장됩니다.

### 구성 가능한 구성 요소 {#configurable-components}

구성 요소에는 다양한 옵션을 가진 대화 상자가 있습니다. 이를 활용하여 구성 요소를 유연하게 구성할 수 있으며, 서로가 대부분 변형인 여러 구성 요소는 구현을 피하십시오.

일반적으로 와이어프레임이나 디자인에 유사한 요소의 변형이 포함된 경우 이러한 변형을 서로 다른 구성 요소가 아닌 변형 중에서 선택 가능한 옵션이 포함된 하나의 구성 요소로 구현해야 합니다.

추가 단계로서, 사이트나 프로젝트에서 구성 요소를 재사용하는 경우 [사전에 구성 가능한 기능](#pre-configurable-capabilities)을 참조하십시오.

### 문제 분리 {#separation-of-concerns}

일반적으로 마크업 템플릿(뷰)과 구성 요소의 논리(또는 모델)를 분리하는 것이 좋습니다. 이를 수행하기 위한 몇 가지 방법이 있지만, 핵심 구성 요소와 마찬가지로 논리에는 [슬링 모드](https://sling.apache.org/documentation/bundles/models.html)를, 마크업에는 [HTML 템플릿 언어](https://experienceleague.adobe.com/docs/experience-manager-htl/using/overview.html)를 사용하는 것이 좋습니다.

Java 주석 세트인 슬링 모드를 통해 POJO에서 필요한 변형에 쉽게 액세스할 수 있으므로 간단하고, 강력하고 효율적으로 구성 요소에 대해 Java 논리를 구현할 수 있습니다.

HTL은 AEM에 맞게 설계된 안전하고 간단한 템플릿 언어입니다. 유연성이 뛰어난 여러 유형의 논리를 호출할 수 있습니다.

## 재사용 가능한 구성 요소 패턴 {#reusable-component-patterns}

모든 유형의 구성 요소에 이 섹션의 가이드라인을 사용할 수 있지만, 핵심 구성 요소 등 사이트나 프로젝트에서 재사용이 가능한 구성 요소에 가장 적합합니다. 따라서 구성 요소가 단일 사이트나 프로젝트에서만 사용되는 경우에는 이 가이드라인을 무시할 수 있습니다.

### 사전에 구성 가능한 기능 {#pre-configurable-capabilities}

페이지 작성자가 사용하는 편집 대화 상자 외에도 구성 요소에는 디자인 대화 상자가 포함되어 템플릿 작성자는 구성 요소를 사전에 구성할 수 있습니다. [템플릿 편집기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html)를 통해 “정책”이라는 사전 구성 항목을 모두 설정할 수 있습니다.

재사용 가능한 구성 요소를 만들려면 사전 구성할 유의미한 옵션이 제공되어야 합니다. 이로써 각기 다른 사이트의 특정 요구 사항에 일치하는 구성 요소 기능을 활성화하거나 비활성화할 수 있습니다.

### 프록시 구성 요소 패턴 {#proxy-component-pattern}

각 콘텐츠 리소스에는 구성 요소 렌더링을 참조하는 `sling:resourceType` 속성이 있기 때문에 이러한 속성을 사용하여 여러 사이트에서 공유하는 구성 요소를 지정하는 대신 사이트별 구성 요소를 지정하는 것이 좋습니다. 한 사이트에서 서로 다른 구성 요소 비헤이비어가 필요한 경우 추가 유연성이 제공되고 콘텐츠 리팩터링이 배제되는 이유는 사이트별 구성 요소의 맞춤화가 다른 사이트에 영향을 미치지 않기 때문입니다.

단, 프로젝트별 구성 요소가 코드를 복제하지 않으면 `sling:resourceSuperType` 속성이 공유된 상위 구성 요소를 참조하십시오. 주로 상위 구성 요소를 참조하는 이 프로젝트별 구성 요소는 “프록시 구성 요소”라 합니다. 기능이 완전히 상속되면 프록시 구성 요소 전체가 비거나 구성 요소의 일부 측면이 재정의될 수 있습니다.

>[!TIP]
>
>프록시 구성 요소를 만드는 방법에 대한 자세한 내용은 [핵심 구성 요소 사용](/help/get-started/using.md#create-proxy-components)을 참조하십시오.

### 구성 요소 버전 관리 {#component-versioning}

지속적으로 구성 요소의 호환성을 최대한 유지해야 하지만 경우에 따라 호환될 수 없는 변경 사항이 필요합니다. 반대 요구 조건에 대한 솔루션으로 리소스 유형 경로와 정규화된 Java 구현 클래스 이름에 번호를 추가하여 구성 요소 버전 관리를 도입할 수 있습니다. 이 버전 번호는 [시맨틱 버전 관리 가이드라인](https://semver.org/)에서 정의된 주요 버전을 나타내고, 이전에 호환되지 않은 경우에만 버전이 증가합니다.

다음 구성 요소 측면에 대한 변경 사항이 호환되지 않으면 새로운 버전의 구성 요소가 생성됩니다.

* 슬링 모델 (다음 시맨틱 버전 관리 가이드라인)
* HTL 스크립트 및 템플릿
* HTML 마크업 및 CSS 선택기
* JSON 표시
* 대화 상자

자세한 내용은 GitHub의 [버전 관리 정책](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-Policies) 문서를 참조하십시오.

리팩터링이 언제 수행되는지 명시되기 때문에 구성 요소 버전 관리는 업그레이드에 중요한 계약 양식을 만듭니다. 다양한 맞춤화 양식을 업그레이드하는 데 필요한 고려할 사항에 대해 설명하는 섹션 [맞춤화의 호환성 업그레이드](customizing.md#upgrade-compatibility-of-customizations)를 참조하십시오.

어려운 콘텐츠 마이그레이션을 피하려면 버전 관리된 구성 요소를 콘텐츠 리소스에서 바로 지정하지 않는 것이 좋습니다. 일반적으로 콘텐츠의 `sling:resourceType`에는 버전 번호가 포함되면 안 됩니다. 또는 구성 요소가 업그레이드되면 콘텐츠도 리팩터링될 수 있습니다. 이를 최대한 피하기 위해서 위에서 설명한 [프록시 구성 요소 패턴](#proxy-component-pattern)을 따르십시오.

### 모델 인터페이스 {#model-interfaces}

이 패턴은 Java 인터페이스를 지정하는 HTL용 `data-sly-use` 지침인 반면에 슬링 모델 구현은 구성 요소의 리소스 유형에 자체 등록됩니다.

위에서 설명한 [프록시 구성 요소 패턴](#proxy-component-pattern)과 결합되면 이러한 이중 바인딩이 제공하는 확장 지점은 다음과 같습니다.

1. HTL 파일이 인터페이스를 계속 지정하는 경우 사이트는 이를 무시하면서 프록시 구성 요소의 리소스 유형에 등록하여 슬링 모델의 구현을 재정의할 수 있습니다.
1. 구성 요소가 구현 논리를 지정해야 하는 경우 사이트는 이를 무시하면서 HTM 마크업을 재정의할 수 있습니다.

## 결합하기 {#putting-it-all-together}

다음에서 제목 핵심 구성 요소를 사례로 전체 리소스 유형 바인딩 구조를 검토합니다. 콘텐츠 리소스에 버전 번호가 포함되지 않도록, 사이트별 프록시 구성 요소를 통해 구성 요소 버전 관리를 해결하는 방법을 보여 줍니다. 구성 요소의 `title.html` [HTL](https://experienceleague.adobe.com/docs/experience-manager-htl/using/overview.html) 파일이 모델 인터페이스에 어떻게 사용되는지 보여 주지만 구현은 [슬링 모델](https://sling.apache.org/documentation/bundles/models.html) 주석을 통해 특정 버전의 구성 요소에 바인딩됩니다.

![리소스 바인딩 개요](/help/assets/chlimage_1-32.png)

아래 검토에는 구현 POJO에 대한 세부 정보가 표시되지 않지만 관련 [템플릿 및 정책](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html)을 참조하는 방법은 표시됩니다.

`cq:allowedTemplates` 속성을 통해 사이트에 사용되는 템플릿을 알려 주고 `cq:template`를 통해 각 페이지에 관련 템플릿에 대한 정보를 제공할 수 있습니다. 모든 템플릿은 다음 세 가지 부품으로 구성됩니다.

* **구조** - 각 페이지에 전달되고 페이지 작성자가 삭제할 수 없는 리소스(예: 페이지 머리말 및 바닥글 구성 요소)가 포함됩니다.
* **최초 콘텐츠** - 제작 시 페이지에 복제되는 최초 콘텐츠가 포함됩니다.
* **정책** - 각 구성 요소에 구성 요소를 사전 구성하는 정책에 대한 매핑이 포함됩니다. 이 매핑을 통해 템플릿에서 정책을 재사용할 수 있으므로 집중 관리해야 합니다.

![템플릿 및 정책 개요](/help/assets/screen_shot_2018-12-07at093102.png)

## AEM Project Archetype {#aem-project-archetype}

[AEM Project Archetype](/help/developing/archetype/overview.md)은 프로젝트 시작점으로 논리용 슬링 모드가 포함된 맞춤형 HTL 구성 요소의 예제와 권장 프록시 패턴이 포함된 핵심 구성의 적절한 구현 등 최소 Adobe Experience Manager 프로젝트를 만듭니다.

**다음 참조:**

* [핵심 구성 요소 사용](/help/get-started/using.md) - 자체 프로젝트에서 핵심 구성 요소를 시작하고 실행합니다.
* [핵심 구성 요소 맞춤화](customizing.md) - 핵심 구성 요소 스타일링 및 사용자 정의하는 방법에 대해 알아봅니다.

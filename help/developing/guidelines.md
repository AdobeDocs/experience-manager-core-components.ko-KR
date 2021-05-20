---
title: 구성 요소 지침
description: 핵심 구성 요소는 기초 구성 요소와 전혀 다른 최신 구현 패턴을 따릅니다.
role: Architect, Developer, Administrator
exl-id: e8c58fa5-c991-433c-8d38-575dacfc3433
source-git-commit: b5b77f21cbeaa46622cef85f3bbaa549f17f1a06
workflow-type: tm+mt
source-wordcount: '1272'
ht-degree: 2%

---

# 구성 요소 지침 {#component-guidelines}

[코어 구성 요소](overview.md)는 기초 구성 요소와 상당히 다른 최신 구현 패턴을 따릅니다.

이 페이지에서는 이러한 패턴과 이러한 패턴을 사용하여 작성 가능한 구성 요소를 작성할 시기를 설명합니다. 첫 번째 섹션 [일반 구성 요소 패턴](#general-component-patterns)은 모든 종류의 구성 요소에 적용되는 반면, 두 번째 섹션 [재사용 가능한 구성 요소 패턴](#reusable-component-patterns)은 예를 들어 핵심 구성 요소와 같이 사이트 또는 프로젝트에서 재사용하려는 구성 요소에 적용됩니다.

## 일반 구성 요소 패턴 {#general-component-patterns}

구성 요소가 단일 프로젝트에만 해당하는지 또는 구성 요소가 사이트 또는 프로젝트에서 폭넓게 재사용되는지 여부에 관계없이 이 섹션의 지침은 구성 요소 유형에 관계없이 권장됩니다.

### 구성 가능한 구성 요소 {#configurable-components}

구성 요소에는 대화 상자가 다양한 옵션을 사용할 수 있습니다. 이 구성 요소를 활용하여 구성 요소를 유연하고 구성할 수 있고, 서로 거의 변형된 여러 구성 요소를 구현하지 않도록 해야 합니다.

일반적으로 와이어프레임 또는 디자인에 유사한 요소의 변형이 포함되어 있는 경우 이러한 변형을 다른 구성 요소로 구현하지 않고 변형 중에서 선택할 수 있는 옵션이 있는 하나의 구성 요소로 구현해야 합니다.

이 단계를 더 수행하려면 구성 요소가 사이트 또는 프로젝트에서 다시 사용되는 경우 [구성 가능한 기능](#pre-configurable-capabilities) 섹션을 참조하십시오.

### 관심 항목 {#separation-of-concerns} 분리

일반적으로 마크업 템플릿(또는 보기)과 구성 요소의 논리(또는 모델)를 별도로 유지하는 것이 좋습니다. 이를 위해 여러 가지 방법이 있지만, 권장되는 방법은 논리에 [Sling Models](https://sling.apache.org/documentation/bundles/models.html) 를 사용하고, 핵심 구성 요소처럼 마크업에 [HTML Template Language](https://docs.adobe.com/content/help/ko-KR/experience-manager-htl/using/overview.html) (HTL)을 사용하는 것입니다.

Sling 모델은 POJO에서 필요한 변수에 쉽게 액세스할 수 있는 Java 주석 세트입니다. 따라서 구성 요소에 대한 Java 로직을 구현하는 간단하고 강력하며 효율적인 방법을 제공합니다.

HTL은 AEM에 맞게 맞춤화된 안전하고 간단한 템플릿 언어로 디자인되었습니다. 그것은 많은 형태의 논리들을 불러일으킬 수 있는데, 그것은 그것을 매우 유연하게 만듭니다.

## 재사용 가능한 구성 요소 패턴 {#reusable-component-patterns}

이 섹션의 지침은 모든 구성 요소에 사용할 수도 있지만 핵심 구성 요소와 같이 사이트 또는 프로젝트에서 재사용하기 위한 구성 요소에 대해서는 가장 적합합니다. 따라서 단일 사이트 또는 프로젝트에서만 사용되는 구성 요소에 대해서는 이러한 지침을 무시할 수 있습니다.

### 사전 구성 가능한 기능 {#pre-configurable-capabilities}

페이지 작성자가 사용하는 편집 대화 상자 외에도 구성 요소에는 템플릿 작성자가 미리 구성할 수 있는 디자인 대화 상자가 있을 수 있습니다. [템플릿 편집기](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)를 사용하면 &quot;정책&quot;이라고 하는 이러한 모든 사전 구성을 설정할 수 있습니다.

구성 요소를 가능한 한 재사용 가능하게 만들려면 사전 구성할 수 있는 의미 있는 옵션을 제공해야 합니다. 이렇게 하면 다른 사이트의 특정 요구 사항에 맞게 구성 요소의 기능을 활성화하거나 비활성화할 수 있습니다.

### 프록시 구성 요소 패턴 {#proxy-component-pattern}

각 컨텐츠 리소스에는 렌더링하기 위해 구성 요소를 참조하는 `sling:resourceType` 속성이 있으므로, 일반적으로 여러 사이트에서 공유한 구성 요소를 가리키는 대신 이러한 속성이 사이트 특정 구성 요소를 가리키는 것이 좋습니다. 이렇게 하면 사이트 특정 구성 요소에서 수행할 수 있고 다른 사이트에 영향을 주지 않으므로, 한 사이트에서 구성 요소에 대해 다른 동작이 필요한 경우 콘텐츠 리팩터링을 방지할 수 있고 더 많은 유연성을 제공할 수 있습니다.

그러나 프로젝트별 구성 요소가 코드를 복제하지 않으려면 각각 `sling:resourceSuperType` 속성이 있는 공유 상위 구성 요소를 참조해야 합니다. 주로 상위 구성 요소만을 참조하는 이러한 프로젝트별 구성 요소를 &quot;프록시 구성 요소&quot;라고 합니다. 프록시 구성 요소는 기능을 완전히 상속하거나 구성 요소의 일부 측면을 재정의할 수 있는 경우 완전히 비어 있을 수 있습니다.

>[!TIP]
>
>프록시 구성 요소를 만드는 방법에 대한 자세한 내용은 [핵심 구성 요소 사용](/help/get-started/using.md#create-proxy-components) 을 참조하십시오.

### 구성 요소 버전 관리 {#component-versioning}

구성 요소는 시간에 따라 완전히 호환되어야 하지만, 경우에 따라 호환될 수 없는 변경 사항이 필요합니다. 이러한 요구 사항에 대한 한 가지 해결 방법은 리소스 유형 경로에 숫자를 추가하고 해당 구현의 정규화된 Java 클래스 이름에 번호를 추가하여 구성 요소 버전 지정을 도입하는 것입니다. 이 버전 번호는 [시맨틱 버전 관리 지침](https://semver.org/)에 정의된 주요 버전을 나타내며, 이전 버전과 호환되지 않는 변경 사항에만 증분됩니다.

구성 요소의 다음 측면에 호환되지 않는 변경 사항이 있으면 새 버전이 발생합니다.

* Sling 모델(다음 시맨틱 버전 관리 지침)
* HTL 스크립트 및 템플릿
* HTML 마크업 및 CSS 선택기
* JSON 표시
* 대화 상자

자세한 내용은 GitHub의 [버전 관리 정책](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-Policies) 문서를 참조하십시오.

구성 요소 버전 관리는 리팩터링해야 하는 경우를 명확히 하기 때문에 업그레이드에 중요한 계약 형식을 만듭니다. 업그레이드에 필요한 여러 사용자 지정 양식의 고려 사항을 설명하는 [사용자 지정 업그레이드 호환성](customizing.md#upgrade-compatibility-of-customizations) 섹션도 참조하십시오.

컨텐츠 마이그레이션이 번거롭지 않게 하려면 컨텐츠 리소스에서 버전이 지정된 구성 요소를 직접 가리키지 않는 것이 중요합니다. 경험상 컨텐츠의 `sling:resourceType`에 버전 번호가 없어야 하거나 구성 요소를 업그레이드하려면 컨텐츠도 다시 팩터링해야 합니다. 이를 방지하는 가장 좋은 방법은 위에 설명된 [프록시 구성 요소 패턴](#proxy-component-pattern)을 따르는 것입니다.

### 모델 인터페이스 {#model-interfaces}

이 패턴은 HTL의 `data-sly-use` 지시에서 Java 인터페이스를 가리키도록 하는 반면 Sling 모델 구현에서는 구성 요소의 리소스 유형에도 자신을 등록하고 있습니다.

위에서 설명한 [프록시 구성 요소 패턴](#proxy-component-pattern)과 결합하면 이 형식의 이중 바인딩 오퍼는 다음과 같은 좋은 확장 지점을 제공합니다.

1. 사이트는 여전히 인터페이스를 가리키는 HTL 파일에 대해 신경쓰지 않고 프록시 구성 요소의 리소스 유형에 등록하여 Sling 모델의 구현을 재정의할 수 있습니다.
1. 사이트는 어떤 구현 논리를 가리킬 필요 없이 구성 요소의 HTL 마크업을 재정의할 수 있습니다.

## 모두 함께 {#putting-it-all-together}

다음은 제목 코어 구성 요소의 예를 들어 전체 리소스 유형 바인딩 구조에 대한 개요입니다. 사이트별 프록시 구성 요소에서 구성 요소 버전 지정을 확인할 수 있도록 어떻게 컨텐츠 리소스에 버전 번호가 포함되어 있는지 확인하는 방법을 설명합니다. 그런 다음 구성 요소의 `title.html` [HTL](https://docs.adobe.com/content/help/en/experience-manager-htl/using/overview.html) 파일이 모델 인터페이스에 어떻게 사용되는지 보여 주는 반면, 구현은 [Sling Model](https://sling.apache.org/documentation/bundles/models.html) 주석을 통해 구성 요소의 특정 버전에 바인딩됩니다.

![리소스 바인딩 개요](/help/assets/chlimage_1-32.png)

다음은 구현 POJO의 세부 사항을 표시하지 않고, 연결된 [템플릿 및 정책](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/components-templates/templates.html)을 참조하는 방법을 보여주는 다른 개요입니다.

`cq:allowedTemplates` 속성은 사이트에 사용할 수 있는 템플릿을 알려줍니다. `cq:template` 은 각 페이지에 대해 연관된 템플릿이 무엇인지 알려줍니다. 모든 템플릿은 다음 세 부분으로 구성됩니다.

* **구조**  - 각 페이지에 강제로 표시될 리소스를 포함하며, 페이지 머리글 및 바닥글 구성 요소와 같이 페이지 작성자는 삭제할 수 없습니다.
* **초기**  - 페이지를 만들 때 페이지에 복제되는 초기 컨텐츠를 포함합니다.
* **정책**  - 구성 요소의 사전 구성인 정책에 대한 매핑을 각 구성 요소에 대해 포함합니다. 이 매핑을 사용하면 템플릿 간에 정책을 다시 사용할 수 있으므로 중앙에서 관리할 수 있습니다.

![템플릿 및 정책 개요](/help/assets/screen_shot_2018-12-07at093102.png)

## AEM 프로젝트 전형 {#aem-project-archetype}

[AEM 프로젝트 ](/help/developing/archetype/overview.md) 원형 은 권장 프록시 패턴으로 코어 구성 요소를 적절하게 구현하고 논리를 위해 SlingModels를 사용하는 사용자 지정 HTL 구성 요소의 예를 포함하여 고유한 프로젝트의 시작점으로 최소 Adobe Experience Manager 프로젝트를 만듭니다.

**다음 참조:**

* [핵심 구성 요소 사용](/help/get-started/using.md)  - 프로젝트에서 핵심 구성 요소를 사용하여 바로 실행할 수 있습니다.
* [핵심 구성 요소 사용자 지정](customizing.md)  - 핵심 구성 요소의 스타일을 지정하고 사용자 지정하는 방법을 알아봅니다.

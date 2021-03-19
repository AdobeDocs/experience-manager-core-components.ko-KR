---
title: 구성 요소 지침
description: 핵심 구성 요소는 기본 구성 요소와 매우 다른 최신 구현 패턴을 따릅니다.
role: 건축가, 개발자, 관리자
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '1262'
ht-degree: 2%

---


# 구성 요소 지침 {#component-guidelines}

[핵심 구성 요소](overview.md)는 기본 구성 요소와 매우 다른 최신 구현 패턴을 따릅니다.

이 페이지에서는 이러한 패턴과 이 패턴을 사용하여 자체 작성 가능한 구성 요소를 만드는 시기를 설명합니다. 첫 번째 섹션 [일반 구성 요소 패턴](#general-component-patterns)은 모든 유형의 구성 요소에 적용되지만, 두 번째 섹션 [재사용 가능한 구성 요소 패턴](#reusable-component-patterns)은 핵심 구성 요소 등과 같이 사이트 또는 프로젝트에서 다시 사용할 수 있도록 만들어진 구성 요소에 적용됩니다.

## 일반 구성 요소 패턴 {#general-component-patterns}

구성 요소가 단일 프로젝트에만 해당하는지 또는 구성 요소가 사이트 또는 프로젝트에서 널리 재사용되고 있는지 여부와 관계없이 이 섹션의 지침은 모든 유형의 구성 요소에 대해 권장됩니다.

### 구성 가능한 구성 요소 {#configurable-components}

구성 요소에는 다양한 옵션이 있는 대화 상자가 있을 수 있습니다. 구성 요소를 유연하게 구성하고 구성할 수 있도록 하며 서로 거의 변형된 여러 구성 요소를 구현하지 않도록 해야 합니다.

일반적으로 와이어프레임 또는 디자인에 유사한 요소의 변형이 포함되어 있는 경우 이러한 변형을 다른 컴포넌트로 구현하지 않고 변형을 선택할 수 있는 옵션이 있는 하나의 컴포넌트로 구현해야 합니다.

이 단계를 자세히 진행하려면 구성 요소를 사이트 또는 프로젝트에서 다시 사용하는 경우 [구성 가능한 사전 기능](#pre-configurable-capabilities) 섹션을 참조하십시오.

### 우려 사항 분리 {#separation-of-concerns}

일반적으로 마크업 템플릿(또는 보기)과 구성 요소의 논리(또는 모델)를 구분하도록 하는 것이 좋습니다. 여러 가지 방법을 사용할 수 있지만 권장 방법은 논리에는 [Sling 모델](https://sling.apache.org/documentation/bundles/models.html)을 사용하고, 핵심 구성 요소처럼 마크업에 [HTML 템플릿 언어](https://docs.adobe.com/content/help/ko-KR/experience-manager-htl/using/overview.html)(HTL)를 사용하는 것입니다.

Sling Models는 POJO에서 필요한 변수에 쉽게 액세스할 수 있는 Java 주석 집합이므로 구성 요소에 대한 Java 로직을 구현하는 간단하고 강력하며 효율적인 방법을 제공합니다.

HTL은 AEM에 맞게 맞춤화된 안전하고 간단한 템플릿 언어로 설계되었습니다. 그것은 많은 형태의 논리라고 부를 수 있는데, 그것은 그것을 매우 유연하게 한다.

## 재사용 가능한 구성 요소 패턴 {#reusable-component-patterns}

이 섹션의 지침은 모든 유형의 구성 요소에도 사용할 수 있지만 핵심 구성 요소와 같이 사이트 또는 프로젝트에서 재사용할 수 있는 구성 요소에 대해서는 가장 적절합니다. 따라서 단일 사이트 또는 프로젝트에서만 사용되는 구성 요소에 대해서는 이러한 지침을 무시할 수 있습니다.

### 사전 구성 가능한 기능 {#pre-configurable-capabilities}

페이지 작성자가 사용하는 편집 대화 상자 외에도 구성 요소에는 템플릿 작성자가 미리 구성할 수 있는 디자인 대화 상자가 있을 수 있습니다. [템플릿 편집기](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)에서는 &quot;정책&quot;이라고 하는 모든 사전 구성을 설정할 수 있습니다.

구성 요소를 가능한 한 다시 사용할 수 있도록 하려면 미리 구성할 수 있는 의미 있는 옵션이 제공됩니다. 이렇게 하면 다른 사이트의 특정 요구 사항에 맞게 구성 요소의 기능을 활성화하거나 비활성화할 수 있습니다.

### 프록시 구성 요소 패턴 {#proxy-component-pattern}

각 컨텐츠 리소스에는 렌더링할 구성 요소를 참조하는 `sling:resourceType` 속성이 있으므로 일반적으로 여러 사이트에서 공유하는 구성 요소를 가리키는 대신 사이트 특정 구성 요소를 가리키는 속성이 있는 것이 좋습니다. 이렇게 하면 사이트 특정 구성 요소에서 이러한 사용자 지정을 수행할 수 있고 다른 사이트에 영향을 주지 않으므로 한 사이트에 구성 요소에 대해 다른 비헤이비어가 필요한 경우 컨텐츠 리팩토링을 더 유연하게 수행할 수 있으며 컨텐츠 리팩토링을 방지할 수 있습니다.

그러나 프로젝트별 구성 요소가 코드를 복제하지 않도록 하려면 각각 `sling:resourceSuperType` 속성이 있는 공유 상위 구성 요소를 참조해야 합니다. 주로 상위 구성 요소만을 참조하는 이러한 프로젝트 특정 구성 요소를 &quot;프록시 구성 요소&quot;라고 합니다. 프록시 구성 요소는 기능을 완전히 상속하거나 구성 요소의 일부 측면을 재정의할 수 있는 경우 완전히 비어 있을 수 있습니다.

### 구성 요소 버전 관리 {#component-versioning}

구성 요소는 시간에 따라 완벽하게 호환되어야 하지만 호환하지 못하는 변경 사항이 있을 수 있습니다. 이러한 요구 사항에 대한 한 가지 해결 방법은 리소스 유형 경로와 구현의 정규화된 Java 클래스 이름에 숫자를 추가하여 구성 요소 버전 관리를 도입하는 것입니다. 이 버전 번호는 [의미 버전 관리 지침](https://semver.org/)에 의해 정의된 주요 버전을 나타냅니다. 이 버전은 이전 버전과 호환되지 않는 변경 사항에만 증가합니다.

구성 요소의 다음 측면을 호환되지 않는 변경 사항은 새 버전으로 이어집니다.

* Sling 모델(다음 의미 체계 버전 관리 지침)
* HTL 스크립트 및 템플릿
* HTML 마크업 및 CSS 선택기
* JSON 표현
* 대화 상자

자세한 내용은 GitHub의 [버전 관리 정책](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-Policies) 문서를 참조하십시오.

구성 요소 버전 매기기를 통해 어떤 것을 리팩토링해야 하는 경우를 명확히 함으로써 업그레이드에 중요한 계약 양식을 만들 수 있습니다. 업그레이드에 필요한 여러 사용자 지정 양식의 고려 사항을 설명하는 [사용자 지정 업그레이드 호환성](customizing.md#upgrade-compatibility-of-customizations) 단원도 참조하십시오.

컨텐츠 마이그레이션이 까다롭지는 않도록 컨텐츠 리소스에서 버전이 지정된 구성 요소를 직접 지정하지 않는 것이 중요합니다. 경험상 콘텐츠의 `sling:resourceType`은 버전 번호를 포함해서는 안 되며, 구성 요소를 업그레이드하려면 컨텐츠도 리팩토링해야 합니다. 이를 피하는 가장 좋은 방법은 위에서 설명한 [프록시 구성 요소 패턴](#proxy-component-pattern)을 따르는 것입니다.

### 모델 인터페이스 {#model-interfaces}

이 패턴은 Java 인터페이스를 가리키도록 HTL의 `data-sly-use` 명령에 대한 것이며, Sling 모델 구현도 구성 요소의 리소스 유형에 자신을 등록하고 있습니다.

위에 설명한 [프록시 구성 요소 패턴](#proxy-component-pattern)과 결합하면 이 형식의 이중 바인딩 확장 지점은 다음과 같습니다.

1. 사이트는 여전히 인터페이스를 가리키는 HTL 파일에 대해 신경 쓰지 않고도 프록시 구성 요소의 리소스 유형에 등록하여 Sling 모델의 구현을 재정의할 수 있습니다.
1. 사이트는 어떤 구현 논리를 가리킬 필요 없이 구성 요소의 HTL 마크업을 재정의할 수 있습니다.

## 모두 함께 {#putting-it-all-together}

다음은 제목 코어 구성 요소의 예를 들어 전체 리소스 유형 바인딩 구조에 대한 개요입니다. 컨텐츠 리소스에 버전 번호가 포함되어 있지 않도록 사이트별 프록시 구성 요소를 사용하여 구성 요소 버전 지정을 확인하는 방법을 설명합니다. 그런 다음 구성 요소의 `title.html` [HTL](https://docs.adobe.com/content/help/en/experience-manager-htl/using/overview.html) 파일이 모델 인터페이스에 어떻게 사용하는지를 보여주며, 구현은 [Sling Model](https://sling.apache.org/documentation/bundles/models.html) 주석을 통해 구성 요소의 특정 버전으로 바인딩합니다.

![리소스 바인딩 개요](/help/assets/chlimage_1-32.png)

다음은 구현 POJO에 대한 세부 정보를 표시하지 않지만 연결된 [템플릿 및 정책](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/components-templates/templates.html)이(가) 참조된 방식을 보여주는 다른 개요입니다.

`cq:allowedTemplates` 속성은 사이트에 사용할 수 있는 템플릿을 알려주고 `cq:template`은 각 페이지에 연관된 템플릿이 무엇인지 알려줍니다. 모든 템플릿은 다음 3개의 부분으로 구성됩니다.

* **구조**  - 각 페이지에 강제로 표시할 리소스와 페이지 머리글 및 바닥글 구성 요소와 같이 페이지 작성자가 삭제할 수 없는 리소스가 포함되어 있습니다.
* **초기**  - 페이지를 만들 때 페이지에 중복될 초기 컨텐츠를 포함합니다.
* **정책**  - 구성 요소의 사전 구성인 정책에 대한 매핑을 포함하는 각 구성 요소에 대해 포함합니다. 이 매핑을 사용하면 정책을 템플릿 간에 다시 사용할 수 있으므로 중앙에서 관리할 수 있습니다.

![템플릿 및 정책 개요](/help/assets/screen_shot_2018-12-07at093102.png)

## AEM 프로젝트 전형 {#aem-project-archetype}

[AEM 프로젝트 ](/help/developing/archetype/overview.md) 원형에서는 권장 프록시 패턴을 사용하여 핵심 구성 요소의 논리 및 적절한 구현에 대한 SlingModels와의 사용자 지정 HTML 구성 요소 예제를 비롯하여 고유한 프로젝트의 시작점으로 최소한의 Adobe Experience Manager 프로젝트를 만듭니다.

**다음 참조:**

* [핵심 구성 요소](/help/get-started/using.md)  사용 - 프로젝트에서 핵심 구성 요소를 바로 사용할 수 있습니다.
* [핵심 구성 요소 사용자](customizing.md)  지정 - 핵심 구성 요소의 스타일을 지정하고 사용자 지정하는 방법을 알아봅니다.

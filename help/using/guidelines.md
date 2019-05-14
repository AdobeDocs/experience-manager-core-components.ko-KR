---
title: 구성 요소 지침
seo-title: 구성 요소 지침
description: 핵심 구성 요소는 기본 구성 요소와 상당히 다른 최신 구현 패턴을 따릅니다.
seo-description: 핵심 구성 요소는 기본 구성 요소와 상당히 다른 최신 구현 패턴을 따릅니다.
uuid: B 1 DAEA 89-DA 3 C -454 F -8 AB 5-D 75 A 19412954
contentOwner: 사용자
content-type: 참조
topic-tags: developing
products: sg_ Experiencemanager/Corecomponents-new
discoiquuid: 170 dba 8 f-a 2 ed -442 e-a 56 e -1126 b 338 c 36 e
translation-type: tm+mt
source-git-commit: 62643e5bd49ab006230f65004bb9374822dcc017

---


# 구성 요소 지침 {#component-guidelines}

[핵심 구성 요소는](developing.md) 기본 구성 요소와 상당히 다른 최신 구현 패턴을 따릅니다.

이 페이지에서는 이러한 패턴에 대해 설명하고, 이러한 패턴을 사용하여 직접 작성 가능한 구성 요소를 만드는 방법을 설명합니다. 첫 번째 섹션 [일반 구성 요소 패턴은](guidelines.md) 모든 종류의 구성 요소에 적용되지만 두 번째 섹션 [재사용 가능한 구성 요소 패턴은](guidelines.md) 예를 들어 핵심 구성 요소처럼 사이트 또는 프로젝트에서 재사용할 구성 요소에 적용됩니다.

## 일반 구성 요소 패턴 {#general-component-patterns}

이 섹션의 지침은 구성 요소가 단일 프로젝트에 고유하는지 아니면 구성 요소가 사이트 또는 프로젝트에서 널리 재사용되는지 관계없이 모든 종류의 구성 요소에 권장됩니다.

### 구성 가능한 구성 요소 {#configurable-components}

구성 요소에는 다양한 옵션이 있는 대화 상자가 있을 수 있습니다. 이 기능을 활용하여 구성 요소를 유연하고 구성할 수 있도록 하고 대부분 서로 다른 여러 구성 요소를 구현하지 않도록 해야 합니다.

일반적으로 와이어프레임 또는 디자인에 유사한 요소가 포함되어 있는 경우 이러한 변형을 다른 구성 요소로 구현해서는 안 되지만 변형 중에 선택할 수 있는 옵션이 있는 구성 요소로 구현하면 안 됩니다.

한 단계 더 나아가 구성 요소가 사이트 또는 프로젝트 간에 재사용되는 경우 사전 구성 [가능한 기능](#pre-configurable-capabilities) 섹션을 참조하십시오.

### 우려 사항 분리 {#separation-of-concerns}

일반적으로 마크업 템플릿 (또는 보기) 과는 별도의 구성 요소의 논리 (또는 모델) 를 유지하는 것이 좋습니다. 여러 가지 방법이 있습니다. 하지만 핵심 구성 요소처럼 마크업에 [대한 sling 모델을](https://sling.apache.org/documentation/bundles/models.html) [사용하는](https://helpx.adobe.com/experience-manager/htl/using/overview.html) 것이 좋습니다.

Sling Models는 Pojos에서 필요한 변수에 쉽게 액세스할 수 있는 Java 주석 세트이므로 구성 요소에 Java 로직을 구현할 수 있는 간단하고 강력하며 성능적인 방법을 제공합니다.

HTL는 AEM에 맞게 만들어진 안전하고 간단한 템플릿 언어로 디자인되었습니다. 다양한 형태의 로직을 호출할 수 있으므로 매우 유연합니다.

## 재사용 가능한 구성 요소 패턴 {#reusable-component-patterns}

이 섹션의 지침은 모든 종류의 구성 요소용으로도 사용할 수 있지만, 예를 들어, 핵심 구성 요소처럼 사이트 또는 프로젝트 간에 재사용하기 위한 구성 요소에 가장 적합합니다. 따라서 단일 사이트나 프로젝트에서만 사용되는 구성 요소에 대해서는 이러한 지침이 무시될 수 있습니다.

### 사전 구성 가능한 기능 {#pre-configurable-capabilities}

페이지 작성자가 사용하는 편집 대화 상자 이외에도 구성 요소에는 템플릿 작성자가 미리 구성할 수 있는 디자인 대화 상자가 있을 수 있습니다. [템플릿 편집기를](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) 사용하면 이러한 사전 구성을 모두 설정할 수 있습니다. 이 모든 사전 구성을 &quot;정책&quot; 이라고 합니다.

구성 요소를 가능한 한 재사용 가능하도록 하려면 미리 구성할 의미 있는 옵션을 제공해야 합니다. 이를 통해 여러 사이트의 특정 요구 사항과 일치하도록 구성 요소의 기능을 활성화하거나 비활성화할 수 있습니다.

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T17:49:04.584-0400

Unclear how I can add my own capability toggle (for example, if i extend a component and want to toggle that extended functionality ... )

 -->

### Proxy component pattern {#proxy-component-pattern}

각 컨텐츠 리소스에는 구성 요소를 참조하는 `sling:resourceType` 속성이 있으므로 일반적으로 여러 사이트에서 공유하는 구성 요소를 가리키기보다는 사이트 전용 구성 요소를 가리키는 이러한 속성을 갖는 것이 좋습니다. 이렇게 하면 사이트 특정 구성 요소에서 이 맞춤화를 수행할 수 있고 다른 사이트에는 영향을 주지 않으므로 한 사이트에 구성 요소에 대해 다른 비헤이비어가 필요한 경우 더 많은 유연성을 제공하고 컨텐츠 리팩토링을 방지할 수 있습니다.

하지만 프로젝트 특정 구성 요소가 코드를 복제하지 않도록 `sling:resourceSuperType` 하려면 속성이 있는 공유된 상위 구성 요소를 각각 참조해야 합니다. 주로 상위 구성 요소를 참조하는 이러한 프로젝트별 구성 요소를 &quot;프록시 구성 요소&quot; 라고 합니다. 프록시 구성 요소는 기능을 완전히 상속하는 경우 완전히 비어 있거나 구성 요소의 일부 측면을 재정의할 수 있습니다.

### 구성 요소 버전 관리 {#component-versioning}

구성 요소는 시간 경과에 따라 완벽하게 호환되어야 하지만 경우에 따라 호환할 수 없는 변경 사항이 필요합니다. 이러한 상충되는 요구 사항에 대한 한 가지 해결 방법은 리소스 유형 경로에 숫자와 구현의 정규화된 Java 클래스 이름에 숫자를 추가하여 구성 요소 버전 관리를 도입하는 것입니다. 이 버전 번호는 이전 버전과 호환되지 않는 변경 사항에만 증분되는 [Semantic 버전 관리 지침으로](https://semver.org/)정의된 주요 버전을 나타냅니다.

구성 요소 측면에 대한 호환되지 않는 변경 사항은 다음과 같은 새 버전의 결과를 가져옵니다.

* Sling Models (다음 시맨틱 버전 관리 지침)
* HTL 스크립트 및 템플릿
* HTML 마크업 및 CSS 선택기
* JSON 표현
* 대화 상자

자세한 내용은 Github [의 버전 관리 정책](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-Policies) 문서를 참조하십시오.

구성 요소 버전 매기기를 사용하면 제품을 리팩토링해야 할 때를 명확히 하므로 업그레이드에 중요한 계약서 양식을 작성할 수 있습니다. 다른 형태의 사용자 정의 요구 사항에 대한 업그레이드가 필요한 사항에 대해 설명하는 사용자 정의 섹션의 섹션 [업그레이드 호환성을 참조하십시오](customizing.md#upgrade-compatibility-of-customizations).

컨텐츠가 마이그레이션되지 않도록 하려면 컨텐츠 리소스에서 버전 구성 요소를 직접 가리키지 않아야 합니다. As rule of thumb, a `sling:resourceType` content must never have a version number in it, or upgrade components will require the content to be refactored too. 이를 피하는 가장 좋은 방법은 위에 설명된 [프록시 구성 요소 패턴을](#proxy-component-pattern) 따르는 것입니다.

### 모델 인터페이스 {#model-interfaces}

This pattern is about HTL&#39;s `data-sly-use` instruction to point to point to point Java interface, while the sling model implementation are also registered to the resource type of the component.

위에 설명된 [프록시 구성 요소 패턴과](#proxy-component-pattern) 함께 사용할 경우, 이 이중 바인딩은 좋은 확장 지점을 다음과 같이 제공합니다.

1. 사이트는 여전히 인터페이스를 가리키는 HTL 파일을 신경 쓰지 않고도 프록시 구성 요소의 리소스 유형에 등록하여 sling 모델의 구현을 재정의할 수 있습니다.
1. 사이트는 가리킬 구현 로직을 신경쓰지 않고 구성 요소의 HTL 마크업을 재정의할 수 있습니다.

## 모든 취합 {#putting-it-all-together}

다음은 제목 핵심 구성 요소의 예제를 가져오는 전체 리소스 유형 바인딩 구조에 대한 개요입니다. 여기서는 컨텐츠 리소스에 버전 번호가 포함되어 있지 않도록 사이트 특정 프록시 구성 요소가 구성 요소 버전 관리를 해결하는 방법을 보여 줍니다. 그런 다음 구성 요소의 `title.html`[HTL](https://helpx.adobe.com/experience-manager/htl/using/overview.html) 파일이 모델 인터페이스에 어떻게 사용하는지 보여주고, 구현은 [Sling 모델](https://sling.apache.org/documentation/bundles/models.html) 주석을 통해 특정 버전의 구성 요소에 바인딩합니다.

![리소스 바인딩 개요](assets/chlimage_1-32.png)

다음은 구현 Pojo의 세부 사항을 표시하지 않지만 관련 [템플릿 및 정책이](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/page-templates-editable.html) 참조되는 방법을 보여주는 다른 개요입니다.

속성은 `cq:allowedTemplates` 사이트에 사용할 수 있는 템플릿을, 연관된 템플릿은 각 페이지에 대해 `cq:template` 알려줍니다. 모든 템플릿은 다음 세 가지 부분으로 구성됩니다.

* **구조에는**
각 페이지에 강제로 강제로 표시되는 리소스가 포함되며, 페이지 작성자는 페이지 머리글과 바닥글 구성 요소와 같이 삭제할 수 없습니다.
* **초기에는**
페이지가 생성될 때 페이지에 복제할 초기 컨텐츠가 포함됩니다.
* **정책은**
각 구성 요소에 대한 매핑을 구성 요소의 사전 구성인 정책에 포함합니다. 이러한 매핑을 통해 여러 템플릿 간에 정책을 재사용할 수 있으므로 중앙에서 관리할 수 있습니다.

![템플릿 및 정책 개요](assets/screen_shot_2018-12-07at093102.png)

**다음을 참조하십시오.**

* [핵심 구성 요소 사용](using.md) - 프로젝트에 핵심 구성 요소를 사용할 수 있습니다.
* [핵심 구성 요소 맞춤화](customizing.md) - 핵심 구성 요소의 스타일을 지정하고 사용자 지정하는 방법을 알아보십시오.

---
title: 핵심 구성 요소 사용자 정의
description: 코어 구성 요소 는 간단한 스타일링에서 고급 기능 재사용에 이르기까지 쉬운 사용자 지정을 허용하는 몇 가지 패턴을 구현합니다.
role: Architect, Developer, Admin
exl-id: ec4b918b-bc70-4d72-ba84-a24556aedb41
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '1106'
ht-degree: 2%

---

# 핵심 구성 요소 사용자 정의{#customizing-core-components}

[코어 구성 요소](overview.md)는 간단한 스타일링에서 고급 기능 재사용에 이르기까지 사용자 지정이 쉬운 여러 패턴을 구현합니다.

## 유연한 아키텍처 {#flexible-architecture}

핵심 구성 요소는 처음부터 유연하고 확장할 수 있도록 디자인되었습니다. 아키텍처에 대한 개요를 살펴보면 사용자 지정을 수행할 수 있는 위치가 표시됩니다.

![핵심 구성 요소 아키텍처](/help/assets/screen_shot_2018-12-07at093742.png)

* [디자인 대화 ](/help/get-started/authoring.md#edit-and-design-dialogs) 상자는 작성자가 편집 대화 상자에서 수행할 수 있는 작업과 할 수 없는 작업을 정의합니다.
* [편집 대화 ](/help/get-started/authoring.md#edit-and-design-dialogs) 상자에는 사용할 수 있는 옵션만 표시됩니다.
* [Sling ](#customizing-the-logic-of-a-core-component) 모델은 뷰(템플릿)에 대한 컨텐츠를 확인하고 준비합니다.
* [Sling 모델의 결과](#customizing-the-logic-of-a-core-component) 를 SPA 사용 사례의 JSON으로 직렬화할 수 있습니다.
* [HTL에서는 ](#customizing-the-markup) 기존 서버측 렌더링에 대해 HTML 서버측을 렌더링합니다.
* [HTML은 ](#customizing-the-markup) 의미론적, 접근성, 검색 엔진 최적화 및 스타일을 쉽게 파악할 수 있습니다.

그리고 모든 코어 구성 요소는 [스타일 시스템](#styling-the-components)을 구현합니다.

## AEM 프로젝트 전형 {#aem-project-archetype}

[AEM 프로젝트 ](/help/developing/archetype/overview.md) 원형 은 권장 프록시 패턴으로 코어 구성 요소를 적절하게 구현하고 논리를 위해 SlingModels를 사용하는 사용자 지정 HTL 구성 요소의 예를 포함하여 고유한 프로젝트의 시작점으로 최소 Adobe Experience Manager 프로젝트를 만듭니다.

## 사용자 지정 패턴 {#customization-patterns}

### 대화 상자 사용자 지정 {#customizing-dialogs}

[디자인 대화 상자 또는 편집 대화 상자](/help/get-started/authoring.md)처럼 핵심 구성 요소 대화 상자에서 사용할 수 있는 구성 옵션을 사용자 지정하는 것이 필요할 수 있습니다.

각 대화 상자에는 일관된 노드 구조가 있습니다. [Sling Resource Merger](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/sling-resource-merger.html) 및 [Hide Conditions](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/hide-conditions.html)을 사용하여 원래 대화 상자의 섹션을 숨기기, 바꾸기 또는 재정렬할 수 있도록 이 구조가 상속 구성 요소에 복제되는 것이 좋습니다. 복제할 구조는 탭 항목 노드 수준까지 정의됩니다.

현재 버전의 대화 상자에 대한 변경 사항과 완전히 호환되도록 하려면 탭 항목 수준 아래의 구조가 터치되지 않는(숨김, 추가, 교체, 순서 변경 등) 것이 매우 중요합니다. 대신 상위의 탭 항목은 `sling:hideResource` 속성([Sling Resource Merger Properties](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/sling-resource-merger.html) 참조)을 통해 숨겨야 하고 맞춤 구성 필드가 포함된 새 탭 항목을 추가해야 합니다. `sling:orderBefore` 필요한 경우 탭 항목의 순서를 변경하는 데 사용할 수 있습니다.

아래 대화 상자는 위에서 설명한 대로 상속된 탭을 숨기거나 바꾸는 방법과 권장 대화 상자 구조를 보여 줍니다.

```xml
<?xml version="1.0" encoding="UTF-8"?>
<jcr:root xmlns:sling="https://sling.apache.org/jcr/sling/1.0"
          xmlns:jcr="https://www.jcp.org/jcr/1.0"
          xmlns:nt="https://www.jcp.org/jcr/nt/1.0"
          xmlns:granite="https://www.adobe.com/jcr/granite/1.0"
          jcr:primaryType="nt:unstructured">
    <content jcr:primaryType="nt:unstructured">
        <items jcr:primaryType="nt:unstructured">
            <tabs jcr:primaryType="nt:unstructured">
                <items jcr:primaryType="nt:unstructured">
                        <originalTab
                                jcr:primaryType="nt:unstructured"
                                sling:hideResource="true"/>
                        </originalTab>
                        <myTab
                               jcr:primaryType="nt:unstructured"
                               jcr:title="My Tab"
                               sling:resourceType="granite/ui/components/coral/foundation/container"/>
                               <!-- myTab content -->
                        </myTab>
                </items>
            </basic>
        </items>
    </content>
</jcr:root>
```

### 핵심 구성 요소의 논리 사용자 지정 {#customizing-the-logic-of-a-core-component}

핵심 구성 요소에 대한 비즈니스 로직은 Sling 모델에서 구현됩니다. Sling 위임 패턴을 사용하여 이 논리를 확장할 수 있습니다.

예를 들어 제목 코어 구성 요소는 요청된 리소스의 `jcr:title` 속성을 사용하여 제목 텍스트를 제공합니다. `jcr:title` 속성이 정의되지 않으면 현재 페이지 제목에 대한 폴백이 구현됩니다. 현재 페이지의 제목이 항상 표시되도록 동작을 변경하려고 합니다.

코어 구성 요소 모델의 구현은 개인이므로 위임 패턴으로 확장해야 합니다.

```java
@Model(adaptables = SlingHttpServletRequest.class,
       adapters = Title.class,
       resourceType = "myproject/components/pageHeadline")
public class PageHeadline implements Title {
    @ScriptVariable private Page currentPage;
    @Self @Via(type = ResourceSuperType.class)
    private Title title;
    @Override public String getText() {
        return currentPage.getTitle();
    }
    @Override public String getType() {
        return title.getType();
    }
}
```

위임 패턴에 대한 자세한 내용은 핵심 구성 요소 GitHub Wiki 문서 [Sling 모델용 위임 패턴](https://github.com/adobe/aem-core-wcm-components/wiki/Delegation-Pattern-for-Sling-Models)을 참조하십시오.

### 마크업 사용자 정의 {#customizing-the-markup}

고급 스타일링을 사용하려면 구성 요소의 다른 마크업 구조가 필요한 경우가 있습니다.

이 작업은 코어 구성 요소에서 수정해야 하는 HTL 파일을 [프록시 구성 요소로 복사하여 수행할 수 있습니다.](guidelines.md#proxy-component-pattern)

코어 탐색 표시 구성 요소의 예를 다시 들어 마크업 출력을 사용자 지정하려면 `breadcrumb.html` 파일을 코어 탐색 표시 구성 요소를 가리키는 `sling:resourceSuperTypes` 가 있는 사이트별 구성 요소에 복사해야 합니다.

### 구성 요소 스타일 지정 {#styling-the-components}

사용자 지정의 첫 번째 형식은 CSS 스타일을 적용하는 것입니다.

이를 쉽게 하기 위해 코어 구성 요소는 의미 있는 마크업을 렌더링하고 [Bootstrap](https://getbootstrap.com/)에서 영감을 받은 표준화된 이름 지정 규칙을 따릅니다. 또한 개별 구성 요소에 대한 스타일을 쉽게 타깃팅하고 네임스페이스를 지정하려면 각 코어 구성 요소를 &quot; `cmp`&quot; 및 &quot; `cmp-<name>`&quot; 클래스를 사용하여 DIV 요소에 래핑됩니다.

예를 들어, v1 코어 탐색 표시 구성 요소의 HTL 파일 보기: [탐색 표시.html](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb/breadcrumb.html) 요소 출력 계층이 `ol.breadcrumb > li.breadcrumb-item > a`인 것을 알 수 있습니다. 따라서 CSS 규칙이 해당 구성 요소의 탐색 표시 클래스에만 영향을 주는지 확인하려면 모든 규칙에 다음과 같이 이름을 지정해야 합니다.

```shell
.cmp-breadcrumb .breadcrumb {}  
.cmp-breadcrumb .breadcrumb-item {}  
.cmp-breadcrumb a {}
```

또한 각 핵심 구성 요소는 템플릿 작성자가 페이지 작성자가 구성 요소에 적용할 수 있는 추가 CSS 클래스 이름을 정의할 수 있도록 해주는 AEM [스타일 시스템 기능](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/style-system.html)을 활용합니다. 이렇게 하면 각 템플릿에 대해 허용된 구성 요소 스타일 목록과 이러한 스타일 중 하나를 해당 종류의 모든 구성 요소에 기본적으로 적용할지 여부를 정의할 수 있습니다.

## 사용자 정의 업그레이드 호환성 {#upgrade-compatibility-of-customizations}

다음과 같은 세 가지 종류의 업그레이드가 가능합니다.

* AEM 버전 업그레이드
* 코어 구성 요소를 새 부 버전으로 업그레이드
* 핵심 구성 요소를 주요 버전으로 업그레이드

일반적으로 AEM을 새 버전으로 업그레이드해도 핵심 구성 요소 또는 수행된 사용자 지정에 영향을 주지 않습니다. 구성 요소의 버전은 로 마이그레이션되는 새 AEM 버전도 지원하고 사용자 지정에서는 [더 이상 사용되지 않거나 제거된 ](https://docs.adobe.com/content/help/ko-KR/experience-manager-cloud-service/release-notes/deprecated-removed-features.html) API를 사용하지 않습니다.

최신 주요 버전으로 전환하지 않고 코어 구성 요소를 업그레이드하면 이 페이지에 설명된 사용자 지정 패턴이 사용되는 한 사용자 지정에 영향을 주지 않습니다.

핵심 구성 요소의 최신 주요 버전으로 전환하는 것은 컨텐츠 구조에만 호환되지만 사용자 지정을 리팩터링해야 할 수 있습니다. 이 페이지에 설명된 사용자 지정 유형에 영향을 주는 변경 사항을 강조 표시하려면 변경 로그 지우기가 각 구성 요소 버전에 대해 게시됩니다.

## 사용자 지정 지원 {#support-of-customizations}

모든 AEM 구성 요소의 경우와 마찬가지로 사용자 지정과 관련된 많은 사항을 알고 있어야 합니다.

1. **코어 구성 요소의 코드는 직접 수정하지 마십시오.**

   이렇게 하면 해당 구성 요소가 완전히 지원되지 않게 되고 향후 구성 요소 업데이트가 번거로운 프로세스로 이루어집니다. 대신 이 페이지에 설명된 사용자 지정 방법을 사용하십시오.

1. **사용자 지정 코드는 사용자의 책임입니다.**

   지원 프로그램은 사용자 지정 코드를 포함하지 않으며, 문서화된 [으로 사용되는 vanilla 코어 구성 요소로 재현할 수 없는 보고된 문제는 적합하지 않습니다.](/help/get-started/using.md)

1. **사용이 중단되거나 제거된 기능을 확인하십시오.**

   새로운 AEM 버전이 으로 업그레이드될 때마다 사용되는 모든 API가 [더 이상 사용되지 않거나 제거된 기능](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/release-notes/deprecated-removed-features.html) 페이지를 계속 검토하여 아직 현지적인지 확인하십시오.

[코어 구성 요소 지원](overview.md#core-component-support) 섹션도 참조하십시오.

**다음 참조:**

* [핵심 구성 요소 사용](/help/get-started/using.md)  - 프로젝트에서 핵심 구성 요소를 사용하여 바로 실행할 수 있습니다.
* [구성 요소 지침](guidelines.md)  - 핵심 구성 요소의 구현 패턴을 알아봅니다.

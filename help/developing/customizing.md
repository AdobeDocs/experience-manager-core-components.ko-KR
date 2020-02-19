---
title: 핵심 구성 요소 사용자 정의
description: 핵심 구성 요소는 간단한 스타일링에서 고급 기능 재사용에 이르기까지 사용자 정의가 용이한 여러 패턴을 구현합니다.
translation-type: tm+mt
source-git-commit: fe8a121520000ffd56ae3347469590e89121eaf0

---


# 핵심 구성 요소 사용자 정의{#customizing-core-components}

코어 [구성](overview.md) 요소는 간단한 스타일링에서 고급 기능 재사용에 이르기까지 사용자 정의가 용이한 몇 가지 패턴을 구현합니다.

## 유연한 아키텍처 {#flexible-architecture}

핵심 구성 요소는 처음부터 유연하고 확장할 수 있게 디자인되었습니다. 아키텍처의 개요를 살펴보면 사용자 정의 가능한 위치를 알 수 있습니다.

![핵심 구성 요소 아키텍처](/help/assets/screen_shot_2018-12-07at093742.png)

* [디자인 대화 상자는](/help/get-started/authoring.md#edit-and-design-dialogs) 작성자가 편집 대화 상자에서 수행할 수 있거나 수행할 수 없는 작업을 정의합니다.
* [편집 대화 상자에는](/help/get-started/authoring.md#edit-and-design-dialogs) 작성자가 사용할 수 있는 옵션만 표시됩니다.
* [Sling 모델은](#customizing-the-logic-of-a-core-component) 뷰의 컨텐츠를 확인하고 준비합니다(템플릿).
* [Sling 모델의](#customizing-the-logic-of-a-core-component) 결과는 SPA 사용 사례를 위해 JSON에 직렬화할 수 있습니다.
* [HTL은 기존 서버측](#customizing-the-markup) 렌더링을 위해 HTML 서버측을 렌더링합니다.
* [HTML 출력은](#customizing-the-markup) 의미 체계, 액세스 가능성, 검색 엔진에 최적화되어 있으며 스타일을 쉽게 지정할 수 있습니다.

모든 핵심 구성 요소는 스타일 시스템을 [구현합니다](#styling-the-components).

## AEM 프로젝트 전형 {#aem-project-archetype}

[AEM Project Tranype은](/help/developing/archetype/overview.md) SlingModels가 포함된 사용자 지정 HTL 구성 요소의 예를 비롯하여 권장 프록시 패턴을 사용하는 핵심 구성 요소의 올바른 구현을 위한 최소한의 Adobe Experience Manager 프로젝트를 고유한 프로젝트의 시작점으로 만듭니다.

## 사용자 정의 패턴 {#customization-patterns}

### 대화 상자 사용자 지정 {#customizing-dialogs}

디자인 대화 상자 또는 편집 대화 상자처럼 핵심 구성 요소 대화 상자에서 사용할 수 있는 구성 옵션을 사용자 [지정할 수 있습니다](/help/get-started/authoring.md).

각 대화 상자에는 일관된 노드 구조가 있습니다. 이 구조는 상속 구성 요소에서 복제되므로 리소스 [합병](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/sling-resource-merger.html) 및 조건 숨기기를 [사용하여 원래 대화 상자의 섹션을 숨기거나 바꾸거나 순서를 변경할](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/hide-conditions.html) 수 있습니다. 복제할 구조는 탭 항목 노드 수준까지의 임의 항목으로 정의됩니다.

현재 버전에서 대화 상자가 변경된 내용과 완전히 호환하려면 탭 항목 수준 아래의 구조를 손대지 않는 것이 중요합니다(숨김, 추가, 교체, 순서 변경 등). 대신 상위의 탭 항목은 `sling:hideResource` 속성을 통해 숨겨져야 합니다(리소스 [통합 속성 참조). 맞춤 구성 필드가 포함된 새 탭](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/sling-resource-merger.html)항목이 추가되었습니다. `sling:orderBefore` 필요한 경우 탭 항목의 순서를 변경하는 데 사용할 수 있습니다.

아래 대화 상자에서는 위에서 설명한 대로 권장되는 대화 상자 구조와 상속된 탭을 숨기거나 교체하는 방법을 보여 줍니다.

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

핵심 구성 요소에 대한 비즈니스 로직은 Sling Models에서 구현됩니다. Sling 위임 패턴을 사용하여 이 논리를 확장할 수 있습니다.

예를 들어 제목 핵심 구성 요소는 요청된 리소스의 `jcr:title` 속성을 사용하여 제목 텍스트를 제공합니다. 속성이 정의되지 않은 `jcr:title` 경우 현재 페이지 제목에 대한 폴백이 구현됩니다. 현재 페이지의 제목이 항상 표시되도록 동작을 변경하려고 합니다.

핵심 구성 요소 모델의 구현은 비공개이므로 위임 패턴으로 확장되어야 합니다.

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

위임 패턴에 대한 자세한 내용은 핵심 구성 요소 GitHub Wiki 문서 Sling 모델에 [대한 위임 패턴을 참조하십시오](https://github.com/adobe/aem-core-wcm-components/wiki/Delegation-Pattern-for-Sling-Models).

### 마크업 사용자 지정 {#customizing-the-markup}

경우에 따라 고급 스타일링을 사용하려면 구성 요소의 다른 마크업 구조가 필요합니다.

이 작업은 핵심 구성 요소에서 프록시 구성 요소로 수정해야 하는 HTL 파일을 복사하여 쉽게 수행할 수 있습니다.

코어 탐색 표시 구성 요소의 예를 다시 들어, 마크업 출력을 사용자 정의하려면 `breadcrumb.html` 파일이 코어 탐색 표시 구성 요소를 가리키는 사이트 특정 구성 요소에 복사되어야 `sling:resourceSuperTypes` 합니다.

### 구성 요소 스타일 지정 {#styling-the-components}

사용자 지정의 첫 번째 형식은 CSS 스타일을 적용하는 것입니다.

이를 쉽게 하기 위해 핵심 구성 요소는 의미 체계 마크업을 렌더링하고 Bootstrap에서 영감을 얻은 표준화된 명명 규칙을 [따릅니다](https://getbootstrap.com/). 또한 개별 구성 요소에 대한 스타일을 쉽게 타깃팅하고 네임스페이스로 지정하려면 각 핵심 구성 요소가 &quot; `cmp`&quot; 및 &quot; `cmp-<name>`&quot; 클래스를 사용하여 DIV 요소로 래핑됩니다.

예를 들어, v1 코어 탐색 표시 구성 요소의 HTL 파일을 봅니다.breadcrumb.html [은](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb/breadcrumb.html)요소 출력의 계층이 `ol.breadcrumb > li.breadcrumb-item > a`있음을 보여줍니다. 따라서 CSS 규칙이 해당 구성 요소의 탐색 표시 클래스에만 영향을 주도록 하기 위해 모든 규칙은 아래와 같이 이름을 지정해야 합니다.

```shell
.cmp-breadcrumb .breadcrumb {}  
.cmp-breadcrumb .breadcrumb-item {}  
.cmp-breadcrumb a {}
```

또한 각 핵심 구성 요소는 템플릿 작성자가 페이지 작성자가 구성 [요소에 적용할 수 있는 추가 CSS 클래스 이름을 정의할 수 있도록 해주는 AEM Style System 기능을](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/style-system.html) 활용합니다. 이렇게 하면 각 템플릿에 허용된 구성 요소 스타일 목록과 이러한 스타일 중 하나가 기본적으로 해당 유형의 모든 구성 요소에 적용되어야 하는지 여부를 정의할 수 있습니다.

## 사용자 정의 업그레이드 호환성 {#upgrade-compatibility-of-customizations}

다음과 같은 세 가지 종류의 업그레이드가 가능합니다.

* aem 버전 업그레이드
* 핵심 구성 요소를 새로운 부 버전으로 업그레이드
* 핵심 구성 요소를 주 버전으로 업그레이드

일반적으로, AEM을 새 버전으로 업그레이드하는 것은 코어 구성 요소나 사용자 지정에 영향을 주지 않습니다. 단, 구성 요소의 버전은 마이그레이션되는 새 AEM 버전도 지원하고 사용자 지정 버전은 [더 이상 사용되지 않거나 제거된](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/release-notes/deprecated-removed-features.html)API를 사용하지 않습니다.

이 페이지에 설명된 사용자 지정 패턴을 사용하는 한, 최신 주 버전으로 전환하지 않고 핵심 구성 요소를 업그레이드하면 사용자 정의에 영향을 주지 않습니다.

최신 주요 버전의 핵심 구성 요소로 전환하는 것은 컨텐츠 구조에만 호환되지만 사용자 지정을 다시 팩토링해야 할 수 있습니다. 각 구성 요소 버전에 대한 변경 사항 로그 지우기가 게시되어 이 페이지에 설명된 사용자 정의 유형에 영향을 주는 변경 사항을 강조 표시합니다.

## 사용자 정의 지원 {#support-of-customizations}

모든 AEM 구성 요소와 마찬가지로 사용자 지정에 대해 알아야 할 사항이 많이 있습니다.

1. **핵심 구성 요소의 코드를 직접 수정하지 마십시오.**

   이렇게 하면 완전히 지원되지 않을 수 있으며 구성 요소의 향후 업데이트를 고통스러운 프로세스가 됩니다. 대신 이 페이지에 설명된 사용자 지정 방법을 사용하십시오.

1. **사용자 지정 코드는 사용자의 책임입니다.**

   Adobe 지원 프로그램은 사용자 지정 코드를 포함하지 않으며, 문서화된 [](/help/get-started/using.md) 대로 사용되는 바닐라 코어 구성 요소로 재현할 수 없는 보고된 문제는 해당되지 않습니다.

1. **사용 중단되거나 제거된 기능을 봅니다.**

   업그레이드되는 각 새로운 AEM 버전이 있으면, 사용된 모든 API가 더 이상 사용되지 않는 기능 및 제거된 기능 [페이지를 계속 볼 수](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/release-notes/deprecated-removed-features.html) 있습니다.

핵심 구성 요소 [지원 섹션을](overview.md#core-component-support) 참조하십시오.

**다음 참조:**

* [핵심 구성 요소](/help/get-started/using.md) 사용 - 프로젝트에서 핵심 구성 요소를 사용하여 바로 시작할 수 있습니다.
* [구성 요소](guidelines.md) 지침 - 핵심 구성 요소의 구현 패턴을 학습합니다.

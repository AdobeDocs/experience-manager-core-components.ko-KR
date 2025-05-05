---
title: 핵심 구성 요소 맞춤화
description: 핵심 구성 요소는 간단한 스타일링부터 고급 기능 재사용까지 간편하게 맞춤화할 수 있는 몇 가지 패턴을 구현합니다.
role: Architect, Developer, Admin
exl-id: ec4b918b-bc70-4d72-ba84-a24556aedb41
source-git-commit: bd688d422a072a9d5627c27817ac67f95829de4f
workflow-type: tm+mt
source-wordcount: '1041'
ht-degree: 100%

---

# 핵심 구성 요소 맞춤화{#customizing-core-components}

[핵심 구성 요소](overview.md)는 간단한 스타일링부터 고급 기능 재사용까지 간편하게 맞춤화할 수 있는 몇 가지 패턴을 구현합니다.

## 유연한 아키텍처 {#flexible-architecture}

시작부터 유연하고 확장 가능한 핵심 구성 요소로 설계되었습니다. 아키텍처 개요를 살펴보면 어디서 맞춤화가 수행되는지 표시됩니다.

![핵심 구성 요소 아키텍처](/help/assets/screen_shot_2018-12-07at093742.png)

* [디자인 대화 상자](/help/get-started/authoring.md#edit-and-design-dialogs)는 작성자가 편집 대화 상자에서 수행할 수 있는 작업 또는 수행할 수 없는 작업을 정의합니다.
* [편집 대화 상자](/help/get-started/authoring.md#edit-and-design-dialogs)는 작성자가 사용할 수 있는 옵션만 보여 줍니다.
* [슬링 모드](#customizing-the-logic-of-a-core-component)는 검색할 콘텐츠를 확인하고 준비합니다(템플릿).
* SPA 사용 사례에서 [슬링 모드의 결과](#customizing-the-logic-of-a-core-component)는 JSON으로 일련화될 수 있습니다.
* [HTL의 HTML 서버측 렌더링](#customizing-the-markup)으로 기존 서버측을 렌더링합니다.
* [HTML 출력](#customizing-the-markup)은 시맨틱하고, 액세스가 가능하고, 검색 엔진에 최적화되고 스타일링이 간단합니다.

모든 핵심 구성 요소는 [스타일 시스템](#styling-the-components)을 지원합니다.

## AEM Project Archetype {#aem-project-archetype}

[AEM Project Archetype](/help/developing/archetype/overview.md)은 프로젝트 시작점으로 논리용 슬링 모드가 포함된 맞춤형 HTL 구성 요소의 예제와 권장 프록시 패턴이 포함된 핵심 구성의 적절한 구현 등 최소 Adobe Experience Manager 프로젝트를 만듭니다.

## 맞춤형 패턴 {#customization-patterns}

### 대화 상자 맞춤화 {#customizing-dialogs}

[디자인 대화 상자 또는 편집 대화 상자](/help/get-started/authoring.md)에서 핵심 구성 요소 대화 상자에 제공되는 맞춤형 구성 옵션이 필요할 수 있습니다.

각 대화 상장에는 일관된 노드 구조가 있습니다. [슬링 리소스 병합](https://helpx.adobe.com/kr/experience-manager/6-4/sites/developing/using/sling-resource-merger.html)과 [조건 숨기기](https://helpx.adobe.com/kr/experience-manager/6-5/sites/developing/using/hide-conditions.html)를 통해 원래 대화 상자의 섹션을 숨기고, 대체하고 순서를 변경할 수 있도록 상속 구성 요소에서 이 구조를 복제하는 것이 좋습니다. 복제할 구조를 탭 항목 노드 레벨로 이동하는 구조로 정의합니다.

현재 버전에서 대화 상자의 변경된 사항과 최대한 호환할 수 있도록 탭 항목 레벨 아래 구조는 터치하지 않는 것이 중요합니다(숨김, 추가, 대체, 순서 변경 등). 대신 상위 탭 항목은 `sling:hideResource` 속성([슬링 리소스 병합 속성](https://helpx.adobe.com/kr/experience-manager/6-5/sites/developing/using/sling-resource-merger.html) 참조)과 맞춤형 구성 필드에 포함된 새 탭 항목을 통해 숨길 수 있습니다. `sling:orderBefore`를 사용하여 필요한 경우 탭 항목 순서를 변경할 수 있습니다.

아래 대화 상자는 위에서 설명한 권장 대화 상자 구조와 상속된 탭을 숨기고 대체하는 방법을 보여 줍니다.

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
                        <myTab
                               jcr:primaryType="nt:unstructured"
                               jcr:title="My Tab"
                               sling:resourceType="granite/ui/components/coral/foundation/container">
                                  
                               <!-- myTab content -->
                                  
                        </myTab>
                </items>
            </tabs>
        </items>
    </content>
</jcr:root>
```

### 핵심 구성 요소의 논리 맞춤화 {#customizing-the-logic-of-a-core-component}

슬링 모드에서 핵심 구성 요소의 비즈니스 논리를 구현합니다. 슬링 전달 패턴을 사용하여 이 논리를 확장할 수 있습니다.

예를 들어 제목 핵심 구성 요소는 요청된 리소스의 `jcr:title` 속성을 사용하여 제목 텍스트를 제공합니다. `jcr:title` 속성이 정의되지 않은 경우 현재 페이지 제목에 대한 대체가 구현됩니다. 현재 페이지 제목을 언제든지 표시할 수 있도록 비헤이비어를 변경합니다.

핵심 구성 요소 모델 구현은 비공개이기 때문에 전달 패턴으로 핵심 구성 요소를 확장해야 합니다.

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

전달 패턴에 대한 자세한 내용은 핵심 구성 요소 GitHub Wiki 문서 [슬링 모드의 전달 패턴](https://github.com/adobe/aem-core-wcm-components/wiki/Delegation-Pattern-for-Sling-Models)을 참조하십시오.

### 마크업 맞춤화 {#customizing-the-markup}

경우에 따라 고급 스타일링에는 서로 다른 구성 요소의 마크업 구조가 필요합니다.

핵심 구성 요소에서 [프록시 구성 요소](guidelines.md#proxy-component-pattern)로 수정할 수 있는 HTL 파일을 복사하여 이 작업을 간편하게 수행할 수 있습니다.

핵심 이동 경로 구성 요소의 예를 다시 사용하여 마크업 출력을 사용자 정의하기 때문에 핵심 이동 경로 구성 요소를 지정하는 `sling:resourceSuperTypes`가 포함된 사이트별 구성 요소에 `breadcrumb.html` 파일을 복사해야 합니다.

### 구성 요소 스타일링 {#styling-the-components}

맞춤화의 첫 번째 양식은 CSS 스타일 적용입니다.

이를 쉽게 수행하기 위해 핵심 구성 요소는 시맨틱 마크업을 렌더링하고 [Bootstrap](https://getbootstrap.com/)에서 영감을 얻은 표준화된 지정 규칙을 수행합니다. 간편하게 타기팅하고 개별 구성 요소의 스타일에 대해 네임스페이스를 수행하기 위해 “`cmp`” 및 “`cmp-<name>`” 클래스와 함께 각 구성 요소를 DIV 요소에서 래핑합니다.

예를 들어 v1 핵심 이동 경로 구성 요소의 HTL 파일([breadcrumb.html](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb/breadcrumb.html))을 살펴보면서 요소 출력의 계층 구조가 `ol.breadcrumb > li.breadcrumb-item > a`인지 확인합니다. 이에 CSS 규칙만 이동 경로에 영향을 미치는지 확인하려면 아래와 같이 모든 규칙에 대해 네임스페이스를 수행해야 합니다.

```shell
.cmp-breadcrumb .breadcrumb {}  
.cmp-breadcrumb .breadcrumb-item {}  
.cmp-breadcrumb a {}
```

또한, 각 핵심 구성 요소는 AEM [스타일 시스템 기능](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/style-system.html?lang=ko)을 활용합니다. 그리고 템플릿 작성자는 이 기능을 통해 페이지 작성자가 구성 요소에 적용할 수 있는 추가 CSS 클래스 이름을 정의할 수 있습니다. 이로써 각 템플릿에서 허용된 구성 요소 스타일 목록을 정의하고, 스타일 중 하나가 기본적으로 해당 구성 요소에 적용되는지 여부를 확인할 수 있습니다.

## 맞춤화 호환성 업그레이드 {#upgrade-compatibility-of-customizations}

서로 다른 세 가지 업그레이드가 가능합니다.

* AEM 버전 업그레이드 중
* 새 보조 버전으로 핵심 구성 요소 업그레이드 중
* 주요 버전으로 핵심 구성 요소 업그레이드 중

일반적으로, 구성 요소 버전이 마이그레이션 중인 새 AEM 버전을 지원하고 맞춤화 과정에서 [더 이상 사용되지 않거나 제거된](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/deprecated-removed-features.html?lang=ko) API를 사용하지 않는 경우 새 버전으로 AEM을 업그레이드하여도 핵심 구성 요소나 맞춤화 수행에는 영향을 미치지 않습니다.

이 페이지에 설명된 맞춤화 패턴을 사용하는 경우에 최신 주요 버전으로 전환하지 않고 핵심 구성 요소를 업그레이드하여도 맞춤화에는 영향을 미치지 않습니다.

최신 주요 버전의 핵심 구성 요소로 전환하면 콘텐츠 구조에만 호환될 수 있지만 맞춤화 리팩터링을 수행해야 합니다. 이 페이지에 설명된 맞춤화에 영향을 미치는 변경 사항을 강조하기 위해 각 구성 요소 버전의 변경 로그를 명확하게 게시할 수 있습니다.

## 맞춤화 지원 {#support-of-customizations}

AEM 구성 요소의 경우와 마찬가지로 맞춤화에 대해 알아야 할 부분이 많습니다.

1. **바로 핵심 구성 요소 코드를 수정하지 않습니다.**

   이로써 구성 요소를 완전히 지원할 수 있으며, 구성 요소에 대한 향후 업데이트가 어려운 프로세스가 될 수 있습니다. 대신 이 페이지에 설명된 맞춤화 방법을 사용합니다.

1. **맞춤화 코드는 사용자가 확인해야 합니다.**

   지원 프로그램은 맞춤화 코드를 다루지 않으며, 보고된 문제가 [문서화된](/help/get-started/using.md) 바닐라 핵심 구성 요소로 재현될 수 없다면 조건이 충족되지 않습니다.

1. **더 이상 사용되지 않거나 제거된 기능을 살펴봅니다.**

   새 AEM 버전으로 업그레이드가 진행 중인 상태에서 [더 이상 사용되지 않거나 제거된 기능](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/deprecated-removed-features.html?lang=ko) 페이지를 살펴보면 사용된 모든 API가 주제 항목이 됩니다.

[핵심 구성 요소 지원](overview.md#core-component-support) 섹션을 참고하십시오.

**다음 참조:**

* [핵심 구성 요소 사용](/help/get-started/using.md) - 자체 프로젝트에서 핵심 구성 요소를 시작하고 실행합니다.
* [구성 요소 가이드라인](guidelines.md) - 핵심 구성 요소의 구현 패턴에 대해 알아봅니다.

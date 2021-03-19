---
title: 핵심 구성 요소 사용자 정의
description: 핵심 구성 요소는 간단한 스타일링에서 고급 기능 재사용에 이르기까지 사용자 정의가 용이한 여러 패턴을 구현합니다.
role: 건축가, 개발자, 관리자
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '1109'
ht-degree: 2%

---


# 핵심 구성 요소 사용자 정의{#customizing-core-components}

[핵심 구성 요소](overview.md)는 간단한 스타일링에서 고급 기능 재사용에 이르기까지 사용자 정의가 용이한 여러 패턴을 구현합니다.

## 유연한 아키텍처 {#flexible-architecture}

핵심 구성 요소는 처음부터 유연성과 확장 가능성으로 설계되었습니다. 아키텍처에 대한 개요를 보면 사용자 지정이 가능한 위치를 알 수 있습니다.

![핵심 구성 요소 아키텍처](/help/assets/screen_shot_2018-12-07at093742.png)

* [디자인 대화 상자](/help/get-started/authoring.md#edit-and-design-dialogs) 는 작성자가 편집 대화 상자에서 수행할 수 있거나 할 수 없는 작업을 정의합니다.
* [편집 대화 상자](/help/get-started/authoring.md#edit-and-design-dialogs) 는 작성자가 사용할 수 있는 옵션만 표시합니다.
* [Sling 모델](#customizing-the-logic-of-a-core-component) 은 뷰(템플릿)에 대한 컨텐트를 확인하고 준비합니다.
* [Sling 모델링의 결과](#customizing-the-logic-of-a-core-component) 는 SPA 사용 사례용 JSON에 직렬화할 수 있습니다.
* [HTL은 기존 서버측 렌더링을 위해 ](#customizing-the-markup) HTMLserver-side를 렌더링합니다.
* [HTML ](#customizing-the-markup) 아웃푸티스 의미, 액세스 가능, 검색 엔진 최적화 및 스타일링하기 쉽습니다.

모든 핵심 구성 요소는 [스타일 시스템](#styling-the-components)을 구현합니다.

## AEM 프로젝트 전형 {#aem-project-archetype}

[AEM 프로젝트 ](/help/developing/archetype/overview.md) 원형에서는 권장 프록시 패턴을 사용하여 핵심 구성 요소의 논리 및 적절한 구현에 대한 SlingModels와 함께 사용자 지정 HTML 구성 요소의 예를 비롯하여 고유한 프로젝트의 시작점으로 최소 Adobe Experience Manager 프로젝트를 사용합니다.

## 사용자 지정 패턴 {#customization-patterns}

### 대화 상자 사용자 지정 {#customizing-dialogs}

[디자인 대화 상자 또는 편집 대화 상자](/help/get-started/authoring.md)와 같이 핵심 구성 요소 대화 상자에서 사용할 수 있는 구성 옵션을 사용자 지정하는 것이 필요할 수 있습니다.

각 대화 상자에는 일관된 노드 구조가 있습니다. [Sling 리소스 합병](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/sling-resource-merger.html) 및 [조건 숨기기](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/hide-conditions.html)를 사용하여 원래 대화 상자의 섹션을 숨기거나 바꾸거나 순서를 변경하는 데 사용할 수 있도록 이 구조가 상속 구성 요소에서 복제되는 것이 좋습니다. 복제할 구조는 탭 항목 노드 수준까지의 모든 것으로 정의됩니다.

현재 버전에서 대화 상자가 변경된 내용과 완전히 호환하려면 탭 항목 수준 아래의 구조를 손대지 않는 것이 중요합니다(숨김, 추가, 교체, 순서 변경 등). 대신 상위의 탭 항목은 `sling:hideResource` 속성([Sling Resource Combination Properties](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/sling-resource-merger.html) 참조)과 맞춤화된 구성 필드가 포함된 새 탭 항목을 통해 숨겨야 합니다. `sling:orderBefore` 필요한 경우 탭 항목의 순서를 변경하는 데 사용할 수 있습니다.

아래 대화 상자는 위에서 설명한 대로 권장되는 대화 상자 구조와 상속된 탭을 숨기거나 교체하는 방법을 보여 줍니다.

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

### 핵심 구성 요소 {#customizing-the-logic-of-a-core-component} 로직 사용자 지정

핵심 구성 요소에 대한 비즈니스 로직은 Sling 모델에 구현됩니다. Sling 위임 패턴을 사용하여 이 논리를 확장할 수 있습니다.

예를 들어 제목 핵심 구성 요소는 요청한 리소스의 `jcr:title` 속성을 사용하여 제목 텍스트를 제공합니다. `jcr:title` 속성이 정의되지 않은 경우 현재 페이지 제목으로의 폴백이 구현됩니다. 현재 페이지의 제목이 항상 표시되도록 동작을 변경하려고 합니다.

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

위임 패턴에 대한 자세한 내용은 핵심 구성 요소 GitHub Wiki 문서 [Sling 모델에 대한 위임 패턴](https://github.com/adobe/aem-core-wcm-components/wiki/Delegation-Pattern-for-Sling-Models)을 참조하십시오.

### 마크업 {#customizing-the-markup} 사용자 지정

고급 스타일링을 사용하려면 구성 요소의 다른 마크업 구조가 필요합니다.

이 작업은 핵심 구성 요소에서 프록시 구성 요소로 수정해야 하는 HTL 파일을 복사하여 쉽게 수행할 수 있습니다.

핵심 탐색 표시 구성 요소의 예를 다시 들어 마크업 출력을 사용자 정의하려면 `breadcrumb.html` 파일이 핵심 탐색 표시 구성 요소를 가리키는 `sling:resourceSuperTypes`이 있는 사이트 특정 구성 요소로 복사되어야 합니다.

### 구성 요소 스타일 지정 {#styling-the-components}

사용자 지정의 첫 번째 형식은 CSS 스타일을 적용하는 것입니다.

이를 쉽게 하기 위해 핵심 구성 요소는 의미 마크업을 렌더링하고 [Bootstrap](https://getbootstrap.com/)에서 영감을 받은 표준 이름 지정 규칙을 따릅니다. 또한 개별 구성 요소에 대한 스타일을 쉽게 타깃팅하고 네임스페이스하기 위해 각 핵심 구성 요소는 &quot; `cmp`&quot; 및 &quot; `cmp-<name>`&quot; 클래스로 DIV 요소에 둘러싸여 있습니다.

예를 들어, v1 코어 탐색 표시 구성 요소의 HTL 파일을 봅니다.[breadcrumb.html](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb/breadcrumb.html) 요소 출력 계층 구조는 `ol.breadcrumb > li.breadcrumb-item > a`입니다. 따라서 CSS 규칙이 해당 구성 요소의 탐색 표시 클래스에만 영향을 주도록 모든 규칙을 아래와 같이 지정해야 합니다.

```shell
.cmp-breadcrumb .breadcrumb {}  
.cmp-breadcrumb .breadcrumb-item {}  
.cmp-breadcrumb a {}
```

또한 각 핵심 구성 요소는 템플릿 작성자가 페이지 작성자가 구성 요소에 적용할 수 있는 추가 CSS 클래스 이름을 정의할 수 있도록 하는 AEM [스타일 시스템 기능](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/style-system.html)을 활용합니다. 이렇게 하면 각 템플릿에 허용된 구성 요소 스타일 목록과 이러한 스타일 중 하나를 해당 종류의 모든 구성 요소에 기본적으로 적용할지 여부를 정의할 수 있습니다.

## 사용자 지정 {#upgrade-compatibility-of-customizations} 업그레이드 호환성

다음과 같이 3가지 유형의 업그레이드가 가능합니다.

* AEM 버전 업그레이드
* 핵심 구성 요소를 새 부 버전으로 업그레이드
* 핵심 구성 요소를 주 버전으로 업그레이드

일반적으로 AEM을 새 버전으로 업그레이드하면 핵심 구성 요소 또는 사용자 지정 작업에 영향을 주지 않습니다. 구성 요소 버전은 마이그레이션되는 새 AEM 버전도 지원하고 사용자 지정 버전은 [사용되지 않거나 ](https://docs.adobe.com/content/help/ko-KR/experience-manager-cloud-service/release-notes/deprecated-removed-features.html)가 제거된 API를 사용하지 않습니다.

최신 주요 버전으로 전환하지 않고 핵심 구성 요소를 업그레이드하면 이 페이지에 설명된 사용자 지정 패턴을 사용하는 한 사용자 정의에 영향을 주지 않습니다.

핵심 구성 요소의 새로운 주요 버전으로 전환하는 것은 컨텐츠 구조에만 호환되지만 사용자 지정을 다시 팩토링해야 할 수 있습니다. 각 구성 요소 버전에 대한 변경 사항 로그 지우기가 게시되어 이 페이지에 설명된 사용자 지정 유형에 영향을 주는 변경 사항을 강조 표시합니다.

## 사용자 지정 지원 {#support-of-customizations}

모든 AEM 구성 요소와 마찬가지로 사용자 지정에 대해 알아야 할 사항이 많습니다.

1. **핵심 구성 요소의 코드를 직접 수정하지 마십시오.**

   이렇게 하면 완전히 지원되지 않을 수 있으며 향후 구성 요소 업데이트를 고통스러운 프로세스로 수행할 수 있습니다. 대신 이 페이지에 설명된 사용자 지정 방법을 사용하십시오.

1. **사용자 지정 코드는 사용자의 책임입니다.**

   Adobe 지원 프로그램은 사용자 지정 코드를 포함하지 않으며, 문서화된](/help/get-started/using.md)으로 사용되는 바닐라 코어 구성 요소로 재현할 수 없는 보고된 문제는 적용되지 않습니다.[

1. **사용 중단되거나 제거된 기능을 봅니다.**

   새 AEM 버전이 업그레이드될 때마다 사용된 모든 API가 [더 이상 사용되지 않음 및 제거된 기능](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/release-notes/deprecated-removed-features.html) 페이지를 참고하여 여전히 시의적인지 확인합니다.

[핵심 구성 요소 지원](overview.md#core-component-support) 섹션을 참조하십시오.

**다음 참조:**

* [핵심 구성 요소](/help/get-started/using.md)  사용 - 프로젝트에서 핵심 구성 요소를 바로 사용할 수 있습니다.
* [구성 요소 지침](guidelines.md)  - 핵심 구성 요소의 구현 패턴을 학습합니다.

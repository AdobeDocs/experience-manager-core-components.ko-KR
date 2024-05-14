---
title: 적응형 양식 조각
description: 양식 조각을 사용하여 양식 세그먼트 또는 필드 그룹을 생성하고 이를 적응형 양식 전체에서 재사용하여 효율성과 재사용성을 개선할 수 있습니다.
role: Architect, Developer, Admin, User
exl-id: bde4a416-1d6b-4e9e-ac74-70fccef473cb
source-git-commit: c3401da271efd930d1a2711bcab25c29f763f38e
workflow-type: tm+mt
source-wordcount: '1895'
ht-degree: 93%

---

# 적응형 양식 단편 구성 요소 {#form-fragment-component-adaptive-forms-core-component}

<span class="preview"> 이 문서에는 다음 내용에 대한 내용이 포함되어 있습니다.  **제목의 리치 텍스트 허용**  기능, 프리릴리스 기능 프리릴리스 기능은 다음을 통해서만 액세스할 수 있습니다. [프리릴리스 채널](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html#new-features).</span>

적응형 양식은 패널이나 필드 그룹과 같은 양식 세그먼트를 생성하여 다양한 적응형 양식에서 재사용할 수 있는 편리한 방법을 제공합니다. 이러한 재사용 가능한 독립 세그먼트를 [적응형 양식 조각](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/adaptive-form-fragments-core-components.html)이라고 합니다.

[문서에 조각을 여러 번 추가](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/adaptive-form-fragments-core-components.html#insert-a-fragment-in-an-adaptive-form)하고 해당 구성 요소의 데이터 바인딩 속성을 사용하여 조각을 다른 데이터 소스나 스키마에 연결할 수 있습니다. 예를 들어 영구, 통신 및 청구 주소에 동일한 주소 조각을 사용하고 이를 데이터 소스 또는 스키마의 다른 필드에 연결할 수 있습니다.

![예](/help/adaptive-forms/assets/using-multiple-fragment-af.gif)


또한 [반복 옵션](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html)을 사용하여 양식 조각 구성 요소와 해당 하위 구성 요소를 복제하고, 최소 및 최대 반복 횟수를 정의하고, 양식 내에서 유사한 섹션을 손쉽게 복제할 수도 있습니다.

>[!NOTE]
>
> [적응형 양식 조각을 처음부터 생성](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/adaptive-form-fragments-core-components.html#create-a-fragment)하거나 기존 적응형 양식의 패널을 조각으로 저장할 수 있습니다.

## 사용 {#usage}

- **재사용성**: 여러 적응형 양식 전체에서 양식 조각을 재사용할 수 있다는 점은 양식 조각 사용의 주요 이점입니다. 조각에 대한 변경 사항이 조각이 사용되는 모든 인스턴스에 반영되므로 디자인과 기능의 일관성을 유지할 수 있습니다.

- **일관된 사용자 경험**: 머리글이나 바닥글과 같은 공통 요소에 양식 조각을 사용하면 일관되고 응집력 있는 사용자 경험이 보장됩니다.

- **손쉬운 유지 관리**: 양식 조각에 대한 변경 사항이나 수정 사항은 해당 양식 조각이 사용되는 모든 인스턴스에 반영됩니다. 이를 통해 유지 관리가 단순화되고 오류 가능성이 줄어듭니다.

- **효율성**: 디자이너와 개발자는 양식 조각을 한 번만 작성하고 테스트하여 시간을 절약할 수 있습니다. 그런 다음 중복 작업 없이 양식 조각을 여러 적응형 양식에 쉽게 통합할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

적응형 양식 조각 핵심 구성 요소는 Cloud Service의 핵심 구성 요소 2.0.50 및 AEM 6.5.16.0 Forms 이상의 핵심 구성 요소 1.1.26 일부로 릴리스되었습니다. 다음 표에서는 지원되는 모든 버전, AEM 호환성 및 해당 문서에 대한 링크를 보여 줍니다.

| 구성 요소 버전 | AEM as a Cloud Service | AEM 6.5.16.0 Forms 이상 |
|---|---|---|
| v1 | <br>[릴리스 2.0.50](/help/adaptive-forms/version.md) 이상 버전과 호환 가능 | <br>[릴리스 1.1.26](/help/adaptive-forms/version.md) 이상과 호환합니다(2.0.0 이전 버전). |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/adaptive-forms/version.md) 문서를 참조하십시오.

## 기술 세부 정보 {#technical-details}

적응형 양식 조각 핵심 구성 요소에 대한 최신 정보는 [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/fragment)의 기술 설명서에서 확인할 수 있습니다. 핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 확인하십시오.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자를 사용하여 방문자를 위한 조각 경험을 손쉽게 사용자 정의할 수 있습니다. 조각 속성을 간편하게 정의하여 원활한 사용자 경험을 제공할 수도 있습니다.

### 기본 탭 {#basic-tab}

![기본 탭](/help/adaptive-forms/assets/fragment-basictab.png)

- **이름** - 양식과 규칙 편집기 모두에서 고유한 이름으로 양식 구성 요소를 쉽게 식별할 수 있습니다. 단, 이름에는 공백이나 특수 문자가 포함되어서는 안 됩니다.

- **제목** - 제목을 사용하면 양식에서 구성 요소를 쉽게 식별할 수 있으며, 기본적으로 제목은 구성 요소 상단에 나타납니다. 제목을 추가하지 않으면 제목 텍스트 대신 구성 요소의 이름이 표시됩니다.
- **제목의 리치 텍스트 허용** - 이 기능을 사용하면 굵게, 기울임꼴, 밑줄이 그어진 텍스트, 다양한 글꼴, 글꼴 크기, 색상 및 추가 옵션과 같은 기능을 통합하여 일반 텍스트 제목의 서식을 지정할 수 있어 시각적 프레젠테이션 및 맞춤화를 향상시킬 수 있습니다. 문서, 웹 사이트 또는 애플리케이션 내에서 제목을 돋보이게 할 때 더 큰 유연성과 창의적인 제어를 제공합니다.\
  에 대한 확인란을 선택하면 **제목의 리치 텍스트 허용** 를 클릭하면 구성 요소 제목의 스타일을 지정하는 서식 지정 옵션이 표시됩니다. 사용 가능한 모든 서식 옵션에 액세스하려면 ![전체 화면 아이콘](/help/adaptive-forms/assets/fullscreen-icon.png) 탭.

  ![리치 텍스트 지원](/help/adaptive-forms/assets/richtext-support-title.png)

- **제목 숨기기** - 구성 요소의 제목을 숨기려면 이 옵션을 선택합니다.
- **양식 제출 시 하위 구성 요소의 데이터 그룹화(오브젝트에 데이터 래핑)** - 이 옵션을 선택하면 하위 구성 요소의 데이터가 상위 구성 요소의 JSON 오브젝트 내에 중첩됩니다. 그러나 이 옵션을 선택하지 않으면 제출된 JSON 데이터는 상위 구성 요소에 대한 오브젝트가 없는 평면 구조를 갖습니다. 예:

   - 이 옵션을 선택하면 하위 구성 요소(예: 도로 번호, 구/군/시 및 우편 번호)의 데이터가 상위 구성 요소(주소) 내에 JSON 오브젝트로 중첩됩니다. 이렇게 하면 계층 구조가 생성되고 데이터는 상위 구성 요소 아래에 구성됩니다.

     제출된 데이터의 구조:

     ```JSON
     { "Address":
     
     { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
     
     }
     ```

   - 이 옵션을 선택하지 않으면 제출된 JSON 데이터는 상위 구성 요소(주소)에 대한 오브젝트가 없는 평면 구조를 갖습니다. 모든 데이터는 계층 구조 없이 동일한 수준에 있습니다.


     제출된 데이터의 구조:

     ```JSON
        { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
     ```

- **조각 참조** - 조각 참조는 외부 데이터 소스에 저장되고 양식에서 사용되는 양식 조각에 대한 참조입니다. 조각 참조를 사용하면 양식 조각을 양식에 동적으로 바인딩할 수 있습니다.

- **바인드 참조** - 바인드 참조는 외부 데이터 소스에 저장되고 양식에서 사용되는 데이터 요소에 대한 참조입니다. 바인드 참조를 사용하면 데이터를 양식 필드에 동적으로 바인딩하여 양식이 데이터 소스의 최신 데이터를 표시하도록 할 수 있습니다. 예를 들어 바인드 참조를 사용하여 양식에 입력된 고객의 ID를 기반으로 고객의 이름과 주소를 양식에 표시할 수 있습니다. 바인드 참조를 사용하여 양식에 입력된 데이터로 데이터 소스를 업데이트할 수도 있습니다. 이러한 방식으로 AEM Forms를 사용하면 외부 데이터 소스와 상호 작용하는 양식을 만들어 데이터 수집 및 관리를 위한 원활한 사용자 경험을 제공할 수 있습니다.

- **구성 요소 숨기기** - 양식에서 구성 요소를 숨기려면 이 옵션을 선택합니다. 구성 요소는 다른 용도로(예: 규칙 편집기에서 계산에 사용) 계속 액세스할 수 있습니다. 구성 요소 숨기기는 사용자가 보거나 직접 변경할 필요가 없는 정보를 저장해야 할 때 유용합니다.
- **구성 요소 비활성화** - 구성 요소를 비활성화하려면 이 옵션을 선택합니다. 비활성화된 구성 요소는 활성 상태가 아니므로 최종 사용자가 편집할 수 없습니다. 사용자는 필드 값을 볼 수 있지만 수정할 수는 없습니다. 구성 요소는 다른 용도로(예: 규칙 편집기에서 계산에 사용) 계속 액세스할 수 있습니다.
- **읽기 전용** - 구성 요소를 편집할 수 없도록 만들려면 이 옵션을 선택합니다. 사용자는 필드 값을 볼 수 있지만 수정할 수는 없습니다. 구성 요소는 다른 용도로(예: 규칙 편집기에서 계산에 사용) 계속 액세스할 수 있습니다.

### 조각 반복 탭 {#repeat-tab}

![조각 반복 탭](/help/adaptive-forms/assets/fragment-repeattab.png)

- **조각을 반복 가능하도록 설정**: 사용자가 반복 기능을 활성화 또는 비활성화할 수 있는 토글 기능입니다.
- **최소 반복**: 조각 구성 요소를 반복할 수 있는 최소 횟수를 설정합니다. 값이 0이면 조각 구성 요소가 반복되지 않음을 나타냅니다. 기본값은 0입니다.
- **최대 반복**: 조각 구성 요소를 반복할 수 있는 최대 횟수를 설정합니다. 기본적으로 이 값은 무제한입니다.

### 도움말 콘텐츠 탭 {#help-content}

![도움말 콘텐츠 탭](/help/adaptive-forms/assets/fragment-helptab.png)

- **간단한 설명** - 간단한 설명은 특정 양식 필드의 용도에 대한 추가 정보 또는 설명을 제공하는 간단한 텍스트 설명입니다. 사용자가 필드에 입력해야 하는 데이터 유형을 이해하는 데 도움이 되며 입력된 정보가 유효하고 원하는 기준을 충족하는지 확인하는 데 도움이 되는 지침 또는 예시를 제공할 수 있습니다. 기본적으로 간단한 설명은 숨겨진 상태로 유지됩니다. **간단한 설명 항상 표시** 옵션을 활성화하여 구성 요소 아래에 표시할 수 있습니다.

- **간단한 설명 항상 표시** - 이 옵션을 활성화하여 구성 요소 아래에 간단한 설명을 표시할 수 있습니다.

- **도움말 텍스트** - 도움말 텍스트는 양식 필드를 올바르게 작성하는 데 도움이 되도록 사용자에게 제공되는 추가 정보 또는 지침을 나타냅니다. 구성 요소 옆에 있는 도움말 아이콘(i)을 클릭하면 표시됩니다. 도움말 텍스트는 양식 필드의 레이블이나 플레이스홀더 텍스트보다 더 자세한 정보를 제공하며 사용자가 필드의 요구 사항이나 제한 사항을 이해하는 데 도움이 되도록 설계되었습니다. 또한 양식을 보다 쉽고 정확하게 작성할 수 있도록 제안이나 예시를 제공할 수도 있습니다.

### 접근성 {#accessibility}

![접근성 탭](/help/adaptive-forms/assets/fragment-accessibilitytab.png)

- **화면 판독기용 텍스트** - 화면 판독기용 텍스트는 시각 장애인이 사용하는 화면 판독기와 같은 보조 기술로 읽을 수 있도록 특별히 고안된 추가 텍스트를 나타냅니다. 이 텍스트는 양식 필드의 용도에 대한 오디오 설명을 제공하며, 여기에는 필드의 제목, 설명, 이름 및 관련 메시지(사용자 정의 텍스트)에 대한 정보가 포함될 수 있습니다. 화면 판독기 텍스트는 시각 장애가 있는 사용자를 포함한 모든 사용자가 양식에 액세스할 수 있도록 돕고 양식 필드 및 해당 요구 사항을 완전히 이해할 수 있도록 합니다.

- **화면 판독기가 알릴 HTML 역할** - HTML 역할은 화면 판독기와 같은 보조 기술에 대한 HTML 요소의 용도를 지정하는 데 사용되는 속성입니다. 역할 속성은 요소에 추가 컨텍스트 및 의미를 제공하는 데 사용되며, 이를 통해 화면 판독기는 콘텐츠를 더 쉽게 해석하고 사용자에게 알릴 수 있습니다. 예를 들어 AEM Forms에서 양식 필드의 레이블은 “레이블”이라는 역할을 가질 수 있으며 해당 입력 필드는 “텍스트 상자”라는 역할을 가질 수 있습니다. 이렇게 하면 화면 판독기가 레이블과 입력 필드 간의 관계를 이해하고 사용자에게 올바르게 알릴 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

디자인 대화 상자는 양식 조각 구성 요소의 CSS 스타일을 정의하고 관리하는 데 사용됩니다.

### 스타일 탭 {#styles-tab}

적응형 양식 양식 조각 핵심 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

![디자인 대화 상자](/help/adaptive-forms/assets/checkbox-style.png)

- **기본 CSS 클래스**: 적응형 양식 양식 조각 핵심 구성 요소에 기본 CSS 클래스를 제공할 수 있습니다.

- **허용된 스타일**: 이름과 스타일을 나타내는 CSS 클래스를 제공하여 스타일을 정의할 수 있습니다. 예를 들어 “bold text”라는 스타일을 만들고 “font-weight: bold”라는 CSS 클래스를 제공할 수 있습니다. 적응형 양식 편집기에서 이러한 스타일을 적응형 양식에 사용하거나 적용할 수 있습니다. 스타일을 적용하려면 적응형 양식 편집기에서 스타일을 적용할 구성 요소를 선택하고 속성 대화 상자로 이동한 다음 **스타일** 드롭다운 목록에서 원하는 스타일을 선택합니다. 스타일을 업데이트하거나 수정해야 하는 경우 디자인 대화 상자로 돌아가서 스타일 탭에서 스타일을 업데이트하고 변경 내용을 저장하면 됩니다.

### 사용자 정의 속성

![사용자 정의 속성 대화 상자](/help/adaptive-forms/assets/checkbox-customproperties.png)

사용자 정의 속성을 사용하면 양식 템플릿을 사용하여 사용자 정의 속성(키-값 쌍)을 적응형 양식 핵심 구성 요소에 연결할 수 있습니다. 사용자 정의 속성은 구성 요소의 Headless 렌디션에서 속성 섹션에 반영됩니다. 사용자 정의 속성 값에 따라 조정되는 동적 양식 동작을 만들 수 있습니다. 예를 들어 개발자는 모바일, 데스크탑 또는 웹 플랫폼을 위한 Headless 양식 구성 요소의 다양한 표현을 디자인하여 다양한 디바이스에서 사용자 경험을 크게 향상시킬 수 있습니다.

- **그룹 이름**: 사용자 정의 속성 그룹을 식별하기 위해 이름을 제공할 수 있습니다. 여러 사용자 정의 속성 그룹을 추가, 삭제 또는 재배열할 수 있습니다. 사용자 정의 속성 그룹을 추가하면 다음 옵션이 표시됩니다.

   - **키-값 쌍**: 각 사용자 정의 속성 그룹의 **추가** 버튼을 클릭하여 여러 사용자 정의 속성 이름과 사용자 정의 속성 값을 추가할 수 있습니다.

   - **삭제**: 사용자 정의 속성 이름과 사용자 정의 속성 값을 탭하거나 클릭하여 삭제할 수 있습니다.

   - **재배열**: 사용자 정의 속성 이름과 사용자 정의 속성 값을 누르거나 클릭하고 드래그하면 재배열할 수 있습니다.


## 관련 문서 {#related-articles}

{{more-like-this}}

## 추가 참조 {#see-also}

{{see-also}}

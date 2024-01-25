---
title: 적응형 양식 단편
description: 양식 조각을 사용하여 양식 세그먼트나 필드 그룹을 만들고 적응형 Forms에서 재사용하여 효율성과 재사용성을 향상시킬 수 있습니다.
role: Architect, Developer, Admin, User
hide: true
hidefromToC: true
source-git-commit: 9b97ea68d176d5194844093afdc41b82bdb45fee
workflow-type: tm+mt
source-wordcount: '1675'
ht-degree: 66%

---


# 양식 단편 구성 요소 {#form-fragment-component-adaptive-forms-core-component}

적응형 Forms은 패널이나 필드 그룹과 같은 양식 세그먼트를 편리하게 만들어 다른 적응형 Forms에서 재사용할 수 있도록 합니다. 이러한 재사용 가능한 독립 세그먼트를 라고 합니다. [적응형 양식 단편](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/adaptive-form-fragments-core-components.html).

다음을 수행할 수 있습니다. [문서에 조각을 여러 번 추가](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/adaptive-form-fragments-core-components.html#insert-a-fragment-in-an-adaptive-form) 구성 요소의 데이터 바인딩 속성을 사용하여 다른 데이터 소스 또는 스키마에 연결합니다. 예를 들어 영구, 통신 및 청구 주소에 동일한 주소 조각을 사용하여 데이터 소스 또는 스키마의 다른 필드에 연결할 수 있습니다.

![예](/help/adaptive-forms/assets/using-multiple-fragment-af.gif)


다음을 사용할 수도 있습니다 [반복 옵션](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html) 양식 조각 구성 요소와 하위 구성 요소를 복제하려면 최소 및 최대 반복 횟수를 정의하고 양식 내에서 유사한 섹션을 쉽게 복제할 수 있습니다.

>[!NOTE]
>
> 다음을 수행할 수 있습니다. [적응형 양식 단편 만들기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/adaptive-form-fragments-core-components.html#create-a-fragment) 기존 적응형 양식에 패널을 처음부터 새로 만들거나 조각으로 저장합니다.

## 사용 {#usage}

- **재사용 가능성**: 여러 적응형 Forms에서 양식 조각을 재사용할 수 있는 기능은 양식 조각 사용의 주요 이점입니다. 조각에 대한 변경 사항은 사용된 모든 인스턴스에 반영되므로 디자인과 기능의 일관성을 유지하는 데 도움이 됩니다.

- **일관된 사용자 경험**: 머리글이나 바닥글과 같은 일반적인 요소에 양식 조각을 사용하면 일관되고 일관된 사용자 경험을 확보할 수 있습니다.

- **손쉬운 유지 관리**: 양식 조각에 수행된 변경 또는 수정 사항은 이 조각이 사용되는 모든 인스턴스에 반영됩니다. 유지 관리를 단순화하고 오류 가능성을 줄입니다.

- **효율성**: 디자이너와 개발자는 양식 조각을 한 번만 빌드하고 테스트하여 시간을 절약합니다. 그런 다음 양식 조각을 중복 작업 없이 여러 적응형 Forms에 쉽게 통합할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

적응형 Forms 조각 핵심 구성 요소는 Cloud Service을 위한 핵심 구성 요소 2.0.50 및 AEM 6.5.16.0 Forms 이상을 위한 핵심 구성 요소 1.1.26의 일부로 릴리스되었습니다. 다음 표에서는 지원되는 모든 버전, AEM 호환성 및 해당 문서에 대한 링크를 보여 줍니다.

| 구성 요소 버전 | AEM as a Cloud Service | AEM 6.5.16.0 Forms 이상 |
|---|---|---|
| v1 | <br>[릴리스 2.0.50](/help/adaptive-forms/version.md) 이상 버전과 호환 가능 | <br>[릴리스 1.1.26](/help/adaptive-forms/version.md) 이상과 호환합니다(2.0.0 이전 버전). |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/adaptive-forms/version.md) 문서를 참조하십시오.

## 기술 세부 정보 {#technical-details}

의 기술 설명서에서 적응형 Forms 조각 핵심 구성 요소에 대한 최신 정보를 알아보십시오 [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/fragment). 핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 확인하십시오.

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자를 통해 방문자의 조각 경험을 손쉽게 맞춤화할 수 있습니다. 또한 원활한 사용자 경험을 위해 조각 속성을 쉽게 정의할 수 있습니다.

### 기본 탭 {#basic-tab}

![기본 탭](/help/adaptive-forms/assets/fragment-basictab.png)

- **이름** - 양식과 규칙 편집기 모두에서 고유한 이름으로 양식 구성 요소를 쉽게 식별할 수 있습니다. 단, 이름에는 공백이나 특수 문자가 포함되어서는 안 됩니다.

- **제목** - 제목을 사용하면 양식에서 구성 요소를 쉽게 식별할 수 있으며, 기본적으로 제목은 구성 요소 상단에 나타납니다. 제목을 추가하지 않으면 제목 텍스트 대신 구성 요소의 이름이 표시됩니다.

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

### 단편 반복 탭 {#repeat-tab}

![단편 반복 탭](/help/adaptive-forms/assets/fragment-repeattab.png)

- **반복 가능한 조각 만들기**: 사용자가 반복 기능을 활성화하거나 비활성화할 수 있는 전환 기능입니다.
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

## 디자인 대화 상자 {#design-dialog}

디자인 대화 상자 를 사용하여 양식 단편 구성 요소의 CSS 스타일을 정의하고 관리합니다.

### 스타일 탭 {#styles-tab}

적응형 양식 단편 핵심 구성 요소는 AEM을 지원합니다. [스타일 시스템](/help/get-started/authoring.md#component-styling).

![디자인 대화 상자](/help/adaptive-forms/assets/checkbox-style.png)

- **기본 CSS 클래스**: 적응형 양식 단편 핵심 구성 요소에 기본 CSS 클래스를 제공할 수 있습니다.

- **허용된 스타일**: 이름과 스타일을 나타내는 CSS 클래스를 제공하여 스타일을 정의할 수 있습니다. 예를 들어 “bold text”라는 스타일을 만들고 “font-weight: bold”라는 CSS 클래스를 제공할 수 있습니다. 적응형 양식 편집기에서 이러한 스타일을 적응형 양식에 사용하거나 적용할 수 있습니다. 스타일을 적용하려면 적응형 양식 편집기에서 스타일을 적용할 구성 요소를 선택하고 속성 대화 상자로 이동한 다음 **스타일** 드롭다운 목록에서 원하는 스타일을 선택합니다. 스타일을 업데이트하거나 수정해야 하는 경우 디자인 대화 상자로 돌아가서 스타일 탭에서 스타일을 업데이트하고 변경 내용을 저장하면 됩니다.

### 사용자 정의 속성

![사용자 정의 속성 대화 상자](/help/adaptive-forms/assets/checkbox-customproperties.png)

사용자 지정 속성을 사용하면 양식 템플릿을 사용하여 사용자 지정 속성(키-값 쌍)을 적응형 양식 핵심 구성 요소에 연결할 수 있습니다. 사용자 정의 속성은 구성 요소의 Headless 렌디션에서 속성 섹션에 반영됩니다. 사용자 정의 속성 값에 따라 조정되는 동적 양식 동작을 만들 수 있습니다. 예를 들어 개발자는 모바일, 데스크탑 또는 웹 플랫폼을 위한 Headless 양식 구성 요소의 다양한 표현을 디자인하여 다양한 디바이스에서 사용자 경험을 크게 향상시킬 수 있습니다.

- **그룹 이름**: 사용자 정의 속성 그룹을 식별하기 위해 이름을 제공할 수 있습니다. 여러 사용자 정의 속성 그룹을 추가, 삭제 또는 재배열할 수 있습니다. 사용자 정의 속성 그룹을 추가하면 다음 옵션이 표시됩니다.

   - **키-값 쌍**: 각 사용자 정의 속성 그룹의 **추가** 버튼을 클릭하여 여러 사용자 정의 속성 이름과 사용자 정의 속성 값을 추가할 수 있습니다.

   - **삭제**: 사용자 정의 속성 이름과 사용자 정의 속성 값을 탭하거나 클릭하여 삭제할 수 있습니다.

   - **재배열**: 탭하거나 클릭하고 드래그하여 사용자 지정 속성 이름과 사용자 지정 속성 값을 재배열합니다.

## 관련 문서 {#related-articles}

{{more-like-this}}

## 추가 참조 {#see-also}

{{see-also}}







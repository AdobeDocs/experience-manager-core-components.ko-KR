---
title: 적응형 양식 핵심 구성 요소 - 이미지
description: 적응형 양식 이미지 핵심 구성 요소를 사용 또는 사용자 정의합니다.
role: Architect, Developer, Admin, User
exl-id: 9ee42d5d-16e3-4973-8364-5bc512ebe72e
source-git-commit: be630c4d0a10ebaa679b77419b901fac818addb1
workflow-type: ht
source-wordcount: '1015'
ht-degree: 100%

---

# 이미지 {#image-adaptive-forms-core-component}

적응형 양식의 이미지 구성 요소를 사용하여 양식에 이미지를 포함할 수 있습니다. 이러한 이미지를 사용하여 양식의 전반적인 디자인을 개선하거나, 추가 정보를 제공하거나, 사용자가 양식의 용도를 이해하는 데 도움이 되는 시각 자료로 사용할 수 있습니다. 이미지 구성 요소를 사용하여 양식에 로고, 사진 또는 그래픽을 추가할 수 있습니다.

접근성을 위해 이미지에 대한 **대체 텍스트**&#x200B;를 지정하여 이미지를 볼 수 없는 사용자에게 이미지를 설명하는 간단한 대체 텍스트를 제공하는 것이 중요합니다.


**예**

![](/help/adaptive-forms/assets/image.png)


## 사용 {#reasons-to-use-image-in-a-form}

적응형 양식에 이미지 구성 요소를 포함하는 것이 유익한 몇 가지 이유는 다음과 같습니다.

* **브랜딩**: 이미지를 사용하여 양식을 만든 조직의 로고나 이름을 표시할 수 있으므로 브랜드 인지도와 신뢰성을 확립하는 데 도움이 됩니다.

* **시각 자료**: 이미지는 사용자가 양식의 용도를 이해하는 데 도움이 되는 시각 자료 역할을 하여 사용자에게 추가 정보를 제공하는 데 도움이 될 수 있습니다.

* **장식**: 이미지를 사용하여 양식의 전반적인 디자인을 개선하고 시각적으로 더 매력적으로 만들 수 있습니다.

* **사용자 경험**: 이미지를 사용하면 사용자가 명확하고 직관적으로 양식 필드에 액세스하고 채울 수 있으므로 양식을 보다 사용자 친화적으로 만들 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

적응형 양식 아코디언 핵심 구성 요소는 Cloud Service의 핵심 구성 요소 2.0.4 및 AEM 6.5.16.0 Forms 이상의 핵심 구성 요소 1.1.12 일부로 2023년 2월에 릴리스되었습니다. 다음 표에서는 지원되는 모든 버전, AEM 호환성 및 해당 문서에 대한 링크를 보여 줍니다.

| 구성 요소 버전 | AEM as a Cloud Service | AEM 6.5.16.0 Forms 이상 |
|---|---|---|
| v1 | 호환 가능 <br>[2.0.4](/help/adaptive-forms/version.md) 및 이후 릴리스 | <br>[릴리스 1.1.12](/help/adaptive-forms/version.md) 이상과 호환합니다(2.0.0 이전 버전). |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/adaptive-forms/version.md) 문서를 참조하십시오.


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## 기술 세부 정보 {#technical-details}

적응형 양식 이미지 핵심 구성 요소에 대한 최신 정보는 [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/image/v1/image)의 기술 설명서에서 확인할 수 있습니다. 핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 확인하십시오.


## 구성 대화 상자 {#configure-dialog}

구성 대화 상자를 사용하여 방문자를 위한 이미지 경험을 손쉽게 사용자 정의할 수 있습니다. 이미지 옵션을 간편하게 정의하여 원활한 사용자 경험을 제공할 수도 있습니다.

![속성 탭](/help/adaptive-forms/assets/image_properties.png)

* **이름** - 양식과 규칙 편집기 모두에서 고유한 이름으로 양식 구성 요소를 쉽게 식별할 수 있습니다. 단, 이름에는 공백이나 특수 문자가 포함되어서는 안 됩니다.

* **제목** - 제목을 사용하면 양식에서 구성 요소를 쉽게 식별할 수 있으며, 기본적으로 제목은 구성 요소 상단에 나타납니다. 제목을 추가하지 않으면 제목 텍스트 대신 구성 요소의 이름이 표시됩니다.

* **기록 문서 바인드 참조** - 이 옵션을 사용하면 적응형 양식 필드를 기록 문서 필드와 연결할 수 있습니다. 사용자가 적응형 양식의 연결된 필드에 값을 입력하면 해당 기록 문서의 연결된 필드에도 해당 값이 나타납니다. 예를 들어 기록 문서 바인드 참조를 사용하여 기록 문서에 입력된 고객의 ID를 기반으로 고객의 이름과 주소를 양식에 표시할 수 있습니다. 이러한 방식으로 AEM Forms를 사용하면 기록 문서를 생성하고 데이터 수집 및 관리를 위한 원활한 사용자 경험을 제공할 수 있습니다.

* **설명** - 설명은 특정 이미지의 용도에 대한 추가 정보 또는 설명을 제공하는 간단한 텍스트 설명입니다.

* **여기에 자산을 놓거나 업로드할 파일 검색** - 이 옵션을 사용하면 마우스 드래그 앤 드롭으로 이미지와 같은 자산을 놓을 수 있습니다. **검색** 버튼을 사용하여 로컬 파일 시스템에서 파일을 업로드할 수도 있습니다. 이미지를 추가하면 이미지 하단에 세 개의 버튼이 나타납니다.
   * **편집** - 자산 편집기에서 자산 렌디션을 관리하려면 **편집**&#x200B;을 탭하거나 클릭합니다.
   * **지우기** - 현재 선택된 이미지의 선택을 해제하려면 **지우기**&#x200B;를 탭하거나 클릭합니다.
   * **선택** - 자산 폴더에서 다른 이미지를 선택하려면 **선택**&#x200B;을 탭하거나 클릭합니다.

* **대체 텍스트** - 이 옵션은 시각 장애가 있는 사용자에게 이미지를 설명해 주는 이미지에 대한 간단한 대체 텍스트를 제공하는 텍스트를 입력하는 데 사용됩니다.

* **구성 요소 숨기기** - 양식에서 구성 요소를 숨기려면 이 옵션을 선택합니다. 구성 요소는 다른 용도로(예: 규칙 편집기에서 계산에 사용) 계속 액세스할 수 있습니다. 구성 요소 숨기기는 사용자가 보거나 직접 변경할 필요가 없는 정보를 저장해야 할 때 유용합니다.

* **읽기 전용** - 구성 요소를 편집할 수 없도록 만들려면 이 옵션을 선택합니다. 사용자는 필드 값을 볼 수 있지만 수정할 수는 없습니다. 구성 요소는 다른 용도로(예: 규칙 편집기에서 계산에 사용) 계속 액세스할 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

디자인 대화 상자는 이미지 구성 요소의 CSS 스타일을 정의하고 관리하는 데 사용됩니다.

### 스타일 탭 {#styles-tab}

탭은 구성 요소의 CSS 스타일을 정의하고 관리하는 데 사용됩니다. 적응형 양식 이미지 핵심 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.

![디자인 대화 상자](/help/adaptive-forms/assets/image_designdialog.png)

**기본 CSS 클래스**: 적응형 양식 이미지 핵심 구성 요소에 기본 CSS 클래스를 제공할 수 있습니다.

**허용된 스타일**: 이름과 스타일을 나타내는 CSS 클래스를 제공하여 스타일을 정의할 수 있습니다. 예를 들어 “bold text”라는 스타일을 만들고 “font-weight: bold”라는 CSS 클래스를 제공할 수 있습니다. 적응형 양식 편집기에서 이러한 스타일을 적응형 양식에 사용하거나 적용할 수 있습니다. 스타일을 적용하려면 적응형 양식 편집기에서 스타일을 적용할 구성 요소를 선택하고 속성 대화 상자로 이동한 다음 **스타일** 드롭다운 목록에서 원하는 스타일을 선택합니다. 스타일을 업데이트하거나 수정해야 하는 경우 디자인 대화 상자로 돌아가서 스타일 탭에서 스타일을 업데이트하고 변경 내용을 저장하면 됩니다.

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->


>[!MORELIKETHIS]
>
>* [아코디언](/help/adaptive-forms/components/accordion.md)
>* [버튼](/help/adaptive-forms/components/button.md)
>* [확인란 그룹](/help/adaptive-forms/components/checkbox-group.md)
>* [날짜 선택기](/help/adaptive-forms/components/date-picker.md)
>* [드롭다운 목록](/help/adaptive-forms/components/drop-down.md)
>* [이메일 입력](/help/adaptive-forms/components/email-input.md)
>* [양식 컨테이너](/help/adaptive-forms/components/form-container.md)
>* [첨부 파일](/help/adaptive-forms/components/file-attachment.md)
>* [바닥글](/help/adaptive-forms/components/footer.md)
>* [헤더](/help/adaptive-forms/components/header.md)
>* [가로 탭](/help/adaptive-forms/components/horizontal-tabs.md)
>* [숫자 입력](/help/adaptive-forms/components/number-input.md)
>* [패널 컨테이너](/help/adaptive-forms/components/panel-container.md)
>* [라디오 버튼](/help/adaptive-forms/components/radio-button.md)
>* [재설정 버튼](/help/adaptive-forms/components/reset-button.md)
>* [제출 버튼](/help/adaptive-forms/components/submit-button.md)
>* [전화번호 입력](/help/adaptive-forms/components/telephone-input.md)
>* [텍스트 입력](/help/adaptive-forms/components/text-input.md)
>* [텍스트](/help/adaptive-forms/components/text.md)
>* [제목](/help/adaptive-forms/components/title.md)
>* [마법사](/help/adaptive-forms/components/wizard.md)


## 추가 참조 {#see-also}

{{see-also}}
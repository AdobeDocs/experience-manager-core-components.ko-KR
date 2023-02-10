---
title: AEM 응용 Forms 핵심 구성 요소 소개
description: 적응형 Forms 핵심 구성 요소의 유연성을 사용하여 매력적인 등록 경험(양식)을 만들고 Adobe Experience Manager의 강력한 기능을 사용하여 전달할 수 있습니다.
role: Architect, Developer, Admin, User
source-git-commit: 86fa434d884b24b8d4b231c6108f5e6151a89813
workflow-type: tm+mt
source-wordcount: '1231'
ht-degree: 11%

---


# 응용 Forms 핵심 구성 요소 소개 {#adaptive-forms-core-components-introduction}

Adobe Experience Manager에서 적응형 Forms 핵심 구성 요소를 사용하면 사용 가능한 유연성 및 사용자 지정 옵션을 활용하여 매력적인 등록 경험을 만들 수 있습니다.

## 핵심 구성 요소  {#overview}

Adobe Experience Manager(AEM)에서 구성 요소는 페이지 및 양식을 만드는 데 사용되는 빌딩 블록입니다. Labs는 작성자가 컨텐츠를 만들고 관리할 수 있는 간단하고 강력한 방법을 제공하는 동시에 개발자에게 사용자 지정 구성 요소를 만드는 데 필요한 유연성과 확장성을 제공합니다. 이 설계는 개발 시간을 단축하고 웹 사이트 및 양식에 대한 유지 관리 비용을 절감하도록 설계되었으며, 유연하고 웹 사이트 및 양식의 특정 요구 사항에 맞게 손쉽게 사용자 지정할 수 있습니다.

핵심 구성 요소는 또한 반응형으로 설계되고 데스크톱, 태블릿 및 스마트폰을 비롯한 다양한 장치를 지원하도록 설계되었습니다. 또한 최신 웹 표준 및 모범 사례를 준수하여 웹 컨텐츠를 만들 수 있는 강력하고 안정적인 솔루션을 제공합니다.

전반적으로 핵심 구성 요소는 AEM에서 웹 컨텐츠를 만들고 관리하는 데 필수적인 도구로, 개발 시간과 유지 관리 비용을 줄이는 데 도움이 되는 강력하고 유연한 솔루션을 제공하며 웹 사이트 방문자에게 훌륭한 사용자 경험을 제공합니다.

## 응용 Forms 핵심 구성 요소

응용 Forms 코어 구성 요소는 Adobe Experience Manager WCM 코어 구성 요소의 기초가 되는 24개의 오픈 소스 BEM 준수 구성 요소 세트입니다. 특히 사용자의 장치, 브라우저 및 화면 크기에 맞게 조정된 양식인 응용 Forms을 만드는 데 사용하도록 설계되었습니다.

이러한 구성 요소를 사용하여 텍스트 필드, 확인란, 드롭다운 메뉴 등을 비롯한 다양한 양식 필드 옵션을 제공하여 예외적인 데이터 캡처 및 등록 경험을 만들 수 있습니다. 또한 유효성 검사, 조건부 논리 및 반응형 디자인과 같은 기능이 포함되어 있으며 사용자 친화적이고 사용하기 쉬운 양식을 만드는 데 사용할 수 있습니다.

또한 이러한 구성 요소가 오픈 소스이므로 개발자는 조직의 특정 요구 사항에 맞게 구성 요소를 쉽게 사용자 지정하고 확장할 수 있습니다. 또한 이러한 구성 요소는 확장 가능하고 유지 관리할 수 있도록 BEM 방식을 기반으로 구축됩니다.

![](assets/sample-adaptive-form.png)

## 기능 {#features}

|  |  |
|---|---|
| 제작 준비 | 응용 Forms 코어 구성 요소는 24개의 강력한 WCM 구성 요소입니다. |
| 클라우드 기반 | 사용 가능  [AEM Forms as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/home.html). |
| 유연성 | 구성 요소는 Forms 작성자가 거의 모든 레이아웃을 어셈블할 수 있는 일반 개념을 나타냅니다. |
| 구성 가능 | 템플릿 수준 [콘텐츠 정책](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/templates.html?lang=ko-KR#content-policies) 사용할 수 있거나 사용하지 않을 기능을 정의합니다. |
| 액세스 가능 | 그들은 [WCAG 2.1 표준](https://www.w3.org/TR/WCAG21/), ARIA 레이블 제공, 키보드 탐색 지원([알려진 문제](https://github.com/adobe/aem-core-wcm-components/issues?utf8=✓&amp;q=is%3Aissue+is%3Aopen+accessibility+in%3Atitle), 및 텍스트(예: 화면 판독기). |
| 테마 가능 | 구성 요소는 [스타일 시스템](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=ko-KR)을 구현하고 마크업이 [BEM CSS 명명](https://getbem.com/)을 따릅니다 |
| 사용자 정의 가능 | 몇 가지 패턴을 사용하여 HTML 조정부터 고급 기능 재사용까지 간편한 맞춤화를 구현할 수 있습니다. |
| 버전 관리 | [버전 관리 정책](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-policies)을 사용하여 몇 가지 개선 사항을 수정하면 사이트는 핵심 구성 요소에 의해 연결이 끊기지 않습니다. |
| 오픈 소스 | 만약 어떤 것이 필요한 것이 아니라면, 여러분의 개선에 기여하세요. |

## 이점 {#benefits}

데이터 캡처 경험은 리드 생성 및 등록에 매우 중요하며, 적응형 Forms 핵심 구성 요소는 데이터 캡처용으로 최적화된 양식을 만드는 강력한 솔루션을 제공합니다. 기초 구성 요소를 통해 이러한 경험을 만들기 위해 핵심 구성 요소를 사용해야 하는 몇 가지 이유는 다음과 같습니다.

* **GitHub 및 포괄적인 설명서의 가용성**: AEM 적응형 Forms 코어 구성 요소 는 오픈 소스이며 포괄적인 설명서와 함께 GitHub에서 사용할 수 있습니다. 이를 통해 개발자가 구성 요소와 작동 방식을 쉽게 이해하고 개발에 기여할 수 있습니다. 다음 [aemcomponents.dev](https://www.aemcomponents.dev/) 웹 사이트는 개발자가 사용 중인 구성 요소를 확인하고 세부 설명서에 액세스할 수 있는 중요한 리소스입니다.

* **스타일링용 BEM 모델**: 코어 구성 요소는 CSS를 구성하기 위해 잘 설정되어 널리 사용되는 방법론인 BEM(블록 요소 수정자) 모델을 따릅니다. 따라서 개발자가 스타일을 구성하는 방법과 특정 요구에 맞게 수정하는 방법을 쉽게 이해할 수 있습니다.

* **타사 라이브러리에 대한 종속성 없음**: 핵심 구성 요소의 이점 중 하나는 JQuery 및 밑줄을 비롯한 타사 JavaScript 라이브러리에 종속되지 않는다는 것입니다. 이를 통해 구성 요소를 보다 빠르고 간단하게 만들 수 있을 뿐만 아니라 기존 AEM 구현에 쉽게 통합할 수 있습니다.

* **성능 및 접근성에 집중**: 코어 구성 요소는 높은 Google Lighthouse 및 웹 바이탈 점수에 반영되는 성능과 액세서빌러티를 염두에 두고 빌드됩니다. 이를 통해 개발자가 액세스 가능하고 성과가 좋은 웹 페이지를 만들기가 쉬워지므로 오늘날의 디지털 환경에서 이러한 작업이 점점 중요해지고 있습니다.

* **Sites 30 템플릿 및 테마의 양식 구성 요소**: 핵심 구성 요소는 Sites 30 템플릿 및 테마의 양식 구성 요소를 지원하므로 개발자가 AEM 내에서 양식을 쉽게 만들고 사용자 지정할 수 있습니다.

* **스타일을 쉽게 지정**: 코어 구성 요소 는 기초 구성 요소 상대보다 스타일을 지정하는 것이 더 쉽습니다. 테마 만들기 프로세스는 상위 사이트 페이지에서 동일한 테마/CSS를 상속할 수 있는 기능을 사용하여 Sites와 유사합니다. 또한 스타일링용 BEM 모델을 사용하면 스타일을 쉽게 이해하고 수정할 수 있습니다.

* **접근성**: 응용 Forms 핵심 구성 요소는 다음과 같은 액세스 가능성 표준 및 지침을 지원합니다  [WCAG 2.1 표준](https://www.w3.org/TR/WCAG21/)을 호출하여 화면 판독기와 같은 보조 기술을 사용하는 등 장애가 있는 사람이 양식을 사용할 수 있도록 했습니다.

* **AEM Sites과 정렬**: 코어 구성 요소는 AEM Sites과 보다 잘 정렬되도록 설계되었으므로 사이트 사용자가 새로운 기능을 배우지 않고도 핵심 구성 요소를 쉽게 채택하고 사용할 수 있습니다. 컴포넌트는 사이트와 동일한 프런트 엔드 파이프라인을 사용하여 모양새를 보다 쉽게 스타일을 지정하고 수정할 수 있습니다. 또한 다음 점은 이 정렬을 추가로 보여 줍니다.

   * **페이지 편집기를 사용하여 인라인 경험 작성**: 핵심 구성 요소에는 페이지 편집기와 유사한 대화 상자 및 기타 경험과 함께 사이트 편집기로 인라인으로 작성된 작성 경험이 있습니다. 이렇게 하면 Sites 사용자가 Sites 편집기의 친숙한 컨텍스트 내에서 양식을 쉽게 만들고 관리할 수 있습니다.

   * **사이트 편집기에서 인라인 양식 편집**: 코어 구성 요소를 사용하면 편집기 내에서 인라인 양식을 편집할 수 있으므로 편집기 간을 앞뒤로 전환할 필요가 없습니다. 이를 통해 작성 환경을 간소화하고 양식을 보다 쉽게 만들고 관리할 수 있습니다.

   * **Forms의 사이트 기능 상속**: 사이트 페이지에서 작성된 Forms은 사이트와 동일한 기능을 상속합니다. AEM Sites 컨텍스트 내에서 양식을 만들고 관리할 수 있도록 원활하고 통합된 환경을 제공합니다

   <!--including Multi Site Manager, the ability to use Sites components within a form for static content, support for scheduled publish/unpublish, form translation aligned with Sites translation, versioning, and targeting -->



## 요구 사항 {#requirements}

응용 Forms 코어 구성 요소에는 다음 요구 사항이 있습니다.

| AEM | AEM Forms 추가 기능 | 핵심 구성 요소 |
|---|---|---|
| AEM as a Cloud Service | Forms - 디지털 등록 | [릴리스 2.20.8](/help/versions.md)+ |


## 응용 Forms 핵심 구성 요소 {#components}

다음을 사용할 수 있습니다 [적응형 Forms 편집기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html) 응용 Forms을 기반으로 하는 핵심 구성 요소를 만들려면 응용 Forms 핵심 구성 요소의 현재 버전은 아래에 나열된 구성 요소 입니다.

* 아코디언
* 버튼
* 확인란 그룹
* 날짜 선택
* 드롭다운 목록
* 전자 메일 입력
* 양식 컨테이너
* 첨부 파일
* 바닥글
* 헤더
* 가로 탭
* 이미지
* 숫자 입력
* 패널 컨테이너
* 라디오 단추
* 재설정 단추
* 전송 단추
* 전화 입력
* 텍스트 입력
* 텍스트
* 제목
* 마법사


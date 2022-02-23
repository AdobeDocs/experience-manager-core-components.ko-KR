---
title: 소셜 공유 구성 요소
description: 핵심 구성 요소의 소셜 구성 요소는 Facebook 및 Pinterest 공유 위젯입니다.
role: Architect, Developer, Admin, User
exl-id: 8bd53c76-da91-479b-b416-f978682a3d43
source-git-commit: 9767a3a10cb9a77f385edc0ac3fb00096c0087af
workflow-type: ht
source-wordcount: '423'
ht-degree: 100%

---

# 소셜 공유 구성 요소{#social-sharing-component}

핵심 구성 요소의 소셜 구성 요소는 Facebook 및 Pinterest 공유 위젯입니다.

## 사용량 {#usage}

소셜 구성 요소는 Facebook 및 Pinterest 공유 링크를 페이지에 추가합니다. 종종 페이지 머리글이나 바닥글에 포함됩니다.

기타 구성 요소와 다르게 소셜 공유 구성 요소는 [초기 페이지 속성](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html)을 통해 템플릿 작성자에 의해 설정하고, [페이지 속성](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html)을 통해 콘텐츠 작성자에 의해 설정합니다.

## 버전 및 호환성 {#version-and-compatibility}

현재 버전의 소셜 공유 구성 요소는 핵심 구성 요소 릴리스 1.0.0과 함께 도입된 v1입니다. 이 문서에서는 해당 구성 요소에 대해 설명합니다.

다음 표에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | 호환 가능 <br>[2.17.4](/help/versions.md) 및 이전 릴리스 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md)을 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

소셜 공유 구성 요소를 경험하고 구성 옵션의 샘플뿐만 아니라 HTML 및 JSON 출력을 확인하려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_sharing_kr)를 참조하십시오.

### 기술 세부 사항 {#technical-details}

소셜 공유 구성 요소에 대한 최신 기술 설명서는[ GitHub에서 확인할 수 있습니다](https://adobe.com/go/aem_cmp_tech_sharing_v1_kr).

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

## 편집 대화 상자 {#edit-dialog}

![소셜 공유 구성 요소의 편집 대화 상자](/help/assets/sharing-edit.png)

* **ID** - 이 옵션을 통해 HTML과 [데이터 레이어](/help/developing/data-layer/overview.md)에서 구성 요소의 고유 식별자를 제어할 수 있습니다.
   * 비워 두면 고유 ID는 자동으로 생성되고 결과 페이지 검사를 통해 발견될 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID가 변경되면 CSS, JS 및 데이터 레이어 추적에 영향을 미칠 수 있습니다.

공유 시 특수 페이지 머리말이 필요하기 때문에 공유는 페이지 수준에서 활성화되어야 합니다. 따라서, 콘텐츠 작성자는 [초기 페이지 속성](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html)을 통해 공유 구성 요소에 대한 편집 옵션을 추가로 사용할 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

공유 시 특수 페이지 머리말이 필요하기 때문에 공유는 페이지 수준에서 활성화되어야 합니다. 따라서, 템플릿 작성자는 [초기 페이지 속성](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html)을 통해 공유 구성 요소에 대한 디자인 옵션을 사용할 수 있습니다.

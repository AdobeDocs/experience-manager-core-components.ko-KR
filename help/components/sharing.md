---
title: 소셜 공유 구성 요소
description: 핵심 구성 요소 소셜 공유 구성 요소는 Facebook 및 Pinterest 공유 위젯입니다.
translation-type: tm+mt
source-git-commit: 4813748bcfa83ce7c73e81d4e4d445ecc8215d26
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 2%

---


# 소셜 공유 구성 요소{#social-sharing-component}

핵심 구성 요소 소셜 공유 구성 요소는 Facebook 및 Pinterest 공유 위젯입니다.

## 사용량 {#usage}

소셜 공유 구성 요소는 페이지에 Facebook 및 Pinterest 공유 링크를 추가합니다. 페이지 머리글이나 바닥글에 종종 포함됩니다.

다른 구성 요소와 달리 소셜 공유 구성 요소의 설정은 템플릿 작성자가 [초기 페이지 속성](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)을 통해 그리고 [페이지 속성](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html)을 통해 컨텐츠 작성자가 수행합니다.

## 버전 및 호환성 {#version-and-compatibility}

소셜 공유 구성 요소의 현재 버전은 v1이며 핵심 구성 요소의 릴리스 1.0.0에 소개되었으며 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 버전이 호환되는 AEM 버전과 구성 요소의 지원되는 모든 버전을 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

HTML 및 JSON 출력뿐만 아니라 소셜 공유 구성 요소의 구성 옵션 예를 보려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_sharing)를 방문하십시오.

### 기술 세부 정보 {#technical-details}

공유 구성 요소 [에 대한 최신 기술 문서는 GitHub](https://adobe.com/go/aem_cmp_tech_sharing_v1)에서 찾을 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)에서 확인할 수 있습니다.

## 편집 대화 상자 {#edit-dialog}

![구성 요소의 편집 대화 상자 공유](/help/assets/sharing-edit.png)

* **ID**  - 이 옵션을 사용하면 HTML 및 데이터 레이어에서 구성 요소의 고유 식별자를 제어할  [수 있습니다](/help/developing/data-layer/overview.md).
   * 비워 두면 자동으로 고유 ID가 생성되며 결과 페이지를 검사하여 찾을 수 있습니다.
   * ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   * ID를 변경하면 CSS, JS 및 데이터 레이어 추적에 영향을 줄 수 있습니다.

공유에는 특별한 페이지 머리글이 필요하므로 페이지 수준에서 모든 공유가 활성화되어 있어야 합니다. 따라서 컨텐츠 작성자의 경우 공유 탭에 있는 [페이지 속성](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html)을 통해 공유 구성 요소에 대한 추가 편집 옵션을 사용할 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

공유에는 특별한 페이지 머리글이 필요하므로 페이지 수준에서 모든 공유가 활성화되어 있어야 합니다. 따라서 템플릿 작성자의 경우 공유 구성 요소에 대한 디자인 옵션은 [초기 페이지 속성](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)을 통해 사용할 수 있습니다.

---
title: 이메일 핵심 구성 요소 소개
description: 이메일 핵심 구성 요소의 유연성을 사용하여 매력적인 이메일 콘텐츠를 만들고 Adobe Campaign의 강력한 기능으로 전달하십시오.
role: Architect, Developer, Admin, User
exl-id: 0a411f28-bd6a-4bad-b473-6bc27c1d1055
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 97%

---


# 이메일 핵심 구성 요소 소개 {#email-core-components-introduction}

이메일 핵심 구성 요소의 유연성을 사용하여 매력적인 이메일 콘텐츠를 만들고 Adobe Campaign의 강력한 기능으로 전달하십시오.

## 개요 {#overview}

이메일 핵심 구성 요소는 핵심 구성 요소와 동일한 강력한 기반 위에 구축됩니다. 이를 통해 Adobe Campaign의 강력한 기능을 사용하여 이메일 콘텐츠를 간단하고 유연하게 드래그 앤 드롭 방식으로 제작한 후 대상자에게 전달할 수 있습니다.

## 이점 {#benefits}

이메일은 브랜드 경험과 고객 여정의 일부입니다. 이메일 핵심 구성 요소를 사용하면 작성자가 AEM 내에서 이메일 콘텐츠를 제작하여 일관된 브랜드 경험을 제공하고 결과적으로 콘텐츠 속도를 높일 수 있습니다.

* 핵심 구성 요소를 사용하여 페이지를 작성하는 것과 마찬가지로, 이메일 핵심 구성 요소를 사용하면 작성자가 브랜딩 지침을 따르면서 기술적 지식 없이도 이메일을 조합할 수 있습니다.
* 또한 에셋과 콘텐츠를 재사용할 수 있다는 점에서 작성자가 브랜딩 지침을 따르고 콘텐츠 만들기 프로세스를 최적화하도록 유도하는 역할을 합니다.

## 기능 {#features}

* 핵심 이메일 구성 요소는 [핵심 구성 요소](/help/introduction.md)에 기반하며 따라서 [편집 가능한 템플릿](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=ko-KR) 및 [스타일 시스템](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/style-system.html?lang=ko-KR)도 지원합니다.
* 이메일 콘텐츠 작성용으로 [이메일에 최적화되고 제작 준비가 완료된 구성 요소 10개](#components)가 있습니다.
* 핵심 이메일 구성 요소는 대부분의 대화 상자 필드에서의 [Adobe Campaign 변수](campaign-variables.md) 삽입을 통해 고급 개인화 기능을 제공합니다.
* 유연한 [세분화 구성 요소](/help/email/components/segmentation.md) 덕분에 콘텐츠의 고급 세분화가 가능합니다.
* 핵심 이메일 구성 요소는 [CSS 스타일 인라이너,](https://github.com/adobe/aem-core-email-components/wiki/CSS-Styles-Inliner:-Technical-documentation) [HTML 속성 인라이너](https://github.com/adobe/aem-core-email-components/wiki/HTML-Inliner) 및 [HTML 삭제기](https://github.com/adobe/aem-core-email-components/wiki/HTML-Sanitizing)를 통해 이메일에 최적화된 HTML 출력을 제공합니다.
* `/content` 아래 어디에나 이메일 콘텐츠를 만들 수 있습니다.
* 이메일 핵심 구성 요소는 [오픈 소스](https://github.com/adobe/aem-core-email-components)입니다.

## 요구 사항 {#requirements}

이메일 핵심 구성 요소에는 다음과 같은 요구 사항이 있습니다.

| AEM | Adobe Campaign | 핵심 구성 요소 |
|---|---|---|
| AEM 6.5.14.0+ 또는 AEM 6.5 LTS GA<br>온프레미스 또는 AMS | Adobe Campaign Classic<br>Adobe Campaign Standard | [릴리스 2.21.2](/help/versions.md)+ |

>[!NOTE]
>
>Adobe Campaign 통합이 AEM as a Cloud Service에서 지원되지 않으므로 이메일 핵심 구성 요소도 AEM as a Cloud Service에서 지원되지 않습니다.

## 이메일 구성 요소 {#components}

이메일 핵심 구성 요소의 현재 버전은 다음 구성 요소 기능이 있습니다.

* [페이지](components/page.md)
* [컨테이너](components/container.md)
* [제목](components/title.md)
* [텍스트](components/text.md)
* [이미지](components/image.md)
* [버튼](components/button.md)
* [티저](components/teaser.md)
* [경험 조각](components/experience-fragment.md)
* [콘텐츠 조각](components/content-fragment.md)
* [세분화](components/segmentation.md)

## 설치 및 사용 {#installation-usage}

이메일 핵심 구성 요소 설치에 대한 자세한 내용은 [이메일 핵심 구성 요소 사용](using.md) 문서를 참조하십시오.

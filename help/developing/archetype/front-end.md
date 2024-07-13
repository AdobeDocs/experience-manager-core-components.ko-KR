---
title: AEM Project Archetype을 사용한 프론트엔드 개발
description: AEM Project Archetype의 Webpack 기반 전용 프론트엔드 빌드 메커니즘(선택 사항)에 대해 알아봅니다.
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 99132b49-bd06-4ac2-9348-12c0dfdfe8b2
source-git-commit: bd92a5d1884056ca7b44ea28e5817d8bde10a4d9
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 100%

---


# AEM Project Archetype을 사용한 프론트엔드 개발 {#front-end}

AEM Project Archetype에는 Webpack 기반의 전용 프론트엔드 빌드 메커니즘(선택 사항)이 포함됩니다. 이에 ui.frontend 모듈은 JavaScript 및 CSS가 포함된 모든 프로젝트 프론트엔드 리소스의 중앙 위치가 됩니다. 이 유용하고 유연한 기능을 최대한 활용하려면 프론트엔드 개발이 AEM 프로젝트에 얼마나 적합한지 이해하는 것이 중요합니다.

이 문서에서는 프론트엔드 빌드 모듈의 일반적인 사용 패턴과 그 역할에 중점을 둡니다. 자세한 빌드 옵션 및 기술 지침은 해당 Archetype의 GitHub 저장소에 있는 설명서를 참조하십시오.

>[!TIP]
>
>최신 AEM Project Archetype 및 관련 기술 문서는 [GitHub에서 찾을 수 있습니다.](https://github.com/adobe/aem-project-archetype)

## AEM 프론트엔드 및 백엔드 개발 {#front-end-back-end}

간단히 정리하면 AEM 프로젝트는 별도로 구성된 2개의 부분이 서로 관련된 것으로 생각할 수 있습니다.

* AEM 논리를 유도하고 Java 라이브러리, OSGi 서비스 등을 생성하는 백엔드 개발
* 결과 웹 프레젠테이션 및 비헤이비어를 유도하고 JavaScript 및 CSS 라이브러리를 생성하는 프론트엔드 개발

이 두 가지 개발 프로세스가 프로젝트의 서로 다른 부분에 중점을 두기 때문에 백엔드 및 프론트엔드 개발이 동시에 발생할 수 있습니다.

![프론트엔드 워크플로 다이어그램](/help/assets/front-end-flow.png)

결과적으로 모든 프로젝트는 이들 두 가지 개발 역량(예: 백엔드 및 프론트엔드)의 출력을 사용해야 합니다.

## 마크업 확인 {#determining-markup}

프로젝트에 어떤 프론트엔드 개발 워크플로를 구현하든지 백엔드 개발자와 프론트엔드 개발자는 먼저 마크업에 동의해야 합니다. 일반적으로 AEM은 핵심 구성 요소에서 제공하는 마크업을 정의합니다. [단, 필요한 경우 이를 사용자 정의할 수 있습니다.](/help/developing/customizing.md#customizing-the-markup)

## 가능한 프론트엔드 개발 워크플로 {#possible-workflows}

프론트엔드 빌드 모듈은 유용하고 매우 유연한 도구이지만 사용 방법에 대해서는 특별한 의견을 제시하지 않습니다. 다음은 사용량에 대한 2가지 *가능한* 사례이지만 개별 프로젝트는 다른 사용 모델을 보여 줄 수 있습니다.

### Webpack 정적 개발 서버 사용 {#using-webpack}

ui.frontend 모듈 내 AEM 웹 페이지의 정적 출력 기반으로 Webpack을 사용하여 스타일링하고 개발할 수 있습니다.

1. 페이지 미리보기 모드를 사용하거나 URL로 `wcmmode=disabled`를 전달하면서 AEM의 페이지 미리보기
1. 페이지 소스를 보고 ui.frontend 모듈 내 정적 HTML로 저장합니다.
1. [Webpack 시작](#webpack-dev-server) 후 필수 JavaScript와 CSS 스타일링 및 생성을 시작합니다.
1. `npm run dev`를 실행하여 clientlib를 생성합니다.

이 흐름에서 AEM 개발자는 단계 1, 2를 수행하고, 정적 HTML을 AEM HTML 출력에 따라 개발한 프론트엔드 개발자에게 전달할 수 있습니다.

>[!TIP]
>
>페이지 수준이 아닌 구성 요소 수준에서 작업할 수 있도록 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_kr)를 활용하여 각 구성 요소의 마크업 출력 샘플을 캡처할 수 있습니다.

### 스토리북 사용 {#using-storybook}

[스토리북](https://storybook.js.org)을 사용하여 보다 작은 단위의 프론트엔드 개발을 수행할 수 있습니다. 스토리북이 AEM Project Archetype에 포함되지 않지만 ui.frontend 모듈에 설치하여 스토리북 아티팩트를 저장할 수 있습니다. AEM에서 테스트할 준비가 되면 `npm run dev`를 실행하여 clientlib로 배포할 수 있습니다.

>[!NOTE]
>
>[스토리북](https://storybook.js.org)은 AEM Project Archetype에 포함되지 않습니다. 스토리북 사용을 선택한 경우 별도로 설치해야 합니다.

## Clientlib 개요 {#clientlibs}

[AEM clientlib로 프론트엔드 모듈을 사용할 수 있습니다.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html). NPM 빌드 스크립트가 실행되면 앱이 빌드되고, `aem-clientlib-generator` 패키지가 결과 빌드 출력을 요청하면 clientlib로 변환됩니다.

clientlib는 다음 파일과 디렉터리로 구성됩니다.

* `css/`: HTML로 요청될 수 있는 CSS 파일
* `css.txt`: 파일이 병합될 수 있도록 AEM에 지시하고 `css/` 파일 이름을 알려 줍니다.
* `js/`: HTML로 요청될 수 있는 JavaScript 파일
* `js.txt` 파일이 병합될 수 있도록 AEM에 지시하고 `js/` 파일 이름을 알려 줍니다.
* `resources/`: 소스 맵, 비-진입점 코드 청크(코드 분할이 원인), 정적 자산(예: 아이콘) 등

>[!TIP]
>
>AEM이 [AEM 개발 설명서](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html)에서 clientlib를 처리하는 방법과 이를 [핵심 구성 요소 설명서](/help/developing/including-clientlibs.md)에 포함하는 방법에 대해 자세히 알아보십시오.

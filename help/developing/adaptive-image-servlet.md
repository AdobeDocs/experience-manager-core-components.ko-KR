---
title: 적응형 이미지 서블릿
description: 핵심 구성 요소가 이미지 제공을 위해 적응형 이미지 서블릿을 사용하는 방법과 해당 사용을 최적화하는 방법에 대해 알아봅니다.
role: Architect, Developer, Admin, User
exl-id: d9199d51-6f09-4000-9525-afc30474437e
source-git-commit: 420e6085da57e5dc6deb670a5f0498b018441cb8
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 61%

---

# 적응형 이미지 서블릿 {#adaptive-image-servlet}

핵심 구성 요소가 이미지 제공을 위해 적응형 이미지 서블릿을 사용하는 방법과 해당 사용을 최적화하는 방법에 대해 알아봅니다.

## 적응형 이미지 서블릿 또는 웹에 최적화된 이미지 제공 {#options}

이미지 핵심 구성 요소는 두 가지 방법을 사용하여 이미지를 제공할 수 있습니다.

* 적응형 이미지 서블릿이 기본값입니다.
* [웹에 최적화된 이미지 제공](/help/developing/web-optimized-image-delivery.md)은 AEMaaCS에서 사용할 수 있으며, 다운로드 크기를 평균적으로 25% 줄일 수 있습니다.

이 문서에서는 기본 적응형 이미지 서블릿에 대해 설명합니다.

## 개요 {#overview}

기본적으로 이미지 구성 요소는 핵심 구성 요소의 적응형 이미지 서블릿을 사용하여 이미지를 제공합니다. [적응형 이미지 서블릿](https://github.com/adobe/aem-core-wcm-components/wiki/The-Adaptive-Image-Servlet)은 이미지를 처리 및 스트리밍하고, 개발자에 의해 [핵심 구성 요소 맞춤화](/help/developing/customizing.md)에 활용될 수 있습니다.

## 표현물 선택 {#rendition-selection}

응용 이미지 서블릿은 표시되는 컨테이너의 크기에 따라 표시할 가장 적합한 변환을 자동으로 선택합니다. 변환 선택 프로세스는 다음과 같습니다.

1. 응용 이미지 서블릿은 이미지 자산의 사용 가능한 모든 변환에서 검토합니다.
1. 참조된 자산의 동일한 mime/유형을 갖는 자산만 선택합니다.
   * 예: 원래 자산이 PNG인 경우 PNG 변환만 고려합니다.
1. 그러한 표현물 중에서 차원을 고려하고 이미지를 표시해야 하는 컨테이너의 크기와 비교합니다.
   1. 표현물이 컨테이너 크기보다 큰 경우 후보 표현물 목록에 추가됩니다.
   1. 표현물이 컨테이너 크기 미만이면 무시됩니다.
   1. 이러한 기준은 표현물의 배율을 상향 조정하지 않으므로 이미지 품질에 영향을 줍니다.
1. 그런 다음 응용 이미지 서블릿이 후보 목록에서 가장 작은 파일 크기로 변환을 선택합니다.

## 렌디션 선택 최적화 {#optimizing-rendition-selection}

적응형 이미지 서블릿은 요청된 이미지 크기 및 유형에 가장 적합한 렌디션을 선택합니다. DAM 렌디션 및 이미지 구성 요소 허용 폭은 적응형 이미지 서블릿이 가능한 한 적게 처리할 수 있도록 동기식으로 정의하는 것이 좋습니다.

이렇게 하면 성능이 향상되고 기본 이미지 처리 라이브러리에서 일부 이미지가 올바르게 처리되지 않는 문제를 방지할 수 있습니다.

## 마지막으로 수정한 헤더 사용 {#last-modified}

적응형 이미지 서블릿은 `Last-Modified` 헤더를 통해 조건부 요청을 지원하지만 `Last-Modified` 헤더[의 캐싱은 발송자](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html?lang=ko#caching-http-response-headers)에서 활성화해야 합니다.

[AEM Project Archetype](/help/developing/archetype/overview.md)의 샘플 발송자 구성에는 이미 이 구성이 포함됩니다.

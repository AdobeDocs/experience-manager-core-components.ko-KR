---
title: 적응형 이미지 서블릿
description: 핵심 구성 요소가 이미지 제공을 위해 적응형 이미지 서블릿을 사용하는 방법과 해당 사용을 최적화하는 방법에 대해 알아봅니다.
role: Architect, Developer, Admin, User
exl-id: d9199d51-6f09-4000-9525-afc30474437e
source-git-commit: 785aa82930e3bcf6ef16d7a1cdc614d230e8daa8
workflow-type: ht
source-wordcount: '410'
ht-degree: 100%

---

# 적응형 이미지 서블릿 {#adaptive-image-servlet}

핵심 구성 요소가 이미지 제공을 위해 적응형 이미지 서블릿을 사용하는 방법과 해당 사용을 최적화하는 방법에 대해 알아봅니다.

## 적응형 이미지 서블릿 또는 웹에 최적화된 이미지 게재 {#options}

이미지 핵심 구성 요소는 두 가지 방법을 사용하여 이미지를 게재할 수 있습니다.

* 적응형 이미지 서블릿이 기본값입니다.
* [웹에 최적화된 이미지 제공](/help/developing/web-optimized-image-delivery.md)은 AEMaaCS에서 사용할 수 있으며, 다운로드 크기를 평균적으로 25% 줄일 수 있습니다.

이 문서에서는 기본 적응형 이미지 서블릿에 대해 설명합니다.

## 개요 {#overview}

기본적으로 이미지 구성 요소는 핵심 구성 요소의 적응형 이미지 서블릿을 사용하여 이미지를 제공합니다. [적응형 이미지 서블릿](https://github.com/adobe/aem-core-wcm-components/wiki/The-Adaptive-Image-Servlet)은 이미지를 처리 및 스트리밍하고, 개발자에 의해 [핵심 구성 요소 맞춤화](/help/developing/customizing.md)에 활용될 수 있습니다.

## 렌디션 선택 {#rendition-selection}

적응형 이미지 서블릿은 표시되는 컨테이너의 크기에 따라 표시할 가장 적절한 렌디션을 자동으로 선택합니다. 렌디션 선택 프로세스는 다음과 같습니다.

1. 적응형 이미지 서블릿이 이미지 자산에 대해 사용 가능한 모든 렌디션을 검토합니다.
1. 원래 참조된 자산에 대해 MIME/유형이 동일한 자산만 선택합니다.
   * 예를 들어 원래 자산이 PNG 라면 PNG 렌디션만 고려하게 됩니다.
1. 이들 렌디션 중 차원을 고려하여 이미지가 표시될 컨테이너의 크기와 비교합니다.
   1. 렌디션이 컨테이너 크기 이상이면 후보 렌디션 목록에 추가됩니다.
   1. 렌디션이 컨테이너 크기 미만이면 무시됩니다.
   1. 이러한 기준은 이미지 품질에 영향을 미칠 수 있는 렌디션의 크기가 초과되지 않도록 보장합니다.
1. 적응형 이미지 서블릿은 이후 후보 목록에서 가장 작은 파일 크기를 갖는 렌디션을 선택합니다.

## 렌디션 선택 최적화 {#optimizing-rendition-selection}

적응형 이미지 서블릿은 요청된 이미지 크기 및 유형에 가장 적합한 렌디션을 선택합니다. DAM 렌디션 및 이미지 구성 요소 허용 폭은 적응형 이미지 서블릿이 가능한 한 적게 처리할 수 있도록 동기식으로 정의하는 것이 좋습니다.

이렇게 하면 성능이 향상되고 기본 이미지 처리 라이브러리에서 일부 이미지가 올바르게 처리되지 않는 문제를 방지할 수 있습니다.

## 마지막으로 수정된 헤더 사용 {#last-modified}

적응형 이미지 서블릿은 `Last-Modified` 헤더를 통해 조건부 요청을 지원하지만 `Last-Modified` 헤더의 캐싱은[ 발송자에서 활성화](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html?lang=ko#caching-http-response-headers)해야 합니다.

[AEM Project Archetype](/help/developing/archetype/overview.md)의 샘플 발송자 구성에는 이미 이 구성이 포함됩니다.

---
title: 웹에 최적화된 이미지 게재
description: 핵심 구성 요소가 AEM as a Cloud Service의 웹에 최적화된 이미지 게재 옵션을 활용하여 이미지를 보다 효율적으로 전달하는 방법에 대해 알아봅니다.
role: Architect, Developer, Admin, User
exl-id: 6080ab8b-f53c-4d5e-812e-16889da4d7de
source-git-commit: eb1822cb41a849695afb5125745ed5f78e3e70a4
workflow-type: tm+mt
source-wordcount: '1061'
ht-degree: 100%

---

# 웹에 최적화된 이미지 게재 {#web-optimized-image-delivery}

핵심 구성 요소가 AEM as a Cloud Service의 웹에 최적화된 이미지 게재 옵션을 활용하여 이미지를 보다 효율적으로 전달하는 방법에 대해 알아봅니다.

## 개요 {#overview}

AEM as a Cloud Service의 웹에 최적화된 이미지 게재 옵션은 DAM의 이미지 자산을 [WebP 형식으로 전달합니다.](https://developers.google.com/speed/webp) WebP는 이미지의 다운로드 크기를 평균적으로 25% 줄일 수 있어 페이지 로드 속도가 빨라집니다.

핵심 구성 요소에서 웹에 최적화된 이미지 게재 옵션을 간단하게 활성화할 수 있으며 모든 일반 브라우저에서 WebP가 지원되므로, 경험은 최종 사용자에게 투명하게 제공됩니다. 유일한 차이점은 콘텐츠가 더욱 빠르게 로드된다는 점입니다.

## 핵심 구성 요소에 대해 웹에 최적화된 이미지 게재 활성화 {#activating}

웹에 최적화된 이미지 게재 옵션을 활성화하려면 페이지 템플릿을 편집한 다음 [이미지 구성 요소의 디자인 대화 상자 내에 있는 **웹에 최적화된 이미지 활성화** 옵션을 활성화하면 됩니다.](/help/components/image.md#design-dialog) 이 옵션은 이미지 구성 요소의 v1, v2 및 v3에 사용할 수 있습니다.

디자인 대화 상자 및 AEM 페이지 템플릿에 익숙하지 않은 경우 [이 문서를 검토하십시오.](/help/get-started/authoring.md#pre-configuring-core-components)

![디자인 대화 상자에서 웹에 최적화된 이미지 게재 활성화](/help/assets/web-optimized-image-delivery.png)

이번 단계가 끝났습니다! 이제 이미지가 이미지 구성 요소에 의해 WebP 형식으로 전달됩니다.

웹에 최적화된 이미지 게재 옵션을 활성화하면 Dispatcher 구성을 확인하여 이미지 게재 서비스에 대한 요청을 차단하지 않는지 확인할 수 있습니다. 자세한 내용은 [이 FAQ 항목](#failure-to-deliver)을 참조하십시오.

## WebP 게재 확인 {#verifying}

웹에 최적화된 이미지 게재는 콘텐츠 소비자에게 투명합니다. 최종 사용자가 알 수 있는 유일한 것은 더 빨라진 로드 시간입니다. 따라서 실제 동작 변화를 관찰하려면 브라우저에서 렌더링된 이미지의 콘텐츠 유형을 확인해야 합니다. 모든 최신 브라우저는 WebP를 지원합니다. 브라우저 지원에 대한 자세한 내용은 [이 사이트](https://caniuse.com/webp)를 참조하십시오.

1. AEM에서 이미지 구성 요소에 대해 [웹에 최적화된 이미지 게재 옵션을 활성화](#activating)한 템플릿에 따라 작성된 페이지를 편집합니다.
1. 페이지 편집기에서 왼쪽 상단의 **페이지 정보** 버튼을 선택한 다음 **게시됨으로 보기**&#x200B;를 선택합니다.
1. 브라우저의 개발자 도구를 열고 네트워크 탭을 선택합니다.
1. 페이지를 다시 로드하고 이미지를 로드하는 HTTP 요청을 찾아 브라우저가 수신한 이미지의 콘텐츠 유형을 확인합니다.

## 웹에 최적화된 이미지 게재 옵션을 사용할 수 없는 경우 {#fallback}

웹에 최적화된 이미지 게재는 AEM as a Cloud Service에서만 사용할 수 있습니다. AEM 6.5를 온프레미스 또는 로컬 개발 인스턴스에서 실행하는 경우와 같이 이 기능을 사용할 수 없는 경우 이미지 게재는 [적응형 이미지 서블릿 사용](/help/developing/adaptive-image-servlet.md)으로 돌아갑니다.

적응형 이미지 서블릿으로 돌아가면 페이지 소스에 있는 `img` 요소의 `src` 속성이 변경됩니다.

## 자주 묻는 질문 {#faq}

### 내 환경에서 웹에 최적화된 이미지를 활성화하는 옵션이 없는 이유는 무엇입니까? {#missing-option}

이 기능은 AEM as a Cloud Service에서만 사용할 수 있습니다. AEM에서 로컬로 실행하거나 온프레미스에서 실행하는 경우 이미지 구성 요소는 적응형 이미지 서블릿 사용으로 [돌아갑니다](#fallback).

### 서비스가 로컬 SDK에서 작동하지 않는 이유는 무엇입니까? {#local-sdk}

`localhost`에서 AEM SDK를 사용하는 경우 이미지 서비스를 사용할 수 없으며 이미지 렌더링은 적응형 이미지 서블릿 사용으로 [돌아갑니다](#fallback).

웹에 최적화된 이미지 게재 서비스를 사용하려면 프로젝트를 AEMaaCS 개발 환경에 배포하여 이미지 서비스가 어떻게 작동하는지 정확하게 테스트할 수 있습니다.

### 내 페이지의 일부 이미지에 대해 서비스가 작동하지 않는 이유는 무엇입니까? {#some-images}

이미지 서비스는 `/content/dam`에 위치한 자산에 대해서만 작동하며 페이지에 바로 업로드되어 `cq:Page` 프로젝트에 저장된 이미지에 대해서는 작동하지 않습니다. 이러한 자산은 여전히 [대체](#fallback) 적응형 이미지 서블릿을 통해 전달됩니다.

### 이 서비스가 더 낮은 품질의 이미지를 표시하거나 이미지 크기를 제한하는 이유는 무엇입니까? {#quality}

`/content/dam` 아래의 이미지 자산이 처리되면 AEM as a Cloud Service 환경에서 다양한 차원의 최적화된 표현을 생성됩니다. 웹에 최적화된 이미지 서비스는 이미지 핵심 구성 요소에서 요청한 폭을 분석하고 원본 이미지와 2048px 이하의 모든 렌디션을 고려하여 그 중에서 가장 큰 이미지(이미지 서비스가 처리할 수 있는 크기 및 치수 제한 내, 현재 50MB 및 `12k`x`12k`)를 요청된 설정(폭, 자르기, 포맷, 품질 등)을 적용할 베이스로 선택합니다.

출력의 충실도를 유지하기 위해 이미지 서비스는 이미지를 확대하지 않습니다. 앞서 언급된 렌디션은 이미지 서비스가 전달할 수 있는 최상의 품질을 정의합니다. 원본 이미지 자산의 크기 및/또는 치수에 영향을 줄 수 없는 경우가 많으므로 이미지 자산이 모두 2048px 확대/축소 렌디션인지 확인하고, 그렇지 않은 경우 다시 처리하십시오.

### 내 이미지의 URL은 .WEBP가 아닌 .JPG 또는 .PNG로 종료되며 SRCSET 속성이나 PICTURE 요소가 없습니다. 이것이 정말로 최적화된 웹 형식을 사용하고 있습니까? {#content-negotiation}

WebP 포맷을 제공하기 위해 웹에 최적화된 이미지 게재 서비스는 [서버 기반 콘텐츠 협상이라는 기술을 수행합니다.](https://developer.mozilla.org/en-US/docs/Web/HTTP/Content_negotiation#server-driven_content_negotiation) 이를 통해 클라이언트가 공지한 기능을 기반으로 이미지에 대한 최적의 출력 포맷을 선택하는 데 도움이 되며, 이미지 게재 서비스가 파일 확장자를 무시할 수 있습니다.

콘텐츠 협상 활용의 장점은 WebP 지원을 공지하지 않는 브라우저에서도 페이지 마크업에 필요한 변경 없이 JPG 또는 PNG 파일 포맷을 가져올 수 있다는 것입니다. 이를 통해 기존 사이트에 대한 최적의 호환성을 제공하고 가장 원활하게 웹에 최적화된 이미지 게재로 전환할 수 있습니다.

### 내 구성 요소와 함께 웹에 최적화된 이미지 게재 옵션을 사용할 수 있습니까?

예, 웹에 최적화된 이미지 게재 서비스는 [이미지 구성 요소를 확장](/help/developing/customizing.md)하여 구축된 사용자 정의 구성 요소에서 사용할 수 있습니다.

다음은 자산 URL을 생성하는 데 사용할 수 있는 서비스 인터페이스입니다.

```
com.adobe.cq.wcm.spi.AssetDelivery.getDeliveryURL(Resource resource, Map<String, Object> parameterMap)
```

>[!WARNING]
>
>앞서 언급한 SPI(AEM as a Cloud Service Sites에서 사용 가능)를 통해 빌드되지 않은 경험에 직접 URL을 임베드하는 것은 [미디어 라이브러리 이용 약관](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/admin/medialibrary.html?lang=ko#use-media-library)을 위반하는 것입니다.

### 웹에 최적화된 이미지를 활성화한 후 이미지가 표시되지 않을 수 있습니까? {#failure-to-deliver}

아니요. 다음과 같은 이유로 이러한 경우는 발생할 수 없습니다.

* HTML에서 웹에 최적화된 이미지를 활성화할 때 마크업은 변경되지 않고 이미지 요소의 `src` 속성 값만 변경됩니다.
* 새 이미지 서비스를 사용할 수 없거나 원하는 이미지를 처리할 수 없을 때마다, 생성된 URL은 [적응형 이미지 서블릿으로 돌아갑니다](#fallback).

그러나 Dispatcher 규칙에 따라 웹에 최적화된 이미지 게재 서비스가 차단될 수 있습니다. 이미지 게재 서비스의 URL은 `/adobe`로 시작하며, [여기에 설명된](https://experienceleague.adobe.com/docs/experience-manager-learn/ams/dispatcher/common-logs.html?lang=ko#filter-rejects) 것처럼 거부된 요청에 대한 Dispatcher 로그를 검사하면 브라우저에 이미지를 게재할 때 발생하는 오류를 해결하는 데 도움이 됩니다.

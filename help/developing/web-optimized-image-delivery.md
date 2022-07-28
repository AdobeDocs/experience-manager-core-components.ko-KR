---
title: 웹에 최적화된 이미지 제공
description: 핵심 구성 요소가 AEM as a Cloud Service의 웹에 최적화된 이미지 전달 기능을 활용하여 이미지를 보다 효율적으로 전달하는 방법을 알아봅니다.
role: Architect, Developer, Admin, User
exl-id: 6080ab8b-f53c-4d5e-812e-16889da4d7de
source-git-commit: a134c2593593efef4df7b01e3a870e03e9860640
workflow-type: tm+mt
source-wordcount: '1169'
ht-degree: 0%

---

# 웹에 최적화된 이미지 제공 {#web-optimized-image-delivery}

핵심 구성 요소가 AEM as a Cloud Service의 웹에 최적화된 이미지 전달 기능을 활용하여 이미지를 보다 효율적으로 전달하는 방법을 알아봅니다.

>[!NOTE]
>
>웹에 최적화된 이미지 제공 서비스는 2022년 6월 GA가 예정된 AEM as a Cloud Service 릴리스의 사전 릴리스 기능입니다.
>
>AEMaaCS의 사전 릴리스 기능에 대한 자세한 내용은 문서를 참조하십시오 [Adobe Experience Manager as a Cloud Service 사전 릴리스 채널](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html)

## 개요 {#overview}

AEM as a Cloud Service의 웹에 최적화된 이미지 전달 기능은 의 DAM에서 이미지 자산을 전달합니다 [WebP 형식입니다.](https://developers.google.com/speed/webp) WebP는 이미지의 다운로드 크기를 평균적으로 25% 줄일 수 있어 페이지 로드 속도가 빨라집니다.

핵심 구성 요소에서 웹에 최적화된 이미지 전달을 활성화하는 것은 간단하며, 모든 일반적인 브라우저는 WebP를 지원하기 때문에 경험은 최종 사용자에게 투명합니다. 컨텐츠가 더 빨리 로드된다는 점만 다를 수 있습니다.

## 핵심 구성 요소에 대해 웹에 최적화된 이미지 전달 활성화 {#activating}

웹에 최적화된 이미지 전달을 활성화하려면 페이지 템플릿을 편집하고 옵션을 활성화하면 됩니다 **웹 최적화 이미지 활성화** 의 디자인 대화 상자 내에서 [이미지 구성 요소.](/help/components/image.md#design-dialog) 이 옵션은 이미지 구성 요소의 v1, v2 및 v3에 사용할 수 있습니다.

디자인 대화 상자 및 AEM 페이지 템플릿을 잘 모를 경우 [이 문서를 검토하십시오.](/help/get-started/authoring.md#pre-configuring-core-components)

![디자인 대화 상자에서 웹에 최적화된 이미지 전달 활성화](/help/assets/web-optimized-image-delivery.png)

이번 단계가 끝났습니다! 이제 이미지가 이미지 구성 요소에 의해 WebP 형식으로 전달됩니다.

웹에 최적화된 이미지 전달 기능을 활성화하면 Dispatcher 구성을 확인하여 이미지 서비스에 대한 요청을 차단하지 않는지 확인할 수도 있습니다. 이 서비스의 URL은 다음 형식을 사용합니다.

```text
/adobe/dynamicmedia/deliver/dm-aid--741ed388-d5f8-4797-8095-10c896dc9f1d/skitouring.jpg?quality=80&preferwebp=true
```

이는 이 정규 표현식으로 일반화할 수 있습니다.

```text
\/adobe\/dynamicmedia\/deliver\/([^:[]|*\/])\/([\w-])\.(gif|png|png8|jpg|pjpg|bjpg|webp|webpll|webply)(?[a-z0-9=&]*)?
```

## WebP 배달 확인 {#verifying}

웹에 최적화된 이미지 전달은 컨텐츠 소비자에게 투명하며 마크업에 영향을 주지 않습니다. 최종 사용자가 알 수 있는 유일한 것은 로드 시간이 더 빠릅니다.

따라서 실제 동작 변경을 관찰하려면 페이지 소스를 확인해야 합니다.

1. AEM에서 사용자가 있는 템플릿을 기반으로 하는 페이지를 편집합니다 [활성화된 웹 최적화 이미지 제공](#activating) 이미지 구성 요소에 사용할 수 있습니다.
1. 페이지 편집기 내에서 **페이지 정보** 왼쪽 상단의 단추를 누른 다음 **게시됨으로 보기**.
1. 브라우저 개발자 도구를 사용하여 페이지의 소스를 보고 렌더링된 마크업이 어떻게 동일하게 유지되는지와 이미지에 있는 이미지를 확인합니다 `src` 특성 지점 [새 이미지 서비스의 URL입니다.](#activating)

## 웹에 최적화된 이미지 전달을 사용할 수 없는 경우 {#fallback}

웹에 최적화된 이미지 전달은 AEM as a Cloud Service에서만 사용할 수 있습니다. AEM 6.5를 온-프레미스 또는 로컬 개발 인스턴스에서 실행하는 것과 같이 사용할 수 없는 경우 이미지 배달이 사용 중으로 폴백됩니다 [응용 이미지 서블릿.](/help/developing/adaptive-image-servlet.md)

웹에 최적화된 이미지 전달을 활성화해도 마크업에 영향을 주지 않는 것처럼 응용 이미지 서블릿으로 폴백해도 마크업에 영향을 주지 않습니다 `src` 의 속성 `img` 요소가 변경되었습니다.

## FAQ {#faq}

### 내 환경에서 웹에 최적화된 이미지를 활성화하는 이러한 옵션이 없는 이유는 무엇입니까? {#missing-option}

이 기능은 AEM as a Cloud Service에서만 사용할 수 있습니다. 이미지 구성 요소인 로컬 또는 온-프레미스에서 AEM 실행 [폴백](#fallback) 응용 이미지 서블릿을 사용하려면 다음을 수행하십시오.

### 서비스가 로컬 SDK에서 작동하지 않는 이유는 무엇입니까? {#local-sdk}

에서 AEM SDK를 사용할 때 `localhost`, 이미지 서비스를 사용할 수 없으며 이미지 렌더링 [폴백](#fallback) 응용 이미지 서블릿을 사용하려면 다음을 수행하십시오.

웹에 최적화된 이미지 제공 서비스를 사용하려면 프로젝트를 AEMaaCS 개발 환경에 배포하여 이미지 서비스에서 이미지 서비스가 어떻게 동작하는지 정확하게 테스트할 수 있습니다.

### 내 페이지의 일부 이미지에 대해 서비스가 작동하지 않는 이유는 무엇입니까? {#some-images}

이미지 서비스는 아래에 있는 자산에만 작동합니다 `/content/dam` 그리고 페이지에 직접 업로드되고 다음에 저장된 이미지에는 작동하지 않습니다 `cq:Page` 개체. 이러한 자산은 여전히 응용 이미지 서블릿과 함께 [대체.](#fallback)

### 이 서비스가 더 나쁜 이미지 또는 이미지 크기를 제한하는 이유는 무엇입니까? {#quality}

웹에 최적화된 이미지 서비스는 2048px 이하 버전인 모든 이미지 렌디션을 고려하며 요청된 설정(너비, 자르기, 형식, 품질 등)을 적용할 기준으로 가장 큰 이미지 렌디션을 선택합니다.

이미지 서비스는 고급 이미지를 제공하지 않습니다. 따라서 이러한 변환은 이미지 서비스가 전달할 수 있는 최상의 크기와 품질을 정의합니다. 따라서 모든 자산에 2048px 확대/축소 표현물이 있는지 확인하고, 그렇지 않은 경우 재처리합니다.

### 내 이미지의 URL은 .WEBP가 아닌 .JPG 또는 .PNG로 종료되며 SRCSET 속성이나 PICTURE 요소가 없습니다. 이렇게 하면 실제로 최적화된 웹 형식을 사용하고 있습니까? {#content-negotiation}

WebP 형식을 제공하기 위해 웹 최적화 이미지 제공 서비스는 &quot;컨텐츠 협상&quot;이라는 기술을 사용합니다. 이 작업은 JPG 또는 PNG 파일 확장명을 요청하는 경우에도 WebP 파일 형식을 반환하면서 수행되지만, 브라우저에서 요청을 제공하는 경우에만 수행됩니다 `image/webp` HTTP 수락 헤더입니다. 이 기술을 지원하는 브라우저는 이 헤더를 제공할 수 있으며 이전 브라우저는 여전히 JPG 또는 PNG 파일 형식을 가져옵니다.

이 기법의 장점은 `img` 요소와 속성이 동일하게 유지될 수 있으므로 기존 사이트에 대한 최적의 호환성을 확보하고 웹 최적화 이미지 전달로 원활하게 전환할 수 있습니다.

### 자체 구성 요소와 함께 웹에 최적화된 이미지 전달을 사용할 수 있습니까?

예. 웹에 최적화된 이미지 제공 서비스는 사용자 지정 구성 요소에서 사용할 수 있습니다. Adobe 권장 사항 [이미지 구성 요소 확장](/help/developing/customizing.md) 이 경우

다음은 자산 URL을 생성하는 데 사용할 수 있는 서비스 인터페이스입니다.

```
com.adobe.cq.wcm.spi.AssetDelivery.getDeliveryURL(Resource resource, Map<String, Object> parameterMap)
```

이 서비스는 자산 리소스를 필수 첫 번째 매개 변수로 사용하며, 다음 매개 변수를 포함할 수 있는 적용할 원하는 이미지 변환의 선택적 맵을 가져올 수 있습니다.

* `path` - 배달할 자산 ID는 패턴이어야 합니다 `([^:\[\]\|\*\/]+)` (예: `unicorn–1234`)
* `seoname` - 이미지 URL에 추가할 사용자 정의 SEO 중심 이름으로, 하이픈은 포함할 수 있으며 패턴이어야 합니다 `([\w-]+)` (예: `my-friend-the-unicorn`)
* `format` - 원하는 이미지 형식을 사용할 수 있습니다. `gif`, `png`, `png8`, `jpg`, `pjpg`, `bjpg`, `webp`, `webpll`, `webply` (예: `webp`)
* `preferwebp` - 가능하면 WebP 출력을 전달하여 `format` 매개 변수([콘텐츠 협상에 대한 FAQ 를 참조하십시오](#content-negotiation)), 부울(예: `true`)
* `width` - 원하는 이미지 해상도(픽셀 단위)는 1보다 커야 합니다(예: `400`)
* `quality` - 다음 사이 원하는 압축 `1` 및 `100` (예: `75`)
* `c` - 원하는 이미지 자르기 좌표, 쉼표로 구분된 픽셀 값(예: `100,100,400,200`)
* `r` - 원하는 이미지 회전을 수행할 수 있습니다. `90`, `180`, `270` (예: `90`)
* `flip` - 원하는 이미지 뒤집기는 `h`, `v`, `hv` (예: `h`)

### 새 이미지 서비스에서 제공하는 이미지의 URL은 무엇입니까? {#url}

이전 섹션을 참조하십시오 [핵심 구성 요소에 대해 웹에 최적화된 이미지 전달 활성화](#activating) 예 URL 및 정규 표현식입니다.

### 웹에 최적화된 이미지를 활성화한 후 이미지가 표시되지 않을 수 있습니까?

이런 일은 절대 안 돼

* HTML에서 마크업은 웹 최적화 이미지를 활성화할 때 변경되지 않고 이미지 요소의 SRC 속성 값만 변경됩니다.
* 새 이미지 서비스를 사용할 수 없거나 원하는 이미지를 처리할 수 없을 때마다 생성된 URL은 [응용 이미지 서블릿에 대한 폴백입니다.](#fallback)
* Dispatcher 규칙은 웹에 최적화된 이미지 서비스를 차단할 수 있습니다. [피쳐를 활성화할 때 선택해야 합니다.](#activating)

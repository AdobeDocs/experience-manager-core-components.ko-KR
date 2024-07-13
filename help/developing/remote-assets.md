---
title: 원격 자산 지원
description: OpenAPI가 포함된 Dynamic Media를 사용하여 원격 자산을 지원하도록 핵심 구성 요소 이미지 및 티저 구성 요소를 구성하는 방법에 대해 알아봅니다.
role: Architect, Developer, Admin, User
exl-id: b462c1f3-a6c8-4a2a-abf4-d08ec82d4371
source-git-commit: 36ef19d5b29fe21f86309719d1e3f6588e31a93b
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 100%

---


# 원격 자산 지원 {#remote-assets-support}

OpenAPI가 포함된 Dynamic Media를 사용하여 원격 자산을 지원하도록 핵심 구성 요소 이미지 및 티저 구성 요소를 구성하는 방법에 대해 알아봅니다.

>[!NOTE]
>
>OpenAPI가 포함된 Dynamic Media는 이전에 차세대 Dynamic Media로 알려졌습니다. 기능과 사용법은 동일합니다.

## 최신 AEM 버전 다운로드 {#latest}

OpenAPI가 포함된 Dynamic Media를 사용하여 원격 자산을 지원하려면 다음과 같은 사항이 필요합니다.

* AEM 6.5 SP 18+ 또는 AEM as a Cloud Service
* 코어 구성 요소 릴리스 2.23.2 이상

## HTTPS 구성 {#https}

일반적으로 HTTP를 사용하여 모든 프로덕션 AEM 인스턴스를 실행하는 것이 좋습니다. 단, 로컬 개발 환경은 이와 같이 설정되지 않을 수 있습니다. 그러나 OpenAPI가 포함된 Dynamic Media를 사용하는 원격 자산이 작동하려면 HTTPS가 필요합니다.

개발 환경을 포함하여 원격 자산을 사용하려는 곳에서 [이 안내서를 사용](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/security/use-the-ssl-wizard.html)하여 HTTPS를 구성하십시오.

## OSGi 구성 {#osgi}

원격 자산의 위치는 OSGi 구성에서 정의되어야 합니다. 다음과 같이 **차세대 Dynamic Media 구성** OSGi 구성을 구성하고 해당 값을 원격 자산 환경의 값으로 대체합니다.

```text
imsClient="<ims-client-name>"
enabled=B"true"
imsOrg="<ims-org>@AdobeOrg"
repositoryId="<repo-id>.adobeaemcloud.com"
```

![차세대 Dynamic Media 구성 OSGi 구성 창](/help/assets/remote-assets-osgi.png)

OSGi 구성 방법에 대한 자세한 내용은 다음 문서를 참조하십시오.

* AEM as a Cloud Service용 [Adobe Experience Manager as a Cloud Service에 대한 OSGi 구성](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi.html)
* AEM 6.5용 [OSGi 구성](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/configuring/configuring-osgi.html)

## 구성 확인 {#verify}

이제 OpenAPI가 포함된 Dynamic Media를 사용하는 원격 자산 기능이 작동하는지 확인할 수 있습니다. 이를 위해 WKND 샘플 사이트 및 코어 구성 요소를 설치할 수 있습니다.

* [코어 구성 요소](https://github.com/adobe/aem-core-wcm-components/releases/download/core.wcm.components.reactor-2.23.2/core.wcm.components.all-2.23.2.zip) 릴리스 2.23.2 이상이 필요합니다.
* [WKND 샘플 사이트](https://github.com/adobe/aem-guides-wknd/releases/download/aem-guides-wknd-3.2.0/aem-guides-wknd.all-3.2.0-classic.zip) 릴리스 3.2.0 이상이 필요합니다.

핵심 구성 요소 및 WKND 사이트가 설치되면 모든 WKND 페이지에서 기능을 테스트할 수 있습니다.

1. HTTPS를 사용하여 AEM 인스턴스에 액세스합니다.

1. `https://<host>:<httpsPort>/editor.html/content/wknd/language-masters/en/magazine/arctic-surfing.html`과 같은 페이지 편집기에서 WKND 데모 페이지를 엽니다.

1. 페이지에 이미지 구성 요소를 추가합니다.

1. 구성 요소의 구성 대화 상자에서 **자산** 탭의 **페이지에서 추천 이미지 상속** 옵션을 선택 해제하고 **선택**&#x200B;을 클릭합니다.

1. 구성이 올바른 경우 **로컬** 및 **원격** 옵션이 포함된 드롭다운이 표시됩니다. **원격**&#x200B;을 선택합니다.

   ![이미지 선택을 위한 원격 및 로컬 선택 옵션](/help/assets/remote-asset-selection.png)

1. 대화 상자가 열리고 원격 서비스에 인증해야 합니다.

1. 인증되면 원격 서비스의 자산 브라우저가 열립니다. 원하는 자산을 선택한 다음 **선택**&#x200B;을 클릭합니다.

   ![원격 자산 선택](/help/assets/remote-asset-picker.png)

원격 자산이 로컬 AEM 페이지에 추가되고 기능이 올바르게 구성되었는지 확인했습니다.

## 원격 자산 사용 {#using}

구성한 다음 [이미지 구성 요소](/help/components/image.md) 및 [티저 구성 요소](/help/components/teaser.md)와 같은 코어 구성 요소를 사용하여 자산을 선택할 수 있는 원격 자산을 선택할 수 있습니다.

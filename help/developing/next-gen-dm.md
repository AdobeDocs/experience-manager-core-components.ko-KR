---
title: 차세대 Dynamic Media 지원
description: 원격 차세대 Dynamic Media 에셋을 지원하도록 핵심 구성 요소 이미지 및 티저 구성 요소를 구성하는 방법을 알아봅니다.
role: Architect, Developer, Admin, User
source-git-commit: 57307b75bd33fd538a1eb704cc37822847c896de
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 1%

---


# 차세대 Dynamic Media 지원 {#next-gen-dm-support}

원격 차세대 Dynamic Media 에셋을 지원하도록 핵심 구성 요소 이미지 및 티저 구성 요소를 구성하는 방법을 알아봅니다.

## 최신 AEM 버전 가져오기 {#latest}

차세대 Dynamic Media 원격 자산을 지원하려면 다음이 필요합니다.

* AEM AEM 6.5 SP 18+ 또는 as a Cloud Service
* 코어 구성 요소 릴리스 2.23.2 이상

## HTTPS 구성 {#https}

일반적으로 HTTP를 사용하여 모든 프로덕션 AEM 인스턴스를 실행하는 것이 좋습니다. 단, 로컬 개발 환경이 이와 같이 설정되지 않을 수 있습니다. 그러나 차세대 Dynamic Media 원격 자산이 작동하려면 HTTPS가 필요합니다.

[이 안내서 사용](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/security/use-the-ssl-wizard.html) 개발 환경을 포함하여 원격 자산을 사용하려는 곳이라면 어디에서든 HTTPS를 구성하십시오.

## OSGi 구성 {#osgi}

원격 자산의 위치를 OSGi 구성에서 정의해야 합니다. 구성 **차세대 Dynamic Media 구성** 값을 원격 자산 환경의 값으로 대체하여 다음과 같이 OSGi 구성을 수행합니다.

```text
imsClient="<ims-client-name>"
enabled=B"true"
imsOrg="<ims-org>@AdobeOrg"
repositoryId="<repo-id>.adobeaemcloud.com"
```

![차세대 Dynamic Media 구성 OSGi 구성 창](/help/assets/remote-assets-osgi.png)

OSGi 구성 방법에 대한 자세한 내용은 다음 문서를 참조하십시오.

* [Adobe Experience Manager as a Cloud Service에 대한 OSGi 구성](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi.html) AEM as a Cloud Service
* [OSGi 구성](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/configuring/configuring-osgi.html) AEM 6.5용

## 구성 확인 {#verify}

이제 차세대 Dynamic Media 원격 자산 기능이 작동하는지 확인할 수 있습니다. 이를 위해 WKND 샘플 사이트 및 핵심 구성 요소를 설치할 수 있습니다.

* [핵심 구성 요소](https://github.com/adobe/aem-core-wcm-components/releases/download/core.wcm.components.reactor-2.23.2/core.wcm.components.all-2.23.2.zip) 릴리스 2.23.2 이상이 필요합니다.
* [WKND 샘플 사이트](https://github.com/adobe/aem-guides-wknd/releases/download/aem-guides-wknd-3.2.0/aem-guides-wknd.all-3.2.0-classic.zip) 릴리스 3.2.0 이상이 필요합니다.

핵심 구성 요소 및 WKND 사이트가 설치되면 모든 WKND 페이지에서 기능을 테스트할 수 있습니다.

1. HTTPS를 사용하여 AEM 인스턴스에 액세스합니다.

1. 다음과 같은 페이지 편집기에서 WKND 데모 페이지를 엽니다. `https://<host>:<httpsPort>/editor.html/content/wknd/language-masters/en/magazine/arctic-surfing.html`

1. 페이지에 이미지 구성 요소를 추가합니다.

1. 구성 요소의 구성 대화 상자에서 옵션을 선택 취소합니다 **페이지에서 추천 이미지 상속** 다음에 있음 **자산** tab 키를 누른 다음 클릭 **선택**.

1. 구성이 올바른 경우 옵션이 포함된 드롭다운이 나타납니다 **로컬** 및 **원격**. 선택 **원격**.

   ![이미지 선택을 위한 원격 및 로컬 선택 옵션](/help/assets/remote-asset-selection.png)

1. 대화 상자가 열리면 원격 서비스를 인증해야 합니다.

1. 인증되면 원격 서비스의 자산 브라우저가 열립니다. 원하는 에셋을 선택하고 을 탭하거나 클릭합니다 **선택**.

   ![원격 자산 선택](/help/assets/remote-asset-selection.png)

원격 자산이 로컬 AEM 페이지에 추가되고 기능이 올바르게 구성되었는지 확인했습니다.

## 원격 자산 사용 {#using}

구성하고 나면 과 같은 핵심 구성 요소를 사용하여 자산을 선택할 원격 자산을 선택할 수 있습니다. [이미지 구성 요소](/help/components/image.md) 및 [티저 구성 요소.](/help/components/teaser.md)

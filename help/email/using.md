---
title: 이메일 핵심 구성 요소 사용
description: 이메일 핵심 구성 요소의 기본 설치, 구성 및 사용에 대해 알아봅니다.
role: Architect, Developer, Admin, User
exl-id: 0e79ca8f-eb0a-4519-b1e8-a9d3b0b99987
index: false
source-git-commit: eb77567dc32cccb81a9fc131493d11fb55b7e93b
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 100%

---


# 이메일 핵심 구성 요소 사용 {#using}

이메일 핵심 구성 요소의 기본 설치, 구성 및 사용에 대해 알아봅니다.

## 이메일 핵심 구성 요소 설치 {#installation}

이메일 핵심 구성 요소는 AEM 6.5와 함께 사용할 수 있습니다. 자세한 내용은 [이메일 핵심 구성 요소 소개 문서의 요구 사항 섹션](introduction.md#requirements)을 참조하십시오.

### 핵심 구성 요소 설치 {#core-components}

이메일 핵심 구성 요소는 AEM 핵심 구성 요소를 기반으로 합니다. 핵심 구성 요소는 AEM 6.5와 함께 제공되지 않으므로 이메일 핵심 구성 요소를 설치하기 전에 먼저 AEM 핵심 구성 요소를 설치해야 합니다.

핵심 구성 요소 설치 방법에 대한 자세한 내용은 핵심 구성 요소 사용 문서의 [다운로드 및 설치](/help/get-started/using.md#download-and-install) 섹션을 참조하십시오.

### 이메일 핵심 구성 요소 설치 {#email-core-components}

핵심 구성 요소를 인스턴스에 설치한 후 이메일 핵심 구성 요소도 마찬가지로 설치해야 합니다. 이메일 핵심 구성 요소는 아직 AEM Project Archetype의 일부가 아니므로 프로젝트에 수동으로 추가해야 합니다. [이메일 핵심 구성 요소 GitHub 위키](https://github.com/adobe/aem-core-email-components/wiki/Adding-to-Existing-Project)의 설명서에 따라 설치하십시오.

이메일 핵심 구성 요소를 사용하도록 기존 프로젝트를 조정하려는 경우 동일한 지침을 따를 수 있습니다.

## 구성 {#configuration}

핵심 구성 요소를 설치한 후 두 가지 중요한 구성 단계를 완료해야 합니다.

### Campaign 구성 {#configure-campaign}

두 솔루션이 통신하려면 AEM-Adobe Campaign 통합을 설정해야 합니다.

* Adobe Campaign 통합 구성
   * Adobe Campaign Classic: [Adobe Campaign Classic과 통합](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignonpremise.html?lang=ko)
   * Adobe Campaign Standard: [Adobe Campaign Standard와 통합](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignstandard.html?lang=ko)
* 이메일 핵심 구성 요소를 사용할 콘텐츠 페이지에 [Adobe Campaign 통합 구성 연결](/help/email/components/page.md#cloud-services-tab)

### 이메일 구성 요소에 대한 AEM 리소스 유형 필터 추가 {#aem-resource-filter}

Adobe Campaign에서 이메일 핵심 구성 요소를 기반으로 이메일을 렌더링할 수 있으려면 Campaign에서 필터를 조정해야 합니다.

1. 클라이언트 콘솔을 사용해 관리자 자격으로 Adobe Campaign에 로그인합니다.

1. 메뉴 표시줄에서 **도구** -> **탐색기**&#x200B;를 선택합니다.

1. 탐색기에서 **관리** -> **플랫폼** -> **옵션** 노드로 이동합니다.

1. 목록에서 `AEMResourceTypeFilter` 옵션을 선택합니다.

1. **값** 필드에서 `core/email/components/page/<v1>/page`를 추가합니다(아직 없는 경우).

   * `<v1>`을 이메일 핵심 구성 요소 [페이지 구성 요소](/help/email/components/page.md)의 현재 버전(예: `v1`)으로 바꿉니다.
   * **값** 필드의 값은 쉼표로 구분해야 합니다.

1. **저장**&#x200B;을 클릭합니다.

## 이메일 핵심 구성 요소 사용 {#using-components}

이메일 구성 요소를 설치하고 Adobe Campaign과의 통합을 구성했으면 이메일 구성 요소를 사용해 AEM에서 이메일 콘텐츠를 만든 다음 Adobe Campaign을 사용하여 해당 콘텐츠를 수신자에게 전송할 수 있습니다. 다음은 워크플로의 개요입니다.

| 단계 | 설명 | 솔루션 |
|---|---|---|
| 1 | 작성자가 폴더 및 이메일 콘텐츠의 자유 형식 계층 구조를 페이지로 만듭니다. | AEM |
| 2 | 작성자가 [템플릿 편집기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=ko-KR)를 사용해 이 페이지 템플릿으로 만드는 모든 이메일 페이지에서 공유할 이메일 머리글 및/또는 바닥글을 구성합니다. | AEM |
| 3 | 작성자가 [페이지 편집기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/editing-content.html?lang=ko)를 사용해 텍스트 편집기를 사용하는 이메일 콘텐츠를 만듭니다. 이때 Adobe Campaign 변수를 선택하고 세분화 구성 요소를 사용해 수신자가 특정 기준을 충족할 경우 조건부로 정보가 표시되도록 할 수 있습니다. | AEM |
| 4 | 이메일 콘텐츠를 완성했으면 [워크플로를 실행](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/workflows/overview.html?lang=ko)하여 콘텐츠를 승인하고 Campaign으로 전송합니다. | AEM |
| 5 | 수신자 목록을 정의하는 전달이 만들어집니다. | 캠페인 |
| 6 | AEM에서 만든 콘텐츠가 전달의 콘텐츠로 선택됩니다. | 캠페인 |
| 7 | Adobe Campaign 변수를 수신자의 개인화된 정보로 대체하여 콘텐츠가 수신자에게 전송됩니다. | 캠페인 |

AEM에서 이메일 콘텐츠를 만들고 Adobe Campaign에서 전달하는 예는 다음 리소스를 참조하십시오.

* AEM 6.5: [Adobe Campaign Classic 및 Adobe Campaign Standard 작업](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/aem-adobe-campaign/campaign.html?lang=ko)

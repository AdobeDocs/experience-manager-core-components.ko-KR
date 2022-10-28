---
title: 이메일 핵심 구성 요소 사용
description: 이메일 핵심 구성 요소의 기본 설치, 구성 및 사용에 대해 알아봅니다.
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 6%

---


# 이메일 핵심 구성 요소 사용 {#using}

이메일 핵심 구성 요소의 기본 설치, 구성 및 사용에 대해 알아봅니다.

## 이메일 핵심 구성 요소 설치 {#installation}

이메일 핵심 구성 요소는 AEM 6.5에서 사용할 수 있습니다. 자세한 내용은 [이메일 핵심 구성 요소 소개 문서의 요구 사항 섹션](introduction.md#requirements) 추가 정보.

### 핵심 구성 요소 설치 {#core-components}

이메일 코어 구성 요소 는 AEM 코어 구성 요소를 기반으로 구축됩니다. 핵심 구성 요소는 AEM과 함께 제공되지 않으므로 이메일 핵심 구성 요소를 설치하기 전에 먼저 AEM 핵심 구성 요소를 설치해야 합니다.

섹션을 참조하십시오 [다운로드 및 설치](/help/get-started/using.md#download-and-install) 핵심 구성 요소 설치 방법에 대한 자세한 내용은 핵심 구성 요소 사용 문서의 섹션을 참조하십시오.

### 이메일 핵심 구성 요소 설치 {#email-core-components}

핵심 구성 요소가 인스턴스에 설치되면 이메일 코어 구성 요소 도 마찬가지로 설치해야 합니다. 이메일 코어 구성 요소 는 아직 AEM Project Archetype의 일부가 아니므로 프로젝트에 수동으로 추가해야 합니다. 의 설명서를 따르십시오 [전자 메일 핵심 구성 요소 GitHub Wiki를 설치](https://github.com/adobe/aem-core-email-components/wiki/Adding-to-Existing-Project)

이메일 코어 구성 요소를 사용하도록 기존 프로젝트를 조정하려는 경우 다음과 동일한 지침을 따를 수 있습니다.

## 구성 {#configuration}

핵심 구성 요소를 설치한 후 두 가지 중요한 구성 단계를 완료해야 합니다.

### Campaign 구성 {#configure-campaign}

두 솔루션이 통신하려면 AEM-Adobe Campaign 통합을 설정해야 합니다.

* Adobe Campaign 통합 구성
   * Adobe Campaign Classic: [Adobe Campaign Classic과 통합](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignonpremise.html)
   * Adobe Campaign Standard: [Adobe Campaign Standard과 통합](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignstandard.html)
* [Adobe Campaign 통합 구성 연결](/help/email/components/page.md#cloud-services-tab) 이메일 핵심 구성 요소를 사용할 컨텐츠 페이지로 이동합니다.

### 이메일 구성 요소에 대한 AEM 리소스 유형 필터 추가 {#aem-resource-filter}

Adobe Campaign이 이메일 핵심 구성 요소를 기반으로 이메일을 렌더링하려면 Campaign에서 필터를 조정해야 합니다.

1. 클라이언트 콘솔을 사용해 관리자 자격으로 Adobe Campaign에 로그인합니다.

1. 메뉴 표시줄에서 **도구** -> **탐색기**&#x200B;를 선택합니다.

1. 탐색기에서 **관리** -> **플랫폼** -> **옵션** 노드 아래에 있어야 합니다.

1. 을(를) 선택합니다 `AEMResourceTypeFilter` 옵션을 선택합니다.

1. 에서 **값** 필드, 추가 `core/email/components/page/<v1>/page` 아직 없는 경우

   * 바꾸기 `<v1>` 이메일 핵심 구성 요소의 현재 버전 사용 [페이지 구성 요소](/help/email/components/page.md) 예 `v1`.
   * 의 값은 **값** 필드는 쉼표로 구분해야 합니다.

1. **저장**&#x200B;을 클릭합니다.

## 이메일 핵심 구성 요소 사용 {#using-components}

이메일 구성 요소가 설치되고 Adobe Campaign와의 통합이 구성되면 이메일 구성 요소 를 사용하여 AEM에서 이메일 컨텐츠를 만든 다음 Adobe Campaign을 사용하여 수신자에게 해당 컨텐츠를 보낼 수 있습니다. 다음은 워크플로우에 대한 개요입니다.

| 단계 | 설명 | 솔루션 |
|---|---|---|
| 1 | 작성자는 폴더 및 이메일 컨텐츠의 자유 형식 계층 구조를 페이지로 만듭니다. | AEM |
| 2 | 사용 [템플릿 편집기,](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=ko-KR) 작성자는 이 페이지 템플릿으로 인한 모든 이메일 페이지 간에 공유할 이메일 머리글 및/또는 바닥글을 구성합니다. | AEM |
| 3 | 작성자는 [페이지 편집기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/editing-content.html) 수신자가 Adobe Campaign 변수를 선택하고 세그먼테이션 구성 요소를 사용하여 수신자가 특정 기준을 충족하는 경우 조건부 정보를 표시할 수 있는 텍스트 편집기를 사용하여 전자 메일 콘텐츠를 만들려면, | AEM |
| 4 | 전자 메일 콘텐츠가 완료되면, [워크플로우가 실행됩니다](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/workflows/overview.html) 컨텐츠를 승인하고 Campaign으로 보내기 위해 | AEM |
| 5 | 수신자 목록을 정의하는 게재를 만듭니다. | 캠페인 |
| 6 | AEM에서 만든 컨텐츠가 게재 컨텐츠로 선택됩니다. | 캠페인 |
| 7 | 컨텐츠가 수신자에게 전송되고 Adobe Campaign 변수가 수신자의 개인화된 정보로 바뀝니다. | 캠페인 |

AEM에서 전자 메일 콘텐츠를 만들고 Adobe Campaign에서 전달하는 예제는 다음 리소스를 참조하십시오.

* AEM as a Cloud Service: [AEM으로 Campaign 뉴스레터 만들기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/campaign/creating-newsletters.html)
* AEM 6.5: [Adobe Campaign Classic 및 Adobe Campaign Standard 작업](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/aem-adobe-campaign/campaign.html)


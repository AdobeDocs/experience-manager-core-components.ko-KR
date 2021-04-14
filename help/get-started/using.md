---
title: 핵심 구성 요소 사용
description: '"프로젝트에서 핵심 구성 요소를 바로 실행하려면 다음 3단계를 수행하십시오.템플릿에 구성 요소를 다운로드하여 설치하고, 프록시 구성 요소를 만들고, 핵심 스타일을 로드하고, 구성 요소를 허용합니다."'
role: Architect, Developer, Administrator, Business Practitioner
exl-id: ee2d25e4-e2b8-4ecc-a62c-f0066de2bf2d
translation-type: tm+mt
source-git-commit: 45a17fe42146516f351f897e85a4a48dcf3aadab
workflow-type: tm+mt
source-wordcount: '977'
ht-degree: 2%

---

# 핵심 구성 요소 사용{#using-core-components}

프로젝트에서 핵심 구성 요소를 바로 실행하려면 아래 섹션에 개별적으로 설명된 4개의 단계가 있습니다.

1. [다운로드 및 설치](#download-and-install)
1. [프록시 구성 요소 만들기](#create-proxy-components)
1. [핵심 스타일 불러오기](#load-the-core-styles)
1. [구성 요소 활성화](#allow-the-components)

>[!TIP]
>
>프로젝트 설정, 핵심 구성 요소, 편집 가능한 템플릿, 클라이언트 라이브러리 및 구성 요소 개발을 처음부터 시작하는 방법에 대한 자세한 지침을 보려면 다음 다중 부분 자습서가 유용할 수 있습니다.\
>[AEM Sites 시작하기 - WKND 튜토리얼](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)

>[!TIP]
>
>[AEM 프로젝트 원형 유형을 사용하는 경우, ](/help/developing/archetype/overview.md) 핵심 구성 요소는 Adobe의 우수 사례 권장 사항을 기반으로 프로젝트에 자동으로 포함됩니다.

## {#download-and-install} 다운로드 및 설치

핵심 구성 요소 뒤에 있는 주요 아이디어 중 하나는 유연성입니다. 새로운 버전의 핵심 구성 요소를 출시하면 Adobe이 새로운 기능을 보다 유연하게 제공할 수 있습니다. 따라서 개발자는 프로젝트에 통합하려는 구성 요소와 프로젝트 업데이트 빈도를 유연하게 지정할 수 있습니다. 따라서 AEM 및 핵심 구성 요소 모두에 대해 별도의 릴리스 프로세스가 이루어집니다.

따라서 AEM을 클라우드 서비스로 실행하든 온프레미스에서 실행하든 여부에 따라 설치 단계가 결정됩니다.

### AEM as a Cloud Service {#aemaacs}

일단은 없어! AEM은 자동으로 최신 버전의 핵심 구성 요소와 함께 제공됩니다. AEMaaCS에서 AEM의 최신 기능을 제공하듯이 AEMaaCS도 자동으로 최신 버전의 핵심 구성 요소를 최신 버전으로 유지합니다.

AEMACS에서 핵심 구성 요소를 사용할 때 주의해야 할 몇 가지 사항입니다.

* 핵심 구성 요소는 `/libs`에 포함됩니다.
* 프로젝트 빌드 파이프라인이 다시 `/apps`의 일부로 핵심 구성 요소를 포함하는 경우 로그에 경고가 생성되며 프로젝트의 일부로 포함된 버전은 무시됩니다.
   * 코어 구성 요소를 포함한 다음 릴리스에서는 파이프라인 빌드가 다시 실패합니다.
* 프로젝트에 이전에 `/apps`에 핵심 구성 요소가 포함되어 있는 경우 [프로젝트를 조정할 수 있습니다.](/help/developing/overview.md#via-aemaacs)
* 핵심 구성 요소가 현재 `/libs`에 있지만 `/apps`에서 동일한 경로의 오버레이를 만드는 것은 권장되지 않습니다. [구성 요소의 ](/help/developing/guidelines.md#proxy-component-pattern) 측면을 사용자 정의해야 하는 경우 대신 프록시 구성 요소 패턴을 사용해야 합니다.

### AEM 6.5 및 이전 {#aem-65}

핵심 구성 요소는 프로덕션 모드에서 시작할 때 빠른 시작(샘플 컨텐츠 없음)에 포함되지 않습니다. 따라서 첫 번째 단계는 [GitHub](https://github.com/adobe/aem-core-wcm-components/releases/latest)에서 최신 릴리스된 컨텐츠 패키지를 다운로드하고 AEM 환경에 설치하는 것입니다.

이를 자동화하는 방법에는 여러 가지가 있지만, 인스턴스에 컨텐츠 패키지를 신속하게 설치하는 가장 간단한 방법은 패키지 관리자를 사용하는 것입니다.[패키지 설치](https://docs.adobe.com/content/help/en/experience-manager-65/administering/contentmanagement/package-manager.html#installing-packages)를 참조하십시오. 또한 게시 인스턴스가 실행 중이면 해당 패키지를 게시자에게 복제해야 합니다.[패키지 복제](https://docs.adobe.com/content/help/en/experience-manager-65/administering/contentmanagement/package-manager.html#replicating-packages)를 참조하십시오.

## 프록시 구성 요소 만들기 {#create-proxy-components}

[프록시 구성 요소 패턴](/help/developing/guidelines.md#proxy-component-pattern) 섹션에 설명된 이유로 핵심 구성 요소를 컨텐츠에서 직접 참조해서는 안 됩니다. 이를 방지하기 위해 모든 구성 요소는 숨겨진 구성 요소 그룹( `.core-wcm` 또는 `.core-wcm-form`)에 속하므로 편집기에 직접 표시되지 않습니다.

대신 사이트 특정 구성 요소를 만들어 페이지 작성자에게 표시할 원하는 구성 요소 이름 및 그룹을 정의하고 각 구성 요소를 상위 유형으로 [핵심 구성 요소]를 참조해야 합니다. 이러한 사이트 특정 구성 요소는 아무 것도 포함할 필요가 없고 주로 사이트에 사용할 구성 요소의 버전을 정의하기 위해 제공되므로 &quot;프록시 구성 요소&quot;라고도 합니다. 그러나 [핵심 구성 요소](/help/developing/customizing.md)를 사용자 정의할 때 이러한 프록시 구성 요소는 마크업 및 논리 사용자 지정에 중요한 역할을 합니다.

따라서 사이트에 사용되기를 원하는 각 핵심 구성 요소에 대해 다음을 수행해야 합니다.

1. 사이트의 구성 요소 폴더에 해당 프록시 구성 요소를 만듭니다.

   **예**
에서  `/apps/my-site/components` 유형의 제목 노드 만들기  `cq:Component`

1. 슈퍼 유형이 있는 해당 코어 구성 요소 버전을 가리킵니다.

   **예**
다음 속성을 추가합니다.\
   `sling:resourceSuperType="core/wcm/components/title/v1/title"`

1. 구성 요소의 그룹, 제목 및 선택적으로 설명을 정의합니다. 이러한 값은 프로젝트별로 다르며 구성 요소가 작성자에게 표시되는 방식을 나타냅니다.

   **예**
다음 속성을 추가합니다.

   ```shell
   componentGroup="My Site"
   jcr:title="Title"  
   jcr:description="Section Heading"
   ```

예를 들어 WKND 사이트](https://github.com/adobe/aem-guides-wknd/blob/master/ui.apps/src/main/content/jcr_root/apps/wknd/components/title/.content.xml)의 [제목 구성 요소를 보십시오. 이 구성 요소는 이러한 방식으로 만들어지는 프록시 구성 요소의 좋은 예입니다.

## 코어 스타일 {#load-the-core-styles} 불러오기

1. 아직 수행하지 않으면 사이트에 필요한 모든 CSS 및 JS 파일을 포함하는 [클라이언트 라이브러리](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html)를 만듭니다.
1. 사이트의 클라이언트 라이브러리에서 필요한 핵심 구성 요소에 종속성을 추가합니다. 이 작업은 `embed` 속성을 추가하여 수행합니다.

   예를 들어 모든 v1 핵심 구성 요소의 클라이언트 라이브러리를 포함하려면 추가할 속성은 다음과 같습니다.

   ```shell
   embed="[  
   core.wcm.components.image.v1,  
   core.wcm.components.list.v1,  
   core.wcm.components.breadcrumb.v1,  
   core.wcm.components.form.container.v1,  
   core.wcm.components.form.text.v1  
   ]"
   ```

다음 섹션으로 이동하기 전에 프록시 구성 요소 및 클라이언트 라이브러리가 AEM 환경에 배포되었는지 확인합니다.

## 구성 요소 {#allow-the-components} 허용

다음 단계는 [템플릿 편집기](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)에서 수행됩니다.

1. 템플릿 편집기에서 레이아웃 컨테이너를 선택하고 정책을 엽니다.
1. 허용된 구성 요소 목록에서 이전에 만든 프록시 구성 요소를 선택합니다. 이 구성 요소는 할당된 구성 요소 그룹 아래에 표시됩니다. 완료되면 변경 사항을 적용합니다.
1. 선택적으로, 디자인 대화 상자가 있는 구성 요소에 대해 사전 구성할 수 있습니다.

바로 그거야! 편집된 템플릿에서 만든 페이지에서 새로 만든 구성 요소를 사용할 수 있어야 합니다.

**다음 참조:**

* [핵심 구성 요소 사용자](/help/developing/customizing.md)  지정 - 핵심 구성 요소의 스타일을 지정하고 사용자 지정하는 방법을 알아봅니다.
* [구성 요소 지침](/help/developing/guidelines.md)  - 핵심 구성 요소의 구현 패턴을 학습합니다.

---
title: 핵심 구성 요소 사용
description: “나만의 프로젝트에서 핵심 구성 요소를 시작하고 실행하려면 프록시 구성 요소 다운로드 및 설치 그리고 제작, 핵심 스타일 로드 및 템플릿에서 구성 요소 사용 등 3가지 단계를 따르십시오.”
role: Architect, Developer, Admin, User
exl-id: ee2d25e4-e2b8-4ecc-a62c-f0066de2bf2d
source-git-commit: 8beae61676340e8aafaee469018d865ea7ed934e
workflow-type: tm+mt
source-wordcount: '1008'
ht-degree: 96%

---

# 핵심 구성 요소 사용{#using-core-components}

“자체 프로젝트에서 핵심 구성 요소를 시작하고 실행하려면 아래 섹션에 자세히 설명된 4가지 단계를 따르십시오.”

1. [다운로드 및 설치](#download-and-install)
1. [프록시 구성 요소 제작](#create-proxy-components)
1. [핵심 스타일 로드하기](#load-the-core-styles)
1. [구성 요소 활성화하기](#allow-the-components)

>[!TIP]
>
>프로젝트 설정, 핵심 구성 요소, 편집 가능한 템플릿, 클라이언트 라이브러리 및 구성 요소 개발 등을 최초 시작하는 방법에 대한 자세한 지침은 다음 멀티 파트 튜토리얼을 참조하십시오.\
>[AEM Sites 시작하기 - WKND 튜토리얼](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html?lang=ko-KR)

>[!TIP]
>
>[AEM Project Archetype](/help/developing/archetype/overview.md)을 사용하는 경우 핵심 구성 요소는 Adobe의 모범 사례 및 권장 사항에 따라 프로젝트에 자동으로 포함됩니다.

## 다운로드 및 설치 {#download-and-install}

핵심 구성 요소를 주도하는 아이디어는 유연성입니다. 새 버전의 핵심 구성 요소가 자주 출시되는 경우 Adobe는 보다 유연하게 새로운 기능을 제공할 수 있습니다. 결과적으로 개발자는 보다 유연하게 프로젝트로의 통합과 프로젝트의 업데이트 빈도를 선택할 수 있습니다. 그 결과 AEM과 핵심 구성 요소를 위한 릴리스 프로세스가 서로 분리됩니다.

따라서 AEM as a Cloud Service 또는 온프레미스의 실행 여부에 따라 설치 단계가 결정됩니다.

### AEM as a Cloud Service {#aemaacs}

1단계는 없습니다. AEM as a Cloud Service에는 최신 버전의 핵심 구성 요소가 자동으로 제공됩니다. AEMaaCS가 AEM의 최신 기능을 제공하는 것과 마찬가지로 AEMaaCS는 자동으로 최신 버전의 핵심 구성 요소를 최신 상태로 유지합니다.

AEMaaCS에서 핵심 구성 요소 사용 시 유의해야 할 몇 가지 사항.

* `/libs`에는 핵심 구성 요소가 포함됩니다.
* 프로젝트 빌드 파이프라인에 핵심 구성 요소가 `/apps`의 일부로 포함되고 프로젝트의 일부로 임베디드 버전이 무시되는 경우 로그에 경고 메지지가 발생합니다.
   * 향후 릴리스에서 핵심 구성 요소가 포함되면 파이프라인 빌드에 오류가 발생합니다.
* 이전에 `/apps`의 핵심 구성 요소가 프로젝트에 포함되면 [프로젝트를 조정할 수 있습니다.](/help/developing/overview.md#via-aemaacs)
* 핵심 구성 요소가 `/libs`에 있어도 `/apps`에서 동일한 경로의 오버레이를 만들지 않는 것이 좋습니다. 구성 요소의 모든 측면을 사용자 정의해야 할 경우 대신 [프록시 구성 요소 패턴](/help/developing/guidelines.md#proxy-component-pattern)을 사용해야 합니다.
* 을 위해 [목차 구성 요소](/help/components/tableofcontents.md) 콘텐츠를 렌더링하려면 OSGi에서 필터를 구성해야 합니다.
   * [구성 요소의 GitHub 설명서를 참조하십시오](https://adobe.com/go/aem_cmp_tech_tableofcontents_v1_kr) 추가 정보.

### AEM 6.5 및 이전 {#aem-65}

프로덕션 모드(샘플 콘텐츠 없음)에서 시작할 때 핵심 핵심 구성 요소는 빠른 시작의 일부가 아닙니다. 따라서 첫 번째 단계는 [GitHub에서 최신 릴리스된 콘텐츠 패키지를 다운로드](https://github.com/adobe/aem-core-wcm-components/releases/latest)하여 AEM 환경에 설치하는 것입니다.

몇 가지 방법으로 이 프로세스를 자동화할 수 있지만 패키지 관리자를 사용하면 인스턴스에서 콘텐츠 패키지를 빠르게 설치할 수 있습니다. [패키지 설치](https://experienceleague.adobe.com/docs/experience-manager-65/administering/contentmanagement/package-manager.html#installing-packages)를 참조하십시오. 또한, 게시 인스턴스가 실행되면 해당 패키지를 복제해야 합니다. [패키지 복제](https://experienceleague.adobe.com/docs/experience-manager-65/administering/contentmanagement/package-manager.html#replicating-packages)를 참조하십시오.

## 프록시 구성 요소 제작 {#create-proxy-components}

[프록시 구성 요소 패턴](/help/developing/guidelines.md#proxy-component-pattern) 섹션에서 설명한 이유를 살펴보면 콘텐츠에서 바로 핵심 구성 요소를 참조해서는 안 됩니다. 이를 방지하기 위해 구성 요소 모두는 숨겨진 구성 요소 그룹(`.core-wcm` 또는 `.core-wcm-form`)에 속합니다. 이로써 구성 요소는 편집기에 바로 표시되지 않습니다.

대신 사이트별 구성 요소를 제작합니다. 페이지 작성자에게 표시하려는 원하는 구성 요소 이름 및 그룹을 정의하고 슈퍼타입으로 핵심 구성 요소에 조회할 수 있습니다. 이 사이트별 구성 요소는 “프록시 구성 요소”라고도 합니다. 이는 구성 요소에 아무것도 포함되지 않고 사이트에 사용할 구성 요소 버전을 정의할 수 없기 때문입니다. 단, [핵심 구성 요소](/help/developing/customizing.md)를 사용자 정의하는 경우 해당 프록시 구성 요소는 마크업과 논리 사용자 정의에 중요한 역할을 수행합니다.

이에 각 핵심 구성 요소를 사이트에 사용할 경우 다음 작업을 수행해야 합니다.

1. 사이트의 구성 요소 폴더에 해당 프록시 구성 요소를 만듭니다.

   **예제**: `/apps/my-site/components`에 유형의 제목 노드 제작 `cq:Component`

1. 슈퍼타입으로 해당 핵심 구성 요소 버전을 지정합니다.

   **예제**: 다음 속성을 추가합니다.\
   `sling:resourceSuperType="core/wcm/components/title/v1/title"`

1. 구성 요소의 그룹, 제목 및 설명 (선택 사항)을 정의합니다. 해당 값은 프로젝트에 따라 다르고 구성 요소가 작성자에게 어떻게 노출되었는지 보여 줍니다.

   **예제**: 다음 속성을 추가합니다.

   ```shell
   componentGroup="My Site"
   jcr:title="Title"  
   jcr:description="Section Heading"
   ```

예를 들어 [WKND 사이트의 제목 구성 요소](https://github.com/adobe/aem-guides-wknd/blob/master/ui.apps/src/main/content/jcr_root/apps/wknd/components/title/.content.xml)를 살펴봅니다. 이러한 식으로 빌드된 프록시 구성 요소의 좋은 사례입니다.

## 핵심 스타일 로드하기 {#load-the-core-styles}

1. 아직 로드되지 않은 경우 사이트에 필요한 CSS와 JS 파일이 모두 포함된 [클라이언트 라이브러리](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html)를 만듭니다.
1. 사이트의 클라이언트에서 종속성을 필요한 핵심 구성 요소에 추가합니다. 이는 `embed` 속성 추가를 통해 수행됩니다.

   예를 들어 v1 핵심 구성 요소의 클라이언트 라이브러리를 모두 포함하려면 추가할 속성은 다음과 같습니다.

   ```shell
   embed="[  
   core.wcm.components.image.v1,  
   core.wcm.components.list.v1,  
   core.wcm.components.breadcrumb.v1,  
   core.wcm.components.form.container.v1,  
   core.wcm.components.form.text.v1  
   ]"
   ```

다음 섹션으로 이동하기 전에 프록시 구성 요소와 클라이언트 라이브러리가 AEM 환경에 배포되었는지 확인합니다.

## 구성 요소 사용하기 {#allow-the-components}

[템플릿 편집기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html)에서 다음 단계를 수행합니다.

1. 템플릿 편집기에서 레이아웃 컨테이너를 선택한 다음 정책을 엽니다.
1. 허용된 구성 요소 목록에서 이전에 제작된 프록시 구성 요소를 선택합니다. 프록시 구성 요소는 해당 구성 요소에 할당된 구성 요소 그룹에 표시됩니다. 완료되면 변경 사항을 적용합니다.
1. 선택적으로, 구성 요소에 디자인 대화 상자가 있는 경우 사전 구성될 수 있습니다.

맞습니다. 편집한 템플릿에서 만든 페이지를 통해 새로 제작한 구성 요소를 사용할 수 있습니다.

**다음 참조:**

* [핵심 구성 요소 맞춤화](/help/developing/customizing.md) - 핵심 구성 요소 스타일링 및 사용자 정의하는 방법에 대해 알아봅니다.
* [구성 요소 가이드라인](/help/developing/guidelines.md) - 핵심 구성 요소의 구현 패턴에 대해 알아봅니다.

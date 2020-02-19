---
title: 핵심 구성 요소 사용
description: '"프로젝트에서 핵심 구성 요소를 바로 실행하려면 다음 3단계를 수행하십시오.다운로드 및 설치, 프록시 구성 요소 제작, 핵심 스타일 로드, 템플릿에 구성 요소 허용 등 다양한 작업을 수행할 수 있습니다."'
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# 핵심 구성 요소 사용{#using-core-components}

자체 프로젝트에서 핵심 구성 요소를 사용하여 바로 실행하려면 아래 섹션에 개별적으로 설명된 4가지 단계가 있습니다.

1. [다운로드 및 설치](#download-and-install)
1. [프록시 구성 요소 만들기](#create-proxy-components)
1. [코어 스타일 로드](#load-the-core-styles)
1. [구성 요소 활성화](#allow-the-components)

>[!NOTE]
>
>또는 프로젝트 설정을 사용하여 처음부터 시작하는 방법에 대한 자세한 지침, 핵심 구성 요소, 편집 가능한 템플릿, 클라이언트 라이브러리 및 구성 요소 개발을 살펴보려면 다음 다중 부분 자습서가 유용할 수 있습니다.\
>[AEM Sites 시작하기 - WKND 자습서](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)

## 다운로드 및 설치 {#download-and-install}

핵심 구성 요소의 주요 아이디어 중 하나는 유연성입니다. 새로운 버전의 핵심 구성 요소를 출시하면 Adobe는 보다 유연하게 새로운 기능을 제공할 수 있습니다. 개발자는 프로젝트에 통합하려는 구성 요소와 프로젝트 업데이트 빈도를 유연하게 지정할 수 있습니다.

이러한 이유로, 핵심 구성 요소는 샘플 컨텐츠 없이 프로덕션 모드에서 시작할 때 빠른 시작에 속하지 않습니다. 따라서 첫 번째 단계는 GitHub에서 최신 릴리스된 콘텐츠 패키지를 [다운로드하고](https://github.com/adobe/aem-core-wcm-components/releases/latest) AEM 환경에 설치하는 것입니다.

이를 자동화하는 방법에는 여러 가지가 있지만, 인스턴스에 컨텐츠 패키지를 신속하게 설치하는 가장 간단한 방법은 패키지 관리자를 사용하는 것입니다.패키지 [설치를 참조하십시오](https://docs.adobe.com/content/help/en/experience-manager-65/administering/contentmanagement/package-manager.html#installing-packages). 또한 게시 인스턴스가 실행 중이면 해당 패키지를 게시자에게 복제해야 합니다.패키지 [복제를 참조하십시오](https://docs.adobe.com/content/help/en/experience-manager-65/administering/contentmanagement/package-manager.html#replicating-packages).

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T16:42:59.142-0400

Should we be promoting embedding the core-component package as an artifact in a customer application, reasoning as follows: 1) a customer application is required to leverage core components (at a minimum, proxy components must be defined) 2) a customer application must be updated to leverage new versions of core components (since it requires adjusting the sling:resourceSuperType to point at the new version of the component) It seems the only time theres an advantage to installing a release directly is if a bug-fix (non version-changing) release of core-components is cut, and it doesnt coincide with an application deployment. WDYT? For example, recommend doing this for ACS Commons which has a similar use-case (https://adobe-consulting-services.github.io/acs-aem-commons/pages/maven.html) We can of course keep the instructions for manually deploying, since some will want to do this, or the bug-fix use-case will appear.

 -->

## 프록시 구성 요소 만들기 {#create-proxy-components}

프록시 구성 요소 패턴 [섹션에 설명된](/help/developing/guidelines.md#proxy-component-pattern) 이유로 핵심 구성 요소를 컨텐츠에서 직접 참조해서는 안 됩니다. 이를 방지하기 위해 모든 구성 요소는 숨겨진 구성 요소 그룹( `.core-wcm` 또는 `.core-wcm-form`)에 속하므로 편집기에서 바로 표시되지 않습니다.

대신, 사이트 특정 구성 요소를 만들어야 합니다. 이 구성 요소는 페이지 작성자에게 표시할 원하는 구성 요소 이름과 그룹을 정의하고 각 구성 요소를 상위 유형으로 핵심 구성 요소를 참조합니다. 이러한 사이트별 구성 요소는 아무 것도 포함할 필요가 없고 주로 사이트에 사용할 구성 요소의 버전을 정의하기 위해 제공되므로 &quot;프록시 구성 요소&quot;라고도 합니다. 그러나 핵심 구성 요소를 사용자 [지정할](/help/developing/customizing.md)때 이러한 프록시 구성 요소는 마크업 및 논리 사용자 지정에 필수적인 역할을 합니다.

따라서 사이트에 사용할 각 핵심 구성 요소에 대해 다음을 수행해야 합니다.

1. 사이트의 구성 요소 폴더에 해당 프록시 구성 요소를 만듭니다.

   **예** Under `/apps/my-site/components` create a title node of type `cq:Component`

1. 슈퍼 유형이 있는 해당 코어 구성 요소 버전을 가리킵니다.

   **예**: 다음 속성 추가:\
   `sling:resourceSuperType="core/wcm/components/title/v1/title"`

1. 구성 요소의 그룹, 제목 및 선택적으로 설명을 정의합니다. 이러한 값은 프로젝트별로 다르며 구성 요소가 작성자에게 어떻게 노출되는지를 나타냅니다.

   **예**: 다음 속성 추가:

   ```shell
   componentGroup="My Site"
   jcr:title="Title"  
   jcr:description="Section Heading"
   ```

예를 들어 We.Retail 참조 사이트의 [제목 구성 요소를](https://github.com/Adobe-Marketing-Cloud/aem-sample-we-retail/blob/master/ui.apps/src/main/content/jcr_root/apps/weretail/components/content/title/.content.xml)보십시오. 이러한 방식으로 만들어지는 프록시 구성 요소의 좋은 예입니다.

## 코어 스타일 로드 {#load-the-core-styles}

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T16:57:16.414-0400

Styles is odd in that most Core Components do not have CSS; very few even have structural CSS (breadcrumbs, list) It may be more apt to title this section: Load the Core JavaScript and CSS or Load the Core Client Libraries ?

 -->

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T17:41:37.115-0400

This section seems to cover the "sites" clientlibs for core components; Do we need a section for ensuring the editor clientlibs are loaded in the Page Editor? Pending: https://github.com/Adobe-Marketing-Cloud/aem-core-wcm-components/issues/15

 -->

<!-- 

Comment Type: annotation
Last Modified By: cotescu
Last Modified Date: 2018-03-09T10:45:52.812-0500

Load the Core Client Libraries sounds way better

 -->

1. 아직 완료하지 않은 경우 [사이트에](https://docs.adobe.com/content/help/en/experience-manager-65/developing/introduction/clientlibs.html) 필요한 모든 CSS 및 JS 파일이 포함된 클라이언트 라이브러리를 만듭니다.
1. 사이트의 클라이언트 라이브러리에서 필요한 핵심 구성 요소에 종속성을 추가합니다. 이 작업은 `embed` 속성을 추가하여 수행됩니다.

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

다음 섹션으로 이동하기 전에 프록시 구성 요소 및 클라이언트 라이브러리가 AEM 환경에 배포되었는지 확인하십시오.

## 구성 요소 허용 {#allow-the-components}

템플릿 편집기에서 다음 단계를 [수행합니다](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

1. 템플릿 편집기에서 레이아웃 컨테이너를 선택하고 정책을 엽니다.
1. 허용된 구성 요소 목록에서 이전에 만든 프록시 구성 요소를 선택합니다. 이 구성 요소는 할당된 구성 요소 그룹 아래에 표시됩니다. 완료되면 변경 내용을 적용합니다.
1. 선택적으로, 디자인 대화 상자가 있는 구성 요소의 경우 미리 구성할 수 있습니다.

그거야! 편집된 템플릿으로 만든 페이지에서 새로 만든 구성 요소를 사용할 수 있습니다.

**다음 참조:**

* [핵심 구성 요소 사용자](/help/developing/customizing.md) 지정 - 핵심 구성 요소의 스타일을 지정하고 사용자 지정하는 방법을 알아봅니다.
* [구성 요소](/help/developing/guidelines.md) 지침 - 핵심 구성 요소의 구현 패턴을 학습합니다.

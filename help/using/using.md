---
title: 핵심 구성 요소 사용
seo-title: 핵심 구성 요소 사용
description: 'null'
seo-description: '" 프로젝트에 핵심 구성 요소를 사용하여 실행하려면 다음 세 가지 단계를 수행해야 합니다. 다운로드 및 설치하고, 프록시 구성 요소를 만들고, 핵심 스타일을 로드하고, 템플릿의 구성 요소를 허용합니다. "'
uuid: A 1 EF 2 ACF -8226-4510-838 B-F 5 FAE 196 F 9 F 1
contentOwner: 사용자
content-type: 참조
topic-tags: developing
products: sg_ Experiencemanager/Corecomponents-new
discoiquuid: 1703 A 171-830 c -477 E-A 34 F -99 Caba 841 EC 4
disttype: dist5
gnavtheme: 밝음
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 1243d6cc1b0b015ee2f37ae89d0e2e42d366cc02

---


# 핵심 구성 요소 사용{#using-core-components}

자체 프로젝트에서 [핵심 구성 요소를](developing.md) 사용하여 실행하려면 다음 네 가지 단계가 있습니다. 이 단계는 아래의 섹션에 개별적으로 설명되어 있습니다.

1. [다운로드 및 설치](#download-and-install)
1. [프록시 구성 요소 만들기](#create-proxy-components)
1. [핵심 스타일 로드](#load-the-core-styles)
1. [구성 요소 활성화](#allow-the-components)

>[!NOTE]
>
>또는 프로젝트 설정, 핵심 구성 요소, 편집 가능한 템플릿, 클라이언트 라이브러리 및 구성 요소 개발을 통해 처음부터 시작하는 방법에 대한 광범위한 지침을 살펴보려면 다음과 같은 다중 파트 자습서를 활용할 수 있습니다.\
>[AEM Sites 시작하기 - WKND 자습서](wknd-tutorial.md)

## 다운로드 및 설치 {#download-and-install}

핵심 구성 요소 뒤에 있는 아이디어 중 하나는 유연성입니다. 새로운 버전의 핵심 구성 요소를 출시하면 Adobe는 새로운 기능을 더욱 유연하게 제공할 수 있게 되었습니다. 따라서 개발자는 프로젝트에 통합하려는 구성 요소 및 업데이트 빈도를 유연하게 파악할 수 있습니다.

이러한 이유로 핵심 구성 요소는 샘플 컨텐츠 없이 프로덕션 모드에서 시작할 때 빠른 시작 부분이 아닙니다. 따라서 첫 번째 단계는 Github에서 최신 릴리스된 콘텐츠 패키지를 [다운로드하고](https://github.com/adobe/aem-core-wcm-components/releases/latest) AEM 환경에 설치하는 것입니다.

이를 자동화하는 방법에는 몇 가지가 있지만, 인스턴스에 컨텐츠 패키지를 신속하게 설치하는 가장 간단한 방법은 패키지 관리자를 사용하는 것입니다. 패키지 [설치를 참조하십시오](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/package-manager.html). 또한 게시 인스턴스를 실행하게 되면 해당 패키지를 게시자에게 복제해야 합니다. 패키지 [복제를 참조하십시오](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/package-manager.html).

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T16:42:59.142-0400

Should we be promoting embedding the core-component package as an artifact in a customer application, reasoning as follows: 1) a customer application is required to leverage core components (at a minimum, proxy components must be defined) 2) a customer application must be updated to leverage new versions of core components (since it requires adjusting the sling:resourceSuperType to point at the new version of the component) It seems the only time theres an advantage to installing a release directly is if a bug-fix (non version-changing) release of core-components is cut, and it doesnt coincide with an application deployment. WDYT? For example, recommend doing this for ACS Commons which has a similar use-case (https://adobe-consulting-services.github.io/acs-aem-commons/pages/maven.html) We can of course keep the instructions for manually deploying, since some will want to do this, or the bug-fix use-case will appear.

 -->

## 프록시 구성 요소 만들기 {#create-proxy-components}

[프록시 구성 요소 패턴](guidelines.md#proxy-component-pattern) 섹션에 설명된 이유로, 핵심 구성 요소는 내용에서 직접 참조되면 안 됩니다. 이를 방지하기 위해 모두 숨겨진 구성 요소 그룹에 속하므로 ( `.core-wcm` OR `.core-wcm-form`) 편집기에 직접 표시되지 않습니다.

대신, 페이지 작성자에게 표시할 구성 요소 이름과 그룹을 정의하고 상위 구성 요소로 핵심 구성 요소를 참조하는 사이트 특정 구성 요소를 만들어야 합니다. 이러한 사이트별 구성 요소는 &quot;프록시 구성 요소&quot; 라고도 합니다. 이러한 구성 요소는 아무 것도 포함할 필요가 없으므로 사이트에 사용할 구성 요소의 버전을 정의하는 데 도움이 됩니다. 그러나 [핵심 구성 요소를](customizing.md)사용자 정의할 때 이러한 프록시 구성 요소는 마크업 및 논리 사용자 정의에 필수적인 역할을 합니다.

따라서 사이트에 사용하려는 각 핵심 구성 요소에 대해 다음을 수행해야 합니다.

1. 사이트의 구성 요소 폴더에 해당 프록시 구성 요소를 만듭니다.

   **Create**
a title node of type under `/apps/my-site/components` type `cq:Component`

1. super-type로 해당 핵심 구성 요소 버전을 가리킵니다.

   **example**
add following property:\
   `sling:resourceSuperType="core/wcm/components/title/v1/title"`

1. 구성 요소의 그룹, 제목 및 선택적으로 설명을 정의합니다. 이러한 값은 프로젝트별로 다르며 작성자가 작성자에게 노출되는 방식을 나타냅니다.

   **예를**
들어 다음 속성을 추가합니다.

   ```shell
   componentGroup="My Site"
   jcr:title="Title"  
   jcr:description="Section Heading"
   ```

예를 들어 We. Retail 참조 사이트의 [제목 구성 요소를 살펴보십시오](https://github.com/Adobe-Marketing-Cloud/aem-sample-we-retail/blob/master/ui.apps/src/main/content/jcr_root/apps/weretail/components/content/title/.content.xml). 이는 이러한 방식으로 구축된 프록시 구성 요소의 좋은 예입니다.

## 핵심 스타일 로드 {#load-the-core-styles}

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

1. 아직 수행하지 않은 경우 사이트에 필요한 모든 CSS 및 JS 파일이 들어 있는 [클라이언트 라이브러리를](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/clientlibs.html) 만듭니다.
1. 사이트의 클라이언트 라이브러리에서 필요한 핵심 구성 요소에 종속성을 추가합니다. 이 작업은 `embed` 속성을 추가하여 수행됩니다.

   예를 들어, 모든 v 1 핵심 구성 요소의 클라이언트 라이브러리를 포함하려면 추가할 속성이 다음과 같습니다.

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

다음 단계는 일반적으로 기존 설정을 위해 [템플릿 편집기에서](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)수행됩니다. 하지만 이 작업은 디자인 모드에서 수행할 수 있습니다.

1. 템플릿 편집기 (또는 디자인 모드) 에서 레이아웃 컨테이너 (또는 parsys) 를 선택하고 해당 정책 (또는 디자인 구성) 를 엽니다.
1. 허용된 구성 요소 목록에서 이전에 만든 프록시 구성 요소를 선택하고 여기에 지정된 구성 요소 그룹 아래에 나타나야 합니다. 완료되면 변경 사항을 적용합니다.
1. 디자인 대화 상자가 있는 구성 요소의 경우 미리 구성할 수 있습니다.

즉, 편집된 템플릿으로 만든 페이지에서 새로 만든 구성 요소를 사용할 수 있습니다.

**다음을 참조하십시오.**

* [핵심 구성 요소 맞춤화](customizing.md) - 핵심 구성 요소의 스타일을 지정하고 사용자 지정하는 방법을 알아보십시오.
* [구성 요소 지침](guidelines.md) - 핵심 구성 요소의 구현 패턴을 학습합니다.

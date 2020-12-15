---
title: PDF 뷰어 구성 요소
description: PDF 뷰어 구성 요소를 사용하면 PDF 문서를 표시할 수 있습니다.
translation-type: tm+mt
source-git-commit: 24a810ff634f8846881dfa0095e879476d0f16f0
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 3%

---


# PDF 뷰어 구성 요소 {#pdf-viewer-component}

핵심 구성 요소 PDF 뷰어 구성 요소를 사용하면 페이지에 PDF 문서를 포함할 수 있습니다.

## 사용량 {#usage}

핵심 구성 요소 PDF 뷰어 구성 요소에는 페이지에 에셋으로 저장된 PDF 파일을 표시하는 뷰어가 포함됩니다.

## 버전 및 호환성 {#version-and-compatibility}

PDF 뷰어 구성 요소의 현재 버전은 v1이며, 2020년 6월 핵심 구성 요소 릴리스 2.10.0에 도입되었으며 이 문서에 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소 버전이 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 설명합니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

HTML 및 JSON 출력뿐만 아니라 PDF 뷰어 구성 요소의 구성 옵션 예를 보려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_pdfviewer)를 방문하십시오.

## 기술 세부 정보 {#technical-details}

PDF 뷰어 구성 요소 [에 대한 최신 기술 문서는 GitHub](https://adobe.com/go/aem_cmp_tech_pdfviewer_v1)에서 찾을 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)에서 확인할 수 있습니다.

>[!NOTE]
>
>PDF 뷰어 구성 요소는 [Adobe의 Document Services API](https://www.adobe.io/apis/documentcloud/dcsdk.html)를 활용하며, 이러한 서비스를 사용하려면 관리자가 [컨텍스트 인식 구성](/help/developing/context-aware-configs.md)을 구성해야 합니다. 이 구성에 대한 [자세한 내용은 구성 요소의 기술 설명서를 참조하십시오.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config)

## 구성 대화 상자 {#configure-dialog}

구성 대화 상자를 사용하면 컨텐츠 작성자가 뷰어를 정의하고 방문자가 페이지를 방문하면서 어떻게 행동하고 나타나는지 정의할 수 있습니다.

### 구성 탭 {#configuration-tab}

구성 탭을 사용하면 작성자가 표시해야 하는 PDF를 정의할 수 있습니다. 경로는 AEM의 에셋으로 정의하거나 다른 리소스에 대한 절대 경로로 정의할 수 있습니다.

![PDF 뷰어 구성 요소의 편집 대화 상자 구성 탭](/help/assets/pdf-viewer-edit-configuration.png)

### 사용자 지정 탭 {#customize-tab}

[사용자 정의] 탭을 사용하여 작성자는 뷰어에서 독자에게 사용할 수 있는 옵션과 뷰어를 표시할 방법을 정의할 수 있습니다.

![PDF 뷰어 구성 요소의 편집 대화 상자 사용자 정의 탭](/help/assets/pdf-viewer-edit-customize.png)

사용 가능한 옵션 수는 선택한 **유형**&#x200B;에 따라 달라집니다.

* [전체 창](#full-window)  - 보기 영역이 전체 브라우저에서 렌더링됩니다. 스토리지 및 생산성 애플리케이션에 가장 적합합니다.
* [크기 컨테이너](#sized-container)  - 보기 영역이 전체 브라우저에서 렌더링됩니다. 스토리지 및 생산성 애플리케이션에 가장 적합합니다.
* [인라인](#in-line)  - 웹 페이지 내에서 한 줄에 렌더링되는 모든 PDF 페이지입니다. 응용 프로그램을 읽는 데 가장 적합합니다.

#### 전체 창 {#full-window}

보기 영역은 전체 브라우저에서 렌더링됩니다. 스토리지 및 생산성 애플리케이션에 가장 적합합니다.

![PDF 뷰어 구성 요소의 편집 대화 상자 전체 창 옵션 사용자 정의](/help/assets/pdf-viewer-edit-customize-full.png)

* **기본 보기 모드**  - 뷰어가 표시되는 페이지에 어떻게 맞게 표시됩니까?
   * 페이지에 맞추기
   * 너비에 맞추기
* **전체 화면**  - 이 옵션을 활성화하면 뷰어가 뷰포트의 전체 높이/폭을 차지하게 됩니다.
* **주석 도구**  - 활성화되면 주석 도구를 사용할 수 있습니다.
* **왼쪽 손 패널**  - 활성화되면 왼쪽 패널이 표시됩니다.
* **PDF**  다운로드 - 활성화되면 다운로드 단추가 표시됩니다.
* **PDF**  인쇄 - 활성화되면 인쇄 단추가 표시됩니다.
* **페이지 컨트롤**  - 페이지 컨트롤의 동작을 전환합니다.
   * 고정
   * 고정 해제

#### 크기가 조정된 컨테이너 {#sized-container}

보기 영역은 전체 브라우저에서 렌더링됩니다. 스토리지 및 생산성 애플리케이션에 가장 적합합니다.

![PDF 뷰어 구성 요소의 편집 대화 상자에서 탭 크기 컨테이너 옵션 사용자 정의](/help/assets/pdf-viewer-edit-customize-sized-container.png)

* **전체 화면**  - 이 옵션을 활성화하면 뷰어가 뷰포트의 전체 높이/폭을 차지하게 됩니다.
* **PDF**  다운로드 - 활성화되면 다운로드 단추가 표시됩니다.
* **PDF**  인쇄 - 활성화되면 인쇄 단추가 표시됩니다.
* **페이지 컨트롤**  - 페이지 컨트롤의 동작을 전환합니다.
   * 고정
   * 고정 해제

#### 인라인 {#in-line}

웹 페이지 내에서 모든 PDF 페이지가 한 줄로 렌더링됩니다. 응용 프로그램을 읽는 데 가장 적합합니다.

![PDF 뷰어 구성 요소의 편집 대화 상자에서 탭 크기 컨테이너 옵션 사용자 정의](/help/assets/pdf-viewer-edit-customize-inline.png)

* **PDF**  다운로드 - 활성화되면 다운로드 단추가 표시됩니다.
* **PDF**  인쇄 - 활성화되면 인쇄 단추가 표시됩니다.

## 디자인 대화 상자 {#design-dialog}

PDF 뷰어 구성 요소에 대한 디자인 대화 상자가 없습니다.

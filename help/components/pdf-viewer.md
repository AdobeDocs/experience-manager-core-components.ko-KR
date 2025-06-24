---
title: PDF 뷰어 구성 요소
description: PDF 뷰어 구성 요소를 사용하여 PDF 문서를 표시할 수 있습니다.
role: Architect, Developer, Admin, User
exl-id: deb635f5-2b73-4e7a-9838-3a941e39e898
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# PDF 뷰어 구성 요소 {#pdf-viewer-component}

핵심 구성 요소의 PDF 뷰어 구성 요소를 사용하여 페이지에 PDF 문서를 포함할 수 있습니다.

{{traditional-aem}}

## 사용량 {#usage}

핵심 구성 요소의 PDF 뷰어 구성 요소는 뷰어를 임베드하여 페이지의 자산으로 저장된 PDF 파일을 표시합니다.

## 버전 및 호환성 {#version-and-compatibility}

현재 버전의 PDF 뷰어 구성 요소는 2020년 6월 핵심 구성 요소 릴리스 2.10.0과 함께 도입된 v1입니다. 이 문서에서는 해당 구성 요소에 대해 설명합니다.

다음 테이블에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |---|---|---|
| v1 | <br>[릴리스 2.17.4](/help/versions.md) 및 이전 버전과 호환 가능 | 호환 가능 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/versions.md)을 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

PDF 뷰어 구성 요소를 경험하고 구성 옵션의 샘플뿐만 아니라 HTML 및 JSON 출력을 확인하려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_pdfviewer_kr)를 참조하십시오.

## 기술 세부 정보 {#technical-details}

PDF 뷰어 구성 요소에 대한 최신 기술 설명서는[ GitHub에서 확인할 수 있습니다](https://adobe.com/go/aem_cmp_tech_pdfviewer_v1_kr).

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

>[!NOTE]
>
>PDF 뷰어 구성 요소는 [Adobe의 문서 서비스 API](https://www.adobe.io/apis/documentcloud/dcsdk.html)를 활용합니다. 관리자는 이를 통해 [텍스트 인식 구성](/help/developing/context-aware-configs.md)을 구성하여 해당 서비스를 사용할 수 있습니다. [이 구성에 대한 자세한 내용](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config)은 구성 요소의 기술 설명서를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

콘텐츠 작성자는 구성 대화 상자를 통해 뷰어와 방문자를 위한 페이지 작동 및 표시 방법을 정의할 수 있습니다.

### 구성 탭 {#configuration-tab}

작성자는 구성 탭을 사용하여 표시할 PDF를 정의할 수 있습니다. AEM의 자산이나 다른 리소스에 대한 절대 경로로 경로를 정의할 수 있습니다.

![PDF 뷰어 구성 요소의 편집 대화 상자 구성 탭](/help/assets/pdf-viewer-edit-configuration.png)

### 맞춤화 탭 {#customize-tab}

콘텐츠 작성자는 맞춤화 탭을 통해 뷰어에서 리더가 사용할 수 있는 옵션과 뷰어를 제공하는 방법을 정의할 수 있습니다.

![PDF 뷰어 구성 요소의 편집 대화 상자 맞춤화 탭](/help/assets/pdf-viewer-edit-customize.png)

사용 가능한 옵션의 수는 선택한 **유형**&#x200B;에 따라 달라집니다.

* [전체 창](#full-window) - 전체 브라우저에서 보기 영역이 렌더링됩니다. 스토리지와 생산성 애플리케이션에 가장 적합합니다.
* [크기가 조정된 컨테이너](#sized-container) - 전체 브라우저에서 보기 영역이 렌더링됩니다. 스토리지와 생산성 애플리케이션에 가장 적합합니다.
* [인라인](#in-line) - 웹 페이지에서 모든 PDF 페이지가 렌더링됩니다. 읽기 애플리케이션에 가장 적합합니다.

#### 전체 창 {#full-window}

전체 브라우저에서 보기 영역이 렌더링됩니다. 스토리지와 생산성 애플리케이션에 가장 적합합니다.

![PDF 뷰어 구성 요소의 전체 창 옵션 맞춤화 탭](/help/assets/pdf-viewer-edit-customize-full.png)

* **기본 보기 모드** - 뷰어가 표시되는 페이지에 뷰어를 맞추는 방법
   * 페이지에 맞추기
   * 너비에 맞추기
* **전체 화면** - 활성화되면 뷰어는 뷰포트의 전체 높이/폭을 차지합니다.
* **주석 툴** - 활성화되면 주석 툴을 사용할 수 있습니다.
* **좌측 패널** - 활성화되면 좌측 패널이 표시됩니다.
* **PDF 다운로드** - 활성화되면 다운로드 버튼이 표시됩니다.
* **PDF 인쇄** - 활성화되면 인쇄 버튼이 표시됩니다.
* **페이지 제어 기능** - 페이지 제어 기능의 비헤이비어를 켜거나 끕니다.
   * 도크
   * 도크 분리

#### 크기가 조정된 컨테이너 {#sized-container}

전체 브라우저에서 보기 영역이 렌더링됩니다. 스토리지와 생산성 애플리케이션에 가장 적합합니다.

![PDF 뷰어 구성 요소의 크기가 조정된 컨테이너 옵션 맞춤화 탭](/help/assets/pdf-viewer-edit-customize-sized-container.png)

* **전체 화면** - 활성화되면 뷰어는 뷰포트의 전체 높이/폭을 차지합니다.
* **PDF 다운로드** - 활성화되면 다운로드 버튼이 표시됩니다.
* **PDF 인쇄** - 활성화되면 인쇄 버튼이 표시됩니다.
* **페이지 제어 기능** - 페이지 제어 기능의 비헤이비어를 켜거나 끕니다.
   * 도크
   * 도크 분리

#### 인라인 {#in-line}

웹 페이지에서 모든 PDF 페이지가 렌더링됩니다. 읽기 애플리케이션에 가장 적합합니다.

![PDF 뷰어 구성 요소의 크기가 조정된 컨테이너 옵션 맞춤화 탭](/help/assets/pdf-viewer-edit-customize-inline.png)

* **PDF 다운로드** - 활성화되면 다운로드 버튼이 표시됩니다.
* **PDF 인쇄** - 활성화되면 인쇄 버튼이 표시됩니다.

## 디자인 대화 상자 {#design-dialog}

PDF 뷰어 구성 요소용 디자인 대화 상자는 없습니다.

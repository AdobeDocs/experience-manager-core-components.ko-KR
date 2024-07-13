---
title: 이미지 구성 요소 (v1)
description: 핵심 구성 요소의 이미지 구성 요소는 바로 편집 기능이 있는 적응형 이미지 구성 요소입니다.
index: n
role: Architect, Developer, Admin, User
exl-id: 625ce8de-5c4a-476d-b749-895493d169b1
source-git-commit: 5f25aee6ebcb7a5c6b8db0df5b8b853f15af97d0
workflow-type: tm+mt
source-wordcount: '1293'
ht-degree: 98%

---

# 이미지 구성 요소 (v1) {#image-component-v}

핵심 구성 요소의 이미지 구성 요소는 바로 편집 기능이 있는 적응형 이미지 구성 요소입니다.

## 사용량 {#usage}

이미지 구성 요소를 사용하여 이미지 에셋을 간단히 배치하고 바로 편집 기능을 제공합니다. 콘텐츠 작성자의 소극적 로드 및 자르기 옵션이 있는 적응형 이미지 선택 기능이 포함됩니다.

템플릿 작성자는 [디자인 대화 상자](#design-dialog)에서 허용된 이미지 폭과 자르기 및 추가 설정 옵션을 정의할 수 있습니다. 콘텐츠 편집기는 [구성 대화 상자](#configure-dialog)에서 에셋을 업로드하거나 선택하고, [편집 대화 상자](#edit-dialog)에서 이미지를 자를 수 있습니다. 편리성을 추가하기 위해 이미지의 간단한 바로 수정 기능을 사용할 수도 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

이 문서에서는 AEM 6.3을 포함하는 핵심 구성 요소 릴리스 1.0.0과 함께 최초 도입된 이미지 구성 요소 v1에 대해 설명합니다.

다음 표에서 이미지 구성 요소 v1의 호환성을 확인할 수 있습니다.

| AEM 버전 | 이미지 구성 요소 v1 |
|--- |--- |
| 6.3 | 호환 가능 |
| 6.4 | 호환 가능 |

>[!CAUTION]
>
>이 문서에서는 이미지 구성 요소 v1에 대해 설명합니다.
>
>현재 버전의 이미지 구성 요소에 대한 자세한 내용은 [이미지 구성 요소](/help/components/image.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

다음은 [We.Retail](https://helpx.adobe.com/kr/experience-manager/6-4/sites/developing/using/we-retail.html)에서 얻은 샘플입니다.

### 스크린샷 {#screenshot}

![](/help/assets/chlimage_1-7.png)

### HTML {#html}

```
<div class="cmp cmp-image aem-GridColumn aem-GridColumn--default--12">
 
        <noscript data-cmp-image="{&#34;smartImages&#34;:[],&#34;smartSizes&#34;:[],&#34;lazyEnabled&#34;:true}">
            <img src="/content/we-retail/us/en/equipment/_jcr_content/root/responsivegrid/image.img.jpg" alt="Surfboard"/>
        </noscript>

</div>
```

### JSON {#json}

```
"image": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "smartSizes": [],
              "smartImages": [],
              "lazyEnabled": true,
              "src": "/content/we-retail/us/en/equipment/equipment/jcr%3acontent/root/responsivegrid/image.img.jpeg",
              ":type": "weretail/components/content/image"
            }
```

>[!NOTE]
>
>핵심 구성 요소에서 JSON을 내보내는 데 핵심 구성 요소 릴리스 1.1.0이 필요합니다. 자세한 내용은 [핵심 구성 요소 v1에 대한 호환성 정보](/help/versions.md)를 참조하십시오.

## 구성 대화 상자 {#configure-dialog}

[표준 편집 대화 상자](#edit-dialog) 및 [디자인 편집 상자](#design-dialog) 외에도 이미지 구성 요소는 설명 및 기본 속성과 함께 이미지 자체를 정의하는 구성 대화 상자를 제공합니다.

![](/help/assets/chlimage_1-50.png)

* **이미지 에셋**
   * [에셋 브라우저](https://helpx.adobe.com/kr/experience-manager/6-3/sites/authoring/using/author-environment-tools.html#main-pars_title)에서 에셋을 삭제하거나 **검색** 옵션을 탭하여 로컬 파일 시스템에서 로드합니다.
   * **지우기**&#x200B;를 탭하거나 클릭하여 현재 선택된 이미지 선택을 해제합니다.
   * **편집**&#x200B;을 탭하거나 클릭하여 에셋 편집기에서 [에셋 렌디션을 관리합니다](https://helpx.adobe.com/kr/experience-manager/6-3/assets/using/managing-assets-touch-ui.html#main-pars_title_19).

* **장식적 이미지** - 이미지가 보조 기술에서 무시되어 대체 텍스트가 필요한지 확인합니다. 이는 장식적 이미지에만 적용됩니다.
* **대체 텍스트** - 이미지 의미 또는 기능에 대한 시각 장애인 독자용 대체 텍스트입니다.
* **링크**
   * 이미지를 다른 리소스에 연결합니다.
   * 선택 대화 상자를 통해 다른 AEM 리소스에 연결합니다.
   * AEM 리소스에 연결되지 않은 경우 절대 URL을 입력합니다. 절대 URL이 아닌 URL은 AEM의 상대 URL로 해석됩니다.

* **캡션** - 이미지 아래 표시된 이미지에 대한 추가 정보는 기본입니다.
* **팝업으로 캡션 표시** - 확인 표시가 되어 있으면 캡션은 이미지 아래에 표시되지 않고 마우스로 이미지를 가리키면 일부 브라우저에서 팝업으로 표시됩니다.

## 편집 대화 상자 {#edit-dialog}

콘텐츠 작성자는 편집 대화 상자를 통해 실행 맵을 자르고 수정하고, 이미지를 확대/축소할 수 있습니다.

![](/help/assets/chlimage_1-8.png)

* 자르기 시작

  ![](/help/assets/chlimage_1-9.png)

  이 옵션을 선택하면 자르기 비율을 사전 정의하는 드롭다운이 열립니다.

   * **프리 핸드** 옵션을 선택하여 자체 자르기를 정의합니다.
   * **자르기 제거** 옵션을 선택하면 원본 에셋이 표시됩니다.

  자르기 옵션이 선택되면 파란색 핸들이 사용하여 이미지에서 자르기 크기를 조정합니다.

  ![](/help/assets/chlimage_1-10.png)

* 오른쪽 회전

  ![](/help/assets/chlimage_1-11.png)

  이 옵션을 사용하여 오른쪽으로(시계 방향으로) 이미지를 90° 회전합니다.

* 맵 실행

  ![](/help/assets/chlimage_1-12.png)

  이 옵션을 사용하여 실행 맵을 이미지에 적용합니다. 이 옵션을 선택하면 사용자가 맵의 모양을 선택할 수 있는 새 창이 열립니다.

   * **사각형 맵 추가**
   * **원형 맵 추가**
   * **다각형 맵 추가**

      * 기본적으로 삼각형 맵을 추가합니다. 해당 모양의 선을 더블 클릭하여 새 측면에 파란색 크기 조정 핸들을 새로 추가합니다.

  맵 모양이 선택되면 이미지 위에 겹쳐 놓고 크기를 조정합니다. 파란색 핸들을 드래그 앤 드롭하여 모양을 조정합니다.

  ![](/help/assets/chlimage_1-13.png)

  실행 앱 크기를 조정하고 나서 클릭하면 플로팅 툴바가 열려 링크 경로를 정의할 수 있습니다.

   * **경로**
      * 경로 피커 옵션을 사용하여 AEM에서 경로를 선택합니다.
      * 경로가 AEM에 없는 경우 절대 URL을 사용합니다. 절대 경로가 아닌 경로는 AEM의 상대 경로로 해석될 수 있습니다.

      * **대체 텍스트**
경로 대상에 대한 대체 설명
      * **대상**
         * **동일한 탭**
         * **새 탭**
         * **상위 프레임**
         * **맨 위 프레임**

  맵을 저장하려면 파란색 확인 표시를 탭하거나 클릭하고, 맵을 취소하려면 검은색 x를 탭하거나 클릭하고, 맵을 삭제하려면 빨간색 휴지통을 탭하거나 클릭합니다.

  ![](/help/assets/chlimage_1-14.png)

* 확대/축소 재설정

  ![](/help/assets/chlimage_1-15.png)

  이미지가 이미 확대/축소되었다면 이 옵션을 사용하여 확대/축소 레벨을 재설정합니다.

* 확대/축소 슬라이더 열기

  ![](/help/assets/chlimage_1-16.png)

  이 옵션을 사용하여 이미지의 확대/축소 레벨을 제어하는 슬라이더를 표시합니다.

  ![](/help/assets/chlimage_1-17.png)

바로 편집 기능을 가진 편집기를 사용하여 이미지를 수정합니다. 공간 제약으로 인라인에서는 기본 옵션만 제공됩니다. 전체 편집 옵션의 경우 전체 화면 모드를 사용합니다.

![](/help/assets/chlimage_1-18.png)

>[!NOTE]
>
>GIF 이미지의 경우 이미지 편집 작업(자르기, 뒤집기, 회전)이 지원되지 않습니다. 편집 모드에 변경 사항이 발생하면 지속되지 않습니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 통해 구성 요소 사용 시 필요한 자르기 업로드 및 회전 업로드를 정의할 수 있습니다.

### 메인 {#main}

**메인** 탭에서 이미지에 대해 허용된 너비 목록을 픽셀 단위로 정의하여 목록에서 가장 적절한 너비를 자동으로 로드합니다.

![](/help/assets/chlimage_1-51.png)

추가 버튼을 탭하거나 클릭하여 다른 크기를 추가합니다.

* 그랩 드래그 핸들을 사용하여 크기의 순서를 재배열합니다.
* 삭제 아이콘을 사용하여 폭을 삭제합니다.

기본적으로 이미지가 표시될 때까지 이미지 로드를 연기합니다. **소극적 로드 활성화** 옵션을 사용하여 페이지 로드에서 이미지를 로드합니다.

* **웹 최적화 이미지 활성화** - 선택하면 [웹에 최적화된 이미지 제공 서비스](/help/developing/web-optimized-image-delivery.md)는 WebP 형식으로 이미지를 전달하여 이미지 크기를 평균 25% 줄일 수 있습니다.
   * 이 옵션은 AEMaaCS에서만 사용할 수 있습니다.
   * 선택하지 않거나 웹 최적화된 이미지 제공 서비스를 사용할 수 없는 경우 [적응형 이미지 서블릿](/help/developing/adaptive-image-servlet.md)이 사용됩니다.

### 기능 {#features}

**기능** 탭에서 업로드 옵션, 방향 및 자르기 옵션을 사용할 때 콘텐츠 작성자가 사용할 수 있는 옵션을 정의할 수 있습니다.

* **웹 최적화 이미지 활성화** - 선택하면 웹에 최적화된 이미지 제공 서비스는 WebP 형식으로 이미지를 전달하여 이미지 크기를 평균 25% 줄일 수 있습니다.
   * 이 옵션은 AEMaaCS에서만 사용할 수 있습니다.
   * 선택하지 않거나 웹 최적화된 이미지 제공 서비스를 사용할 수 없는 경우 [적응형 이미지 서블릿](/help/developing/adaptive-image-servlet.md)이 사용됩니다.

* 소스

  ![](/help/assets/chlimage_1-19.png)

  **파일 시스템에서 에셋 업로드 허용** 옵션을 선택하여 콘텐츠 작성자는 자신의 컴퓨터에서 이미지를 업로드할 수 있습니다. 콘텐츠 작성자가 AEM에서 에셋만 강제 선택하려면 이 옵션 선택을 해제합니다.

* 방향

  ![](/help/assets/chlimage_1-20.png)

   * **회전** - 이 옵션을 사용하여 콘텐츠 작성자는 **오른쪽 회전** 옵션을 사용할 수 있습니다.
   * **뒤집기**
이 옵션을 사용하여 콘텐츠 작성자는 **가로 뒤집기** 및 **세로 뒤집기** 옵션을 사용할 수 있습니다.

  >[!CAUTION]
  >
  >**뒤집기** 옵션은 기본적으로 비활성화되어 있습니다. 옵션이 활성화되면 이미지 구성 요소의 편집 대화 상자에 **가로 뒤집기**&#x200B;와 **세로 뒤집기** 버튼이 표시됩니다. 하지만 AEM에서는 현재 기능을 지원하지 않으며 이 옵션 사용으로 변경 사항이 발생하면 지속되지 않습니다.

* 자르기

  ![](/help/assets/chlimage_1-21.png)

  **자르기 허용** 옵션을 선택하여 콘텐츠 작성자는 편집 대화 상자의 구성 요소에 있는 이미지를 자를 수 있습니다.
   * **추가**&#x200B;를 클릭하여 사전 정의된 자르기 종횡비를 추가합니다.
   * **자르기 시작** 드롭다운에 표시된 설명하는 이름을 입력합니다.
   * 숫자로 된 종횡비를 입력합니다.
   * 드래그 핸들을 사용하여 종횡비의 순서를 재배열합니다.
   * 휴지통을 사용하여 종횡비를 삭제합니다.

  >[!CAUTION]
  >
  >AEM에서 자르기 종횡비는 **높이/폭**&#x200B;으로 정의됩니다. 이는 종래의 폭/높이 정의와 다르며, 레거시 호환성을 위해 수행됩니다. 종횡비 이름이 UI에 명확하게 표시되고 종황비 자체가 아니기 때문에 이름이 제공되어도 콘텐츠 작성자는 차이를 알 수 없습니다.

## 기술 세부 사항 {#technical-details}

이미지 구성 요소에 대한 최신 기술 설명서는[ GitHub에서 확인할 수 있습니다](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/image/v1/image).

GitHub에서 전체 핵심 구성 요소 프로젝트를 다운로드할 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

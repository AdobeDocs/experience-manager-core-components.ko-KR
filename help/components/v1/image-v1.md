---
title: 이미지 구성 요소(v1)
description: 코어 구성 요소 이미지 구성 요소 는 즉석 편집 중인 응용 이미지 구성 요소 기능입니다.
index: n
role: Architect, Developer, Administrator, Business Practitioner
exl-id: 625ce8de-5c4a-476d-b749-895493d169b1
source-git-commit: 8ff36ca143af9496f988b1ca65475497181def1d
workflow-type: tm+mt
source-wordcount: '1229'
ht-degree: 3%

---

# 이미지 구성 요소(v1) {#image-component-v}

코어 구성 요소 이미지 구성 요소 는 즉석 편집 중인 응용 이미지 구성 요소 기능입니다.

## 사용량 {#usage}

이미지 구성 요소를 사용하면 이미지 자산 및 오퍼를 즉석 편집할 수 있습니다. 레이지 로딩과 컨텐츠 작성자를 위한 자르기가 포함된 적응형 이미지 선택이 가능합니다.

자르기와 추가 설정은 물론 허용되는 이미지 너비는 [디자인 대화 상자](#design-dialog)에서 템플릿 작성자가 정의할 수 있습니다. 컨텐츠 편집기는 [구성 대화 상자](#configure-dialog)에서 자산을 업로드하거나 선택하고 [편집 대화 상자](#edit-dialog)에서 이미지를 자를 수 있습니다. 편의상 간단한 이미지 즉석 수정 작업도 가능합니다.

## 버전 및 호환성 {#version-and-compatibility}

이 문서에서는 원래 AEM 6.3과 함께 코어 구성 요소 릴리스 1.0.0에 소개된 이미지 구성 요소 v1에 대해 설명합니다.

다음 표에는 이미지 구성 요소 v1의 호환성이 나와 있습니다.

| AEM 버전 | 이미지 구성 요소 v1 |
|--- |--- |
| 6.3 | 호환 가능 |
| 6.4 | 호환 가능 |

>[!CAUTION]
>
>이 문서에서는 이미지 구성 요소의 v1에 대해 설명합니다.
>
>이미지 구성 요소의 현재 버전에 대한 자세한 내용은 [이미지 구성 요소](/help/components/image.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

다음은 [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html)에서 가져온 샘플입니다.

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
>코어 구성 요소에서 JSON 내보내기를 사용하려면 핵심 구성 요소 릴리스 1.1.0이 필요합니다. 자세한 내용은 코어 구성 요소 v1](/help/versions.md)에 대한 호환성 정보를 참조하십시오.[

## 구성 대화 상자 {#configure-dialog}

표준 [편집 대화 상자](#edit-dialog) 및 [디자인 대화 상자](#design-dialog) 외에도 이미지 구성 요소는 설명 및 기본 속성과 함께 이미지 자체가 정의된 구성 대화 상자를 제공합니다.

![](/help/assets/chlimage_1-50.png)

* **이미지 자산**
   * [자산 브라우저](https://helpx.adobe.com/experience-manager/6-3/sites/authoring/using/author-environment-tools.html#main-pars_title)에서 자산을 끌어 놓거나 **찾아보기** 옵션을 탭하여 로컬 파일 시스템에서 업로드합니다.
   * **지우기**&#x200B;를 탭하거나 클릭하여 현재 선택한 이미지를 선택 취소합니다.
   * **편집**&#x200B;을 탭하거나 클릭하여 [자산 편집기에서 자산](https://helpx.adobe.com/experience-manager/6-3/assets/using/managing-assets-touch-ui.html#main-pars_title_19)의 변환을 관리합니다.

* **이미지가 장식용임**  - 보조 기술에 의해 이미지가 무시되어야 하므로 대체 텍스트가 필요 없는지 확인합니다. 이것은 장식 이미지만 적용됩니다.
* **대체 텍스트**  - 시각 장애가 있는 독자를 위한 이미지의 의미 또는 기능의 텍스트 대체 요소입니다.
* **링크**
   * 이미지를 다른 리소스에 연결합니다.
   * 선택 대화 상자를 사용하여 다른 AEM 리소스에 연결합니다.
   * AEM 리소스에 연결하지 않을 경우 절대 URL을 입력합니다. 비솔루션 URL은 AEM을 기준으로 해석됩니다.

* **캡션**  - 이미지 아래에 표시되는 이미지에 대한 추가 정보는 기본값이 됩니다.
* **캡션을 팝업으로 표시**  - 이 확인란을 선택하면 캡션이 이미지 아래에 표시되지 않고 이미지를 마우스로 가리키면 일부 브라우저에서 표시하는 팝업입니다.

## 편집 대화 상자 {#edit-dialog}

편집 대화 상자에서는 컨텐츠 작성자가 이미지를 자르거나, 론치 맵을 수정하고, 확대/축소할 수 있습니다.

![](/help/assets/chlimage_1-8.png)

* 자르기 시작

   ![](/help/assets/chlimage_1-9.png)

   이 옵션을 선택하면 사전 정의된 자르기 비율에 대한 드롭다운이 열립니다.

   * 직접 자르기를 정의하려면 **자유 손** 옵션을 선택합니다.
   * **자르기 제거** 옵션을 선택하여 원래 자산을 표시합니다.

   자르기 옵션을 선택하면 파란색 핸들을 사용하여 이미지에서 자르기 크기를 지정합니다.

   ![](/help/assets/chlimage_1-10.png)

* 오른쪽으로 회전

   ![](/help/assets/chlimage_1-11.png)

   이미지 90°을 오른쪽(시계 방향)으로 회전하려면 이 옵션을 사용합니다.

* 맵 시작

   ![](/help/assets/chlimage_1-12.png)

   이 옵션을 사용하여 이미지에 론치 맵을 적용합니다. 이 옵션을 선택하면 사용자가 맵의 모양을 선택할 수 있는 새 창이 열립니다.

   * **사각형 맵 추가**
   * **순환 맵 추가**
   * **다각형 맵 추가**

      * 기본적으로 삼각형 맵을 추가합니다. 셰이프의 선을 두 번 클릭하여 새 측면에 파란색 크기 조정 핸들을 새로 추가합니다.

   맵 모양을 선택하면 크기 조정을 허용하는 이미지에 겹쳐집니다. 파란색 크기 조정 핸들을 끌어다 놓아 모양을 조정합니다.

   ![](/help/assets/chlimage_1-13.png)

   론치 맵의 크기를 조정한 후 해당 아이콘을 클릭하여 부동 도구 모음을 열어 링크의 경로를 정의합니다.

   * **경로**
      * AEM에서 경로를 선택하려면 경로 선택기 옵션을 사용합니다
      * 경로가 AEM에 없는 경우에는 절대 URL을 사용하십시오. 절대 경로가 아닌 경로는 AEM을 기준으로 해석됩니다.

      * **대체**
텍스트경로 대상에 대한 대체 설명입니다
      * **타겟**
         * **동일한 탭**
         * **새 탭**
         * **상위 프레임**
         * **상위 프레임**

   파란색 확인 표시를 탭하거나 클릭하여 저장하고, 취소할 검은색 x를 클릭하고 빨간색 휴지통으로 맵을 삭제할 수 있습니다.

   ![](/help/assets/chlimage_1-14.png)

* 확대/축소 재설정

   ![](/help/assets/chlimage_1-15.png)

   이미지가 이미 확대/축소된 경우 이 옵션을 사용하여 확대/축소 수준을 재설정합니다.

* 확대/축소 슬라이더 열기

   ![](/help/assets/chlimage_1-16.png)

   이 옵션을 사용하여 슬라이더를 표시하여 이미지의 확대/축소 수준을 제어합니다.

   ![](/help/assets/chlimage_1-17.png)

즉석 편집기를 사용하여 이미지를 수정할 수도 있습니다. 공간 제한 때문에 기본적인 옵션만 온라인으로 사용할 수 있습니다. 전체 편집 옵션의 경우 전체 화면 모드를 사용합니다.

![](/help/assets/chlimage_1-18.png)

>[!NOTE]
>
>GIF 이미지에는 이미지 편집 작업(자르기, 뒤집기, 회전)이 지원되지 않습니다. 편집 모드에서 GIF로 수행된 모든 변경 사항은 지속되지 않습니다.

## 디자인 대화 상자 {#design-dialog}

디자인 대화 상자에서는 템플릿 작성자가 이 구성 요소를 사용할 때 컨텐츠 작성자가 가지고 있는 자르기, 업로드 및 회전을 정의할 수 있습니다.

### 기본 {#main}

**주** 탭에서 이미지에 가장 적절한 너비를 목록에서 자동으로 로드할 수 있도록 허용되는 너비 목록을 픽셀 단위로 정의할 수 있습니다.

![](/help/assets/chlimage_1-51.png)

추가 단추를 탭하거나 클릭하여 다른 크기를 추가합니다.

* 탭 핸들을 사용하여 크기 순서를 다시 정렬합니다.
* 삭제 아이콘을 사용하여 너비를 제거합니다.

기본적으로 이미지 로드가 표시될 때까지 지연됩니다. 페이지 로드 시 이미지를 로드하려면 **레이지 로드 비활성화** 옵션을 선택합니다.

### 기능 {#features}

**기능** 탭에서 업로드 옵션, 방향 및 자르기 옵션을 포함한 구성 요소를 사용할 때 컨텐츠 작성자가 사용할 수 있는 옵션을 정의할 수 있습니다.

* 소스

   ![](/help/assets/chlimage_1-19.png)

   컨텐츠 작성자가 로컬 컴퓨터의 이미지를 업로드할 수 있도록 하려면 **파일 시스템에서 자산 업로드 허용 옵션을 선택합니다.** 컨텐츠 작성자가 AEM에서 자산만 선택하도록 하려면 이 옵션을 선택 취소합니다.

* 방향

   ![](/help/assets/chlimage_1-20.png)

   * **회전**  - 이 옵션을 사용하여 컨텐츠 작성자가 오른쪽으로  **회전 옵션을 사용할 수** 있습니다.
   * ****
뒤집기이 옵션을 사용하여 컨텐츠 작성자가 
**수평** 대칭 이동 및  **수직** 대칭 이동 옵션.
   >[!CAUTION]
   >
   >기본적으로 **Flip** 옵션이 비활성화됩니다. 이 기능을 활성화하면 이미지 구성 요소의 편집 대화 상자에 **세로로 뒤집기** 및 **가로로 뒤집기** 단추가 표시되지만, 이 기능은 현재 AEM에서 지원하지 않으며, 이러한 옵션을 사용하여 변경한 사항은 유지되지 않습니다.

* 자르기

   ![](/help/assets/chlimage_1-21.png)

   컨텐츠 작성자가 편집 대화 상자의 구성 요소에서 이미지를 자르도록 하려면 **자르기 허용** 옵션을 선택합니다.
   * 사전 정의된 자르기 종횡비를 추가하려면 **추가**&#x200B;를 클릭하십시오.
   * **자르기 시작** 드롭다운에 표시되는 수사적 이름을 입력합니다.
   * 종횡비의 숫자 비율을 입력합니다.
   * 드래그 핸들을 사용하여 종횡비의 순서를 다시 정렬합니다
   * 종횡비를 삭제하려면 휴지통 아이콘을 사용하십시오.

   >[!CAUTION]
   >
   >AEM에서 자르기 종횡비는 **height/width**&#x200B;로 정의됩니다. 이것은 종래의 폭/높이 정의와 다르며, 레거시 호환성을 위해 수행됩니다. 비율이 비율 자체가 아니라 UI에 이름이 표시되므로 콘텐츠 작성자는 명확한 이름을 제공하면 차이를 알지 못합니다.

## 기술 세부 정보 {#technical-details}

이미지 구성 요소 [에 대한 최신 기술 설명서는 GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/image/v1/image)에 있습니다.

전체 코어 구성 요소 프로젝트는 GitHub에서 다운로드할 수 있습니다.

코어 구성 요소 개발에 대한 자세한 내용은 [코어 구성 요소 개발자 설명서](/help/developing/overview.md)에서 확인할 수 있습니다.

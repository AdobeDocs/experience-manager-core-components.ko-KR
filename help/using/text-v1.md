---
title: 텍스트 구성 요소 (v 1)
seo-title: 텍스트 구성 요소 (v 1)
description: 'null'
seo-description: 텍스트 구성 요소는 즉석 편집을 특징으로 하는 리치 텍스트 편집 및 구성 구성 요소입니다.
uuid: b 787 ebac-fa 85-416 a-b 96 b -9 d 2 ee 85428 ec
content-type: 참조
products: sg_ Experiencemanager/Corecomponents-new
discoiquuid: d 5 e 37 dc 7-dfd 4-4 a 44-89 b 6-c 15651472 c 43
disttype: dist5
gnavtheme: 밝음
groupsectionnavitems: 아니오
hidemerchandisingbar: 상속
hidepromocomponent: 상속
modalsize: 426x240
noindex: 'true'
index: n
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# 텍스트 구성 요소 (v 1){#text-component-v}

텍스트 구성 요소는 즉석 편집을 특징으로 하는 리치 텍스트 편집 및 구성 구성 요소입니다.

## 사용량 {#usage}

텍스트 구성 요소는 전체 화면 포맷뿐만 아니라 간단한 인라인 편집기에서 손쉽게 텍스트를 편집할 수 있는 강력한 리치 텍스트 편집기를 제공합니다.

[편집 대화 상자에는](text-v1.md#main-pars_title) 전체 화면 편집 대화 상자에서 사용할 수 있는 전체 기능을 사용하여 제한된 옵션이 포함된 인라인 편집이 포함되어 있습니다. [디자인 대화 상자를](text-v1.md#main-pars_title_1995166862)사용하면 컨텐츠 작성자용 템플릿에 대해 머리글, 특수 문자 및 단락 스타일과 같은 텍스트 서식 지정 옵션을 구성할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

이 문서에서는 원래 AEM 6.3 이 있는 핵심 구성 요소의 릴리스 1.0.0에 도입된 텍스트 구성 요소의 v 1에 대해 설명합니다.

다음 표에는 텍스트 구성 요소의 v 1 호환성이 나와 있습니다.

| AEM 버전 | 텍스트 구성 요소 v 1 |
|--- |--- |
| 6.3 | 호환 가능 |
| 6.4 | 호환 가능 |

>[!CAUTION]
>
>이 문서에서는 텍스트 구성 요소의 v 1를 설명합니다.
>
>텍스트 구성 요소의 현재 버전에 대한 자세한 내용은 [텍스트 구성 요소](text.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

[다음은 We. Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html)에서 가져온 샘플입니다.

### 스크린샷 {#screenshot}

![](assets/chlimage_1-27.png)

### HTML {#html}

```
<div class="cmp cmp-text aem-GridColumn aem-GridColumn--default--12">
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer porttitor ante a tortor volutpat maximus. Donec eu porta eros. Aenean sit amet eleifend arcu, eu vestibulum magna. Fusce eget nisi tincidunt, tristique felis quis, tincidunt est. Aliquam consequat aliquam quam non eleifend. Phasellus ut magna luctus, aliquam risus eget, fermentum augue. Aliquam lobortis accumsan magna, quis efficitur enim dictum eu. Pellentesque iaculis felis eget felis commodo, non euismod dolor euismod. Quisque nec arcu rutrum, mollis tortor non, sollicitudin odio. Sed dictum nulla mauris, eu pretium dui vulputate a. Maecenas lacus massa, egestas vitae tincidunt eu, interdum et magna. Lorem ipsum dolor sit amet, consectetur adipiscing elit. In eleifend ex lacus, in consectetur nunc interdum et. Donec interdum mi vitae dolor pretium mattis. In quis arcu sapien. Phasellus at metus vitae nisi tincidunt varius.<br />
</p>
</div>
```

### JSON {#json}

```
"text": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "text": "<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer porttitor ante a tortor volutpat maximus. Donec eu porta eros. Aenean sit amet eleifend arcu, eu vestibulum magna. Fusce eget nisi tincidunt, tristique felis quis, tincidunt est. Aliquam consequat aliquam quam non eleifend. Phasellus ut magna luctus, aliquam risus eget, fermentum augue. Aliquam lobortis accumsan magna, quis efficitur enim dictum eu. Pellentesque iaculis felis eget felis commodo, non euismod dolor euismod. Quisque nec arcu rutrum, mollis tortor non, sollicitudin odio. Sed dictum nulla mauris, eu pretium dui vulputate a. Maecenas lacus massa, egestas vitae tincidunt eu, interdum et magna. Lorem ipsum dolor sit amet, consectetur adipiscing elit. In eleifend ex lacus, in consectetur nunc interdum et. Donec interdum mi vitae dolor pretium mattis. In quis arcu sapien. Phasellus at metus vitae nisi tincidunt varius.</p>\n",
              "richText": true,
              ":type": "weretail/components/content/text"
            }
```

>[!NOTE]
>
>핵심 구성 요소에서 JSON 내보내기를 사용하려면 핵심 구성 요소의 릴리스 1.1.0 이 필요합니다. 자세한 내용은 [핵심 구성 요소 v 1](versions.md#main-pars_title_236368006) 의 호환성 정보를 참조하십시오.

## 편집 대화 상자 {#edit-dialog}

편집 대화 상자는 사용자가 텍스트를 구성할 것으로 예상되는 표준 리치 텍스트 서식 지정 도구를 제공합니다.

![](assets/chlimage_1-52.png)

* 굵게

   ![](assets/chlimage_1-53.png)

   선택한 텍스트에 굵은 서식을 적용하거나 커서 이후에 입력한 텍스트를 굵게 지정하는 데 사용됩니다.

   **Ctrl + B** 는 키보드 단축키로 사용할 수 있습니다.

* 기울임체

   ![](assets/chlimage_1-54.png)

   선택한 텍스트에 기울임꼴 서식을 적용하거나 커서 이후에 입력한 텍스트를 기울임꼴로 만드는 데 사용됩니다.

   **Ctrl + I** 키보드 단축키로 사용할 수 있습니다.

* 밑줄

   ![](assets/chlimage_1-55.png)

   선택한 텍스트에 밑줄이 그어진 서식을 적용하거나 커서 이후에 입력한 텍스트에 밑줄 서식을 적용하는 데 사용됩니다.

   **Ctrl + U** 는 키보드 단축키로 사용할 수 있습니다.

* 아래 첨자

   ![](assets/chlimage_1-56.png)

   커서 다음에 입력한 텍스트나 텍스트를 아래 첨자로 지정하는 데 사용됩니다.

* 위 첨자

   ![](assets/chlimage_1-57.png)

   커서 다음에 선택된 텍스트나 텍스트를 superscript로 지정하는 데 사용됩니다.

* 텍스트로 붙여넣기

   ![](assets/chlimage_1-58.png)

   복사된 텍스트를 서식이 없는 일반 텍스트로 붙여넣습니다.

   이 옵션을 선택하면 텍스트를 텍스트에 삽입하기 전에 미리 보기로 서식이 없는 일반 텍스트로 붙여넣을 수 있는 창이 열립니다. 확인 표시를 탭하거나 클릭하여 수락하고 X를 탭하거나 클릭하여 취소합니다.

   ![](assets/chlimage_1-59.png)

* Word에서 붙여넣기

   ![](assets/chlimage_1-60.png)

   이 옵션을 선택하면 텍스트를 텍스트에 삽입하기 전에 미리 보기로 유지하여 텍스트를 붙여넣을 수 있는 창이 열립니다. 확인 표시를 탭하거나 클릭하여 수락하고 X를 탭하거나 클릭하여 취소합니다.

   ![](assets/chlimage_1-61.png)

* 하이퍼링크

   ![](assets/chlimage_1-62.png)

   이 옵션을 사용하여 선택한 텍스트를 하이퍼링크로 변환하거나 이미 정의된 링크를 수정합니다. 이 옵션은 텍스트가 이미 선택되어 있는 경우에만 활성화되며 링크를 설정하기 위한 추가 옵션이 있는 창을 엽니다.

   ![](assets/chlimage_1-63.png)

   * 위치 입력

      * 선택 열기 대화 상자를 사용하여 AEM에서 경로를 선택합니다.
      * 링크가 AEM 내에 없는 경우 절대 URL (절대 경로는 AEM와 관련하여 해석됨) 를 입력합니다.
   * 링크에 대한 대체 설명 텍스트를 입력합니다.
   * 링크 동작 선택

      * 타겟
      * 동일한 탭
      * 새 탭
      * 상위 프레임
      * 상위 프레임
   확인 표시를 탭하거나 클릭하여 링크를 적용하거나 X를 클릭하여 취소합니다.

* 연결 해제

   ![](assets/chlimage_1-64.png)

   이 옵션을 사용하여 선택한 텍스트에 이미 적용된 링크를 제거합니다. 이 옵션은 링크가 이미 선택된 경우에만 활성화됩니다.

* 찾기

   ![](assets/chlimage_1-65.png)

   이 옵션을 사용하여 지정된 텍스트 문자열이 발생한 텍스트를 검색합니다. 이 옵션을 선택하면 검색 옵션을 지정하기 위한 창이 열립니다.

   ![](assets/chlimage_1-66.png)

   검색할 텍스트를 입력하고 **검색을** 탭하거나 클릭하여 검색을 시작합니다. 취소하려면 X를 탭하거나 클릭합니다.

   사례에 따라 정확히 일치하려면 검색 시작 전에 대/소문자 **일치** 옵션을 선택합니다.

   일치하는 항목이 발견되면 강조 표시되고 검색 대화 상자가 흐리게 표시됩니다. 희미하게 표시되는 대화 상자에서 **찾기** 단추를 다시 탭하거나 클릭하여 다음 항목을 검색합니다.

   ![](assets/chlimage_1-67.png)

   추가 발생이 발견되지 않으면 메시지가 표시되고 텍스트 시작 부분에서 검색이 다시 시작됩니다.

   ![](assets/chlimage_1-68.png)

* 바꾸기

   ![](assets/chlimage_1-69.png)

   이 옵션을 사용하여 지정된 텍스트 문자열이 발생한 텍스트를 검색하고 일치 항목을 다른 문자열로 바꿉니다. 이 옵션을 선택하면 검색 및 바꾸기 옵션을 지정하는 창이 열립니다.

   ![](assets/chlimage_1-70.png)

   검색할 텍스트를 입력하고 바꿀 텍스트를 입력합니다.

   검색을 시작하려면 **검색을** 탭하거나 클릭합니다. 취소하려면 X를 클릭하거나 탭합니다.

   사례에 따라 정확히 일치하려면 검색 시작 전에 대/소문자 **일치** 옵션을 선택합니다.

   일치하는 항목이 발견되면 강조 표시되고 검색 대화 상자가 흐리게 표시됩니다. 흐리게 표시된 대화 상자에서 **찾기** 단추를 다시 클릭하여 다음 항목을 검색하거나 **대체** 단추를 선택하여 강조 표시된 텍스트를 대체합니다. [ **바꾸기** ] 단추는 일치가 이루어진 후에만 활성화됩니다.

   모든 텍스트를 **한 번에 바꾸려면 모두** 바꾸기를 선택합니다.

* 왼쪽으로 텍스트 정렬

   ![](assets/chlimage_1-71.png)

   텍스트를 왼쪽 여백에 정렬하는 데 사용됩니다.

* 텍스트를 가운데로

   ![](assets/chlimage_1-72.png)

   텍스트를 가운데에 정렬하는 데 사용됩니다.

* 오른쪽으로 텍스트 정렬

   ![](assets/chlimage_1-73.png)

   텍스트를 오른쪽 여백에 정렬하는 데 사용됩니다.

* 글머리 기호

   ![](assets/chlimage_1-74.png)

   선택된 텍스트를 글머리 기호 목록으로 서식을 지정하거나 커서 뒤에 글머리 기호 목록 삽입을 시작하는 데 사용됩니다.

   글머리 기호 목록을 종료하려면 **글머리 기호** 단추를 다시 누르거나 클릭하거나 두 개의 캐리지 리턴을 입력합니다.

* numbered

   ![](assets/chlimage_1-75.png)

   선택한 텍스트의 서식을 번호 매기기 목록으로 지정하거나 커서 뒤에 번호 매기기 목록을 삽입하는 데 사용됩니다.

   번호 매기기 목록을 종료하려면 **번호 매기기 단추를** 다시 누르거나 클릭하거나 두 개의 캐리지 리턴을 입력합니다.

* 내어쓰기

   ![](assets/chlimage_1-76.png)

   선택한 텍스트 또는 커서 이후에 입력한 텍스트의 들여쓰기 수준을 줄이는 데 사용됩니다.

   선택한 텍스트 또는 커서 위치가 이미 들여쓰기된 경우에만 활성 상태입니다.

* 들여쓰기

   ![](assets/chlimage_1-77.png)

   커서 이후에 입력한 텍스트나 텍스트의 들여쓰기 수준을 높이는 데 사용됩니다.

* 표

   ![](assets/chlimage_1-78.png)

   텍스트를 텍스트에 삽입하는 데 사용됩니다. 이 옵션을 선택하면 표의 세부 사항을 지정하는 창이 열립니다.

   ![](assets/chlimage_1-79.png)

   * **열** - 표의 열 수 (필수)
   * **행** - 표의 행 수 (필수)
   * **너비** - 표의 폭
   * **높이** - 표의 높이
   * **셀 패딩**- 셀 컨텐츠 주위의 공백
   * **셀 간격** - 셀 사이의 공백
   * **테두리** - 표의 테두리 선 두께
   * if the header of the table:

      * 첫 번째 행을 사용해야 합니다.
      * 첫 번째 열을 사용해야 합니다.
      * 첫 번째 행과 첫 번째 열을 사용해야 합니다.
      * 또는 헤더를 사용하지 않아야 합니다.
   * **캡션** - 표의 캡션


* 맞춤법 검사

   ![](assets/chlimage_1-80.png)

   텍스트 컨텐츠의 맞춤법을 확인하는 데 사용됩니다. 잘못된 철자는 빨간색 선으로 밑줄로 표시됩니다.

* 특수 문자

   ![](assets/chlimage_1-81.png)

   텍스트에 특수 문자를 삽입하는 데 사용됩니다. 이 옵션을 선택하면 사용 가능한 문자가 표시되는 창이 열립니다.

   ![](assets/chlimage_1-82.png)

   원하는 문자를 탭하거나 클릭하여 커서를 커서 다음에 삽입합니다. 여러 문자를 삽입할 수 있습니다. X를 탭하거나 클릭하여 선택 창을 닫습니다.

* 소스 편집

   ![](assets/chlimage_1-83.png)

   텍스트의 HTML 소스를 보고 수정하는 데 사용됩니다.

   **소스 편집** 아이콘을 탭하거나 클릭하여 서식이 지정된 보기에서 텍스트 컨텐츠를 변경하여 원시 HTML를 봅니다. 이 모드에서는 다른 모든 서식 옵션이 비활성화됩니다. **소스 편집** 아이콘을 다시 탭하거나 클릭하여 서식이 지정된 보기로 돌아갑니다.

   >[!CAUTION]
   >
   >Raw HTML에 대한 액세스 권한이 항상 그렇듯이 **소스 편집** 옵션을 사용할 때는 주의해야 합니다.
   >
   >
   >**소스 편집을** 통해 입력한 HTML는 XSS 위험에 대해 스캔되며 삽입된 스크립트는 제거되고 결과 페이지에 나타나지 않습니다. **그러나 소스 편집에서** 입력한 잘못된 형식의 HTML는 페이지의 템플릿을 끊어서 예기치 않은 서식 지정 또는 결과 페이지를 사용할 수 없게 만들 수 있습니다.

* 단락 형식

   ![](assets/chlimage_1-84.png)

   선택한 텍스트 또는 커서 다음에 삽입된 텍스트에 단락 서식을 적용하는 데 사용됩니다. 이 옵션을 선택하면 단락 형식이 선택된 드롭다운이 열립니다.

   ![](assets/chlimage_1-85.png)

텍스트 구성 요소는 인라인 편집도 가능하지만 공백 제한 때문에 모든 서식 옵션이 인라인 사용 가능하지는 않습니다. 모든 옵션을 보려면 전체 화면 모드로 전환합니다.

![](assets/chlimage_1-86.png)

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 사용하여 컨텐츠 작성자가 사용할 수 있는 텍스트 서식 지정 옵션을 정의할 수 있습니다.

### 기능 {#features}

![](assets/chlimage_1-28.png)

다음 기능은 구성 요소에 대해 활성화하거나 비활성화할 수 있습니다.

* 일반 텍스트 붙여넣기
* Word에서 이전
* 찾기 및 바꾸기
* 맞춤법 검사기
* 소스 편집

### 형식 지정 {#formatting}

![](assets/chlimage_1-29.png)

다음 서식 옵션은 구성 요소에 대해 활성화하거나 비활성화할 수 있습니다.

* 표
* 목록
* 정렬
* 굵게, 기울임꼴, 밑줄
* 링크
* sub/superscript

### 단락 스타일 {#paragraph-styles}

![](assets/chlimage_1-30.png)

구성 요소에 대해 단락 스타일을 활성화하거나 비활성화할 수 있습니다. 활성화하면 허용되는 형식을 정의할 수 있습니다.

* **추가** 단추를 탭하거나 클릭하여 새 스타일을 삽입합니다.
* 스타일 코드와 편집 대화 상자에 표시할 설명을 입력합니다.
* 스타일을 제거하려면 **삭제** 단추를 탭하거나 클릭합니다.
* 형식 순서를 재배치하려면 핸들을 탭하거나 클릭하고 드래그합니다.

### 특수 문자 {#special-characters}

![](assets/chlimage_1-31.png)

특수 문자를 삽입하는 옵션은 구성 요소에 대해 활성화하거나 비활성화할 수 있습니다. 활성화되면 허용되는 문자를 정의할 수 있습니다.

* **추가** 단추를 탭하거나 클릭하여 새 문자를 삽입합니다.
* 편집 대화 상자에 표시할 문자와 설명의 HTML 코드를 입력합니다.
* 문자를 제거하려면 [ **삭제** ] 단추를 탭하거나 클릭합니다.
* 문자 순서를 재배치하려면 핸들을 누르거나 클릭하고 핸들을 드래그합니다.

## 기술 세부 정보 {#technical-details}

텍스트 구성 요소에 [대한 최신 기술 설명서는 Github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v1/text)에서 찾을 수 있습니다.

Github에서 전체 핵심 구성 요소 프로젝트를 다운로드할 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서를](developing.md)참조하십시오.

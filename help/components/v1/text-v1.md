---
title: 텍스트 구성 요소 (v1)
description: 텍스트 구성 요소는 바로 편집 기능이 있는 서식 있는 텍스트 편집 및 작성 구성 요소입니다.
index: n
role: Architect, Developer, Admin, User
exl-id: c9fe3052-a33d-412e-9456-52c9a0cea292
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '1657'
ht-degree: 100%

---

# 텍스트 구성 요소 (v1) {#text-component-v}

텍스트 구성 요소는 바로 편집 기능이 있는 서식 있는 텍스트 편집 및 작성 구성 요소입니다.

## 사용량 {#usage}

텍스트 구성 요소는 인라인 편집기와 전체 화면 포맷으로 간편한 텍스트 편집이 가능한 강력한 서식 있는 텍스트 편집기를 제공합니다.

[편집 대화 상자](#edit-dialog)에는 전체 화면 편집 대화 상자에서 전체 기능을 사용할 수 있고 제한된 옵션이 제공되는 인라인 편집 기능이 있습니다. [디자인 대화 상자](#design-dialog)를 통해 콘텐츠 작성자용 템플릿에서 텍스트 서식 옵션을 구성할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

이 문서에서는 AEM 6.3을 포함하는 핵심 구성 요소 릴리스 1.0.0과 함께 최초 도입된 텍스트 구성 요소 v1에 대해 설명합니다.

다음 표에서 텍스트 구성 요소 v1의 호환성을 확인할 수 있습니다.

| AEM 버전 | 텍스트 구성 요소 v1 |
|--- |--- |
| 6.3 | 호환 가능 |
| 6.4 | 호환 가능 |

>[!CAUTION]
>
>이 문서에서는 텍스트 구성 요소 v1에 대해 설명합니다.
>
>현재 버전의 텍스트 구성 요소에 대한 자세한 내용은 [텍스트 구성 요소](/help/components/text.md) 문서를 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

다음은 [We.Retail](https://helpx.adobe.com/kr/experience-manager/6-4/sites/developing/using/we-retail.html)에서 얻은 샘플입니다.

### 스크린샷 {#screenshot}

![](/help/assets/chlimage_1-27.png)

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
>핵심 구성 요소에서 JSON을 내보내는 데 핵심 구성 요소 릴리스 1.1.0이 필요합니다. 자세한 내용은 [핵심 구성 요소 v1에 대한 호환성 정보](/help/versions.md)를 참조하십시오.

## 편집 대화 상자 {#edit-dialog}

편집 대화 상자는 사용자가 텍스트를 작성할 서식 있는 표준 텍스트 서식 도구를 제공합니다.

![](/help/assets/chlimage_1-52.png)

* 볼드체

   ![](/help/assets/chlimage_1-53.png)

   선택한 텍스트에 볼드체 서식 지정을 적용하거나 커서 다음에 입력한 텍스트를 볼드체로 서식 지정하는 데 사용됩니다,

   키보드 단축키로 **Ctrl+B**&#x200B;를 사용할 수 있습니다.

* 이탤릭체

   ![](/help/assets/chlimage_1-54.png)

   선택한 텍스트에 이탤릭체 서식 지정을 적용하거나 커서 다음에 입력한 텍스트를 이탤릭체로 서식 지정하는 데 사용됩니다,

   키보드 단축키로 **Ctrl+I**&#x200B;를 사용할 수 있습니다.

* 밑줄

   ![](/help/assets/chlimage_1-55.png)

   선택한 텍스트에 밑줄 서식 지정을 적용하거나 커서 다음에 입력한 텍스트를 밑줄로 서식 지정하는 데 사용됩니다,

   키보드 단축키로 **Ctrl+U**&#x200B;를 사용할 수 있습니다.

* 아래 첨자

   ![](/help/assets/chlimage_1-56.png)

   선택한 텍스트나 커서 다음에 입력한 텍스트를 아래 첨자로 서식 지정하는 데 사용됩니다,

* 위 첨자

   ![](/help/assets/chlimage_1-57.png)

   선택한 텍스트나 커서 다음에 입력한 텍스트를 위 첨자로 서식 지정하는 데 사용됩니다,

* 텍스트로 붙여넣기

   ![](/help/assets/chlimage_1-58.png)

   서식 지정 없이 복사한 텍스트를 일반 텍스트로 붙여넣습니다.

   이 옵션을 선택하면 서식 지정 없이 텍스트를 일반 텍스트로 붙여넣을 수 있는 창이 텍스트에 삽입되기 전 미리보기로 열립니다. 확인 표시를 탭하거나 클릭하여 수락하고 x를 탭하거나 클릭하여 취소합니다.

   ![](/help/assets/chlimage_1-59.png)

* Word에서 붙여넣기

   ![](/help/assets/chlimage_1-60.png)

   이 옵션을 선택하면 서식 지정을 유지하면서 텍스트를 일반 텍스트로 붙여넣을 수 있는 창이 텍스트에 삽입되기 전 미리보기로 열립니다. 확인 표시를 탭하거나 클릭하여 수락하고 x를 탭하거나 클릭하여 취소합니다.

   ![](/help/assets/chlimage_1-61.png)

* 하이퍼링크

   ![](/help/assets/chlimage_1-62.png)

   이 옵션을 사용하여 선택한 텍스트를 하이퍼링크로 변환하거나 이미 정의된 링크를 수정합니다. 이 옵션은 텍스트가 이미 선택되고 링크를 설정하는 추가 옵션으로 창을 여는 경우에만 활성화됩니다.

   ![](/help/assets/chlimage_1-63.png)

   * 위치 입력

      * 선택 열기 대화 상자를 통해 AEM의 경로를 선택합니다.
      * 링크가 AEM 내에 없는 경우 절대 URL을 입력합니다(절대가 아닌 경로는 AEM의 상대로 해석됨).
   * 링크에 대한 대체 설명 텍스트 입력
   * 링크 비헤이비어 선택

      * 대상
      * 동일한 탭
      * 새 탭
      * 상위 프레임
      * 맨 위 프레임

   확인 표시를 탭하거나 클릭하여 링크를 적용하거나 x를 탭하거나 클릭하여 취소합니다.

* 연결 해제

   ![](/help/assets/chlimage_1-64.png)

   이 옵션을 사용하여 선택한 텍스트에 이미 적용된 링크를 제거합니다. 이 옵션은 링크가 이미 선택된 경우에만 활성화됩니다.

* 찾기

   ![](/help/assets/chlimage_1-65.png)

   지정된 텍스트 문자열의 발생 횟수를 알아보려면 이 옵션을 사용하여 텍스트를 검색합니다. 이 옵션을 선택하면 검색 옵션을 지정하는 창이 열립니다.

   ![](/help/assets/chlimage_1-66.png)

   검색할 텍스트를 입력하고 **찾기**&#x200B;를 탭하거나 클릭하여 검색을 시작합니다. x를 탭하거나 클릭하여 취소합니다.

   사례에 따라 정확하게 일치시키려면 **사례 일치** 옵션을 선택한 다음 검색을 시작합니다.

   일치가 발견되면 강조 표시되고 검색 대화 상자가 흐리게 표시됩니다. 흐리게 표시된 대화 상자에서 **찾기** 버튼을 다시 탭하거나 클릭하여 다음 발생 횟수를 검색합니다.

   ![](/help/assets/chlimage_1-67.png)

   추가 발생 항목이 없는 경우 메시지가 표시되고 텍스트 시작부터 검색이 다시 시작됩니다.

   ![](/help/assets/chlimage_1-68.png)

* 바꾸기

   ![](/help/assets/chlimage_1-69.png)

   지정된 텍스트 문자열의 발생 횟수를 알아보려면 이 옵션을 사용하여 텍스트를 검색하고 일치하는 문자열을 다른 문자열로 대체합니다. 이 옵션을 선택하면 검색 옵션을 지정하는 창이 열리고 옵션을 대체합니다.

   ![](/help/assets/chlimage_1-70.png)

   검색할 텍스트와 대체해야 할 텍스트를 입력합니다.

   **찾기**&#x200B;를 탭하거나 클릭하여 검색을 시작합니다. x를 클릭하거나 탭하여 취소합니다.

   사례에 따라 정확하게 일치시키려면 **사례 일치** 옵션을 선택한 다음 검색을 시작합니다.

   일치가 발견되면 강조 표시되고 검색 대화 상자가 흐리게 표시됩니다. 흐리게 표시된 대화 상자에서 **찾기** 버튼을 다시 클릭하여 다음 발생 항목을 검색하거나, **바꾸기** 버튼을 선택하여 강조 표시 및 일치된 텍스트를 대체합니다. 일치하는 항목이 있는 경우에만 **바꾸기** 버튼이 활성화됩니다.

   **모두 바꾸기**&#x200B;를 선택하여 한 번에 모든 발생 항목을 바꿉니다.

* 왼쪽으로 텍스트 정렬

   ![](/help/assets/chlimage_1-71.png)

   왼쪽 여백으로 텍스트를 정렬하는 데 사용됩니다.

* 텍스트를 가운데로

   ![](/help/assets/chlimage_1-72.png)

   가운데로 텍스트를 정렬하는 데 사용됩니다.

* 오른쪽으로 텍스트 정렬

   ![](/help/assets/chlimage_1-73.png)

   오른쪽 여백으로 텍스트를 정렬하는 데 사용됩니다.

* 글머리 기호

   ![](/help/assets/chlimage_1-74.png)

   선택한 텍스트 서식을 글머리 기호 목록으로 지정하거나 커서 다음에 글머리 기호 목록을 삽입하는 데 사용됩니다.

   글머리 기호 목록을 종료하려면 **글머리 기호** 버튼을 다시 탭 또는 클릭하거나 캐리지 리턴을 2번 입력합니다.

* 번호 매기기

   ![](/help/assets/chlimage_1-75.png)

   선택한 텍스트 서식을 번호 매기기 목록으로 지정하거나 커서 다음에 번호 매기기 목록을 삽입하는 데 사용됩니다.

   번호 매기기 목록을 종료하려면 **번호 매기기** 버튼을 다시 탭 또는 클릭하거나 캐리지 리턴을 2번 입력합니다.

* 내어쓰기

   ![](/help/assets/chlimage_1-76.png)

   선택한 텍스트나 커서 다음에 입력한 텍스트의 들여쓰기 레벨을 낮추는 데 사용됩니다,

   선택한 텍스트나 커서의 위치가 이미 들여 쓴 경우에만 활성화됩니다.

* 들여쓰기

   ![](/help/assets/chlimage_1-77.png)

   선택한 텍스트나 커서 다음에 입력한 텍스트의 들여쓰기 레벨을 높이는 데 사용됩니다,

* 표

   ![](/help/assets/chlimage_1-78.png)

   표를 텍스트에 삽입하는 데 사용됩니다. 이 옵션을 선택하면 표의 세부 정보를 지정하는 창이 열립니다.

   ![](/help/assets/chlimage_1-79.png)

   * **열** - 표의 열 수(필수)
   * **행** - 표의 행 수 (필수)
   * **폭** - 표의 폭
   * **높이** - 표의 높이
   * **셀 패딩** - 셀 내용 앞뒤 공백
   * **셀 간격** - 셀 간 간격
   * **테두리** - 표 테두리 라인 두께
   * 표 머리말의 경우:

      * 첫 번째 행을 사용해야 합니다.
      * 첫 번째 열을 사용해야 합니다.
      * 첫 번째 행과 첫 번째 열을 사용해야 합니다.
      * 또는 머리말을 사용해서는 안 됩니다.
   * **캡션** - 표의 캡션


* 맞춤법 검사

   ![](/help/assets/chlimage_1-80.png)

   텍스트 맞춤법을 검사하는 데 사용됩니다. 오자는 빨간색 점선으로 밑줄이 그어져 있습니다.

* 특수 문자

   ![](/help/assets/chlimage_1-81.png)

   특수 문자를 텍스트에 삽입하는 데 사용됩니다. 이 옵션을 선택하면 창이 열리고 사용할 수 있는 문자가 표시됩니다.

   ![](/help/assets/chlimage_1-82.png)

   원하는 문자를 탭하거나 클릭하여 커서 다음 텍스트에 삽입합니다. 여러 문자들을 삽입할 수 있습니다. x를 탭하거나 클릭하여 선택 창을 닫습니다.

* 소스 편집

   ![](/help/assets/chlimage_1-83.png)

   텍스트의 HTML 소스를 확인하고 수정하는 데 사용됩니다.

   원시 HTML을 보려면 **소스 편집** 아이콘을 탭하거나 클릭하여 서식이 지정된 보기에서 텍스트 콘텐츠를 변경합니다. 이 모드에서 다른 모든 서식 지정 옵션이 비활성화됩니다. 서식이 지정된 보기로 돌아가려면 **소스 편집** 아이콘을 다시 탭하거나 클릭합니다.

   >[!CAUTION]
   >
   >원시 HTML에 액세스하는 경우와 마찬가지로 **소스 편집** 옵션을 사용할 때 주의해야 합니다
   >
   >
   >XSS 위험이 있는 경우 **소스 편집**&#x200B;을 통해 입력된 HTML을 스캔합니다. 그리고 삽입한 스크립트를 제거하면 결과 페이지에 나타나지 않습니다. **소스 편집**&#x200B;을 통해 입력한 HTML의 형식이 잘못되어도 페이지용 템플릿이 깨질 수 있습니다. 그 결과 페이지가 예고 없이 서식 지정되거나 렌더링되어 사용할 수 없게 됩니다.

* 단락 형식

   ![](/help/assets/chlimage_1-84.png)

   선택한 텍스트이나 커서 다음에 삽입한 텍스트에 단락 형식을 적용하는 데 사용됩니다. 이 옵션을 선택하면 단락 형식이 선택된 위치에서 드롭다운이 열립니다.

   ![](/help/assets/chlimage_1-85.png)

텍스트 구성 요소는 또한 인라인으로 편집할 수 있지만, 서식 옵션은 공백이 제한되어 인라인으로 사용할 수 없습니다. 모든 옵션을 보려면 전체 화면 모드로 전환합니다.

![](/help/assets/chlimage_1-86.png)

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 통해 콘텐츠 작성자가 사용할 수 있는 텍스트 서식 옵션을 정의할 수 있습니다.

### 기능 {#features}

![](/help/assets/chlimage_1-28.png)

구성 요소에서 다음 기능을 활성화하거나 비활성화할 수 있습니다.

* 일반 텍스트 붙여넣기
* Word에서 붙여넣기
* 찾기 및 바꾸기
* 맞춤법 검사기
* 소스 편집

### 서식 {#formatting}

![](/help/assets/chlimage_1-29.png)

구성 요소에서 다음 서식 옵션을 활성화하거나 비활성화할 수 있습니다.

* 표
* 목록
* 정렬
* 볼드체, 이탤릭체, 밑줄
* 링크
* 아래 첨자/위 첨자

### 단락 스타일 {#paragraph-styles}

![](/help/assets/chlimage_1-30.png)

구성 요소에서 단락 스타일을 활성화하거나 비활성화할 수 있습니다. 활성화되면 허용된 포맷을 정의할 수 있습니다.

* **추가** 버튼을 탭하거나 클릭하여 새 스타일을 삽입합니다.
* 편집 대화 상자에 표시할 스타일 및 설명에 대한 코드를 입력합니다.
* 스타일 제거하려면 **삭제** 버튼을 탭하거나 클릭합니다.
* 포맷 순서를 재배열하려면 핸들을 탭하거나 클릭하여 드래그합니다.

### 특수 문자 {#special-characters}

![](/help/assets/chlimage_1-31.png)

구성 요소에서 특수 문자를 삽입하는 옵션을 활성화하거나 비활성화할 수 있습니다. 활성화되면 허용된 문자를 정의할 수 있습니다.

* **추가** 버튼을 탭하거나 클릭하여 새 문자를 삽입합니다.
* 편집 대화 상자에 표시할 문자 및 설명에 대한 HTML 코드를 입력합니다.
* 문자를 제거하려면 **삭제** 버튼을 탭하거나 클릭합니다.
* 문자 순서를 재배열하려면 핸들을 탭하거나 클릭하여 드래그합니다.

## 기술 세부 사항 {#technical-details}

텍스트 구성 요소에 대한 최신 기술 설명서는[ GitHub에서 확인할 수 있습니다](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v1/text).

GitHub에서 전체 핵심 구성 요소 프로젝트를 다운로드할 수 있습니다.

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

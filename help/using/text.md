---
title: 텍스트 구성 요소
seo-title: 텍스트 구성 요소
description: 텍스트 구성 요소는 즉석 편집을 특징으로 하는 리치 텍스트 편집 및 구성 구성 요소입니다.
seo-description: 텍스트 구성 요소는 즉석 편집을 특징으로 하는 리치 텍스트 편집 및 구성 구성 요소입니다.
uuid: 5 F 8 EEE 8 F -7317-4712-A 77 F-E 34 E 8 A 024187
contentOwner: 사용자
content-type: 참조
topic-tags: 핵심 구성 요소
discoiquuid: 9 A 290584-565 E -4392-999 C -999 EE 4 A 93 DA 1
translation-type: tm+mt
source-git-commit: eef608fb06001485aa2c2c0b574af412ed7f15a4

---


# 텍스트 구성 요소{#text-component}

핵심 구성 요소 텍스트 구성 요소는 즉석 편집을 특징으로 하는 리치 텍스트 편집 및 구성 구성 요소입니다.

## 사용량 {#usage}

텍스트 구성 요소는 전체 화면 포맷뿐만 아니라 간단한 인라인 편집기에서 손쉽게 텍스트를 편집할 수 있는 강력한 리치 텍스트 편집기를 제공합니다.

[편집 대화 상자에는](#edit-dialog) 전체 화면 편집 대화 상자에서 사용할 수 있는 전체 기능을 사용하여 제한된 옵션이 포함된 인라인 편집이 포함되어 있습니다. [디자인 대화 상자를](#design-dialog)사용하면 컨텐츠 작성자용 템플릿에 대해 머리글, 특수 문자 및 단락 스타일과 같은 텍스트 서식 지정 옵션을 구성할 수 있습니다.

## Version and Compatibility {#version-and-compatibility}

현재 버전의 텍스트 구성 요소는 2018 년 1 월에 핵심 구성 요소의 릴리스 2.0.0에서 처음 소개된 v 2 이며, 이 문서에는 설명되어 있습니다.

다음 표에서는 구성 요소의 지원되는 모든 버전, 구성 요소의 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서에 대한 링크를 제공합니다.

| 구성 요소 버전 | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|---|---|---|---|
| v2 | 호환 가능 | 호환 가능 | 호환 가능 |
| [v1](text-v1.md) | 호환 가능 | 호환 가능 | 호환 가능 |

For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

To experience the Text Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/text.html).

### Technical Details {#technical-details}

The latest technical documentation about the Text Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/text/v2/text).

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md).

## The Text Component and the Rich Text Editor {#the-text-component-and-the-rich-text-editor}

핵심 구성 요소 텍스트 구성 요소는 AEM 리치 텍스트 편집기 (RTE) 를 활용합니다. RTE는 컨텐츠 작성자에게 텍스트 컨텐츠를 편집할 수 있는 다양한 기능을 제공합니다. RTE는 구성이 매우 유연하며 다양한 옵션을 제공합니다. Further details about how the RTE can be configured can be found in the articles [Configure the Rich Text Editor](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/rich-text-editor.html) and [Configure the Rich Text Editor plug-ins](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/configure-rich-text-editor-plug-ins.html).

이 문서의 나머지 부분에서는 기본 RTE 구성이 있는 핵심 구성 요소 텍스트 구성 요소의 표준 구성을 설명합니다.

>[!NOTE]
>
>Only options enabled by [UI configurations of the RTE](https://chl-author-preview.corp.adobe.com/content/help/en/experience-manager/6-5/sites/administering/using/rich-text-editor.html) are available by in the Text Component.

## Edit Dialog {#edit-dialog}

편집 대화 상자는 사용자가 텍스트를 구성할 것으로 예상되는 표준 리치 텍스트 서식 지정 도구를 제공합니다.

![](assets/screen_shot_2018-01-11at143025.png)

### 굵게

![](assets/screen_shot_2018-01-11at125602.png)

선택한 텍스트에 굵은 서식을 적용하거나 커서 이후에 입력한 텍스트를 굵게 지정하는 데 사용됩니다.

**Ctrl + B** 는 키보드 단축키로 사용할 수 있습니다.

### 기울임체

![](assets/screen_shot_2018-01-11at125609.png)

선택한 텍스트에 기울임꼴 서식을 적용하거나 커서 이후에 입력한 텍스트를 기울임꼴로 만드는 데 사용됩니다.

**Ctrl + I** 키보드 단축키로 사용할 수 있습니다.

### 밑줄

![](assets/screen_shot_2018-01-11at125615.png)

선택한 텍스트에 밑줄이 그어진 서식을 적용하거나 커서 이후에 입력한 텍스트에 밑줄 서식을 적용하는 데 사용됩니다.

**Ctrl + U** 는 키보드 단축키로 사용할 수 있습니다.

### 아래 첨자

![](assets/screen_shot_2018-01-11at125703.png)

커서 다음에 입력한 텍스트나 텍스트를 아래 첨자로 지정하는 데 사용됩니다.

### 위 첨자

![](assets/screen_shot_2018-01-11at125708.png)

커서 다음에 선택된 텍스트나 텍스트를 superscript로 지정하는 데 사용됩니다.

### 텍스트로 붙여넣기

![](assets/screen_shot_2018-01-11at125713.png)

복사된 텍스트를 서식이 없는 일반 텍스트로 붙여넣습니다.

이 옵션을 선택하면 텍스트를 텍스트에 삽입하기 전에 미리 보기로 서식이 없는 일반 텍스트로 붙여넣을 수 있는 창이 열립니다. 확인 표시를 탭하거나 클릭하여 수락하고 X를 탭하거나 클릭하여 취소합니다.

![](assets/screen_shot_2018-01-11at143234.png)

### Word에서 붙여넣기

![](assets/screen_shot_2018-01-11at125717.png)

이 옵션을 선택하면 텍스트를 텍스트에 삽입하기 전에 미리 보기로 유지하여 텍스트를 붙여넣을 수 있는 창이 열립니다. 확인 표시를 탭하거나 클릭하여 수락하고 X를 탭하거나 클릭하여 취소합니다.

![](assets/screen_shot_2018-01-11at143250.png)

### 하이퍼링크

![](assets/screen_shot_2018-01-11at125839.png)

이 옵션을 사용하여 선택한 텍스트를 하이퍼링크로 변환하거나 이미 정의된 링크를 수정합니다. 이 옵션은 텍스트가 이미 선택되어 있는 경우에만 활성화되며 링크를 설정하기 위한 추가 옵션이 있는 창을 엽니다.

![](assets/screen_shot_2018-01-11at130003.png)

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

### 연결 해제

![](assets/screen_shot_2018-01-11at125901.png)

이 옵션을 사용하여 선택한 텍스트에 이미 적용된 링크를 제거합니다. 이 옵션은 링크가 이미 선택된 경우에만 활성화됩니다.

### 찾기

![](assets/screen_shot_2018-01-11at125906.png)

이 옵션을 사용하여 지정된 텍스트 문자열이 있는지 텍스트를 검색합니다. 이 옵션을 선택하면 검색 옵션을 지정하기 위한 창이 열립니다.

![](assets/screen_shot_2018-01-11at130107.png)

Enter the text for which you want to search and tap or click **Find** to begin the search. 취소하려면 X를 탭하거나 클릭합니다.
If you wish to do an exact match according to the case, select the option **Match Case** before starting the search.
일치하는 항목이 발견되면 강조 표시되고 검색 대화 상자가 흐리게 표시됩니다. Tap or click the **Find** button again in the dimmed dialog to search for the next occurrence.

![](assets/screen_shot_2018-01-11at130145.png)

추가 발생이 발견되지 않으면 메시지가 표시되고 텍스트 시작 부분에서 검색이 다시 시작됩니다.

![](assets/screen_shot_2018-01-11at130241.png)

### 바꾸기

![](assets/screen_shot_2018-01-11at125910.png)

이 옵션을 사용하여 지정된 텍스트 문자열이 발생한 텍스트를 검색하고 일치 항목을 다른 문자열로 바꿉니다. 이 옵션을 선택하면 검색 및 바꾸기 옵션을 지정하는 창이 열립니다.

![](assets/screen_shot_2018-01-11at130441.png)

검색할 텍스트를 입력하고 바꿀 텍스트를 입력합니다.

Tap or click **Find** to begin the search. 취소하려면 X를 클릭하거나 탭합니다.

If you wish to do an exact match according to the case, select the option **Match Case** before starting the search.

일치하는 항목이 발견되면 강조 표시되고 검색 대화 상자가 흐리게 표시됩니다. Click the **Find** button again in the dimmed dialog to search for the next occurrence or select the **Replace** button to replace the highlighted, matched text. Note that the **Replace** button is only active once a match is made.

Select **Replace all** to replace all occurrences of the text at once.

### 왼쪽으로 텍스트 정렬

![](assets/screen_shot_2018-01-11at142012.png)

텍스트를 왼쪽 여백에 정렬하는 데 사용됩니다.

### 텍스트를 가운데로

![](assets/screen_shot_2018-01-11at142017.png)

텍스트를 가운데에 정렬하는 데 사용됩니다.

### 오른쪽으로 텍스트 정렬

![](assets/screen_shot_2018-01-11at142021.png)

텍스트를 오른쪽 여백에 정렬하는 데 사용됩니다.

### 글머리 기호

![](assets/screen_shot_2018-01-11at142025.png)

선택된 텍스트를 글머리 기호 목록으로 서식을 지정하거나 커서 뒤에 글머리 기호 목록 삽입을 시작하는 데 사용됩니다.

To end a bulleted list, tap or click the **Bullet** button again or enter two carriage returns.

### numbered

![](assets/screen_shot_2018-01-11at142030.png)

선택한 텍스트의 서식을 번호 매기기 목록으로 지정하거나 커서 뒤에 번호 매기기 목록을 삽입하는 데 사용됩니다.

To end a numbered list, tap or click the **Numbered** button again or enter two carriage returns.

### 내어쓰기

![](assets/screen_shot_2018-01-11at141917.png)

선택한 텍스트 또는 커서 이후에 입력한 텍스트의 들여쓰기 수준을 줄이는 데 사용됩니다.

선택한 텍스트 또는 커서 위치가 이미 들여쓰기된 경우에만 활성 상태입니다.

### 들여쓰기

![](assets/screen_shot_2018-01-11at141922.png)

커서 이후에 입력한 텍스트나 텍스트의 들여쓰기 수준을 높이는 데 사용됩니다.

### 표

![](assets/screen_shot_2018-01-11at141928.png)

텍스트를 텍스트에 삽입하는 데 사용됩니다. 이 옵션을 선택하면 표의 세부 사항을 지정하는 창이 열립니다.

![](assets/screen_shot_2018-01-11at142405.png)

* **열**
표의 열 수 (필수)
* **행**
표의 행 수 (필수)
* **너비표**
너비
* **높이**
표의 높이
* **셀 내용**주위의 공백 패딩
셀
* **셀 간격** 셀 간격
* **테두리**
표의 테두리 획 두께
* if the header of the table:
   * 첫 번째 행을 사용해야 합니다.
   * 첫 번째 열을 사용해야 합니다.
   * 첫 번째 행과 첫 번째 열을 사용해야 합니다.
   * 또는 헤더를 사용하지 않아야 합니다.
* **캡션** 캡션 캡션

### 맞춤법 검사

![](assets/screen_shot_2018-01-11at141935.png)

텍스트 컨텐츠의 맞춤법을 확인하는 데 사용됩니다. 잘못된 철자는 빨간색 선으로 밑줄로 표시됩니다.

Further details about spell checking and customizing spell check dictionaries can be found in the document [Configure the Rich Text Editor Plug-Ins](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/configure-rich-text-editor-plug-ins.html).

### 특수 문자 {#special-characters}

![](assets/screen_shot_2018-01-11at142600.png)

텍스트에 특수 문자를 삽입하는 데 사용됩니다. 이 옵션을 선택하면 사용 가능한 문자가 표시되는 창이 열립니다.

![](assets/screen_shot_2018-01-11at142635.png)

원하는 문자를 탭하거나 클릭하여 커서를 커서 다음에 삽입합니다. 여러 문자를 삽입할 수 있습니다. X를 탭하거나 클릭하여 선택 창을 닫습니다.

### 소스 편집

![](assets/screen_shot_2018-01-11at142746.png)

텍스트의 HTML 소스를 보고 수정하는 데 사용됩니다.

**소스 편집** 아이콘을 탭하거나 클릭하여 서식이 지정된 보기에서 텍스트 컨텐츠를 변경하여 원시 HTML를 봅니다. 이 모드에서는 다른 모든 서식 옵션이 비활성화됩니다. **소스 편집** 아이콘을 다시 탭하거나 클릭하여 서식이 지정된 보기로 돌아갑니다.

>[!CAUTION]
>
>As always the case with access to raw HTML, care must be exercised when using the **Source Edit** option!
>
>**소스 편집을** 통해 입력한 HTML는 XSS 위험에 대해 스캔되며 삽입된 스크립트는 제거되고 결과 페이지에 나타나지 않습니다. **그러나 소스 편집에서** 입력한 잘못된 형식의 HTML는 페이지의 템플릿을 끊어서 예기치 않은 서식 지정 또는 결과 페이지를 사용할 수 없게 만들 수 있습니다.

>[!NOTE]
>
>**소스 편집을** 통해 입력한 HTML는 XSS 위험과 스크립트가 검색되고 스크립트가 자동으로 제거되므로, 소스 편집에서 **입력한 내용에 따라 지속된 실제 컨텐츠가 달라질** 수 있습니다. For this reason, in order to save changes made using **Source Edit**, you must first exit **Source Edit** to view the text in the normal editor before saving.

### 단락 형식

![](assets/screen_shot_2018-01-11at142752.png)

선택한 텍스트 또는 커서 다음에 삽입된 텍스트에 단락 서식을 적용하는 데 사용됩니다. 이 옵션을 선택하면 단락 형식이 선택된 드롭다운이 열립니다.

![](assets/screen_shot_2018-01-11at142828.png)

텍스트 구성 요소는 인라인 편집도 가능하지만 공백 제한 때문에 모든 서식 옵션이 인라인 사용 가능하지는 않습니다. 모든 옵션을 보려면 전체 화면 모드로 전환합니다.

![](assets/screen_shot_2018-01-11at142921.png)

## Design Dialog {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 사용하여 컨텐츠 작성자가 사용할 수 있는 텍스트 서식 지정 옵션을 정의할 수 있습니다.

### Plugins Tab {#plugins-tab}

플러그인 탭은 컨텐츠 작성자가 사용할 수 있는 다양한 텍스트 서식 지정 옵션을 활성화 및 비활성화하는 데 사용됩니다.

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
* To remove a style tap or click the **Delete** button.
* 형식 순서를 재배치하려면 핸들을 탭하거나 클릭하고 드래그합니다.

### Configuring Special Characters {#configuring-special-characters}

![](assets/chlimage_1-31.png)

특수 문자를 삽입하는 옵션은 구성 요소에 대해 활성화하거나 비활성화할 수 있습니다. 활성화되면 허용되는 문자를 정의할 수 있습니다.

* **추가** 단추를 탭하거나 클릭하여 새 문자를 삽입합니다.
* 편집 대화 상자에 표시할 문자와 설명의 HTML 코드를 입력합니다.
* To remove a character tap or click the **Delete** button.
* 문자 순서를 재배치하려면 핸들을 누르거나 클릭하고 핸들을 드래그합니다.

## Styles Tab {#styles-tab}

The Text Component supports the AEM [style system](authoring.md#component-styling).
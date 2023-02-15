---
title: 이메일 텍스트 구성 요소
description: 이메일 텍스트 구성 요소는 바로 편집 기능이 있는 서식 있는 텍스트 편집 및 작성 구성 요소입니다.
role: Architect, Developer, Admin, User
exl-id: 4aa192f6-8314-40e7-8732-c6626d647986
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# 이메일 텍스트 구성 요소 {#email-text-component}

이메일 텍스트 구성 요소는 바로 편집 기능이 있는 서식 있는 텍스트 편집 및 작성 구성 요소입니다.

## 사용 {#usage}

이메일 텍스트 구성 요소는 인라인 편집기와 전체 화면 포맷으로 간편한 텍스트 편집이 가능한 강력한 서식 있는 텍스트 편집기를 제공합니다.

* [편집 대화 상자](#edit-dialog)에는 전체 화면 편집 대화 상자에서 전체 기능을 사용할 수 있고 제한된 옵션이 제공되는 인라인 편집 기능이 있습니다.
* [디자인 대화 상자](#design-dialog)를 통해 콘텐츠 작성자용 템플릿에서 텍스트 서식 옵션을 구성할 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

현재 버전의 이메일 텍스트 구성 요소는 2022년 10월 이메일 핵심 구성 요소 릴리스 X과(와) 함께 도입된 v1입니다. 이 문서에서는 해당 구성 요소에 대해 설명합니다.

다음 표에서 구성 요소의 모든 지원 버전, 구성 요소 버전과 호환되는 AEM 버전 및 이전 버전에 대한 설명서 링크에 대해 자세히 살펴볼 수 있습니다.

| 구성 요소 버전 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | 호환 가능 | 호환 가능 |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 문서 [이메일 핵심 구성 요소 버전](/help/email/versions.md)을 참조하십시오.

## 샘플 구성 요소 출력 {#sample-component-output}

텍스트 구성 요소를 경험하고 구성 옵션의 샘플뿐만 아니라 HTML 및 JSON 출력을 확인하려면 [구성 요소 라이브러리](https://adobe.com/go/aem_cmp_library_email_text_kr)를 참조하십시오.

### 기술 세부 사항 {#technical-details}

이메일 텍스트 구성 요소에 대한 최신 기술 설명서는 [GitHub에서 확인할 수 있습니다](https://adobe.com/go/aem_cmp_tech_email_text_v1_kr).

핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 참조하십시오.

## 이메일 텍스트 구성 요소 및 리치 텍스트 편집기 {#the-text-component-and-the-rich-text-editor}

이메일 텍스트 구성 요소는 AEM 리치 텍스트 편집기(RTE)를 활용합니다. RTE를 통해 텍스트 콘텐츠를 편집할 수 있는 다양한 기능이 콘텐츠 작성자에게 제공됩니다. RET는 유연하게 구성되고 다양한 옵션을 제공합니다. RTE를 구성하는 방법에 대한 자세한 내용은 [리치 텍스트 편집기 구성](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/configuring-and-extending/rich-text-editor.html) 및 [리치 텍스트 편집기 플러그인 구성](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html) 문서에서 확인할 수 있습니다.

이 문서의 나머지 부분에서 즉시 사용 가능한 RTE 구성과 함께 이메일 텍스트 구성 요소에 대한 표준 구성을 보여 줍니다.

>[!NOTE]
>
>[RTE의 UI 구성](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html)에서 활성화되는 옵션만 이메일 텍스트 구성 요소에서 사용할 수 있습니다.

## 편집 대화 상자 {#edit-dialog}

![텍스트 구성 요소의 편집 대화 상자](/help/email/assets/email-text-edit.png)

### 서식 옵션 {#options}

편집 대화 상자는 사용자가 텍스트를 작성할 서식 있는 표준 텍스트 서식 도구를 제공합니다.

#### 볼드체

![볼드체 아이콘](/help/assets/text-bold.png)

선택한 텍스트에 볼드체 서식 지정을 적용하거나 커서 다음에 입력한 텍스트를 볼드체로 서식 지정하는 데 사용됩니다,

키보드 단축키로 **Ctrl+B**&#x200B;를 사용할 수 있습니다.

#### 이탤릭체

![이탤릭체 아이콘](/help/assets/text-italic.png)

선택한 텍스트에 이탤릭체 서식 지정을 적용하거나 커서 다음에 입력한 텍스트를 이탤릭체로 서식 지정하는 데 사용됩니다,

키보드 단축키로 **Ctrl+I**&#x200B;를 사용할 수 있습니다.

#### 밑줄

![밑줄 아이콘](/help/assets/text-underline.png)

선택한 텍스트에 밑줄 서식 지정을 적용하거나 커서 다음에 입력한 텍스트를 밑줄로 서식 지정하는 데 사용됩니다,

키보드 단축키로 **Ctrl+U**&#x200B;를 사용할 수 있습니다.

#### 아래 첨자

![아래 첨자 아이콘](/help/assets/text-subscript.png)

선택한 텍스트나 커서 다음에 입력한 텍스트를 아래 첨자로 서식 지정하는 데 사용됩니다,

#### 위 첨자

![위 첨자 아이콘](/help/assets/text-superscript.png)

선택한 텍스트나 커서 다음에 입력한 텍스트를 위 첨자로 서식 지정하는 데 사용됩니다,

#### 텍스트로 붙여넣기

![텍스트로 붙여넣기 아이콘](/help/assets/text-paste-text.png)

서식 지정 없이 복사한 텍스트를 일반 텍스트로 붙여넣습니다.

이 옵션을 선택하면 서식 지정 없이 텍스트를 일반 텍스트로 붙여넣을 수 있는 창이 텍스트에 삽입되기 전 미리보기로 열립니다. 확인 표시를 탭하거나 클릭하여 수락하고 x를 탭하거나 클릭하여 취소합니다.

![텍스트로 붙여넣기 예제](/help/assets/text-paste-text-example.png)

#### Word에서 붙여넣기

![Word에서 붙여넣기 아이콘](/help/assets/text-paste-word.png)

이 옵션을 선택하면 서식 지정을 유지하면서 텍스트를 일반 텍스트로 붙여넣을 수 있는 창이 텍스트에 삽입되기 전 미리보기로 열립니다. 확인 표시를 탭하거나 클릭하여 수락하고 x를 탭하거나 클릭하여 취소합니다.

![Word에서 붙여넣기 사례](/help/assets/text-paste-word-example.png)

#### 하이퍼링크

![하이퍼링크 아이콘](/help/assets/text-hyperlink.png)

이 옵션을 사용하여 선택한 텍스트를 하이퍼링크로 변환하거나 이미 정의된 링크를 수정합니다. 이 옵션은 링크 설정 추가 옵션이 있는 창을 엽니다.

![하이퍼링크 예](/help/assets/text-hyperlink-example.png)

* 경로 입력
   * **선택 열기** 대화 상자를 통해 AEM의 경로 선택
   * 링크가 AEM 내에 없는 경우 절대 URL을 입력합니다.
      * 절대 경로가 아닌 경로는 AEM의 상대 경로로 해석됩니다.
* 링크에 대한 대체 설명 텍스트 입력
* 링크 비헤이비어 선택
   * 대상
   * 동일한 탭
   * 새 탭
   * 상위 프레임
   * 맨 위 프레임

확인 표시를 탭하거나 클릭하여 링크를 적용하거나 x를 탭하거나 클릭하여 취소합니다.

#### 연결 해제

![링크 해제 아이콘](/help/assets/text-unlink.png)

이 옵션을 사용하여 선택한 텍스트에 이미 적용된 링크를 제거합니다. 이 옵션은 링크가 이미 선택된 경우에만 활성화됩니다.

#### 앵커 {#anchor}

![앵커 아이콘](/help/email/assets/anchor.png)

이 옵션을 사용하여 텍스트에 앵커를 삽입합니다.

#### 찾기

![찾기 아이콘](/help/assets/text-find.png)

지정된 텍스트 문자열의 발생 횟수를 알아보려면 이 옵션을 사용하여 텍스트를 검색합니다. 이 옵션을 선택하면 검색 옵션을 지정하는 창이 열립니다.

![찾기 사례](/help/assets/text-find-example.png):

검색할 텍스트를 입력하고 **찾기**를 탭하거나 클릭하여 검색을 시작합니다. x를 탭하거나 클릭하여 취소합니다.
사례에 따라 정확하게 일치시키려면 **사례 일치** 옵션을 선택한 다음 검색을 시작합니다.
일치가 발견되면 강조 표시되고 검색 대화 상자가 흐리게 표시됩니다. 흐리게 표시된 대화 상자에서 **찾기** 버튼을 다시 탭하거나 클릭하여 다음 발생 횟수를 검색합니다.

![찾기 사례 확인](/help/assets/text-find-example-found.png):

추가 발생 항목이 없는 경우 메시지가 표시되고 텍스트 시작부터 검색이 다시 시작됩니다.

![찾기 사례(더 이상 발생 횟수 없음)](/help/assets/text-find-example-found-end.png)

#### 바꾸기

![바꾸기 아이콘](/help/assets/text-replace.png)

지정된 텍스트 문자열의 발생 횟수를 알아보려면 이 옵션을 사용하여 텍스트를 검색하고 일치하는 문자열을 다른 문자열로 대체합니다. 이 옵션을 선택하면 검색 옵션을 지정하는 창이 열리고 옵션을 대체합니다.

![바꾸기 사례](/help/assets/text-replace-example.png)

검색할 텍스트와 대체해야 할 텍스트를 입력합니다.

* **찾기**&#x200B;를 탭하거나 클릭하여 검색을 시작합니다. x를 클릭하거나 탭하여 취소합니다.
* 사례에 따라 정확하게 일치시키려면 **사례 일치** 옵션을 선택한 다음 검색을 시작합니다.
* **모두 바꾸기**&#x200B;를 선택하여 한 번에 모든 발생 항목을 바꿉니다.

일치가 발견되면 강조 표시되고 검색 대화 상자가 흐리게 표시됩니다. 흐리게 표시된 대화 상자에서 **찾기** 버튼을 다시 클릭하여 다음 발생 항목을 검색하거나, **바꾸기** 버튼을 선택하여 강조 표시 및 일치된 텍스트를 대체합니다. 일치하는 항목이 있는 경우에만 **바꾸기** 버튼이 활성화됩니다.

찾기를 클릭하면 찾기 및 바꾸기 대화 상자가 투명해지고, 바꾸기를 클릭하면 불투명해집니다. 이로써 작성자는 대체될 텍스트를 검토할 수 있습니다.

>[!NOTE]
>
>바꾸기 기능을 사용하면 찾을 문자열과 동시에 바꿀 문자열을 입력해야 합니다. 단, 계속 찾기를 클릭하여 문자열을 대체하기 전에 검색할 수 있습니다. 찾기를 클릭한 후 바꾸기 문자열을 입력하면 검색은 텍스트 시작으로 재설정됩니다.

#### 실행 취소

![실행 취소 아이콘](/help/email/assets/undo.png)

리치 텍스트 편집기에서 마지막 편집을 실행 취소하는 데 사용됩니다.

#### 다시 실행

![다시 실행 아이콘](/help/email/assets/redo.png)

실행 취소 아이콘을 사용하여 실행 취소된 편집을 실행 취소하는 데 사용됩니다.

#### 왼쪽으로 텍스트 정렬

![왼쪽으로 정렬 아이콘](/help/assets/text-left.png)

왼쪽 여백으로 텍스트를 정렬하는 데 사용됩니다.

#### 텍스트를 가운데로

![텍스트를 가운데로 아이콘](/help/assets/text-center.png)

가운데로 텍스트를 정렬하는 데 사용됩니다.

#### 오른쪽으로 텍스트 정렬

![오른쪽으로 정렬 아이콘](/help/assets/text-right.png)

오른쪽 여백으로 텍스트를 정렬하는 데 사용됩니다.

#### 글머리 기호

![글머리 기호 아이콘](/help/assets/text-bullet.png)

선택한 텍스트 서식을 글머리 기호 목록으로 지정하거나 커서 다음에 글머리 기호 목록을 삽입하는 데 사용됩니다.

글머리 기호 목록을 종료하려면 **글머리 기호** 버튼을 다시 탭 또는 클릭하거나 캐리지 리턴을 2번 입력합니다.

#### 번호 매기기

![번호 매기기 목록 아이콘](/help/assets/text-numbered.png)

선택한 텍스트 서식을 번호 매기기 목록으로 지정하거나 커서 다음에 번호 매기기 목록을 삽입하는 데 사용됩니다.

번호 매기기 목록을 종료하려면 **번호 매기기** 버튼을 다시 탭 또는 클릭하거나 캐리지 리턴을 2번 입력합니다.

#### 내어쓰기

![내어쓰기 아이콘](/help/assets/text-outdent.png)

선택한 텍스트나 커서 다음에 입력한 텍스트의 들여쓰기 레벨을 낮추는 데 사용됩니다,

선택한 텍스트나 커서의 위치가 이미 들여 쓴 경우에만 활성화됩니다.

#### 들여쓰기

![들여쓰기 아이콘](/help/assets/text-indent.png)

선택한 텍스트나 커서 다음에 입력한 텍스트의 들여쓰기 레벨을 높이는 데 사용됩니다,

#### 표

![표 아이콘](/help/assets/text-table.png)

표를 텍스트에 삽입하는 데 사용됩니다. 이 옵션을 선택하면 표의 세부 정보를 지정하는 창이 열립니다.

![표 예제](/help/assets/text-table-example.png)

* **열** - 표의 열 수 (필수)
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

#### 이미지

![이미지 아이콘](/help/email/assets/image-icon.png)

삽입된 이미지를 정렬하는 데 사용됩니다.

#### 맞춤법 검사

![맞춤법 검사 아이콘](/help/assets/text-spellcheck.png)

텍스트 맞춤법을 검사하는 데 사용됩니다. 오자는 빨간색 점선으로 밑줄이 그어져 있습니다.

맞춤법 검사와 맞춤법 검사 사전 맞춤화에 대한 자세한 내용은 [리치 텍스트 편집기 플러그인 구성](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html) 문서에서 확인할 수 있습니다.

#### 특수 문자 {#special-characters}

![특수 문자 아이콘](/help/assets/text-special-characters.png)

특수 문자를 텍스트에 삽입하는 데 사용됩니다. 이 옵션을 선택하면 창이 열리고 사용할 수 있는 문자가 표시됩니다.

![특수 문자 예제](/help/assets/text-special-characters-example.png)

원하는 문자를 탭하거나 클릭하여 커서 다음 텍스트에 삽입합니다. 여러 문자들을 삽입할 수 있습니다. x를 탭하거나 클릭하여 선택 창을 닫습니다.

#### 소스 편집

![소스 편집 아이콘](/help/assets/text-source.png)

텍스트의 HTML 소스를 확인하고 수정하는 데 사용됩니다.

원시 HTML을 보려면 **소스 편집** 아이콘을 탭하거나 클릭하여 서식이 지정된 보기에서 텍스트 콘텐츠를 변경합니다. 이 모드에서 다른 모든 서식 지정 옵션이 비활성화됩니다. 서식이 지정된 보기로 돌아가려면 **소스 편집** 아이콘을 다시 탭하거나 클릭합니다.

>[!CAUTION]
>
>원시 HTML에 액세스하는 경우와 마찬가지로 **소스 편집** 옵션을 사용할 때 주의해야 합니다
>
>XSS 위험이 있는 경우 **소스 편집**&#x200B;을 통해 입력된 HTML을 스캔합니다. 그리고 삽입한 스크립트를 제거하면 결과 페이지에 나타나지 않습니다. **소스 편집**&#x200B;을 통해 입력한 HTML의 형식이 잘못되어도 페이지용 템플릿이 깨질 수 있습니다. 그 결과 페이지가 예고 없이 서식 지정되거나 렌더링되어 사용할 수 없게 됩니다.

>[!NOTE]
>
>XSS 위험 및 특정 스크립트가 존재하는 경우 **소스 편집**&#x200B;을 통해 입력된 HTML을 스캔하여 발견된 위험이 자동으로 제거되기 때문에 지속되는 실제 콘텐츠가 **소스 편집**&#x200B;에 입력된 내용과 달라질 수 있습니다. 따라서 **소스 편집**&#x200B;을 통해 변경 사항을 저장하려면 먼저 **소스 편집**&#x200B;을 종료하고 저장하기 전에 일반 편집기에서 텍스트를 조회해야 합니다.

#### 단락 형식

![단락 형식 아이콘](/help/assets/text-paragraph.png)

선택한 텍스트이나 커서 다음에 삽입한 텍스트에 단락 형식을 적용하는 데 사용됩니다. 이 옵션을 선택하면 단락 형식이 선택된 위치에서 드롭다운이 열립니다.

![단락 형식 예제](/help/assets/text-paragraph-example.png)

#### Adobe Campaign 변수 선택

![Adobe Campaign 변수 선택 아이콘](/help/email/assets/select-adobe-campaign-variable-icon.png)

Adobe Campaign의 다이내믹 콘텐츠를 삽입하기 위한 [Adobe Campaign 변수 선택](/help/email/campaign-variables.md) 대화 상자를 엽니다.

### 인라인 편집 {#in-line-editing}

텍스트 구성 요소는 인라인으로도 편집할 수 있습니다. 인라인으로 편집하려면 콘텐츠 페이지에서 이메일 텍스트 구성 요소를 선택합니다.

![이메일 텍스트 구성 요소 선택](/help/email/assets/email-text-select-component.png)

그런 다음 구성 요소에 표시되는 팝업 도구 모음에서 **편집** 아이콘을 탭하거나 클릭합니다. 도구 모음이 제한된 텍스트 서식 옵션(**Adobe Campaign 변수 선택** 옵션 액세스 포함)을 표시하도록 변경되며, 텍스트를 인라인으로 편집할 수 있습니다.

![인라인 편집 예제](/help/email/assets/email-text-edit-inline-example.png)

도구 모음에서 확인 표시를 탭하거나 클릭하여 변경 사항을 저장하거나 X를 눌러 취소합니다.

공간 제약으로 일부 서식 옵션은 인라인에서 사용할 수 없습니다. 모든 옵션을 보려면 전체 화면 모드로 전환합니다.

### ID 설정 {#setting-id}

이 옵션을 통해 HTML에서 구성 요소의 고유 식별자를 제어할 수 있습니다.

* 비워 두면 고유 ID는 자동으로 생성되고 결과 페이지 검사를 통해 발견될 수 있습니다.
* ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
* ID를 변경하면 CSS에 영향을 줄 수 있습니다.

## 디자인 대화 상자 {#design-dialog}

템플릿 작성자는 디자인 대화 상자를 통해 콘텐츠 작성자가 사용할 수 있는 텍스트 서식 옵션을 정의할 수 있습니다.

### 플러그인 탭 {#plugins-tab}

**플러그인** 탭을 통해 콘텐츠 작성자가 사용할 수 있는 텍스트 서식 옵션을 활성화 및 비활성화합니다.

### 기능 {#features}

![디자인 대화 상자 기능](/help/assets/text-design-features.png)

구성 요소에서 다음 기능을 활성화하거나 비활성화할 수 있습니다.

* 일반 텍스트 붙여넣기
* Word에서 붙여넣기
* 찾기 및 바꾸기
* 실행 취소 및 다시 실행
* 맞춤법 검사기
* 삽입한 이미지 수정 옵션
* HTML 소스 편집

### 서식 {#formatting}

![디자인 대화 상자 서식](/help/assets/text-design-formatting.png)

구성 요소에서 다음 서식 옵션을 활성화하거나 비활성화할 수 있습니다.

* 표
* 목록 (글머리, 번호, 들여쓰기, 내어쓰기)
* 정렬 (왼쪽, 오른쪽, 중앙)
* 볼드체, 이탤릭체, 밑줄
* 연결 (및 연결 해제)
* 아래 첨자/위 첨자

### 단락 스타일 {#paragraph-styles}

![디자인 대화 상자 단락 스타일](/help/assets/text-design-paragraph.png)

구성 요소에서 단락 스타일을 활성화하거나 비활성화할 수 있습니다. 활성화되면 허용된 포맷을 정의할 수 있습니다.

* **추가** 버튼을 탭하거나 클릭하여 새 스타일을 삽입합니다.
* 편집 대화 상자에 표시할 스타일 및 설명에 대한 코드를 입력합니다.
* 스타일을 제거하려면 **삭제** 버튼을 탭하거나 클릭합니다.
* 포맷 순서를 재배열하려면 핸들을 탭하거나 클릭하여 드래그합니다.

### 특수 문자 {#configuring-special-characters}

![디자인 대화 상자 특수 문자](/help/assets/text-design-special-characters.png)

구성 요소에서 특수 문자를 삽입하는 옵션을 활성화하거나 비활성화할 수 있습니다. 활성화되면 허용된 문자를 정의할 수 있습니다.

* **추가** 버튼을 탭하거나 클릭하여 새 문자를 삽입합니다.
* 편집 대화 상자에 표시할 문자 및 설명에 대한 HTML 코드를 입력합니다.
* 문자를 제거하려면 **삭제** 버튼을 탭하거나 클릭합니다.
* 문자 순서를 재배열하려면 핸들을 탭하거나 클릭하여 드래그합니다.

## 스타일 탭 {#styles-tab}

이메일 텍스트 구성 요소는 AEM [스타일 시스템](/help/get-started/authoring.md#component-styling)을 지원합니다.
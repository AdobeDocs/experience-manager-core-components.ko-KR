---
title: Adobe 클라이언트 데이터 레이어를 사용하여 핵심 구성 요소 및 Adobe Launch 통합
description: Adobe Launch를 사용하여 핵심 구성 요소 이벤트를 등록하도록 Adobe Launch를 구성하는 방법
translation-type: tm+mt
source-git-commit: f930a0d6004a29369b189137dd9c52e637ea3a61
workflow-type: tm+mt
source-wordcount: '1160'
ht-degree: 1%

---


# Adobe 클라이언트 데이터 레이어를 사용하여 핵심 구성 요소 및 Adobe Launch 통합 {#launch-integration}

핵심 구성 요소는 Adobe 클라이언트 데이터 레이어를 사용하여 Adobe Launch와 통합할 수 있습니다. 이 문서에서는 이미지 구성 요소의 클릭 이벤트를 추적하기 위해 Adobe Launch를 구성하는 방법에 대해 설명합니다.

구성된 경우, 핵심 이미지 구성 요소를 클릭하면 Launch가 브라우저 콘솔에서 다음 출력을 생성합니다.

![콘솔 출력 예](/help/assets/launch-console-output.png)

## AEM과 통합 실행 {#launch-aem}

첫 번째 Adobe Launch는 AEM 사이트와 통합되어야 합니다.

### 1단계 - Adobe I/O에서 통합 만들기 {#create-io-integration}

먼저 Adobe I/O에 로그인하여 통합 구성을 시작합니다.

1. 이동 `https://console.adobe.io`.
1. Adobe ID를 사용하여 로그인합니다.
1. 빠른 시작 섹션에서 통합 **만들기를 클릭합니다**.
1. Select **Access an API** and click **Continue**.
1. Adobe **Experience Platform** 아래의 Experience Platform Launch API를 선택하고 **계속을 클릭합니다**.

### 2단계 - AEM에서 IMS 구성 만들기 {#ims-configuration}

AEM에서 Adobe I/O에서 구성을 시작한 통합을 정의해야 합니다.

1. AEM 홈 페이지로 이동하여 **도구 -> 보안 -> Adobe IMS 구성을 클릭합니다**.
1. **만들기**&#x200B;를 클릭합니다.
1. Cloud **솔루션으로****Adobe Launch를 선택합니다**.
1. 새 인증서 **만들기를 선택합니다**.
1. aem-launch-certificate와 같은 인증서 **의 별칭을 입력합니다**.
1. 인증서 **만들기를** 클릭하고 팝업 **에서 확인을** 클릭하여 인증서를 만듭니다.
1. [ **공개 키** 다운로드]를 클릭하고 팝업 창에서 [ **다운로드]를 클릭합니다**.

### 3단계 - Adobe I/O 구성 완료 {#finish-io}

AEM IMS 구성에서 만든 인증서와 키를 사용하여 Adobe I/O 구성을 완료할 수 있습니다.

1. 1단계처럼 Adobe I/O 콘솔로 [돌아갑니다.](#create-io-integration)
1. 새 **통합** 만들기 창에서 이름 및 AEM Launch 데이터 레이어 **와 같은 설명을 입력합니다**.
1. 공개 키 인증서 **에서** 2단계에서 만든 인증서를 [업로드합니다.](#ims-configuration)
1. 론치 - **제품 프로파일을 선택합니다**.
1. Click **Create integration**.
1. 통합 세부 사항 **을 확인하려면 계속을 클릭합니다**. AEM 인스턴스의 IMS 구성을 완료하려면 나중에 이러한 세부 정보가 필요합니다.

### 4단계 - IMS 구성 완료 {#finish-ims}

Adobe I/O 통합 세부 사항을 사용하여 AEM IMS 구성을 완료할 수 있습니다.

1. AEM 탭의 **Adobe IMS 기술 계정 구성** 탭에서 [다음](#ims-configuration) 을 **클릭합니다**.
1. Adobe Launch의 **IMS 구성과 같은 제목을 입력합니다**.
1. Adobe I/O 탭에서 **API 키(클라이언트 ID)를 복사합니다**.
1. AEM 탭에서 이전에 복사한 키를 **API 키 필드에 붙여 넣습니다**.
1. Adobe I/O에서 **클라이언트 암호** 검색을 클릭하고 복사합니다.
1. AEM 탭에서 클라이언트 **암호** 필드에 붙여 넣습니다.
1. Adobe I/O 탭에서 **JWT** 탭을 선택하고 다음과 같은 URL을 복사합니다 `https://ims-na1.adobelogin.com`.
1. AEM 탭에서 URL을 **인증 서버** 필드에 붙여 넣습니다.
1. Adobe I/O 탭에서 JWT 페이로드(중괄호 사이의 코드)를 복사합니다.
1. AEM 탭에서 페이로드 **필드에** 붙여 넣습니다.
1. 만들기를 **클릭하여** AEM에서 IMS 구성을 만듭니다.

### 5a 단계 - Adobe Launch에서 속성 만들기 {#create-property}

속성은 Launch가 사이트에 삽입할 수 있는 기능을 정의합니다.

1. Adobe Launch로 이동합니다 `https://launch.adobe.com`.
1. Adobe ID를 사용하여 로그인합니다.
1. 새 **속성을 클릭합니다**.
1. AEM 데이터 레이어 **실행과 같은 이름을 입력합니다**.
1. 도메인을 입력합니다.
1. **저장**&#x200B;을 클릭합니다.

### 5b 단계 - 론치에서 규칙 만들기 {#launch-rule}

만든 속성을 사용하여 작업 발생 시 발생할 상황을 지정하는 규칙을 정의할 수 있습니다.

1. 5단계 [실행 AEM 데이터 레이어](#create-property) 에서 새로 **추가된 속성을 클릭합니다**.
1. 규칙 **탭을** 선택하고 새 규칙 **만들기를 클릭합니다**.
1. 이미지 클릭 **과 같은 이름을 입력합니다**.
1. 이벤트 아래의 **+** 단추를 **클릭합니다**.
1. **코어** 를 **확장자로**&#x200B;선택하고 **이벤트 유형** Enter **-Enter** -imageMpCSS 선택기로 클릭합니다 **** ****.
1. 변경 **내용 유지를 클릭합니다**.
1. 작업 아래의 **+** 버튼을 **클릭합니다**.
1. **코어** 를 **확장**&#x200B;유형으로 **** 사용자 지정 코드 **를 선택하고 Action** 을 클릭한 다음 Open Editor ****&#x200B;를 클릭합니다.
1. 편집기에서 다음 코드를 입력합니다. `console.log("DOM click event tracked by Launch for image: ", event.target.src);`
1. **저장**&#x200B;을 클릭합니다.
1. 변경 **내용 유지를 클릭합니다**.
1. 저장을 **클릭하여** 새 규칙을 만듭니다.

### 6단계 - 론치 규칙 게시 {#publish-rule}

AEM 사이트에서 새 규칙을 사용할 수 있도록 하려면 이를 게시해야 합니다.

1. Adobe **Launch** 탭에서 **게시** 탭을선택합니다.
1. 새 **라이브러리 추가를 클릭합니다**.
1. 데모 **1** 과 같이 적절한 이름을 **입력합니다**.
1. 환경 **의** 경우 **개발(개발)과 같이 적절한 것으로 선택합니다**.
1. 리소스 **추가를 클릭합니다**.
1. 규칙 **-> 이미지 클릭 -> 최신** 버전을 선택하고 **선택 및 새 개정 만들기를 클릭합니다**.
1. **개발을 위한 저장 및 구축**&#x200B;을 클릭합니다.
1. 팝업에서 업데이트 **적용 및 계속을 클릭합니다**.
1. 라이브러리가 빌드되면 줄임표 아이콘을 클릭하고 승인을 위해 **제출을 선택합니다**.
1. 팝업에서 제출을 **클릭합니다**.
1. 줄임표 아이콘을 클릭하고 스테이징용 **빌드를 선택합니다**.
1. 빌드가 완료되면 줄임표 아이콘을 클릭하고 게시를 **위한 승인을 선택합니다**.
1. 팝업에서 승인을 **클릭합니다**.
1. 줄임표 아이콘을 클릭하고 제작 및 **출판을 선택합니다**.
1. 팝업에서 게시를 **클릭합니다**.

### 7단계 - 사이트에 대한 클라우드 구성 활성화 {#enable-configurations}

통합을 사용하려면 AEM에서 클라우드 구성으로 할당해야 합니다.

1. AEM 콘솔에서 **도구 -> 일반 -> 구성 브라우저를 클릭합니다**.
1. 핵심 **구성 요소 예를** 확인하고 속성을 **클릭합니다**.
1. 클라우드 **구성을** 선택하고 **저장 및 닫기를 클릭합니다**.

### 8단계 - AEM에서 사이트와 실행 통합 만들기 {#create-launch-integration}

AEM이 Launch와 연동하려면 론치 통합이 필요합니다.

1. AEM 콘솔에서 **도구 -> 클라우드 서비스 -> Adobe Launch 구성을 클릭합니다**.
1. 핵심 **구성 요소 예를** 선택하고 만들기를 **클릭합니다**.
1. 론치 구성 **과** 같은 **제목을 입력합니다**.
1. 4단계에서 만든 IMS 구성을 [선택합니다.](#finish-ims)
1. As **Company** select as appropriate.
1. As **속성** 5단계에서 새로 추가된 론치 속성을 [선택합니다.](#create-property)
1. 작성자에 **프로덕션 코드 포함** 슬라이더를 오른쪽으로 이동하고 다음을 **클릭합니다**.
1. **다음**&#x200B;을 클릭합니다.
1. **다음**&#x200B;을 클릭합니다.
1. **만들기**&#x200B;를 클릭합니다.

### 9단계 - AEM 사이트를 론치 통합에 연결 {#connect-aem}

AEM에서 론치 통합을 사용하려면 클라우드 구성으로 할당해야 합니다.

1. AEM 콘솔에서 사이트 **를** 클릭하고 **핵심**&#x200B;구성 요소 사이트를확인합니다.
1. Click **Properties**.
1. Select the **Advanced** tab.
1. [ **클라우드 구성**]으로 **핵심 구성 요소 예** 를 선택하고 [선택]을 **클릭합니다**.
1. Click **Save &amp; Close**.

### 10단계 - 론치 로직이 페이지에 적용되었는지 확인 {#verify-launch}

지금까지 이 단계를 성공적으로 수행했는지 테스트합니다.

1. 미리 보기 모드에서 핵심 구성 요소 라이브러리의 이미지 페이지를 엽니다. `http://<lhost&gt;:<port&gt;/editor.html/content/core-components-examples/library/page-authoring/image.html`
1. 이미지를 클릭하고 메시지가 브라우저 콘솔 `A Core Image was clicked` 에 표시되는지 확인합니다.

## AEM 및 데이터 레이어와 통합 실행 {#data-layer-launch}

이제 AEM과 Launch 간의 통합이 설정되었으므로 데이터 레이어와 통합할 수 있습니다.

### 1단계 - Adobe Launch에서 규칙 만들기 {#create-rule}

다음 값을 사용하여 [5단계의](#launch-rule) 단계를 반복하여 Adobe Launch에서 새 규칙을 추가합니다.

* 이름: `image-click-data-layer`
* 이벤트:
   * 확장: 코어
   * 이벤트 유형: DOM 준비
* 작업:
   * 확장: 코어
   * 작업 유형: 사용자 지정 코드
   * 코드:

      ```
        function onImageClick(event) {
          console.log("Data layer click event tracked by Launch for image: " + event.info.path);
          console.log("dataLayer.getState(): ", adobeDataLayer.getState()); 
        }
        adobeDataLayer.addEventListener('image clicked', onImageClick);
      ```

### 2단계 - 실행 규칙을 게시하여 AEM 사이트에서 사용할 수 있도록 설정 {#publish-rule-2}

새 규칙을 게시하려면 [6단계의](#publish-rule) 단계를 반복합니다.

### 3단계 - 론치 로직이 페이지에 적용되었는지 확인 {#verify}

1. 미리 보기 모드에서 핵심 구성 요소 라이브러리의 이미지 페이지를 엽니다. `http://<host&gt;:<port&gt;/editor.html/content/core-components-examples/library/page-authoring/image.html`
1. 이미지를 클릭하고 다음 메시지가 브라우저 콘솔에 표시되는지 확인합니다.

   ![데이터 레이어 콘솔 출력](/help/assets/data-layer-console-output.png)

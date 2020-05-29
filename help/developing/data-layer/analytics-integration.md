---
title: Adobe 클라이언트 데이터 레이어를 사용하여 핵심 구성 요소 및 Adobe Analytics 통합
description: 핵심 구성 요소 이벤트를 등록하도록 Adobe Analytics를 구성하는 방법
translation-type: tm+mt
source-git-commit: f930a0d6004a29369b189137dd9c52e637ea3a61
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 2%

---


# Adobe 클라이언트 데이터 레이어를 사용하여 핵심 구성 요소 및 Adobe Analytics 통합 {#analytics-integration}

이 문서에서는 AEM, Adobe Client Data Layer, Adobe Launch 및 Adobe Analytics를 기반으로 하여 다음을 추적하기 위한 엔드 투 엔드 구성을 설정하는 방법에 대해 자세히 설명합니다.

* 페이지를 로드할 때 Adobe 클라이언트 데이터 레이어에 저장된 페이지 ID
* 이미지를 클릭할 때 Adobe 클라이언트 데이터 레이어에 저장되는 이미지 경로

코어 구성 요소를 예로 사용하지만 사용자 지정 구성 요소에 사용할 수 있습니다.

##  1단계 - Adobe Analytics에서 보고서 세트 만들기 {#create-report-suite}

데이터를 집계하고 분석하려면 먼저 보고서 세트를 만들어야 합니다.

1. 이동 `https://analytics.adobe.com`.
1. Adobe ID를 사용하여 로그인합니다.
1. Click the **Analytics** icon.
1. 관리 **-> 보고서 세트로 이동합니다**.
1. 새로 **만들기 -> 보고서 세트를 클릭합니다**.
1. 양식 채우기:
   1. **보고서 세트 ID**: `yourSuiteID`
   1. **사이트 제목**: `Your suite description`
   1. **시간대**: 적합한
   1. **Go Live 날짜**: 오늘 날짜 또는 적절한 날짜
   1. **예상 일별 페이지 보기 수**: 100개 또는 적절한
1. 보고서 **세트 만들기를 클릭합니다**.

성공하면 다음 메시지가 녹색으로 표시됩니다. `Report Suite <yourReportSuite> has been successfully created.`

## 2단계 - 보고서 세트를 표시 {#make-visible}

새 보고서 세트를 사용하려면 이 보고서 세트를 표시해야 합니다.

1. 이동 `https://adminconsole.adobe.com`.
1. Adobe ID를 사용하여 로그인합니다.
1. Adobe **Analytics - &lt;yourSite>** 카드를 클릭합니다
1. Adobe **Analytics - &lt;yourSite>** 링크를 클릭합니다
1. Select the **Permissions** tab
1. 보고서 **세트** 행의 **편집** 단추 클릭
1. 1단계에서 만든 보고서 세트의 **+** 단추 [를](#create-report-suite) 클릭하여 **포함된 권한 항목** 카테고리에추가합니다.
1. **저장**&#x200B;을 클릭합니다.

## 3단계 - Adobe Launch와 AEM 사이트 통합 {#integrate-launch}

데이터를 생성하려면 론치를 AEM 사이트와 통합해야 합니다.

핵심 구성 요소 및 Adobe [Launch 문서를 통합하려면 Adobe 클라이언트 데이터 레이어를](launch-integration.md) 사용합니다.

## 4단계 - Adobe Launch에서 Adobe Analytics 확장 설치 및 구성 {#install-extension}

Adobe Analytics 익스텐션을 사용하면 Analytics와 Launch를 통합할 수 있습니다.

1. Adobe Launch에서 3단계에서 새로 만든 속성을 [선택합니다.](#integrate-launch)
1. 확장 **탭으로** 이동하여 **카탈로그를 선택합니다**.
1. Adobe **Analytics를 검색합니다**.
1. 설치를 **클릭합니다**.
1. 확장 기능을 구성합니다.
   1. 적절한 환경에 대해 **1단계에서** 만든 [Analytics 보고서 세트 ID를](#create-report-suite) 입력합니다.
   1. 문자 **세트를** UTF-8로 설정
1. 저장을 클릭합니다

## 5단계 - Adobe Launch에서 페이지 ID에 대한 데이터 요소 만들기 {#create-data-element}

페이지 ID를 추적하려면 론치에 데이터 요소가 필요합니다.

1. Adobe Launch에서 3단계에서 만든 속성을 [선택합니다.](#integrate-launch)
1. 데이터 요소 **탭을** 선택하고 데이터 요소 **추가를 클릭합니다**.
   1. **이름**: `dl-page-id`
   1. **확장**: **코어**
   1. **데이터 요소 유형**: **사용자 지정 코드**
1. 편집기 **열기를 클릭합니다.**
1. 편집기에서 코드를 입력합니다. `return adobeDataLayer.getState().page.id;`
1. **저장**&#x200B;을 클릭합니다.
1. 저장 **을** 클릭하여 데이터 요소를 만듭니다.

## 6단계 - Analytics에서 페이지 ID를 추적할 Adobe Launch에서 규칙 만들기 {#track-page}

규칙은 Analytics에서 페이지 ID와 같은 검색 속성을 추적할 수 있도록 해줍니다.

핵심 구성 요소 및 Adobe Launch [문서를 통합하려면 Adobe 클라이언트 데이터 레이어](launch-integration.md#launch-rule) 사용 5b부의 단계를 반복하여 Adobe Launch에서 다음 규칙을 추가합니다.

* **이름**: `track-dl-page-id`
* 이벤트:
   * **확장**: **코어**
   * **이벤트 유형**: **페이지 하단**
* 동작 1:
   * **확장**: **Adobe Analytics**
   * **작업 유형**: **변수 설정**
   * **prop1**: `%dl-page-id%`
* 동작 2:
   * **확장**: **Adobe Analytics**
   * **작업 유형**: **비콘 보내기**
   * s. **t() 확인: 데이터를 Adobe Analytics로 보내고 페이지 보기로 처리**

## 7단계 - Adobe Launch에서 규칙을 만들어 이미지 클릭 이벤트 등록 {#register-click}

규칙은 Analytics의 클릭 이벤트와 같은 검색 속성을 추적할 수 있도록 해줍니다.

핵심 구성 요소 및 Adobe Launch [문서를 통합하려면 Adobe 클라이언트 데이터 레이어](launch-integration.md#launch-rule) 사용 5b부의 단계를 반복하여 Adobe Launch에서 다음 규칙을 추가합니다.

* **이름**: `register-dl-image-click`
* 이벤트:
   * **확장**: **코어**
   * **이벤트 유형**: **페이지 하단**
* 동작 1:
   * **확장**: **코어**
   * **작업 유형**: **사용자 지정 코드**
   * 편집기: 다음 코드 입력

      ```
      var myListener = function(event) {
        _satellite.track('dlImageClicked', event.info.path);
      };
      adobeDataLayer.addEventListener('image clicked', myListener());
      ```

## 8단계 - Adobe Launch에서 규칙을 만들어 Analytics에서 이미지 클릭 이벤트를 추적합니다 {#track-click}

규칙은 Analytics의 클릭 이벤트와 같은 검색 속성을 추적할 수 있도록 해줍니다.

핵심 구성 요소 및 Adobe Launch [문서를 통합하려면 Adobe 클라이언트 데이터 레이어](launch-integration.md#launch-rule) 사용 5b부의 단계를 반복하여 Adobe Launch에서 다음 규칙을 추가합니다.

* **이름**: `track-dl-image-click`
* 이벤트:
   * **확장**: **코어**
   * **이벤트 유형**: **직접 호출**
   * **식별자**: `dlImageClicked`
* 동작 1:
   * **확장**: **Adobe Analytics**
   * **작업 유형**: **변수 설정**
   * **prop2**: 다음으로 설정 `%event.detail%`
* 동작 2:
   * **확장**: **Adobe Analytics**
   * **작업 유형**: **비콘 보내기**
   * s. **t() 확인: 데이터를 Adobe Analytics로 보내고 페이지 보기로 처리**

## 9단계 - 웹 사이트에 론치 코드 게시 {#publish-launch}

Launch에서 이러한 규칙 및 속성의 추적을 활성화하려면 코드를 게시해야 합니다.

1. Adobe **Launch** 탭에서 **게시** 탭을선택합니다.
1. 새 **라이브러리 추가를 클릭합니다**.
1. 이름 **입력** : `data-layer-analytics-1`.
1. 환경 **에서** 개발 **(개발)을 선택합니다**.
1. 변경된 모든 리소스 **추가를 클릭합니다**.
1. 세 가지 규칙(`track-dl-page-id`, `register-dl-image-click` 및 `track-dl-image-click`)에 대해 다음을 수행합니다.
1. 규칙 **-> 규칙 -> 최신** 버전을 선택하고 **선택 및 새 개정 만들기를 클릭합니다**.
1. **개발을 위한 저장 및 구축**&#x200B;을 클릭합니다.

## 10단계 - Adobe Analytics로 정보를 전송할 페이지를 트리거합니다. {#trigger-page}

이 단계에서는 Chrome 확장 프로그램 **Launch 및 DTM 스위치를 설치합니다**. 이 확장 기능을 사용하면 개발 환경에 론치 코드를 빌드하고 배포하기만 하면 됩니다. 스테이징 및 프로덕션 환경을 배포할 필요가 없습니다.

1. Discovery에서 Chrome 확장 **실행 및 DTM 스위치를** 설치합니다.
1. Launch **Switch** 아이콘을 클릭하고 Debug를 ON으로 *설정합니다*.
1. 페이지 다시 로드 `http://<host>:<port>/content/core-components-examples/library/image.html`.
1. 브라우저 콘솔을 열면 다음과 유사한 내용이 표시됩니다.

![Analytics 콘솔 출력](/help/assets/analytics-console-output.png)

>[!TIP]
>
>Chrome용 **Experience Cloud Debugger** 확장 프로그램을 설치하여 Adobe Launch 및 Analytics에 대한 특정 정보를 볼 수도 있습니다.

## 11단계 - Adobe Analytics에서 추적된 정보 보기 {#view-info}

이제 Adobe Analytics에서 트리거한 이벤트를 볼 수 있습니다.

1. 이동 `https://analytics.adobe.com`.
1. Adobe ID를 사용하여 로그인합니다.
1. Click the **Analytics** icon.
1. Select the **Reports** tab.
1. 오른쪽 상단의 드롭다운에서 1단계에서 만든 보고서 세트를 [선택합니다.](#create-report-suite)
1. 첫 번째 열에서 **사용자 지정 트래픽 -> 사용자 지정 트래픽 1-10 -> 사용자 지정 인사이트 1을** 선택하여 데이터 레이어에 저장된 추적된 페이지 ID(경로)를 봅니다. 다음과 같이 표시됩니다.

   ![커스텀 인사이트 1](/help/assets/custom-insight-1.png)

1. 사용자 **지정 인사이트 2에** 액세스하여 데이터 레이어에 저장된 추적된 이미지 경로를 봅니다. 다음과 같이 표시됩니다.

   ![커스텀 인사이트 2](/help/assets/custom-insight-2.png)

---
title: 캠페인 변수
description: 캠페인 변수를 자리 표시자로 사용하여 개인화된 이메일 콘텐츠를 작성합니다.
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 0%

---


# 캠페인 변수 {#campaign-variables}

캠페인 변수를 사용하여 개인화된 이메일 콘텐츠를 작성합니다. 캠페인 변수는 전자 메일 콘텐츠에 삽입할 수 있는 Adobe Campaign 값에 대한 자리 표시자 역할을 합니다. 컨텐츠가 Adobe Campaign을 통해 전송되면 Campaign은 해당 변수를 수신자의 개인화된 컨텐츠로 대체합니다.

## 사용량 {#usage}

이메일 코어 구성 요소 를 사용하면 공통 텍스트 필드 옆에 있는 개인화 버튼을 통해 캠페인 변수에 쉽게 액세스할 수 있습니다. 누르면 개인화 필드를 선택할 수 있는 대화 상자가 나타납니다.

사용 가능한 개인화 필드 목록은 Adobe Campaign 인스턴스와 동기화됩니다. 필드는 스키마에서 Adobe Campaign에서 관리됩니다 `nms:seedMember`. 의 모든 필드 `nms:seedMember` 수신자 테이블에도 있어야 합니다.

## Adobe Campaign 변수 선택 대화 상자 {#dialog}

Adobe Campaign 변수 선택 대화 상자는 이메일 코어 구성 요소의 많은 편집 대화 상자에서 사용할 수 있습니다. 이 기능을 사용하려면 **Adobe Campaign 변수 선택** 아이콘 을 클릭하여 제품에서 사용할 수 있습니다. 이 아이콘은 두 개의 양식을 사용할 수 있습니다.

![Adobe Campaign 단추](/help/email/assets/campaign-button.png)
![Adobe Campaign 변수 선택 아이콘](/help/email/assets/select-adobe-campaign-variable-icon.png)

두 아이콘을 모두 클릭하면 **Adobe Campaign 변수 선택** 대화 상자.

![Adobe Campaign 변수 선택 대화 상자](assets/select-campaign-variable-dialog.png)

열 보기를 사용하여 삽입할 변수를 찾습니다. 열의 노드를 클릭하면 오른쪽의 새 열에 있는 해당 하위 항목이 표시됩니다. 이러한 방식으로 변수 컨텐츠 구조를 탐색할 수 있습니다.

삽입할 변수를 선택한 다음 대화 상자의 오른쪽 맨 위에 있는 확인 표시를 클릭합니다.

![Adobe Campaign 변수 선택](assets/select-campaign-variable-dialog-selected.png)

그러면 변수가 이메일 코어 구성 요소의 편집 대화 상자 필드에 삽입됩니다.

![편집 대화 상자에 삽입된 Campaign 변수](assets/campaign-variable.png)

대화 상자 왼쪽 상단에서 언제든지 X 를 클릭하여 대화 상자를 취소하고 닫습니다.

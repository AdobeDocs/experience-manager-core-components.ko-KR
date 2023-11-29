---
title: 적응형 양식 핵심 구성 요소 - 바닥글
description: 적응형 양식 바닥글 핵심 구성 요소를 사용 또는 사용자 정의합니다.
role: Architect, Developer, Admin, User
exl-id: c8e7d3fe-4b82-4a80-8da2-19f6cff1e3e9
source-git-commit: e0ed415bd7f45fdca6fbbb8ba409604d9e82a647
workflow-type: ht
source-wordcount: '775'
ht-degree: 100%

---

# 바닥글 {#footer-adaptive-forms-core-component}

적응형 양식의 바닥글 구성 요소는 일반적으로 양식 하단에 표시되는 영역으로 저작권 고지, 관련 리소스에 대한 링크 또는 연락처 정보와 같은 정보를 포함합니다. 바닥글은 접근성이 필요한 사용자에게 도움이 될 수 있는 마지막 업데이트일과 같은 추가 정보를 제공할 수 있습니다.

**예**

![예](/help/adaptive-forms/assets/footer.png)

## 사용 {#reasons-to-use-footer}

양식에 바닥글 구성 요소를 포함하는 것이 유익한 몇 가지 이유는 다음과 같습니다.

- **법적 요구 사항**: 면책 조항, 저작권 고지 또는 기타 법적 정보를 포함하기 위해 일부 양식이 필요할 수 있습니다. 바닥글에 이 정보를 편리하게 포함할 수 있습니다.

- **탐색**: 바닥글은 개인정보 처리방침, 서비스 약관 또는 연락처 페이지와 같은 웹 사이트의 다른 중요한 페이지에 대한 링크를 제공할 수 있습니다.

- **브랜딩**: 바닥글을 사용하여 로고 또는 기타 브랜딩 요소를 포함하여 조직 또는 웹 사이트의 정체성을 강화할 수 있습니다.

- **일관성**: 바닥글은 양식의 디자인과 레이아웃에 일관성을 제공하여 사용자가 보다 직관적이고 쉽게 탐색할 수 있도록 합니다.

- **추가 컨텍스트**: 바닥글은 양식을 설명하는 텍스트나 관련 리소스에 대한 링크와 같은 추가 컨텍스트를 양식에 제공하여 양식을 보다 유익하고 사용자 친화적으로 만들 수 있습니다.

## 버전 및 호환성 {#version-and-compatibility}

적응형 양식 아코디언 핵심 구성 요소는 Cloud Service의 핵심 구성 요소 2.0.4 및 AEM 6.5.16.0 Forms 이상의 핵심 구성 요소 1.1.12 일부로 2023년 2월에 릴리스되었습니다. 다음 표에서는 지원되는 모든 버전, AEM 호환성 및 해당 문서에 대한 링크를 보여 줍니다.

| 구성 요소 버전 | AEM as a Cloud Service | AEM 6.5.16.0 Forms 이상 |
|---|---|---|
| v1 | 호환 가능 <br>[2.0.4](/help/adaptive-forms/version.md) 및 이후 릴리스 | <br>[릴리스 1.1.12](/help/adaptive-forms/version.md) 이상과 호환합니다(2.0.0 이전 버전). |

핵심 구성 요소 버전 및 릴리스에 대한 자세한 내용은 [핵심 구성 요소 버전](/help/adaptive-forms/version.md) 문서를 참조하십시오.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## 기술 세부 정보 {#technical-details}

적응형 양식 바닥글 핵심 구성 요소에 대한 최신 정보는 [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/footer/v1/footer)의 기술 설명서에서 확인할 수 있습니다. 핵심 구성 요소 개발에 대한 자세한 내용은 [핵심 구성 요소 개발자 설명서](/help/developing/overview.md)를 확인하십시오.


## 구성 대화 상자 {#configure-dialog}

구성 대화 상자를 사용하여 방문자를 위한 바닥글 경험을 손쉽게 사용자 정의할 수 있습니다. 바닥글 옵션을 간편하게 정의하여 원활한 사용자 경험을 제공할 수도 있습니다.

![속성 탭](/help/adaptive-forms/assets/footer_propertiestab.png)

- **편집 대화 상자**
편집 대화 상자는 사용자가 바닥글에 대한 텍스트를 만들 수 있는 서식 있는 표준 텍스트 서식 도구를 제공합니다.

- **볼드체** - 이 옵션은 선택한 텍스트에 볼드체 서식 지정을 적용하거나 커서 다음에 입력한 텍스트를 볼드체로 서식 지정하는 데 사용됩니다. 키보드 단축키는 `Ctrl+B`입니다.

- **이탤릭체** - 선택한 텍스트에 이탤릭체 서식 지정을 적용하거나 커서 다음에 입력한 텍스트를 이탤릭체로 서식 지정하는 데 사용됩니다. 키보드 단축키는 `Ctrl+I`입니다.

![글머리 기호 옵션](/help/adaptive-forms/assets/footer_bullet.png)


- **글머리 기호**

   - **글머리 기호 아이콘** - 선택한 텍스트 서식을 글머리 기호 목록으로 서식 지정하거나 커서 다음에 글머리 기호 목록을 삽입하는 데 사용됩니다. 글머리 기호 목록을 종료하려면 글머리 기호 버튼을 다시 탭 또는 클릭하거나 캐리지 리턴을 2번 입력합니다.

   - **번호 매기기 목록 아이콘** - 선택한 텍스트 서식을 번호 매기기 목록으로 서식 지정하거나 커서 다음에 번호 매기기 목록을 삽입하는 데 사용됩니다. 번호 매기기 목록을 종료하려면 번호 매기기 버튼을 다시 탭 또는 클릭하거나 캐리지 리턴을 2번 입력합니다.

   - **내어쓰기 아이콘** - 선택한 텍스트나 커서 다음에 입력한 텍스트의 들여쓰기 레벨을 낮추는 데 사용됩니다. 선택한 텍스트나 커서의 위치가 이미 들여 쓴 경우에만 활성화됩니다.

   - **들여쓰기 아이콘** - 선택한 텍스트나 커서 다음에 입력한 텍스트의 들여쓰기 레벨을 높이는 데 사용됩니다.

![하이퍼링크 옵션](/help/adaptive-forms/assets/footer_link.png)

- **하이퍼링크**

   - **경로** - 경로를 입력합니다.
      1. 선택 열기 대화 상자를 통해 AEM의 경로를 선택합니다.
      1. 링크가 AEM 내에 없는 경우 절대 URL을 입력합니다.
      1. 절대 경로가 아닌 경로는 AEM의 상대 경로로 해석됩니다.

   - **대체 텍스트** - 링크에 대한 대체 설명 텍스트를 입력합니다.

   - **대상** - 링크 동작을 선택합니다.
      - 대상
      - 동일한 탭
      - 새 탭
      - 상위 프레임
      - 맨 위 프레임

   - **연결 해제 아이콘** - 이 옵션을 사용하여 선택한 텍스트에 이미 적용된 링크를 제거합니다. 이 옵션은 링크가 이미 선택된 경우에만 활성화됩니다.

   - **단락 형식 아이콘** - 이 옵션을 사용하면 선택한 텍스트에 단락 형식을 적용할 수 있습니다. 또한 커서 뒤에 삽입된 텍스트의 서식을 지정하는 데 도움이 됩니다. 제목의 머리말 수준을 정의합니다.

- **ID**: 이 옵션을 통해 HTML과 데이터 레이어에서 구성 요소의 고유 식별자를 제어할 수 있습니다.

   - 비워 두면 고유 ID는 자동으로 * 생성되고 결과 페이지 검사를 통해 발견될 수 있습니다.
   - ID가 지정된 경우 작성자는 ID가 고유한지 확인해야 합니다.
   - ID가 변경되면 CSS, JS 및 데이터 레이어 추적에 영향을 미칠 수 있습니다.

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## 관련 문서 {#related-articles}

{{more-like-this}}

## 추가 참조 {#see-also}

{{see-also}}

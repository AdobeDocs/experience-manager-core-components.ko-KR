---
title: 핵심 이메일 구성 요소 버전
description: 핵심 이메일 구성 요소는 릴리스로 게시됩니다.
role: Architect, Developer, Admin, User
exl-id: 9733659a-641c-4a98-8d10-84e93e0e0a5d
source-git-commit: 91cf78d4c6622bbdec5ac7d22954c9c081c839d2
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 87%

---


# 핵심 이메일 구성 요소 버전 {#core-components-versions}

이메일 핵심 구성 요소의 현재 릴리스는 1.3.0이며 AEM 6.5(온-프레미스 및 AMS)와 호환됩니다.

요구 사항 및 설치에 대한 자세한 내용은 각각 이메일 핵심 구성 요소 소개 문서의 [요구 사항 섹션](/help/email/introduction.md#requirements) 및 이메일 핵심 구성 요소 사용 문서의 [설치 섹션](/help/email/using.md#installing-the-email-core-components)을 참조하십시오.

## 릴리스 내역 및 호환성 {#release-history-and-compatibility}

이메일 핵심 구성 요소는 유연하고, 지원되는 모든 AEM 버전과 호환할 수 있도록 설계되었습니다. 이메일 핵심 구성 요소의 버전 내역에 대한 자세한 내용은 [GitHub에서 확인할 수 있습니다.](https://github.com/adobe/aem-core-email-components/releases) 단, 다음 테이블에 이메일 핵심 구성 요소 릴리스와 AEM 릴리스 및 Java 버전과의 호환성에 대한 개요가 나와 있습니다.

| 릴리스 | 설명 | AEM 6.5 | AEM 6.5 LTS | 핵심 구성 요소 | Java | 릴리스 일자 |
|---|---|---|---|---|---|---|
| [1.3.0](https://github.com/adobe/aem-core-email-components/releases/tag/core.email.components.reactor-1.3.0) | 이 릴리스는 포함된 jsup 라이브러리를 업데이트합니다. | 6.5.14.0+ | - | [2.21.2+](/help/versions.md) | 8, 11 | 2024년 6월 28일 |
| [1.2.2](https://github.com/adobe/aem-core-email-components/releases/tag/core.email.components.reactor-1.2.2) | 이 유지 관리 릴리스는 선택기 필터링을 수정하고 `SelectorParseException`을(를) 해결했으며 다른 오류를 해결했습니다. | 6.5.14.0+ | - | [2.21.2+](/help/versions.md) | 8, 11 | 2023년 5월 24일 |
| [1.2.0](https://github.com/adobe/aem-core-email-components/releases/tag/core.email.components.reactor-1.2.0) | 이 릴리스에는 Selenium e2e 테스트가 도입되었으며 다양한 버그 수정이 포함되었습니다. | 6.5.14.0+ | - | [2.21.2+](/help/versions.md) | 8, 11 | 2022년 11월 29일 |
| [1.0.0](https://github.com/adobe/aem-core-email-components/releases/tag/core.email.components.reactor-1.0.0) | 첫 번째 공개 릴리스, 자세한 내용은 릴리스 정보 참조 | 6.5.14.0+ | - | [2.21.2+](/help/versions.md) | 8, 11 | 2022년 11월 29일 |
| [0.18.0](https://github.com/adobe/aem-core-email-components/releases/tag/v0.18.0) | 수정 사항 | 6.5.13.0+ |  |  | 8, 11 | 2022년 9월 30일 |
| [0.17.0](https://github.com/adobe/aem-core-email-components/releases/tag/v0.17.0) | 수정 사항 | 6.5.13.0+ |  |  | 8, 11 | 2022년 9월 27일 |
| [0.16.0](https://github.com/adobe/aem-core-email-components/releases/tag/v0.16.0) | 수정 사항 | 6.5.13.0+ |  |  | 8, 11 | 2022년 9월 14일 |
| [0.14.0](https://github.com/adobe/aem-core-email-components/releases/tag/v0.14.0) | iOS에서 Outlook에 대한 미디어 쿼리 수정 | 6.5.13.0+ |  |  | 8, 11 | 2022년 8월 8일 |
| [0.13.0](https://github.com/adobe/aem-core-email-components/releases/tag/v0.13.0) | 래퍼 DIV 성능 수정, 리치 텍스트의 처리 링크 수정 | 6.5.13.0+ |  |  | 8, 11 | 2022년 7월 27일 |
| [0.11.0](https://github.com/adobe/aem-core-email-components/releases/tag/v0.11.0) | 세분화 구성 요소에 대한 사용자 정의 세그먼트 지원, HTML 인라인, 수정 | 6.5.13.0+ |  |  | 8, 11 | 2022년 7월 6일 |
| [0.10.0](https://github.com/adobe/aem-core-email-components/releases/tag/v0.10.0) | 페이지 구성 요소 열 설정에 대한 페이지 정책 활성화, 세분화 구성 요소 업데이트, 코드 적용 범위 개선 | 6.5.13.0+ |  |  | 8, 11 | 2022년 6월 15일 |
| [0.9.0](https://github.com/adobe/aem-core-email-components/releases/tag/v0.9.0) | 제목 및 컨테이너 구성 요소 수정 및 업데이트 | 6.5.13.0+ |  |  | 8, 11 | 2022년 6월 1일 |
| [0.8.0](https://github.com/adobe/aem-core-email-components/releases/tag/v0.8.0) | 티저 구성 요소 추가, 수정, 코드 적용 범위 개선 | 6.5.13.0+ |  |  | 8, 11 | 2022년 5월 19일 |
| [0.7.0](https://github.com/adobe/aem-core-email-components/releases/tag/v0.7.0) | 수정 사항 | 6.5.13.0+ |  |  | 8, 11 | 2022년 5월 4일 |
| [0.6.0](https://github.com/adobe/aem-core-email-components/releases/tag/v0.6.0) | 제목, 버튼 및 경험 조각 구성 요소 추가, ContextHub 지원 추가 | 6.5.13.0+ |  |  | 8, 11 | 2022년 4월 20일 |
| [0.5.0](https://github.com/adobe/aem-core-email-components/releases/tag/v0.5.0) | 스타일 인라이너 및 콘텐츠 조각 구성 요소 추가 | 6.5.13.0+ |  |  | 8, 11 | 2022년 4월 7일 |
| [0.4.0](https://github.com/adobe/aem-core-email-components/releases/tag/v0.4.0) | URL 외부화, 개인화 및 세분화 구성 요소 추가 | 6.5.13.0+ |  |  | 8, 11 | 2022년 3월 23일 |
| [0.3.0](https://github.com/adobe/aem-core-email-components/releases/tag/v0.3.0) | 텍스트 및 컨테이너 구성 요소 추가, 작성 UI 추가, 수정 | 6.5.13.0+ |  |  | 8, 11 | 2022년 3월 9일 |
| [0.2.0](https://github.com/adobe/aem-core-email-components/releases/tag/v0.2.0) | 페이지 구성 요소 및 다양한 POC가 포함된 초기 프리릴리스 | 6.5.13.0+ |  |  | 8, 11 | 2022년 2월 24일 |

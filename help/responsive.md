---
title: 핵심 구성 요소의 반응형 디자인
description: 핵심 구성 요소의 반응형 디자인과 이것이 프로젝트에 어떤 영향을 미칠 수 있는지 알아보십시오.
role: Architect, Developer, Admin, User
exl-id: c0eff174-6803-4b44-aeb1-eae3bc8a36ea
source-git-commit: 5f49fb45869d1721e16a787a2c6ff927b6ad49fe
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 100%

---

# 핵심 구성 요소의 반응형 디자인 {#responsive-design}

모든 핵심 구성 요소는 완벽하게 반응하도록 설계되어 여러 장치에서 원활한 경험을 보장합니다. 일부 고급 구성 요소(예: [슬라이드,](/help/components/carousel.md) [탭](/help/components/tabs.md) 및 [아코디언 구성 요소](/help/components/accordion.md))에는 모든 상태에서 응답성을 유지하기 위해 구현 프로젝트의 컨텍스트 내에서 특별한 고려 사항이 필요할 수 있습니다.

이러한 구성 요소가 반응형 동작을 나타낼 수 있는 다양한 방식을 고려하여, 핵심 구성 요소를 기본적으로 간단하게 즉시 사용 가능하도록 유지하려는 Adobe의 노력의 일환으로, 세부적인 반응형 측면을 구현할 책임은 의도적으로 프로젝트에 맡겨집니다.

예를 들어, 좁은 화면에서 탭 구성 요소는 넓은 탭을 새 줄로 나누거나, 세로 스크롤을 허용하거나, 탭을 드롭다운으로 변환하거나, 아코디언 스타일을 채택하여 조정할 수 있습니다. 이러한 모든 동작을 구현하면 성능에 잠재적인 영향을 미칠 수 있으므로 [clientlib](/help/developing/including-clientlibs.md#provided)가 완전한 솔루션 대신 구현자를 위한 출발점으로 사용됩니다.

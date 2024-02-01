---
title: 핵심 구성 요소의 응답형 디자인
description: 핵심 구성 요소의 응답형 디자인과 이것이 프로젝트에 어떤 영향을 미칠 수 있는지 알아봅니다.
role: Architect, Developer, Admin, User
source-git-commit: d39fe0084522f67664203a026340b23d325c1883
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---


# 핵심 구성 요소의 응답형 디자인 {#responsive-design}

모든 핵심 구성 요소는 완벽한 응답을 제공하도록 설계되어 장치 간에 원활한 경험을 제공합니다. 다음과 같은 일부 고급 구성 요소에 유의해야 합니다. [회전판,](/help/components/carousel.md) [탭,](/help/components/tabs.md) 및 [아코디언 구성 요소,](/help/components/accordion.md) 는 모든 조건에서 응답성을 유지하기 위해 구현 프로젝트 컨텍스트 내에서 특정 고려가 필요할 수 있습니다.

이러한 구성 요소가 반응형 동작을 나타낼 수 있는 다양한 방법을 고려할 때 핵심 구성 요소를 즉시 사용할 수 있도록 유지하려는 Adobe의 노력에 따라 반응형 세부 요소의 구현에 대한 책임은 프로젝트에 맡깁니다.

예를 들어 좁은 화면에서 탭 구성 요소는 넓은 탭을 새 라인으로 나누거나, 세로 스크롤을 허용하거나, 탭을 드롭다운으로 변환하거나, 아코디언 스타일을 채택하여 조정할 수 있습니다. 이러한 모든 동작을 구현하면 성능에 미칠 수 있는 잠재적 영향 때문에 [clientlibs](/help/developing/including-clientlibs.md#provided) 는 완전한 해결이 아니라 구현자의 시작점으로 사용됩니다.

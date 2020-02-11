---
product: Adobe Experience Manager
git-repo: https://github.com/AdobeDocs/experience-manager-core-components.en
index: y
solution-title: AEM에 대한 학습 및 지원
solution-hub-url: https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/home.html
getting-started-title: AEM용 개발 시작
getting-started-url: https://docs.adobe.com/content/help/en/experience-manager-cloud-service/core-concepts/home.html
tutorials-title: AEM 자습서
tutorials-url: https://docs.adobe.com/content/help/en/experience-manager-learn/cloud-service/overview.html
translation-type: tm+mt
source-git-commit: a3085d266baf32649fda528a7f4703e133d03ab7

---


# 내부용 메타데이터

GitHub 저작 시스템의 메타데이터는 계층적이며 다음과 같은 선례 수준을 증가시킵니다.

1. metadata.md
1. ToC
1. 기사

metadata.md 파일에 정의된 메타데이터는 전체 보고서에 적용되지만 ToC 및 아티클 수준에서 재정의할 수 있습니다. 메타데이터를 재정의하는 작업은 가능한 가장 낮은 수준에서 수행해야 합니다.

Experience-manager-core-components.en repo의 메타데이터는 최소한으로 필요합니다.

metadata.md

* `product`
* `git-repo`
* `index: y`
* `solution-title`
* `solution-hub-url`
* `getting-started-title`
* `getting-started-url`
* `tutorials-title`
* `tutorials-url`

ToCs

* `sub-product`
* `user-guide-title`

기사

* `title`
* `description`
* `index: n` (이전 버전의 구성 요소에만 해당)

메타데이터에 대한 자세한 내용은 [내부 작성 안내서를 참조하십시오.](https://docs.adobe.com/help/en/collaborative-doc-instructions/collaboration-guide/markdown/metadata.html#solution-metadata)

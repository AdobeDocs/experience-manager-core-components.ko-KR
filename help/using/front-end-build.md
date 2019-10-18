---
title: AEM 프로젝트 원형 프런트 엔드 빌드
seo-title: AEM 프로젝트 원형 프런트 엔드 빌드
description: AEM 기반 응용 프로그램용 프로젝트 템플릿
seo-description: AEM 기반 응용 프로그램용 프로젝트 템플릿
contentOwner: 보허트
content-type: 참조
topic-tags: 핵심 구성 요소
translation-type: tm+mt
source-git-commit: 0a61f4e6d1ad8b4d5e3778018838dc70d496e1fc

---


# AEM 프로젝트 원형 프런트 엔드 빌드 {#aem-project-archetype-front-end-build}

AEM 프로젝트 전형(선택 사항)에는 다음 기능이 포함된 웹팩을 기반으로 하는 전용 프런트 엔드 빌드 메커니즘이 포함되어 있습니다.

* 전체 TypeScript, ES6 및 ES5 지원(적용 가능한 웹 팩 래퍼 포함)
* TSLint 규칙 세트를 사용한 TypeScript 및 JavaScript 린팅
* 기존 브라우저 지원을 위한 ES5 출력
* Globbing
   * 어디에서나 가져오기 추가 필요 없음
   * 이제 모든 JS 및 CSS 파일을 각 구성 요소에 추가할 수 있습니다.
      * 우수 사례는 `/clientlib/js`또는 `/clientlib/css`또는 `/clientlib/scss`
   * 모든 것이 웹 팩을 통해 실행되므로 `.content.xml` 필요 `js.txt`또는`css.txt` 파일 없음
   * 글로벌 번호는 `/component/` 폴더 아래의 모든 JS 파일을 가져옵니다.
      * Webpack을 사용하면 CSS/SCSS 파일을 JS 파일을 통해 체인으로 연결할 수 있습니다.
      * 그들은 두 개의 진입점을 통해 `sites.js` , 그리고 `vendors.js`있습니다.
   * AEM에서 사용되는 유일한 파일은 출력 파일이며, 출력 파일뿐만 `site.js` 아니라, `site.css``/clientlib-site` `dependencies.js` `dependencies.css` 및 `/clientlib-dependencies`
* 청크
   * 기본(사이트 js/css)
   * 공급업체(종속성 js/css)
* 전체 Sass/Scss 지원(Sass는 Webpack을 통해 CSS로 컴파일됨).

## 설치 {#installation}

1. NodeJS [](https://nodejs.org/en/download/) (v10+)를 전역적으로 설치합니다. npm도 설치합니다.
1. 프로젝트에서 ui.frontend로 이동하고 실행합니다 `npm install`.

## 사용량 {#usage}

다음 npm 스크립트는 프런트 엔드 워크플로우를 구동합니다.

* `npm run dev` - JS 최적화가 비활성화되어 있고(트리 흔들기 등) 소스 맵이 활성화되어 있으며 CSS 최적화가 비활성화되어 있습니다.
* `npm run prod` - JS 최적화(트리 흔들기 등)가 활성화된 완벽한 빌드, 소스 맵 비활성화 및 CSS 최적화가 활성화된 소스 맵

## 출력 {#output}

### 일반 {#general}

* 사이트 - `site.js` clientlib-site 폴더에 `site.css` 만들어집니다.
* 종속성 - `dependencies.js` clientlib-dependencies 폴더에 `dependencies.css` 만들어집니다.

### JavaScript {#javascript}

* 최적화 - 프로덕션 빌드의 경우 사용 중이거나 호출되지 않는 모든 JS가 제거됩니다.

### CSS {#css}

* 자동 수정 - 모든 CSS는 사전 수정을 통해 실행되며 사전 수정이 필요한 모든 속성은 자동으로 CSS에 추가됩니다.
* 최적화 - 이후 모든 CSS는 다음 기본 규칙에 따라 표준화하는 최적기(cssnano)를 통해 실행됩니다.
   * 브라우저 호환성 및 압축을 모두 보장하여 가능한 경우 CSS 계산 표현식을 줄이고 등가 길이, 시간 및 각도 값 간을 전환합니다. 기본적으로 길이 값은 변환되지 않습니다.
   * 규칙, 선택기 및 선언과 관련된 주석 제거
   * 중복된 규칙, at-rules 및 선언을 제거합니다.
      * 이 기능은 정확한 복제에만 작동합니다.
   * 출력에 영향을 주지 않으므로 빈 규칙, 미디어 쿼리 및 빈 선택기가 있는 규칙을 제거합니다.
   * 인접한 규칙을 선택기와 겹쳐진 속성/값 쌍으로 병합
   * CSS 파일에 하나의 @charset만 있고 문서 맨 위로 이동하는지 확인
   * 결과 출력이 작으면 CSS 초기 키워드를 실제 값으로 바꿉니다.
   * SVGO를 사용하여 인라인 SVG 정의 압축
* 정리 - 생성된 CSS, JS 및 Map 파일을 On-Demand로 정리하기 위한 명시적 정리 작업을 포함합니다.
* 소스 매핑 - 개발 빌드만

>[!NOTE]
>프런트 엔드 빌드 옵션은 일반 구성 파일을 공유하는 개발 전용 및 prod 전용 웹 팩 구성 파일을 사용합니다. 이렇게 하면 개발 및 제작 설정을 개별적으로 수정할 수 있습니다.

원문: [atlassian/react-beautiful-dnd](https://github.com/atlassian/react-beautiful-dnd)

번역 일자: 2020년 10월 7일 (수)

<p align="center">
  <img src="https://user-images.githubusercontent.com/2182637/53611918-54c1ff80-3c24-11e9-9917-66ac3cef513d.png" alt="react beautiful dnd logo" />
</p>
<h1 align="center">react-beautiful-dnd <small><sup>(rbd)</sup></small></h1>

<div align="center">

**예쁘고 쉬운** [`React`](https://facebook.github.io/react/) 리스트 드래그 앤 드롭

[![CircleCI branch](https://img.shields.io/circleci/project/github/atlassian/react-beautiful-dnd/master.svg)](https://circleci.com/gh/atlassian/react-beautiful-dnd/tree/master)
[![npm](https://img.shields.io/npm/v/react-beautiful-dnd.svg)](https://www.npmjs.com/package/react-beautiful-dnd)

![quote application example](https://user-images.githubusercontent.com/2182637/53614150-efbed780-3c2c-11e9-9204-a5d2e746faca.gif)

[이 예시도 한 번 살펴보세요!](https://react-beautiful-dnd.netlify.com/iframe.html?selectedKind=board&selectedStory=simple)

</div>

## 주요 특징 (Core characteristics)

- 아이템 이동이 아름답고 [자연스러움](/docs/about/animations.md) 💐
- [접근성이 좋음](/docs/about/accessibility.md): 키보드와 스크린 리더 적극 지원 ♿️
- [기능성이 뛰어남](/docs/support/media.md) 🚀
- API가 깔끔하고 뛰어나 시작하기에 편함
- 기본적인 브라우저 상호작용의 작동이 뛰어남
- [독창적인 스타일](/docs/guides/preset-styles.md)
- 추가로 DOM을 생성할 필요가 없음 - 플렉스박스(flexbox)와 포커스 매니지먼트(focus management)에 친화적입니다!

## 시작하기 (Get started) 👩‍🏫

`react-beautiful-dnd`를 보다 쉽고 빠르게 시작할 수 있도록 [`egghead.io` 무료 강좌 🥚](https://egghead.io/courses/beautiful-and-accessible-drag-and-drop-with-react-beautiful-dnd)를 준비했습니다.

[![course-logo](https://user-images.githubusercontent.com/2182637/43372837-8c72d3f8-93e8-11e8-9d92-a82adde7718f.png)](https://egghead.io/courses/beautiful-and-accessible-drag-and-drop-with-react-beautiful-dnd)

## 현재 지원되는 기능 (Currently supported feature set) ✅

- 세로 리스트 ↕
- 가로 리스트 ↔
- 리스트간의 이동(▤ ↔ ▤)
- [가상 리스트 지원 👾](/docs/patterns/virtual-lists.md) - 10,000 아이템 잠금 해제 @ 60fps
- [아이템 결합](/docs/guides/combining.md)
- 마우스 🐭와 키보드 🎹♿️, 그리고 터치 👉📱 (휴대폰과 태블릿 기기 등등) 지원
- [멀티 드래그 지원](/docs/patterns/multi-drag.md)
- 단말기기 지원 ♿️ - 별도의 설치나 구성 📦 없이 바로 사용할 수 있어 영어권 스크린 리더에게 최고의 경험을 제공합니다. 또한, 필요한 이들을 위해 사용자 맞춤 설정과 국제화를 지원합니다 💖.
- 상황에 맞는 [드래깅(dragging)](/docs/api/draggable.md#optional-props)과 [드로핑(dropping)](/docs/api/droppable.md#conditionally-dropping)
- 한 페이지에 비치할 수 있는 여러 개의 개별적인 리스트
- 아이템 크기 조정 - 드래그 가능한 아이템은 서로 다른 높이(세로 리스트)와 넓이(가로 리스트)로 설정할 수 있습니다.
- [드래그 중 아이템을 더하거나 뺄 수 있음](/docs/guides/changes-while-dragging.md)
- `<table>` 재배치 - [표 사용 양식](/docs/patterns/tables.md)
- [자동 스크롤](/docs/guides/auto-scrolling.md) - 드래그할 때 컨테이너나 창이 자동으로 스크롤됩니다(키보드에도 지원되는 기능입니다 🔥).
- 사용자 맞춤 드래그 핸들 - 아이템의 일부만 이동시킬 수 있습니다.
- 드래그 중 아이템을 다른 아이템으로 이동시킬 수 있음(복사, 포털) - [`<Draggable />` 리패런팅(reparenting)](/docs/guides/reparenting.md)
- [드래그 앤 드롭 명령어 경험(scripted experience) 만들기 🎮](/docs/sensors/sensor-api.md)
- [다양한 입력(input) 🕹](/docs/sensors/sensor-api.md)을 위한 익스텐션 허용
- [`@atlaskit/tree`](https://atlaskit.atlassian.com/packages/core/tree) 패키지를 통한 🌲 나무 지원
- `<Droppable />` 리스트는 스크롤 가능한 parent가 없는 스크롤 컨테이너 또는 스크롤 컨테이너의 child가 될 수 있음
- 개별적인 중첩 리스트 - 리스트는 타 리스트의 child가 될 순 있지만, 아이템을 parent 리스트에서 child 리스트로 드래그 할 순 없습니다.
- Server side rendering(SSR) 호환 - [resetServerContext()](/docs/api/reset-server-context.md)를 참고하세요.
- [상호적인 중첩 요소](/docs/api/draggable.md#interactive-child-elements-within-a-draggable-)와의 원활한 사용

## 제작 동기 (Motivation) 🤔

`react-beautiful-dnd`는 시각장애인을 포함한 누구나 예쁜 드래그 앤 드롭 리스트를 만들 수 있게 하기 위해 제작되었습니다. 제작 동기와 과정을 엿보고 싶은 분들은 이 링크를 참고해주세요:

- 📖 [드래그 앤 드롭 다시 생각하기](https://medium.com/@alexandereardon/rethinking-drag-and-drop-d9f5770b4e6b)
- 🎧 [React 팟캐스트: 빠르고 접근성 좋고 아름다운 드래그 앤 드롭](https://reactpodcast.simplecast.fm/17)

## 참고사항 (Not for everyone) ✌️

React를 사용한 드래그 앤 드롭 라이브러리는 많습니다. 그 중 가장 주목할 만한 라이브러리는 [`react-dnd`](https://github.com/react-dnd/react-dnd)입니다. `react-dnd`는 훌륭한 드래그 앤 드롭 기초 요소를 포함하고 있는데, 이는 [일관성이 떨어지는](https://www.quirksmode.org/blog/archives/2009/09/the_html5_drag.html) html5 드래그 앤 드롭 기능과 함께 사용하기 좋습니다. `react-beautiful-dnd`는 리스트(가로, 세로, 리스트 간의 이동, 중첩 리스트 등등)를 위해 만들어진 추상화로, 기능성과 더불어 강력하고 자연스러우며 아름다운 드래그 앤 드롭 경험을 제공합니다. 하지만 `react-dnd`처럼 제공하는 기능이 많지 않으므로 경우에 따라 `react-beautiful-dnd`가 맞지 않을 수 있습니다.

## 관련 문서 (Documentation) 📖

### `react-beautiful-dnd`에 대하여 👋

- [설치방법](/docs/about/installation.md)
- [예시와 샘플](/docs/about/examples.md)
- [시작하기](https://egghead.io/courses/beautiful-and-accessible-drag-and-drop-with-react-beautiful-dnd)
- [디자인 법칙](/docs/about/design-principles.md)
- [애니메이션](/docs/about/animations.md)
- [접근성](/docs/about/accessibility.md)
- [지원되는 브라우저](/docs/about/browser-support.md)

### 센서 🔉

> The ways in which somebody can start and control a drag

- [마우스 드래깅(dragging) 🐭](/docs/sensors/mouse.md)
- [터치 드래깅(dragging) 👉📱](/docs/sensors/touch.md)
- [키보드 드래깅(dragging) 🎹♿️](/docs/sensors/keyboard.md)
- [센서 만들기](/docs/sensors/sensor-api.md) (명령어 경험(scripted experience)을 포함한 어느 종류의 입력(input)에나 적용 가능)

### API 🏋️‍

![diagram](https://user-images.githubusercontent.com/2182637/53607406-c8f3a780-3c12-11e9-979c-7f3b5bd1bfbd.gif)

- [`<DragDropContext />`](/docs/api/drag-drop-context.md) - _앱에서 드래그 앤 드롭을 사용하고 싶은 부분을 감싸는 태그_
- [`<Droppable />`](/docs/api/droppable.md) - _드롭 가능한 위치; `<Draggable />`를 포함함_
- [`<Draggable />`](/docs/api/draggable.md) - _드래그 가능한 것_
- [`resetServerContext()`](/docs/api/reset-server-context.md) - _Server side rendering(SSR)을 위한 유틸리티_

### 사용 안내서 🗺

- [`<DragDropContext />` 리스폰더(Responders)](/docs/guides/responders.md) - _`onDragStart`와 `onDragUpdate`, `onDragEnd`, 그리고 `onBeforeDragStart`_
- [`<Draggable />` 결합하기](/docs/guides/combining.md)
- [자주 발생하는 셋업 문제들](/docs/guides/common-setup-issues.md)
- [`innerRef` 사용하기](/docs/guides/using-inner-ref.md)
- [셋업 문제 감지와 에러 수정](/docs/guides/setup-problem-detection-and-error-recovery.md)
- [`draggableId`와 `droppableId`를 사용하는 규칙](/docs/guides/identifiers.md)
- [브라우저 포커스(browser focus) 보유](/docs/guides/browser-focus.md)
- [드롭 애니메이션 수정/제거하기](/docs/guides/drop-animation.md)
- [자동 스크롤](/docs/guides/auto-scrolling.md)
- [스크린 리더 조작하기](/docs/guides/screen-reader.md)
- [Html5 `doctype` 사용하기](/docs/guides/doctype.md)
- [`TypeScript`과 `flow`: 타입(type)에 대하여](/docs/guides/types.md)
- [`<svg>` 드래그하기](/docs/guides/dragging-svgs.md)
- [사진 깜빡임을 방지하는 법](/docs/guides/avoiding-image-flickering.md)
- [보이지 않는 프리셋(preset) 스타일](/docs/guides/preset-styles.md)
- [스크롤 컨테이너 감지하는 법](/docs/guides/how-we-detect-scroll-containers.md)
- [Dom 이벤트 사용법](/docs/guides/how-we-use-dom-events.md) - _`react-beautiful-dnd`를 기반으로 하여 만들 때 유용함_
- [드래그하는 동안 `<Draggable />` 추가하기(11.x 적용)](/docs/guides/changes-while-dragging.md) - _⚠️ 심화과정_
- [Content Security Policy (CSP) 셋업하기](/docs/guides/content-security-policy.md)

### 패턴 👷‍

- [가상 리스트 👾](/docs/patterns/virtual-lists.md)
- [멀티 드래그](/docs/patterns/multi-drag.md)
- [표](/docs/patterns/tables.md)
- [`<Draggable />` 리패런팅(reparenting)](/docs/guides/reparenting.md) - _개인 포털(portal)에 우리의 복제된 API를 사용함_

### 지원 👩‍⚕️

- [건강한 공학(Engineering health)](/docs/support/engineering-health.md)
- [커뮤니티(community)와 애드온(addon)](/docs/support/community-and-addons.md)
- [출시 노트와 체인지로그(changelog)](https://github.com/atlassian/react-beautiful-dnd/releases)
- [업그레이드](/docs/support/upgrading.md)
- [로드맵](https://github.com/atlassian/react-beautiful-dnd/issues)
- [미디어](/docs/support/media.md)

## 번역문 (Read this in other languages) 🌎

- [![kr](https://raw.githubusercontent.com/gosquared/flags/master/flags/flags/shiny/24/South-Korea.png) **한글/Korean**](https://github.com/LeeHyungGeun/react-beautiful-dnd-kr)
- [![ru](https://raw.githubusercontent.com/gosquared/flags/master/flags/flags/shiny/24/Russia.png) **На русском/Russian**](https://github.com/vtereshyn/react-beautiful-dnd-ru)
- [![pt](https://raw.githubusercontent.com/gosquared/flags/master/flags/flags/shiny/24/Brazil.png) **Português/Portuguese**](https://github.com/dudestein/react-beautiful-dnd-pt)

## 제작자 (Author) ✍️

Alex Reardon [@alexandereardon](https://twitter.com/alexandereardon)

## 협력자 (Collaborators) 🤝

- Bogdan Chadkin [@IAmTrySound](https://twitter.com/IAmTrySound)
- Luke Batchelor [@alukebatchelor](https://twitter.com/alukebatchelor)
- Jared Crowe [@jaredjcrowe](https://twitter.com/jaredjcrowe)
- 그리고 [@Atlassian](https://twitter.com/Atlassian)들!

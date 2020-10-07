# 설치 방법 (Installation)

[![module formats: umd, cjs, and esm](https://img.shields.io/badge/module%20formats-umd%2c%20cjs%2c%20esm-green.svg?style=flat)](https://unpkg.com/react-beautiful-dnd/dist/)

## 일반 (General)

1. `react-beautiful-dnd` 패키지 더하기

```bash
# yarn
yarn add react-beautiful-dnd

# npm
npm install react-beautiful-dnd --save
```

2. 패키지 사용하기

```js
import { DragDropContext } from 'react-beautiful-dnd';
```

3. 패키지 즐기기 🕺

## `React` 환경 (`React` environment)

`react-beautiful-dnd`를 사용하기 전에 `React` 환경을 셋업(setup)해주세요.

- [웹사이트에 react 더하기](https://reactjs.org/docs/add-react-to-a-website.html) - 공식 `React` 문서
- [`create-react-app`을 사용하여 react 환경 셋업하기](https://egghead.io/lessons/react-set-up-a-react-environment-with-create-react-app) - [무료 시작 과정](https://egghead.io/courses/beautiful-and-accessible-drag-and-drop-with-react-beautiful-dnd)

## 분배 번들 (Distribution bundle)

[Universal Module Definition (UMD)](https://github.com/umdjs/umd) 번들(bundle)은 `npm`의 `/dist` 폴더 안에 게재되어 있습니다. 게재되어있는 파일은 아래와 같습니다:

- `dist/react-beautiful-dnd.js`
- `dist/react-beautiful-dnd.min.js` (축소된 번들)

이 번들은 필요로 하는 외부 `react` 목록을 포함합니다. 이는 번들의 크기를 줄이고 사용자가 `react`를 매번 불러 오지 않도록 하기 위함입니다. 모듈 시스템을 사용하거나 `윈도우`에 `react`를 설치해두면 번들에 `react`를 제공할 수 있습니다.

UMD를 사용하면 `react-beautiful-dnd`를 브라우저에서 직접 사용할 수 있습니다.

```html
<!-- peer dependency -->
<script src="https://unpkg.com/react@16.3.1/umd/react.development.js"></script>
<!-- lib (x.x.x를 사용하는 버전에 맞게 바꿔주세요) -->
<script src="https://unpkg.com/react-beautiful-dnd@x.x.x/dist/react-beautiful-dnd.js"></script>
<!-- react 앱을 마운트(mount) 할 때 필요합니다 -->
<script src="https://unpkg.com/react-dom@16.3.1/umd/react-dom.development.js"></script>

<script>
  const React = window.React;
  const ReactDOM = window.ReactDOM;
  const { DragDropContext, Draggable, Droppable } = window.ReactBeautifulDnd;

  function App() {
    // ...
  }

  // 지원되는 환경에서는 JSX를 사용할 수 있습니다
  ReactDOM.render(React.createElement(App), document.getElementById('app'));
</script>
```

이와 같은 설치 방법으로 [codepen 예시](https://codepen.io/alexreardon/project/editor/ZyNMPo)를 사용해 볼 수 있습니다.

## [`ClojureScript`](https://clojurescript.org/)

[CLJSJS](https://cljsjs.github.io/)을 사용하면 `ClojureScript`에서 `react-beautiful-dnd`를 사용 가능합니다.

[← 이전 화면으로 돌아가기](/README.md#documentation-)

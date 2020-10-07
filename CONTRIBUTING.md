# 협업 (Contributing)

`react-beautiful-dnd`에 협력해주셔서 감사합니다! ❤️

협업에 관한 카테고리 몇 가지를 개별적으로 짚고 넘어가겠습니다.

## 관련 문서 (Documentation)

문서 개선방안이 떠오를 경우 - 풀 리퀘스트(pull request)를 마음껏 보내주세요!

## 버그 (Bug)

버그를 찾으셨다면 이슈(issue) 페이지에 올려주세요. 물론 직접 고치는 것도 환영합니다! 이슈(Issue)를 발행할 때에는 버그에 관한 정보를 자세히 적어주세요.

## 기능 요청 (Feature request)

라이브러리에 추가했으면 하는 기능이 있다면 아래를 읽어주세요:

1.  `README.md`를 읽고 라이브러리의 제작 동기를 생각해주세요. 이 라이브러리는 보편적인 드래그 앤 드롭 라이브러리와는 달리 보통의 라이브러리에서 지원하고자 하는 모든 드래그 앤 드롭을 지원하지 않습니다.
2.  [이슈(issue) (현재 열려있거나 닫혀있는 이슈 포함)](https://github.com/atlassian/react-beautiful-dnd/issues?utf8=%E2%9C%93&q=is%3Aissue)에 이미 요청된 기능인지 확인해주세요.
3.  기능의 의도가 청렴하고 공익을 위한 것인지 생각해주세요.
4.  꼭 [이슈(issue)를 발행하여](https://github.com/atlassian/react-beautiful-dnd/issues/new) 기능을 요청해주세요.

**직접적으로 pull request를 올리면 안 됩니다**. 요청하고자 하는 기능을 추가할 수 없는 이유가 있을 수 있습니다.

## 대규모 협력 (Large contributions)

`react-beautiful-dnd`에 많은 협력을 원하는 개발자들에게 추천하고 싶은 자료들이 있습니다. 이 프로젝트에는 방대한 양의 라이브러리와 기술, 그리고 도구가 사용되므로 관련 자료들을 정리해두었습니다. 모두에게 필요하지는 않겠지만 어디서부터 시작해야 할 지 모르는 사람들에게는 분명 좋은 시작점이 될 것입니다.

아래에 언급되는 자료들은 유료이므로 대체 자료를 찾아보아도 괜찮습니다. 개인적으로는 종합적인 내용을 다루는 `egghead.io`를 추천하고 싶습니다.

### 기본 지식 (General knowledge)

- [You Don't Know JS](https://github.com/getify/You-Dont-Know-JS): JavaScript를 깊이있게 이해하는 데에 도움이 되는 훌륭한 자료입니다.

### 기술

#### `React`

이 프로젝트는 `React` 프로젝트이므로 이에 친숙해지는 건 필수입니다!

- [`react`](https://facebook.github.io/react/)
- [React 시작하기](https://egghead.io/courses/start-using-react-to-build-web-applications)

#### `Redux`

이 프로젝트에서는 상태 관리(state management)를 위해 `redux`를 사용합니다. `redux`를 사용해 본 적이 없다면 미리 알아두면 도움이 될 것입니다.

- [`redux`](http://redux.js.org/docs/introduction/): 라이브러리 안에도 많은 자료가 들어있습니다.
- [Redux 시작하기](https://egghead.io/courses/getting-started-with-redux): 전체 강의를 들어주세요.
- [Idiomatic Redux를 사용하여 React 앱 만들기](https://egghead.io/courses/building-react-applications-with-idiomatic-redux): React router와 data fetching에 대한 강의는 들을 필요 없습니다.
- [`react-redux`](https://github.com/reactjs/react-redux): `redux`를 위한 `react` 바인딩(bindings)
- [`reselect`](https://github.com/reactjs/reselect): 우리는 상태 셀렉터(state selectors)의 빠른 속도를 보장하기 위해 `reselect`를 사용합니다. 이 링크의 메인 페이지, 특히 [sharing Selectors with Props Across Multiple Components](https://github.com/reactjs/reselect#sharing-selectors-with-props-across-multiple-components) 섹션을 읽어주세요.

#### 테스트

우리는 앱을 철저하게 테스트합니다. 테스트 없이는 수정 요청을 수락하지 않습니다.

- [`jest`](https://facebook.github.io/jest/): 이 프로젝트에서는 jest test runner를 사용하므로 친숙해지면 좋습니다.
- [Jest를 이용한 JavaScript 테스팅](https://egghead.io/lessons/javascript-test-javascript-with-jest)
- [React Testing Cookbook](https://egghead.io/courses/react-testing-cookbook)

#### 성능 (Performance)

성능은 이 프로젝트에서 **매우 중요**하므로 React 성능 고려사항(performance considerations)에 익숙해져야 합니다. 코어 성능 특징(core performance characteristics)을 무너뜨리는 수정은 수락하지 않습니다.

- [Performance optimisations for React applications](https://medium.com/@alexandereardon/performance-optimisations-for-react-applications-b453c597b191)
- [Performance optimisations for React applications round 2](https://medium.com/@alexandereardon/performance-optimisations-for-react-applications-round-2-2042e5c9af97)
- [React 성능 도구](https://facebook.github.io/react/docs/perf.html)
- [React 성능 문서](https://facebook.github.io/react/docs/optimizing-performance.html)
- [React는 느리지만, React는 빠르다](https://marmelab.com/blog/2017/02/06/react-is-slow-react-is-fast.html)

#### 플로우 (Flow)

이 프로젝트는 [`flow`](https://flow.org/)에 기반하여 프로그래밍 되었습니다. 유동형(flow typing)이 정확하지 않은 수정은 수락하지 않습니다. 특정 상황(use case)이 불확실할 경우 플로우(flow)로 작동을 중단시킨 뒤에 pull request에서 논의할 수 있습니다.

- [`flow`](https://flow.org/en/docs/getting-started/): `flow` 문서가 훌륭합니다.
- [Up and Running with Facebook Flow for Typed JavaScript](https://egghead.io/lessons/javascript-up-and-running-with-facebook-flow-for-typed-javascript): `flow`에 대한 간단한 입문서입니다.

### 드래그 앤 드롭 문제 공간 (problem space)

#### HTML5 드래그 앤 드롭

이 라이브러리에서 유저가 api를 사용하면 앱에서는 세부 도구(implementation detail)를 이용해 드래깅을 작동합니다. html5 드래그 앤 드롭 api로는 우리가 원하는 강력하고 아름다운 경험을 제공할 수 없으므로 사용되지 않습니다. 이에 대해 보다 자세히 설명할 수 있지만 이 문서에서는 더 깊게 들어가지 않겠습니다.

아래의 html5 드래그 앤 드롭에 대한 자료들을 통해 html5 드래그 앤 드롭의 개념과 api에 친숙해지는 게 좋습니다.

- [HTML5 드래그 앤 드롭 api](https://developer.mozilla.org/en-US/docs/Web/API/HTML_Drag_and_Drop_API)
- [HTML5 Rocks - dnd 기초](https://www.html5rocks.com/en/tutorials/dnd/basics/)
- [The HTML5 드래그 앤 드롭 disaster](https://www.quirksmode.org/blog/archives/2009/09/the_html5_drag.html)
- [HTML5 드래그 앤 드롭 브라우저와 일관성](http://mereskin.github.io/dnd/)

#### 드래그 앤 드롭 라이브러리 (Prior work)

다른 라이브러리의 드래그 앤 드롭을 보며 철학과 api를 참고하는 것도 큰 도움이 됩니다. `react-beautiful-dnd`은 타 드래그 앤 드롭 라이브러리에 비해 독선적이고 추상적입니다. 모든 상황(use case)에 지원해주기보다는 사용자를 위한 아름다운 경험과 원활한 사용과 깔끔하고 강력한 api를 유지할 수 있을 정도의 통제만을 제공하고자 합니다.

- [`react-dnd`](https://react-dnd.github.io/react-dnd/) - `react-beautiful-dnd`는 `react-dnd`에서 영감을 받은 프로젝트이지만 `react-dnd`는 드래그 앤 드롭 기초요소를 제공하는 데 중점을 둔 라이브러리로, 이 프로젝트와는 목표가 다릅니다.
- [`react-sortable-hoc`](https://github.com/clauderic/react-sortable-hoc/) - 겉으로는 `react-beautiful-dnd`와 비슷해보일 수 있습니다. 두 라이브러리를 비교해놓은 [블로그 포스트](https://medium.com/@alexandereardon/thanks-for-reaching-out-dimitar-nestorov-8c0bf9abe19)로 차이점을 알아보세요.
- [`jQuery sortable`](http://jqueryui.com/sortable/) - 꽤 오랜 기간동안 드래그 앤 드롭의 왕좌를 지켜온 라이브러리입니다.

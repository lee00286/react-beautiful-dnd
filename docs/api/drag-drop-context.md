# `<DragDropContext />`

드래그 앤 드롭을 사용하려면 `React` tree의 일부를 가지고 있어야 합니다. 우리는 사용자의 전체 어플리케이션(application)을 `<DragDropContext />`로 감쌀 것을 권고합니다. `<DragDropContext />`를 다른 코드로 감싸는 건 지원되지 _않습니다_. 권고사항을 따른다면 `<Droppable />`과 `<Draggable />`을 이용한 조건부의 드래깅(dragging)과 드로핑(dropping)을 사용할 수 있습니다. `<DragDropContext />`와 [react-redux 제공자 컴포넌트(provider component)](https://react-redux.js.org/api/provider)가 비슷한 목적을 갖고 있다고 생각해도 무방합니다. 내용물-안전-보호 속성 nonce가 제공될 경우에는 인젝티드 스타일 태그(injected style tags)에 추가됩니다.

## 내용물 (Props)

```js
type Responders = {|
  // 선택
  onBeforeCapture?: OnBeforeCaptureResponder
  onBeforeDragStart?: OnBeforeDragStartResponder,
  onDragStart?: OnDragStartResponder,
  onDragUpdate?: OnDragUpdateResponder,
  // 필수
  onDragEnd: OnDragEndResponder,
|};

import type { Node } from 'react';

type Props = {|
  ...Responders,
  // 기술적으로는 이 컴포넌트의 children이 필요하지 않음
  children: Node | null,
  // 드래그 조정(drag handle)에 집중할 경우, 스크린 리더(screen readers)가 읽음
  dragHandleUsageInstructions?: string,
  // 엄격한 내용물 안전 방침에 사용됨
  nonce?: string,
  // 센서(sensors)를 원하는 대로 수정할 때 사용
  sensors?: Sensor[],
  enableDefaultSensors?: ?boolean,
|};
```

- `dragHandleUsageInstructions`: 브라우저 포커스(browser focus)가 _드래그 조정(drag handle)_에 맞춰져있을 때 스크린 리더가 읽는 부분입니다. [스크린 리더 문서](/docs/guides/screen-reader.md)를 참고해주세요.
- `nonce`: 엄격한 내용물 안전 방침 셋업(setups)에 사용됩니다. [내용물 안전 방침 가이드](/docs/guides/content-security-policy.md)를 참고해주세요.
- `sensors`: `<DragDropContext />`를 위한 `센서`를 보낼 때 사용됩니다. [센서 api 문서](/docs/sensors/sensor-api.md)를 참고해주세요.
- `enableDefaultSensors`: 기본 센서([마우스](/docs/sensors/mouse.md), [키보드](/docs/sensors/keyboard.md), [터치](/docs/sensors/touch.md))의 활성화 여부를 알려줍니다. [센서 api 문서](/docs/sensors/sensor-api.md)를 참고해주세요.

> 자세한 정보는 [타입(types) 가이드](/docs/guides/types.md)를 읽어주세요

## 기본적인 사용법 (Basic usage)

### `class` 컴포넌트 사용하기 (Using a `class` component)

```js
import React from 'react';
import { DragDropContext } from 'react-beautiful-dnd';

class App extends React.Component {
  onBeforeCapture = () => {
    /*...*/
  };

  onBeforeDragStart = () => {
    /*...*/
  };

  onDragStart = () => {
    /*...*/
  };
  onDragUpdate = () => {
    /*...*/
  };
  onDragEnd = () => {
    // 유일하게 필수인 부분
  };

  render() {
    return (
      <DragDropContext
        onBeforeCapture={this.onBeforeCapture}
        onBeforeDragStart={this.onBeforeDragStart}
        onDragStart={this.onDragStart}
        onDragUpdate={this.onDragUpdate}
        onDragEnd={this.onDragEnd}
      >
        <div>Hello world</div>
      </DragDropContext>
    );
  }
}
```

### `function` 컴포넌트 사용하기 (Using a `function` component)

```js
import React from 'react';
import { DragDropContext } from 'react-beautiful-dnd';

function App() {
  // useCallback 사용은 선택
  const onBeforeCapture = useCallback(() => {
    /*...*/
  }, []);
  const onBeforeDragStart = useCallback(() => {
    /*...*/
  }, []);
  const onDragStart = useCallback(() => {
    /*...*/
  }, []);
  const onDragUpdate = useCallback(() => {
    /*...*/
  }, []);
  const onDragEnd = useCallback(() => {
    // 유일하게 필수인 부분
  }, []);

  return (
    <DragDropContext
      onBeforeCapture={onBeforeCapture}
      onBeforeDragStart={onBeforeDragStart}
      onDragStart={onDragStart}
      onDragUpdate={onDragUpdate}
      onDragEnd={onDragEnd}
    >
      <div>Hello world</div>
    </DragDropContext>
  );
}
```

## `Responders`

> `Responders`는 `Hooks`로도 알려져있습니다.

Responders는 상태와 스타일 업데이트, 그리고 스크린 리더 공지를 띄울 때 사용되는 최고 수준의 어플리케이션 이벤트(top level application events)입니다.

Responders에 대한 자세한 정보는 [responders 설명서](/docs/guides/responders.md)를 참고해주세요 ❤️

[← 이전 화면으로 돌아가기](/README.md#documentation-)

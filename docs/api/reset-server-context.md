# `resetServerContext`

`resetServerContext` 함수는 서버 사이드 렌더링(SSR)을 할 때 사용됩니다. 이는 컨텍스트의 상태(context state)가 수차례의 렌더링 동안 지속되어 클라이언트/서버 마크업(markup)의 부조화를 초래하지 않도록 합니다.

아래의 코드를 서버 사이드 렌더링 메소드(method)를 호출하기 전에 사용하세요:

```js
import { resetServerContext } from 'react-beautiful-dnd';
import { renderToString } from 'react-dom/server';

// ...

resetServerContext();
renderToString(...);
```

[← 이전 화면으로 돌아가기](/README.md#documentation-)

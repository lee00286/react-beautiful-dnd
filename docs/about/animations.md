# 세심한 애니메이션 (Carefully designed animations)

화면에서 여러가지가 움직이면 산만해지기 쉽상입니다. 따라서 우리는 유도와 작동성, 그리고 상호성의 균형을 맞출 수 있도록 애니메이션을 수정했습니다.

## 드로핑 (Dropping)

드롭(drop) 애니메이션은 역동성과 무게감을 느낄 수 있게끔 설계되었습니다. 이는 [`spring`](https://developer.android.com/guide/topics/graphics/spring-animation)을 기반으로 하며, CSS 애니메이션의 유연한 지속시간을 통해 효과를 구현했습니다.

![결과 커브(result-curve)](https://user-images.githubusercontent.com/2182637/48235467-1ce34200-e412-11e8-8c69-2060a0c2f61a.png)

> 애니메이션 커브(animation curve)는 드로핑(dropping) 할 때 사용합니다. 지속시간은 이동 거리에 따라 달라집니다.

원할 경우 드롭(drop) 애니메이션을 수정할 수 있습니다. 안내 문서를 확인해주세요: [드롭(drop) 애니메이션](/docs/guides/drop-animation.md)

## 범위를 벗어난 아이템 (Moving out of the way)

드래깅(dragging) 아이템의 범위를 벗어난 아이템은 물리 대신 CSS 트랜지션(transition)으로 구현하였습니다. 이는 GPU로 움직임을 제어하여 작동성을 극대화시키기 위함입니다. CSS 애니메이션 커브(animation curve)는 범위를 벗어난 것을 알리는 용도로 사용되었습니다.

구성 방법:

1.  자연 반응 시간을 따라하기 위한 준비(warm up) 시간
2.  범위를 빠르게 벗어나도록 하기 위한 단계
3.  글씨가 움직이고 있는 동안에도 글씨를 읽을 수 있도록 하기 위한 긴 꼬리

![애니메이션 커브(animation curve)](https://raw.githubusercontent.com/alexreardon/files/master/resources/dnd-ease-in-out-small.png?raw=true)

> 애니메이션 커브(animation curve)는 범위를 벗어날 때 사용합니다.

[← 이전 화면으로 돌아가기](/README.md#documentation-)

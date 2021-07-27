# CSS

## inline 과 inline-block 의 차이점은 무엇인가요?

inline과 inline-block은 기본적으로 엘리먼트를 전후 줄바꿈 없이 한 줄에 나란히 배치된다.

inline은 해당 태그가 가지고 있는 컨텐트의 크기만큼만 공간을 차지해서 width와 height 속성을 지정해도 무시된다.

margin과 padding 속성의 경우 좌우 간격만 반영되고, 상하간격을 반영되지 않는다.

inline-block의 경우 width, height, margin, padding 속성의 상하간격까지 모두 지정이 가능하다.

inline-block은 여러 개의 엘리먼트를 줄바꿈 없이 원하는 크기만큼 배치할 수 있기 때문에 레이아웃에 활용할 수 있다.

button과 select 태그는 inline-block이 기본 display 설정값이다.

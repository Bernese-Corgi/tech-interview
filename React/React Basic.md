# React Basic

- [React Basic](#react-basic)
  - [state와 props의 차이는 무엇인가요?](#state와-props의-차이는-무엇인가요)

## state와 props의 차이는 무엇인가요?

props는 상위 컴포넌트로부터 전달받는 속성으로, 읽기전용 값이므로 업데이트가 불가하다. 반면 state는 컴포넌트 자신이 가지는 상태로, 업데이트가 가능한 값이다.

state가 업데이트되면 리액트는 ui를 다시 렌더링한다.

state와 props는 연관되는 개념이다. 상위 요소의 state를 하위요소가 props로 전달받는것이다.

하위 요소가 전달받은 props는 클래스의 setState()를 사용해 state를 변경할 수 있다. 이 때 state의 변경은 상위 요소에게는 적용되지 않고, 상태를 변경한 해당 요소와 그 하위 요소들에게만 변경사항이 적용된다.

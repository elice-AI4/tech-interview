파일명은 `이름.md`로 해주세요. ex. `chaejung.md`

예시 형식

## 1. MVC pattern을 간략하게 설명하고, 발생할 수 있는 문제점에 대해 이야기해보세요.

### 답변

> MVC는 Model, View, Controller를 구성요소로 가집니다.<br>
> Model은 데이터의 형태를 정의하고 수정하는 역할을,<br>
> View는 모델을 UI로 표현하고 사용자의 입력을 받아 Controller에 전달하며,<br>
> Controller는 입력받은 이벤트를 애플리케이션 내에 어떻게 처리할지 판단하고 가공하여 Model 또는 View를 조작하는 역할을 합니다.<br>
> MVC 패턴은 각 구성요소들끼리 양방향으로 통신하게 되므로 연쇄적인 변화가 발생하여 결국 애플리케이션의 동작 흐름을 분석하거나 예측할 수 없는 문제가 발생할 수 있습니다.

- 출처: 원티드 프리온보딩 프론트엔드 6차 황연욱 멘토님

## 2. React의 Virtual DOM은 무엇인가요?

### 답변

> 실제 DOM은 요소가 바뀔 때마다 새로운 render tree를 생성하여 렌더링 효율이 떨어집니다.
> Virtual DOM은 가상으로 UI를 메모리에 저장했다가, 실제 DOM과 동기화하는 프로그래밍 개념 또는 UI 객체를 말합니다.
> React에서는 ReactDOM과 같은 라이브러리에 의해 실제 DOM과 동기화되는데,
> 이런 과정을 재조정(reconciliation)이라 하고, 변화가 일어난 부분만 다시 렌더링하도록 합니다.
> Reconciliation은 React에게 원하는 UI 상태를 알려주고 DOM이 해당 상태와 일치하도록 합니다.
> 이 과정에서 이벤트 처리, 수동 DOM 업데이트를 추상화합니다.

- [출처: React 공식 문서](https://ko.reactjs.org/docs/faq-internals.html#gatsby-focus-wrapper)

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

> 실제 DOM은 요소가 바뀔 때마다 새로운 render tree를 생성하여 렌더링 효율이 떨어집니다.<br>
> Virtual DOM은 가상으로 UI를 메모리에 저장했다가, 실제 DOM과 동기화하는 프로그래밍 개념 또는 UI 객체를 말합니다.<br>

> React에서는 ReactDOM과 같은 라이브러리에 의해 실제 DOM과 동기화되는데,<br>
> 이런 과정을 재조정(reconciliation)이라 하고, 변화가 일어난 부분만 다시 렌더링하도록 합니다.<br>
> Reconciliation은 React에게 원하는 UI 상태를 알려주고 DOM이 해당 상태와 일치하도록 합니다.<br>
> 이 과정에서 이벤트 처리, 수동 DOM 업데이트를 추상화합니다.

- [출처: React 공식 문서](https://ko.reactjs.org/docs/faq-internals.html#gatsby-focus-wrapper)

## 3. CORS는 무엇이고, CORS 에러를 방지하려면 어떻게 해야하나요?

### 답변

> Cross Origin Resource Sharing의 줄임말로, 교차 출처 리소스 공유이며,<br>
> 브라우저는 동일 출처 정책에 의해 출처가 다른 리소스 요청을 방지하는 HTTP 헤더 기반 메커니즘입니다.<br>
> 출처가 다르다는 것은 도메인, 하위도메인, 포트, 프로토콜이 다르다는 것을 의미하는데,<br>
> CORS에 의해 요청이 차단되지 않으려면 이 네 가지가 모두 동일해야합니다.<br>

> 또는 프론트엔드에서는 프록시 서버를 만들어 동일한 출처로 만드는 방법도 있습니다.<br>
> 백엔드에는 express의 cors 미들웨어 라이브러리를 사용하거나,<br>
> 응답 헤더에 Access-Control-Allow-Origin에 허용하고자 하는 도메인을 세팅하는 방법이 있습니다.

- [출처: fetch-crossorigin](https://ko.javascript.info/fetch-crossorigin)

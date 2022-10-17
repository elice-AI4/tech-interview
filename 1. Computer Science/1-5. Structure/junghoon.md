## 1. 디자인 패턴은 무엇인가요?

### 답변

> 1. 과거 소프트워에 개발 과정에서 발견한 설계 노하우를 패턴으로 정리한 것이다.
> 2. 프로그램을 설계할 때 발생했던 문제점들을 객체 간의 상호 관계 등을 이용하여 해결할 수 있도록 하나의 규약 형태로 만들어 놓은 것이다.
> 3. 소프트웨어를 개발하는 과정의 반복되는 일반적인 문제들에 대해 기준이 되는 해결책을 제공하는 중요한 개념이다.

- 출처
  - https://patterns-dev-kr.github.io/design-patterns/introduction/
  - 면접을 위한 CS 전공 지식 노트

## 2. passport에 대해서 설명해 주시고, passport의 디자인 패턴에 대해서 설명 해 주실수 있나요

### 답변

#### passport

> Express.js 어플리케이션에 간단하게 사용자 인증 기능을 구현하게 도와주는 패키지다.  
> 유저 세션을 관리하고, 다양한 로그인 방식(구글, 카카오 등)을 추가할 수 있다.  
> 그러니까... 쿠키와 세션을 주고받는 과정을 직접 다 구현하지 않고, passport를 통해 쉽게 사용자 인증을 할 수 있다.

#### passport의 디자이너 패턴

> passport는 여러 가지 '전략'을 기반으로 인증할 수 있게 한다.  
> 서비스 내의 회원가입된 아이디와 비밀번호 기반으로 인증하는 LocalStrategy 전략과, 페이스북, 네이버 등 다른 서비스를 기반으로 인증하는 OAuth 전략 등을 지원한다.  
> 즉 지원만 바꿔서 인증을 할 수 있고, 이는 전략 패턴을 활용한 것이다.

- 출처: 면접을 위한 CS 전공 지식 노트

## 3. 객체가 무엇인가요?

### 답변

> 어떠한 문제를 해결하기 위해 추상화를 거쳐 집단에 속하는 속성과 행위를 변수와 메서드의 묶어 정의 한 것

## 4. 오버로딩 및 오버라이딩에 대해서 설명하고, JS에서 오버로딩을 구현하는 방법을 설명 해 보세요.

### 답변

#### 오버로딩

> 같은 이름의 함수를 매개변수의 타입과 개수를 다르게 해서 여러개 정의하여 사용하는 것이다.

#### 오버라이딩

> 부모 클래스의 메서드를 자식 클래스에서 재정의하여 사용하는 것이다.

#### JS에서 오버로딩을 구현하는 방법

> JS에서는 제일 나중에 선언한 함수가 같은 이름의 함수를 덮어씌워버린다.

```js
function a() {
  console.log("a");
}

function a() {
  console.log("b");
}

function a() {
  console.log("c");
}

a(); // c
```

```js
function func(a, b, c) {
  if (typeof c === "function") {
    c(a, b);
  } else if (typeof b === "function") {
    b(a);
  } else {
    a();
  }
}

function callback(a, b) {
  if (b) {
    console.log("a, b 둘 넘어옴", a, b);
  } else if (a) {
    console.log("a만 받아옴", a);
  } else {
    console.log("매개변수 없음");
  }
}
func("malza", "pokemon", callback); // a, b 둘 넘어옴 malza pokemon
func({ name: "malza", value: "front-end" }, callback); // a만 받아옴 {name: 'malza', value: 'front-end'}
func(callback); // 매개변수 없음
```

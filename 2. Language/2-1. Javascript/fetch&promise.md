# fetch

## 쓰는 이유

기존 XMLHTTPRequest를 대체하는 HTTP 요청 API

원격 API를 간편하게 호출할 수 있도록 브라우저에서 제공

> fetch가 비동기를 사용하는 이유: 데이터를 가져오는 동안 언제 응답이 올지 모르면 프로그램이 멈출 수 있기 때문

## 특징

ES6에 추가된 Promise를 리턴하도록 정의된다.

    네트워크 요청 성공 시, Promise는 Response 객체를 resolve한다
    네트워크 요청 실패 시, Promise는 에러를 reject한다.

//promise: `const fetchResponsePromise = fetch(url)`

<기본 구성>

```js
fetch("https://example.com")
  //json 데이터 타입을 자바스크립트에 바로 쓸 수 없기 때문에 converting
  .then((response) => response.json())
  .then((data) => console.log("Success:", data))
  .catch((err) => console.error("Error:", err));
```

```bash
Response { status: 200, ok: true, redirected: false, type: "cors", url:'https://example.com', ...}
```

<JSON 데이터 업로드>

```js
const data = { username: "John Doe" };

fetch("https://example.com", {
  method: "POST",
  headers: {
    "Content-Type": "application//json",
  },
  body: JSON.stringify(data),
})
  .then((res) => res.json())
  .then((data) => console.log("Success:", data))
  .catch((err) => console.log("Error:", err));
```

```bash
# Response { status: 201, ok: true, redirected: false, type: "cors", url: "https:/example.com", ...}

{ username: 'John Doe' }
```

## fetch vs axios

| fetch                                              | axios                                         |
| -------------------------------------------------- | --------------------------------------------- |
| 자바스크립트 내장<br>별도의 import나 설치 불필요   | 설치 필요                                     |
| 인터넷 익스플로어 버전에서 지원하지 않는 경우 존재 | 브라우저 호환성이 fetch보다 뛰어남            |
| 지원하지 않는 기능 존재                            | JSON 자동 변환, 응답 시간 초과 설정 기능 지원 |

# Promise

## promise의 특징

비동기를 위한 처리 방식
fetch는 왜 비동기를 사용할까
데이터를 가져오는 동안 언제 응답이 올지 모르면 멈출 수 있다, 그래서 비동기를 사용
promise를 쓰는 이유는 비동기가 끝나고 실행됐으면 하는 함수를 쓰기 위함.

## promise 만드는 방법

1. promise를 반환하는 함수면 `func().then(callback)` 형태를 가진다.

2. Promise 생성자, promise 함수는 콜백함수를 입력받는다

```js
let promise = new Promise((resolve, reject) => {...} )
```

<Promise 메서드 체인>

```js
promise
  .then((data) => {
    return fetchUser(data);
  })
  .then((user) => {
    console.log("User: ", user);
  })
  .catch((err) => {
    console.log("Fail: ", err);
  });
```

<Promise.resolve, Promise.reject>

네트워크 요청 성공 시, response 객체를 resolve, 실패 시 에러를 reject

```js
promise.resolve(10).then(console.log);
promise.reject("Error").then(console.log);
```

<Promise.all>

promise의 배열을 받아 모두 성공 시 각 promise의 resolved 값을 배열로 반환

하나의 promise라도 실패 시, 가장 먼저 실패한 promise의 실패 이유를 반환

```js
Promise.all([promise1, promise2, promise3]);
```

<기본 예제>

```js
function promiseTest(num) {
  return new Promise((resolve, reject) => {
    if (num == 5) resolve("Success");
    else reject("Fail");
  });
}

promiseTest(10).then((data) => console.log(data));
// Promise {<rejected>: 'Fail'}
promiseTest(5).catch((data) => console.log(data));
// Promise {<fulfilled>: 'Success'}
```

> promise를 직접 만들기보다는 fetch를 쓰는 일이 더 많을 것

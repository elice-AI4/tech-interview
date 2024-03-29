# Node.js

V8엔진을 이용해 JavaScript를 웹 브라우저 뿐만 아니라 어느 환경에서나 실행할 수 있게 하는 실행기

## Browser & Node.js 
|Browser|Node.js|
|--|--|
|브라우저에서 실행|크로스 플랫폼에서 실행|
|웹 내부 제한된 동작|제한 없는 동작|
|웹 프론트 개발자의 언어|다양한 어플리케이션 개발|

## 활용
- FE: React.js
- BE: Express.js
- Mobile-App: React-Native
- Desktop: Electron
- Machine-Learning: Brain.js

## 특징
1. 싱글 스레드
    스레드: 명령을 실행하는 단위, 한 개의 스레드는 한 가지 동작만 가능

    장점: 스레드가 늘어나지 않아 리소스 관리에 효율적

    단점: 스레드 기반의 작업들의 효율이 떨어짐 ex. CPU 연산 작업

    > 그래서 Node.js는 비동기 동작으로 스레드 기반의 작업을 최소화

2. 이벤트 기반
    비동기 동작의 완료를 처리하는 방법

    비동기 방식은 특정 동작을 실행한 후, 해당 동작을 전혀 신경 쓰지 않는다.

    대신 해당 동작이 완료될 경우 실행할 함수를 미리 등록

    비동기 동작이 완료가 되면 미리 등록된 함수를 실행
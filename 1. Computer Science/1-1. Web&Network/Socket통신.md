## Socket 통신

### 1. Socket이란?

- socket이란 컴퓨터 네트워크를 경유하는 프로세스 간 통신의 종착점(endpoint)으로 다양한 수단을 이용하여 데이터를 주고 받는 통신 방식을 의미한다.

- 소켓 구현은 TCP / UDP 방식으로 나누어진다.

- TCP vs UDP

> ⭐ TCP 소켓과 웹소켓은 다른 개념([참고](https://medium.com/@hyun.sang/network-%EC%86%8C%EC%BC%93%EA%B3%BC-%EC%9B%B9%EC%86%8C%EC%BC%93%EC%9D%98-%EC%B0%A8%EC%9D%B4%EC%A0%90-b1b745fcdcc2))이고 아래에 기술할 내용들은 모두 웹소켓에 관련된 내용이다.

### 2. Socket 통신 vs. HTTP 통신

- 가장 큰 차이점 => **방향성**
- **HTTP 통신**은 클라이언트에서 서버로 요청을 보내고 서버에서 클라이언트로 응답하면 연결이 끊기는 단방향 통신 <br>=> 지속적으로 요청해야하는 경우(실시간 통신) 계속해서 요청을 보내기 때문에 부하가 큼
- **Socket 통신**은 서버와 클라이언트 간 양방향 통신이 가능하고 연결을 끊지 않으면 지속적으로 통신이 가능하기 때문에 실시간 통신에 적합
<br>=> 지속적인 요청이 필요 없는 상황에서 socket 통신을 이용하는 경우에 불필요한 자원 낭비가 생길 수 있음

<br>

| 기준 | Socket 통신 | HTTP 통신 |
| --- | --- | --- |
| 방향성 | 양방향 <br> (서버 <-> 클라이언트) | 단방향 <br>  요청: 클라이언트 -> 서버 <br> 응답: 서버 -> 클라이언트 |
| 활용 | 실시간 통신 (실시간 채팅, 스트리밍 등) 서비스 | 지속적인 연결을 필요로 하지 않는 모든 서비스 |

### 3. Socket 구현 방법 (추가 예정)
#### 3-1. WebSocket 과 Socket.io
- Websocket은 socket을 이용한 양방향 통신 프로토콜을 의미합니다.
- Socket.io는 웹소켓 기술을 활용하는 라이브러리입니다.

- WebSocket
    - HTML5 웹 표준 기술
    - 매우 빠르게 작동하며 통신할 때 아주 적은 데이터를 이용함
    - 이벤트를 단순히 듣고, 보내는 것만 가능함
- Socket.io
    - 표준 기술이 아니며, 라이브러리임
    - 소켓 연결 실패 시 fallback을 통해 다른 방식으로 알아서 해당 클라이언트와 연결을 시도함
    - 방(room) 개념을 이용해 일부 클라이언트에게만 데이터를 전송하는 브로드캐스팅이 가능함

    - socket.io를 사용할 경우 클라이언트와 서버 모두 socket.io 라이브러리를 사용해야함

<br>

#### 3-2. ws 구현 방법

#### 3-3. socket.io 구현 방법


## 출처
### [1]: [socket 정의1-네이버지식백과](https://terms.naver.com/entry.naver?docId=837501&cid=42344&categoryId=42344)
### [2]: [socket 정의2-위키백과](https://ko.wikipedia.org/wiki/%EB%84%A4%ED%8A%B8%EC%9B%8C%ED%81%AC_%EC%86%8C%EC%BC%93)
### [3]: [TCP/UDP 방식 차이](https://badayak.com/entry/tcpip%EC%99%80-udpip-%ED%86%B5%EC%8B%A0-%EC%B0%A8%EC%9D%B4%EC%A0%90)
### [4]: [Http 프로그래밍과 Socket 프로그래밍 차이](https://mangkyu.tistory.com/48)
### [5]: [웹소켓 vs socket.io](https://www.peterkimzz.com/websocket-vs-socket-io/)
### [6]: [WebSocket과 Socket.io](https://d2.naver.com/helloworld/1336)
### [7]: [웹소켓-위키피디아](https://en.wikipedia.org/wiki/WebSocket)
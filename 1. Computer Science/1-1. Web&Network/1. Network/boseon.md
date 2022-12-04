1. HTTP 1.1 HTTP 2.0 차이
   HTTP 1.1의 단점이 무엇인가?
   요청과 응답이 순차적으로 이루어지기 때문에 여러개의 요청 응답이 이루어질때 앞의 응답 속도가 느려지면 나머지의 응답 시간도 길어진다.
   무거운 헤더 구조, 헤더에 쿠키 등 많은 메타 데이터가 들어있기 때문에 무겁다

2. keep-alive가 뭔지 아시나요?
   persistent connection, 연결의 지속 시간을 설정해 매번 요청/응답시 TCP 연결을 하지않고 설정한 시간동안 연결을 유지

3. pipelining
   클라이언트에서 요청을 응답에 상관없이 보내고 Server에서는 요청 순서대로 응답을 보낸다. 결국 HOL Blocking 발생한다.

4. HTTP 2.0
   HTTP 2.0은 HTTPS 위에서 동작합니다.
   HTTP 1.1은 요청 응답 메시지를 text 형식으로 전달됬지만, 2.0은 프레임 단위로 나누고, 바이너리 형식으로 인코딩해서 전달한다. \* 바이너리는 컴퓨터가 이해하기 더 쉽다.

**HTTP 2.0 특징**

멀티플렉싱을 통해 하나의 연결 내 병렬적인 스트림들을 통해 데이터를 통신한다.
스트림의 패킷이 손실되어도 나머지 스트림에 영향을 주지 않는다.
응답은 요청 순서에 상관없이 스트림으로 주고 받는다.
각 스트림에는 고유 넘버가 있기 때문에 수신쪽에서 섞여서 전달되어도 고유넘버로 재조합 가능

헤더 데이터를 압축해서 보낸다.

스트림 우선순위 지정을 통해 서버가 높은 우선 순위 스트림을 우선적으로 응답할 수 있도록 한다.

서버 푸시
1.1에서는 클라이언트가 서버에 요청을 해야 파일을 다운받을 수 있었지만, 2.0에서는 클라이언트 요청 없이 서버가 바로 리소스를 푸시할 수 있다.
서버에서 HTML에 포함된 리소스를 요청하지 않아도 전달해주는 방법이다.

---

5. 쿠키와 세션의 설명
   클라이언트에 저장되는 작은 기록 정보 파일
   쿠키는 오랜 시간동안 유지가 가능
   자바스크립트를 이용해 쿠키에 접근할 수 있기 때문에 쿠키에 민감한 정보를 담는 것은 위험, 주로 노출되어도 상관없는 정보들을 저장하는데 이용

6. 쿠키 통신 방법

   1. 최초 통신에서는 쿠키값이 없고, 클라이언트는 서버에 페이지 요청
   2. 서버에서 클라이언트가 보낸 요청 헤더에 쿠키가 없음을 확인하고, 통신 상태를 저장한 쿠키를 HTTP 헤더에 저장해 응답으로 보냄
   3. 클라이언트의 브라우저가 받은 쿠키를 생성/보존
   4. 두 번째 연결부터 같은 요청시 HTTP 헤더에 쿠키를 담아 서버에 요청

7. 세션
   서버에 관리하며, 유출 되서는 안되는 중요한 데이터 저장하며, 브라우저를 종료할 때까지 유지된다.
   각 클라이언트 고유 세션 ID를 부여
   사용자가 많아질수록 서버 메모리를 많이 차지함

8. 세션 통신 방법
   1. 클라이언트가 웹 사이트 접근
   2. 서버는 접근한 클라이언트의 요청 헤더에 쿠키를 확인해 세션 ID를 보냈는지 확인
   3. 세션 ID가 존재하지 않으면, 서버는 세션 ID를 생성해 클라이언트에게 전송
   4. 서버에서는 클라이언트로 전송한 세션 ID를 서버에 저장
   5. 클라인트가 재접속 시 클라이언트 세션 ID가 저장된 쿠키를 이용해 세션 ID를 서버에 전달

---

HTTP 1.1의 단점이 무엇인가요
요청과 응답이 순차적으로 이루어지기 때문에 여러개의 요청 응답이 이루어질때 앞의 응답 속도가 느려지면 나머지의 응답 시간도 길어진다.
무거운 헤더 구조, 헤더에 쿠키 등 많은 메타 데이터가 들어있기 때문에 무겁다

HTTP 2.0
HTTP 2.0은 HTTPS 위에서 동작합니다.
HTTP 1.1은 요청 응답 메시지를 text 형식으로 전달됬지만, 2.0은 프레임 단위로 나누고, 바이너리 형식으로 인코딩해서 전달한다.

멀티플렉싱을 통해 하나의 연결 내 병렬적인 스트림들을 통해 데이터를 통신한다.
스트림의 패킷이 손실되어도 나머지 스트림에 영향을 주지 않는다.
응답은 요청 순서에 상관없이 스트림으로 주고 받는다.
각 스트림에는 고유 넘버가 있기 때문에 수신쪽에서 섞여서 전달되어도 고유넘버로 재조합 가능
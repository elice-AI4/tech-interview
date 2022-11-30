
## 1. TCP와 UDP의 차이점에 대해 설명해주세요.
    
### 답변

| TCP | VS | UDP |
| --- | --- | --- |
| 연결 지향형 | 연결? | 비연결 지향형 |
| 가상회선 패킷 교환 방식 | 교환 방식 | 데이터그램 패킷 교환 방식 |
| 보장 | 패킷 순서 | 보장 X |
| 신뢰성 보장
(연결시 3-way Handshake
연결 해제시 4-way Handshake) | 신뢰성 | 신뢰성 보장 X |
| 파일 전송 | 사용처 | 스트리밍 서비스 |
| 느림 | 속도 | 빠름 |
| ex> HTTP/1 ~ 2 | HTTP? | ex> HTTP/3 (QUIC) |

- TCP는 무엇을 통해 신뢰성을 보장하나요?
    
    3-way Handshake
        
- UDP는 항상 신뢰성을 보장하지 않나요?
    
    프로토콜 자체는 신뢰성을 보장하지 않으나 신뢰성을 보장할 수 있도록 로직을 추가할 수 있습니다.
        
- 각 프로토콜의 사용처를 하나씩 설명해주세요!
    
    파일전송 서비스(TCP), 스트리밍 서비스(UDP)
        
## 2. RESTful-API 가 무엇인가요?

### 답변

- Representational State Transfer(REST)는 효율적인 API 구현을 위한 소프트웨어 아키텍처이며 <br>
이 방식을 준수하는 애플리케이션 프로그래밍 인터페이스(API)를 RESTful API라고 합니다.

- REST 아키텍처의 6가지 제약 조건
    - 단일 인터페이스
    - 무상태성
    - 캐싱 가능
    - 자체 표현 구조
    - Client -Server 구조
    - 계층형 구조

<br>

- RESTful API를 작성하기 위해서 기본적으로 **URI가 자원을 명시해야 하며, 자원에 대한 행위는
http method를 통해 구분**합니다. (C: POST, R: GET, U: PUT/PATCH, D: DELETE)

<br>

- 각 method를 설명해주세요.
    
    
    | Method | Description | HasBody? | Attribution |
    | --- | --- | --- | --- |
    | GET | 서버에서 해당 자원을 조회(요청)한다. | No | Safe, Idempotent, Cacheable |
    | POST | 서버가 처리해야 할 데이터를 전송(제출)한다. | Yes | Cacheable(rarely) |
    | PUT | 서버에 요청 메시지의 본문을 (해당 자원에) 저장한다. | Yes | Idempotent |
    | DELETE | 서버에서 해당 자원을 제거한다. | No | Idempotent |
    | PATCH | 서버에서 해당 자원의 일부분을 수정한다. | Yes |  |
    | OPTIONS | 서버가 어떤 메서드를 수행할 수 있는지 확인한다. | No | Safe, Idempotent |
    | HEAD | 서버에서 해당 자원에 대한 헤더만 가져온다. (응답 본문 X) | No | Safe, Idempotent, Cacheable |
    | TRACE | 요청 메시지가 프락시를 거쳐 서버에 도달하는 과정을 추적한다. (loop-back test) | No | Safe, Idempotent |
    | CONNECT | 목적 리소스로 식별되는 서버로의 터널을 맺습니다. (요청 리소스에 대한 양방향 연결을 시작) | No |  |

<br>

> 출처: <br>
[1] https://kyun2da.dev/CS/http-%EB%A9%94%EC%86%8C%EB%93%9C%EC%99%80-%EC%83%81%ED%83%9C%EC%BD%94%EB%93%9C/ <br>
[2] https://developer.mozilla.org/ko/docs/Web/HTTP/Methods <br>
[3] 주홍철, 『면접을 위한 cs 전공 지식 노트』(길벗, 2022) p80 - 87. <br>
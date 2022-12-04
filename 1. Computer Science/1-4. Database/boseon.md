관계형 DB 비관계형 DB 차이

관계형 DB

- 트랜잭션(전부 아니면 무): 전체 트랜잭션이 하나의 단위로 기록. 실패 시 전체 롤백

- 정규화: DB설계 시 중복을 최소화해서 구조화하는 프로세스

장점

- 데이터의 성능이 일반적으로 좋아 정렬, 탐색, 분류가 빠름

- 신뢰성이 높아 데이터의 무결성을 보장

- 정규화에 따른 갱신 비용을 최소화

단점

- 기존에 작성된 스키마를 수정하기 어려움

- 데이터베이스의 부하를 분석하기 어려움

- 빅데이터를 처리하는데 매우 비효율적임.

비관계형 DB

- 거대한 Map으로서 key-value 형식을 지원함.

- 관계형 db와 달리 PK,FK JOIN등 관계를 정의하지 않음.

- 스키마에 대한 정의가 없다.

장점

- 대용량 데이터 처리를 하는데 효율적임.

- 읽기 작업보다 쓰기 작업이 더 빠르고 관계형 데이터베이스에 비해 쓰기와 읽기 성능이 빠름.

- 데이터 모델링이 유연함.

- 뛰어난 확장성으로 검색에 유리함.

- 최적화된 키 값 저장 기법을 사용하여 응답속도나 처리효율 등에서 성능이 뛰어남.

- 복잡한 데이터 구조를 표현할 수 있음.

단점

- 쿼리 처리시 데이터를 파싱 후 연산을 해야해서 큰 크기의 document를 다룰 때는 성능이 저하됨.

---

객체지향 프로그래밍 특징
객체의 핵심적인 개념 또는 기능만을 추출하는 추상화(abstraction)를 통해 모델링하려는 프로그래밍

추상화, 캡슐화, 상속성, 다형성

추상화 : 객체의 공통적인 속성과 기능을 추출하여 정의하는 것을 말한다
캡슐화 : 객체의 속성과 메서드를 하나로 묶고 일부를 외부에 감추어 은닉하는 것

장점

1. 재사용성
   상속을 통해 프로그래밍시 코드의 재사용을 높일 수 있음.

2. 생산성 향상
   잘 설계된 클래스를 만들어서 독립적인 객체를 사용함으로써 개발의 생산성을 향상시킬 수 있음.

3. 자연적인 모델링
   우리 일상생활의 모습의 구조가 객체에 자연스럽게 녹아들어 있기 때문에 생각하고 있는 것을 그대로 자연스럽게 구현할 수 있다.

4. 유지보수의 우수성
   프로그램 수정시 추가, 수정을 하더라도 캡슐화를 통해 주변 영향이 적기때문에 유지보수가 쉬워서 매우 경제적이라할

수 있다.

단점

1. 개발속도가 느린점
   객체가 처리하려는 것에 대한 정확한 이해가 필요하기에 설계단계부터 많은 시간이 소모 된다.

2. 실행속도가 느린점

객체지향언어는 대체적으로 실행속도가 느리다.

3. 코딩난이도 상승
   다중 상속이 지원되는 C++ 같은 경우에 너무 복잡해져 코딩의 난이도가 상승할 수 있다.

/////////////////////////
객체지향 설계 원칙

SOLID

SRP(Single Responsibility Principle) : 단일 책임 원칙
클래스는 단 하나의 책임을 가져야 하며 클래스를 변경하는 이유는 단 하나의 이유이어야 한다.
OCP(Open-Closed Principle) : 개방-폐쇄 원칙
확장에는 열려 있어야 하고 변경에는 닫혀 있어야 한다.
LSP(Liskov Substitution Principle) : 리스코프 치환 원칙
상위 타입의 객체를 하위 타입의 객체로 치환해도 상위 타입을 사용하는 프로그램은 정상적으로 동작해야 한다.
ISP(Interface Segregation Principle) : 인터페이스 분리 원칙
인터페이스는 그 인터페이스를 사용하는 클라이언트를 기준으로 분리해야 한다.
DIP(Dependency Inversion Principle) : 의존 역전 원칙
고수준 모듈은 저수준 모듈의 구현에 의존해서는 안된다.
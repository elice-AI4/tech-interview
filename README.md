# tech-interview

웹 개발 기술 면접(FE&amp;BE)을 위한 레포지토리입니다.

# 목표

웹 개발 기술 면접에서 충분히 나올 법한 키워드를 중심으로 정리하며 자기 것으로 만듭니다.

main repository로 PR 전에 퀴즈를 내고, 답하면서 정확히 학습했는지 확인합니다!

# 주의할 점!

1. 🖇**출처 표기**는 명확히 해주세요! <br> 각 페이지 말단에 다음과 같이 기재해주세요.

```
ex)
## 출처

### [1]: [네이버 D2-브라우저는 어떻게 동작하는가?](https://d2.naver.com/helloworld/59361)

### [2]: [네이버 포스트-브라우저는 웹페이지를 어떻게 그리나요? - Critical Rendering Path](https://m.post.naver.com/viewer/postView.nhn?volumeNo=8431285&memberNo=34176766)
```

2. 👩‍💻적으면서 **왜/장단점** 생각하고 정리하기! <br> 어떤 기술, 속성에 대해서 왜 필요한지, 어떻게 쓰이는지 생각하고, <br> 장/단점을 위주로 정리합니다

3. 😵‍💫헷갈리는 용어, 비교할 만한 용어끼리는 ">"를 사용하여 정리합니다.

```
> ⭐️URL vs URI: URI는 이름, 위치 또는 그 둘로 고유하게 인터넷에 있는 자원 또는 이름을 특정한다.<br>
URL은 URI의 유형으로 자원뿐만 아니라 인터넷에서 **어떻게 도달**할 것인지도 명시한다.
```

<그럼 이렇게 보여요>

> ⭐️URL vs URI: URI는 이름, 위치 또는 그 둘로 고유하게 인터넷에 있는 자원 또는 이름을 특정한다.<br> URL은 URI의 유형으로 자원뿐만 아니라 인터넷에서 **어떻게 도달**할 것인지도 명시한다.

3. Commit convention

[상태: [주제]]

`ex) add: [1/1-1/브라우저]`
`ex) update: [4/4-1]`

# 기여하는 법

1️⃣ 클론하세요!

```
$ git clone https://github.com/elice-AI4/tech-interview.git
$ cd tech-interview
$ git checkout -b [기여자 이름] main
```

2️⃣ 작성하세요!

```
ex)
> 1_Computer_Science/1-1_Web/Network/브라우저.md

### 렌더링 동작 과정
- 중요 렌더링 경로(Critical Rendering Path): 브라우저가 하나의 화면을 그려내는 과정
1. 서버에서 응답받은 HTML 데이터 파싱
2. 파싱한 결과로 DOM 트리 구축
3. 파싱 중 CSS 파일 링크로 요청 및 파싱
4. CSSOM 구축
5. Render 트리(DOM 트리+CSSOM) 구축
6. Layout 과정
7. 화면에 실제 픽셀 Paint

```

3️⃣ 푸쉬하세요!

```
$ git add .
$ git commit -m "commit message"
$ git push -u origin [기여자 이름]
```

4️⃣ PR하세요!

바로 main으로 merge하지 마시고 우선 PR을 올려주세요.

2명 이상의 다른 contributor에게 확인 comment를 받으면 그 뒤로 merge 합니다.

5️⃣ 목차를 바꿔주세요!

main으로 merge가 완료된 이후 README.md에서 해당 페이지 링크를 걸어주세요!

(예시 추후 작성 예정)

# 받았던 질문

(작성 예정입니다)

# 전체 목차

- 1. Computer Science
  - 1-1. Web/Network
    - 1. Networl
      - 1. basic
      - 2. TCP-IP
      - 3. network device
      - 4. IP
      - 5. HTTP
    - 브라우저 🔥
    - HTTP
      - 쿠키/세션/토큰
      - JWT
      - CORS
      - 아파치와 Nginx
    - HTTPS
    - CSR/SSR
    - RESTful API 🔥
    - OAuth 2.0
    - Socket 통신
  - 1-2. OS 운영체제
    - 1. OS&computer
    - 2. Memory
    - 3. Process&Thread
    - 4. CPU scheduling algorithm
  - 1-3. Data Control
    - JSON 🔥
    - YAML 🔥
  - 1-4. Database
    - 1. basic
    - 2. ERD&regulation
    - 3. trasaction&integrity
    - 4-1. SQL
    - 4-2. NoSQL
    - 5. index/key
    - 6. Join
  - 1-5. Structure
    - MVC pattern
    - MVP pattern
    - MVVM pattern
- 2. Language
  - 2-1. Javascript
    - ECMAScript
    - 실행 컨텍스트, hoisting
    - closure
    - map, filter, reduce
    - 동기/비동기
    - fetch, promise
    - Node.js
  - 2-2. Typescript
  - 2-3. Python
- 3. Front
  - 3-1. HTML/CSS
  - 3-2. React
    - SPA
    - component
    - state
    - rendering
    - hook
- 4. Back

  - 4-1. Express
  - 4-2. Docker
  - 4-3. Kubernetes

- 5. Algorithm
  - 5-1. 시간 복잡도/공간 복잡도
  - 5-2. Data Structure
    - Array/Linked List
    - Hash Table
    - Tree
    - Heap
    - Stack
    - Queue, Deque
  - 5-3. 재귀호출
  - 5-4. 완전탐색
  - 5-5. 분할정복법, 탐욕적 기법
- 6. ECT
  - 6-1. Programming Paradigm
    - declarative&fucntional
    - OOP(Object Oriented Programming)
  - 6-2. 애자일 방법론
  - 6-3. TDD(Test Driven Development)

# RESTful API

## 쓰는 이유
서버와 클라이언트가 데이터를 주고받을 때 가장 많이 사용하는 통신 규격.
요청 주소와 메서드(GET, POST 등), JSON 규격을 이용하여 API를 정의하고 사람이 읽기 쉬운 형태이기 때문에 오늘날 가장 범용적으로 사용.

## 메서드
|이름|이용|형태|
|--|--|--|
|POST|새로운 객체를 생성합니다|Create|
|GET|객체를 가져옵니다|Read|
|PUT/PATCH|기존 객체를 업데이트합니다|Update|
|DELETE|기존 객체를 삭제합니다|Delete|

> PUT과 PATCH의 차이? PUT: 클라이언트가 모든 자원을 업데이트하는 데이터를 보내는 곳의 자원을 변경, PATCH: 클라이언트가 모든 데이터를 변경시키지 않고 부분적인 자원만 업데이트하고자 하는 자원을 변경
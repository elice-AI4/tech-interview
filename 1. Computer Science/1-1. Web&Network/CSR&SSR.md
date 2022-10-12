# 동적 웹의 두 가지 구현 방법

## CSR(Client Side Rendering)

- FE에서 사용자가 페이지에서 보는 동적인 부분을 대부분 처리하는 방식

- FE 코드에 페이지 리소스들이 미리 정의되어 있다

- 서버와의 통신은 API통신을 이용

- 빠른 반응이지만 페이지의 내용은 API 호출이 완료된 후에 보여진다

- 복잡한 프로젝트 구성, 큰 개발 사이즈

| 특징          | CSR                                                                                | SSR                                                       |
| ------------- | ---------------------------------------------------------------------------------- | --------------------------------------------------------- |
| 이름          | Client Side Rendering                                                              | Server Side Rendering                                     |
| 방식          | FE에서 사용자가 페이지에서 보는 동적인 부분을 대부분 처리하는 방식                 | BE에서 페이지 대부분의 영역을 처리해서 FE로 전달하는 방식 |
| 보여주는 방식 | FE 코드에 페이지 리소스들이 미리 정의되어 있다<br/>서버와의 통신은 API 통신을 이용 | BE에서 HTML 파일을 작성해서 FE로 전달                     |
| 규모          | 복잡한 프로젝트 구성, 큰 개발 사이즈                                               | 쉬운 구성, 작은 개발 사이즈                               |
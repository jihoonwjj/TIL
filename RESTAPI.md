# REST API란
- - -
> REST를 기반으로 만들어진 API.

## REST란?

REST(Representational State Transfer)의 약자로 자원을 이름으로 구분하여 해당 자원의 상태를 주고받는 모든 것을 의미한다.

즉, REST는 HTTP URI를 통해 자원을 명시하고, HTTP Method를 통해 해당 자원에 대한 *CRUD Operation*을 적용하는 것을 의미한다.
### CRUD Operation이란?

CRUD란, CREATE(생성), READ(읽기), UPDATE(갱신), DELETE(삭제)를 일컫는 말로, REST에서의 CRUD는 Operation 동작 예시는
```
Create: 데이터 생성(POST)
Read: 데이터 조회(GET)
Update: 데이터 갱신(PUT, PATCH)
Delete: 데이터 삭제(DELETE)
```
가 있다.

## REST의 구성요소

* 자원(Resource): HTTP URI
* 자원에 대한 행위(Verb): HTTP Method
* 저원에 대한 행위의 내용(Representations): HTTP Message Pay Load

## REST의 특징

* 서버 - 클라이언트 구조이다.
* 무상태
* 

# REST API란
- - -
> REST의 원리를 따르는 API. 

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
  * REST는 리소스를 중심으로 설계되어야 한다. 리소스는 고유한 식별자를 가지며, 클라이언트는 이러한 리소스를 조작하기 위해 HTTP 메서드를 사용한다. 
* 무상태
  * 요청 간의 상태를 서버에 저장하지 않는 상태없음 특징을 갖는다. 각 요청은 서버에 대한 완전한 정보를 포함하고 있어야 하며, 서버는 클라이언트의 상태를 관리하지 않는다.
* 캐시 처리 가능
  * 클라이언트는 서버의 응답을 캐시할 수 있다. 이를 통해 동일한 요청에 반복적인 네트워크 요청을 줄임으로써 성능을 향상시킨다.
* 계층화
  * 클라이언트는 중간계층(로드밸런서, 캐시 서버 등)을 통해서버와 통신할 수 있으며, 중간계층은 요청의 처리나 보안등을 담당한다.
* 인터페이스 일관성
  * 리소스에 대한 조작을 위한 HTTP 메소드와 리소스 표현을 위한 미디어 타입을 사용한다.

# REST API의 설계 규칙

* URI는 동사보다는 명사, 대문자 보다는 소문자를 사용해야 한다.
* 마지막에 슬래시를 붙이지 않는다.
* 언더바(_) 대신에 하이폰(-)을 사용한다.
* 파일확장자는 URI에 포함시키지 않는다.
```
X https://example.com/cat.jpg
O https://example.com/cat
```
* 행위를 포함시키지 않는다.
```
X https://example.com/delete-post/1
O https://example.com/post/1
```

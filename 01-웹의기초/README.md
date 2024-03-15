# HTTP

## 1장 HTTP 웹의 기초

### 웹 리소스란?

> 웹에 콘텐츠를 제공하는 모든 것

웹 서버는 모든 HTTP 객체 데이터에 MIME(Multipurpose Internet Mail Extensions) 타입을 설정한다.
우리가 개발할 때 사용하는 Content-Type 혹은 Accept-Type 에서 헤더로 지정한다.
URI는 Uniform Resource Identifier의 약자로서 자원의 식별자 같은 느낌이다.

> https://www.naver.com/special/download.gif

- 첫번재로 오는 https:/ 가 scheme
- 두번째로 오는 www.naver.com 이 인터넷 서버의 주소
- 마지막인 /special/download.gif 가 리소스

### 트랜잭션

HTTP Protocol을 통해서 요청 명령과 응답 결과로 이루어진 하나의 상호작용

### TCP Connection

보통 TCP를 기반으로 HTTP가 동작한다고 한다.

### 그 외 용어들

- proxy: client와 server 사이에 위치한 HTTP 중개자
- cache: 많이 찾는 웹 페이지를 client 가까이에 보관하는 HTTP 창고
- gateWay: 다른 Application과 연결된 특별한 웹 서버
- Tunnel: 단순히 HTTP 통신을 전달하기만 하는 특별한 proxy
- Agent: 자동화된 HTTP 요청을 만드는 준지능적 웹 클라이언트

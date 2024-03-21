# HTTP

## 9장 HTTP 인증

### HTTP 인증이란 ?

HTTP 인증은 웹 서버와 클라이언트 간의 통신에서 사용자를 식별하고 인증하는 과정으로 웹 애플리케이션 및 API와 같은 웹 기반 서비스에 사용자의 보완 및 권한을 관리하는데 중요하다.

### 1. Basic Authentication (기본 인증)

- 사용자 이름과 비밀번호를 인코딩한 문자열을 HTTP 요청 헤더의 "Authorization" 필드에 포함하여 전송
- 매우 안전하지 않은, SSL/TLS와 함께 사용됨

### 2. Bearer Token Authentication (토큰 기반 인증)

- 클라이언트가 발급받은 토큰을 HTTP 요청 헤더의 "Authorization" 필드에 "Bearer" 접두어와 함께 포함하여 전송한다.
- JWT을 사용하여 인증
- 간단한 방식, 상태를 유지하지 않음, 확정성이 높음
- 토큰의 노출 위험, 토큰 관리가 힘듬

### JWT (JSON Web Token)

클레임이라고 불리는 정보를 JSON 형태로 안전하게 전송하기 위한 토큰 기반의 표준

- 일반적으로 인증과 정보 교환에 사용, 서명이 되어 있어 신뢰성 확보

Header : 토큰의 타입과 사용된 알고리즘 정보를 담고 있음, Base64Url로 인코딩
Payload : 클레임 정보, 대상, 발행자, 만료 시간 등 다양한 정보가 포함됨, Base64Url로 인코딩
Signature : Header와 Payload, Secret Key를 사용하여 생성된 서명

### 3. OAuth (Open Authorization)

- 토큰기반 인증 방식, 사용자가 직접 자격을 증명 하는것이 아니라 미리 인증을 받아서 토큰을 발급 받고 이 토큰을 이용하여 API를 요청하는 방식 일반적으로 OAuth 2.0 을 사용 하고있음
- 주로 소셜 미디어 플랫폼 (Facebook, Google, Twitter 등)에서 사용

### 4. API Key Authentication (API 키 인증)

- key 발급을 받고 키 포함해서 서버에 전송
- 주로 공개 API에 접근할 때 사용된다.

### 5. Session-based-Authentication (세션 기반 인증)

- 사용자가 로그인하면 서버는 세션 ID를 생성하고 클라이언트에게 전달한다. 클라이언트는 이 세션 ID를 유지하며 요청 시 서버에 제공하여 인증
- 주로 웹 애플리케이션에서 사용되며, 상태를 유지하는 방식

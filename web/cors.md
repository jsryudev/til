# CORS

`CORS`는 Cross-Origin Resource Sharing (교차 출처 리소스 공유)의 줄임말이다.

브라우저는 보안상의 이유로 다른 출처의 HTTP 요청을 제한한다.  
CORS 체제는 브라우저와 서버 간의 안전한 교차 출처 요청 및 데이터 전송을 지원한다.

서버 사이드에서 `Access-Control-Allow-Origin` 헤더에 응답값을 담음으로서 동작한다.

## CORS 명세

서버 데이터에 사이드 이펙트를 일으킬 수 있는 HTTP 메서드(GET 제외)에 대하여  
preflight(사전 전달) 하여 메서드를 요청하고, 서버가 허가 할 경우 실제 요청 보내도록 한다.  
이 때, 서버는 클라이언트(브라우저)에게 인증정보를 함께 보내야 한다는 조건을 알려줄 수도 있다.

## Example

### 모든 출처에 대한 허용

```
HTTP/1.1 200 OK
Date: Mon, 01 Dec 2008 00:23:53 GMT
Server: Apache/2
Access-Control-Allow-Origin: *
Keep-Alive: timeout=2, max=100
Connection: Keep-Alive
Transfer-Encoding: chunked
Content-Type: application/xml
```

`Access-Control-Allow-Origin`에 \*(와일드 카드)가 포함 된다.

### 특정 출처에 대한 허용

```
HTTP/1.1 200 OK
Date: Mon, 01 Dec 2008 00:23:53 GMT
Server: Apache/2
Access-Control-Allow-Origin: https://foo.example
Keep-Alive: timeout=2, max=100
Connection: Keep-Alive
Transfer-Encoding: chunked
Content-Type: application/xml
```

`Access-Control-Allow-Origin`에 특정 URL이 포함 된다.

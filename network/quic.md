# QUIC

HTTP의 3번째 메이저 버전인 HTTP/3에서는 기존의 TCP/IP를 버리고 UDP를 경유하는 `QUIC`를 프로토콜로 사용한다.  
`QUIC`으로 전환은 헤드 오브 라인 블로킹이라는 기존 HTTP의 문제를 해결한다.

`QUIC`은 2021년 5월 27일 **RFC 9000**이 되었다.  
Ref: https://www.rfc-editor.org/rfc/rfc9000.html

## 헤드 오브 라인 블로킹 (Head-of-line Blocking)

네트워크에서 같은 큐에 있는 패킷이 첫 번째 패킷에 의해 지연될 경우 발생하는 성능 저하 현상.  
처리 속도 지연 및 패킷 손실을 발생시킬 수 있다.

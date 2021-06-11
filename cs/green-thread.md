# Green Thread

`Green Thread`는 런타임 혹은 가상머신에서 OS의 네이티브 `Thread`를 emulate 한다.  
kernel space 대신 user space에서 관리되며, 네이티브 `Thread`가 지원되지 않는 환경에서도 `Thread`를 사용할 수 있다는 장점이 있다.

단점으로 필연적인 오버헤드가 발생한다.

`Coroutine`, `Fibers` 등이 `Green Thread` 범주에 속한다.

## 어원

`Java`의 `Thread` 라이브러리에서 유래 되었다.

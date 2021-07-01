# Pure DI

의존성 그래프를 구성하는 컨테이너는 [Inversion of Control](inversion-of-control.md) 사용이 필수적이라고 이야기 된다.  
하지만 `Pure DI`는 [Inversion of Control](inversion-of-control.md)가 없는 DI이다.

`Pure DI`의 장점으로는 Weakly typed에 대한 문제를 해결한다.  
[Inversion of Control](inversion-of-control.md) Container가 없으므로,
직접 코드로 의존성 그래프를 작성해야 하기 때문에 비용이 높다는 단점이 있다.

의존성 그래프 작성 비용과 [Inversion of Control](inversion-of-control.md) Container 학습비용을 잘 고려하여 DI를 선택해야 한다.

## 참고문서

https://jwchung.github.io/DI%EB%8A%94-IoC%EB%A5%BC-%EC%82%AC%EC%9A%A9%ED%95%98%EC%A7%80-%EC%95%8A%EC%95%84%EB%8F%84-%EB%90%9C%EB%8B%A4

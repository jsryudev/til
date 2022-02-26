# SOLID

로버트 마틴이 제창한 객체 지향 프로그래밍의 다섯가지 설계 원칙으로,
유지보수가 용이하고 유연한 소프트웨어를 만들기 위한 지침이다.

**S**: Single responsibility principle (단일 책임 원칙)  
**O**: Open/closed principle (개방-폐쇄 원칙)  
**L**: Liskov substitution principle (리스코프 치환 원칙)  
**I**: Interface segregation principle (인터페이스 분리 원칙)  
**D**: Dependency inversion principle (의존관계 역전 원칙)

## [Single responsibility principle (단일 책임 원칙)](./srp.md)

### 한 객체는 하나의 책임만 가져야 한다.

## Open/closed principle (개방-폐쇄 원칙)

### 소프트웨어 요소는 확장에는 열려 있으나 변경에는 닫혀 있어야 한다

## Liskov substitution principle (리스코프 치환 원칙)

### 프로그램의 객체는 프로그램의 정확성을 깨뜨리지 않으면서 하위 타입의 인스턴스로 바꿀 수 있어야 한다.

## Interface segregation principle (인터페이스 분리 원칙)

### 특정 클라이언트를 위한 인터페이스 여러 개가 범용 인터페이스 하나보다 낫다

## Dependency inversion principle (의존관계 역전 원칙)

### 프로그래머는 추상화에 의존해야지, 구체화에 의존해선 안된다.

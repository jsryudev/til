# LSP

Liskov Substitution Principle (리스코프 치환 원칙)
프로그램에서 자료형 *S*가 자료형 *T*의 하위형이라면, 필요한 프로그램의 속성 변경 없이 *T*타입의 객체를 *S*타입의 객체로 치환할 수 있어야 한다는 원칙이다.

LSP를 위반하는 전형적인 예로, 너비와 높이의 `getter`, `setter` 메서드를 가진 직사각형 클래스로부터 정사각형 클래스를 파생하는 경우를 들 수 있다.

```typescript
// Rectangle.ts
class Rectangle {
  private width: number;
  private height: number;

  constructor(width: number, height: number) {
    this.width = width;
    this.height = height;
  }

  public setWidth(width: number): void {
    this.width = width;
  }

  public setHeight(height: number): void {
    this.height = height;
  }

  public area(): number {
    return this.width * this.height;
  }
}
```

```typescript
// Square.ts
class Square extends Rectangle {
  constructor(width: number, height: number) {
    super(width, height);
  }

  public setWidth(width: number): void {
    this.width = width;
    this.height = width;
  }

  public setHeight(height: number): void {
    this.width = height;
    this.height = height;
  }

  public area(): number {
    return this.width * this.height;
  }
}
```

LSP 위반은 LSP를 위반한 클래스를 사용하는 코드가 실제로 기대하는 조건에 따라 문제가 될 수도 있고 아닐수도 있다.  
**여기서 중요한 사안은 가변성이다.**  
정사각형과 직사각형이 조회 메서드만 가진다면, LSP 위반을 발생하지 않는다.

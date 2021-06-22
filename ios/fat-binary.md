# Fat Binaray

확장자는 `.a`이며, static하다.  
때문에 컴파일 시간에 링크된다.

[Fat Framework](fat-framework.md)와 달리 `Fat Binaray`는 static, dynamic을 선택할 수 없다.

Fat Binaray는 [Fat Framework](fat-framework.md)와 같이 `lipo` command 를 이용하여,
universal architecture binary로 만들 수 있다.

iPhone용 Binary, simulator용 Banary를 생성하여 [XCFramework](xcframework.md)를 만들 수 있다.

## iPhone용 Binary, simulator용 Banary를 Fat Binary로 만들기

```sh
lipo -create "iphone/Foo.a" "slmulator/Foo.a" -output "Foo"
```

## Foo.framework의 architectures 표시

```sh
$ lipo -i Foo.a
```

## Foo.framework의 i386 architecture 지원을 제거

```sh
lipo -remove i386 Foo.a o Foo.a
```

# Fat Framework

시뮬레이터, 실물 기기에서 모두 동작할 수 있도록,  
x86_64, i386, ARM64, ARMv7 아키텍쳐를 모두 지원하는 Framework를 Fat Framework 라고 한다.

기본적으로 `lipo` 커맨드를 통하여 universal architecture Framework를 생성할 수 있다.

## iPhone용 Framework, simulator용 Framework를 Fat Framework로 만들기

```sh
lipo -create "iphone/Foo.framework/Foo" "slmulator/Foo.framework/Foo" -output "Foo"
```

## Foo.framework의 architectures 표시

```sh
$ lipo -i Foo.framework/Foo
```

## Foo.framework의 i386 아키텍처 지원을 제거

```sh
lipo -remove i386 Foo.framework o Foo.framework
```

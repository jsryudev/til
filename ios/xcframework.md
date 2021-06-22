# XCFramework

`XCFramework`는 WWDC2019에서 Binary Frameworks in Swift라는 제목으로 발표되었다.  
Ref: https://developer.apple.com/videos/play/wwdc2019/416/

Xcode 11부터 제공하는 새로운 Framework format이다.  
Static Framework와 C binary 배포를 지원하며 여러 Framework를 묶어 배포할 수 있다.

Third party SDK를 `XCFramework`로 만들거나,  
Framework로 모듈화 한 기능들을 `Swift Package Manager`(SPM)를 통하여 배포하거나, 관리할 수 있다.

## `.framework`로 XCFramework 만들기

`xcodebuild -create-xcframework`를 사용하여 `.framework`를 `XCFramework`로 빌드할 수 있다.

```sh
xcodebuild -create-xcframework \
  -framework "ios/Foo.framework" \
  -framework "simulator/Foo.framework" \
  -output "Foo.xcframework"
```

## C binary `.a`로 XCFramework 만들기

```sh
xcodebuild -create-xcframework \
  -library "ios/Foo.a" \
  -headers "ios/Foo.h" \
  -library "simulator/Foo.a" \
  -headers "simulator/Foo.h" \
  -output "Foo.xcframework"
```

# App Thinning

Apple App Store에서 제공하는 `App Thinning`은 3가지로 구분할 수 있다.

- Slicing
- Bitcode
- On Demand Resource

## Slicing

App Store에 바이너리를 업로드 할 경우  
지원하는 디바이스에 대해 각기 다른 번들을 생성하고, 디바이스에 가장 적합한 번들을 제공한다.

## [Bitcode](bitcode.md)

TARGET의 Build Settings -> Build Options에서 확인할 수 있다.  
`ENABLE_BITCODE` 옵션이 Yes(true)로 되어 있어야 `App Thinning`이 동작한다.

[Bitcode](bitcode.md)가 활성화 되어 있다면 배포시 App Store에 [Bitcode](bitcode.md)가 업로드 되고,
디바이스에 맞는 바이너리를 App Store에서 컴파일한다.

장점으로는 앱의 사이즈가 줄어드는 효과가 있으나,
단점으로는 dSYM 변경에 의한 Third Party Crash 수집기 동작이 어려워 진다.

## On Demand Resource

필요할 때 리소스를 다운로드 받는다.  
인앱 구매를 예로 들 수 있다.

# Bitcode

`Bitcode`는 LLVM의 IR(Intermediate Representation)이다.  
iOS 9부터 도입 된 `Bitcode`는 활성화하게 되면 앱의 용량이 줄어드는 효과를 볼 수 있다.  
이는 개발자는 여러 아키텍처가 포함되어 있는 **Fat Binary** 대신 `Bitcode`를 AppStore에 업로드 하기 때문이다.

AppStore에서는 `App Thining`, `App Slicing`등의 최적화 작업을 거친 뒤 각 디바이스에 대한 바이너리 컴파일한 뒤, 사용자에게 제공된다.

단점으로는 포함 된 Framework 중 단 1개라도 `Bitcode`가 활성화 되어 있지 않으면 앱에서 활성화 할 수 없다는 점과,  
Firebase Crashlytics와 같은 Third Party Crash 로그 수집기가 동작하기 어려워진다는 점이 있다.  
Third Party Crash 수집기가 동작하기 어려워지는 이유는 아카이브시 결과물인 `dSYM`을 사용할 수 없기 때문이다.

따라서, `Bitcode`가 적용 된 앱의 경우 Organizer 메뉴나, AppStore Connect에서 `dSYM`을 다운로드 받아 사용하여야 한다.

## LLVM IR(Intermediate Representation)

LLVM의 어셈블리와 유사한 저수준 언어

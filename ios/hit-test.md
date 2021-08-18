# Hit Test

```swift
func hitTest(_ point: CGPoint, with event: UIEvent?) -> UIView?
```

하위 View 계층을 탐색하여 터치 이벤트를 받아야 하는 View를 결정한다.  
메서드를 직접 호출할 필요는 거의 없지만 하위 보기에서 터치 이벤트를 숨기기 위해 override 할 수 있다.

View 객체가 hidden 되거나, userInteraction이 disabled 되거나, View의 alpha 값이 0.01보다 작은 경우 이 메서드는 해당 뷰를 무시한다.  
즉, View의 `isHidden`, `isUserInteractionEnabled`, `alpha`에 영향을 받는다.

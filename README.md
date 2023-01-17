# Calculator


## 🧩 개요

계산기

## 🤔 배운 내용

### ✔️ 커스텀 버튼을 스토리보드에 적용하기 (with @IBInspectable, @IBDesignable)

> @IBInspectable

기존의 코드로 작성해야 하는 속성(Attribute)들을 스토리보드에 추가하고 프로퍼티의 값을 쉽게 변경 가능하게 한다.

> @IBDesignable

스토리보드에서 생성한 객체와 소스코드를 연결하여 해당 객체의 현재 속성을 스토리보드에 실시간 반영하여 뷰를 그려준다.


```

import UIKit

@IBDesignable
class RoundButton: UIButton {
  @IBInspectable var isRound: Bool = false {
    didSet {
      if isRound {
        self.layer.cornerRadius = self.frame.height / 2
      }
    }
  }
}
```

> 커스텀 버튼이 적용된 스토리보드 

<img width="242" alt="image" src="https://user-images.githubusercontent.com/42196410/212871804-b4716ba1-c454-4641-993c-b9b488298f11.png">
<img width="254" alt="image" src="https://user-images.githubusercontent.com/42196410/212871934-ee7dd519-9da3-44c3-b222-6adc513f7089.png">


### ✔️ truncatingRemainder

Double, Float 타입을 나머지(%)연산 할때 사용되는 메서드 

```
if let result = Double(self.result), result.truncatingRemainder(dividingBy: 1) == 0 {
  self.result = "\(Int(result))"
}
```

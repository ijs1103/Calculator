# Calculator


## π§© κ°μ

κ³μ°κΈ°

## π€ λ°°μ΄ λ΄μ©

### βοΈ μ»€μ€ν λ²νΌμ μ€ν λ¦¬λ³΄λμ μ μ©νκΈ° (with @IBInspectable, @IBDesignable)

> @IBInspectable

κΈ°μ‘΄μ μ½λλ‘ μμ±ν΄μΌ νλ μμ±(Attribute)λ€μ μ€ν λ¦¬λ³΄λμ μΆκ°νκ³  νλ‘νΌν°μ κ°μ μ½κ² λ³κ²½ κ°λ₯νκ² νλ€.

> @IBDesignable

μ€ν λ¦¬λ³΄λμμ μμ±ν κ°μ²΄μ μμ€μ½λλ₯Ό μ°κ²°νμ¬ ν΄λΉ κ°μ²΄μ νμ¬ μμ±μ μ€ν λ¦¬λ³΄λμ μ€μκ° λ°μνμ¬ λ·°λ₯Ό κ·Έλ €μ€λ€.


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

> μ»€μ€ν λ²νΌμ΄ μ μ©λ μ€ν λ¦¬λ³΄λ 

<img width="242" alt="image" src="https://user-images.githubusercontent.com/42196410/212871804-b4716ba1-c454-4641-993c-b9b488298f11.png">
<img width="254" alt="image" src="https://user-images.githubusercontent.com/42196410/212871934-ee7dd519-9da3-44c3-b222-6adc513f7089.png">


### βοΈ truncatingRemainder

Double, Float νμμ λλ¨Έμ§(%)μ°μ° ν λ μ¬μ©λλ λ©μλ 

```
if let result = Double(self.result), result.truncatingRemainder(dividingBy: 1) == 0 {
  self.result = "\(Int(result))"
}
```

### 5. Computed Properties

```swift
struct DoubleNumber {
    var number: Int
    var doubleNumber: Int {
        get {
            return self.number * 2
        }
        set {
            self.number = newValue / 2
        }
    }
}

var test = DoubleNumber(number: 5)
print(test.doubleNumber)

test.doubleNumber = 18
print(test.number)
```

- 계산속성은 `getter`와 `setter`을 제공한다.
    - getter/setter은 다른 프로퍼티의 값을 간접적으로 검색하고 설정할 수 있다.
- 계산속성은 항상 `var 키워드`를 사용해 **가변 프로퍼티**로 선언해야 한다.
- 

### Setter

- `setter` 을 설정할 때, 새로 받아올 값의 이름을 정하지 않은 경우 default 이름인 `newValue` 가 사용된다.
- `setter`만 존재하는 계산 속성은 없다.

### Getter

- `getter` 의 클로저가 한줄(single expression)일 때, `return` 을 생략해도 암묵적으로 반환된다.
- **Read-Only Computed Properties** 를 만들 수 있다.
    - `getter`만 존재하는 계산 속성을 **읽기 전용 계산 속성**이라고 말한다.
    - 값을 읽을 수는 있지만,  다른 값으로 설정할 수 없다.

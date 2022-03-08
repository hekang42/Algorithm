# programmers

## N진수 게임


[문제링크](https://programmers.co.kr/learn/courses/30/lessons/17687)


### 코드

```swift
func solution(_ n:Int, _ t:Int, _ m:Int, _ p:Int) -> String {
    // 2 * 4 -> 8 digit
    var value: String = ""
    for i in 0...m*t {
        value = value + String(i, radix: n)
    }
    let array = Array(value)
    var ret: String = ""

    for (index, c) in array.enumerated() {
        if (index) % m == p - 1 {
            ret = ret + String(c)
        }
    }

    ret = ret.substring(to: t)
    return ret.uppercased()
}
```

### 풀이 이유
-

### 참고한 내용
- 
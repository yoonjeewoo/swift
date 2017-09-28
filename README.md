# Swift

## let과 var

`let`은 변하진 않는 상수를 선언할 떄, `var`는 변하는 변수를 선언할 때 사용한다.

```
let maxSpeed = 400
//maxSpeed = 200
var currentSpeed = 200
currentSpeed:Int += 100
//currentSpeed += 20.5
```

위의 코드에서 알 수 있듯이, 상수를 한번 선언하면 그 값을 바꿀 수 없으며, 한번 변수의 타입이 정해지면, **바꿀 수 없다**.

## String과 Numbers

`String`은 말그대로 문자열이고, 다음과 같이 사용 할 수 있다.

```
let name = "Jeewoo" 
var greeting = "Hello"
greeting += " " + name //Hello Jeewoo
```
`String`을 이용하면 `Swift`에서 많은 일을 쉽게 해낼수 가 있는데 아래가 그 예시이다.

```
let characters = name.characters
//위에서 선언한 name이라는 상수에 characters라는 메소드를 실행하면, 
//배열과 비슷한 형태와 기능을 가지고 있는 Swift의 Array를 리턴해준다.
let count = characters.count
//위의 코드에서 받은 Array의 개수를 세고 싶을 때는 위와 같이 코드를 입력하면 된다.
let url = "yoonjeewoo.github.io"
let hasProtocol = url.hasPrefix("https://")
//위의 코드는 주어진 URL에 프로토콜(https)가 붙어있는지를 확인하는 코드이다. 
//이 역시 String 내장메소드를 사용하면 편리하게 구할 수가 있다.
print("\(name)")
//변수를 출력하기 위해선 다음과 같이 코드를 작성한다.
```

이전 Chapter에서 살펴보았던 코드를 다시 살펴보자.
```
var currentSpeed = 200
currentSpeed:Int += 100
//currentSpeed += 20.5
```
위 코드의 주석을 풀게 되면 에러가 발생한다. 왜냐하면, `Swift`는 타입을 정확하게 지켜야 하기 때문이다. 그렇다면, `Int`와 `Double`을 더하기 위해선 어떻게 해야할까?

```
var currentSpeed = 200
currentSpeed += 100 //300
currentSpeed += Int(20.5) //320
```
다음과 같이 Int로 타입캐스팅을 해줘야 더할 수 있다. 그렇다면 **다른 경우**를 살펴보자.
```
let pi = 3.14
let diveder = 2
let halfPi = 3.14/Double(diveder)
```
위의 코드도 만약 `Double`로 타입캐스팅을 해주지 않았더라면, 에러가 발생했을 것이다. 이와같이 다른 타입의 값들을 사칙연산 할때는 늘 타입에 유의하고 코드를 작성해야한다.

추가적으로 `Swift`의 `Int`와 `UInt`를 살펴보자.
여기서 `Int`는 우리가 흔히들 아는 그냥 `int`이고, `UInt`는 `unsigned int`의 줄임말이다.
```
let intMax = Int.max
let unsignedMax = UInt.max
let intMin = Int.min
let unsignedMin = UInt.min
```

	
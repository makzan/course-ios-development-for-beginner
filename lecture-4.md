
# Basic of Swift Programming Language

---- 

## Variables and Constant

```swift
var name = "iOS Development"
```

```swift
let constant = 123
```
---- 


## Type

```swift
var name:String = "iOS Development"
```

```swift
let constant:Int = 123
```

---- 

## String

`"String in quote"`

---- 

## String interpolation

```swift
var variable=123.45
var message = "String with \(variable)"
```

---- 

## Basic Types

- Int
- Float/Double
- Bool
- String
---- 

## Type casting

```swift
var num1 = 123
var num2 = 0.45
var num3 = Double(num1) + num2
```
---- 

## if-else

```swift
var isRaining = true
if isRaining {
  print("It is raining.")
}
```
---- 

## if-else

```swift
var height = 170
var money = 5600
if height > 160 && money > 10000 {
  print("Success")
}
```

---- 

## Equal == and ===

- `==` compares value
- `===` compares if they are the same object.

---- 

## switch

```swift
var grade = 0
switch grade {
  case 0:
    var message = "😭"
  case 100:
    var message = "🤩"
  default:
    var message = "😄"  
}
```

---- 
## switch and fallthrough

```swift
var grade = 0
switch grade {
  case 0:
    var message = "😭"
    fallthrough
  case 100:
    var message = "🤩"
  default:
    var message = "😄"  
}
```

---- 

## switch

```swift
var grade = 0
switch grade {
  case 0,100:
    var message = "😭"
  default:
    var message = "😄"  
}
```

---- 

## switch range


```swift
var grade = 0
switch grade {
  case 60...100:
    var message = "😄"
  default:
    var message = "😭"
}
```

---- 

## range

- `1...10` from 1 to 10.
- `1..<10` from 1 to 9.

---- 

## Optional

```swift
var age:Int? = 18
age = age! + 1
```

---- 
```swift
var age:Int? = 18
if age != nil {
  age = age! + 1
}
```

---- 

```swift
var age:Int? = nil
var ageNumber = age ?? 18
```


---- 

## Function

---- 

```swift
func hello() {
  print("Hello iOS")
}

hello()
```

---- 

```swift
func sayHello(to name:String) {
  print("Hello " + name)
}
```

---- 

## API Design Guideline

---- 
^ API Design Guideline

# Clarity is more important than brevity

---- 
^ API Design Guideline

# Include all the words needed to avoid ambiguity

---- 

^ API Design Guideline

# Omit needless words

---- 
^ API Design Guideline

# Prefer grammatical English phrases

---- 

^ Prefer grammatical English phrases
```swift
x.move(from: x, to: y)
X.insert(y, at: x)
X.subViews(havingColor: y)
```

---- 
^ API Design Guideline

# Distinguish mutating and non-mutating

---- 
^ Distinguish mutating and non-mutating
```swift
x.sort()
z = x.sorted()

x.append(y)
z = x.appending(y)
```
---- 
^ API Design Guideline

# Boolean methods and properties should read as assertion

```swift
x.isEmpty
```

---- 

# Argument Labels

```swift
func move(from start:Point, to end:Point) {}
move(from: x, to: y)
```


---- 

# Prepositional phrase on first argument

```swift
// Bad
a.move(toX: b, y: c)
a.fade(fromRed: b, green: c, blue: d)
```

---- 
# Prepositional phrase on first argument

```swift
// Good
a.moveTo(x: b, y: c)
a.fadeFrom(red: b, green: c, blue: d)
```




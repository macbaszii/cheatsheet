#### Assignment
```swift
let constant = "Constant cannot be changed"
var variable = "Variable can be changed later"

var x,y: Int
let x = 0, y = 0
```

#### Types
```swift
let i:Int = -1
let u:UInt = 99

let s:String = "A String"

let f:Float = 1.2
let d:Double = 6.7
let d = 6.7 //inferred to Double

let b:Boolean = true

let convert:Int = Int(1.2)

typealias Celcius = Int
```

#### Optional
```swift
var s?:String
s = "needle"
s = nil

let forced:String = s!

if let forced = s {
  println(forced)
} else {
  println("not found")
}

let forced:String = s ?? "default value" //if (s == nil) use default value
```

### Tuples
```swift
let p1 = (1,2)
let p2 = (x:1, y:2)

let (x1,y1) = p1
let (x1,_) = p1
let x1 = p1.0, y1 = p1.1

let x = p2.x, y= p2.y
```

### String
```swift
let str = "a string"

let emptyStr = String()
let stringSize = countElements(str)
let isEmpty = emptyStr.isEmpty

let c:Character = "a"
let charAt:Character = Array(str)[2]
for c in "string" {
    print(c)
}

let concat = "a" + "b"
let interpolation = "Value is \(str)"
let compare = (str == "another")
```

#### Array
```swift
var colors = [String]()
var colors:[String] = []
var colors:[String] = ["red","green","blue"]

colors += ["yellow"]
colors += ["orange", "purple"]
colors.append("blue")
colors.insert("cyan", atIndex: 1)
colors[0...1] = ["brown", "gray"] //Three dots

let aColor = colors[0]
let subColors = colors[1...2] //Three dots

print(subColors)

for color in colors {
}
for (index, color) in enumerate(colors) {
}
```

#### Dictionary
```swift
var capitals:[String:String] = ["France":"Paris", "Thailand": "Bangkok"]
var capitals = [String:String]()
var capitals:[String:String] = [:]

let cap:String = capitals["Thailand"]! //Dereferece to optionals

cap["England"] = "London" //add
cap["Thailand"] = nil //remove

let keys = [String](dict.keys)
let values = [String](dict.values)


for (key,value) in dict {
}
```

#### Loops
```swift
for i in 1..10 {
}
for var i = 1; i<=10; i++ {
}
```

#### Conditionals
```swift
let point = (1,1)
switch point {
  case (let x, 0): println("point on x with displacement of \(x)")
  case (0, _): println("point on y")
  case (1..5, 1..5): println("point within bounds")
  case let (x,y) where x == y: println("point is on line")
  case let (x,y): println("point out of bounds at \(x), \(y)")
}
```

#### Functions
```swift
func getBounds(numbers:[Int] = []) -> (lower: Int, upper:Int) {

}
func varArgs(numbers:Int...) {

}
func variableParameter(var i:Int) {
  //i can be changed, but no effect on the caller
}
func inoutParameter(inout i:Int) {
  //i can be changed, with effect on caller
}

//External parameters
func findDistance(aPoint p1: Point, anotherPoint p2: Point) -> [Double] {
}
func findDistance(#aPoint: Point, #anotherPoint: Point) -> [Double] {
}
```

#### Comments
```swift
//Single Line
/* Multiple line
   comment */
```

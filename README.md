# Scala CheatSheet

## Basics

```scala
val hello: String = "Hello" // VALUES are immutable constants
var hi: String =  hello  // VARIABLES are mutable
println(hello + " world!")
```

```scala
val number: Int = 1
val bool: Boolean = true
val letter: Char = 'a'
val pi: Double = 3.14
// also: Float, Long, Byte
```

```scala
val piSinglePrecision: Float = 3.1415f
println(f"Pi is about $piSignlePrecision%.3f")
println(s"My variable number=$number")
println(s"3=${1+2}")
```

## Control Flows

```scala
if (0<1) println("True") else println("False")

if (1>0) {
    println("Makes sense")
} else {
    println("Does not make sense")
}
```

```scala
    val number = 3 // same as number : Int=3
    number match {
        case 1 => println("One")
        case 3 => println("Two")
        case _ => println("Else")
    }
```

```scala
for (x <- 1 to 5) {
    println(x)
}

var x = 10
while (x >= 0) {
    println(x)
    x -= 1
}

x = 0
do { println(x); x+=1} while (x <=10)
```

## Functions

```scala
def square(x: Int): Int = {
    x*x
}
println(square(3)) //9
```

```scala
def transform(x: Int, f: Int => Int): Int = {
    f(x)
}

transform(10, x => {val y = y+x})
```

## Data Structures

```scala
// Tuples
val stuff = ("Item1", 3, false) // Multi types tuple
println(stuff._1) // Item1. One based index.
```

```scala
val myDict = "Key" -> "Value"
println(myDict._2) // Value
```

```scala
val myList = List("one", "two", "three") // has to be single type
println(myList(1)) // two
println(myList.head) // one
println(myList.tail) // ("two", "three")

for (x <- myList) {println(x)}
val k = myList.map( (x: String) => {x.reverse} )
```

```scala
val aList = List(1, 2, 3)
val anotherList = List(4, 5, 6)
// concat
val fullList = aList ++ anotherList
println({fullList.reduce( (x: Int, y: Int) => x + y )}) // 21
println({fullList.filter(x: Int) => x > 3}) // List(4, 5, 6)
// Other list functions: .reverse, .sorted, .distinct, .max, .sum, .contains(x)
```

```scala
val myMap = Map(1->2, 3->4)

myMap(3) // 4
myMap.contains(4) // false
```

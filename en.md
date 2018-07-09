
## Common Style Guide

* Put a space after `:`.
* Use 4 spaces for indentation.

## Function

* Declare with `fun`
    * Normal
        ```
        fun sum(a: Int, b: Int): Int {
            return a + b
        }
        ```
    * Short (Single-Expression)
        ```
        fun sun(a: Int, b: Int): Int = a + b
        ```
    * Do not put a space before an opening parenthesis in method declaration or method call.
* As default, function is final. To make it overrideable, add `open` to the head.
    ```
    open fun function() { ... }
    ```
* Modifier

    | Keyword  | Effect on top-level declarations | Effect on Class Members |
    |:--|:--|:--|
    | public | visible everywhere | visible everywhere if class is accessible |
    | private | visible inside the file only | visible inside the class only |
    | protected | - | visible in class and subclasses |
    | internal | visible inside the same module | visible in the same module, if class is accessible |

* Main Funcition
    ```
    fun main(vararg args: String) { }
    ```
* Extension Function
    ```
    fun Class.function() { ... }
    ```
* Anonymous Function

```
val anonymousFunction = fun(x: Int, y: Int): Int { return x + y }
```
   
* Lambda

```
val lambda1 = { x: Int, y: Int -> x + y }
val lambda2: (Int, Int, Int) -> Int = { x, y, z -> x * y * z }

```

* Operator

```
```

## Variable

* Declation
    ```
    val a = 1  // can be changed 
    var b = 2L // can't be changed
    ```
    * Top-level or object `val` properties with no custom get function) should be uppercase underscore-separated names.
* Declaring Constant: only for primitive types
    ```
    const val A = 1
    ```
    * Names of constants (marked with `const`) should be uppercase underscore-separated names.
* Nullable Type
    * `Type?` represents `Type` or `null`.
        ```
        var a: Int?
        a = 1
        a = null
        ```
        * Do not put a space before `?`
    * `?:` (elvis operator), `!!`
    * `?.`
         * Never put a space around . or ?.
    * `as?`
   
## Flow Control

* Put spaces between control flow keywords (`if`, `when`, `for` and `while`) and the corresponding opening parenthesis.

### `if` expression

* Returns value.
* `if (condition) a else b`
* ```if (condition) { a } else { b }```

### `when` expression

Returns value.

* Pattern 1
    ```
    when (value) {
        a -> { ... }
        b, c -> { ... }
        in d -> { ... }
        is Type => { ... }
        else -> { ... }
    }
    ```
* Pattern 2
    ```
    when {
        a == 2 -> 1
        b > 2 -> 2
        else -> 3
    }
    ```

### `for` loop

```
for (c in "sequence") { ... }
for ((i, c) in "sequence".withIndex()) { println("$i: $c") }
```

#### Loop for collection

```
for (c in 'A'..'Z') { ... }
for (i in intArrayOf(1, 2, 3)) { ... }
```

#### Loop for number

##### Ordinary Order

```
for (i in 1..10) { ... }
for (i in 1..10 step 3) { ... }
```

The number just after `step` must be greater than 0.

##### Reverse Order

```
for (i in 10 downTo 5) { ... }
for (i in 10 downTo 5 step 2) { ... }
```

### `while` loop

```
while (condition) { ... }
```

```
do { ... } while (condition)
```

## Class

### Class Common

* As default, Kotlin class is final class, can't be inherited.
    * If you want to inherit, add `open` to before the `class` identifier.
        ```
        open class Config { ... }
        ```

* Primary Constructor
   ```
   class A(name: String, val propertyValue1: Int, var propertyValue2: Int) {
      init {
         // initializer
      }
   }
   ```
   * Do not put a space before an opening parenthesis in a primary constructor declaration
* Secondary Constructor
   ```
   class A(name: String) {
      fun constructor(int: Int): this(int.toString()) {
         // secondary constructor
      }
   }
   ```
* Instanciation
   ```
   val a = ClassName()
   ```
* Inheritance
    ```
    class Parent
    class Child() : Parent()
    ```
    * Put space before `:` which seperates subclass and superclass.
* Property
    * Plain
    ```
    val a: Int = 1
    var b: Long = 2
    ```
    * With Accessors
    ```
    var c: Boolean
    get () { return true }
    set (value) { field = value }
    ```
* Modifire


### Data Class

* For value object.

```
data clss User(name: String, email: Address)
```

### Abstract Class

```
abstract class AbstractClass {
   abstract val a: Int
   abstract fun b()
}
```

### Enum Class

* Simple Version
    ```
    enum class EnumClass(val a: Int, var b: Int) {
      First(1, 1),
      Second(2, 2)
    }
    ```
* With Function
    ```
    interface EnumInterface { fun p() = { println(1) } }
    enum class EnumClass(val a: Int) : EnumInterface {
        First(1) {
            override fun enumFunction() { ... }
        },
        Second(2) {
            override fun enumFunction() { ... }
        };
        abstract fun enumFunction() { ... }
    }
    ```
* Naming
    * Either uppercase underscore-separated names or regular camel-humps names starting with an uppercase letter, depending on the usage.

### Sealed Class


### Object

* Internally, singleton class
    ```
    object Object {
        const val c = 1
        fun objectFunction() { ... }
    }
    ```

### Interface

```
interface Interface {
    val value: Long
    fun interfaceFunction1(): Int
    fun interfaceFunction2() { println(1) }
}
class InheritClass : Interface {
    override val value = 1L
    override fun interfaceFunction1() = 1
}
```

## Type

### Basic Type

* Number
    * `Int`, `Short`, `Long`, `Float`, `Double`, `Byte`
* `Boolean`: `true` and `false`
    * Operated by `||`, `&&`, and `!`
* `Char`: represents like 'C'
    * Can add number: `'C' + 1 // 'D'`
* `String`

### Collection

List, Map, Array

### Alias

* `typealias`: Add alias to a type.
   ```
   typealias Matrix = Array<DoubleArray>
   typealias IntPredicate = (Int) -> Boolean
   ```
   * `typealias` can be used in top level.

## Scope Function

| Identifier | Is extension function | The object is represented as | return value |
|:--|:--|:--|:--|
| `also` | Yes | `it` | The Object |
| `let` | Yes | `it` | Result |
| `apply` | Yes | `this` | The Object |
| `run` | Yes | `this` | Result |
| `with` | No | `this` | Result |

## Delegation

* Variable
    ```
    val a by lazy {
        1 + 1
    }
    ```
* observable
* Function

## DSL Development

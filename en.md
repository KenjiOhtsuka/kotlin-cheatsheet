
## Coding Rule

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
* Anonymous Function
* Lambda



## Variable

* Declation
    ```
    val a = 1  // can be changed 
    var b = 2L // can't be changed
    ```
* Declaring Constant: only for primitive types
    ```
    const val a = 1
    ```
* Nullable Type
    * `Type?` represents `Type` or `null`.
        ```
        var a: Int?
        a = 1
        a = null
        ```
    * `?:`, `?.`, `!!`
   
## Flow Control

* `if` expression
    * Returns value.
    * `if (condition) a else b`
    * ```if (condition) { a } else { b }```
* `when` expression
    * Returns value.
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
* `for` loop
* `while` loop

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
    interface EnumInterface { fun p() = { println(1) }}
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


### Sealed Class


### Object

* Internally, singleton class
    ```
    object Object {
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

### Collection

## Scope Function

> let, with, run, apply, also

| Identifier | Is extension function | The object is represented as | return value |
|:--|:--|:--|:--|
| `also` | Yes | `it` | The Object |
| `let` | Yes | `it` | Result |
| `apply` | Yes | `this` | The Object |
| `run` | Yes | `this` | Result |
| `with` | No | `this` | Result |

## Delegation

* Property
* Function

## DSL Development

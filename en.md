
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
        when (condition) {
            a -> {}
            in b -> {}
            is Type => {}
            else -> {}
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

* Primary Constructor
* Secondary Constructor
* Inheritance
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

### Enum Class

### Sealed Class

### Object

### Interface

## Type

### Basic Type

### Collection

## Scope Function

> let, with, run, apply, also

## Delegation

* Property
* Function

## DSL Development


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
    
### Data Class

### Abstract Class

### Enum Class

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

> if you here for requesting Kotlin Cheat Sheet, I recommend to see the following URLs.
> * https://blog.kotlin-academy.com/kotlin-cheat-sheet-1137588c75a
> * https://kotlinexpertise.com/dzone_refcard_kotlin/

* Declaring Function
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

* Declaring Variables
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
    *

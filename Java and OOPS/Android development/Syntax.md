```kotlin
fun start(): String {
    return "OK"
}
```
- **`fun`**: This keyword is used to define a function in Kotlin. It is similar to how you define a function with `function` in JavaScript or `def` in Python.
    
- **`start`**: This is the name of the function. Function names should be descriptive and follow the camelCase naming convention by Kotlin standards.
    
- **`()`:** These parentheses indicate that the function does not take any arguments. If the function were to take parameters, they would be listed inside the parentheses.
    
- **`: String`**: This part indicates the return type of the function. In this case, the function returns a value of type `String`. In Kotlin, return types are explicitly declared after a colon (`:`) when defining functions that return values.
    
- **`= "OK"`**: This is a shorthand syntax for returning a value directly without using the `return` keyword. The `=` operator signifies that the function will return the value immediately after it. The function here returns the string `"OK"`.

A concise way to define a function is 
```kotlin
fun start(): String = "OK"
```

## Function Arguments
- #### Default Arguments
- #### Named Arguments

> Default: If you don't say anything, you get what's already set.  
> Named: You can be very specific about what you want, in any order! 


## Strings and String Literals

Strings in kotlin are represented by the type string.
Generally strings are sequence of characters in double quotes (").
```kotlin
val str = "abc 123"
```

> Strings are immutable, once I initialize a string I cannot modify or assign a new value to it

#### String Literals
> -> Escaped Strings 
> -> Multiline Strings


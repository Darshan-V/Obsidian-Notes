**Java is statically typed** : which means type of a variable is known at *compile-time* . Assigning a value to the variable is known as defining a variable, a variable is defined by explicitly specifying it's type
```java
int explicitVar = 10
```
**Java is an object oriented language and required all the functions defined inside a class**
```java
class Calculator {
//....
}
```

**A function inside a class is know as method**. Each method can have zero or more parameters. All parameters must be explicitly typed, there is no type inference for parameters, similarly the return type must also be specified. To allow a method to be called by other classes, the public access modifier must be added.

```java
class Calculator {
	public int add (int x, int y){
		return x + y;
	}
}
```

**Invoking or Calling a method is done by specifying it's class and method name and passing arguments for each of the method's parameters**

```java
int sum = new Calculator.add(10, 5)
```

## Strings
#### Modifiers
**Methods**

| **Modifier and Type** | **Method and Description**                                                                                                                                               |
| --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `int`                 | `indexOf(int ch)`<br>Returns the index within this string of the first occurrence of the specified character.                                                            |
| `int`                 | `indexOf(int ch, int fromIndex)`<br>Returns the index within this string of the first occurrence of the specified character, starting the search at the specified index. |
| `int`                 | `indexOf(String str)`<br>Returns the index within this string of the first occurrence of the specified substring.                                                        |
| `int`                 | `indexOf(String str, int fromIndex)`<br>Returns the index within this string of the first occurrence of the specified substring, starting at the specified index.        |
| `String`              | `substring(int beginIndex)`<br>Returns a new string that is a substring of this string.                                                                                  |
| `String`              | `substring(int beginIndex, int endIndex)`<br>Returns a new string that is a substring of this string.                                                                    |
| `String`              | `trim()`<br>Returns a copy of the string, with leading and trailing whitespace omitted.                                                                                  |
| `String`              | `toLowerCase()`<br>Converts all of the characters in this String to lower case using the rules of the default locale.                                                    |
| `String`              | `toLowerCase(Locale locale)`<br>Converts all of the characters in this String to lower case using the rules of the given Locale.                                         |

### Booleans
**Represented by *boolean* type**, which value can be either `true` or `false`.
#### Three boolean operators in `Java`
- `!` NOT : negates the boolean
- `&&` AND : takes two booleans and and returns `true` only if both are true.
- `||` OR : returns `true` if any one of the booleans are true.
```java
!true // => false 
!false // => true 
true && false // => false 
true && true // => true 
false || false // => false 
false || true // => true
```


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

## IF - ELSE (conditionals)
```java
class Car {
	void drive() { 
		if (fuel > 5) {
			 fuel--; 
			 } 
			 else if (fuel > 0) { 
				 turnOnFuelLight(); 
				 fuel--; 
			} 
			else { 
				stop(); 
			} 
	} 
}
```

## Number
#### Types of numbers
- **Integers**
- **Floating point**
*common numeric types `int` `double` *
- `int` can be converted to `double`, reverse doesn't hold, to achieve that need to *cast into int*, 
In Java, there are two types of casting:

- **Widening Casting** (automatically) - converting a smaller type to a larger type size  
    `byte` -> `short` -> `char` -> `int` -> `long` -> `float` -> `double`  
      
    
- **Narrowing Casting** (manually) - converting a larger type to a smaller size type  
    `double` -> `float` -> `long` -> `int` -> `char` -> `short` -> `byte`

## Chars
`type` smallest addressable components of text.
- Multiple `char`s can comprise a string such as `"word"` or `char`s can be processed independently. Their literals have single quotes e.g. `'A'`
- `java.lang.Character` class contains many builtin library methods to inspect and manipulate `char`.
```java
//SqueakyClean example from exercism
class SqueakyClean { static String clean(String identifier) { 
StringBuilder res = new StringBuilder(); 
boolean dashFlag = false; 
for(int i=0; i < identifier.length(); i++){ 
char c = identifier.charAt(i); 
if ( c == ' ' ){ 
res.append('_'); 
}
else if( c == '-'){
dashFlag = true; 
} 
else if ( Character.isISOControl(c) ){
res.append("CTRL"); 
} 
else if (Character.isDigit(identifier.charAt(i))) { 
if (identifier.charAt(i) == '4') { 
res.append("a");
} 
if (identifier.charAt(i) == '3') {
res.append("e"); 
} 
if (identifier.charAt(i) == '0')
{ res.append("o");
} 
if (identifier.charAt(i) == '1') { 
res.append("l"); 
}
if (identifier.charAt(i) == '7') {
res.append("t"); 
} 
} 
else if ( Character.isLetter(c) && (c < 'α' || c > 'ω')){
if(dashFlag){
	c = Character.toUpperCase(c); 
			 dashFlag = false; 
			 } res.append(c); 
			 } 
			 }
			  return res.toString(); 
			  }
			   }
```

- squeakyClean feedback
- You don't need to go through all the characters in the string, except perhaps for the character conversion to upper case after hyphen. The String class has two methods called **replace** and **replaceAll**:
```java
private static String convertLeetspeak(String text) {
var transformedText = text.replaceAll("0", "o") 
.replaceAll("1", "l") 
............... return transformedText;
}
```
- Always try to break the problem into very small functions. Your code will be much more readable. And use descriptive names for variables and methods.
## Nullability
**`null` literal is used to denote the absence of a value**

## Classes
- The primary object-oriented construct in Java is the _class_, which is a combination of data ([_fields_](https://docs.oracle.com/javase/tutorial/java/javaOO/classvars.html)), also known as instance variables, and behavior ([_methods_](https://docs.oracle.com/javase/tutorial/java/javaOO/methods.html)). The fields and methods of a class are known as its _members_.
- [`public`](https://en.wikibooks.org/wiki/Java_Programming/Keywords/public): the member can be accessed by any code (no restrictions).
- [`private`](https://en.wikibooks.org/wiki/Java_Programming/Keywords/private): the member can only be accessed by code in the same class.
- he above-mentioned grouping of related data and behavior plus restricting access to members is known as [_encapsulation_](https://en.wikipedia.org/wiki/Encapsulation_(computer_programming)),

## Ternary Operators
The _ternary operator_ is a lightweight, compact alternative for simple _if/else_ statements.
```java
boolean expr = 0 != 200;

int value = expr ? 22 : 33; 
```

## Arrays
```java
type[] variableName = new type[size];
```

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

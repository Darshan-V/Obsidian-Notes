### Variable Declaration
![[Pasted image 20240808120147.png]]

### Variable initialisation
![[Pasted image 20240808120245.png]]

#### *Example of declaring and initialising variable*
```java
int count = 10;
```

## Types of Variables
1. Local Variables
2. Instance Variables
3. Static Variables

1. ==**Local Variables:**== Local Variables are variables that are declared inside the body of a method.
2. ==**Instance Variables:**== Instance Variables are defined with the STATIC keyword. They are defined outside the method declaration. They are object specific and are known as instance variables.
3. ==**Static Variables:**== Static variables are initialised only once, at the start of the program execution. These variables should be initialised first, before initialisation of any instance variables.
#### *Example*
```java
class car {
	static char bodyType = "hatchback";//(static variable)
	char wheel = "3 spoke alloy";//(instance variable)
	void method{
		char drive = "fwd";//(local variable)
	}
}
```

## ==Data Types in Java==
Data types in java are defined as specifiers that allocate different sizes and types of value that can be stored in the variable or identifier. Java has a rich set of data types.

#### Two Parts of data types in Java
1. Primitive data types -> These datatypes are predefined and available within Java language. **Primitive values do not share state with other primitive values**
2. Non-primitive data types -> 
![[Pasted image 20240808123047.png]]

### Understanding Primitives in Java

Java has **eight** primitive data types: `byte`, `short`, `int`, `long`, `float`, `double`, `char`, and `boolean`. These are the most basic data types in Java, and they differ from objects in a few key ways:

1. **Memory Allocation**:
    
    - Primitive types are stored directly in the memory location (or stack) where the variable is declared.
    - Each primitive variable has its own memory space.
2. **Value Copying**:
    
    - When you assign the value of one primitive variable to another, Java creates a copy of that value.
    - The two variables now hold the same value, but they are completely independent of each other.
    - Changing the value of one variable does not affect the other.

### What Does "Do Not Share State" Mean?

"Do not share state" means that primitive variables operate independently. Each variable that holds a primitive value has its own state, which is its value. These variables do not reference or point to the same memory location. Thus, any changes made to one variable do not impact any other variable.

#### Example:

```java
int a = 5; 
int b = a; // b is now 5, but independent of a  a = 10;
// Changing a does not change b 
System.out.println(a); // Outputs: 10 
System.out.println(b); // Outputs: 5
```

|Data Type|Default Value|Default size|
|---|---|---|
|byte|0|1 byte|
|short|0|2 bytes|
|int|0|4 bytes|
|long|0L|8 bytes|
|float|0.0f|4 bytes|
|double|0.0d|8 bytes|
|boolean|false|1 bit|
|char|‘\u0000’|2 bytes|

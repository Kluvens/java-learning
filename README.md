# java-learning

##  Basic Java
Code for "Hello World"
```java
public class Main {
  public static void main(String[] args) {
    System.out.println("Hello World");
  }
}
```
- Everyline of code that runs in Java must be inside a class. The name of the java file must match the class name.
- Any code inside the ```main()``` method will be executed.
- The curly braces ```{}``` marks the begining and the end of a block of code.
- ```println()``` method is short for print line.
- each code statement must end with a semicolon(```;```).

## Java comments
- Single-line comments start with two forward slashes (```//```).
- Multi-line comments start with ```/*``` and ends with ```*/```. Any text between ```/*``` and ```*/``` will be ignored by Java.

## Java variables
There are different types of variables(Primitive data types).
- ```String``` - stores text
- ```int``` - stores integers
- ```float``` - stores floating point numbers
- ```char``` - stores single characters
- ```boolean``` - stores true or false
- ```short``` - for integers from -32768 to 32767
- ```long``` - for integers from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807
- ```double``` - for 15 decimal digits

Declaring (Creating) Variables
```type variableName = value;```

identifiers are the names given to variables.

Primitive types are predefined (already defined) in Java. Non-primitive types are created by the programmer and is not defined by Java (except for String).

Examples of non-primitive types are Strings, Arrays, Classes, Interface, etc.

Type casting:
widening casting(automatically) - converting a smaller type to a larger type size byte -> short -> char -> int -> int -> float -> double

## Java operators
Java operators include ```+, -, *, /, %, ++, --, =, +=, -=, *=, /=, %=, &=, |=, ^=, >>=, <<=, ==, !=, >, <, >=, <=, &&, ||, !```

## Java strings
- we can get the length of string by using length() method
- we can get lower case string by toLowerCase()
- we can get upper case string by toUpperCase()
- we can get the index of the first occurence of a text in a string by indexOf()
- we can concatenate by + or concat method
- ```\'``` for ```'``` and ```\"``` for ```"``` and ```\\``` for ```\```

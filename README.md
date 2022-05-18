# Basic Java

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

## Java Math
- Math.max(x, y) method can be used to find the highest value of x and y
- Math.min(x, y) method can be used to find the lowest value of x and y
- Math.sqrt(x) method returns the square root of x
- Math.abs(x) method returns the absolute value of x
- Math.random() returns a random number between 0.0 and 1.0

## Java if... else
``` java
int time = 22;
if (time < 10) {
  System.out.println("Good morning.");
} else if (time < 20) {
  System.out.println("Good day.");
} else {
  System.out.println("Good evening.");
}
```

``` java
int time = 20;
String result = (time < 18) ? "Good day." : "Good evening.";
System.out.println(result);
```

``` java
int day = 4;
switch (day) {
  case 6:
    System.out.println("Today is Saturday");
    break;
  case 7:
    System.out.println("Today is Sunday");
    break;
  default:
    System.out.println("Looking forward to the Weekend");
}
```

## Java while loop
``` java
int i = 0;
while (i < 5) {
  System.out.println(i);
  i++;
}
```

``` java
int i = 0;
do {
  System.out.println(i);
  i++;
}
while (i < 5);
```

## Java for loop
``` java
for (int i = 0; i < 5; i++) {
  System.out.println(i);
}
```

## Java for each loop
``` java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
for (String i : cars) {
  System.out.println(i);
}
```

## Java break and continue
``` java
for (int i = 0; i < 10; i++) {
  if (i == 4) {
    break;
  }
  System.out.println(i);
}
```

``` java
for (int i = 0; i < 10; i++) {
  if (i == 4) {
    continue;
  }
  System.out.println(i);
}
```

## Java arrays
``` java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
int[] myNum = {10, 20, 30, 40};
```

Access the elements of an array
``` java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
System.out.println(cars[0]);
```

Change an array element
``` java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
cars[0] = "Opel";
```

Array length
``` java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
System.out.println(cars.length);
```

Loop through an array
``` java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
for (int i = 0; i < cars.length; i++) {
  System.out.println(cars[i]);
}
```
``` java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
for (String i : cars) {
  System.out.println(i);
}
```

## Java multi-dimensinal arrays
``` java
int[][] myNumbers = { {1, 2, 3, 4}, {5, 6, 7} };
```
``` java
public class Main {
  public static void main(String[] args) {
    int[][] myNumbers = { {1, 2, 3, 4}, {5, 6, 7} };
    for (int i = 0; i < myNumbers.length; ++i) {
      for(int j = 0; j < myNumbers[i].length; ++j) {
        System.out.println(myNumbers[i][j]);
      }
    }
  }
}
```

## Java methods
A method is a block of code which only runs when it is called
``` java
public class Main {
  static void myMethod() {
    System.out.println("I just got executed!");
  }

  public static void main(String[] args) {
    myMethod();
  }
}
```

Java method parameters
``` java
public class Main {
  static void myMethod(String fname) {
    System.out.println(fname + " Refsnes");
  }

  public static void main(String[] args) {
    myMethod("Liam");
    myMethod("Jenny");
    myMethod("Anja");
  }
}
```

Multiple parameters
``` java
public class Main {
  static void myMethod(String fname, int age) {
    System.out.println(fname + " is " + age);
  }

  public static void main(String[] args) {
    myMethod("Liam", 5);
    myMethod("Jenny", 8);
    myMethod("Anja", 31);
  }
}
```

Return values
``` java
public class Main {
  static int myMethod(int x) {
    return 5 + x;
  }

  public static void main(String[] args) {
    System.out.println(myMethod(3));
  }
}
```

A method with if... else
``` java
public class Main {

  // Create a checkAge() method with an integer variable called age
  static void checkAge(int age) {

    // If age is less than 18, print "access denied"
    if (age < 18) {
      System.out.println("Access denied - You are not old enough!");

    // If age is greater than, or equal to, 18, print "access granted"
    } else {
      System.out.println("Access granted - You are old enough!");
    }

  }

  public static void main(String[] args) {
    checkAge(20); // Call the checkAge method and pass along an age of 20
  }
}
```

## Java method overloading 
Multiple methods can have the same name as long as the number and/or type of parameters are different.
``` java
static int plusMethod(int x, int y) {
  return x + y;
}

static double plusMethod(double x, double y) {
  return x + y;
}

public static void main(String[] args) {
  int myNum1 = plusMethod(8, 5);
  double myNum2 = plusMethod(4.3, 6.26);
  System.out.println("int: " + myNum1);
  System.out.println("double: " + myNum2);
}
```

## Java Scope
In Java, variables are only accessible inside the region they are created. This is called scope.

Method Scope
``` java
public class Main {
  public static void main(String[] args) {

    // Code here CANNOT use x

    int x = 100;

    // Code here can use x
    System.out.println(x);
  }
}
```

Block Scope
``` java
public class Main {
  public static void main(String[] args) {

    // Code here CANNOT use x

    { // This is a block

      // Code here CANNOT use x

      int x = 100;

      // Code here CAN use x
      System.out.println(x);

   } // The block ends here

  // Code here CANNOT use x

  }
}
```

## Java recursion
Recursion is the technique of making a function call itself.
``` java
public class Main {
  public static void main(String[] args) {
    int result = sum(10);
    System.out.println(result);
  }
  public static int sum(int k) {
    if (k > 0) {
      return k + sum(k - 1);
    } else {
      return 0;
    }
  }
}
```

# Java OOP(Object-Oriented Programming)

## Java classes/objects
Everything in Java is associated with classes and objects, along with its attributes and methods. For example: in real life, a car is an object. The car has attributes, such as weight and color, and methods, such as drive and brake.

create a class:
``` java
public class Main {
  int x = 5;
}
```

create an object
``` java
public class Main {
  int x = 5;

  public static void main(String[] args) {
    Main myObj = new Main();
    System.out.println(myObj.x);
  }
}
```

multiple objects
``` java
public class Main {
  int x = 5;

  public static void main(String[] args) {
    Main myObj1 = new Main();  // Object 1
    Main myObj2 = new Main();  // Object 2
    System.out.println(myObj1.x);
    System.out.println(myObj2.x);
  }
}
```

## Java class attributes
``` java
public class Main {
  int x = 5;

  public static void main(String[] args) {
    Main myObj = new Main();
    System.out.println(myObj.x);
  }
}
```

override existing values:
``` java
public class Main {
  int x = 10;

  public static void main(String[] args) {
    Main myObj = new Main();
    myObj.x = 25; // x is now 25
    System.out.println(myObj.x);
  }
}
```

multiple attributes
``` java
public class Main {
  String fname = "John";
  String lname = "Doe";
  int age = 24;

  public static void main(String[] args) {
    Main myObj = new Main();
    System.out.println("Name: " + myObj.fname + " " + myObj.lname);
    System.out.println("Age: " + myObj.age);
  }
}
```

## Java class methods
``` java
public class Main {
  static void myMethod() {
    System.out.println("Hello World!");
  }

  public static void main(String[] args) {
    myMethod();
  }
}
```

**Static vs. Non-static**
we created a static method, which means that it can be accessed without creating an object of the class, unlike public, which can only be accessed by objects
``` java
public class Main {
  // Static method
  static void myStaticMethod() {
    System.out.println("Static methods can be called without creating objects");
  }

  // Public method
  public void myPublicMethod() {
    System.out.println("Public methods must be called by creating objects");
  }

  // Main method
  public static void main(String[] args) {
    myStaticMethod(); // Call the static method
    // myPublicMethod(); This would compile an error

    Main myObj = new Main(); // Create an object of Main
    myObj.myPublicMethod(); // Call the public method on the object
  }
}
```

Access methods with an object
``` java
// Create a Main class
public class Main {
 
  // Create a fullThrottle() method
  public void fullThrottle() {
    System.out.println("The car is going as fast as it can!");
  }

  // Create a speed() method and add a parameter
  public void speed(int maxSpeed) {
    System.out.println("Max speed is: " + maxSpeed);
  }

  // Inside main, call the methods on the myCar object
  public static void main(String[] args) {
    Main myCar = new Main();   // Create a myCar object
    myCar.fullThrottle();      // Call the fullThrottle() method
    myCar.speed(200);          // Call the speed() method
  }
}
```

## Java constructors
A constructor in Java is a special method that is used to initialize objects. The constructor is called when an object of a class is created. It can be used to set initial values for object attributes
``` java
public class Main {
  int modelYear;
  String modelName;

  public Main(int year, String name) {
    modelYear = year;
    modelName = name;
  }

  public static void main(String[] args) {
    Main myCar = new Main(1969, "Mustang");
    System.out.println(myCar.modelYear + " " + myCar.modelName);
  }
}
```

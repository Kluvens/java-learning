# Basic Java

## Object oriented programming (OOP)
- programmers concentrate on creating their own user-defined types called classes.
- each class contains data as well as the set of methods that manipulate the data.
- an instance of a user-defined type is called an object
- OOP encapsulates data and methods into objects, the data and methods of an object are intinately tried together.
- objects have the property of information hiding.

### Inheritance in object oriented programming
- Inheritance is a form of software reusability in which new classes are created from the existing classes by absorbing their attributes and behaviours.
- instead of defining completely new class, the programmer can designate that the new class is to inherit attributes and behaviours of the existing class which is called superclass. The new class is referred to as subclass.
- programmers can add more attributes and behaviours to the subclass, hence, normally subclasses have more features than their super class.

**Is-a - inheritance relationship**
- is an "is-a" relationship, an object of a subclass may aslo be treated as an object of the superclass.
- use inheritance to model "is-a" relationship

**Has-a association relationship**
- In a "has-a" relationship, a class object has an object of another class to store its state or do its work.
- The "has-a" relationship is quite different from an "is-a" relationship.
- "Has-a" relationship are examples of creating new classes by composition of existing classes.

### classes and objects
- a class is a collection of data and methods that operate on that data
- objects are instances of a class and in java, objects are created by instantiating a class
- we can access data fields of an object
- to access the methods of an object, we can use the same syntax as accessing the data of an object

## Super calsses, objects, and the class hierarchy
- every class has a superclass
- if we don't define a superclass, by default, the superclass is the class Object
- Object class is the only class that does not have a superclass
- The methods defined by Object can be called by any java object(instance)

## Abstract classes
Using abstract classses,
- we can declare classes that define only part of an implementation
- leaving extended classes to provide specific implementation of some or all the methods

The benefits of an abstract class:
- is that methods may be declared such that the programmer knows the interface deinition of an object.
- however, methods can be implementated differently in different subclasses of the abstract class.

Some rules about abstract classes:
- an abstract class is a class that declared abstract
- if a class includes abstract methods, then the class itself must be declared abstract
- an abstract class cannot be instantiated
- a subclass of an abstract class can be instantiated if it overrides each of the abstract methods of its superclass and provides an implementation for all of them
- if a subclass of an abstract class does not implement all the abstract methods it inherits, that subclass is itself abstract

``` java
public abstract class Shape {
	public abstract double area();
	public abstract double circumference();
}
```

## single inheritance vs. multiple inheritance
- in java, a new class can extend exactly one superclasses - a model known as single inheritance
- in java, interface in the class hierarchy can be used to add multiple inheritance

## Interfaces
- interfaces are like abstract classes, but with few important difference
- all the methods defined within an interface are implicitly abstract, which means we don't need to use abstract keyword
- variables declared in an interface must be static and final, that means, they must be constants
- just like a class extends its superclass, it also can optionally implements an interface
- in order to implement an interface, a class must first declare the interface in an implements clause, and then it must provide an implementation for all of the abstract methods of the interface
- a class can implements more than one interfaces
- interfaces can have sub-interfaces just like classes can have subclasses
- a sub-interface inherits all the abstract methods and constants of its super-interface, and may define new astract methods and constants
- interface can extend more than one interface at a time

## methods overriding (polymorphism)
- when a class defines a method using the same name, return type, and by the number, type, and position of its arguments as a method in its superclass, the method in the class overrides the method in the superclass
- if a method is invoked for an object of the class, it's the new definition of the method that is called, and not the superclass's old definition
- an object's ability to decide what method to apply to itself, depending on where it is in the inheritance hierarchy, is usually called polymorphism

### method overloading
Defining methods with the same name and different argument or return types is called method overloading

In java, a method is distinguished by its method signature - its name, return type, and by the number, type, and position of its arguments.

## Data hiding and encapsulation
We can hide the data within the class and make it available only through the methods

This can help in maintaining the consistency of the data for an object, that means the state of an object.

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

## Java modifiers
access modifier means that it is used to set the access level for classes, attributes, methods and constructors.

### Access modifiers:
for classes:
- public - the class is accessible by any other class
- default - the class is only accessible by classes in the same package.

for attributes, methods and constructors:
- public - the code is accessible for all classes
- private - the code is only accessible within the declared class
- default - the code is only accessible in the same package
- protected - the code is accessible in the same package and subclasses

### Non-access modifiers:
for classes:
- final - the class cannot be inherited by other classes
- abstract - the class cannot be used to create objects

for attributes and methods:
- final - attributes and methods cannot be overridden/modified
- static - attributes and methods belongs to the class, rather than an object
- abstract - can only be used in an abstract class, and can only be used on methods
- transient - attributes and methods are skipped when serializing the object containing them
- synchronized - methods can only be accessed by one thread at a time
- volatitle - the value of an attribute is not cached thread-locally, and is always read from the "main memory"

## Encapsulation
The meaning of Encapsulation, is to make sure that "sensitive" data is hidden from users. To achieve this, you must:
- declare class variables/attributes as private
- provide public get and set methods to access and update the value of a private variable

``` java
public class Person {
  private String name; // private = restricted access

  // Getter
  public String getName() {
    return name;
  }

  // Setter
  public void setName(String newName) {
    this.name = newName;
  }
}
```

**Why encapsulation:**
- Better control of class attributes and methods
- Class attributes can be made read-only (if you only use the get method), or write-only (if you only use the set method)
- Flexible: the programmer can change one part of the code without affecting other parts
- Increased security of data

## Java packages & API
A package in Java is used to group related classes.
We use packages to avoid name conflicts, and to write a better maintainable code.

Packages are divided into two categories:
- Built-in Packages (packages from the Java API)
- User-defined Packages (create your own packages)

### Built-in packages

**Import a class:**
``` java
import java.util.Scanner;

class MyClass {
  public static void main(String[] args) {
    Scanner myObj = new Scanner(System.in);
    System.out.println("Enter username");

    String userName = myObj.nextLine();
    System.out.println("Username is: " + userName);
  }
}
```

**Import a package:**
``` java
import java.util.*;
```

### user-defined packages
``` java
package mypack;
class MyPackageClass {
  public static void main(String[] args) {
    System.out.println("This is my package!");
  }
}
```

## Java inheritance (subclass and superclass)
In Java, it is possible to inherit attributes and methods from one class to another. We group the "inheritance concept" into two categories:
- subclass (child) - the class that inherits from another class
- superclass (parent) - the class being inherited from

To inherit from a class, use the extends keyword.
If you don't want other classes to inherit from a class, use the final keyword

``` java
class Vehicle {
  protected String brand = "Ford";        // Vehicle attribute
  public void honk() {                    // Vehicle method
    System.out.println("Tuut, tuut!");
  }
}

class Car extends Vehicle {
  private String modelName = "Mustang";    // Car attribute
  public static void main(String[] args) {

    // Create a myCar object
    Car myCar = new Car();

    // Call the honk() method (from the Vehicle class) on the myCar object
    myCar.honk();

    // Display the value of the brand attribute (from the Vehicle class) and the value of the modelName from the Car class
    System.out.println(myCar.brand + " " + myCar.modelName);
  }
}
```

## Java polymorphism
Inheritance lets us inherit attributes and methods from another class. Polymorphism uses those methods to perform different tasks. This allows us to perform a single action in different ways.

``` java
class Animal {
  public void animalSound() {
    System.out.println("The animal makes a sound");
  }
}

class Pig extends Animal {
  public void animalSound() {
    System.out.println("The pig says: wee wee");
  }
}

class Dog extends Animal {
  public void animalSound() {
    System.out.println("The dog says: bow wow");
  }
}

class Main {
  public static void main(String[] args) {
    Animal myAnimal = new Animal();  // Create a Animal object
    Animal myPig = new Pig();  // Create a Pig object
    Animal myDog = new Dog();  // Create a Dog object
    myAnimal.animalSound();
    myPig.animalSound();
    myDog.animalSound();
  }
}
```

## Java enums
An enum is a special "class" that represents a group of constants (unchangeable variables, like final variables).

``` java
public class Main {
  enum Level {
    LOW,
    MEDIUM,
    HIGH
  }

  public static void main(String[] args) {
    Level myVar = Level.MEDIUM; 
    System.out.println(myVar);
  }
}
```

## Java User Input
The Scanner class is used to get user input, and it is found in the java.util package.
``` java
import java.util.Scanner;  // Import the Scanner class

class Main {
  public static void main(String[] args) {
    Scanner myObj = new Scanner(System.in);  // Create a Scanner object
    System.out.println("Enter username");

    String userName = myObj.nextLine();  // Read user input
    System.out.println("Username is: " + userName);  // Output user input
  }
}
```

## Java ArrayList
The ArrayList class is a resizable array, which can be found in the java.util package.

The difference between a built-in array and an ArrayList in Java, is that the size of an array cannot be modified (if you want to add or remove elements to/from an array, you have to create a new one). While elements can be added and removed from an ArrayList whenever you want.

**add items**
``` java
import java.util.ArrayList;

public class Main {
  public static void main(String[] args) {
    ArrayList<String> cars = new ArrayList<String>();
    cars.add("Volvo");
    cars.add("BMW");
    cars.add("Ford");
    cars.add("Mazda");
    System.out.println(cars);
  }
}
```

**access an item**
``` java
cars.get(0);
```

**change an item**
``` java
cars.set(0, "Opel");
```

**remove an item**
``` java
cars.remove(0);
```

**remove all elements in the list**
``` java
cars.clear();
```

**arraylist size**
``` java
cars.size();
```

**loop through an arraylist**
``` java
public class Main {
  public static void main(String[] args) {
    ArrayList<String> cars = new ArrayList<String>();
    cars.add("Volvo");
    cars.add("BMW");
    cars.add("Ford");
    cars.add("Mazda");
    for (int i = 0; i < cars.size(); i++) {
      System.out.println(cars.get(i));
    }
    /*
    for (String i : cars) {
      System.out.println(i);
    }
    */
  }
}
```

**sort an arraylist**
``` java
import java.util.ArrayList;
import java.util.Collections;  // Import the Collections class

public class Main {
  public static void main(String[] args) {
    ArrayList<String> cars = new ArrayList<String>();
    cars.add("Volvo");
    cars.add("BMW");
    cars.add("Ford");
    cars.add("Mazda");
    Collections.sort(cars);  // Sort cars
    for (String i : cars) {
      System.out.println(i);
    }
  }
}
```

## Java LinkedList
**The LinkedList class is almost identical to the ArrayList.**
The LinkedList stores its items in "containers." The list has a link to the first container and each container has a link to the next container in the list. To add an element to the list, the element is placed into a new container and that container is linked to one of the other containers in the list.

``` java
import java.util.LinkedList;

public class Main {
  public static void main(String[] args) {
    LinkedList<String> cars = new LinkedList<String>();
    cars.add("Volvo");
    cars.add("BMW");
    cars.add("Ford");
    
    // Use addFirst() to add the item to the beginning
    cars.addFirst("Mazda");
    System.out.println(cars);
    
    // Use addLast() to add the item to the end
    cars.addLast("Honda");
    System.out.println(cars);
    
    // Use removeFirst() remove the first item from the list
    cars.removeFirst();
    System.out.println(cars);
    
    // Use removeLast() remove the last item from the list
    cars.removeLast();
    System.out.println(cars);
    
    // Use getFirst() to display the first item in the list
    System.out.println(cars.getFirst());
    
    // Use getLast() to display the last item in the list
    System.out.println(cars.getLast());
  }
}
```

## Java HashMap
**add items**
``` java
// Import the HashMap class
import java.util.HashMap;

public class Main {
  public static void main(String[] args) {
    // Create a HashMap object called capitalCities
    HashMap<String, String> capitalCities = new HashMap<String, String>();

    // Add keys and values (Country, City)
    capitalCities.put("England", "London");
    capitalCities.put("Germany", "Berlin");
    capitalCities.put("Norway", "Oslo");
    capitalCities.put("USA", "Washington DC");
    System.out.println(capitalCities);
  }
}
```

**access an item**
``` java
capitalCities.get("England");
```

**remove an item**
``` java
capitalCities.remove("England");
```

**remove all items**
``` java
capitalCities.clear();
```

**hashmap size**
``` java
capitalCities.size();
```

**loop through a hashmap**
``` java
// Print keys
for (String i : capitalCities.keySet()) {
  System.out.println(i);
}
```

``` java
// Print values
for (String i : capitalCities.values()) {
  System.out.println(i);
}
```

``` java
// Print keys and values
for (String i : capitalCities.keySet()) {
  System.out.println("key: " + i + " value: " + capitalCities.get(i));
}
```

## Java HashSet
A HashSet is a collection of items where every item is unique, and it is found in the java.util package

**add items**
``` java
// Import the HashSet class
import java.util.HashSet;

public class Main {
  public static void main(String[] args) {
    HashSet<String> cars = new HashSet<String>();
    cars.add("Volvo");
    cars.add("BMW");
    cars.add("Ford");
    cars.add("BMW");
    cars.add("Mazda");
    System.out.println(cars);
  }
}
```

**check if an item exists**
``` java
cars.contains("Mazda");
```

**remove an item**
``` java
cars.remove("Volvo");
```

**remove all items**
``` java
cars.clear();
```

**hashset size**
``` java
cars.size();
```

**loop through a hashset**
``` java
for (String i : cars) {
  System.out.println(i);
}
```

## Java iterator
``` java
import java.util.ArrayList;
import java.util.Iterator;

public class Main {
  public static void main(String[] args) {
  
    // Make a collection
    ArrayList<String> cars = new ArrayList<String>();
    cars.add("Volvo");
    cars.add("BMW");
    cars.add("Ford");
    cars.add("Mazda");
  
    // Get the iterator
    Iterator<String> it = cars.iterator();
  
    // Print the first item
    while(it.hasNext()) {
  		System.out.println(it.next());
	}
  }
}
```

## Java exception
``` java
// this is very similar to python try..except block
public class Main {
  public static void main(String[] args) {
    try {
      int[] myNumbers = {1, 2, 3};
      System.out.println(myNumbers[10]);
    } catch (Exception e) {
      System.out.println("Something went wrong.");
    } finally {
      System.out.println("The 'try catch' is finished.");
    }
  }
}
```
The throw keyword:
``` java
// this is similar to raise statement in python
public class Main {
  static void checkAge(int age) {
    if (age < 18) {
      throw new ArithmeticException("Access denied - You must be at least 18 years old.");
    }
    else {
      System.out.println("Access granted - You are old enough!");
    }
  }

  public static void main(String[] args) {
    checkAge(15); // Set age to 15 (which is below 18...)
  }
}
```

## Java lambda
``` java
import java.util.ArrayList;

public class Main {
  public static void main(String[] args) {
    ArrayList<Integer> numbers = new ArrayList<Integer>();
    numbers.add(5);
    numbers.add(9);
    numbers.add(8);
    numbers.add(1);
    numbers.forEach( (n) -> { System.out.println(n); } );
  }
}
```

## Java interface
``` java
// interface can achieve abstraction in java
// An interface is a completely abstract class that is used to group related methods with empty bodies

// Interface
interface Animal {
  public void animalSound(); // interface method (does not have a body)
  public void sleep(); // interface method (does not have a body)
}

// Pig "implements" the Animal interface
class Pig implements Animal {
  public void animalSound() {
    // The body of animalSound() is provided here
    System.out.println("The pig says: wee wee");
  }
  public void sleep() {
    // The body of sleep() is provided here
    System.out.println("Zzz");
  }
}

class Main {
  public static void main(String[] args) {
    Pig myPig = new Pig();  // Create a Pig object
    myPig.animalSound();
    myPig.sleep();
  }
}
```
- Like abstract classes, interfaces cannot be used to create objects
- Interface methods do not have a body - the body is provided by the "implement" class
- On implementation of an interface, you must override all of its methods
- An interface cannot contain a constructor


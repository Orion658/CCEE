**[ ] JAVA CCEE Syllabus**

### Introduction to Java:

Java is a high-level, object-oriented programming language developed by Sun Microsystems (now owned by Oracle Corporation) in 1995. It was designed with the goal of being platform-independent, meaning that Java programs can run on any device or operating system that has a Java Virtual Machine (JVM) installed. This "write once, run anywhere" capability is one of Java's most prominent features.

### Features of Java:

1.  **Platform Independence**: Java achieves platform independence by compiling source code into an intermediate bytecode format, which can run on any system with a Java Virtual Machine (JVM). This makes Java highly portable.
2.  **Object-Oriented**: Java is an object-oriented programming language, which means it follows the principles of encapsulation, inheritance, and polymorphism. Everything in Java is an object, which allows for modular and reusable code.
3.  **Simple and Familiar Syntax**: Java syntax is similar to that of C and C++, making it easy for programmers who are familiar with these languages to transition to Java.
4.  **Robust and Secure**: Java's strong type-checking mechanism, exception handling, and memory management make it a robust language. Additionally, Java's security features, such as the bytecode verifier, help protect systems from malicious code.
5.  **Multithreading and Concurrency**: Java supports multithreading, allowing multiple threads of execution to run concurrently within a single program. This makes it well-suited for developing multi-threaded applications.
6.  **Dynamic and Extensible**: Java supports dynamic loading of classes, which allows new code to be loaded and executed dynamically at runtime. This feature enables Java applications to be extensible and flexible.
7.  **Rich Standard Library**: Java comes with a vast standard library, providing pre-built classes and methods for common programming tasks, such as I/O operations, networking, data structures, and more.

### JVM Architecture:

The Java Virtual Machine (JVM) is an essential component of the Java platform. It is responsible for executing Java bytecode and providing runtime services. The JVM architecture consists of three main components:

1.  **Class Loader Subsystem**: This subsystem is responsible for loading Java classes into memory as they are referenced by a Java program. The class loader loads classes from the file system, network, or other sources and then passes them to the runtime area.
2.  **Runtime Data Area**: The runtime data area is where the JVM stores data during program execution. It consists of several components:
    1.  **Method Area**: This area stores class metadata, static variables, and method bytecode.
    2.  **Heap**: The heap is where objects created by the program are allocated. It is shared among all threads and is managed by the garbage collector.
    3.  **Java Stack**: Each thread in a Java program has its own Java stack, which stores method invocations and local variables.
    4.  **PC Register**: The program counter register keeps track of the currently executing instruction.
    5.  **Native Method Stack**: This stack is used for executing native methods, which are methods written in languages other than Java.
3.  **Execution Engine**: The execution engine is responsible for executing Java bytecode. It consists of two components:
    1.  **Interpreter**: The interpreter reads bytecode instructions and executes them one by one.
    2.  **Just-In-Time (JIT) Compiler**: The JIT compiler compiles frequently executed bytecode into native machine code for improved performance.

### 

### JDK (Java Development Kit) and Its Usage:

The Java Development Kit (JDK) is a set of tools that developers use to develop Java applications. It includes the Java Runtime Environment (JRE), compilers, debuggers, and other tools needed for Java development. Here's a breakdown of its components and usage:

1.  **Java Compiler (javac)**: The JDK includes the Java compiler (`javac`), which is used to compile Java source code (.java files) into bytecode (.class files). You can invoke the compiler from the command line or integrate it into your development environment.
2.  **Java Runtime Environment (JRE)**: The JRE, also included in the JDK, is needed to run Java applications. It consists of the Java Virtual Machine (JVM) and class libraries. When you install the JDK, it also installs the JRE.
3.  **Java Development Tools**: The JDK provides various development tools, such as:
    1.  **Java Debugger (jdb)**: Used for debugging Java programs.
    2.  **Java Archive Tool (jar)**: Used for creating and managing Java archive (JAR) files, which are collections of Java classes and resources.
    3.  **Java Documentation Tool (javadoc)**: Used for generating API documentation from source code comments.
4.  **JavaFX and Other Libraries**: The JDK includes additional libraries like JavaFX for building rich client applications, as well as other standard libraries for tasks such as networking, I/O, and database access.

### Structure of a Java Class:

A Java class is the basic building block of Java programs. It encapsulates data and methods (functions) that operate on that data. Here's the general structure of a Java class:

```java
public class MyClass {
    // Fields (variables)
    private int myField1;
    private String myField2;

    // Constructors
    public MyClass() {
        // Constructor code
    }

    // Methods
    public void myMethod1() {
        // Method code
    }

    public int myMethod2(int param) {
        // Method code with a parameter and return value
        return param * 2;
    }

    // Main method (entry point of the program)
    public static void main(String[] args) {
        // Main method code
    }
}
```

Let's break down each part:

-   **Class Declaration**: The `public class MyClass { ... }` line declares a class named `MyClass`. In Java, a source file can contain only one public class, and the filename must match the class name.
-   **Fields (Variables)**: Fields represent the state of the object. They define the data the class holds. In the example, `myField1` and `myField2` are private fields.
-   **Constructors**: Constructors are special methods used for initializing objects. They have the same name as the class and no return type. In the example, `MyClass()` is a constructor.
-   **Methods**: Methods define the behavior of the class. They perform actions and can return values. In the example, `myMethod1()` and `myMethod2(int param)` are methods.
-   **Main Method**: The `main` method is the entry point of a Java program. It's where the program starts executing. It must have the signature `public static void main(String[] args)`.

### Primitive data types:

1.  **byte**:
    1.  Size: 8 bits
    2.  Range: -128 to 127
    3.  Default value: 0
    4.  Used for: storing small integral values
2.  **short**:
    1.  Size: 16 bits
    2.  Range: -32,768 to 32,767
    3.  Default value: 0
    4.  Used for: storing small integral values
3.  **int**:
    1.  Size: 32 bits
    2.  Range: -2\^31 to 2\^31-1
    3.  Default value: 0
    4.  Used for: storing integral values
4.  **long**:
    1.  Size: 64 bits
    2.  Range: -2\^63 to 2\^63-1
    3.  Default value: 0L
    4.  Used for: storing large integral values
5.  **float**:
    1.  Size: 32 bits
    2.  Range: Approximately ±3.40282347E+38F
    3.  Default value: 0.0f
    4.  Used for: storing floating-point numbers with single precision
6.  **double**:
    1.  Size: 64 bits
    2.  Range: Approximately ±1.79769313486231570E+308
    3.  Default value: 0.0d
    4.  Used for: storing floating-point numbers with double precision
7.  **char**:
    1.  Size: 16 bits
    2.  Range: Unicode characters (0 to 65,535)
    3.  Default value: '\\u0000'
    4.  Used for: storing single characters
8.  **boolean**:
    1.  Size: Not precisely defined
    2.  Range: true or false
    3.  Default value: false
    4.  Used for: storing boolean values (true or false)

### Java Tokens:

Java tokens are the smallest elements of a Java program. They include identifiers, keywords, operators, separators, and literals.

1.  **Identifiers**: Identifiers are names given to variables, methods, classes, etc. They must start with a letter, dollar sign (\$), or underscore (_) and can be followed by letters, digits, underscores, or dollar signs. Example: `myVariable`, `calculateTotal`.
2.  **Keywords**: Keywords are reserved words that have special meanings in Java. They cannot be used as identifiers. Examples: `public`, `class`, `if`, `while`, `int`, `boolean`, etc.
3.  **Operators**: Operators are symbols used to perform operations on operands. Examples: `+`, `-`, `*`, `/` (arithmetic operators), `==`, `!=`, `>`, `<` (relational operators), `&&`, `||`, `!` (logical operators), `=`, `+=`, `-=` (assignment operators), etc.
4.  **Separators**: Separators are symbols used to separate tokens in a Java program. Examples: `;` (semicolon), `,` (comma), `.` (dot), `{}`, `()` (brackets), `[]` (square brackets), etc.
5.  **Literals**: Literals represent constant values in Java. Examples: `123` (integer literal), `3.14` (floating-point literal), `'A'` (character literal), `"Hello"` (string literal), `true` or `false` (boolean literals), etc.

Now, let's move on to declaring variables and methods:

### Declaring Variables:

In Java, variables must be declared before they can be used. The declaration consists of the variable's data type followed by its name.

```java
// Syntax: dataType variableName;
int age; // Declaration of an integer variable named age
double salary; // Declaration of a double variable named salary
boolean isStudent; // Declaration of a boolean variable named isStudent
```

Optionally, you can also initialize variables when declaring them:

```java
// Syntax: dataType variableName = initialValue;
int count = 10; // Declaration and initialization of an integer variable named count with initial value 10
double pi = 3.14; // Declaration and initialization of a double variable named pi with initial value 3.14
String name = "John"; // Declaration and initialization of a string variable named name with initial value "John"
```

### Declaring Methods:

Methods in Java are blocks of code that perform a specific task and may return a value. A method declaration consists of several components:

```java
// Syntax: returnType methodName(parameterList) {
//            // Method body
//          }

// Example:
public int add(int a, int b) {
    return a + b; // Method to add two integers and return the result
}
```

-   **returnType**: Specifies the type of value the method returns. Use `void` if the method doesn't return any value.
-   **methodName**: Name of the method.
-   **parameterList**: List of parameters (if any) that the method accepts. Parameters are variables that hold the values passed to the method.
-   **Method body**: Contains the code that defines what the method does.

### Data Type Compatibility:

In Java, data type compatibility refers to how different data types can interact with each other in expressions and assignments. Java has rules for implicit and explicit type conversions, which ensure type safety.

1.  **Implicit Type Conversion (Widening Conversion)**: Automatic conversion of a smaller data type to a larger data type. It occurs when no data loss will happen. For example, converting an `int` to a `double`:

```java
int intValue = 10;
double doubleValue = intValue; // Implicit conversion from int to double
```

1.  **Explicit Type Conversion (Narrowing Conversion)**: Manual conversion of a larger data type to a smaller data type. It requires explicit casting and may result in data loss. For example, converting a `double` to an `int`:

```java
double doubleValue = 10.5;
int intValue = (int) doubleValue; // Explicit conversion from double to int
```

### Operators:

Operators in Java are symbols that perform operations on operands. Java supports various types of operators:

1.  **Arithmetic Operators**: Perform mathematical operations such as addition, subtraction, multiplication, division, and modulus.
2.  **Relational Operators**: Compare two values and return a boolean result (true or false) based on the comparison.
3.  **Logical Operators**: Perform logical operations such as AND (`&&`), OR (`||`), and NOT (`!`).
4.  **Assignment Operators**: Assign values to variables, combined with arithmetic or bitwise operations.
5.  **Increment and Decrement Operators**: Increase or decrease the value of a variable by one.
6.  **Conditional (Ternary) Operator**: A shorthand way of writing an if-else statement.
7.  **Bitwise Operators**: Perform bitwise operations on binary representations of integer values.

### Control Statements:

Control statements in Java determine the flow of execution in a program. They include conditional statements and looping statements:

1.  **Conditional Statements**:
    1.  **if**: Executes a block of code if a specified condition is true.
    2.  **if-else**: Executes one block of code if a condition is true and another block if it's false.
    3.  **else-if**: Checks multiple conditions sequentially.
    4.  **switch**: Evaluates an expression and executes code based on matching cases.
2.  **Looping Statements**:
    1.  **for**: Executes a block of code repeatedly until a specified condition is false.
    2.  **while**: Executes a block of code as long as a specified condition is true.
    3.  **do-while**: Executes a block of code once, and then repeats the execution as long as a specified condition is true (similar to while loop, but ensures that the code block is executed at least once).

### 1-D Arrays:

A one-dimensional array in Java is a collection of elements of the same data type arranged in a linear sequence.

#### Method 1: Using Array Initialization Syntax:

You can initialize an array with predefined values at the time of declaration.

```java
// Initializing array with predefined values
int[] numbers = {1, 2, 3, 4, 5};
```

#### Method 2: Using the `new` Operator:

You can create an array without initializing its values immediately.

```java
// Creating an array without initializing values
int[] numbers = new int[5]; // Array with size 5
```

### Multidimensional Arrays:

A multidimensional array in Java is an array of arrays. It can be visualized as a table of elements arranged in rows and columns.

#### Method 1: Using Array Initialization Syntax:

You can initialize a multidimensional array with predefined values at the time of declaration.

```java
// Initializing a 2-D array with predefined values
int[][] matrix = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};
```

#### Method 2: Using Nested Array Initialization Syntax:

You can create a multidimensional array by nesting arrays within arrays.

```java
// Creating a 2-D array using nested arrays
int[][] matrix = new int[3][3]; // Array with size 3x3
```

#### Method 3: Initializing Each Row Separately:

You can initialize each row of a 2-D array separately.

```java
// Creating a 2-D array by initializing each row separately
int[][] matrix = new int[3][];
matrix[0] = new int[]{1, 2, 3};
matrix[1] = new int[]{4, 5, 6};
matrix[2] = new int[]{7, 8, 9};
```

### 

### Introduction to OOP:

Object-Oriented Programming (OOP) is a programming paradigm based on the concept of "objects", which can contain data in the form of fields (attributes or properties) and code in the form of procedures (methods or functions). OOP aims to organize software design around data and the operations that can be performed on that data.

### Classes and Objects:

-   **Class**: A class is a blueprint or template for creating objects. It defines the attributes (data fields) and methods (functions) that the objects of the class will have.

```java
public class Car {
    // Attributes (data fields)
    String color;
    int speed;
    
    // Methods
    void drive() {
        // Code to drive the car
    }
    
    void brake() {
        // Code to apply brakes
    }
}
```

-   **Object**: An object is an instance of a class. It represents a real-world entity with its own state (attributes) and behavior (methods).

```java
public class Main {
    public static void main(String[] args) {
        // Creating objects of the Car class
        Car myCar = new Car();
        Car yourCar = new Car();
        
        // Accessing object attributes and methods
        myCar.color = "Red";
        myCar.speed = 60;
        myCar.drive();
        
        yourCar.color = "Blue";
        yourCar.speed = 70;
        yourCar.brake();
    }
}
```

### OOP Principles:

1.  **Encapsulation**: Encapsulation is the bundling of data (attributes) and methods that operate on that data into a single unit or class. It hides the internal state of an object and only exposes the necessary methods to interact with it, providing data integrity and security.
2.  **Abstraction**: Abstraction is the process of hiding the implementation details and showing only the essential features of an object. It allows us to focus on what an object does rather than how it does it, simplifying complex systems and improving maintainability.
3.  **Inheritance**: Inheritance is the mechanism by which a class can inherit properties and behavior (attributes and methods) from another class. It promotes code reusability and allows for hierarchical relationships between classes.
4.  **Polymorphism**: Polymorphism allows objects of different classes to be treated as objects of a common superclass. It enables a single interface to represent multiple types, allowing for flexibility and extensibility in software design.

### 

### Static Variables and Methods:

In Java, static variables and methods belong to the class rather than individual instances (objects) of the class. They are shared among all instances of the class and can be accessed directly using the class name.

#### Static Variables:

```java
public class MyClass {
    static int count; // Static variable
    
    // Constructor
    public MyClass() {
        count++; // Increment count each time a new object is created
    }
}
```

#### Static Methods:

```java
public class MathUtils {
    public static int add(int a, int b) {
        return a + b;
    }
}
```

### Accessing Static Variables and Methods of Different Class:

Static variables and methods can be accessed directly using the class name without creating an instance of the class.

```java
public class Main {
    public static void main(String[] args) {
        // Accessing static variable
        MyClass.count = 10;
        
        // Accessing static method
        int sum = MathUtils.add(5, 3);
    }
}
```

### Introduction to Reference Data Types:

Reference data types in Java are types that hold references (memory addresses) to objects rather than the actual data itself. Examples include classes, arrays, and interfaces.

### Reference Variables and Methods:

Reference variables are variables that hold references to objects of reference data types. You can use reference variables to access methods and properties of objects.

```java
public class Student {
    String name;
    int age;
    
    public void displayInfo() {
        System.out.println("Name: " + name + ", Age: " + age);
    }
}

public class Main {
    public static void main(String[] args) {
        Student student1 = new Student();
        student1.name = "John";
        student1.age = 20;
        
        student1.displayInfo(); // Calling method using reference variable
    }
}
```

### Difference Between Reference Data Types and Primitive Data Types:

-   **Reference Data Types**: Reference data types store references to objects in memory. They include classes, arrays, and interfaces.
-   **Primitive Data Types**: Primitive data types store actual values. They include int, double, boolean, etc.

### Difference Between Reference Variable and Static Variable:

-   **Reference Variable**: Reference variables hold references to objects of reference data types. They are declared using the class name followed by the variable name.
-   **Static Variable**: Static variables belong to the class rather than individual instances. They are declared using the `static` keyword and are shared among all instances of the class.

### 

### 

### Constructors and Initializing Reference Variables Using Constructors:

Constructors are special methods used to initialize objects of a class. They have the same name as the class and do not have a return type. You can use constructors to initialize reference variables with specific values.

```java
public class Person {
    String name;
    int age;
    
    // Constructor
    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
}

public class Main {
    public static void main(String[] args) {
        // Initializing reference variable using constructor
        Person person1 = new Person("John", 25);
    }
}
```

### Pass by Value vs. Pass by Reference:

Java is strictly pass by value. When you pass a primitive type to a method, a copy of the value is passed. When you pass a reference type (object or array) to a method, a copy of the reference (memory address) is passed, not the actual object.

```java
public void modifyValue(int value) {
    value = 10; // Changes only the local copy of 'value'
}

public void modifyArray(int[] arr) {
    arr[0] = 10; // Changes the original array
}
```

### Re-assigning a Reference Variable:

You can re-assign a reference variable to point to a different object or null.

```java
Person person1 = new Person("John", 25);
Person person2 = new Person("Alice", 30);

person1 = person2; // Re-assigning 'person1' to point to the same object as 'person2'
person1 = null; // Re-assigning 'person1' to null
```

### Passing Reference Variables to a Method:

When you pass a reference variable to a method, you are passing the reference (memory address) to the object. Any changes made to the object inside the method will affect the original object.

```java
public void modifyPerson(Person person) {
    person.age = 35; // Modifies the original object
}
```

### Initializing Reference Variables of Different Classes:

You can initialize reference variables of different classes using constructors or by assigning them to objects created using constructors.

```java
// Initializing reference variable using constructor
Person = new Person("John", 25);

// Initializing reference variable by assigning it to an object created using constructor
Employee employee = new Employee("Alice", 30, "Manager");
```

### Heap Memory and Stack Memory:

-   **Heap Memory**: Heap memory is used for storing objects and is shared among all threads. Objects created using the `new` keyword are stored in the heap memory.
-   **Stack Memory**: Stack memory is used for storing method invocations and local variables. Each thread has its own stack memory. Method calls and local variables are stored in stack memory.

### Inheritance:

Inheritance is a mechanism in object-oriented programming that allows a class (subclass or derived class) to inherit properties and behavior (attributes and methods) from another class (superclass or base class).

#### Single Inheritance:

In single inheritance, a subclass inherits from only one superclass.

```java
// Superclass
class Animal {
    void eat() {
        System.out.println("Animal is eating");
    }
}

// Subclass inheriting from Animal
class Dog extends Animal {
    void bark() {
        System.out.println("Dog is barking");
    }
}
```

#### Multilevel Inheritance:

In multilevel inheritance, a subclass inherits from another subclass, forming a chain of inheritance.

```java
// Superclass
class Animal {
    void eat() {
        System.out.println("Animal is eating");
    }
}

// Subclass inheriting from Animal
class Dog extends Animal {
    void bark() {
        System.out.println("Dog is barking");
    }
}

// Subclass inheriting from Dog
class Labrador extends Dog {
    void swim() {
        System.out.println("Labrador is swimming");
    }
}
```

#### Hierarchical Inheritance:

In hierarchical inheritance, multiple subclasses inherit from the same superclass.

```java
// Superclass
class Animal {
    void eat() {
        System.out.println("Animal is eating");
    }
}

// Subclass inheriting from Animal
class Dog extends Animal {
    void bark() {
        System.out.println("Dog is barking");
    }
}

// Another subclass inheriting from Animal
class Cat extends Animal {
    void meow() {
        System.out.println("Cat is meowing");
    }
}
```

### Association, Aggregation, and Composition:

These are different types of relationships between classes:

1.  **Association**: Association represents a relationship where one class is related to another class, but there is no ownership. It can be one-to-one, one-to-many, or many-to-many.
2.  **Aggregation**: Aggregation is a type of association where one class owns or contains another class, but the contained class can exist independently. It's a "has-a" relationship.
3.  **Composition**: Composition is a stronger form of aggregation where the lifetime of the contained class is dependent on the lifetime of the container class. It's a "part-of" relationship.

```java
// Association: Car has an Engine
class Engine {
    // Engine properties and methods
}

class Car {
    Engine engine; // Association
}

// Aggregation: Department has Employees
class Employee {
    // Employee properties and methods
}

class Department {
    List<Employee> employees; // Aggregation
}

// Composition: Car has Wheels
class Wheel {
    // Wheel properties and methods
}

class Car {
    List<Wheel> wheels; // Composition
}
```

Understanding inheritance and the different types of class relationships (association, aggregation, composition) is essential for designing and modeling complex systems in object-oriented programming. These concepts facilitate code reuse, modularity, and maintainability in software development.

### Polymorphism:

Polymorphism allows objects to be treated as instances of their parent class, enabling methods to be called on objects of different types through a common interface.

#### Compile-Time Polymorphism (Method Overloading):

Method overloading allows a class to have multiple methods with the same name but different parameters. The compiler determines which method to call based on the number and types of arguments.

```java
class Calculator {
    int add(int a, int b) {
        return a + b;
    }

    double add(double a, double b) {
        return a + b;
    }
}
```

#### Runtime Polymorphism (Method Overriding):

Method overriding allows a subclass to provide a specific implementation of a method that is already provided by its superclass. It allows the subclass to provide its own implementation of the method.

```java
class Animal {
    void sound() {
        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}
```

### Rules of Overriding and Overloading:

#### Rules of Method Overriding:

1.  The method in the subclass must have the same signature as the method in the superclass.
2.  The method in the subclass must have the same return type as the method in the superclass or its subtype (covariant return types are allowed in Java 5 and later).
3.  The method in the subclass must not have a more restrictive access modifier than the method in the superclass (e.g., if the method in the superclass is `protected`, it can't be `private` in the subclass).
4.  The method in the subclass may throw the same, fewer, or no exceptions as the method in the superclass (or its subtype).

#### Rules of Method Overloading:

1.  The methods must have the same name.
2.  The methods must have different parameter lists (number or type of parameters).

### Usage of `super` and `this` Keyword:

-   **super**: The `super` keyword is used to refer to the superclass of the current object or to invoke superclass constructors and methods.
-   **this**: The `this` keyword is used to refer to the current object or to call other constructors of the same class.

```java
class Animal {
    String name;

    Animal(String name) {
        this.name = name; // 'this' keyword refers to the current object
    }
}

class Dog extends Animal {
    Dog(String name) {
        super(name); // 'super' keyword invokes superclass constructor
    }
}
```

### Upcasting & Downcasting of a Reference Variable:

#### Upcasting:

Upcasting refers to the process of casting a reference variable to a superclass type. It allows you to treat an object of a subclass as an object of its superclass.

```java
class Animal { }

class Dog extends Animal { }

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
        Animal animal = dog; // Upcasting
    }
}
```

#### Downcasting:

Downcasting refers to the process of casting a reference variable to a subclass type. It allows you to treat an object of a superclass as an object of its subclass. It must be done explicitly and may result in a `ClassCastException` if the object is not actually an instance of the subclass.

```java
class Animal { }

class Dog extends Animal { }

public class Main {
    public static void main(String[] args) {
        Animal animal = new Dog();
        Dog dog = (Dog) animal; // Downcasting
    }
}
```

### Abstract Class and Abstract Methods:

#### Abstract Class:

An abstract class is a class that cannot be instantiated directly and may contain abstract methods (methods without a body) as well as concrete methods.

```java
abstract class Shape {
    abstract void draw(); // Abstract method
}

class Circle extends Shape {
    void draw() {
        System.out.println("Drawing a circle");
    }
}
```

### Interface (Implementing Multiple Interfaces):

#### Interface:

An interface in Java is a reference type similar to a class but can only contain abstract methods, default methods, static methods, and constant variables. A class implements an interface, thereby inheriting the abstract methods of the interface.

```java
interface Animal {
    void sound();
}

interface Mammal {
    void eat();
}

class Dog implements Animal, Mammal {
    public void sound() {
        System.out.println("Barking");
    }
    public void eat() {
        System.out.println("Eating");
    }
}
```

A class can implement multiple interfaces by separating them with commas.

```java
class MyClass implements Interface1, Interface2, Interface3 {
    // Class implementation
}
```

### Final Variables, Final Methods, and Final Classes:

#### Final Variables:

A final variable is a variable whose value cannot be changed once assigned. It must be initialized when declared or in the constructor.

```java
class MyClass {
    final int VALUE = 10; // Final variable
}
```

#### Final Methods:

A final method is a method that cannot be overridden by subclasses. It prevents subclasses from changing the behavior of the method.

```java
class Parent {
    final void display() { // Final method
        System.out.println("This is a final method");
    }
}
```

#### Final Classes:

A final class is a class that cannot be subclassed. It prevents other classes from extending it.

```java
final class MyClass { // Final class
    // Class implementation
}
```

### Functional Interface:

A functional interface is an interface that contains only one abstract method. It can have multiple default methods or static methods.

```java
@FunctionalInterface
interface MyFunctionalInterface {
    void myMethod(); // Abstract method

    default void myDefaultMethod() {
        // Default method implementation
    }

    static void myStaticMethod() {
        // Static method implementation
    }
}
```

### New Interface Features (Java 8 & 11):

#### Java 8:

Java 8 introduced several new features for interfaces, including default methods, static methods, and functional interfaces.

```java
interface MyInterface {
    default void defaultMethod() {
        // Default method implementation
    }

    static void staticMethod() {
        // Static method implementation
    }
}
```

#### Java 11:

Java 11 introduced private methods in interfaces, allowing interface methods to be encapsulated.

```java
interface MyInterface {
    default void defaultMethod() {
        // Default method implementation
    }

    private void privateMethod() {
        // Private method implementation
    }
}
```

### Lambda Expression:

A lambda expression is a concise way to represent an anonymous function. It provides a clear and compact syntax for writing anonymous methods.

```java
// Syntax: (parameters) -> expression or statement block
Runnable runnable = () -> {
    System.out.println("This is a lambda expression");
};
```

### Inner Classes:

Inner classes are classes defined within another class. There are several types of inner classes:

-   Regular Inner Class
-   Method-local Inner Class
-   Anonymous Inner Class
-   Static Inner Class

```java
class Outer {
    class Inner { // Regular Inner Class
        // Class implementation
    }

    void method() {
        class LocalInner { // Method-local Inner Class
            // Class implementation
        }
    }

    Runnable runnable = new Runnable() { // Anonymous Inner Class
        public void run() {
            // Implementation of the run method
        }
    };

    static class StaticInner { // Static Inner Class
        // Class implementation
    }
}
```

### Enum:

Enums in Java have several properties that make them powerful and useful:

1.  **Constants**: Enums are a way to define a fixed set of constants. Each enum constant represents a unique value of the enum type.

```java
enum Day {
    SUNDAY, MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, SATURDAY
}
```

1.  **Instance of a Class**: Enums are implicitly final and implicitly extend `java.lang.Enum`, making them full-fledged classes. They can have fields, constructors, and methods like regular classes.

```java
enum Day {
    SUNDAY("Sun"), MONDAY("Mon"), TUESDAY("Tue");
    
    private final String abbreviation;
    
    Day(String abbreviation) {
        this.abbreviation = abbreviation;
    }
    
    public String getAbbreviation() {
        return abbreviation;
    }
}
```

1.  **Type Safety**: Enums provide type safety, ensuring that only valid enum constants can be assigned to variables of the enum type.

```java
Day today = Day.MONDAY;
```

1.  **Compile-Time Checks**: Enums are checked at compile-time, so any attempt to assign an invalid value results in a compilation error.

```java
// This will result in a compilation error
Day invalidDay = Day.INVALID;
```

1.  **Iteration**: Enums can be iterated over using the enhanced for loop.

```java
for (Day day : Day.values()) {
    System.out.println(day);
}
```

1.  **Switch Statements**: Enums are commonly used with switch statements, providing a cleaner and more readable alternative to if-else chains.

```java
switch (today) {
    case MONDAY:
        System.out.println("It's Monday");
        break;
    // Other cases...
}
```

1.  **Singleton Pattern**: Enums can be used to implement the singleton pattern, ensuring that only one instance of the enum constant exists.

```java
enum Singleton {
    INSTANCE;
}
```

1.  **Enums as Method Parameters**: Enums are commonly used as method parameters to restrict input to a predefined set of values.

```java
void processDay(Day day) {
    // Method implementation
}
```

### Access Modifiers:

Access modifiers control the accessibility of classes, variables, methods, and constructors in Java. There are four access modifiers:

1.  **Public**: The public access modifier allows unrestricted access to the class, variable, method, or constructor from any other class or package.
2.  **Private**: The private access modifier restricts access to the class, variable, method, or constructor to only within the same class.
3.  **Protected**: The protected access modifier allows access to the class, variable, method, or constructor within the same package or by subclasses, even if they are in different packages.
4.  **Default (Package-private)**: If no access modifier is specified, the default access modifier is applied. It allows access to the class, variable, method, or constructor only within the same package.

### Packages and Import Statements:

Packages are used to organize classes into namespaces. They help in avoiding naming conflicts and provide a logical structure to the codebase.

```java
package com.example.mypackage; // Package declaration

public class MyClass {
    // Class implementation
}
```

Import statements are used to make classes and packages available in the current source file.

```java
import java.util.ArrayList; // Importing a class from a package

public class Main {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>(); // Using the imported class
    }
}
```

### Static Imports:

Static imports allow static members (variables and methods) of a class to be used directly without qualifying them with the class name.

```java
import static java.lang.Math.*; // Static import

public class Main {
    public static void main(String[] args) {
        double result = sqrt(25); // Using static method without qualifying with class name
    }
}
```

### Constructor Chaining:

Constructor chaining is the process of calling one constructor from another constructor within the same class or superclass.

```java
class MyClass {
    MyClass() {
        this(10); // Constructor chaining to another constructor
    }
    
    MyClass(int value) {
        // Constructor implementation
    }
}
```

### Accessing Protected Variables and Methods Outside the Package:

Protected members can be accessed outside the package only through inheritance.

```java
package com.example.package1;

public class MyClass {
    protected int value;
    protected void myMethod() {
        // Method implementation
    }
}

package com.example.package2;

import com.example.package1.MyClass;

public class MySubClass extends MyClass {
    public void accessProtected() {
        value = 10; // Accessing protected variable
        myMethod(); // Accessing protected method
    }
}
```

In this example, `MySubClass` can access the protected members of `MyClass` because it inherits from `MyClass`. If `MySubClass` were in a different package and not a subclass of `MyClass`, it would not have access to the protected members.

### 

### Garbage Collection in Java:

Garbage collection is the process by which Java automatically reclaims memory occupied by objects that are no longer reachable or in use by the program. It helps manage memory efficiently and prevents memory leaks.

### Requesting JVM to Run Garbage Collection:

While Java provides automatic garbage collection, you can request the JVM to run garbage collection using the `System.gc()` method. However, this is just a suggestion to the JVM, and there's no guarantee that garbage collection will be performed immediately.

```java
System.gc(); // Requesting JVM to run garbage collection
```

### Making Objects Eligible for Garbage Collection:

There are several ways to make objects eligible for garbage collection:

1.  **Nulling a Reference Variable**: Assigning `null` to a reference variable removes the reference to the object, making it eligible for garbage collection.

```java
MyClass obj = new MyClass(); // Creating an object
obj = null; // Nulling the reference variable
```

1.  **Reassigning a Reference Variable**: Assigning a new object to a reference variable without any references to the previous object makes the previous object eligible for garbage collection.

```java
MyClass obj1 = new MyClass(); // Creating an object
MyClass obj2 = new MyClass(); // Creating another object
obj1 = obj2; // Reassigning the reference variable
```

1.  **Island of Isolation**: Objects that reference each other but are not referenced by any live thread become unreachable and eligible for garbage collection.

```java
MyClass obj1 = new MyClass(); // Creating an object
MyClass obj2 = new MyClass(); // Creating another object
obj1.setOtherObject(obj2); // Object 1 references Object 2
obj2.setOtherObject(obj1); // Object 2 references Object 1
obj1 = null; // Nulling the reference variable to Object 1
obj2 = null; // Nulling the reference variable to Object 2
```

### Finalize Method:

The `finalize` method is called by the garbage collector on an object before it is reclaimed. It can be overridden in a class to perform cleanup operations, but its usage is discouraged as it is unreliable and may not be called promptly or at all.

```java
class MyClass {
    // Other class members
    
    @Override
    protected void finalize() throws Throwable {
        // Cleanup operations
        super.finalize();
    }
}
```

It's important to note that while you can request garbage collection and make objects eligible for it, the decision of when and if garbage collection actually occurs is ultimately up to the JVM. Garbage collection happens in a separate thread and is influenced by various factors such as memory usage, JVM implementation, and garbage collection algorithms.

### Wrapper Classes:

Wrapper classes in Java provide a way to represent primitive data types as objects. They are used when an object is required, such as collections, generics, and dealing with APIs that work with objects rather than primitives.

#### Primitive Data Types vs. Wrapper Classes:

-   **Primitive Data Types**: byte, short, int, long, float, double, char, boolean
-   **Wrapper Classes**: Byte, Short, Integer, Long, Float, Double, Character, Boolean

### Constant Pools:

In Java, the constant pool is a special area of memory allocated to store literal values and symbolic references used by a Java program. It includes string literals, class and method names, field names, and other constants.

### String Class:

The String class in Java represents a sequence of characters. It is immutable, meaning once created, its value cannot be changed. Any operation that appears to modify a String actually creates a new String object.

```java
String str = "Hello"; // String literal
String str2 = new String("World"); // Using constructor
```

### StringBuffer & StringBuilder Class:

StringBuffer and StringBuilder are mutable counterparts of the String class. They allow modification of the character sequence without creating a new object. StringBuffer is thread-safe but slower, while StringBuilder is not thread-safe but faster.

```java
StringBuffer sb = new StringBuffer("Hello");
StringBuilder sb = new StringBuilder("World");
```

### String Pool:

The String pool, also known as the intern pool, is a special memory area in the JVM where String literals are stored. When a String literal is encountered, the JVM checks if it already exists in the pool. If it does, a reference to the existing String object is returned. If not, a new String object is created and added to the pool.

### How Wrapper Classes and Constant Pools Work Together:

When using wrapper classes, such as `Integer` or `Double`, to represent primitive data types, the JVM maintains a cache of commonly used values within the constant pool. This means that for frequently used values, the wrapper class may return the same object from the constant pool rather than creating a new one each time.

```java
Integer a = 10;
Integer b = 10;
System.out.println(a == b); // Output: true (because both a and b refer to the same object in the constant pool)
```

### 

### Exception Hierarchy:

In Java, exceptions are objects representing exceptional conditions that occur during the execution of a program. They are organized in a hierarchical structure:

-   **Throwable**: The superclass of all exceptions and errors.
    -   **Error**: Represents serious problems that a reasonable application should not try to catch. Examples include `OutOfMemoryError` and `StackOverflowError`.
    -   **Exception**: Represents exceptional conditions that a well-behaved program should handle.
        -   **RuntimeException**: Represents exceptions that can be caught during the normal operation of the Java Virtual Machine. Examples include `NullPointerException` and `ArrayIndexOutOfBoundsException`.
        -   **Checked Exceptions**: All exceptions that are not subclasses of RuntimeException. They must be caught or declared to be thrown. Examples include `IOException` and `SQLException`.

### Exception Propagation:

Exception propagation is the mechanism by which an exception is thrown from one method to another until it is caught or the program terminates. When a method encounters an exception that it cannot handle, it throws the exception to its caller.

### Try-Catch-Finally Block:

The try-catch-finally block is used to handle exceptions in Java. It consists of three parts:

-   **try**: The block of code where exceptions may occur.
-   **catch**: The block of code that handles exceptions thrown within the try block.
-   **finally**: The block of code that executes regardless of whether an exception is thrown or not. It is often used for cleanup operations.

```java
try {
    // Code that may throw an exception
} catch (ExceptionType e) {
    // Code to handle the exception
} finally {
    // Code that always executes
}
```

### Throws Clause and Throw Keyword:

The throws clause is used in method declarations to indicate that the method may throw certain exceptions. The throw keyword is used to explicitly throw an exception within a method.

```java
void myMethod() throws IOException {
    if (condition) {
        throw new IOException("An IO error occurred");
    }
}
```

### Multi-Catch Block:

Java 7 introduced the multi-catch block, allowing multiple exceptions to be caught in a single catch block.

```java
try {
    // Code that may throw exceptions
} catch (IOException | SQLException e) {
    // Code to handle IOException or SQLException
}
```

### Creating User-Defined Checked and Unchecked Exceptions:

You can create your own custom exceptions by extending existing exception classes.

```java
// Custom checked exception
class MyCheckedException extends Exception {
    // Constructor
}

// Custom unchecked exception
class MyUncheckedException extends RuntimeException {
    // Constructor
}
```

### InputStream and OutputStream Interfaces:

-   **InputStream**: It is an abstract class representing an input stream of bytes. It is used to read data from a source.
-   **OutputStream**: It is an abstract class representing an output stream of bytes. It is used to write data to a destination.

### Reader and Writer Interfaces:

-   **Reader**: It is an abstract class representing a character stream input. It is used to read characters from a source.
-   **Writer**: It is an abstract class representing a character stream output. It is used to write characters to a destination.

### NIO Package:

The NIO (New I/O) package, introduced in Java 1.4, provides an alternative to the standard I/O API (InputStream, OutputStream, Reader, Writer). It offers improved performance and support for non-blocking I/O operations.

Key components of the NIO package include:

-   **Buffers**: Byte buffers and character buffers for efficient data handling.
-   **Channels**: Provides support for I/O operations on channels, such as FileChannel and SocketChannel.
-   **Selectors**: Allows for multiplexed, non-blocking I/O operations.

### Serialization and Deserialization:

Serialization is the process of converting an object into a byte stream, which can be persisted or transmitted over a network. Deserialization is the reverse process of reconstructing the object from the byte stream.

```java
// Serialization
try (ObjectOutputStream out = new ObjectOutputStream(new FileOutputStream("data.bin"))) {
    out.writeObject(myObject);
}

// Deserialization
try (ObjectInputStream in = new ObjectInputStream(new FileInputStream("data.bin"))) {
    MyClass myObject = (MyClass) in.readObject();
}
```

### Shallow Copy and Deep Copy:

-   **Shallow Copy**: Involves creating a new object and then copying the non-static fields of the current object to the new object. If the field is a primitive type, a shallow copy copies the actual value; if it is a reference type, it copies the reference, not the object itself.
-   **Deep Copy**: Involves creating a new object and then recursively copying all fields, including nested objects, to the new object. This ensures that the new object is entirely independent of the original object.

```java
// Shallow copy example
MyClass shallowCopy = original.clone();

// Deep copy example
MyClass deepCopy = original.deepClone();
```

### Date, DateTime, and Calendar Classes:

-   **Date Class**: Represents a specific instant in time, with millisecond precision. It's part of the `java.util` package.
-   **DateTime Class**: There is no specific DateTime class in Java, but you can manipulate dates and times using the Date class along with other classes like Calendar and SimpleDateFormat.
-   **Calendar Class**: Provides methods for manipulating dates and times in a calendar. It's also part of the `java.util` package and offers more functionality than the Date class.

### Converting Date to String and String to Date using SimpleDateFormat:

The SimpleDateFormat class is used to format and parse dates in a specific pattern.

```java
import java.text.SimpleDateFormat;
import java.util.Date;

public class Main {
    public static void main(String[] args) {
        // Creating a Date object
        Date date = new Date();

        // Converting Date to String
        SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");
        String dateString = sdf.format(date);
        System.out.println("Date to String: " + dateString);

        // Converting String to Date
        try {
            Date parsedDate = sdf.parse(dateString);
            System.out.println("String to Date: " + parsedDate);
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Object Class: Overriding toString, equals, and hashCode Methods:

The Object class is the root class for all Java classes. It provides several methods that can be overridden in subclasses for custom behavior:

-   **toString()**: Returns a string representation of the object. It's often overridden to provide meaningful information about the object's state.
-   **equals()**: Compares two objects for equality. It's overridden to define custom equality criteria for objects.
-   **hashCode()**: Returns a hash code value for the object. It's overridden when the equals method is overridden to maintain the general contract of hashCode.

```java
public class MyClass {
    private int id;
    private String name;

    // Constructor, getters, and setters

    @Override
    public String toString() {
        return "MyClass{" +
                "id=" + id +
                ", name='" + name + '\'' +
                '}';
    }

    @Override
    public boolean equals(Object obj) {
        if (this == obj) return true;
        if (obj == null || getClass() != obj.getClass()) return false;
        MyClass myClass = (MyClass) obj;
        return id == myClass.id && Objects.equals(name, myClass.name);
    }

    @Override
    public int hashCode() {
        return Objects.hash(id, name);
    }
}
```

### Introduction to Collections: Collection Hierarchy

In Java, the Collections Framework provides a set of interfaces and classes to represent and manipulate groups of objects, known as collections. The core interfaces in the framework include:

1.  **Collection Interface**: The root interface in the collections hierarchy. It defines the basic methods shared by all collection types, such as `add`, `remove`, and `size`.
2.  **List Interface**: Extends the Collection interface and represents an ordered collection of elements. Lists allow duplicate elements and maintain the order of insertion.
3.  **Queue Interface**: Also extends the Collection interface, representing a collection designed for holding elements prior to processing. Queues typically follow the First-In-First-Out (FIFO) order.
4.  **Set Interface**: Extends the Collection interface but does not allow duplicate elements. Sets have no defined order.
5.  **Map Interface**: Represents a collection of key-value pairs, where each key is associated with exactly one value. Maps do not extend the Collection interface.

### List, Queue, Set, and Map Collections:

-   **List**: Ordered collection that allows duplicate elements. Common implementations include ArrayList, LinkedList, and Vector.
-   **Queue**: Represents a collection designed for holding elements prior to processing. Common implementations include LinkedList and PriorityQueue.
-   **Set**: Unordered collection that does not allow duplicate elements. Common implementations include HashSet, LinkedHashSet, and TreeSet.
-   **Map**: Represents a collection of key-value pairs. Common implementations include HashMap, LinkedHashMap, TreeMap, and Hashtable.

### List Collection:

-   **ArrayList**: Implements a dynamic array, providing fast random access and efficient insertions/deletions at the end. It is not synchronized.
-   **LinkedList**: Implements a doubly-linked list, allowing for fast insertions/deletions at any position. It also implements the Queue interface.
-   **Vector**: Similar to ArrayList but synchronized, making it thread-safe. However, it is considered less efficient than ArrayList.

### Collections Class:

The `Collections` class in the `java.util` package provides utility methods for working with collections. It includes methods like `sort`, `shuffle`, `reverse`, and `binarySearch`, among others.

### Comparable and Comparator Interfaces:

-   **Comparable**: The `Comparable` interface is used to define the natural order of elements of a class. The class whose objects are being compared must implement the `Comparable` interface.
-   **Comparator**: The `Comparator` interface is used to define a custom order for objects of a class. It is often used when you want to sort objects based on criteria other than their natural order.

### Queue Collection:

The `Queue` interface represents a collection designed for holding elements prior to processing. It extends the Collection interface and adds methods for operations such as insertion, removal, and examination of the elements.

Common implementations include `LinkedList` and `PriorityQueue`.

```java
Queue<String> queue = new LinkedList<>();
queue.offer("Element 1");
queue.offer("Element 2");

String head = queue.poll(); // Retrieves and removes the head of the queue
```

### Set Collection:

A Set is a collection that contains unique elements. It does not allow duplicate elements. In Java, the Set interface is part of the Collections Framework and is implemented by several classes.

### HashSet:

-   HashSet is an implementation of the Set interface that uses a hash table for storage.
-   It does not guarantee the order of elements.
-   It provides constant-time performance for basic operations such as add, remove, contains, and size, assuming the hash function disperses the elements properly among the buckets.

### LinkedHashSet:

-   LinkedHashSet is an implementation of the Set interface that maintains insertion order.
-   It internally uses a hash table along with a linked list to maintain the insertion order of elements.
-   It provides constant-time performance for basic operations such as add, remove, contains, and size, assuming the hash function disperses the elements properly among the buckets.

### TreeSet:

-   TreeSet is an implementation of the Set interface that maintains elements in sorted order.
-   It internally uses a red-black tree structure to store elements in sorted order.
-   It provides log(n) time complexity for basic operations such as add, remove, contains, and size.

### Backed Set Collections:

In Java, backed collections are collections that are created as views of other collections. Modifying the original collection reflects changes in the backed collection, and vice versa.

For sets, you can create backed collections using the `Collections.synchronizedSet` and `Collections.unmodifiableSet` methods.

#### Synchronized Set:

```java
Set<String> originalSet = new HashSet<>();
Set<String> synchronizedSet = Collections.synchronizedSet(originalSet);
```

The `synchronizedSet` method returns a synchronized (thread-safe) view of the original set.

#### Unmodifiable Set:

```java
Set<String> originalSet = new HashSet<>();
Set<String> unmodifiableSet = Collections.unmodifiableSet(originalSet);
```

The `unmodifiableSet` method returns an unmodifiable view of the original set, meaning that attempts to modify the collection will result in an UnsupportedOperationException.

### 

### Map Collection:

A Map is a collection that stores key-value pairs. Each key is associated with exactly one value, and keys are unique within the map. In Java, the Map interface is part of the Collections Framework and is implemented by several classes.

### Hashtable:

-   Hashtable is one of the original implementations of the Map interface in Java.
-   It is synchronized, meaning it is thread-safe.
-   It does not allow null keys or values.
-   It does not maintain any order of the elements.

### HashMap:

-   HashMap is a widely-used implementation of the Map interface.
-   It is not synchronized, making it more efficient in single-threaded scenarios.
-   It allows null keys and values.
-   It does not maintain any order of the elements.

### LinkedHashMap:

-   LinkedHashMap is an implementation of the Map interface that maintains insertion order.
-   It maintains a doubly-linked list to preserve the insertion order of elements.
-   It offers predictable iteration order, making it suitable for use cases that require ordered iteration.

### TreeMap:

-   TreeMap is an implementation of the Map interface that maintains elements in sorted order.
-   It internally uses a red-black tree structure to store elements in sorted order.
-   It offers log(n) time complexity for basic operations such as add, remove, contains, and size.

### Backed Map Collections:

Similar to backed set collections, you can create backed map collections using the `Collections.synchronizedMap` and `Collections.unmodifiableMap` methods.

#### Synchronized Map:

```java
Map<String, Integer> originalMap = new HashMap<>();
Map<String, Integer> synchronizedMap = Collections.synchronizedMap(originalMap);
```

The `synchronizedMap` method returns a synchronized (thread-safe) view of the original map.

#### Unmodifiable Map:

```java
Map<String, Integer> originalMap = new HashMap<>();
Map<String, Integer> unmodifiableMap = Collections.unmodifiableMap(originalMap);
```

The `unmodifiableMap` method returns an unmodifiable view of the original map, meaning that attempts to modify the map will result in an UnsupportedOperationException.

### Concurrent Collections:

Java provides a set of concurrent collections in the `java.util.concurrent` package, which are designed for use in multi-threaded scenarios where multiple threads may access and modify the collections concurrently.

Some commonly used concurrent map collections include ConcurrentHashMap and ConcurrentSkipListMap.

```java
ConcurrentMap<String, Integer> concurrentMap = new ConcurrentHashMap<>();
```

These concurrent collections offer thread-safe operations and high concurrency performance, making them suitable for use in multi-threaded applications without the need for explicit synchronization.

### Thread Class and Runnable Interface:

-   **Thread Class**: Represents a single thread of execution in a Java program. You can create a thread by extending the Thread class and overriding its `run()` method.

```java
class MyThread extends Thread {
    public void run() {
        // Thread execution logic
    }
}
```

-   **Runnable Interface**: Provides a way to create a thread by implementing the Runnable interface and passing an instance of it to a Thread object.

```java
class MyRunnable implements Runnable {
    public void run() {
        // Thread execution logic
    }
}

Thread thread = new Thread(new MyRunnable());
```

### Thread Methods:

-   **sleep(long milliseconds)**: Causes the currently executing thread to sleep (temporarily pause execution) for the specified number of milliseconds.
-   **join()**: Waits for the thread on which it is called to terminate.
-   **yield()**: Causes the currently executing thread to pause temporarily and allow other threads of the same priority to execute.
-   **setPriority(int priority)**: Sets the priority of the thread. The priority range is from MIN_PRIORITY (1) to MAX_PRIORITY (10).
-   **getPriority()**: Returns the priority of the thread.

### ThreadGroup Class:

The ThreadGroup class represents a group of threads. Threads can be organized into groups for ease of management and control. Some key methods of the ThreadGroup class include:

-   **ThreadGroup(String name)**: Constructs a new thread group with the specified name.
-   **setMaxPriority(int priority)**: Sets the maximum priority of the thread group.
-   **activeCount()**: Returns the number of active threads in the thread group and its subgroups.
-   **list()**: Prints information about the thread group to the standard output stream.

### Example:

```java
class MyThread extends Thread {
    public void run() {
        System.out.println("Thread running");
    }
}

public class Main {
    public static void main(String[] args) {
        ThreadGroup group = new ThreadGroup("MyThreadGroup");

        MyThread thread1 = new MyThread();
        Thread thread2 = new Thread(group, new MyRunnable());

        thread1.start();
        thread2.start();

        System.out.println("Active threads in group: " + group.activeCount());
        group.list();
    }
}
```

### Synchronization:

Synchronization in Java is the capability to control the access of multiple threads to shared resources. It ensures that only one thread can access the resource at any given time, preventing data corruption and ensuring thread safety.

### Deadlock:

Deadlock occurs when two or more threads are blocked forever, waiting for each other to release resources. This typically happens when two or more threads hold locks on resources and wait for each other to release their locks.

### wait, notify, and notifyAll methods:

-   **wait()**: Causes the current thread to wait until another thread invokes the notify() or notifyAll() method for the same object.
-   **notify()**: Wakes up a single thread that is waiting on this object's monitor. If multiple threads are waiting, only one of them is awakened.
-   **notifyAll()**: Wakes up all threads that are waiting on this object's monitor.

These methods must be called from synchronized code blocks or synchronized methods.

### Producer & Consumer Problem:

The Producer-Consumer problem is a classic synchronization problem where there are two types of threads: producers and consumers. Producers produce data items and put them into a shared buffer, while consumers consume these data items from the buffer.

```java
class Buffer {
    private List<Integer> buffer = new ArrayList<>();
    private int capacity;

    Buffer(int capacity) {
        this.capacity = capacity;
    }

    public synchronized void produce(int data) throws InterruptedException {
        while (buffer.size() == capacity) {
            wait(); // Wait if buffer is full
        }
        buffer.add(data);
        notifyAll(); // Notify consumers
    }

    public synchronized int consume() throws InterruptedException {
        while (buffer.isEmpty()) {
            wait(); // Wait if buffer is empty
        }
        int data = buffer.remove(0);
        notifyAll(); // Notify producers
        return data;
    }
}

class Producer implements Runnable {
    private Buffer buffer;

    Producer(Buffer buffer) {
        this.buffer = buffer;
    }

    public void run() {
        try {
            while (true) {
                int data = produceData();
                buffer.produce(data);
                Thread.sleep(1000);
            }
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
    }

    private int produceData() {
        return new Random().nextInt(100);
    }
}

class Consumer implements Runnable {
    private Buffer buffer;

    Consumer(Buffer buffer) {
        this.buffer = buffer;
    }

    public void run() {
        try {
            while (true) {
                int data = buffer.consume();
                consumeData(data);
                Thread.sleep(2000);
            }
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
    }

    private void consumeData(int data) {
        System.out.println("Consumed: " + data);
    }
}

public class Main {
    public static void main(String[] args) {
        Buffer buffer = new Buffer(5);
        Thread producerThread = new Thread(new Producer(buffer));
        Thread consumerThread = new Thread(new Consumer(buffer));

        producerThread.start();
        consumerThread.start();
    }
}
```

Here are the keywords to remember for the above two questions on synchronization and the Producer & Consumer problem:

### Synchronization:

1.  **Deadlock**: Situation where two or more threads are blocked forever, waiting for each other to release resources.
2.  **wait()**: Causes the current thread to wait until another thread invokes the notify() or notifyAll() method for the same object.
3.  **notify()**: Wakes up a single thread that is waiting on this object's monitor.
4.  **notifyAll()**: Wakes up all threads that are waiting on this object's monitor.

### Producer & Consumer Problem:

1.  **Producer**: Thread responsible for producing data items and putting them into a shared buffer.
2.  **Consumer**: Thread responsible for consuming data items from the shared buffer.
3.  **Buffer**: Shared resource where producers put data items and consumers consume them.
4.  **wait()**: Method called by threads to wait if the buffer is full or empty.
5.  **notify()**: Method called to wake up threads waiting on the buffer.
6.  **synchronized**: Keyword used to ensure that only one thread can access a synchronized block of code or method at a time.
7.  **Race Condition**: Situation where the outcome of a program depends on the relative timing of events between threads.

Let's explore Generics and the Reflection API in Java.

### Generics:

Generics in Java allow you to parameterize types. They provide a way to specify the type of objects that a collection can contain, or the type of objects that a method can operate on, without specifying the actual type until runtime.

-   **Type Safety**: Generics provide compile-time type checking, which helps detect errors at compile time rather than at runtime.
-   **Code Reusability**: Generics allow you to write reusable code that can work with different types without the need for type casting.
-   **Elimination of Type Casting**: With generics, you can avoid explicit type casting, making the code cleaner and more readable.

```java
// Generic class
class Box<T> {
    private T value;

    public T getValue() {
        return value;
    }

    public void setValue(T value) {
        this.value = value;
    }
}

// Using the generic class
Box<Integer> integerBox = new Box<>();
integerBox.setValue(10);
int value = integerBox.getValue(); // No need for type casting
```

### Reflection API:

The Reflection API in Java allows you to inspect and manipulate classes, interfaces, fields, methods, and constructors at runtime.

-   **Dynamic Class Loading**: Reflection enables you to dynamically load classes, instantiate objects, and invoke methods without knowing their names at compile time.
-   **Introspection**: Reflection provides the ability to examine the properties of objects at runtime, such as their fields and methods, and to invoke methods dynamically.
-   **Extensibility**: Reflection allows frameworks and libraries to be more flexible and adaptable, as they can interact with unknown classes and objects at runtime.

```java
// Example of using Reflection to inspect a class
Class<?> clazz = MyClass.class;
Field[] fields = clazz.getDeclaredFields();
Method[] methods = clazz.getDeclaredMethods();

for (Field field : fields) {
    System.out.println("Field: " + field.getName());
}

for (Method method : methods) {
    System.out.println("Method: " + method.getName());
}
```

### Use Cases:

-   Generics are commonly used in collections such as ArrayList, HashMap, etc., to provide type-safe operations.
-   Reflection is used in frameworks like Spring and Hibernate for dependency injection and object-relational mapping, where classes and methods need to be dynamically loaded and instantiated at runtime.

### Introduction to Generics:

Generics in Java provide a way to create classes, interfaces, and methods that can work with any type of data. They allow you to specify a placeholder for a type that will be determined when the code is used, rather than when it is written.

### Generic Classes:

Generic classes in Java are classes that can operate on any type of data. They are defined with one or more type parameters enclosed in angle brackets (`<>`).

```java
class Box<T> {
    private T value;

    public T getValue() {
        return value;
    }

    public void setValue(T value) {
        this.value = value;
    }
}
```

### Generic Methods:

Generic methods are methods that can operate on any type of data. They are declared with a type parameter that is specified before the return type.

```java
class Utils {
    public <T> void printValue(T value) {
        System.out.println("Value: " + value);
    }
}
```

### Wildcards (Upper and Lower):

Wildcards in Java generics allow you to specify unknown types in a generic type declaration. There are two types of wildcards: upper bounded wildcard (`<? extends T>`) and lower bounded wildcard (`<? super T>`).

-   **Upper Bounded Wildcard**: Restricts the type to be a specific type or a subtype of that type.
-   **Lower Bounded Wildcard**: Restricts the type to be a specific type or a supertype of that type.

```java
public void printList(List<? extends Number> list) {
    for (Number n : list) {
        System.out.println(n);
    }
}
```

In Java generics, `extends` and `super` are used in the context of bounded wildcards to specify the upper and lower bounds of a generic type parameter. They provide flexibility in defining generic classes, methods, and wildcards.

### `extends` in Generics:

-   **Upper Bounded Wildcard**: `extends` is used to specify the upper bound of a generic type parameter. It restricts the type to be a specific type or a subtype of that type.
-   It is primarily used when you want to accept a collection of elements of a certain type or its subtypes.

```java
public void printList(List<? extends Number> list) {
    for (Number n : list) {
        System.out.println(n);
    }
}
```

In this example, `<? extends Number>` means that the method can accept a list of elements of type `Number` or its subtypes (e.g., `Integer`, `Double`, etc.).

### `super` in Generics:

-   **Lower Bounded Wildcard**: `super` is used to specify the lower bound of a generic type parameter. It restricts the type to be a specific type or a supertype of that type.
-   It is primarily used when you want to add elements to a collection that are of a certain type or its supertypes.

```java
public void addNumbers(List<? super Integer> list) {
    list.add(10);
    list.add(20);
}
```

In this example, `<? super Integer>` means that the method can accept a list that can hold elements of type `Integer` or its supertypes (e.g., `Number`, `Object`, etc.).

### Comparison:

-   `extends` is used to specify an upper bound, allowing the generic type to be any subtype of the specified type.
-   `super` is used to specify a lower bound, allowing the generic type to be any supertype of the specified type.

### When to Use:

-   Use `extends` when you want to consume (read) elements from a collection.
-   Use `super` when you want to produce (write) elements to a collection.

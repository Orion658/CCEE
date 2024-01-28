**[ ] C++ CCEE Syllabus**

### Installation and Setup of Development Environment:

To start programming in C++, you need a compiler and an IDE (Integrated Development Environment) or a text editor. Here's a basic setup guide:

1.  **Compiler**: You can use GCC (GNU Compiler Collection) or Clang, both of which are widely used and support C++.
    1.  For Windows: You can use MinGW (Minimalist GNU for Windows) or install GCC via tools like Cygwin or MSYS2.
    2.  For macOS: Clang comes pre-installed with Xcode command line tools. You can also install GCC via Homebrew.
    3.  For Linux: GCC usually comes pre-installed. You can install Clang via your package manager.
2.  **IDE**: Choose an IDE or a text editor with C++ support. Some popular options include Visual Studio (Windows), Xcode (macOS), CLion, Code::Blocks, and Eclipse.
3.  **Text Editor**: If you prefer a lightweight option, you can use text editors like Visual Studio Code, Sublime Text, Atom, or Vim, with plugins for C++ support.

Once you've installed a compiler and chosen your preferred IDE or text editor, you're ready to start writing C++ code!

### The Need for C++:

C++ was developed to overcome the limitations of the C programming language by adding features such as classes, inheritance, polymorphism, and more. It provides a balance between high-level abstraction and low-level control, making it suitable for a wide range of applications, including system programming, game development, and performance-critical software.

### Features of C++:

-   **Object-Oriented**: C++ supports object-oriented programming paradigms, including classes, objects, inheritance, polymorphism, encapsulation, and abstraction.
-   **Efficiency**: C++ gives you fine-grained control over system resources and memory, allowing for high-performance code.
-   **Standard Library**: C++ provides a rich standard library (STL) with containers, algorithms, iterators, and utilities.
-   **Compatibility with C**: C++ is largely compatible with C, allowing you to leverage existing C code and libraries.
-   **Portability**: C++ code can be compiled and run on various platforms with minimal changes.
-   **Flexibility**: C++ allows for both high-level and low-level programming, making it suitable for a wide range of applications.

### C++ versus C:

-   **Object-Oriented Programming**: C++ supports OOP concepts like classes and objects, which are absent in C.
-   **Stronger Type Checking**: C++ has stricter type checking compared to C.
-   **Standard Library**: C++ has a richer standard library compared to C.
-   **Exception Handling**: C++ supports exception handling, while C relies on error codes and manual error handling.
-   **Compatibility**: C++ is mostly compatible with C, meaning most C code can be compiled with a C++ compiler.
-   **Namespace Support**: C++ introduces namespaces for better organization of code, which is not present in C.

### History of C++:

-   C++ was developed by Bjarne Stroustrup at Bell Labs in the early 1980s as an extension of the C programming language.
-   The first commercial implementation of C++ was released in 1985.
-   C++ underwent standardization in 1998 (C++98), followed by C++11, C++14, C++17, and C++20, each introducing new features and improvements to the language.

### Writing Your First C++ Program:

Here's a simple "Hello, World!" program in C++:

```cpp
#include <iostream>

int main() {
    std::cout << "Hello, World!" << std::endl;
    return 0;
}
```

Explanation:

-   `#include <iostream>`: This line includes the input/output stream library, which provides functions for input and output operations.
-   `int main() { }`: This is the main function where program execution begins.
-   `std::cout << "Hello, World!" << std::endl;`: This line outputs "Hello, World!" to the console.
-   `return 0;`: Indicates successful program termination.

### 1. Print Hello World:

```cpp
#include <iostream>

int main() {
    std::cout << "Hello, World!" << std::endl;
    return 0;
}
```

### 2. Add Two Numbers:

```cpp
#include <iostream>

int main() {
    int num1 = 5;
    int num2 = 7;
    int sum = num1 + num2;
    std::cout << "Sum: " << sum << std::endl;
    return 0;
}
```

### 3. Calculate Compound Interest:

```cpp
#include <iostream>
#include <cmath>

int main() {
    double principal = 1000;
    double rate = 5.5;
    double time = 2.5;
    
    double compound_interest = principal * pow((1 + rate / 100), time);
    
    std::cout << "Compound Interest: " << compound_interest << std::endl;
    
    return 0;
}
```

### 4. Calculate Power of a Number:

```cpp
#include <iostream>
#include <cmath>

int main() {
    double base = 3.0;
    int exponent = 4;
    
    double result = pow(base, exponent);
    
    std::cout << "Result: " << result << std::endl;
    
    return 0;
}
```

### 5. Swap Two Numbers:

```cpp
#include <iostream>

int main() {
    int a = 5;
    int b = 10;
    
    std::cout << "Before swapping: a = " << a << ", b = " << b << std::endl;
    
    // Swap logic using a temporary variable
    int temp = a;
    a = b;
    b = temp;
    
    std::cout << "After swapping: a = " << a << ", b = " << b << std::endl;
    
    return 0;
}
```

### 6. Calculate Area of Rectangle:

```cpp
#include <iostream>

int main() {
    double length = 5.0;
    double width = 3.0;
    
    double area = length * width;
    
    std::cout << "Area of Rectangle: " << area << std::endl;
    
    return 0;
}
```

### 1. Introduction of Advanced C++ Concepts and Features of C++17:

C++17 introduced several new features and improvements, including:

1.  **Structured Bindings**:
    1.  Structured bindings allow you to unpack the elements of a tuple or a pair into separate variables easily.
    2.  Example:

```cpp
std::tuple<int, double> result = {10, 3.14};
auto [x, y] = result;
```

1.  **Inline Variables**:
    1.  C++17 introduces inline variables, which allow the definition of variables directly within class definitions.
    2.  Example:

```cpp
class MyClass {
public:
    inline static int value = 5;
};
```

1.  **constexpr if**:
    1.  `constexpr if` allows compile-time conditional branching based on template parameters or constexpr conditions.
    2.  It enables more concise and expressive code without resorting to template metaprogramming tricks.
    3.  Example:

```cpp
template <typename T>
void process(T value) {
    if constexpr (std::is_integral<T>::value) {
        // Code specific to integral types
    } else {
        // Code for other types
    }
}
```

1.  **std::optional**:
    1.  `std::optional` is a nullable value type that can hold a value or be empty.
    2.  It provides a safer alternative to using pointers or sentinel values to represent optional values.
    3.  Example:

```cpp
std::optional<int> maybeValue;
if (maybeValue.has_value()) {
    int value = maybeValue.value();
}
```

1.  **std::variant**:
    1.  `std::variant` is a type-safe union that can hold a value from a specified set of alternative types.
    2.  It provides a type-safe alternative to traditional unions and can be used for implementing polymorphic behavior.
    3.  Example:

```cpp
std::variant<int, double, std::string> value;
value = 10;
std::cout << std::get<int>(value) << std::endl;
```

1.  **std::filesystem**:
    1.  `std::filesystem` provides a modern, object-oriented interface for filesystem operations.
    2.  It simplifies common filesystem tasks like file and directory manipulation, path operations, and file status queries.
    3.  Example:

```cpp
#include <filesystem>
namespace fs = std::filesystem;
fs::path currentPath = fs::current_path();
```

1.  **Parallel Algorithms**:
    1.  C++17 introduces parallel versions of several standard algorithms in the `<algorithm>` header.
    2.  These algorithms leverage multi-core processors to execute computations in parallel, improving performance for large datasets.
    3.  Example:

```cpp
std::vector<int> data = {1, 2, 3, 4, 5};
std::for_each(std::execution::par, data.begin(), data.end(), [](int& x) { x *= 2; });
```

-   Fold Expressions
-   Improved constexpr functions
-   and more.

### 3. C++ Tokens:

Tokens are the smallest units in a C++ program. They can be identifiers, keywords, literals, operators, or punctuators. Examples:

-   Identifiers: `variableName`, `ClassName`
-   Keywords: `int`, `class`, `if`, `else`, `return`
-   Literals: `123`, `3.14`, `"Hello"`
-   Operators: `+`, `-`, `*`, `/`, `=`
-   Punctuators: `;`, `,`, `()`, `{}`, `[]`

### 4. Initialization:

Initialization in C++ can be done in several ways:

-   **Direct Initialization**: `int x(5);`
-   **Copy Initialization**: `int y = 10;`
-   **List Initialization (Uniform Initialization)**: `int z{15};`
-   **Default Initialization**: `int a;` (uninitialized variables are default-initialized)

### 5. Static Members:

Static members of a class are shared by all instances of the class. They are declared using the `static` keyword and can be accessed without creating an instance of the class.

```cpp
class MyClass {
public:
    static int count; // Static member variable
    void display() {
        cout << "Count: " << count << endl;
    }
};

int MyClass::count = 0; // Initializing static member variable

int main() {
    MyClass obj1, obj2;
    obj1.display(); // Output: Count: 0
    obj2.display(); // Output: Count: 0
    
    MyClass::count = 5; // Accessing and modifying static member
    obj1.display(); // Output: Count: 5
    obj2.display(); // Output: Count: 5
    
    return 0;
}
```

### 6. Constant Members:

Constant member variables are declared using the `const` keyword and cannot be modified after initialization. They must be initialized in the constructor initializer list.

```cpp
class Circle {
private:
    const double pi = 3.14;
    const double radius;
public:
    Circle(double r) : radius(r) {}
    double getArea() {
        return pi * radius * radius;
    }
};

int main() {
    Circle c(5.0);
    cout << "Area: " << c.getArea() << endl;
    return 0;
}
```

### 7. Expressions:

Expressions in C++ are combinations of operators, constants, variables, and function calls that produce a value. Examples:

-   Arithmetic Expressions: `x + y`, `a * b - c`
-   Relational Expressions: `x < y`, `a == b`
-   Logical Expressions: `x && y`, `!(a || b)`
-   Assignment Expressions: `x = 5`, `y += 10`
-   Function Call Expressions: `func(5, 10)`


[ ] Operators in C++:

### 1. Arithmetic Operators:

Arithmetic operators are used to perform mathematical operations on operands. These include addition, subtraction, multiplication, division, modulus, and increment/decrement.

-   **Addition (+)**: Adds two operands.
-   **Subtraction (-)**: Subtracts the second operand from the first.
-   **Multiplication (\*)**: Multiplies two operands.
-   **Division (/)**: Divides the first operand by the second.
-   **Modulus (%)**: Returns the remainder of division.
-   **Increment (++)**: Increases the value of an operand by 1.
-   **Decrement (--)**: Decreases the value of an operand by 1.

### 2. Relational Operators:

Relational operators are used to compare two operands. They return a boolean value (true or false) based on the comparison.

-   **Equal to (==)**: Checks if two operands are equal.
-   **Not equal to (!=)**: Checks if two operands are not equal.
-   **Greater than (\>)**: Checks if the first operand is greater than the second.
-   **Less than (\<)**: Checks if the first operand is less than the second.
-   **Greater than or equal to (\>=)**: Checks if the first operand is greater than or equal to the second.
-   **Less than or equal to (\<=)**: Checks if the first operand is less than or equal to the second.

### 3. Logical Operators:

Logical operators are used to combine multiple conditions or to negate a condition. They return a boolean value.

-   **Logical AND (&&)**: Returns true if both operands are true.
-   **Logical OR (\|\|)**: Returns true if at least one operand is true.
-   **Logical NOT (!)**: Returns the opposite boolean value of the operand.

### 4. Unary Operators:

Unary operators operate on a single operand.

-   **Unary Plus (+)**: Indicates a positive value.
-   **Unary Minus (-)**: Negates the value of an operand.
-   **Logical NOT (!)**: Inverts the boolean value of an operand.
-   **Increment (++)**: Increases the value of an operand by 1.
-   **Decrement (--)**: Decreases the value of an operand by 1.

### 5. Ternary Operator:

The ternary operator (also known as the conditional operator) is a conditional expression that evaluates a condition and returns one of two possible values depending on whether the condition is true or false.

-   **Syntax**: `condition ? value_if_true : value_if_false`
-   Example: `int x = (a > b) ? a : b;`

### 6. Assignment Operator:

Assignment operators are used to assign a value to a variable.

-   **Simple Assignment (=)**: Assigns the value of the right operand to the left operand.
-   **Compound Assignment (e.g.,** `+=`**,** `-=`**,** `*=`**,** `/=`**,** `%=`**, etc.)**: Performs an arithmetic operation on the variable and assigns the result to the variable.

**[ ] C++ operators, from highest to lowest precedence:**

1.  **Parentheses** `()`: Highest precedence, used to group expressions.
2.  **Unary Operators**: Including `++`, `--`, `+, -`, `!`.
3.  **Multiplicative Operators**: Including `*`, `/`, `%`.
4.  **Additive Operators**: Including `+`, `-`.
5.  **Relational Operators**: Including `<`, `>`, `<=`, `>=`.
6.  **Equality Operators**: Including `==`, `!=`.
7.  **Logical AND Operator** `&&`.
8.  **Logical OR Operator** `||`.
9.  **Conditional Operator (Ternary)** `? :`.
10. **Assignment Operators**: Including `=`, `+=`, `-=`, `*=`, `/=`, `%=`, etc.
11. **Comma Operator** `,`: Lowest precedence, used to separate expressions.

Keep in mind that precedence determines the order in which operators are evaluated within an expression. Parentheses can be used to override the default precedence and explicitly specify the order of evaluation.


**[ ] Conditional and Looping Statements**

### 1. If, else if, switch:

-   **if Statement**: Executes a block of code if a specified condition is true.
-   **else if Statement**: Allows you to check multiple conditions.
-   **switch Statement**: Evaluates an expression and executes code blocks based on matching cases.

### 2. For Loop:

-   **for Loop**: Executes a block of code a specified number of times.

```cpp
for (initialization; condition; increment/decrement) {
    // code to be executed
}
```

### 3. While Loop:

-   **while Loop**: Executes a block of code as long as a specified condition is true.

```cpp
while (condition) {
    // code to be executed
}
```

### 4. Do While Loop:

-   **do-while Loop**: Similar to the while loop, but guarantees that the code block is executed at least once before the condition is tested.

```cpp
do {
    // code to be executed
} while (condition);
```

### 5. Jump Statements:

-   **break**: Terminates the loop or switch statement and transfers control to the statement immediately following the loop or switch.
-   **continue**: Skips the rest of the current iteration and continues with the next iteration of the loop.
-   **return**: Exits the current function and returns a value.

### 6. Arrays:

-   **Arrays**: Collection of elements of the same data type, stored in contiguous memory locations.
-   **Declaration and Initialization**:

```cpp
int myArray[5]; // Declaration of an array of size 5
int myArray[] = {1, 2, 3, 4, 5}; // Declaration and initialization
```

-   **1-D Arrays**: Single-dimensional arrays.
-   **2-D Arrays**: Multi-dimensional arrays represented as arrays of arrays.

```cpp
int matrix[3][3]; // Declaration of a 2-D array
```

Arrays are fundamental data structures in C++ and are widely used for storing and manipulating collections of data. They offer efficient access to elements using indexing.

**[ ] Functions in C++ :**

### 1. Different Forms of Functions:

-   **Regular Functions**: Standard functions that perform a specific task and return a value (if needed).
-   **Void Functions**: Functions that do not return a value.
-   **Function Overloading**: Defining multiple functions with the same name but different parameter lists.
-   **Recursive Functions**: Functions that call themselves either directly or indirectly.

### 2. Function Prototyping:

-   **Function Prototypes**: Declaration of a function before its actual implementation.
-   Helps the compiler identify the functions before they are used.
-   Typically placed at the beginning of the file or in a header file.
-   Syntax: `returnType functionName(parameters);`

### 3. Call by Reference:

-   **Call by Reference**: Passing arguments to a function by reference, allowing the function to modify the original value of the arguments.
-   Changes made to the parameters inside the function affect the original variables.
-   Syntax: `void functionName(int &a) { }`

### 4. Inline Functions:

-   **Inline Functions**: Functions whose code is inserted directly at each point of call, rather than invoking a separate function call.
-   Typically used for small, frequently-called functions to reduce the overhead of function calls.
-   Declared with the `inline` keyword.
-   Example:

```cpp
inline int square(int x) {
    return x * x;
}
```

### 5. Math Library Functions:

-   C++ provides a built-in math library (`<cmath>`) containing various mathematical functions.
-   Common functions include `sqrt()`, `pow()`, `sin()`, `cos()`, `tan()`, `log()`, `exp()`, etc.
-   These functions operate on numeric data types and return the result of the mathematical operation.


[ ] Introduction to memory management in C++ :

Memory management in C++ involves allocating and deallocating memory for variables, objects, and data structures. It includes concepts such as dynamic memory allocation, deallocation, and management of memory resources. Pointers play a crucial role in memory management by allowing direct access to memory locations and enabling dynamic memory allocation.

### Pointers in C++:

-   **Definition**: Pointers are variables that store memory addresses as their values. They "point" to the location of another object or variable in memory.
-   **Declaration**: Pointers are declared using the data type of the variable they point to, followed by an asterisk (`*`).

```cpp
int *ptr; // Declaration of a pointer to an integer
```

-   **Initialization**: Pointers can be initialized to point to the address of another variable.

```cpp
int x = 5;
int *ptr = &x; // Pointer ptr now points to the address of variable x
```

-   **Dereferencing**: Dereferencing a pointer means accessing the value stored at the memory address it points to. It is done using the asterisk (`*`) operator.

```cpp
int value = *ptr; // Dereferencing ptr to access the value it points to
```

-   **Pointer Arithmetic**: Pointers can be incremented or decremented to move to the next or previous memory location of their data type.

```cpp
ptr++; // Moves ptr to the next memory location of type int
```

-   **Null Pointers**: Pointers can be assigned a special value called a null pointer (`nullptr`), indicating that they do not point to any valid memory address.

```cpp
int *ptr = nullptr; // Initializing ptr as a null pointer
```

-   **Dynamic Memory Allocation**: Pointers are commonly used for dynamic memory allocation using the `new` and `delete` operators.

```cpp
int *ptr = new int; // Allocates memory for an integer and assigns its address to ptr
delete ptr; // Deallocates the memory pointed to by ptr
```

Memory management using pointers requires careful attention to avoid memory leaks (memory that is allocated but not deallocated) and dangling pointers (pointers that point to invalid memory locations). It is important to properly allocate and deallocate memory and ensure that pointers are always pointing to valid memory locations.

Sure, here's a concise overview:

### Arrays Using Pointers:

-   Arrays and pointers are closely related in C++.
-   An array name acts like a constant pointer pointing to the first element.
-   Pointers can be used to access, iterate over, and pass arrays to functions.

#### Accessing Array Elements Using Pointers:

```cpp
int arr[5] = {1, 2, 3, 4, 5};
int *ptr = arr; // Pointer ptr points to the first element of the array

// Accessing array elements using pointers
cout << "First element: " << *ptr << endl; // Output: 1
cout << "Second element: " << *(ptr + 1) << endl; // Output: 2
```

#### Iterating Over Arrays Using Pointers:

```cpp
for (int i = 0; i < 5; ++i) {
    cout << *(ptr + i) << " "; // Output: 1 2 3 4 5
}
```

#### Passing Arrays to Functions Using Pointers:

```cpp
void printArray(int *arr, int size) {
    for (int i = 0; i < size; ++i) {
        cout << *(arr + i) << " ";
    }
}

int main() {
    int arr[5] = {1, 2, 3, 4, 5};
    printArray(arr, 5); // Pass array and its size to the function
    return 0;
}
```

### Enumeration (enum):

-   Enumeration is a user-defined data type for defining named integral constants.
-   Enums improve code readability and maintainability by providing meaningful names for constants.
-   Enums can have explicit values assigned.
-   Enums are commonly used in switch statements for better code organization.

#### Declaration and Initialization:

```cpp
enum Color { RED, GREEN, BLUE }; // Declaration of an enumeration type

Color selectedColor = RED; // Initialization of an enum variable
```

#### Enumeration with Explicit Values:

```cpp
enum Month { JAN = 1, FEB = 2, MAR = 3, APR = 4, MAY = 5 }; // Enum with explicit values
```

### Typedef:

-   `typedef` is a keyword in C++ used to create aliases for existing data types.
-   It allows you to define new names for existing types, making complex types easier to read and maintain.
-   Syntax:

```cpp
typedef existingType newTypeName;
```

-   Example:

```cpp
typedef int Integer; // Defines Integer as an alias for int
Integer num = 10; // Now Integer can be used instead of int
```

### Using New Operator:

-   The `new` operator is used for dynamic memory allocation in C++.
-   It allocates memory for a single variable or an array on the heap.
-   Syntax:

```cpp
int *ptr = new int; // Allocates memory for a single int
int *arr = new int[5]; // Allocates memory for an array of 5 ints
```

-   The `new` operator returns a pointer to the allocated memory.
-   It is accompanied by the `delete` operator to deallocate the dynamically allocated memory.
-   Example:

```cpp
int *ptr = new int; // Allocate memory for a single int
*ptr = 10; // Assign a value to the dynamically allocated int
delete ptr; // Deallocate the memory to avoid memory leaks
```

Both `typedef` and the `new` operator are useful language features that enhance the readability and flexibility of C++ code.

### Class Pointer:

-   Class pointers are pointers that point to objects of a class type.
-   They are used to access members and methods of class objects dynamically.
-   Example:

```cpp
class MyClass {
public:
    int x;
    void display() {
        cout << "Value of x: " << x << endl;
    }
};

MyClass obj;
MyClass *ptr = &obj;
ptr->x = 10;
ptr->display(); // Output: Value of x: 10
```

### this Pointer:

-   The `this` pointer is a pointer that holds the address of the current object.
-   It is implicitly available within non-static member functions of a class.
-   It is used to access members of the current object.
-   Example:

```cpp
class MyClass {
public:
    int x;
    void setX(int x) {
        this->x = x; // Using this pointer to distinguish between member variable and parameter
    }
};

MyClass obj;
obj.setX(10);
```

### Comparison of new over malloc, calloc, and realloc:

-   `new`: Allocates memory for a single object of a specified type, invokes constructor, returns a pointer to the allocated memory.
-   `malloc`: Allocates a block of memory of a specified size in bytes, does not initialize memory, returns a void pointer.
-   `calloc`: Allocates a block of memory for an array of elements, initializes memory to zero, returns a void pointer.
-   `realloc`: Resizes a previously allocated block of memory, may move the block to a new location, returns a void pointer.
-   `new` is type-safe, automatically calculates size, calls constructor, `malloc`/`calloc` return void pointers which require explicit typecasting.

### Memory Freeing Using Delete Operator:

-   The `delete` operator is used to deallocate memory allocated dynamically using `new`.
-   It invokes the destructor of an object before deallocating memory.
-   Syntax:

```cpp
delete ptr; // Deallocates memory for a single object
delete[] arr; // Deallocates memory for an array of objects
```

Using `new` and `delete` is preferred in C++ over `malloc` and `free` because they handle type safety, constructor/destructor calls, and array size calculations automatically, leading to safer and more manageable code.

### 1. Classes and Objects:

-   **Classes**: Blueprint for creating objects that encapsulate data (attributes) and functions (methods) to operate on that data.
-   **Objects**: Instances of classes that hold data and provide methods to manipulate that data.
-   Example:

```cpp
class Car {
public:
    string brand;
    string model;
    int year;
};

Car myCar; // Creating an object of class Car
myCar.brand = "Toyota";
myCar.model = "Camry";
myCar.year = 2020;
```

### 2. Access Specifiers:

-   **Access Specifiers**: Keywords used to control the access level of members (variables and functions) of a class.
-   Three access specifiers in C++: `public`, `private`, and `protected`.
-   `public`: Members are accessible from outside the class.
-   `private`: Members are accessible only from within the class.
-   `protected`: Members are accessible within the class and its derived classes.
-   Example:

```cpp
class MyClass {
public:
    int publicVar;    // Public member
private:
    int privateVar;   // Private member
protected:
    int protectedVar; // Protected member
};
```

### 3. Overloading:

-   **Function Overloading**: Defining multiple functions with the same name but different parameter lists.
-   **Operator Overloading**: Defining operators for user-defined classes to perform custom operations.
-   Example (Function Overloading):

```cpp
int add(int x, int y) {
    return x + y;
}

double add(double x, double y) {
    return x + y;
}
```

### 4. Inheritance:

-   **Inheritance**: Mechanism where a class (derived class) inherits properties and behavior from another class (base class).
-   Types of inheritance: Single, Multiple, Multilevel, Hierarchical, Hybrid.
-   Example:

```cpp
class Animal {
public:
    void eat() {
        cout << "Eating..." << endl;
    }
};

class Dog : public Animal {
public:
    void bark() {
        cout << "Barking..." << endl;
    }
};
```

### 5. Polymorphism:

-   **Polymorphism**: Ability of objects of different classes to respond to the same message (method call) differently.
-   Achieved through function overloading and virtual functions.
-   Types of polymorphism: Compile-time (Function overloading) and Runtime (Function overriding).
-   Example (Function Overriding):

```cpp
class Animal {
public:
    virtual void makeSound() {
        cout << "Animal sound" << endl;
    }
};

class Dog : public Animal {
public:
    void makeSound() override {
        cout << "Woof!" << endl;
    }
};
```

### 6. Constructors and Destructors:

-   **Constructors**: Special member functions called when an object is created. Used to initialize object's data members.
-   **Destructors**: Special member functions called when an object goes out of scope or is explicitly deleted. Used to release resources held by the object.
-   Example:

```cpp
class MyClass {
public:
    // Constructor
    MyClass() {
        cout << "Constructor called" << endl;
    }
    // Destructor
    ~MyClass() {
        cout << "Destructor called" << endl;
    }
};
```

### 7. Namespaces:

-   **Namespaces**: Feature for organizing code into logical groups and avoiding naming conflicts.
-   Used to prevent naming collisions between different libraries, frameworks, or user-defined identifiers.
-   Example:

```cpp
namespace math {
    const double PI = 3.14;
    double square(double x) {
        return x * x;
    }
}
```

### Constructors:

-   **Constructors** are special member functions of a class that are automatically called when an object of that class is created.
-   They initialize the object's data members.
-   Constructors have the same name as the class and no return type.
-   Example:

```cpp
class Car {
public:
    // Constructor
    Car() {
        cout << "Constructor called" << endl;
    }
};

int main() {
    Car myCar; // Constructor called when object is created
    return 0;
}
```

### Parameterized Constructors:

-   **Parameterized Constructors** accept parameters to initialize the object's data members with specific values.
-   They allow for initialization of objects with different values.
-   Example:

```cpp
class Car {
public:
    string brand;
    // Parameterized Constructor
    Car(string b) {
        brand = b;
        cout << "Constructor called with brand " << brand << endl;
    }
};

int main() {
    Car myCar("Toyota"); // Parameterized constructor called
    return 0;
}
```

### Multiple Constructors in Class:

-   A class can have multiple constructors with different parameter lists.
-   This allows for different ways of initializing objects.
-   Example:

```cpp
class Car {
public:
    string brand;
    int year;
    // Parameterized Constructor
    Car(string b, int y) {
        brand = b;
        year = y;
    }
    // Default Constructor
    Car() {
        brand = "Unknown";
        year = 0;
    }
};

int main() {
    Car myCar1("Toyota", 2020); // Parameterized constructor called
    Car myCar2; // Default constructor called
    return 0;
}
```

### Dynamic Initialization of Objects:

-   Objects can be dynamically initialized using the `new` operator.
-   This allocates memory for the object on the heap.
-   Example:

```cpp
Car *myCar = new Car("Toyota", 2020); // Dynamic initialization of object
delete myCar; // Deallocate memory when object is no longer needed
```

### Copy Constructors:

-   **Copy Constructors** are special constructors used to create a new object as a copy of an existing object.
-   They are called when an object is initialized with another object of the same class.
-   Example:

```cpp
class Car {
public:
    string brand;
    // Copy Constructor
    Car(const Car &otherCar) {
        brand = otherCar.brand;
        cout << "Copy constructor called" << endl;
    }
};

int main() {
    Car myCar1("Toyota");
    Car myCar2 = myCar1; // Copy constructor called
    return 0;
}
```

### Destructors:

-   **Destructors** are special member functions that are called when an object goes out of scope or is explicitly deleted.
-   They release resources held by the object, such as dynamically allocated memory.
-   Destructors have the same name as the class preceded by a tilde (`~`) and no parameters or return type.
-   Example:

```cpp
class Car {
public:
    ~Car() {
        cout << "Destructor called" << endl;
    }
};

int main() {
    Car myCar;
    return 0;
} // Destructor called when myCar goes out of scope
```

**{ } Things to remember about constructors and destructors**

### Constructors:

1.  **Initialization**: Constructors are used to initialize the object's data members.
2.  **Same Name as Class**: Constructors have the same name as the class they belong to.
3.  **No Return Type**: Constructors do not have a return type, not even `void`.
4.  **Automatic Invocation**: Constructors are automatically called when an object is created.
5.  **Multiple Constructors**: A class can have multiple constructors with different parameter lists.
6.  **Initialization Lists**: Constructors can use initialization lists to initialize data members directly.
7.  **Default Constructor**: If no constructor is defined, C++ provides a default constructor that initializes data members to default values.
8.  **Copy Constructor**: Special constructor used to create a new object as a copy of an existing object.
9.  **Inheritance**: Constructors of base classes are called before constructors of derived classes.

### Destructor:

1.  **Cleanup**: Destructors are used to release resources held by the object, such as dynamically allocated memory.
2.  **Same Name as Class with Tilde**: Destructors have the same name as the class, preceded by a tilde (`~`).
3.  **No Parameters or Return Type**: Destructors do not have any parameters or return type, not even `void`.
4.  **Automatic Invocation**: Destructors are automatically called when an object goes out of scope or is explicitly deleted.
5.  **Inheritance**: Destructors of derived classes are called before destructors of base classes.
6.  **Virtual Destructors**: When dealing with polymorphism and dynamic memory allocation, it's recommended to make the destructor virtual to ensure proper cleanup of resources in derived classes.

### Types of Inheritance:

#### 1. Single Inheritance:

-   A derived class inherits from only one base class.
-   It forms a simple parent-child relationship.
-   Example:

```cpp
class Base {
    // Base class members
};

class Derived : public Base {
    // Derived class members
};
```

#### 2. Multiple Inheritance:

-   A derived class inherits from more than one base class.
-   It combines properties and behaviors from multiple parent classes.
-   Example:

```cpp
class Base1 {
    // Base class 1 members
};

class Base2 {
    // Base class 2 members
};

class Derived : public Base1, public Base2 {
    // Derived class members
};
```

#### 3. Multilevel Inheritance:

-   A derived class inherits from another derived class.
-   It forms a hierarchical chain of classes.
-   Example:

```cpp
class Base {
    // Base class members
};

class Intermediate : public Base {
    // Intermediate class members
};

class Derived : public Intermediate {
    // Derived class members
};
```

#### 4. Hierarchical Inheritance:

-   Multiple derived classes inherit from a single base class.
-   It forms a tree-like structure.
-   Example:

```cpp
class Base {
    // Base class members
};

class Derived1 : public Base {
    // Derived class 1 members
};

class Derived2 : public Base {
    // Derived class 2 members
};
```

#### 5. Hybrid Inheritance:

-   Combination of multiple types of inheritance.
-   It can involve any combination of single, multiple, multilevel, or hierarchical inheritance.
-   Example:

```cpp
class Base {
    // Base class members
};

class Derived1 : public Base {
    // Derived class 1 members
};

class Derived2 : public Base, public AnotherBase {
    // Derived class 2 members
};
```

### Virtual Base Class:

Virtual base classes are used in situations where a class is inherited by multiple paths in the inheritance hierarchy, leading to ambiguity and potential issues with duplicate instances of the base class. By declaring a base class as virtual, you ensure that only one instance of that base class exists in the inheritance hierarchy, resolving these issues.

### Example without Virtual Base Class:

Consider the following scenario where the `Base` class is inherited by two derived classes, `Derived1` and `Derived2`:

```cpp
class Base {
public:
    int data;
};

class Derived1 : public Base {
public:
    // Derived1 members
};

class Derived2 : public Base {
public:
    // Derived2 members
};
```

Now, if a class `Derived3` inherits from both `Derived1` and `Derived2`:

```cpp
class Derived3 : public Derived1, public Derived2 {
public:
    // Derived3 members
};
```

The `Derived3` class will have two instances of the `Base` class embedded in its memory layout, one inherited through `Derived1` and the other through `Derived2`. This duplication of base class objects can lead to problems like ambiguity and incorrect behavior when accessing members of the base class.

### Solution with Virtual Base Class:

To avoid such issues, we can declare the `Base` class as virtual in the derived classes:

```cpp
class Derived1 : virtual public Base {
    // Derived1 members
};

class Derived2 : virtual public Base {
    // Derived2 members
};
```

Now, when `Derived3` inherits from both `Derived1` and `Derived2`:

```cpp
class Derived3 : public Derived1, public Derived2 {
    // Derived3 members
};
```

There will be only one shared instance of the `Base` class in the memory layout of `Derived3`, preventing duplication and resolving ambiguity.

### Key Points:

-   Virtual base classes ensure that only one instance of the base class is shared among multiple paths of inheritance.
-   They prevent duplicate instances of the base class and resolve ambiguity in member access.
-   Virtual inheritance is achieved by declaring the base class as `virtual` when inheriting from it in the derived classes.
-   Virtual base classes are particularly useful in diamond inheritance scenarios where a derived class inherits from multiple paths leading to a common base class.

### Constructors in Derived Class:

-   Constructors in derived classes are used to initialize the derived class's data members.
-   They can call the constructor of the base class explicitly using an initialization list.
-   Example:

```cpp
class Base {
public:
    Base(int x) {
        // Base constructor
    }
};

class Derived : public Base {
public:
    Derived(int x, int y) : Base(x) {
        // Derived constructor
    }
};
```

### Types of Polymorphism:

#### 1. Compile-Time Polymorphism:

-   **Function Overloading**: Defining multiple functions with the same name but different parameter lists.
    -   Resolved at compile time based on the number and types of arguments.
-   **Operator Overloading**: Defining custom behavior for operators on user-defined types.
    -   Allows operators to work with objects of user-defined classes.

#### 2. Runtime Polymorphism:

-   **Function Overriding**: Redefining a base class function in a derived class with the same signature.
    -   Resolved at runtime based on the actual object type.
-   **Virtual Functions**: Functions declared in the base class and overridden in derived classes.
    -   Resolved dynamically at runtime based on the object's actual type.
    -   Implemented using dynamic dispatch.

### Overloading Functions:

-   **Function Overloading**: Defining multiple functions with the same name but different parameter lists.
-   Allows a function name to be used for different behaviors depending on the context.
-   Resolved at compile time based on the number and types of arguments.
-   Example:

```cpp
void print(int num) {
    cout << "Integer: " << num << endl;
}

void print(double num) {
    cout << "Double: " << num << endl;
}
```

### Overloading Operators:

-   **Operator Overloading**: Defining custom behavior for operators on user-defined types.
-   Allows operators such as `+`, `-`, `*`, `/` to be used with objects of user-defined classes.
-   Implemented as member functions or global functions.
-   Example:

```cpp
class Complex {
public:
    Complex operator+(const Complex& other) {
        Complex result;
        result.real = this->real + other.real;
        result.imaginary = this->imaginary + other.imaginary;
        return result;
    }
};
```

### Friend Functions:

-   **Friend Functions**: Functions that are not members of a class but have access to its private and protected members.
-   Declared within the class with the `friend` keyword.
-   Useful for operations that require access to private members but don't logically belong to the class.
-   Example:

```cpp
class MyClass {
private:
    int data;
public:
    friend void displayData(const MyClass& obj);
};

void displayData(const MyClass& obj) {
    cout << "Data: " << obj.data << endl;
}
```

### Constant Functions:

-   **Constant Functions**: Member functions declared as `const` that do not modify the object's data members.
-   Can be called on const and non-const objects.
-   Ensures that the member function does not modify the object's state.
-   Example:

```cpp
class MyClass {
public:
    int getData() const {
        return data;
    }
};
```

### Run-Time Polymorphism:

-   **Run-Time Polymorphism**: The ability of a function call to be resolved at runtime rather than compile time.
-   Achieved using virtual functions and inheritance.
-   Allows a base class pointer or reference to point to derived class objects and invoke overridden functions dynamically.
-   Example:

```cpp
class Base {
public:
    virtual void show() {
        cout << "Base class" << endl;
    }
};

class Derived : public Base {
public:
    void show() override {
        cout << "Derived class" << endl;
    }
};

int main() {
    Base *ptr = new Derived(); // Base class pointer pointing to Derived class object
    ptr->show(); // Derived class function is called
    delete ptr;
    return 0;
}
```

### Virtual Functions and Pure Virtual Functions:

-   **Virtual Functions**: Functions declared in a base class and overridden in derived classes.
    -   Can be dynamically bound at runtime based on the object's actual type.
-   **Pure Virtual Functions**: Virtual functions declared in a base class without providing an implementation.
    -   Classes containing pure virtual functions are called abstract classes and cannot be instantiated.
-   Example:

```cpp
class Shape {
public:
    virtual void draw() = 0; // Pure virtual function
};

class Circle : public Shape {
public:
    void draw() override {
        cout << "Drawing a circle" << endl;
    }
};
```

### dynamic_cast, static_cast, const_cast, reinterpret_cast:

-   **dynamic_cast**: Used for performing safe downcasting of pointers/references in polymorphic classes.
    -   Requires the use of virtual functions and RTTI (Run-Time Type Identification).

```cpp
Base *basePtr = new Derived();
Derived *derivedPtr = dynamic_cast<Derived*>(basePtr);
if (derivedPtr) {
    // Downcast successful
    // Use derivedPtr
}
```

-   **static_cast**: Used for static type conversions that do not involve polymorphism.
    -   Performs conversions that the compiler can determine to be safe.

```cpp
#include <iostream>

int main() {
    // Implicit conversion from int to double using static_cast
    int intValue = 10;
    double doubleValue = static_cast<double>(intValue);

    std::cout << "Double Value: " << doubleValue << std::endl;

    return 0;
}
```

-   **const_cast**: Used to add or remove const or volatile qualifiers from pointers/references.

```cpp
#include <iostream>

int main() {
    // Removing constness using const_cast
    const int constValue = 10;
    int *ptr = const_cast<int*>(&constValue);

    *ptr = 20; // Modifying the value pointed by ptr

    std::cout << "Modified Value: " << constValue << std::endl; // Output: Modified Value: 20

    return 0;
}
```

-   **reinterpret_cast**: Used for low-level casting between pointer types, such as casting between unrelated pointer types.

```cpp
#include <iostream>

int main() {
    // Reinterpreting pointer types using reinterpret_cast
    int intValue = 10;
    int* ptr = &intValue;
    char* charPtr = reinterpret_cast<char*>(ptr);

    std::cout << "Value at charPtr: " << *charPtr << std::endl; // Output depends on system's byte order

    return 0;
}
```


**[ ] Interfaces vs Abstract class :**

### Interfaces:

1.  **Definition**:
    1.  **Interfaces** define a contract specifying a set of methods that a class must implement. They focus on what a class can do, not how it does it.
    2.  Interfaces contain only method signatures (declarations), without any method implementations.
2.  **Usage**:
    1.  Interfaces are used to define a common set of behaviors that multiple classes can implement.
    2.  They provide a way to achieve abstraction and polymorphism, allowing objects of different classes to be treated uniformly.
3.  **Implementation**:
    1.  In C++, interfaces are typically implemented using abstract classes with pure virtual functions.
    2.  Classes that implement an interface must provide definitions for all the methods declared in the interface.
4.  **Instantiation**:
    1.  Interfaces cannot be instantiated directly. They serve as a blueprint for classes that implement them.
5.  **Example**:

```cpp
class Printable {
public:
    virtual void print() const = 0; // Pure virtual function
};
```

### Abstract Classes:

1.  **Definition**:
    1.  **Abstract Classes** are classes that cannot be instantiated and may contain one or more pure virtual functions.
    2.  They may also include concrete methods (with implementations) and member variables.
2.  **Usage**:
    1.  Abstract classes provide a partial implementation of a class, leaving some methods to be implemented by derived classes.
    2.  They are used to define a common interface and behavior for a group of related classes.
3.  **Implementation**:
    1.  Abstract classes may contain both pure virtual functions and concrete methods.
    2.  Derived classes must provide implementations for all pure virtual functions to become concrete classes.
4.  **Instantiation**:
    1.  Abstract classes cannot be instantiated directly. They serve as a blueprint for derived classes.
5.  **Example**:

```cpp
class Shape {
public:
    virtual double area() const = 0; // Pure virtual function
    virtual double perimeter() const = 0; // Pure virtual function

    // Concrete method
    void display() const {
        cout << "Displaying shape." << endl;
    }
};
```

### Summary:

-   **Interfaces** focus on defining a contract for classes without any implementation details.
-   **Abstract classes** provide a partial implementation with some methods left to be implemented by derived classes.
-   Both interfaces and abstract classes promote code reuse, abstraction, and polymorphism, but they have different use cases and implementation details.

### 

### Exception Handling Introduction:

1.  **Throwing Exceptions**:
    1.  Use the `throw` keyword to raise an exception when an error occurs.
    2.  You can throw any data type as an exception, but it's common to use standard or custom exception classes.
    3.  Example:

```cpp
throw runtime_error("Division by zero error");
```

1.  **Catching Exceptions**:
    1.  Use `try`, `catch` blocks to handle exceptions.
    2.  The `try` block encloses the code that may throw an exception, and the `catch` block handles the exception.
    3.  Multiple `catch` blocks can be used to handle different types of exceptions.
    4.  Example:

```cpp
try {
    // Code that may throw an exception
}
catch (const std::exception& e) {
    // Handle exception
    std::cerr << "Exception caught: " << e.what() << std::endl;
}
```

1.  **Rethrowing Exceptions**:
    1.  You can rethrow an exception within a `catch` block to propagate it to an outer scope.
    2.  Allows higher-level code to handle the exception or log the error.
    3.  Example:

```cpp
try {
    // Code that may throw an exception
}
catch (const std::exception& e) {
    // Handle exception
    // Rethrow the exception
    throw;
}
```

1.  **Specifying Exceptions**:
    1.  Functions can specify the types of exceptions they may throw using the `throw` keyword in the function declaration.
    2.  Helps callers understand potential error conditions and handle them appropriately.
    3.  Example:

```cpp
void foo() throw(std::runtime_error) {
    // Function body
}
```


**[ ] Managing Console I/O Operations in C++ :**

### Introduction:

-   Console I/O operations involve reading input from the user and displaying output on the console.
-   Proper management of console I/O is essential for creating interactive and user-friendly applications.

### C++ Streams:

-   **Streams** are sequences of characters flowing into or out of a program.
-   In C++, input and output operations are performed using streams, which are represented by objects of stream classes.
-   Streams provide a convenient and uniform way of handling different types of I/O devices, such as the console, files, and network sockets.

### C++ Stream Classes:

-   C++ provides several stream classes, such as `iostream`, `ifstream`, `ofstream`, and `stringstream`, for input and output operations.
-   `iostream` is used for console input and output.
-   `ifstream` and `ofstream` are used for file input and output, respectively.
-   `stringstream` allows manipulation of strings as streams.

### Unformatted I/O Operations:

-   **Unformatted I/O operations** involve reading or writing data without any specific formatting.
-   Functions like `get()`, `put()`, `getline()`, `write()`, etc., are used for unformatted I/O operations.
-   Unformatted input reads characters as they are, without any interpretation of their meaning.

### Formatted I/O Operations:

-   **Formatted I/O operations** involve reading or writing data with specific formatting rules.
-   Functions like `>>` (extraction operator) and `<<` (insertion operator) are used for formatted input and output.
-   Formatted output allows the programmer to control the appearance of the output data, such as specifying field widths, precision, etc.

### Managing Output with Manipulators:

-   **Manipulators** are special functions or objects used to modify the behavior of output streams.
-   They are used with the insertion operator (`<<`) to control formatting and other aspects of output.
-   Common manipulators include `setw()`, `setprecision()`, `setfill()`, `endl`, `setw()`, `left`, `right`, etc.
-   Manipulators provide flexibility in formatting output according to specific requirements.

{ } examples for each concept:

### Unformatted I/O Operations:

#### Reading Input:

```cpp
#include <iostream>
#include <string>

int main() {
    std::string name;
    std::cout << "Enter your name: ";
    std::getline(std::cin, name); // Unformatted input with getline
    std::cout << "Hello, " << name << "!" << std::endl;
    return 0;
}
```

#### Writing Output:

```cpp
#include <iostream>

int main() {
    int num = 42;
    char ch = 'A';
    std::cout.put(ch); // Unformatted output with put
    std::cout << " " << num << std::endl;
    return 0;
}
```

### Formatted I/O Operations:

#### Formatted Input:

```cpp
#include <iostream>

int main() {
    int num;
    std::cout << "Enter a number: ";
    std::cin >> num; // Formatted input with >>
    std::cout << "You entered: " << num << std::endl;
    return 0;
}
```

#### Formatted Output:

```cpp
#include <iostream>
#include <iomanip>

int main() {
    double pi = 3.14159265359;
    std::cout << "Value of pi: " << std::fixed << std::setprecision(2) << pi << std::endl; // Formatted output with precision
    return 0;
}
```

### Managing Output with Manipulators:

```cpp
#include <iostream>
#include <iomanip>

int main() {
    int width = 10;
    int num = 42;
    std::cout << std::setw(width) << std::left << num << std::endl; // Using setw() and left manipulators
    return 0;
}
```

In this example, `setw(width)` sets the field width to 10 characters, and `left` aligns the output to the left within that field width.

Let's dive into file handling in C++:

### Definition of File:

-   A **file** is a collection of data stored on a storage device, such as a hard disk, SSD, or flash drive.
-   Files can contain various types of data, including text, images, audio, video, and binary data.
-   In C++, files are typically accessed and manipulated using file streams.

### File Handling in C++:

-   **File handling** in C++ involves performing operations like reading from and writing to files.
-   C++ provides the `<fstream>` header for file input/output operations.
-   File handling in C++ is done through file stream objects like `ifstream` (for reading from files), `ofstream` (for writing to files), and `fstream` (for both reading and writing).

### Performing Read and Write Operations in Files:

#### Writing to a File:

```cpp
#include <iostream>
#include <fstream>

int main() {
    std::ofstream outfile("example.txt"); // Open file for writing
    if (outfile.is_open()) {
        outfile << "Hello, World!" << std::endl; // Write data to file
        outfile.close(); // Close the file
        std::cout << "Data written to file successfully." << std::endl;
    } else {
        std::cerr << "Unable to open file for writing." << std::endl;
    }
    return 0;
}
```

#### Reading from a File:

```cpp
#include <iostream>
#include <fstream>
#include <string>

int main() {
    std::ifstream infile("example.txt"); // Open file for reading
    if (infile.is_open()) {
        std::string line;
        while (std::getline(infile, line)) { // Read file line by line
            std::cout << line << std::endl; // Print each line
        }
        infile.close(); // Close the file
    } else {
        std::cerr << "Unable to open file for reading." << std::endl;
    }
    return 0;
}
```

In these examples:

-   `ofstream` is used to open a file for writing (`"example.txt"`).
-   `ifstream` is used to open a file for reading (`"example.txt"`).
-   Data is written to the file using the insertion operator (`<<`) or read from the file using `getline()`.

File handling in C++ allows you to store and retrieve data persistently, making it useful for applications that need to store and retrieve data across multiple program runs. Remember to handle file open/close operations and error conditions appropriately for robust file handling.

### Introduction to Templates:

-   **Templates** in C++ are a powerful feature that allows you to write generic code.
-   They enable you to define functions and classes with placeholder types that can be instantiated with any data type.
-   Templates facilitate code reuse and provide a way to write flexible and efficient code.

### Function Templates:

-   **Function Templates** allow you to define a generic function that can operate on different data types.
-   The function template is defined using the `template` keyword followed by the template parameter list.
-   Inside the function template, you can use the template parameter to represent the data type.
-   Example:

```cpp
template <typename T>
T add(T a, T b) {
    return a + b;
}
```

### Class Templates:

-   **Class Templates** enable you to define a generic class that can work with different data types.
-   The class template is defined similarly to function templates, using the `template` keyword followed by the template parameter list.
-   Inside the class template, you can use the template parameter to define member variables, member functions, and nested classes.
-   Example:

```cpp
template <typename T>
class Stack {
private:
    std::vector<T> elements;
public:
    void push(const T& element) {
        elements.push_back(element);
    }
    // Other member functions...
};
```

Templates provide a way to write reusable code that can work with different data types without sacrificing type safety or performance. They are widely used in modern C++ programming to implement data structures, algorithms, and libraries.



**[ ] Standard Library and then move on to Run-Time Type Information (RTTI):**

### Introduction to C++ Standard Library (STL):

The C++ Standard Library, often referred to as the Standard Template Library (STL), is a collection of classes and functions that provide common programming data structures and algorithms. It is part of the C++ language specification and is available in all conforming C++ compilers. The STL consists of several components:

1.  **Containers**: Classes that store collections of objects. Examples include vectors, lists, sets, maps, and queues.
2.  **Algorithms**: Functions that operate on containers to perform various operations, such as sorting, searching, and modifying elements.
3.  **Iterators**: Objects that provide a way to traverse the elements of a container sequentially. They generalize pointers and allow algorithms to work with different types of containers.
4.  **Function Objects (Functors)**: Objects that behave like functions and can be used as arguments to algorithms. They provide more flexibility than regular functions.
5.  **Iterators Adapters**: Utilities that adapt iterators to provide additional functionality. Examples include `reverse_iterator`, `move_iterator`, and `istream_iterator`.
6.  **Utilities**: Miscellaneous utilities such as `pair` (a simple container holding two values), `tuple` (a container holding multiple values of different types), and `smart pointers` (classes that manage dynamically allocated memory).

### Introduction to Run-Time Type Information (RTTI) in C++:

Run-Time Type Information (RTTI) is a mechanism in C++ that provides information about the data type of objects at runtime. It allows you to determine the actual type of an object and perform type-safe operations accordingly. RTTI consists of two main components:

1.  `typeid` **Operator**:
    1.  The `typeid` operator allows you to determine the dynamic type of an object at runtime.
    2.  It returns a reference to a `type_info` object, which contains information about the type of the expression.
    3.  Example:

```cpp
class Base {
public:
    virtual ~Base() {}
};
class Derived : public Base {};

int main() {
    Base* ptr = new Derived();
    if (typeid(*ptr) == typeid(Derived)) {
        std::cout << "ptr points to a Derived object." << std::endl;
    }
    delete ptr;
    return 0;
}
```

1.  `dynamic_cast` **Operator**:
    1.  The `dynamic_cast` operator is used to perform safe downcasting of pointers or references to derived classes.
    2.  It checks the validity of the conversion at runtime and returns a pointer or reference to the target type if successful, or `nullptr` if the conversion is not possible.
    3.  Example:

```cpp
class Base {
public:
    virtual ~Base() {}
};
class Derived : public Base {};

int main() {
    Base* basePtr = new Derived();
    Derived* derivedPtr = dynamic_cast<Derived*>(basePtr);
    if (derivedPtr) {
        std::cout << "Dynamic cast successful." << std::endl;
    }
    delete basePtr;
    return 0;
}
```

RTTI provides a powerful mechanism for writing flexible and type-safe code in C++, especially in situations where the exact type of objects is not known at compile time. However, it should be used judiciously as it incurs some runtime overhead and may not be needed in all scenarios.

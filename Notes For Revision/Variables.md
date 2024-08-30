
### Java Basics: Comprehensive Notes

---

#### **1. Introduction to Java**
Java is a high-level, class-based, object-oriented programming language designed to have as few implementation dependencies as possible. It is intended to let application developers write once, run anywhere (WORA), meaning that compiled Java code can run on all platforms that support Java without the need for recompilation.

**Key Characteristics:**
- **Platform Independence:** Java code is compiled into bytecode, which can run on any platform using the Java Virtual Machine (JVM).
- **Object-Oriented:** Everything in Java is an object which encapsulates data and behavior.
- **Robust and Secure:** Java has strong memory management, exception handling, and security features.
- **Multithreaded:** Java allows you to perform many tasks simultaneously, making your applications more efficient.
- **Portable:** The same Java program can run on different types of hardware without modification.

---

#### **2. Setting Up the Java Environment**
To start coding in Java, you need to set up your environment by installing the Java Development Kit (JDK) and a suitable Integrated Development Environment (IDE).

**Steps:**
- **Download and Install JDK:** Visit the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) and download the latest version of the JDK.
- **Set Up Path:** After installation, set the `JAVA_HOME` environment variable and update the `PATH` variable to include the path to the JDK bin directory.
- **Install an IDE:** Popular IDEs include IntelliJ IDEA, Eclipse, and NetBeans. You can also use text editors like VSCode with appropriate plugins.

---

#### **3. Basic Syntax and Structure**
Java programs are written in classes, which are the building blocks of Java applications. Here’s a basic structure of a Java program:

```java
// A simple Java program
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");  // Prints "Hello, World!" to the console
    }
}
```

**Key Points:**
- **Class Declaration:** Every Java application must have at least one class definition.
- **Main Method:** The entry point of any Java application. It has the signature `public static void main(String[] args)`.
- **System.out.println:** A method used to print text to the console.

---

#### **4. Data Types and Variables**
Java is a statically typed language, which means you must declare a variable's type before using it. 

**Primitive Data Types:**
- **byte:** 8-bit integer. `byte age = 30;`
- **short:** 16-bit integer. `short temperature = 5000;`
- **int:** 32-bit integer. `int salary = 50000;`
- **long:** 64-bit integer. `long distance = 123456789L;`
- **float:** 32-bit floating point. `float price = 10.99f;`
- **double:** 64-bit floating point. `double pi = 3.14159;`
- **char:** 16-bit Unicode character. `char grade = 'A';`
- **boolean:** Represents true or false. `boolean isJavaFun = true;`

**Non-Primitive Data Types:**
- **Strings:** Represents sequences of characters. `String name = "Vrinda";`
- **Arrays:** Holds multiple values of the same type. `int[] numbers = {1, 2, 3, 4};`

**Variable Declaration:**
```java
int number = 10;  // Declare an integer variable
String name = "John";  // Declare a string variable
```

---

#### **5. Operators in Java**
Operators are special symbols that perform operations on variables and values.

**Types of Operators:**
- **Arithmetic Operators:** `+`, `-`, `*`, `/`, `%`
- **Relational Operators:** `==`, `!=`, `>`, `<`, `>=`, `<=`
- **Logical Operators:** `&&`, `||`, `!`
- **Assignment Operators:** `=`, `+=`, `-=`, `*=`, `/=`
- **Unary Operators:** `++`, `--`
- **Bitwise Operators:** `&`, `|`, `^`, `~`, `<<`, `>>`

**Examples:**
```java
int a = 5, b = 10;
int sum = a + b;  // sum is 15
boolean isEqual = (a == b);  // isEqual is false
```

---

#### **6. Control Flow Statements**
Control flow statements determine the order in which statements are executed.

**Conditional Statements:**
- **if Statement:**
    ```java
    if (condition) {
        // Code to execute if condition is true
    }
    ```
- **if-else Statement:**
    ```java
    if (condition) {
        // Code to execute if condition is true
    } else {
        // Code to execute if condition is false
    }
    ```
- **else-if Ladder:**
    ```java
    if (condition1) {
        // Code to execute if condition1 is true
    } else if (condition2) {
        // Code to execute if condition2 is true
    } else {
        // Code to execute if both conditions are false
    }
    ```
- **switch Statement:**
    ```java
    switch (variable) {
        case value1:
            // Code for case 1
            break;
        case value2:
            // Code for case 2
            break;
        default:
            // Default case
            break;
    }
    ```

**Looping Statements:**
- **for Loop:**
    ```java
    for (int i = 0; i < 5; i++) {
        System.out.println(i);
    }
    ```
- **while Loop:**
    ```java
    int i = 0;
    while (i < 5) {
        System.out.println(i);
        i++;
    }
    ```
- **do-while Loop:**
    ```java
    int i = 0;
    do {
        System.out.println(i);
        i++;
    } while (i < 5);
    ```

**Break and Continue:**
- **break:** Exits the loop prematurely.
- **continue:** Skips the current iteration and continues with the next.

---

#### **7. Object-Oriented Programming (OOP) Concepts**
Java is an object-oriented language, and understanding OOP is crucial.

**Core OOP Concepts:**
- **Class and Object:** A class is a blueprint for objects. An object is an instance of a class.
    ```java
    class Dog {
        String name;
        int age;

        void bark() {
            System.out.println("Woof!");
        }
    }

    public class Main {
        public static void main(String[] args) {
            Dog myDog = new Dog();  // Create an object of Dog
            myDog.name = "Buddy";   // Access object properties
            myDog.bark();           // Call object methods
        }
    }
    ```
- **Encapsulation:** Bundling data (variables) and methods that operate on the data into a single unit (class), and restricting access to some of the object's components.
    ```java
    class Person {
        private String name;
        
        public String getName() {
            return name;
        }
        
        public void setName(String name) {
            this.name = name;
        }
    }
    ```
- **Inheritance:** Mechanism where one class inherits the properties and behavior of another class.
    ```java
    class Animal {
        void eat() {
            System.out.println("Eating...");
        }
    }

    class Dog extends Animal {
        void bark() {
            System.out.println("Barking...");
        }
    }
    ```
- **Polymorphism:** Ability to present the same interface for different data types.
    ```java
    class Animal {
        void sound() {
            System.out.println("Animal is making a sound");
        }
    }

    class Dog extends Animal {
        void sound() {
            System.out.println("Dog is barking");
        }
    }
    ```
- **Abstraction:** Hiding complex implementation details and showing only the essential features.
    ```java
    abstract class Animal {
        abstract void sound();  // Abstract method
    }

    class Dog extends Animal {
        void sound() {
            System.out.println("Barking...");
        }
    }
    ```

---

#### **8. Exception Handling**
Exceptions are events that occur during the execution of a program that disrupt the normal flow of instructions.

**Types of Exceptions:**
- **Checked Exceptions:** Exceptions that are checked at compile time (e.g., IOException).
- **Unchecked Exceptions:** Exceptions that are not checked at compile time (e.g., ArithmeticException, NullPointerException).

**Handling Exceptions:**
- **try-catch Block:**
    ```java
    try {
        // Code that might throw an exception
    } catch (ExceptionType e) {
        // Code to handle the exception
    }
    ```
- **finally Block:** Code that is always executed after the try-catch block, regardless of whether an exception was thrown.
    ```java
    try {
        // Code that might throw an exception
    } catch (ExceptionType e) {
        // Code to handle the exception
    } finally {
        // Code that will always run
    }
    ```
- **throw Statement:** Used to throw an exception manually.
    ```java
    throw new ArithmeticException("Cannot divide by zero");
    ```

---

#### **9. Java Standard Library (Java API)**
Java provides a rich set of pre-built classes and interfaces grouped

 into packages, which you can reuse in your applications.

**Commonly Used Packages:**
- **java.lang:** Contains fundamental classes like `String`, `Math`, `Integer`, etc.
- **java.util:** Provides utility classes such as `ArrayList`, `HashMap`, `Date`, etc.
- **java.io:** Classes for system input and output through data streams, serialization, and file system manipulation.
- **java.net:** Classes for networking applications (e.g., `Socket`, `URL`).
- **java.nio:** Non-blocking I/O classes, used for file and network operations.

---

#### **10. Basic Input and Output (I/O)**
Java provides several ways to read input from the user and display output.

**Console Input:**
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);  // Create a Scanner object
        System.out.print("Enter your name: ");
        String name = scanner.nextLine();  // Read user input
        System.out.println("Hello, " + name);  // Output user input
    }
}
```

**File I/O:**
```java
import java.io.File;
import java.io.FileWriter;
import java.io.IOException;

public class FileExample {
    public static void main(String[] args) {
        try {
            File file = new File("filename.txt");  // Create a File object
            if (file.createNewFile()) {
                System.out.println("File created: " + file.getName());
            } else {
                System.out.println("File already exists.");
            }
            
            FileWriter writer = new FileWriter("filename.txt");  // Write to the file
            writer.write("Hello, World!");
            writer.close();
        } catch (IOException e) {
            System.out.println("An error occurred.");
            e.printStackTrace();
        }
    }
}
```

---

#### **11. Java Memory Management**
Java memory management is handled by the JVM through a process called garbage collection, which automatically frees up memory that is no longer in use.

**Heap and Stack:**
- **Heap:** Stores objects created by `new`.
- **Stack:** Stores primitive data types and references to objects.

**Garbage Collection:**
- **Automatic Process:** JVM automatically removes objects that are no longer referenced to free up memory.
- **No Explicit Freeing:** Unlike languages like C++, you don’t need to explicitly free memory.

---

#### **12. Java Development Best Practices**
- **Follow Naming Conventions:** Use camelCase for variables and methods, PascalCase for class names, and UPPER_SNAKE_CASE for constants.
- **Use Comments:** Provide meaningful comments to explain complex logic.
- **Organize Code:** Group related code into methods and classes. Use packages to organize related classes.
- **Avoid Hardcoding Values:** Use constants or configuration files for values that might change.
- **Write Unit Tests:** Ensure your code is tested using frameworks like JUnit.

---
---
### Variables in Java: Comprehensive Notes

---

#### **1. What is a Variable?**
A variable in Java is a container that holds data that can be used and manipulated within a program. Think of a variable as a name associated with a space in the computer's memory where information is stored.

**Key Characteristics:**
- **Data Storage:** Variables store data values that can be used in computations.
- **Mutable:** The value of a variable can change during the execution of a program.
- **Typed:** Variables in Java must be declared with a specific data type, which defines the kind of data it can store.

---

#### **2. Variable Declaration and Initialization**
In Java, before using a variable, you must declare it by specifying its type and name. You can also initialize the variable with a value when you declare it.

**Syntax:**
```java
type variableName;  // Declaration
variableName = value;  // Initialization

// Or both in one line:
type variableName = value;
```

**Examples:**
```java
int age;  // Declaration
age = 25;  // Initialization

// Declaration and initialization in one step
int year = 2024;
```

---

#### **3. Data Types of Variables**
Java is a statically typed language, meaning each variable must be declared with a data type. The data type determines what kind of data the variable can hold.

**Primitive Data Types:**
- **byte:** 8-bit integer (`byte b = 10;`)
- **short:** 16-bit integer (`short s = 20;`)
- **int:** 32-bit integer (`int i = 100;`)
- **long:** 64-bit integer (`long l = 1000L;`)
- **float:** 32-bit floating-point (`float f = 10.5f;`)
- **double:** 64-bit floating-point (`double d = 99.99;`)
- **char:** 16-bit Unicode character (`char c = 'A';`)
- **boolean:** Represents true or false (`boolean b = true;`)

**Non-Primitive Data Types:**
- **String:** Represents a sequence of characters (`String name = "Vrinda";`)
- **Array:** A collection of elements of the same type (`int[] numbers = {1, 2, 3};`)
- **Classes, Interfaces, Enums:** Custom data types defined by the programmer.

---

#### **4. Types of Variables in Java**
Java variables are categorized based on their scope and lifetime.

**1. Local Variables:**
- **Definition:** Declared inside a method, constructor, or block.
- **Scope:** Accessible only within the method, constructor, or block where it is declared.
- **Lifetime:** Exists only during the execution of the method, constructor, or block.
- **Initialization:** Must be initialized before use.

**Example:**
```java
public void calculateSum() {
    int num1 = 5;  // Local variable
    int num2 = 10;  // Local variable
    int sum = num1 + num2;
    System.out.println(sum);
}
```

**2. Instance Variables:**
- **Definition:** Declared inside a class but outside any method, constructor, or block.
- **Scope:** Accessible throughout the class.
- **Lifetime:** Exists as long as the object of the class exists.
- **Initialization:** Initialized to default values (0, null, false) if not explicitly initialized.

**Example:**
```java
public class Dog {
    String breed;  // Instance variable
    int age;       // Instance variable

    public void display() {
        System.out.println("Breed: " + breed);
        System.out.println("Age: " + age);
    }
}
```

**3. Static Variables (Class Variables):**
- **Definition:** Declared inside a class with the `static` keyword.
- **Scope:** Shared among all instances of the class.
- **Lifetime:** Exists as long as the class is loaded into memory.
- **Initialization:** Initialized to default values if not explicitly initialized.

**Example:**
```java
public class Car {
    static int wheels = 4;  // Static variable

    public void displayWheels() {
        System.out.println("Number of wheels: " + wheels);
    }
}
```

---

#### **5. Variable Naming Conventions**
In Java, variable names should follow specific conventions to improve code readability and maintainability.

**Rules:**
- **Case Sensitivity:** Variable names are case-sensitive (`age` and `Age` are different).
- **Start with a Letter or Underscore:** Variable names must begin with a letter (a-z, A-Z) or an underscore (_), but not a number.
- **No Special Characters:** Variable names cannot contain special characters like `!`, `@`, `#`, etc., except for `_`.
- **Avoid Reserved Words:** Do not use Java reserved words (e.g., `int`, `class`, `static`) as variable names.

**Best Practices:**
- **Use Meaningful Names:** Choose names that clearly describe the variable's purpose (`totalAmount`, `customerName`).
- **Camel Case for Multi-Word Names:** Start the first word in lowercase and capitalize subsequent words (`firstName`, `accountBalance`).

**Examples:**
```java
int totalCost;
String firstName;
boolean isActive;
```

---

#### **6. Default Values of Variables**
Variables in Java have default values if not explicitly initialized, but this only applies to instance and static variables. Local variables must be initialized before use.

**Default Values:**
- **byte, short, int, long:** `0`
- **float, double:** `0.0`
- **char:** `\u0000` (null character)
- **boolean:** `false`
- **Reference Types (e.g., String, Arrays):** `null`

**Example:**
```java
public class Example {
    int number;       // Default value is 0
    boolean isActive; // Default value is false
    String name;      // Default value is null

    public void display() {
        System.out.println("Number: " + number);
        System.out.println("Is Active: " + isActive);
        System.out.println("Name: " + name);
    }
}
```

---

#### **7. Variable Scope**
The scope of a variable determines where it can be accessed in the code.

**Types of Scope:**
- **Method Scope (Local Scope):** Variables declared within a method are only accessible within that method.
- **Class Scope (Instance and Static Variables):** Variables declared within a class are accessible to all methods of that class, but instance variables require an object to be accessed.

**Example:**
```java
public class ScopeExample {
    int instanceVar = 5;  // Class scope (instance variable)

    public void methodOne() {
        int localVar = 10;  // Method scope (local variable)
        System.out.println("Instance Var: " + instanceVar);
        System.out.println("Local Var: " + localVar);
    }

    public void methodTwo() {
        System.out.println("Instance Var: " + instanceVar);
        // System.out.println("Local Var: " + localVar);  // Error: localVar is not accessible here
    }
}
```

---

#### **8. Variable Lifespan**
The lifespan of a variable refers to the duration for which the variable exists in memory during program execution.

- **Local Variables:** Lifespan is limited to the method/block where they are declared. They are created when the method is called and destroyed when the method finishes execution.
- **Instance Variables:** Lifespan is tied to the object they belong to. They exist as long as the object exists.
- **Static Variables:** Lifespan is tied to the class. They exist as long as the class is loaded in memory.

**Example:**
```java
public class LifespanExample {
    static int staticVar = 100;  // Lifespan: Until class is unloaded
    int instanceVar = 50;  // Lifespan: Until object is destroyed

    public void display() {
        int localVar = 25;  // Lifespan: Until method finishes execution
        System.out.println("Local Var: " + localVar);
    }
}
```

---

#### **9. Constant Variables (final keyword)**
In Java, if you want a variable to be constant and not changeable after its initial assignment, you use the `final` keyword.

**Key Points:**
- **Once Assigned, Cannot be Modified:** The value of a final variable cannot be changed once it’s assigned.
- **Naming Convention:** Constants are usually named using uppercase letters with underscores separating words (`MAX_SIZE`, `PI`).

**Example:**
```java
public class Constants {
    final int MAX_SPEED = 120;  // Constant variable
    final double PI = 3.14159;  // Constant variable

    public void display() {
        System.out.println("Max Speed: " + MAX_SPEED);
        System.out.println("Value of PI: " + PI);
    }
}
```

---

#### **10. Type Casting of Variables**
Type casting is the process of converting one data type into another. Java supports two types of casting:

**1. Implicit (Widening) Casting:**
- Automatic conversion from a smaller to a larger type.
- Safe as there is no loss of data.

**Example:**
```java
int num = 100;
double doubleNum = num;  // int to double (widening)
```

**2. Explicit (Narrowing) Casting:**
- Manually converting from a larger to a smaller type.
- Risky as it may lead to loss of data



.

**Example:**
```java
double doubleNum = 9.78;
int intNum = (int) doubleNum;  // double to int (narrowing)
```

---


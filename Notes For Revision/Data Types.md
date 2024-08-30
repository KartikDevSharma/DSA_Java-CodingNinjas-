### Data Types in Java: Comprehensive Notes

---

#### **1. What are Data Types?**
Data types in Java define the type of data a variable can hold. They determine the size of memory allocated for the variable and the operations that can be performed on it. Java is a statically typed language, meaning each variable must be declared with a data type before it is used.

**Categories of Data Types:**
- **Primitive Data Types:** Built-in data types that hold simple values.
- **Non-Primitive Data Types:** Reference types that are created by the programmer.

---

#### **2. Primitive Data Types**
Java provides eight built-in data types that are categorized as primitive. These are the most basic data types available in Java.

**1. Integer Data Types:**
- **byte:**
  - **Size:** 8 bits
  - **Range:** -128 to 127
  - **Usage:** Useful for saving memory in large arrays where the memory savings are most needed.
  - **Example:** `byte b = 100;`

- **short:**
  - **Size:** 16 bits
  - **Range:** -32,768 to 32,767
  - **Usage:** Can be used to save memory, like `byte`. Slightly larger range than `byte`.
  - **Example:** `short s = 10000;`

- **int:**
  - **Size:** 32 bits
  - **Range:** -2^31 to 2^31 - 1
  - **Usage:** The most commonly used integer type.
  - **Example:** `int i = 100000;`

- **long:**
  - **Size:** 64 bits
  - **Range:** -2^63 to 2^63 - 1
  - **Usage:** Used when a wider range than `int` is needed.
  - **Example:** `long l = 100000L;`
  - **Note:** The suffix `L` or `l` is used to indicate a `long` literal.

**2. Floating-Point Data Types:**
- **float:**
  - **Size:** 32 bits
  - **Range:** Approximately ±3.40282347E+38F (6-7 significant decimal digits)
  - **Usage:** Used to save memory in large arrays of floating-point numbers.
  - **Example:** `float f = 10.5f;`
  - **Note:** The suffix `f` or `F` is used to indicate a `float` literal.

- **double:**
  - **Size:** 64 bits
  - **Range:** Approximately ±1.79769313486231570E+308 (15 significant decimal digits)
  - **Usage:** Default data type for decimal values, generally the default choice for floating-point calculations.
  - **Example:** `double d = 99.99;`

**3. Character Data Type:**
- **char:**
  - **Size:** 16 bits (Unicode character)
  - **Range:** `\u0000` to `\uffff` (0 to 65,535 in unsigned int)
  - **Usage:** Used to store a single character.
  - **Example:** `char c = 'A';`

**4. Boolean Data Type:**
- **boolean:**
  - **Size:** 1 bit (but JVM may use more space depending on the system)
  - **Values:** `true` or `false`
  - **Usage:** Used for simple flags that track true/false conditions.
  - **Example:** `boolean isJavaFun = true;`

---

#### **3. Non-Primitive Data Types**
Non-primitive data types, also known as reference types, are more complex than primitive data types. These include classes, arrays, and interfaces. Non-primitive types are created by the programmer and can be used to call methods to perform operations.

**Key Points:**
- **Memory Location:** Non-primitive types reference a memory location where the actual data is stored, not the actual data value.
- **Default Value:** The default value of any reference variable is `null`.
- **Size:** The size of reference types is not fixed and depends on the JVM.

**1. Strings:**
- **Definition:** A sequence of characters.
- **Usage:** Strings are used to store text.
- **Example:** `String greeting = "Hello, World!";`

**2. Arrays:**
- **Definition:** A collection of elements, all of the same type.
- **Usage:** Arrays are used to store multiple values in a single variable.
- **Example:** `int[] numbers = {1, 2, 3, 4, 5};`

**3. Classes:**
- **Definition:** A blueprint from which objects are created.
- **Usage:** Classes are used to define new data types and methods.
- **Example:**
  ```java
  public class Dog {
      String breed;
      int age;

      void bark() {
          System.out.println("Woof!");
      }
  }
  ```

**4. Interfaces:**
- **Definition:** A reference type in Java, similar to a class, that can contain only constants, method signatures, default methods, static methods, and nested types.
- **Usage:** Interfaces are used to achieve abstraction and multiple inheritance in Java.
- **Example:**
  ```java
  interface Animal {
      void eat();
      void sleep();
  }
  ```

**5. Enums:**
- **Definition:** A special data type that enables a variable to be a set of predefined constants.
- **Usage:** Enums are used when a variable can only take one out of a small set of possible values.
- **Example:**
  ```java
  enum Day {
      SUNDAY, MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, SATURDAY
  }
  ```

---

#### **4. Type Conversion**
Type conversion in Java refers to changing a variable from one data type to another.

**1. Implicit Type Conversion (Widening):**
- **Definition:** Automatic conversion of a smaller data type to a larger one.
- **Safe Conversion:** No data loss occurs.
- **Example:** `int to long`, `float to double`
- **Example:**
  ```java
  int num = 100;
  double doubleNum = num;  // int to double
  ```

**2. Explicit Type Conversion (Narrowing):**
- **Definition:** Manually converting a larger data type to a smaller one.
- **Possible Data Loss:** May lead to loss of data.
- **Syntax:** Use the cast operator `(type)`
- **Example:** `double to int`, `long to int`
- **Example:**
  ```java
  double doubleNum = 9.78;
  int intNum = (int) doubleNum;  // Explicit cast
  ```

---

#### **5. Wrapper Classes**
Wrapper classes provide a way to use primitive data types as objects. Each primitive data type has a corresponding wrapper class in Java.

**1. Autoboxing:**
- **Definition:** Automatic conversion of a primitive data type into its corresponding wrapper class.
- **Example:**
  ```java
  int num = 10;
  Integer numObj = num;  // Autoboxing
  ```

**2. Unboxing:**
- **Definition:** Automatic conversion of a wrapper class object back to its corresponding primitive data type.
- **Example:**
  ```java
  Integer numObj = 10;
  int num = numObj;  // Unboxing
  ```

**Common Wrapper Classes:**
- **byte:** `Byte`
- **short:** `Short`
- **int:** `Integer`
- **long:** `Long`
- **float:** `Float`
- **double:** `Double`
- **char:** `Character`
- **boolean:** `Boolean`

---

#### **6. Default Values of Data Types**
When variables are declared but not initialized, Java assigns them default values. This only applies to instance variables and static variables; local variables must be initialized before use.

**Default Values:**
- **byte, short, int, long:** `0`
- **float, double:** `0.0`
- **char:** `\u0000` (null character)
- **boolean:** `false`
- **Object references (e.g., String, Arrays):** `null`

**Example:**
```java
public class Example {
    int number;       // Default value is 0
    double decimal;   // Default value is 0.0
    boolean isActive; // Default value is false
    String name;      // Default value is null

    public void display() {
        System.out.println("Number: " + number);
        System.out.println("Decimal: " + decimal);
        System.out.println("Is Active: " + isActive);
        System.out.println("Name: " + name);
    }
}
```

---

#### **7. Type Inference with `var`**
In Java 10 and later, the `var` keyword allows the compiler to infer the data type of a variable based on the value assigned to it. This feature simplifies variable declarations without losing type safety.

**Key Points:**
- **Local Variables:** `var` can only be used for local variables inside methods, for loops, and lambda expressions.
- **Cannot Change Type:** Once inferred, the type of the variable cannot be changed.
- **Readability:** While `var` can make code shorter, it should be used carefully to avoid reducing code readability.

**Example:**
```java
var number = 10;        // int
var name = "Vrinda";    // String
var isActive

 = true;    // boolean

// Invalid: var x; (cannot declare without initialization)
```

---

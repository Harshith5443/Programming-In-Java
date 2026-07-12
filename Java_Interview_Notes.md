# Java Interview Simple Notes

> Simple English, simple points, and interview-friendly notes.

## 1. What is JDK?

JDK stands for **Java Development Kit**.

-   It is used to develop Java applications.
-   It contains the compiler, JVM, and Java development tools.
-   It contains `javac` and `java` commands.

**Formula:** `JDK = JRE + Development Tools`

## 2. Which is the latest version of Java?

As of July 2026:

-   Latest Java version: **Java 26**
-   Latest LTS version: **Java 25**
-   LTS means **Long-Term Support**.

## 3. What are the advantages of Java?

-   Platform independent
-   Object-oriented
-   Simple
-   Secure
-   Robust
-   Portable
-   Multithreaded
-   Automatic memory management
-   Large library support

## 4. `javac` and `java` commands are available in which folder?

They are available inside the **`bin` folder of JDK**.

-   `javac` → Compiles Java program.
-   `java` → Executes Java program.

## 5. What is the signature of the main method?

``` java
public static void main(String[] args)
```

-   `public` → JVM can access it.
-   `static` → Object is not required.
-   `void` → Returns nothing.
-   `main` → Method name.
-   `String[] args` → Command-line arguments.

## 6. What is a keyword? List some keywords.

A keyword is a **reserved word in Java**. It has a special meaning.

Examples: `class`, `public`, `private`, `static`, `void`, `int`, `if`,
`else`, `for`, `while`, `return`, `final`, `abstract`, `extends`,
`implements`, `this`, `super`.

We cannot use keywords as identifiers.

## 7. What is an identifier?

An identifier is a **name given to a class, method, or variable**.

``` java
int age;
```

Here, `age` is an identifier.

Rules:

-   Cannot start with a number.
-   Cannot use a keyword.
-   Can use letters, digits, `_`, and `$`.
-   Java identifiers are case-sensitive.

## 8. What are literals?

Literals are **fixed values written directly in a program**.

``` java
int a = 10;
char ch = 'A';
String s = "Java";
boolean b = true;
```

`10`, `'A'`, `"Java"`, and `true` are literals.

## 9. Java is platform independent. Explain.

Java source code is compiled into **bytecode**. Bytecode can run on any
system having a JVM.

`Java Source Code → javac → Bytecode → JVM → Operating System`

Therefore Java follows **Write Once, Run Anywhere (WORA)**.

## 10. What is JRE?

JRE stands for **Java Runtime Environment**.

It is used to run Java applications.

**Formula:** `JRE = JVM + Java Libraries`

## 11. What is a variable?

A variable is a **named memory location used to store data**.

``` java
int age = 25;
```

## 12. Mention all primitive data types in Java.

Java has 8 primitive data types:

1.  `byte`
2.  `short`
3.  `int`
4.  `long`
5.  `float`
6.  `double`
7.  `char`
8.  `boolean`

## 13. What are primitive variables?

Variables that store primitive values are called primitive variables.

``` java
int a = 10;
char ch = 'A';
boolean b = true;
```

They directly store values.

## 14. What are reference variables?

Reference variables store a reference to an object.

``` java
Student s = new Student();
```

`s` is a reference variable.

## 15. What is String in Java?

`String` is a class used to store a sequence of characters.

``` java
String name = "Java";
```

String objects are **immutable**.

## 16. What is a method?

A method is a **block of code used to perform a task**.

``` java
void display() {
    System.out.println("Hello");
}
```

## 17. General syntax for a method

``` java
accessModifier returnType methodName(parameters) {
    // statements
}
```

Example:

``` java
public int add(int a, int b) {
    return a + b;
}
```

## 18. What is Method Overloading?

Developing multiple methods with the **same name but different parameter
lists** is called method overloading.

``` java
void add(int a, int b) {
}

void add(int a, int b, int c) {
}
```

It is **compile-time polymorphism**.

## 19. Why Method Overloading?

-   Improves readability.
-   Same operation can use the same method name.
-   Reduces confusion.
-   Supports compile-time polymorphism.

## 20. What are members?

Variables and methods declared inside a class are called **members of a
class**.

## 21. What are static members?

Members declared using the `static` keyword are static members.

``` java
static int a;

static void display() {
}
```

They belong to the **class**.

## 22. What are non-static members?

Members declared without `static` are non-static members.

``` java
int a;

void display() {
}
```

They belong to an **object**.

## 23. Static vs Non-static members

### Static members

-   Belong to the class.
-   One copy is created.
-   Access using class name.
-   Available with class initialization.

### Non-static members

-   Belong to an object.
-   Separate copy for each object.
-   Access using an object reference.
-   Created as part of an object.

## 24. What is an Object?

An object is an **instance of a class**.

``` java
Student s = new Student();
```

## 25. What is a class?

A class is a **blueprint or template for creating objects**.

``` java
class Student {
    int id;
    String name;
}
```

## 26. What are global variables?

Variables declared directly inside a class are commonly called global
variables or class-level variables.

Java normally calls them **fields**.

## 27. How can you access a static global variable?

Using the class name:

``` java
ClassName.variableName
```

## 28. How can you access non-static global variables?

Using an object reference:

``` java
Demo d = new Demo();
System.out.println(d.a);
```

## 29. Default values for global variables

  Type        Default Value
  ----------- ---------------
  byte        0
  short       0
  int         0
  long        0
  float       0.0
  double      0.0
  char        `\u0000`
  boolean     false
  Reference   null

## 30. Default value for reference variables

The default value of an instance or static reference variable is `null`.

## 31. Default value for boolean variable

The default value is `false` for instance and static boolean variables.

## 32. Difference between local and global variables

### Local variable

-   Declared inside a method or block.
-   No default value.
-   Must be initialized before use.
-   Scope is limited.

### Global/Class-level variable

-   Declared inside a class.
-   Gets a default value.
-   Can be static or non-static.
-   Scope depends on access level.

## 33. How can you declare constant variables in Java?

Using `final`:

``` java
final int MAX = 100;
```

Common style:

``` java
static final double PI = 3.14;
```

## 34. Can we just declare a final global variable?

Yes.

``` java
final int a;
```

It must be initialized exactly once.

It can be initialized during declaration, in a constructor, or in an
initialization block. A static final field can be initialized in a
static block.

## 35. What is an SIB?

SIB stands for **Static Initialization Block**.

``` java
static {
    System.out.println("SIB");
}
```

## 36. When does SIB execute?

SIB executes when the class is initialized by the JVM.

## 37. How many times will SIB execute?

Normally **once per class initialization by a class loader**.

## 38. What is an IIB?

IIB stands for **Instance Initialization Block**.

``` java
{
    System.out.println("IIB");
}
```

## 39. When will IIB execute?

IIB executes during object creation, before the constructor body.

## 40. How many times will IIB execute?

It executes **once for every object created**.

## 41. What does a method's return type signify?

The return type specifies the **type of value returned by a method**.

``` java
int add() {
    return 10;
}
```

## 42. Can we develop a method without a return type?

Every Java method must declare a return type.

If it returns nothing, use `void`.

``` java
void display() {
}
```

Constructors do not have a return type because constructors are not
methods.

## 43. What is call by value and call by reference?

Java is **always pass-by-value**.

For primitive values, a copy of the value is passed.

For objects, a copy of the reference value is passed.

Java does not support true pass-by-reference.

## 44. What is a constructor?

A constructor is a special class member used to initialize objects.

-   Same name as the class.
-   No return type.
-   Executes during object creation.

``` java
class Demo {
    Demo() {
        System.out.println("Constructor");
    }
}
```

## 45. What are two types of constructors?

Commonly discussed types:

1.  No-argument constructor
2.  Parameterized constructor

## 46. What is a default constructor?

A default constructor is a no-argument constructor automatically
provided by the compiler when we do not write any constructor.

## 47. What is `this()` calling statement?

`this()` calls another constructor of the same class.

``` java
Demo() {
    this(10);
}

Demo(int a) {
}
```

It must be the first statement in the constructor.

## 48. What is Recursion?

When a method calls itself, it is called recursion.

A stopping condition is required.

## 49. Recursion in constructor overloading gives compile-time or runtime error?

Direct or indirect recursive constructor invocation gives a
**compile-time error**.

## 50. What is `this` keyword?

`this` refers to the **current object**.

``` java
this.name = name;
```

## 51. What is instance variable hiding?

When a local variable or parameter has the same name as an instance
variable, the instance variable is hidden.

``` java
int age;

void setAge(int age) {
    this.age = age;
}
```

## 52. What is the use of `this` keyword?

-   Access current object variable.
-   Access current object method.
-   Resolve variable hiding.
-   Pass current object.
-   Return current object.

## 53. What is Inheritance?

Inheritance is the process of acquiring properties and methods of
another class.

``` java
class A {
}

class B extends A {
}
```

## 54. Different types of inheritance

1.  Single inheritance
2.  Multilevel inheritance
3.  Hierarchical inheritance
4.  Multiple inheritance
5.  Hybrid inheritance

Java classes directly support single, multilevel, and hierarchical
inheritance. Multiple inheritance of type can be achieved using
interfaces.

## 55. What is `extends`?

`extends` is a keyword used to inherit one class from another class.

``` java
class B extends A {
}
```

## 56. Does Java support multiple inheritance?

Java does not support multiple inheritance using classes.

Java supports multiple inheritance of type using interfaces.

## 57. What is Diamond Problem?

When a child inherits the same method through multiple parents, it can
create ambiguity about which implementation should be selected. This is
called the **Diamond Problem**.

## 58. Why doesn't Java support multiple inheritance using classes?

-   Avoids ambiguity.
-   Avoids the Diamond Problem.
-   Makes code simpler.
-   Makes inheritance easier to understand.

## 59. What is `super()` calling statement?

`super()` calls the parent class constructor.

``` java
class B extends A {
    B() {
        super();
    }
}
```

It must be the first statement in a constructor.

## 60. What is `super` keyword?

`super` refers to the immediate parent class part of the current object.

Uses:

-   Access parent variable.
-   Call parent method.

``` java
super.a;
super.display();
```

## 61. Difference between `super()` and `this()`

### `this()`

-   Calls a constructor of the same class.
-   Used for constructor chaining in the same class.

### `super()`

-   Calls the parent class constructor.
-   Used for constructor chaining between parent and child.

Both must be the first statement in a constructor.

## 62. Difference between `super` and `this`

### `this`

-   Refers to the current object.
-   Accesses current class members.

### `super`

-   Refers to the parent class part.
-   Accesses immediate parent members.

## 63. What is Method Overriding?

Providing a new implementation for an inherited instance method in a
subclass is called method overriding.

``` java
class A {
    void display() {
        System.out.println("A");
    }
}

class B extends A {
    @Override
    void display() {
        System.out.println("B");
    }
}
```

It supports runtime polymorphism.

## 64. Can we override static methods?

No. Static methods are **hidden**, not overridden. This is called method
hiding.

## 65. What is an abstract method?

A method declared without a body is called an abstract method.

``` java
abstract void display();
```

## 66. What is an abstract class?

A class declared using the `abstract` keyword is called an abstract
class.

It may contain abstract methods, concrete methods, variables,
constructors, and static methods.

## 67. Can we instantiate an abstract class?

No.

## 68. Rule for subclass of an abstract class

A concrete subclass must implement all inherited abstract methods.
Otherwise, the subclass must also be declared abstract.

## 69. Can an abstract class inherit another abstract class?

Yes.

## 70. Is an abstract class 100% abstract?

No. An abstract class can contain both abstract and concrete methods.

## 71. What is an interface?

An interface is a reference type used to define a contract.

``` java
interface Animal {
    void sound();
}
```

## 72. Difference between abstract class and interface

### Abstract class

-   Uses `abstract class`.
-   Can have constructors.
-   Can have instance variables.
-   A class can extend only one class.
-   Can contain abstract and concrete methods.

### Interface

-   Uses `interface`.
-   Has no constructors.
-   Interface fields are `public static final`.
-   A class can implement multiple interfaces.
-   Can contain abstract, default, static, and private methods under
    modern Java rules.

## 73. Does an abstract class have constructors? Why?

Yes. The constructor initializes the abstract class part of a child
object.

## 74. Does an interface have constructors?

No.

## 75. Can we instantiate an interface?

No.

## 76. What is `implements` keyword?

`implements` is used by a class to implement an interface.

``` java
class Dog implements Animal {
}
```

## 77. Can an interface inherit another interface?

Yes, using `extends`.

An interface can extend multiple interfaces.

## 78. What is casting?

Casting means converting a value or reference from one type to another.

Types:

1.  Primitive casting
2.  Object casting

## 79. What is primitive casting?

Converting one primitive data type into another primitive type.

## 80. What is Auto Widening and Explicit Narrowing?

### Auto Widening

Smaller compatible type to bigger type.

``` java
int a = 10;
double d = a;
```

### Explicit Narrowing

Bigger type to smaller type.

``` java
double d = 10.5;
int a = (int) d;
```

## 81. What is derived or Object casting?

Object casting means converting one compatible reference type into
another.

Types:

-   Upcasting
-   Downcasting

## 82. What is Auto Upcasting and Explicit Downcasting?

### Upcasting

``` java
Animal a = new Dog();
```

Child object is viewed using a parent reference. It is automatic.

### Downcasting

``` java
Dog d = (Dog) a;
```

Explicit casting is required.

## 83. Can we achieve Object casting without inheritance?

Generally no. There must be a compatible inheritance or interface
relationship.

## 84. Can we achieve downcasting without upcasting?

The actual object must be compatible with the child type.

``` java
Animal a = new Dog();
Dog d = (Dog) a;
```

Wrong downcasting can cause `ClassCastException`.

## 85. What is polymorphism?

Polymorphism means **one name or reference showing multiple forms or
behaviours**.

## 86. Different types of polymorphism

1.  Compile-time polymorphism → Method overloading
2.  Runtime polymorphism → Method overriding and dynamic method dispatch

## 87. What is abstraction?

Abstraction means **hiding implementation details and showing essential
functionality**.

Achieved using:

-   Abstract classes
-   Interfaces

## 88. What are packages?

A package is a group of related classes and interfaces.

``` java
package com.demo;
```

## 89. Why packages?

-   Organize classes.
-   Avoid naming conflicts.
-   Provide access control.
-   Improve maintenance.
-   Improve reusability.

## 90. Different access levels in Java

### `private`

Accessible only inside the same class.

### default/package-private

Accessible inside the same package.

### `protected`

Accessible in the same package and eligible subclasses outside the
package.

### `public`

Accessible from anywhere, subject to normal Java access rules.

## 91. What is a Singleton class?

A Singleton class controls object creation so that one shared instance
is exposed.

``` java
class Demo {
    private static final Demo obj = new Demo();

    private Demo() {
    }

    public static Demo getInstance() {
        return obj;
    }
}
```

## 92. What is encapsulation?

Encapsulation means wrapping data and methods inside a class and
controlling direct access to data.

Usually achieved using private variables and public getter/setter
methods.

## 93. Which is the supermost class for all classes in Java?

`java.lang.Object` is the root superclass of normal Java class
hierarchies.

## 94. Explain `toString()` of Object class

`toString()` returns a string representation of an object.

The default representation generally looks like:

`ClassName@hexadecimalHash`

## 95. Explain `hashCode()` of Object class

`hashCode()` returns an integer hash value for an object.

It is commonly used by hash-based collections such as `HashMap` and
`HashSet`.

If two objects are equal according to `equals()`, they must have the
same hash code.

## 96. Explain `equals()` of Object class

`equals()` is used to compare objects for equality.

The default `Object.equals()` compares reference identity. Classes can
override it for content-based equality.

## 97. Can a subclass override `toString()`, `hashCode()`, and `equals()`?

Yes. These methods can be overridden.

## 98. What is a final method?

A method declared using `final` cannot be overridden.

## 99. What is a final class?

A final class cannot be inherited.

## 100. What is the use of `finalize()`?

`finalize()` was historically related to garbage collection cleanup.

It is deprecated and should not be used for resource management.

Prefer try-with-resources, `AutoCloseable`, or explicit cleanup.

## 101. What is the use of `clone()`?

`clone()` is used to create a field-by-field copy of an object.

Traditional cloning commonly uses the `Cloneable` marker interface.

Modern code often prefers copy constructors or factory methods.

## 102. What is a marker interface?

An interface with no methods or fields is traditionally called a marker
interface.

Examples:

-   `Serializable`
-   `Cloneable`

## 103. Strings are immutable in Java. Justify.

Once a String object is created, its value cannot be changed.

``` java
String s = "Java";
s.concat(" Developer");
```

The original `"Java"` object is not modified. A new String is produced.

Benefits include security, thread safety, String pool support, and
stable hash values.

## 104. Can we inherit the String class?

No. `String` is a `final` class.

## 105. `toString()`, `hashCode()`, and `equals()` in String

-   `toString()` → Returns the String itself.
-   `equals()` → Compares String contents.
-   `hashCode()` → Calculates hash code based on String contents.

Equal Strings have equal hash codes.

## 106. String Constant Pool and non-constant pool

String literals are stored in the String pool.

``` java
String s1 = "Java";
String s2 = "Java";
```

Both can refer to the same pooled String object.

``` java
String s3 = new String("Java");
```

`new` explicitly creates a new String object on the heap.

## 107. What are arrays?

An array stores multiple values of the same declared type.

``` java
int[] a = {10, 20, 30};
```

-   Fixed size.
-   Index starts from 0.
-   Stores the same declared type.

## 108. What is a primitive array?

An array storing primitive values.

``` java
int[] a = new int[5];
```

## 109. What is a derived array?

An array storing reference values is often called a derived or
reference-type array.

``` java
String[] names = new String[5];
Student[] students = new Student[5];
```

## 110. What is Boxing and Unboxing?

### Boxing

Primitive to wrapper object.

``` java
int a = 10;
Integer i = a;
```

### Unboxing

Wrapper object to primitive.

``` java
Integer i = 10;
int a = i;
```

## 111. What are Wrapper classes?

  Primitive   Wrapper
  ----------- -----------
  byte        Byte
  short       Short
  int         Integer
  long        Long
  float       Float
  double      Double
  char        Character
  boolean     Boolean

## 112. What is Collection API/Framework?

Java Collection Framework provides classes and interfaces to store and
manipulate groups of objects.

Important interfaces:

-   List
-   Set
-   Queue
-   Map

`Map` is part of the Collections Framework, but it does not extend
`Collection`.

## 113. Explain List collection

-   Maintains insertion order.
-   Allows duplicates.
-   Supports index-based access.

Examples:

-   `ArrayList`
-   `LinkedList`
-   `Vector`
-   `Stack`

## 114. Explain Set collection

-   Stores unique elements.
-   Does not allow duplicate elements.
-   Ordering depends on implementation.

Examples:

-   `HashSet`
-   `LinkedHashSet`
-   `TreeSet`

## 115. Explain Queue collection

Queue is mainly used to hold elements for processing.

Common idea: **FIFO --- First In, First Out**.

Examples:

-   `PriorityQueue`
-   `ArrayDeque`
-   `LinkedList`

Exact processing order depends on the implementation.

## 116. Difference between List, Set, and Queue

  List                Set                       Queue
  ------------------- ------------------------- ------------------------
  Ordered             Unique elements           Processing-oriented
  Allows duplicates   No duplicates             Commonly FIFO
  Index supported     No general index access   Uses offer, poll, peek

## 117. What are exceptions?

An exception is an abnormal condition that interrupts the normal flow of
a program.

``` java
int a = 10 / 0;
```

This causes `ArithmeticException`.

## 118. How to handle exceptions?

Using:

-   `try`
-   `catch`
-   `finally`
-   `throw`
-   `throws`

``` java
try {
    int a = 10 / 0;
} catch (ArithmeticException e) {
    System.out.println("Exception handled");
}
```

## 119. What are checked exceptions?

Exceptions checked by the compiler for mandatory catch or declaration.

Examples:

-   `IOException`
-   `SQLException`
-   `ClassNotFoundException`

## 120. What are unchecked exceptions?

Exceptions in the `RuntimeException` family.

Examples:

-   `ArithmeticException`
-   `NullPointerException`
-   `ArrayIndexOutOfBoundsException`
-   `ClassCastException`

## 121. Different ways of handling checked exceptions

1.  Using `try-catch`
2.  Using `throws`

## 122. Difference between `final`, `finalize()`, and `finally`

-   `final` → Keyword used with variables, methods, and classes.
-   `finally` → Block used with exception handling.
-   `finalize()` → Deprecated method historically associated with
    garbage collection cleanup.

## 123. How to write data into a text file?

``` java
import java.io.FileWriter;
import java.io.IOException;

class Demo {
    public static void main(String[] args) throws IOException {
        FileWriter fw = new FileWriter("data.txt");
        fw.write("Hello Java");
        fw.close();
    }
}
```

## 124. How to read data from a text file?

``` java
import java.io.File;
import java.io.FileNotFoundException;
import java.util.Scanner;

class Demo {
    public static void main(String[] args)
            throws FileNotFoundException {

        Scanner sc = new Scanner(new File("data.txt"));

        while (sc.hasNextLine()) {
            System.out.println(sc.nextLine());
        }

        sc.close();
    }
}
```

## 125. What is the use of Scanner class?

`Scanner` is used to read input.

It can read:

-   Console input
-   File input
-   String input

## 126. How to read a String from the console?

``` java
import java.util.Scanner;

class Demo {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String name = sc.nextLine();
        System.out.println(name);
        sc.close();
    }
}
```

## 127. What are Threads?

A thread is a path of execution inside a process.

Threads allow multiple tasks to make progress concurrently.

## 128. What is the use of `sleep()` in Threads?

`Thread.sleep()` pauses the current thread for a specified time.

``` java
Thread.sleep(1000);
```

1000 milliseconds = 1 second.

It can throw `InterruptedException`.

## 129. Can we develop final methods in an interface?

No. Interface methods cannot be declared `final`.

## 130. Can we develop a final abstract class?

No.

-   `abstract` means the class is intended for inheritance.
-   `final` means the class cannot be inherited.

## 131. Can we develop a static method in an abstract class?

Yes.

``` java
abstract class Demo {
    static void display() {
        System.out.println("Java");
    }
}
```

## 132. Can we declare a variable in an interface without initializing?

No.

Interface fields are implicitly `public static final`, so they must be
initialized.

``` java
interface Demo {
    int A = 10;
}
```

# Experience Interview Questions

## Method Overloading

Same method name with different parameter lists. It is compile-time
polymorphism.

## Method Overriding

A subclass provides a new implementation of an inherited instance
method. It supports runtime polymorphism.

## Polymorphism

Polymorphism means one name, interface, or reference can represent
multiple forms or behaviours.

-   Overloading → Compile-time polymorphism
-   Overriding → Runtime polymorphism

## Abstract Class

A class declared with `abstract` keyword.

``` java
abstract class Animal {
    abstract void sound();

    void eat() {
        System.out.println("Eating");
    }
}
```

We cannot directly instantiate an abstract class.

## Collection: List, Set, Queue

-   **List** → Ordered, duplicates allowed, index supported.
-   **Set** → Unique elements, no duplicates.
-   **Queue** → Used for processing elements, commonly FIFO.

# Java Programs

## Reverse the String `"javadeveloper"`

``` java
class ReverseString {
    public static void main(String[] args) {
        String s = "javadeveloper";
        String rev = "";

        for (int i = s.length() - 1; i >= 0; i--) {
            rev = rev + s.charAt(i);
        }

        System.out.println(rev);
    }
}
```

**Output:** `repolevedavaj`

## Rearrange the given sentence

Input:

`dinga and dingi is are so good`

Expected output:

`good and dingi dinga are so is`

``` java
class Sentence {
    public static void main(String[] args) {
        String s = "dinga and dingi is are so good";
        String[] a = s.split(" ");

        System.out.println(
            a[6] + " " +
            a[1] + " " +
            a[2] + " " +
            a[0] + " " +
            a[4] + " " +
            a[5] + " " +
            a[3]
        );
    }
}
```

## Star Triangle Pattern

``` text
      *
    * *
  * * *
* * * *
```

``` java
class Pattern {
    public static void main(String[] args) {
        int n = 4;

        for (int i = 1; i <= n; i++) {
            for (int j = i; j < n; j++) {
                System.out.print("  ");
            }

            for (int j = 1; j <= i; j++) {
                System.out.print("* ");
            }

            System.out.println();
        }
    }
}
```

## Number Pattern

``` text
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
1 2 3 4 5
```

``` java
class Pattern {
    public static void main(String[] args) {
        for (int i = 1; i <= 4; i++) {
            for (int j = 1; j <= 5; j++) {
                System.out.print(j + " ");
            }

            System.out.println();
        }
    }
}
```

## Hollow Rectangle Pattern

``` text
0000000
0     0
0     0
0     0
0     0
0000000
```

``` java
class Pattern {
    public static void main(String[] args) {
        int rows = 6;
        int columns = 7;

        for (int i = 1; i <= rows; i++) {
            for (int j = 1; j <= columns; j++) {
                if (i == 1 || i == rows || j == 1 || j == columns) {
                    System.out.print("0");
                } else {
                    System.out.print(" ");
                }
            }

            System.out.println();
        }
    }
}
```

## Factorial of a Number

``` java
class Factorial {
    public static void main(String[] args) {
        int n = 5;
        int fact = 1;

        for (int i = 1; i <= n; i++) {
            fact = fact * i;
        }

        System.out.println(fact);
    }
}
```

## Fibonacci Series

``` java
class Fibonacci {
    public static void main(String[] args) {
        int a = 0;
        int b = 1;

        for (int i = 1; i <= 8; i++) {
            System.out.print(a + " ");
            int c = a + b;
            a = b;
            b = c;
        }
    }
}
```

**Output:** `0 1 1 2 3 5 8 13`

## Odd or Even Number

``` java
class OddEven {
    public static void main(String[] args) {
        int n = 10;

        if (n % 2 == 0) {
            System.out.println("Even Number");
        } else {
            System.out.println("Odd Number");
        }
    }
}
```

## Prime Number

``` java
class PrimeNumber {
    public static void main(String[] args) {
        int n = 7;
        int count = 0;

        for (int i = 1; i <= n; i++) {
            if (n % i == 0) {
                count++;
            }
        }

        if (count == 2) {
            System.out.println("Prime Number");
        } else {
            System.out.println("Not Prime Number");
        }
    }
}
```

## Swap Two Numbers Without a Third Variable

``` java
class Swap {
    public static void main(String[] args) {
        int a = 10;
        int b = 20;

        a = a + b;
        b = a - b;
        a = a - b;

        System.out.println("a = " + a);
        System.out.println("b = " + b);
    }
}
```

# Quick Interview Revision

-   JDK → Java Development Kit
-   JRE → Java Runtime Environment
-   JVM → Executes Java bytecode
-   Class → Blueprint
-   Object → Instance of class
-   Variable → Stores data
-   Method → Performs a task
-   Constructor → Initializes object
-   Inheritance → Acquiring properties from parent
-   Polymorphism → Many forms
-   Abstraction → Hiding implementation
-   Encapsulation → Protecting and controlling data
-   Overloading → Same method name, different parameters
-   Overriding → New subclass implementation of inherited method
-   List → Ordered and duplicates allowed
-   Set → Unique elements
-   Queue → Processing order, commonly FIFO
-   String → Immutable class
-   Array → Fixed-size collection of the same declared type
-   Exception → Abnormal condition
-   Thread → Path of execution
-   static → Belongs to class
-   non-static → Belongs to object
-   this → Current object
-   super → Immediate parent class part
-   final → Restricts change, overriding, or inheritance depending on
    use
-   finally → Exception-handling cleanup block
-   finalize() → Deprecated cleanup method
-   SIB → Static Initialization Block
-   IIB → Instance Initialization Block
-   Upcasting → Child object viewed using parent reference
-   Downcasting → Parent-type reference cast to child type
-   Boxing → Primitive to Wrapper
-   Unboxing → Wrapper to Primitive
-   Checked Exception → Compiler requires catch or declaration
-   Unchecked Exception → RuntimeException family
-   Object → Root superclass
-   Serializable → Marker interface
-   Cloneable → Marker interface

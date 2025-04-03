# Java Interview Questions and Answers

## What is the difference between JDK, JVM, & JRE?
The **Java Development Kit (JDK)** is a full-featured development environment for Java, including the Java Runtime Environment (JRE), compilers, and debuggers. The **Java Virtual Machine (JVM)** is the runtime that executes Java bytecode. The **Java Runtime Environment (JRE)** is a subset of the JDK containing the JVM and libraries needed to run Java applications but not to develop them.

## What is the JIT compiler?
The **Just-In-Time (JIT) compiler** is a component of the JVM that improves performance by compiling bytecode into native machine code at runtime, reducing the need for interpretation.

## What is Java Memory? Describe Stack and Heap.
Java memory is divided into **Stack** and **Heap**:
- **Stack**: Stores method-specific values, including primitive data types and method call references. It follows LIFO order.
- **Heap**: Stores objects and class instances. It is managed by the garbage collector.

## What is OOP? Elaborate on the four pillars.
**Object-Oriented Programming (OOP)** is a paradigm that organizes software around objects. The four pillars are:
1. **Encapsulation**: Hiding internal details of an object and exposing only necessary parts.
2. **Abstraction**: Simplifying complex systems by exposing only relevant details.
3. **Inheritance**: Allowing one class to inherit attributes and behaviors from another.
4. **Polymorphism**: Enabling a single interface to represent multiple implementations.

## What are Wrapper classes?
Wrapper classes allow primitive types to be treated as objects. Examples include `Integer` for `int`, `Double` for `double`, and `Boolean` for `boolean`.

## Java access modifiers
- **Public**: Accessible from anywhere.
- **Private**: Accessible only within the same class.
- **Protected**: Accessible within the same package and subclasses.
- **Default**: Accessible within the same package.

## Relationship between class and object
A **class** is a blueprint for creating objects. An **object** is an instance of a class containing real values.

## What is the role of a constructor?
A **constructor** initializes an object when it is created. It has the same name as the class and does not have a return type.

## Abstract classes vs. interfaces
- **Abstract Class**: Can have both abstract and concrete methods, but cannot be instantiated.
- **Interface**: Can only have abstract methods (before Java 8) and allows multiple inheritance.

## Can you implement multiple interfaces in Java? Can you extend multiple classes?
Yes, a class can implement multiple interfaces, but it can only extend one class due to the diamond problem.

## What does the `static` keyword do?
The `static` keyword makes a method or variable belong to the class rather than instances of the class.

## What does `default` do in an interface method?
Introduced in Java 8, it allows methods in an interface to have an implementation.

## What are the different scopes in Java?
- **Method Scope**: Variables declared within a method.
- **Class Scope**: Variables declared within a class but outside methods.
- **Instance Scope**: Instance variables belonging to an object.
- **Block Scope**: Variables declared inside loops or blocks.

## Tell me about access and non-access modifiers.
- **Access Modifiers**: `public`, `private`, `protected`, `default`.
- **Non-Access Modifiers**: `final`, `static`, `abstract`, `synchronized`.

## Tell me about the two different kinds of exceptions.
- **Checked Exceptions**: Must be handled at compile-time (e.g., `IOException`).
- **Unchecked Exceptions**: Occur at runtime (e.g., `NullPointerException`).

## How to create custom exceptions?
Extend `Exception` or `RuntimeException` and define a constructor.

## How to compare (equate) two objects in Java?
Use the `equals()` method instead of `==`, which compares references.

## Overloading vs Overriding?
- **Overloading**: Defining multiple methods with the same name but different parameters.
- **Overriding**: Redefining a method in a subclass.

## Can we change the order of `public static void main`?
No, the order must be `public static void main(String[] args)`.

## Difference between `final` and `finally`?
- `final`: Used for constants, method prevention, and class prevention.
- `finally`: A block in exception handling that always executes.

## What is a singleton?
A design pattern ensuring only one instance of a class exists.

## What is the garbage collector? Can you force garbage collection?
It automatically reclaims memory. `System.gc()` suggests garbage collection but does not force it.

---

# SQL Interview Questions and Answers

## What is a Transaction and what are the ACID properties?
A **transaction** is a unit of work performed in a database. **ACID** properties ensure reliability:
- **Atomicity**: All or nothing.
- **Consistency**: Maintains database integrity.
- **Isolation**: Transactions operate independently.
- **Durability**: Changes are permanent after commit.

## Name and describe some SQL joins.
- **INNER JOIN**: Returns matching rows.
- **LEFT JOIN**: Returns all rows from the left table and matches from the right.
- **RIGHT JOIN**: Returns all rows from the right table and matches from the left.
- **FULL JOIN**: Returns all rows from both tables.

---

# HTTP Interview Questions and Answers

## What is HTTP?
HTTP (HyperText Transfer Protocol) is the foundation of communication on the web.

## What are HTTP status codes? Example of different types?
- **2xx**: Success (e.g., `200 OK`)
- **3xx**: Redirection (e.g., `301 Moved Permanently`)
- **4xx**: Client errors (e.g., `404 Not Found`)
- **5xx**: Server errors (e.g., `500 Internal Server Error`)

---

# Spring Interview Questions and Answers

## What is Spring Boot?
A framework for creating stand-alone Spring applications with minimal configuration.

## What is the purpose of the `@Component` annotation?
Marks a class as a Spring-managed component.

## What is Autowiring?
Spring's way of injecting dependencies automatically.

---

# Git Interview Questions and Answers

## What is a branch?
A separate line of development in Git.

## How to merge a branch?
Use `git merge <branch-name>`.

## What is CI/CD?
Continuous Integration and Continuous Deployment automate testing and deployment processes.

---

This document provides answers to common Java, SQL, HTTP, Spring, and Git interview questions. Feel free to update and add more details as needed!

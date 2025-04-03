# Interview Questions and Answers

## Java

### What is the difference between JDK, JVM, & JRE?
JDK (Java Development Kit), JVM (Java Virtual Machine), and JRE (Java Runtime Environment) are essential components of the Java ecosystem:
- **JDK**: Includes the compiler, libraries, and development tools to write and compile Java applications.
- **JVM**: The virtual machine that runs Java bytecode, making Java platform-independent.
- **JRE**: Provides libraries and environment to run Java applications but does not include the compiler.

### What is the JIT compiler?
The **Just-In-Time (JIT) compiler** is part of the JVM that improves performance by compiling bytecode into native machine code at runtime.

### What is Java Memory? Describe Stack and Heap.
Java memory is divided into:
- **Stack**: Stores method calls and local variables. It is fast and follows the Last-In-First-Out (LIFO) principle.
- **Heap**: Stores objects and instance variables. It is managed by the garbage collector.

### What is OOP? Elaborate on the four pillars
Object-Oriented Programming (OOP) is a paradigm that structures code using objects. The four pillars are:
1. **Encapsulation** - Hiding internal details and exposing only necessary parts.
2. **Inheritance** - Allowing one class to inherit properties and methods from another.
3. **Polymorphism** - Ability of an object to take many forms.
4. **Abstraction** - Hiding complex implementation details.

### What are Wrapper classes?
Wrapper classes convert primitive data types into objects (e.g., `Integer` for `int`, `Double` for `double`).

### Java access modifiers
Java has four access modifiers:
- `public` (accessible everywhere)
- `protected` (accessible within the same package and subclasses)
- `default` (accessible within the same package)
- `private` (accessible only within the same class)

### Relationship between class and object
A **class** is a blueprint for creating objects. An **object** is an instance of a class.

### What is the role of a constructor?
A constructor initializes an object when it is created.

### Abstract classes vs. Interfaces
- **Abstract classes**: Can have method implementations and fields.
- **Interfaces**: Only declare methods (until Java 8, which introduced default methods).

### Can you implement multiple interfaces in Java? Can you extend multiple classes?
- Yes, a class can implement multiple interfaces.
- No, a class can only extend one class due to Java's single inheritance model.

### What does the static keyword do?
Defines a method or variable that belongs to the class, not instances.

### What does default do in an interface method?
From Java 8, `default` allows methods in interfaces to have a default implementation.

### What are the different scopes in Java?
1. Method scope
2. Class scope
3. Instance scope
4. Global scope

### Tell me about access and non-access modifiers
- **Access modifiers**: `public`, `private`, `protected`, `default`
- **Non-access modifiers**: `static`, `final`, `abstract`, `synchronized`, `transient`

### Tell me about the 2 different kinds of exceptions
1. **Checked Exceptions**: Must be handled at compile time (e.g., `IOException`).
2. **Unchecked Exceptions**: Runtime exceptions (e.g., `NullPointerException`).

### How do you handle exceptions?
Using `try-catch-finally` or `throws`.

### How do exceptions and errors differ?
- **Exceptions** can be recovered from.
- **Errors** (e.g., `OutOfMemoryError`) are usually not recoverable.

### How to create custom exceptions?
By extending the `Exception` class:
```java
class CustomException extends Exception {
    public CustomException(String message) {
        super(message);
    }
}
```

### How to compare (equate) 2 objects in Java?
Using `.equals()` or overriding `hashCode()` and `equals()`.

### Overloading vs Overriding?
- **Overloading**: Multiple methods with the same name but different parameters.
- **Overriding**: Redefining a method in a subclass.

### Explain each part of `public static void main(String[] args){}`
- `public` – Accessible from anywhere.
- `static` – No need to create an object.
- `void` – No return type.
- `main` – Entry point of Java application.
- `String[] args` – Command-line arguments.

### Difference between final and finally?
- `final`: Used for variables, methods, and classes to make them constant.
- `finally`: A block that always executes after `try-catch`.

### What is a singleton?
A design pattern ensuring only one instance of a class exists.

### What is the garbage collector? Can you force garbage collection?
Manages memory by removing unused objects. Cannot force, but can request using `System.gc()`.

### What is unit testing? How do we do it in Java?
Testing individual components using frameworks like JUnit.

---

## SQL

### What is a Transaction and what are the ACID properties?
A **transaction** is a sequence of operations treated as a single unit.
**ACID**:
- **Atomicity**: All operations complete or none.
- **Consistency**: Maintains database integrity.
- **Isolation**: Transactions don’t interfere with each other.
- **Durability**: Changes persist even after system failure.

### Name and describe some SQL joins
1. **INNER JOIN**: Returns matching rows from both tables.
2. **LEFT JOIN**: Returns all rows from the left table and matching rows from the right.
3. **RIGHT JOIN**: Returns all rows from the right table and matching rows from the left.
4. **FULL JOIN**: Returns all rows when there is a match in either table.

### What does GROUP BY do in SQL?
Groups rows with the same values and applies aggregate functions.

---

## HTTP

### What is HTTP?
A protocol used for communication between clients and servers.

### What are HTTP status codes?
- `200 OK` (Success)
- `404 Not Found` (Resource not found)
- `500 Internal Server Error` (Server issue)

### What are HTTP verbs?
- `GET`: Retrieve data
- `POST`: Submit data
- `PUT`: Update data
- `DELETE`: Remove data

---

## Spring

### What is Spring Boot?
A framework that simplifies Java development with embedded servers, auto-configuration, and dependency injection.

### What are Spring Beans?
Objects managed by the Spring container.

### What is the purpose of the `@Component` annotation?
Marks a class as a Spring-managed component.

### What is Autowiring?
Spring’s way of injecting dependencies automatically.

---

## Git

### What is a branch?
A separate line of development in Git.

### What is CI/CD?
Continuous Integration and Continuous Deployment automate software delivery.

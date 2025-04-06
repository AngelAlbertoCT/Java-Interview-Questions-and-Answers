# Interview Questions and Answers

## Java

### 1. What is the difference between JDK, JVM, & JRE?

* **What**: JDK (Java Development Kit), JVM (Java Virtual Machine), and JRE (Java Runtime Environment) are three crucial components in Java.

* **Why**: Each serves a different purpose in the Java ecosystem.

* **How**:

    * **JDK**: It’s a full-featured software development kit used to develop Java applications. It includes the JRE, JVM, and additional tools like compilers (javac).
 
    * **JRE**: It provides libraries, Java Virtual Machine, and other components necessary to run applications written in Java.

    * **JVM**: It is the engine that provides runtime environment to execute Java bytecode, converting it into machine code for the operating system.

**Example**: In my project at Revature, we used the JDK to compile and run Java code locally on our machines, while the JVM ensured the bytecode we generated was cross-platform compatible.

### 2. What is the JIT compiler?
* **What**: The Just-In-Time (JIT) compiler is part of the JVM that compiles bytecode into machine code at runtime.

* **Why**: It helps improve performance by translating code into machine code just when it is needed.

* **How**: It works by compiling frequently used bytecode into native machine code, so the JVM doesn’t need to interpret the code every time it's executed.

**Example**: While working on a performance optimization project, we noticed a significant speedup when JIT was enabled, as the frequently used code paths were compiled directly to machine code.

### 3. What is Java Memory? Describe Stack and Heap.
* **What**: Java memory is divided into two main parts: Stack and Heap.

* **Why**: These areas are responsible for managing data during the execution of Java applications.

* **How**:

    * **Stack**: Stores method calls, local variables, and references to objects. It is managed by the JVM and is automatically cleaned up when a method finishes executing.

    * **Heap**: Used for dynamic memory allocation. Objects are stored here and managed by the garbage collector.

**Example**: In a project, I worked on optimizing memory usage where we noticed that unnecessary object creation was increasing heap usage. We refactored the code to use primitive types more efficiently.

### 4. What is OOP? Elaborate on the four pillars
* **What**: OOP (Object-Oriented Programming) is a programming paradigm based on the concept of objects, which contain data and methods.

* **Why**: It helps in creating modular, reusable, and maintainable code.

* **How**:

    * **Encapsulation**: Wrapping data and code together as a single unit and restricting access to certain components.

    * **Abstraction**: Hiding complex implementation details and showing only necessary functionality.

    * **Inheritance**: One class inherits properties and methods from another, allowing code reuse.

    * **Polymorphism**: The ability to take many forms, where methods can be overridden to behave differently based on the object.

**Example**: In a school management system project, I used inheritance to create a base `Person` class, which was extended by `Student` and `Teacher` classes.

### 5. What are Wrapper classes?
* **What**: Wrapper classes are objects that encapsulate primitive types.

* **Why**: They allow primitives to be treated as objects, which is useful in collections that can only store objects.

* **How**: Each primitive type (e.g., `int`, `char`) has a corresponding wrapper class (e.g., `Integer`, `Character`).

**Example**: In a project, we needed to store integers in a list. Since Java collections work with objects, I used `Integer` (the wrapper class) instead of the primitive `int`.

### 6. Java Access Modifiers
* **What**: Access modifiers in Java control the visibility of classes, methods, and variables.

* **Why**: They help in enforcing encapsulation by restricting access to certain parts of the code.

* **How**:

    * **public**: Accessible from any class.

    * **private**: Accessible only within the same class.

    * **protected**: Accessible within the same package and by subclasses.

    * **default**: Accessible only within the same package.

**Example**: In the REST API I developed using Spring Boot, I used `private` for variables to ensure they could only be accessed or modified via getters and setters.

### 7. Relationship between Class and Object
* **What**: A class is a blueprint for creating objects (instances), which are actual representations of that class.

* **Why**: This relationship allows for creating multiple instances from a single class definition.

* **How**: An object contains state (attributes) and behavior (methods) defined by the class.

**Example**: In my Java project for a library system, I created a `Book` class, and then instantiated multiple `Book` objects with different titles, authors, and publication years.

### 8. What is the role of a constructor?
* **What**: A constructor initializes an object when it is created.

* **Why**: It sets the initial state of the object and can take parameters to provide specific values.

* **How**: It has the same name as the class and doesn’t have a return type.

**Example**: In the same library system project, I created a constructor in the `Book` class to initialize the title, author, and year of publication when creating a new book object.

### 9. abstract classes vs. interfaces
* **What**: Abstract classes and interfaces both define methods that can be implemented by subclasses, but they have key differences.

* **Why**: They provide different ways of designing reusable code and ensuring that subclasses follow a specific contract.

* **How**:

    * **Abstract classes**: Can have both abstract (without implementation) and concrete (with implementation) methods. Can have fields, constructors.

    * **Interfaces**: Can only have abstract methods (prior to Java 8), but can have default methods and static methods as of Java 8. They cannot have fields.

**Example**: In an e-commerce platform I worked on, I used interfaces to define various payment methods (PaymentMethod), while the abstract class was used for common behavior shared across different product types.

### 10. Can you implement multiple interfaces in Java? Can you extend multiple classes?
* **What**: Yes, you can implement multiple interfaces, but Java does not allow multiple class inheritance.

* **Why**: This allows Java to avoid complexity and ambiguity in class inheritance.

* **How**: A class can implement multiple interfaces, but it can only extend one class.

**Example**: In a project where we were developing a customer management system, I had a `Customer` class implement both `Serializable` and `Cloneable` interfaces.

### 11. What does the static keyword do?
* **What**: The `static` keyword is used to declare members (variables or methods) that belong to the class itself rather than to instances of the class.

* **Why**: It allows the members to be accessed without creating an instance of the class, and it can be shared among all instances.

* **How**: You can use the `static` keyword for methods, variables, and blocks.

**Example**: In my project, I used a `static` method to generate a unique customer ID, which didn't require an instance of the `Customer` class to be created.

### 12. What does default do in an interface method?
* **What**: The `default` keyword allows you to define a method in an interface with a body, providing a default implementation.

* **Why**: It enables you to add new methods to interfaces without breaking existing implementations of the interface.

* **How**: Any class that implements the interface can use the default implementation, but can also override it if necessary.

**Example**: In a project where I had multiple payment methods, I used a default method in the `PaymentMethod` interface to provide a common `refund()` method, which could be customized in individual payment method classes.

### 13. What are the different scopes in Java?
* **What**: Scopes in Java define where variables and methods are accessible within a program.

* **Why**: They help in organizing code and preventing unintended access to variables.

* **How**:

    * **Local scope**: Variables declared within a method or block.

    * **Instance scope**: Variables declared within a class but outside of methods.

    * **Class scope**: Variables declared with `static` keyword, accessible through the class.

    * **Global scope**: Variables accessible throughout the entire class.

**Example**: During my work on a banking system, I declared class-level variables for user accounts and local variables within methods to calculate transactions.

### 14. Tell me about access and non-access modifiers?
* **What**: Access modifiers control the visibility of classes, methods, and variables, while non-access modifiers modify behavior and attributes of these members.

* **Why**: These modifiers provide control over how data is accessed or modified and provide functionality like thread synchronization or immutability.

* **How**:

    * **Access modifiers**: `public`, `private`, `protected`, and default (package-private).

Non-access modifiers: `static`, `final`, `abstract`, `synchronized`, `volatile`, etc.

**Example**: In a multi-threaded application, I used the `synchronized` keyword to ensure that certain methods could only be accessed by one thread at a time.

### 15. Tell me about the 2 different kinds of exceptions
* **What**: In Java, exceptions are categorized into checked and unchecked exceptions.

* **Why*: This distinction helps in deciding whether or not an exception needs to be handled during compilation or runtime.

* **How**:

    * **Checked exceptions**: Exceptions that are checked at compile-time, like `IOException` or `SQLException`. They must be either caught or declared.

    * **Unchecked exceptions**: Exceptions that are not checked at compile-time, like `NullPointerException` or `ArrayIndexOutOfBoundsException`. These are usually programming errors.

**Example**: In a project, I handled a `SQLException` (a checked exception) when querying a database, and caught a `NullPointerException` (an unchecked exception) in places where an object might not have been initialized.

### 16. What are some examples of checked and unchecked exceptions?
* **What**: As mentioned earlier, checked exceptions are those that must be explicitly handled by the programmer, while unchecked exceptions don’t require explicit handling.

* **Why**: The distinction ensures that potential errors are addressed early (for checked exceptions) and allows developers more flexibility with unchecked exceptions.

* **How**:

    * **Checked**: `IOException`, `SQLException`, `FileNotFoundException`.

    * **Unchecked**: `NullPointerException`, `ArithmeticException`, `IndexOutOfBoundsException`.

**Example**: In a project where I worked on file handling, I used `IOException` when reading from a file to ensure proper error handling for scenarios like missing files.

### 17. How do you handle exceptions?
* **What**: Exceptions are handled using `try`, `catch`, `finally` blocks.

* **Why**: This allows programs to handle errors gracefully, ensuring they don’t crash unexpectedly.

* **How**:

    * `try`: Used to define the block of code that might throw an exception.

    * `catch`: Used to define how to handle specific exceptions.

    * `finally`: Defines a block of code that will run regardless of whether an exception occurs or not.

**Example**: In a recent project, I wrapped database connection code inside a `try-catch` block and used finally to close the connection after operations were complete.

### 18. How do exceptions and errors differ?
* **What**: Exceptions and errors both represent abnormal conditions, but errors typically indicate serious issues that the program cannot recover from.

* **Why**: Understanding this distinction helps developers decide how to handle different types of failures.

* **How**:

    * **Exceptions**: Usually caused by external factors, like user input or incorrect file paths. Can be caught and handled.

    * **Errors**: Caused by JVM issues or other internal system failures (e.g., OutOfMemoryError), which cannot typically be recovered from.

**Example**: While working on a web application, I handled SQLException (an exception) for database issues, but did not attempt to catch errors like `OutOfMemoryError` because they often indicate unrecoverable system failures.

### 19. How to create custom exceptions?
* **What**: Custom exceptions are user-defined exceptions that extend either `Exception` or `RuntimeException`.

* **Why**: They allow you to throw meaningful errors specific to your application’s needs.

* **How**: You define a custom exception class and throw it in your code when a specific condition is met.

**Example**: In my project to manage user access, I created a `UserNotFoundException` to signal when a user is not found in the database, allowing the application to handle the error appropriately.

### 20. How to compare (equate) 2 objects in Java?
* **What**: In Java, comparing two objects can be done using the `equals()` method, and also the `==` operator.

* **Why**: Using `==` compares references (memory addresses), while `equals()` compares the actual contents of the objects.

* **How**: Override the `equals()` method in your class to compare the contents of two objects meaningfully.

**Example**: In a project where I handled a list of users, I overrode the `equals()` method in the `User` class to compare users based on their unique `id` field rather than their reference.

### 21. Overloading vs Overriding?
* **What**: Overloading and overriding are two concepts used for method polymorphism in Java, but they are different.

* **Why**: They help with flexibility and code reuse.

* **How**:

    * **Overloading**: It occurs when you have multiple methods with the same name but different parameters (either in number, type, or both).

    * **Overriding**: It happens when a subclass provides a specific implementation of a method that is already defined in its superclass.

**Example**: In a calculator project, I overloaded the `add()` method to handle different types of parameters (e.g., `int add(int a, int b)` and `double add(double a, double b)`). Additionally, I overrode the `toString()` method from the `Object` class to give a custom string representation of a `Product` class.

### 22. Explain each of the parts of `public static void main(String[] args){}`
* **What**: The `main` method is the entry point for Java applications.

* **Why**: It is required to start the execution of any Java application, except for Java applets.

* **How**:

    * **public**: Access modifier that makes the `main` method accessible from outside the class.

    * **static**: Means that this method can be called without creating an instance of the class.

    * **void**: Specifies that the method does not return any value.

    * **main**: The name of the method that the JVM looks for when starting a program.

    * **String[] args**: This is an array of `String` arguments that can be passed to the program from the command line.

**Example**: In a project where I created a Java-based to-do list application, I used the `main()` method to instantiate the `TaskManager` and start interacting with the user.

### 23. Can we change the order of `public static void main(String[] args)`?
* **What**: No, the order and signature of the `main` method cannot be changed.

* **Why**: The JVM specifically looks for this signature to begin the program execution.

* **How**: You must use `public static void main(String[] args)` exactly as is. Changing the order, returning a value, or removing `String[] args` would result in a runtime error.

**Example**: I once tried changing the method signature in a project, and the JVM couldn't recognize the entry point, leading to a runtime error.

### 24. What happens if I don’t make the `main` method static?
* **What**: If the `main` method is not static, the JVM will throw an error since it cannot call a non-static method without creating an instance of the class first.

* **Why**: The `main` method is the starting point of the program and must be accessible without creating an instance of the class.

* **How**: The JVM needs to execute it without needing an object of the class.

**Example**: In a test scenario, I mistakenly omitted the `static` keyword in a project, and the application failed to start because the JVM couldn’t access the method directly.

### 25. Difference between final and finally?
* **What**: `final` and `finally` are related to different aspects of Java.

* **Why**: They are used in different contexts for various purposes.

* **How**:

    * `final`: Used to define constants, prevent method overriding, or prevent inheritance of a class.

    * `finally`: A block of code that is always executed after a `try` block, regardless of whether an exception occurs or not.

**Example**: In a database operation project, I used `final` for constant values (e.g., database URLs) and a `finally` block to close the connection to the database, ensuring it gets closed whether or not an exception occurs.

### 26. What is a singleton?
* **What**: A singleton is a design pattern that ensures a class has only one instance and provides a global point of access to it.

* **Why**: This pattern is useful when exactly one instance of a class is required to control actions like database connections.

* **How**: The class should have a private constructor and a static method to provide access to the single instance.

**Example**: In a logging system I developed, I implemented the singleton pattern for the Logger class, ensuring only one instance of the `logger` existed across the entire application.

### 27. What is the garbage collector? Can you force garbage collection?
* **What**: The garbage collector in Java automatically removes objects from memory that are no longer in use, freeing up resources.

* **Why**: It helps manage memory and avoids memory leaks by automatically reclaiming memory from objects that are no longer referenced.

* **How**: The JVM handles garbage collection, but you can suggest it by calling `System.gc()`, though it is not guaranteed that it will execute.

**Example**: In a project dealing with large data sets, we optimized memory usage by relying on the garbage collector to clean up unused objects, allowing the application to run more efficiently.

### 28. What is unit testing? How do we do it in Java?
* **What**: Unit testing involves testing individual units or components of a program in isolation to ensure they behave as expected.

* **Why**: It helps detect bugs early in development and ensures the reliability of each part of the application.

* **How**: In Java, unit testing is commonly done using frameworks like JUnit or TestNG.

**Example**: In a project where I developed a banking system, I wrote unit tests using JUnit to verify that all account operations like deposits and withdrawals worked correctly.

### 29. Have knowledge of the Collections API (List, Set, Queue, good idea to have an example of a concrete Class for each of these)
* **What**: The Java Collections Framework provides interfaces and classes that allow you to store and manipulate groups of data.

* **Why**: It simplifies the management of data structures like lists, sets, and queues.

* **How**:

    * **List**: A collection that allows duplicates and maintains order. Example: `ArrayList`.

    * **Set**: A collection that does not allow duplicates. Example: `HashSet`.

    * **Queue**: A collection that follows the FIFO (First In First Out) principle. Example: `LinkedList`.

**Example**: In a scheduling system, I used a `Queue` to manage tasks to be processed in order, an `ArrayList` to store user tasks (allowing duplicates), and a `HashSet` to store unique task IDs.

### 30. Array vs ArrayList? How to get the length of each?
* **What**: Arrays and `ArrayList` are both used to store elements, but they have key differences.

* **Why**: `ArrayList` is more flexible but requires more memory, while arrays are more efficient for fixed-size collections.

* **How**:

    * **Array**: Has a fixed size, accessed with an index. Use `.length` to get the size.

    * **ArrayList**: Dynamic in size, elements can be added or removed. Use `.size()` to get the size.

**Example**: In a project that dealt with managing a list of users, I used an `ArrayList` for dynamic resizing as users registered, while I used an array to store the fixed number of departments.

### 31. How can I remove duplicate elements from a List? (tricky one with multiple solutions, but I'd just say convert the List into a Set)
* **What**: Removing duplicates from a `List` ensures that only unique elements are retained.

* **Why**: This is useful when you need to maintain uniqueness in a collection without manually checking each element.

* **How**: The easiest approach is to convert the `List` to a `Set` since a `Set` automatically eliminates duplicates. Alternatively, you can use Java streams for more flexibility.

**Example**: In a project where I processed a list of user emails, I used `HashSet` to remove duplicates like this:

```java
List<String> emails = Arrays.asList("user1@example.com", "user2@example.com", "user1@example.com");
Set<String> uniqueEmails = new HashSet<>(emails);
```
This ensured that only unique emails remained.

### 32. HashTable vs HashMap?
* **What**: Both `HashTable` and `HashMap` are used to store key-value pairs, but they differ in synchronization and performance.

* **Why**: Understanding their differences helps you choose the right one based on concurrency requirements.

* **How**:

    * `HashTable`: Synchronized and thread-safe, but slower because of the synchronization overhead.

    * `HashMap`: Not synchronized and not thread-safe, but faster than `HashTable` in single-threaded applications.

**Example**: In a multi-threaded application I worked on, I used `Hashtable` when I needed thread safety for accessing shared data, whereas in a single-threaded application, I used `HashMap` for faster performance.

### 33. What is an Optional?
* **What**: `Optional` is a container object used to represent a value that may or may not be present.

* **Why**: It helps avoid `NullPointerExceptions` and makes the code more readable and maintainable.

* **How**: You can use `Optional.of()`, `Optional.empty()`, or `Optional.ofNullable()` to create an Optional object and then use methods like `ifPresent()` to perform actions only if the value is present.

**Example**: In a project where I fetched user data, I used `Optional` to handle cases where the user might not be found in the database:

```java

Optional<User> user = Optional.ofNullable(userRepository.findById(userId));
user.ifPresent(u -> System.out.println("User found: " + u.getName()));
```
### 34. Threads/Runnable
* **What**: `Thread` and `Runnable` are both used to create concurrent tasks in Java.

* **Why**: They help execute multiple tasks simultaneously, improving the responsiveness and performance of applications.

* **How**:

    * `Thread`: You can extend the `Thread` class and override its `run()` method.

    * `Runnable`: You implement the `Runnable` interface and define the `run()` method, which can then be passed to a `Thread` object.

**Example**: In a video processing project, I used `Runnable` to execute multiple tasks simultaneously. Here’s a simplified version:

```java

Runnable task = () -> System.out.println("Processing video...");
Thread thread = new Thread(task);
thread.start();
```
### 35. Lambdas/Functional Interfaces
* **What**: Lambdas are a way to express instances of single-method interfaces (functional interfaces) in a more concise and readable manner.

* **Why**: They simplify code by reducing boilerplate and promoting functional programming.

* **How**: A lambda expression implements the abstract method of a functional interface. A functional interface is an interface with just one abstract method.

**Example**: In a filtering operation on a list of products, I used a lambda to define the condition:

```java

List<Product> products = Arrays.asList(new Product("Phone", 500), new Product("Laptop", 1000));
products.stream().filter(p -> p.getPrice() > 600).forEach(System.out::println);
```
### 36. What is the Reflection API?
* **What**: The Reflection API allows you to inspect or modify the runtime behavior of classes, methods, fields, and constructors.

* **Why**: It is useful when you need to work with classes dynamically (e.g., loading classes at runtime or invoking methods without knowing them in advance).

* **How**: Using `Class.forName()`, `Method.invoke()`, and other methods, you can interact with classes and methods at runtime.

**Example**: In a plugin-based architecture, I used reflection to dynamically load and invoke methods from external modules:

```java

Class<?> clazz = Class.forName("com.example.Module");
Method method = clazz.getMethod("execute");
method.invoke(clazz.newInstance());
```
### 37. What is method reference syntax?
* **What**: Method reference syntax is a shorthand way to refer to a method of a class or an instance.

* **Why**: It makes the code cleaner and easier to understand by reducing the verbosity of lambda expressions.

* **How**: You can refer to a method directly using `ClassName::methodName` or `instance::methodName`.

* **Example**: Instead of using a lambda like `x -> System.out.println(x)`, you can use a method reference:

```java

List<String> names = Arrays.asList("Alice", "Bob", "Charlie");
names.forEach(System.out::println);  // Method reference
```
### 38. What are streams? Intermediate vs Terminal operations?
* **What**: Streams provide a way to process sequences of elements in a functional style. They allow you to perform complex data manipulations on collections.

* **Why**: Streams simplify working with collections, allowing operations like filtering, mapping, and reducing to be done declaratively.

* **How**:

    * **Intermediate operations**: Operations that return a new stream and allow chaining (e.g., filter(), map()).

    * **Terminal operations**: Operations that produce a result or side effect and trigger the processing of the stream (e.g., forEach(), collect()).

**Example**: In a customer management project, I used streams to filter and collect data:

```java

List<Customer> customers = Arrays.asList(new Customer("Alice", 30), new Customer("Bob", 25));
List<Customer> filtered = customers.stream().filter(c -> c.getAge() > 26).collect(Collectors.toList());
```
### 39. How do you write logs in Java?
* **What**: Logging in Java is done using libraries such as `java.util.logging`, Apache Log4j, or SLF4J.

* **Why**: Logging helps you track the flow of execution and diagnose issues by recording runtime information.

* **How**: You can use a logging framework to log messages at different levels (e.g., `INFO`, `DEBUG`, `ERROR`).

**Example**: In a backend service I worked on, I used Log4j to log information about incoming requests:

```java

import org.apache.log4j.Logger;
Logger logger = Logger.getLogger(MyClass.class);
logger.info("Request received at: " + System.currentTimeMillis());
```

## SQL

### 1. Tell me about the different SQL sublanguages? Can you name some operations/statements per each sublanguage?
- **What**: SQL is divided into different sublanguages that serve distinct purposes.
- **Why**: Each sublanguage has a specific purpose in interacting with databases, and they help in performing operations like querying, modifying, and managing data.
- **How**: 
  - **DML (Data Manipulation Language)**: Used for querying and modifying data. Operations include:
    - `SELECT`, `INSERT`, `UPDATE`, `DELETE`.
  - **DDL (Data Definition Language)**: Used for defining and managing database structures (tables, schemas, etc.). Operations include:
    - `CREATE`, `ALTER`, `DROP`.
  - **DCL (Data Control Language)**: Used to control access to the database. Operations include:
    - `GRANT`, `REVOKE`.
  - **TCL (Transaction Control Language)**: Deals with transactions and operations on transactions. Operations include:
    - `COMMIT`, `ROLLBACK`, `SAVEPOINT`.

**Example**: In a recent project, I used `SELECT` to query records, `INSERT` to add new entries, and `CREATE` to define new tables and `ALTER` to modify existing columns.

### 2. How can you change a table's columns without dropping and recreating it?
- **What**: You can modify the columns of an existing table without dropping it using the `ALTER TABLE` statement.
- **Why**: It helps avoid losing data or having to rebuild the table.
- **How**: 
  - **To add a column**: `ALTER TABLE table_name ADD column_name datatype;`
  - **To modify a column**: `ALTER TABLE table_name MODIFY COLUMN column_name datatype;`
  - **To drop a column**: `ALTER TABLE table_name DROP COLUMN column_name;`

**Example**: In a project where I was updating a user database, I added a `birthdate` column to the `users` table like this:
```sql
ALTER TABLE users ADD birthdate DATE;
```
### 3. How do you create a table in PostgreSQL?
* **What**: You can create a table in PostgreSQL using the `CREATE TABLE` statement.

* **Why**: This is essential for defining the structure of your data in a relational database.

* **How**:

```sql
CREATE TABLE table_name (
  column1 datatype CONSTRAINTS,
  column2 datatype CONSTRAINTS,
  ...
);
```
**Example**: I created a `students` table in a project like this:

```sql
CREATE TABLE students (
  student_id SERIAL PRIMARY KEY,
  first_name VARCHAR(50),
  last_name VARCHAR(50),
  birthdate DATE
);
```
### 4. How do you define foreign keys in PostgreSQL?
* **What**: A foreign key is used to link two tables together, ensuring referential integrity.

* **Why**: Foreign keys help maintain data consistency by enforcing relationships between tables.

* **How**:

```sql
ALTER TABLE child_table
ADD CONSTRAINT fk_name
FOREIGN KEY (column_name) 
REFERENCES parent_table (parent_column);
```
**Example**: In a project where I created a `orders` table referencing a `customers` table, I defined the foreign key as:

```sql
ALTER TABLE orders
ADD CONSTRAINT fk_customer_id
FOREIGN KEY (customer_id)
REFERENCES customers (customer_id);
```

### 5. How to select all from a DB?
* **What**: To select all rows from a database, you use the `SELECT *` statement.

* **Why**: This is useful when you want to retrieve all data from a table without applying any filters.

* **How**:

```sql
SELECT * FROM table_name;
```
**Example**: In a project where I was displaying all records from the `employees` table, I used:

```sql
SELECT * FROM employees;
```

### 6. How to filter the results of a select? (where clause)
* **What**: To filter the results of a `SELECT` query, you use the `WHERE` clause.

* **Why**: The `WHERE` clause allows you to specify conditions that the data must meet.

* **How**:

```sql
SELECT column1, column2 FROM table_name
WHERE condition;
```
**Example**: In a project tracking orders, I filtered orders that were placed after a certain date:

```sql
SELECT order_id, order_date FROM orders
WHERE order_date > '2023-01-01';
```

### 7. What is a Transaction and what are the ACID properties?
* **What**: A transaction is a sequence of operations that are treated as a single unit of work.

* **Why**: Transactions ensure that a set of operations are completed successfully or not at all, ensuring data consistency.

* **How**: The ACID properties are:

    * **Atomicity**: The transaction is all-or-nothing.

    * **Consistency**: The transaction takes the database from one valid state to another.

    * **Isolation**: Transactions are isolated from each other.

    * **Durability**: Once a transaction is committed, it is permanent.

**Example**: In a banking project, I used transactions to transfer money between accounts, ensuring that both withdrawal and deposit happen together or not at all.

### 8. Tell me about the normal forms you know
* **What**: Normalization is the process of organizing data to reduce redundancy and improve integrity. Normal forms define rules for this process.

* **Why**: Normalizing data ensures that it is stored efficiently and consistently.

* **How**:

    * **1NF (First Normal Form)**: Data is stored in tables with no repeating groups or arrays.

    * **2NF (Second Normal Form)**: Data is in 1NF, and all non-key attributes are fully dependent on the primary key.

    * **3NF (Third Normal Form)**: Data is in 2NF, and all attributes are directly dependent on the primary key, eliminating transitive dependencies.

**Example**: I normalized a database in a student management system, breaking down data into multiple tables to avoid redundancy.

### 9. Name and describe some SQL joins
* **What**: Joins are used to combine rows from two or more tables based on a related column.

* **Why**: They allow you to perform complex queries that involve multiple tables.

* **How**:

    * **INNER JOIN**: Returns rows when there is a match in both tables.

    * **LEFT JOIN** (or LEFT OUTER JOIN): Returns all rows from the left table and matched rows from the right table.

    * **RIGHT JOIN** (or RIGHT OUTER JOIN): Returns all rows from the right table and matched rows from the left table.

    * **FULL JOIN** (or FULL OUTER JOIN): Returns rows when there is a match in either table.

**Example**: In a project with customers and orders, I used an `INNER JOIN` to list customers and their orders:

```sql
SELECT customers.name, orders.order_id
FROM customers
INNER JOIN orders
ON customers.customer_id = orders.customer_id;
```

### 10. What SQL functions are you aware of? Two different types?
* **What**: SQL functions are used to perform operations on data and return a result.

* **Why**: They help process data and perform operations like aggregation or transformations.

* **How**:

    * **Aggregate Functions**: Operate on a set of rows and return a single value. Examples: `COUNT()`, `SUM()`, `AVG()`, `MAX()`, `MIN()`.

    * **Scalar Functions**: Operate on a single value and return a single value. Examples: `UPPER()`, `LOWER()`, `CONCAT()`, `NOW()`.

**Example**: I used `COUNT()` to find the number of orders for each customer:

```sql
SELECT customer_id, COUNT(order_id)
FROM orders
GROUP BY customer_id;
```

### 11. What does GROUP BY do in SQL?
* **What**: The `GROUP BY` clause groups rows that have the same values in specified columns into summary rows.

* **Why**: It is commonly used with aggregate functions to perform operations like counting or summing grouped data.

* **How**:

```sql
SELECT column, AGGREGATE_FUNCTION(column)
FROM table_name
GROUP BY column;
```
**Example**: In a project analyzing sales, I grouped sales data by `store_id` and calculated the total sales for each store:

```sql
SELECT store_id, SUM(sales_amount)
FROM sales
GROUP BY store_id;
```

### 12. What is a view in SQL?
* **What**: A view is a virtual table that represents the result of a stored query.

* **Why**: Views help simplify complex queries and can be used to encapsulate data from one or more tables.

* **How**:

```sql
CREATE VIEW view_name AS
SELECT column1, column2
FROM table_name
WHERE condition;
```
**Example**: I created a view in a sales system to display the total sales per store:

```sql
CREATE VIEW total_sales AS
SELECT store_id, SUM(sales_amount) AS total_sales
FROM sales
GROUP BY store_id;
```
## HTTP

### 1. What is HTTP?
- **What**: HTTP (Hypertext Transfer Protocol) is a protocol used for transferring data over the web.
- **Why**: It defines how messages are formatted and transmitted between clients (such as browsers) and servers.
- **How**: HTTP operates over a request-response model. Clients send HTTP requests, and servers send HTTP responses.

**Example**: In a recent web project, I used HTTP to fetch data from an API endpoint using a `GET` request and display the result in the frontend.

### 2. What is an API?
- **What**: An API (Application Programming Interface) is a set of rules and protocols that allow different software applications to communicate with each other.
- **Why**: APIs allow systems to interact with one another, enabling the integration of different services and functionalities.
- **How**: APIs can be accessed through HTTP requests and generally return data in formats like JSON or XML.

**Example**: In an e-commerce project, I integrated a payment gateway API to handle transactions between the user and the payment provider.

### 3. What are https status codes? Example of different types of http status codes?
- **What**: HTTP status codes are three-digit codes returned by the server to indicate the result of an HTTP request.
- **Why**: They provide information about the success or failure of an HTTP request.
- **How**: HTTP status codes are divided into five classes:
  - **1xx** (Informational): The request was received, and the process is continuing (e.g., `100 Continue`).
  - **2xx** (Success): The request was successfully processed (e.g., `200 OK`, `201 Created`).
  - **3xx** (Redirection): Further action is needed to complete the request (e.g., `301 Moved Permanently`).
  - **4xx** (Client Error): The request contains bad syntax or cannot be fulfilled (e.g., `404 Not Found`, `400 Bad Request`).
  - **5xx** (Server Error): The server failed to fulfill a valid request (e.g., `500 Internal Server Error`).

**Example**: While working on a project with an API, I encountered a `404 Not Found` error when the requested endpoint was incorrect, and a `200 OK` when the request was successful.

### 4. What are https verbs? Example of different types of http verbs?
- **What**: HTTP verbs (also known as HTTP methods) define the actions that can be performed on resources in a web application.
- **Why**: They are essential in RESTful APIs to specify the operation to be performed.
- **How**: The most common HTTP verbs include:
  - **GET**: Retrieve data from the server (e.g., fetching a resource).
  - **POST**: Send data to the server to create a resource (e.g., submitting a form).
  - **PUT**: Update a resource on the server (e.g., modifying user details).
  - **DELETE**: Remove a resource from the server.
  - **PATCH**: Partially update a resource.

**Example**: In an API I developed, I used `GET` to fetch user data, `POST` to add a new user, and `DELETE` to remove a user from the system:
```javascript
// Example GET request to fetch user data
fetch('/api/users/1', { method: 'GET' })
  .then(response => response.json())
  .then(data => console.log(data));
```
### 5. What is postman used for?
* **What**: Postman is a popular API development tool used to test and interact with APIs.

* **Why**: It helps developers and testers send HTTP requests, view responses, and debug APIs.

* **How**: Postman allows you to easily create requests with different HTTP methods, pass parameters, set headers, and view the response status, headers, and body.

**Example**: In a recent project, I used Postman to test API endpoints during development by sending different types of requests (e.g., `GET`, `POST`) and verifying the responses.

## Spring

### 1. What is Spring? Spring Boot?
- **What**: Spring is a comprehensive framework for building Java applications, primarily used for building web applications, microservices, and enterprise-level applications. Spring Boot is a part of the Spring Framework that simplifies the setup and configuration of Spring applications by providing defaults for various configurations.
- **Why**: Spring helps manage the complexities of enterprise applications, offering features like dependency injection, transaction management, and aspect-oriented programming.
- **How**: Spring Boot makes it easier to create stand-alone, production-grade applications by providing embedded servers, automatic configuration, and minimal configuration requirements.

**Example**: In a recent microservices project, I used Spring Boot to quickly set up a RESTful service with minimal configuration using embedded Tomcat.

### 2. How would you set up a Spring Boot project?
- **What**: Setting up a Spring Boot project involves creating a `pom.xml` file for Maven or `build.gradle` for Gradle, and including the required Spring Boot dependencies.
- **Why**: This setup enables the application to start with all the default configurations and components needed to run a Spring Boot application.
- **How**:
  1. You can use **Spring Initializr** to generate a skeleton project.
  2. Add dependencies like `spring-boot-starter-web`, `spring-boot-starter-data-jpa`, etc., based on your requirements.
  3. Create the `@SpringBootApplication` class with the `main` method to launch the application.
  
**Example**:
```java
@SpringBootApplication
public class MyApplication {
    public static void main(String[] args) {
        SpringApplication.run(MyApplication.class, args);
    }
}
```
### 3. What are some annotations you've used? (some good ones: stereotype annotations, main method annotations, MVC, Data JPA)
* **What**: Spring provides a wide range of annotations that help simplify configuration and wiring in the application.

* **Why**: These annotations enable various functionalities in a Spring application, such as dependency injection, web requests, database interaction, etc.

* **How**:

    * **@Component**: Marks a class as a Spring Bean for automatic component scanning.

    * **@Autowired**: Injects dependencies automatically into Spring-managed beans.

    * **@Controller**: Defines a controller class in Spring MVC.

    * **@Service**: Marks a service class in the service layer.

    * **@Repository**: Indicates a data access object (DAO).

    * **@Entity**: Marks a class as a JPA entity.

    * **@SpringBootApplication**: Combines `@Configuration`, `@EnableAutoConfiguration`, and `@ComponentScan`.

### 4. What is the purpose of the @Component annotation?
* **What**: `@Component` is a Spring annotation that marks a class as a Spring-managed bean. It is used for automatic detection and wiring of components in the application context.

* **Why**: It allows Spring to manage the lifecycle of the class, including its dependencies.

* **How**: When a class is annotated with `@Component`, Spring will register it as a bean and make it available for dependency injection.

### 5. What are Spring Beans?
* **What**: Spring Beans are objects that are managed by the Spring IoC (Inversion of Control) container. These beans are instantiated, configured, and managed by Spring.

* **Why**: Beans enable loose coupling and dependency injection, which makes applications more modular and maintainable.

* **How**: Beans can be created through annotations like `@Component`, `@Service`, `@Repository`, etc., or via XML configuration.

### 6. What Bean Scopes are you aware of?
* **What**: Bean scopes define the lifecycle of a Spring Bean in the application context.

* **Why**: Scopes help manage the number of instances created for a bean and its lifespan.

* **How**:

    * **Singleton**: One instance per Spring container (default scope).

    * **Prototype**: A new instance is created each time the bean is requested.

    * **Request**: A new instance is created for each HTTP request.

    * **Session**: A new instance is created for each HTTP session.

    * **Application**: One instance per ServletContext.

### 7. Describe Spring MVC Controllers?
* **What**: Spring MVC Controllers are classes that handle HTTP requests in a Spring Web application.

* **Why**: They enable the separation of concerns between the model, view, and controller in a web application.

* **How**: Controllers are annotated with `@Controller` or `@RestController`, and methods within them are mapped to specific HTTP requests using annotations like `@RequestMapping`.

### 8. What is a "REST api"?
* **What**: A RESTful API (Representational State Transfer) is an architectural style for designing networked applications.

* **Why**: It relies on stateless communication and standard HTTP methods for CRUD operations, making it scalable and flexible.

* **How**: REST APIs use HTTP methods like `GET`, `POST`, `PUT`, `DELETE`, and are typically structured around resources (objects) that are represented in a certain format, like JSON.

**Example**: A REST API for managing books might have endpoints like:

* `GET /books` (retrieve all books)

* `POST /books` (add a new book)

* `PUT /books/{id}` (update a book)

* `DELETE /books/{id}` (delete a book)

### 9. How would you handle HTTP calls/mappings using Spring?
* **What**: HTTP calls and mappings in Spring are handled using Spring MVC's `@RequestMapping` and other specific annotations like `@GetMapping`, `@PostMapping`, `@PutMapping`, and `@DeleteMapping`.

* **Why**: These annotations simplify the process of mapping HTTP requests to Java methods.

* **How**:

Use `@RequestMapping` to map a method to a specific HTTP request type and URL.

Use `@GetMapping`, `@PostMapping`, etc., for more specific mappings.

### 10. What is RestTemplate? What does it let us do?
* **What**: `RestTemplate` is a Spring class that simplifies communication with RESTful APIs by providing methods for sending HTTP requests and receiving responses.

* **Why**: It abstracts away the complexity of working with HTTP, making it easier to consume REST APIs in a Spring application.

* **How**: `RestTemplate` provides methods like `getForObject()`, `postForObject()`, etc., to perform HTTP operations.

### 11. What is Spring Data? What are the JPA annotations?
* **What**: Spring Data is a part of the Spring Framework that provides easy integration with data access technologies like JPA (Java Persistence API), JDBC, and NoSQL.

* **Why**: It simplifies database interaction by providing automatic implementations for repositories.

* **How**:

    * `@Entity`: Marks a class as a JPA entity.

    * `@Id`: Marks a field as the primary key.

    * `@GeneratedValue`: Specifies how the primary key value is generated.

    * `@Table`: Defines the table name for the entity.

### 12. What does the @Entity annotation do?
* **What**: `@Entity` marks a class as a JPA entity that is mapped to a database table.

* **Why**: This annotation enables the object-relational mapping (ORM) for the class, allowing it to be persisted in a relational database.

* **How**: The class will automatically be mapped to a table with columns corresponding to the entity's fields.

### 13. How do you handle database interactions with Spring Data?
* **What**: Spring Data provides a repository abstraction that handles database interactions for you.

* **Why**: It simplifies database operations by eliminating the need for boilerplate code.

* **How**: Define repository interfaces that extend `JpaRepository` or `CrudRepository` and Spring Data will automatically implement methods for CRUD operations.

### 14. What is Autowiring?
* **What**: Autowiring is a Spring feature that allows automatic dependency injection.

* **Why**: It reduces the need for explicit bean wiring and simplifies the code.

* **How**: You can use `@Autowired` to inject dependencies into Spring-managed beans.

### 15. What is Spring Initializer?
* **What**: Spring Initializr is a web-based tool for generating Spring Boot projects with the required dependencies.

* **Why**: It helps developers quickly set up a Spring Boot application without manually configuring the project structure.

* **How**: You can access it via start.spring.io, choose the desired dependencies, and generate a project.

**Example**: I used Spring Initializr to create a new Spring Boot project with dependencies like `Spring Web` and `Spring Data JPA` for a recent application I built.

## React/Frontend

### 1. Explain what you know about HTML and CSS?
* **What**: HTML (HyperText Markup Language) is the standard language used to create the structure of web pages, and CSS (Cascading Style Sheets) is used to control the look and feel of a webpage, including layouts, colors, fonts, and more.
* **Why**: HTML is essential for structuring content on the web, while CSS enhances the visual experience by styling the page.
* **How**: HTML defines elements such as headers, paragraphs, and images, while CSS is used to position those elements, apply styles, and create responsive designs.
  
**Example**: In a recent project, I structured the webpage with HTML and used CSS to make the site responsive on mobile devices using media queries.

## 2. What does HTML stand for?
* **What**: HTML stands for HyperText Markup Language.
* **Why**: It is the standard markup language for creating web pages and web applications.
* **How**: HTML uses tags to define the structure of content, such as headings (`<h1>`, `<h2>`), paragraphs (`<p>`), and links (`<a>`).

**Example**: 
```html
<p>This is a paragraph in HTML.</p>
```

### 3. What is a promise object?
* **What**: A promise is an object representing the eventual completion (or failure) of an asynchronous operation.

* **Why**: Promises help manage asynchronous operations and provide a cleaner alternative to callbacks, improving readability and handling errors.

* **How**: A promise has three states: pending, resolved (fulfilled), and rejected. You can use `.then()` to handle success and `.catch()` for error handling.

### 4. What is the advantage of using React as opposed to using plain JavaScript frontends?
* **What**: React is a JavaScript library for building user interfaces that offers several advantages over plain JavaScript, including better state management, reusable components, and a more declarative approach.

* **Why**: React's component-based structure makes the development process more efficient by allowing developers to reuse code and break down complex UIs into smaller parts.

* **How**: React also uses the virtual DOM, which optimizes rendering performance by updating only the necessary parts of the UI when the state changes.

**Example**: In a recent project, React allowed me to create reusable UI components like buttons and forms, which significantly reduced development time.

### 5. Tell me about the virtual DOM.
* **What**: The virtual DOM is a lightweight copy of the actual DOM (Document Object Model) that React uses to optimize updates and rendering.

* **Why**: The virtual DOM allows React to efficiently determine which parts of the real DOM need to be updated when the state of an application changes, making the application faster.

* **How**: When the state or props change, React first updates the virtual DOM, then compares it with the real DOM using a process called "reconciliation" to minimize the changes to be applied.

**Example**: I noticed a significant performance improvement in my React application when handling large lists of data, as the virtual DOM minimized unnecessary re-rendering.

### 6. What is TSX? (They may ask about JSX, just remind them we used React TypeScript and TSX, not JSX)
* **What**: TSX (TypeScript JSX) is a syntax extension for TypeScript that allows you to write React components using TypeScript with JSX syntax.

* **Why**: TSX allows the type-checking benefits of TypeScript while still using JSX for writing UI components in React.

* **How**: Just like JSX, TSX allows embedding HTML-like syntax in JavaScript/TypeScript files, but with TypeScript features such as static typing.

### 7. What are components in React?
* **What**: In React, components are reusable building blocks that encapsulate a piece of the user interface and its logic.

* **Why**: Components enable code reusability, modularity, and easier maintenance, making React applications scalable and efficient.

* **How**: Components can be functional (stateless) or class-based (stateful), and they return JSX that defines the UI.

### 8. How do you create a component in React?
* **What**: In React, a component can be created either as a function component or a class component.

* **Why**: Function components are now the modern standard due to their simplicity and the use of hooks.

* **How**: A function component is defined as a JavaScript (or TypeScript) function that returns JSX, while a class component is defined as a class extending `React.Component`.

### 9. What is "export" in React?
* **What**: `export` is a keyword in JavaScript/TypeScript that allows you to expose functions, objects, or classes from a module so they can be imported elsewhere.

* **Why**: It enables modularity in your codebase, allowing you to organize code into separate files and re-use components.

* **How**: You can export a component or function with `export default` (for the default export) or just `export` (for named exports).

### 10. What is props and state?
* **What**: `props` (short for properties) are used to pass data from parent to child components, while `state` is used to manage internal data within a component.

* **Why**: `props` allow components to be dynamic and reusable by passing different values, while `state` enables components to respond to user interactions and changes over time.

* **How**: `props` are passed into a component and cannot be changed by the component itself, whereas `state` can be modified using `setState` or `useState`.

### 11. Can you send props from child to parent?
* **What**: In React, data flows from parent to child via `props`. However, to send data from child to parent, you can use callback functions passed down as props from the parent to the child.

* **Why**: React follows a unidirectional data flow, so parents send props down to children, and children communicate with parents using functions.

* **How**: You pass a function from the parent to the child as a prop, and the child calls that function with the data it wants to send back.

### 12. How does Routing work in React? How did you create routes?
* **What**: In React, routing is handled by the `react-router` library. It allows you to navigate between different components based on the URL.

* **Why**: It enables single-page applications to have multiple views without reloading the page.

* **How**: You define routes using `<Route />` components inside a `<Router />` container. Each route associates a path with a component that is rendered when that path is matched.

### 13. Describe the function component hooks you've used
* **What**: Hooks are functions that allow you to "hook into" React's state and lifecycle features from function components.

* **Why**: They make function components more powerful and allow them to manage state, side effects, context, etc.

* **How**: Commonly used hooks include:

    * **useState**: For managing local state.

    * **useEffect**: For running side effects like data fetching, subscriptions, or DOM manipulation.

    * **useContext**: For accessing context data.

### 14. What is axios? What have you used it for?
* **What**: Axios is a promise-based HTTP client for making requests to external APIs or servers.

* **Why**: It simplifies handling asynchronous HTTP requests and responses, including JSON data, with built-in support for promises and error handling.

* **How**: Axios is commonly used to fetch data from an API using `axios.get()` or `axios.post()`.

### 15. How can I render a list of elements in React?
* **What**: In React, you can render a list of elements by mapping over an array of data and returning JSX for each item.

* **Why**: This allows you to dynamically generate components based on data, such as rendering a list of users or items.

* **How**: Use `Array.prototype.map()` to iterate over the data and return JSX.

### 16. How can I conditionally render content in React?
* **What**: You can conditionally render content in React using JavaScript's conditional operators, such as `if`, ternary operators, or logical operators.

* **Why**: Conditional rendering allows you to display different UI elements based on the application state or props.

* **How**: Use `if` statements or ternary operators inside your JSX to decide what should be rendered.

**Example**:

```tsx
const isLoggedIn = true;

const WelcomeMessage = () => {
  return (
    <div>
      {isLoggedIn ? <p>Welcome back!</p> : <p>Please log in.</p>}
    </div>
  );
};
```

### 17. Good to know: Class Component (old) vs Function Component (modern)
* **What**: Class components were the original way to define components in React, using `class` syntax. Function components are the modern standard and are used with hooks for state and lifecycle management.

* **Why**: Function components are simpler, more concise, and allow hooks, which makes them the preferred choice in modern React development.

* **How**: Function components have become the dominant pattern, while class components are still supported for legacy codebases.

**Example**:

```tsx
// Class Component
class MyComponent extends React.Component {
  render() {
    return <div>Class Component</div>;
  }
}

// Function Component
const MyFunctionComponent = () => {
  return <div>Function Component</div>;
};
```

## Cloud/SDLC

### 1. What Agile processes have you used?
* **What**: Agile is a methodology that emphasizes iterative development, flexibility, and close collaboration with stakeholders. It includes various frameworks like Scrum, Kanban, and Lean.
* **Why**: Agile is popular for its adaptability, allowing teams to respond to changes and deliver value incrementally.
* **How**: In my recent project, we used **Scrum**, where we worked in two-week sprints, held daily standups, and conducted sprint reviews and retrospectives.

**Example**: In my project, I participated in sprint planning meetings, where we discussed the work to be done for the sprint, and I helped create and manage user stories in our project’s backlog.

### 2. What is retrospective in Agile?
* **What**: A retrospective is a meeting held at the end of each sprint in Agile, where the team reflects on the past sprint, discussing what went well, what could be improved, and how to implement changes.
* **Why**: Retrospectives aim to improve team processes and work habits by fostering open communication and continuous improvement.
* **How**: During retrospectives, the team discusses challenges faced during the sprint and agrees on actionable steps to improve in the next sprint.

**Example**: In one of our retrospectives, the team realized that our code review process was too slow, so we agreed to adopt a more streamlined review workflow to speed up development.

### 3. What AWS services have you used?
* **What**: AWS (Amazon Web Services) offers a wide range of cloud services for computing, storage, databases, machine learning, and more.
* **Why**: AWS is widely used for its scalability, reliability, and cost-effectiveness for hosting and managing cloud applications.
* **How**: In my projects, I’ve used services like **EC2** for virtual machines, **S3** for object storage, **RDS** for relational databases, and **Lambda** for serverless computing.

**Example**: In a recent project, I used **EC2** to host a backend API and **S3** to store images uploaded by users. I also utilized **RDS** to manage user data.

### 4. How do you host projects on AWS?
* **What**: Hosting projects on AWS typically involves selecting the right AWS services to deploy and manage your application, such as EC2 instances, Lambda functions, or Elastic Beanstalk.
* **Why**: AWS allows developers to focus on building applications while AWS manages the underlying infrastructure, scaling, and security.
* **How**: I’ve hosted projects using **Elastic Beanstalk**, which simplifies deployment and scaling, or manually deploying an application to an **EC2** instance.

**Example**: For one of my projects, I used **Elastic Beanstalk** to deploy a Node.js API. It handled provisioning, load balancing, and scaling automatically.

### 5. Briefly describe IaaS, PaaS, SaaS and describe one of them more in-depth.
* **What**: 
  * **IaaS (Infrastructure as a Service)**: Provides virtualized computing resources over the internet (e.g., AWS EC2, Azure VMs).
  * **PaaS (Platform as a Service)**: Offers a platform that allows developers to build and deploy applications without managing the underlying infrastructure (e.g., AWS Elastic Beanstalk, Heroku).
  * **SaaS (Software as a Service)**: Delivers software applications over the internet, typically on a subscription basis (e.g., Google Workspace, Dropbox).
* **Why**: These services allow businesses to reduce the overhead of managing infrastructure, improve scalability, and provide software solutions on-demand.
* **How**: 
  * For **IaaS**, I’ve used **AWS EC2** to manage virtual machines.
  * For **PaaS**, I’ve used **Heroku** to quickly deploy a web application without worrying about the underlying infrastructure.
  * For **SaaS**, I frequently use **Google Docs** for real-time collaboration.

**Example**: I worked on a project where we used **AWS Elastic Beanstalk (PaaS)** to deploy our backend, allowing us to focus more on our code without managing the servers.

### 6. Know the SOLID design principles
* **What**: SOLID is an acronym for five design principles that help developers create more maintainable and flexible software:
  1. **S** - Single Responsibility Principle (SRP)
  2. **O** - Open/Closed Principle (OCP)
  3. **L** - Liskov Substitution Principle (LSP)
  4. **I** - Interface Segregation Principle (ISP)
  5. **D** - Dependency Inversion Principle (DIP)
* **Why**: SOLID principles aim to reduce software complexity, improve readability, and make systems easier to maintain and extend.
* **How**: 
  * In a recent project, I used the **Single Responsibility Principle (SRP)** to ensure that each class had one reason to change. This helped improve code modularity.
  * I applied the **Open/Closed Principle (OCP)** by writing extensible code that could be modified without altering existing functionality, such as using abstract classes and interfaces.

**Example**: In one of my applications, I used the **Dependency Inversion Principle (DIP)** by depending on abstractions instead of concrete classes. This made it easier to swap out implementations and facilitated unit testing.

## Git

### 1. What is your experience with GitHub?
* **What**: GitHub is a platform that uses Git for version control and provides collaborative tools for software development, such as repositories, pull requests, and issue tracking.
* **Why**: GitHub is widely used in open-source and enterprise projects to manage source code, track changes, and collaborate with other developers.
* **How**: In my previous projects, I used GitHub for managing code repositories, collaborating with team members, reviewing pull requests, and tracking issues. I also utilized GitHub Actions for automating CI/CD pipelines.

**Example**: In my last team project, I was responsible for maintaining the repository on GitHub, creating branches, reviewing pull requests, and ensuring the code met the project's standards.

### 2. Basic commands (pushing to repo, pulling from repo)
* **What**: Basic Git commands allow you to interact with a Git repository, push changes to a remote server, and pull updates from it.
* **Why**: These commands are essential for sharing code and collaborating with other developers on the same project.
* **How**: 
  * **git clone**: Used to clone a repository from a remote server.
  * **git add**: Stages changes to be committed.
  * **git commit**: Saves the changes locally with a commit message.
  * **git push**: Pushes the local commits to a remote repository.
  * **git pull**: Fetches and merges changes from a remote repository to the local repo.

**Example**: In my recent project, I used the following commands: 
```bash
git clone <repository_url>
git add .
git commit -m "Implemented feature X"
git push origin main
```

### 3. What is a branch?
What: A branch in Git allows you to diverge from the main line of development (usually `main` or `master`) to work on a feature or fix independently, without affecting the main codebase.

* **Why**: Branches provide a way to isolate changes and enable parallel development, making collaboration more efficient and reducing the risk of conflicts.

* **How**: To create a branch, you can use the `git branch <branch_name>` command, and then switch to that branch with `git checkout <branch_name>`.

### 4. How to merge a branch?
* **What**: Merging in Git is the process of integrating changes from one branch into another, typically from a feature branch into the main branch.

* **Why**: Merging ensures that the changes made in a separate branch are incorporated into the main codebase, allowing for a collaborative and unified project.

* **How**:

    * First, switch to the branch you want to merge changes into (usually `main` or `master`).

    * Then, use the `git merge <branch_name>` command to merge the changes from the feature branch.

### 5. What is CI/CD?
* **What**: CI/CD stands for Continuous Integration and Continuous Deployment/Delivery. It's a practice in modern software development where code changes are automatically tested and deployed.

* **Why**: CI/CD automates the process of integrating new code, running tests, and deploying applications, ensuring faster delivery, fewer bugs, and greater reliability.

* **How**:

    * **CI (Continuous Integration)** involves automatically testing code changes as they are integrated into the repository.

    * **CD (Continuous Deployment/Delivery)** automatically deploys the code to a production or staging environment after passing tests.

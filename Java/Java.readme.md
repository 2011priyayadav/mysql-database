# Core Java
----
## Java Comments
### Types of Comments in Java

| Comment Type         | Syntax               | Example                                                                 |
|----------------------|----------------------|-------------------------------------------------------------------------|
| Single-line Comment  | `// comment`         | `// This is a single-line comment`<br>`int age = 25; // Age of user`   |
| Multi-line Comment   | `/* ... */`          | `/* This is a multi-line comment`<br>`   explaining multiple lines */`  |
| Documentation Comment| `/** ... */`         | `/**`<br>` * This method prints name`<br>` */`<br>`public void printName() {}` |

---

### Example Showing All 
```java
/**
 * This program demonstrates all types of comments in Java.
 */
public class CommentExample {
    public static void main(String[] args) {
        // This is a single-line comment
        int x = 10;

        /* This is a multi-line comment
           explaining the following calculation */
        int y = x * 2;

        System.out.println(y); // Output will be 20
    }
}
```
----


## Variable in Java
## What is a Variable in Java?
*A variable in Java is a named memory location used to store data that can change during the execution of a program.*
## Rules for Variables
- Must begin with a letter (A–Z or a–z), dollar sign ($), or underscore (_)
- Cannot start with a number
- Cannot use Java reserved keywords (like class, int, new, etc.)
- Java is case-sensitive: age and Age are different

## Example:
```java
int age = 25;
int: Data type
```
- age: Variable name
- 25: Value assigned to the variable

## Types of Variables in Java
*Java has three main types of variables:*
- **Local Variable**	Inside a method/block	Only within that block/method	No default
- **Instance Variable**	Inside a class (non-static)	Per object	Depends on type
- **Static Variable**	Inside a class (static)	Shared across all objects	Depends on type
----

## Java Data Types for Variables
## Java Data Types for Variables

| Data Type     | Description                                                | Example               |
|---------------|------------------------------------------------------------|-----------------------|
| byte          | Stores whole numbers from -128 to 127                      | `byte b = 100;`       |
| short         | Stores whole numbers from -32,768 to 32,767                | `short s = 1000;`     |
| int           | Integer values from -2,147,483,648 to 2,147,483,647        | `int x = 10;`         |
| long          | Large integers from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 | `long l = 10000000000L;` |
| float         | Decimal numbers (single precision, 6-7 digits)             | `float f = 3.14f;`    |
| double        | Decimal numbers (double precision, ~15 digits)             | `double d = 9.99;`    |
| boolean       | Stores true or false                                       | `boolean b = true;`   |
| char          | Stores a single character (16-bit Unicode)                 | `char c = 'A';`       |
| String (class)| Stores a sequence of characters (object, not primitive)    | `String s = "Java";`  |


## Complete Example (All Variable Types)
```java
public class Employee {
    // Instance variable
    String empName;

    // Static variable
    static String company = "TCS";

    void setEmployee(String name) {
        // Local variable
        int id = 101;
        empName = name;
        System.out.println("ID: " + id + ", Name: " + empName + ", Company: " + company);
    }

    public static void main(String[] args) {
        Employee e1 = new Employee();
        e1.setEmployee("Priya");
    }
}
```
## output
- ID: 101, Name: Priya, Company: TCS
----
## Type Casting in Java
**Type Casting** in Java is the process of converting a variable from one data type to another.
There are two types of casting in Java: **Widening (implicit)** and **Narrowing (explicit)**.
### Type Casting Table

| Casting Type         | Definition                                     | Example Code                                               | Output   |
|----------------------|-----------------------------------------------|-------------------------------------------------------------|----------|
| Widening Casting     | Converting a smaller type to a larger type. Done automatically by Java. | `int num = 10;`<br>`double result = num;`<br>`System.out.println(result);` | `10.0`   |
| Narrowing Casting    | Converting a larger type to a smaller type. Requires explicit cast. May lose data. | `double num = 10.75;`<br>`int result = (int) num;`<br>`System.out.println(result);` | `10`     |


### Notes
- **Widening**: No data loss, safe conversion.
- **Narrowing**: May result in loss of precision or truncation.
- Always use parentheses `()` for **narrowing casting**.

----
## Java Operators
Operators in Java are used to perform operations on variables and values.
### Types of Java Operators

| Operator Type         | Symbol(s)           | Description                                   | Example Code                          | Output       |
|------------------------|---------------------|-----------------------------------------------|----------------------------------------|--------------|
| Arithmetic Operators   | `+ - * / %`         | Perform basic math operations                 | `int a = 10 + 5;`                      | `15`         |
| Relational Operators   | `== != > < >= <=`   | Compare two values                            | `10 > 5`                               | `true`       |
| Logical Operators      | `&& || !`           | Combine or invert boolean expressions         | `(5 > 3 && 2 < 4)`                     | `true`       |
| Assignment Operators   | `= += -= *= /=`     | Assign values to variables                    | `int x = 5; x += 3;`                   | `8`          |
| Unary Operators        | `+ - ++ -- !`       | Perform operations on a single operand        | `int x = 5; x++;`                      | `6`          |
| Bitwise Operators      | `& | ^ ~ << >> >>>` | Perform operations on bits                    | `5 & 3`                                | `1`          |
| Ternary Operator       | `? :`               | Shortcut for `if-else` condition              | `int max = (a > b) ? a : b;`           | `greater`    |

----
## Java String
## What is a String in Java?
*In Java, a String is a sequence of characters treated as an object. It is part of the java.lang package and is immutable, meaning its value cannot be changed once created*


| Type               | Description                  | Example                                   | Output    |
| ------------------ | ---------------------------- | ----------------------------------------- | --------- |
| String Literal     | Stored in string pool        | `String s = "Hello";`                     | `Hello`   |
| Using `new`        | Stored in heap               | `String s = new String("Hi");`            | `Hi`      |
| `char[]` to String | Convert char array to string | `new String(new char[]{'J','a','v','a'})` | `Java`    |
| `StringBuilder`    | Mutable, not thread-safe     | `new StringBuilder("Hi").append(" All")`  | `Hi All`  |
| `StringBuffer`     | Mutable, thread-safe         | `new StringBuffer("Hi").append(" All")`   | `Hi All`  |
| `valueOf()`        | Convert primitive to string  | `String.valueOf(123);`                    | `"123"`   |
| `format()`         | Format string                | `String.format("Age: %d", 25);`           | `Age: 25` |

## Common String Methods
| Method               | Description                   | Example                           | Output            |
| -------------------- | ----------------------------- | --------------------------------- | ----------------- |
| `length()`           | Length of string              | `"Java".length()`                 | `4`               |
| `charAt()`           | Character at index            | `"Java".charAt(1)`                | `a`               |
| `substring()`        | Substring of string           | `"Java".substring(1, 3)`          | `av`              |
| `toUpperCase()`      | Convert to uppercase          | `"java".toUpperCase()`            | `JAVA`            |
| `toLowerCase()`      | Convert to lowercase          | `"JAVA".toLowerCase()`            | `java`            |
| `equals()`           | Compare strings               | `"Java".equals("Java")`           | `true`            |
| `equalsIgnoreCase()` | Compare strings ignoring case | `"Java".equalsIgnoreCase("java")` | `true`            |
| `contains()`         | Check if contains text        | `"Hello".contains("lo")`          | `true`            |
| `replace()`          | Replace characters            | `"Test".replace('T','B')`         | `Best`            |
| `trim()`             | Remove extra spaces           | `"  Java  ".trim()`               | `Java`            |
| `split()`            | Split string by delimiter     | `"a,b,c".split(",")`              | `["a", "b", "c"]` |

## String Comparison
| Comparison Method     | Use Case                | Example                           | Result |
| --------------------- | ----------------------- | --------------------------------- | ------ |
| `==`                  | Compares memory address | `"Java" == "Java"`                | `true` |
| `.equals()`           | Compares actual value   | `"Java".equals("Java")`           | `true` |
| `.equalsIgnoreCase()` | Ignores case            | `"Java".equalsIgnoreCase("java")` | `true` |

##  String Conversion
| From → To        | Method               | Example                           | Output              |
| ---------------- | -------------------- | --------------------------------- | ------------------- |
| int → String     | `String.valueOf()`   | `String.valueOf(123)`             | `"123"`             |
| String → int     | `Integer.parseInt()` | `Integer.parseInt("123")`         | `123`               |
| String → char\[] | `.toCharArray()`     | `"Java".toCharArray()`            | `['J','a','v','a']` |
| char\[] → String | `new String(char[])` | `new String(new char[]{'A','B'})` | `"AB"`              |



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

----
## Java MATH
Java provides a built-in `Math` class in the `java.lang` package that contains methods for performing basic numeric operations such as exponentiation, rounding, square roots, trigonometry, and more.
### ✅ Definition
The `Math` class in Java provides static methods to perform common mathematical tasks. Since all methods are `static`, you do not need to create an object to use them.
**Syntax:**
```java
Math.methodName(arguments);
```
| Method              | Description                                  | Example Code              | Output       |
| ------------------- | -------------------------------------------- | ------------------------- | ------------ |
| `Math.abs(x)`       | Returns absolute (positive) value            | `Math.abs(-10)`           | `10`         |
| `Math.max(a, b)`    | Returns the greater of two values            | `Math.max(5, 9)`          | `9`          |
| `Math.min(a, b)`    | Returns the smaller of two values            | `Math.min(5, 9)`          | `5`          |
| `Math.sqrt(x)`      | Returns square root                          | `Math.sqrt(25)`           | `5.0`        |
| `Math.cbrt(x)`      | Returns cube root                            | `Math.cbrt(27)`           | `3.0`        |
| `Math.pow(a, b)`    | Returns a raised to the power of b           | `Math.pow(2, 3)`          | `8.0`        |
| `Math.round(x)`     | Rounds to the nearest whole number           | `Math.round(4.6)`         | `5`          |
| `Math.ceil(x)`      | Rounds **up** to nearest integer             | `Math.ceil(4.1)`          | `5.0`        |
| `Math.floor(x)`     | Rounds **down** to nearest integer           | `Math.floor(4.9)`         | `4.0`        |
| `Math.random()`     | Returns random number between 0.0 and 1.0    | `Math.random()`           | `0.0 to 1.0` |
| `Math.log(x)`       | Returns natural logarithm (base e)           | `Math.log(10)`            | `2.302...`   |
| `Math.log10(x)`     | Returns logarithm base 10                    | `Math.log10(100)`         | `2.0`        |
| `Math.exp(x)`       | Returns Euler’s number raised to the power x | `Math.exp(1)`             | `2.718...`   |
| `Math.sin(x)`       | Returns sine (radians)                       | `Math.sin(Math.PI/2)`     | `1.0`        |
| `Math.cos(x)`       | Returns cosine (radians)                     | `Math.cos(0)`             | `1.0`        |
| `Math.tan(x)`       | Returns tangent (radians)                    | `Math.tan(Math.PI/4)`     | `1.0`        |
| `Math.toRadians(x)` | Converts degrees to radians                  | `Math.toRadians(180)`     | `3.1415...`  |
| `Math.toDegrees(x)` | Converts radians to degrees                  | `Math.toDegrees(Math.PI)` | `180.0`      |
| `Math.signum(x)`    | Returns sign of number (-1, 0, or 1)         | `Math.signum(-5)`         | `-1.0`       |

----
## Java Booleans

### ✅ Definition

In Java, a **boolean** is a data type that can hold only **two values**: `true` or `false`. It is often used in conditional statements, loops, and logic operations.

**Syntax:**
```java
boolean isJavaFun = true;
boolean isHot = false;
```
| Concept             | Description                      | Example Code                                    | Output                                 |           |   |            |        |
| ------------------- | -------------------------------- | ----------------------------------------------- | -------------------------------------- | --------- | - | ---------- | ------ |
| Boolean Declaration | Declare a boolean variable       | `boolean isJavaFun = true;`                     | `true`                                 |           |   |            |        |
| Comparison Result   | Returns boolean after comparison | `5 > 3`                                         | `true`                                 |           |   |            |        |
| Logical AND (`&&`)  | True if both conditions are true | `(5 > 3) && (10 > 5)`                           | `true`                                 |           |   |            |        |
| Logical OR (\`      |                                  | \`)                                             | True if at least one condition is true | \`(5 < 3) |   | (10 > 5)\` | `true` |
| Logical NOT (`!`)   | Inverts boolean value            | `!(5 > 3)`                                      | `false`                                |           |   |            |        |
| Boolean in `if`     | Used in conditional statements   | `if (isJavaFun) { System.out.println("Yes"); }` | `Yes`                                  |           |   |            |        |
## Example:
```java
public class BooleanExample {
    public static void main(String[] args) {
        boolean isJavaFun = true;
        boolean isFishTasty = false;

        System.out.println(isJavaFun);          // true
        System.out.println(isFishTasty);        // false

        System.out.println(10 > 5);             // true
        System.out.println(10 < 5);             // false

        // Logical operators
        boolean result = (5 > 3) && (8 > 5);     // true
        System.out.println(result);

        // Using NOT operator
        System.out.println(!(5 > 3));           // false

        // Conditional check
        if (isJavaFun) {
            System.out.println("Java is fun!");
        }
    }
}
```
----
## Java if-else Statement

The `if-else` statement is used to make decisions in Java. It executes one block if a condition is true, otherwise another block.

### Syntax

```java
if (condition) {
    // code if true
} else {
    // code if false
}
```
## Simple if-else
```java
int age = 18;
if (age >= 18) {
    System.out.println("Eligible to vote");
} else {
    System.out.println("Not eligible");
}
```
## if-else-if Ladder
```java
int score = 85;
if (score >= 90) {
    System.out.println("Grade A");
} else if (score >= 75) {
    System.out.println("Grade B");
} else {
    System.out.println("Grade C");
}
```
## Nested if
```java
int age = 20;
boolean hasID = true;
if (age >= 18) {
    if (hasID) {
        System.out.println("Entry allowed");
    } else {
        System.out.println("ID required");
    }
} else {
    System.out.println("You must be 18+");
}
```

## Java Ternary Operator
The **ternary operator** is a shortcut for `if-else`. It is used for making quick decisions in a single line.
### Syntax
```java
variable = (condition) ? value_if_true : value_if_false;
```
----


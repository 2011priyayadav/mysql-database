# Core Java
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


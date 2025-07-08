# Core Java
## Variable in Java
## What is a Variable in Java?
*A variable in Java is a named memory location used to store data that can change during the execution of a program.*
## Example:
```java
int age = 25;
int: Data type
```
- age: Variable name
- 25: Value assigned to the variable

## Types of Variables in Java
*Java has three main types of variables:*
- Local Variable	Inside a method/block	Only within that block/method	No default
- Instance Variable	Inside a class (non-static)	Per object	Depends on type
- Static Variable	Inside a class (static)	Shared across all objects	Depends on type

## 1. Local Variable
- Declared inside methods, constructors, or blocks.
- Must be initialized before use.
- No default value assigned automatically.
## Example:
```java
public void printAge() {
    int age = 25;  // Local variable
    System.out.println(age);
}
```
## 2. Instance Variable
Declared inside a class but outside any method.
Does not have the static keyword.

Each object of the class gets its own copy.

Example:

java
Copy
Edit
public class Student {
    String name;  // Instance variable

    void setName(String n) {
        name = n;
    }

    void printName() {
        System.out.println(name);
    }
}
3. Static Variable (Class Variable)
Declared using the static keyword inside the class.

Shared among all instances of the class.

Initialized only once in memory.

Example:

java
Copy
Edit
public class Student {
    static String school = "ABC High School";  // Static variable

    void showSchool() {
        System.out.println(school);
    }
}
Access static variable using the class name:

java
Copy
Edit
Student.school;
Variable Declaration & Initialization
java
Copy
Edit
int a;        // Declaration
a = 10;       // Initialization

int b = 20;   // Declaration and initialization combined
Variable Scope
Type	Scope
Local	Within the method/block
Instance	Within the class per object
Static	Throughout the class (shared across all objects)

Java Data Types for Variables
Data Type	Description	Example
int	Integer values	int x = 10;
float	Decimal numbers (single precision)	float f = 3.14f;
double	Decimal numbers (double precision)	double d = 9.99;
boolean	True or false values	boolean b = true;
char	Single character	char c = 'A';
String (class)	Sequence of characters	String s = "Java";

Complete Example (All Variable Types)
java
Copy
Edit
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
Output:

yaml
Copy
Edit
ID: 101, Name: Priya, Company: TCS
Naming Rules for Variables (Identifiers)
Must begin with a letter (A–Z or a–z), dollar sign ($), or underscore (_)

Cannot start with a number

Cannot use Java reserved keywords (like class, int, new, etc.)

Java is case-sensitive: age and Age are different

Valid names: studentName, _count, $total
Invalid names: 2value, class, student-name

Best Practices for Variables
Use meaningful and descriptive names (e.g., totalSalary, studentAge)

Use camelCase for naming (employeeName, orderTotal)

Keep variables local if used only inside a single method

Declare constants using final and uppercase with underscores

Example:

java
Copy
Edit
final int MAX_USERS = 100;

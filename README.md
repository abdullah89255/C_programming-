# C_programming-
C is a widely-used, general-purpose programming language that was developed in the early 1970s by Dennis Ritchie at Bell Labs. It is a foundational language in computer science and is known for its efficiency, portability, and flexibility.

### Key Features of C:
1. **Low-Level Access**: C provides low-level memory access, making it suitable for system programming (e.g., operating systems, embedded systems).
2. **Portability**: C code can be compiled on different platforms with minimal changes.
3. **Rich Library Support**: Standard libraries provide a wide range of functionality.
4. **Modularity**: Code can be organized into functions, making programs easier to debug and maintain.
5. **Efficiency**: Programs written in C are highly efficient in terms of execution speed.
6. **Structured Programming**: Encourages breaking down tasks into functions for better organization and readability.

### Basic Syntax of C:
Here's a simple "Hello, World!" program in C:

```c
#include<stdio.h>

int main() {
    printf("Hello, World!\n");
    return 0;
}
```

#### Explanation:
1. **`#include<stdio.h>`**:
   - Includes the standard input/output library for functions like `printf()` and `scanf()`.

2. **`int main()`**:
   - The entry point of the program.
   - The return type `int` indicates that the program returns an integer to the operating system.

3. **`printf()`**:
   - Outputs text to the console.

4. **`return 0;`**:
   - Indicates successful execution of the program.

### Basic Concepts:
1. **Data Types**:
   - `int`: Integer (e.g., 1, 42)
   - `float`: Floating-point number (e.g., 3.14)
   - `char`: Single character (e.g., 'a')
   - `double`: Double-precision floating-point number
   - `void`: Indicates no return value or no arguments

2. **Control Structures**:
   - **Conditional Statements**: `if`, `else if`, `else`
   - **Loops**: `for`, `while`, `do-while`

3. **Functions**:
   - Break programs into reusable blocks of code.

   Example:
   ```c
   int add(int a, int b) {
       return a + b;
   }
   ```

4. **Arrays**:
   - Store multiple elements of the same type.
   ```c
   int arr[5] = {1, 2, 3, 4, 5};
   ```

5. **Pointers**:
   - Variables that store the address of other variables.
   ```c
   int x = 10;
   int *ptr = &x; // Pointer to x
   ```

6. **Structures**:
   - Group variables of different types under one name.
   ```c
   struct Point {
       int x;
       int y;
   };
   ```

In the C programming language, **data types** are used to define variables and functions with specific types of data that they can hold or operate on. C supports several data types, categorized into **basic**, **derived**, and **user-defined** types.

---

### **Basic Data Types**

1. **Integer Types (`int`)**:
   - Used to store whole numbers.
   - **Range**: Depends on the system (e.g., 32-bit system: `-2,147,483,648` to `2,147,483,647` for `int`).
   - **Size**: Typically 4 bytes.
   - Example:
     ```c
     int age = 25;
     ```

2. **Floating-point Types (`float`, `double`)**:
   - Used to store numbers with decimal points.
   - `float`: Single precision, typically 4 bytes.
   - `double`: Double precision, typically 8 bytes.
   - Example:
     ```c
     float pi = 3.14;
     double e = 2.718281828459;
     ```

3. **Character Type (`char`)**:
   - Used to store a single character (e.g., `'a'` or `'1'`).
   - Stored as an ASCII value (1 byte).
   - Example:
     ```c
     char grade = 'A';
     ```

4. **Void (`void`)**:
   - Represents "no value".
   - Often used for functions that do not return a value or take no arguments.
   - Example:
     ```c
     void displayMessage() {
         printf("Hello!");
     }
     ```

---

### **Derived Data Types**

1. **Arrays**:
   - Collection of elements of the same type.
   - Example:
     ```c
     int numbers[5] = {1, 2, 3, 4, 5};
     ```

2. **Pointers**:
   - Variables that store the memory address of another variable.
   - Example:
     ```c
     int x = 10;
     int *ptr = &x;
     ```

3. **Functions**:
   - Blocks of code designed to perform specific tasks.
   - Example:
     ```c
     int add(int a, int b) {
         return a + b;
     }
     ```

4. **Structures (`struct`)**:
   - Groups variables of different types under a single name.
   - Example:
     ```c
     struct Point {
         int x;
         int y;
     };
     ```

5. **Unions (`union`)**:
   - Similar to `struct`, but all members share the same memory location.
   - Example:
     ```c
     union Data {
         int i;
         float f;
     };
     ```

---

### **User-defined Data Types**

1. **Enumerations (`enum`)**:
   - Defines a set of named integer constants.
   - Example:
     ```c
     enum Day { MON, TUE, WED, THU, FRI, SAT, SUN };
     ```

2. **Typedef**:
   - Allows creating new names (aliases) for existing data types.
   - Example:
     ```c
     typedef unsigned int uint;
     uint age = 25;
     ```

---

### **Modifiers**

C provides **modifiers** to adjust the size and range of data types:

1. **Signed**:
   - Default for integer and character types.
   - Can store positive and negative values.
   - Example:
     ```c
     signed int x = -10;
     ```

2. **Unsigned**:
   - Stores only non-negative values.
   - Example:
     ```c
     unsigned int x = 10;
     ```

3. **Short**:
   - Reduces the size of an integer type.
   - Example:
     ```c
     short int x = 32767;
     ```

4. **Long**:
   - Increases the size of an integer type.
   - Example:
     ```c
     long int x = 100000L;
     ```

---

### **Data Type Sizes**

| **Data Type**       | **Size (in Bytes)** | **Range**                       |
|----------------------|---------------------|----------------------------------|
| `char`              | 1                   | `-128` to `127`                 |
| `unsigned char`     | 1                   | `0` to `255`                    |
| `int`               | 4                   | `-2,147,483,648` to `2,147,483,647` |
| `unsigned int`      | 4                   | `0` to `4,294,967,295`          |
| `short int`         | 2                   | `-32,768` to `32,767`           |
| `unsigned short`    | 2                   | `0` to `65,535`                 |
| `long int`          | 8                   | `-9,223,372,036,854,775,808` to `9,223,372,036,854,775,807` |
| `unsigned long`     | 8                   | `0` to `18,446,744,073,709,551,615` |
| `float`             | 4                   | Approximately `±3.4E–38` to `±3.4E+38` |
| `double`            | 8                   | Approximately `±1.7E–308` to `±1.7E+308` |

---

### Example Program Demonstrating Data Types

```c
#include<stdio.h>

int main() {
    int age = 25;
    float pi = 3.14159;
    char initial = 'A';
    unsigned int distance = 150;
    double precise_pi = 3.141592653589793;

    printf("Age: %d\n", age);
    printf("Pi: %f\n", pi);
    printf("Initial: %c\n", initial);
    printf("Distance: %u meters\n", distance);
    printf("Precise Pi: %.15lf\n", precise_pi);

    return 0;
}
```

Output:
```
Age: 25
Pi: 3.141590
Initial: A
Distance: 150 meters
Precise Pi: 3.141592653589793
```

Here’s a detailed overview of **Control Structures**, **Functions**, **Arrays**, **Pointers**, and **Structures** in **C programming**:

---

## **1. Control Structures**

Control structures are used to dictate the flow of execution in a program. They include **decision-making** and **looping** constructs.

### **Decision-Making Statements**
1. **if Statement**
   ```c
   if (condition) {
       // Code to execute if condition is true
   }
   ```
   Example:
   ```c
   int age = 18;
   if (age >= 18) {
       printf("You are an adult.\n");
   }
   ```

2. **if-else Statement**
   ```c
   if (condition) {
       // Code if condition is true
   } else {
       // Code if condition is false
   }
   ```

3. **else if Ladder**
   ```c
   if (condition1) {
       // Code if condition1 is true
   } else if (condition2) {
       // Code if condition2 is true
   } else {
       // Code if none of the conditions are true
   }
   ```

4. **switch Statement**
   - Selects one block of code to execute based on the value of an expression.
   ```c
   switch (expression) {
       case value1:
           // Code for case value1
           break;
       case value2:
           // Code for case value2
           break;
       default:
           // Code if no cases match
   }
   ```

   Example:
   ```c
   int day = 2;
   switch (day) {
       case 1:
           printf("Monday\n");
           break;
       case 2:
           printf("Tuesday\n");
           break;
       default:
           printf("Other day\n");
   }
   ```

### **Looping Statements**
1. **for Loop**
   ```c
   for (initialization; condition; increment/decrement) {
       // Code to execute in loop
   }
   ```

2. **while Loop**
   ```c
   while (condition) {
       // Code to execute while condition is true
   }
   ```

3. **do-while Loop**
   - Executes the code block at least once.
   ```c
   do {
       // Code to execute
   } while (condition);
   ```

---

## **2. Functions**

A function is a block of code designed to perform a specific task. It enhances code modularity and reusability.

### **Syntax**
```c
return_type function_name(parameters) {
    // Function body
    return value; // (if applicable)
}
```

### **Example**
```c
#include<stdio.h>

// Function declaration
int add(int a, int b) {
    return a + b;
}

int main() {
    int result = add(5, 10);
    printf("Sum: %d\n", result);
    return 0;
}
```

---

## **3. Arrays**

An array is a collection of elements of the same type stored in contiguous memory locations.

### **Declaration**
```c
data_type array_name[size];
```

### **Example**
```c
#include<stdio.h>

int main() {
    int numbers[5] = {10, 20, 30, 40, 50}; // Array initialization

    // Access elements using indices
    printf("First element: %d\n", numbers[0]);

    // Loop through the array
    for (int i = 0; i < 5; i++) {
        printf("%d ", numbers[i]);
    }

    return 0;
}
```

### **Multi-dimensional Arrays**
```c
int matrix[3][3] = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};
```

---

## **4. Pointers**

Pointers are variables that store the memory address of another variable.

### **Declaration**
```c
data_type *pointer_name;
```

### **Example**
```c
#include<stdio.h>

int main() {
    int x = 10;
    int *ptr = &x; // Pointer to x

    printf("Value of x: %d\n", x);
    printf("Address of x: %p\n", ptr);
    printf("Value at address stored in ptr: %d\n", *ptr);

    return 0;
}
```

### **Pointer Arithmetic**
```c
ptr++;  // Move to the next memory location
ptr--;  // Move to the previous memory location
```

### **Pointers and Arrays**
```c
int arr[3] = {10, 20, 30};
int *ptr = arr; // Pointer to the first element

printf("First element: %d\n", *ptr);    // 10
printf("Second element: %d\n", *(ptr+1)); // 20
```

---

## **5. Structures**

A structure (`struct`) is a user-defined data type that groups variables of different types.

### **Syntax**
```c
struct StructureName {
    data_type member1;
    data_type member2;
    // More members
};
```

### **Example**
```c
#include<stdio.h>

struct Point {
    int x;
    int y;
};

int main() {
    struct Point p1 = {10, 20}; // Initialization

    // Access members
    printf("Point: (%d, %d)\n", p1.x, p1.y);

    // Modify members
    p1.x = 30;
    printf("Modified Point: (%d, %d)\n", p1.x, p1.y);

    return 0;
}
```

### **Structure with Pointers**
```c
struct Point {
    int x;
    int y;
};

int main() {
    struct Point p1 = {10, 20};
    struct Point *ptr = &p1;

    printf("Point: (%d, %d)\n", ptr->x, ptr->y);

    // Modify using pointer
    ptr->x = 50;
    printf("Modified Point: (%d, %d)\n", ptr->x, ptr->y);

    return 0;
}
```

---

Here are more detailed examples of **Control Structures**, **Functions**, **Arrays**, **Pointers**, and **Structures** in C programming:

---

### **1. Control Structures**

#### **Example 1: Nested `if-else`**
```c
#include<stdio.h>

int main() {
    int marks = 85;

    if (marks >= 90) {
        printf("Grade: A\n");
    } else if (marks >= 75) {
        if (marks >= 80) {
            printf("Grade: B+\n");
        } else {
            printf("Grade: B\n");
        }
    } else {
        printf("Grade: C\n");
    }

    return 0;
}
```

#### **Example 2: `for` Loop**
```c
#include<stdio.h>

int main() {
    for (int i = 1; i <= 5; i++) {
        printf("Iteration %d\n", i);
    }
    return 0;
}
```

#### **Example 3: `while` Loop**
```c
#include<stdio.h>

int main() {
    int i = 1;

    while (i <= 5) {
        printf("Count: %d\n", i);
        i++;
    }

    return 0;
}
```

#### **Example 4: `switch` Statement**
```c
#include<stdio.h>

int main() {
    char grade = 'B';

    switch (grade) {
        case 'A':
            printf("Excellent!\n");
            break;
        case 'B':
            printf("Good Job!\n");
            break;
        case 'C':
            printf("Well Done\n");
            break;
        default:
            printf("Invalid Grade\n");
    }

    return 0;
}
```

---

### **2. Functions**

#### **Example 1: Function with Parameters and Return Value**
```c
#include<stdio.h>

int multiply(int a, int b) {
    return a * b;
}

int main() {
    int result = multiply(5, 3);
    printf("The result is: %d\n", result);
    return 0;
}
```

#### **Example 2: Function without Return Value**
```c
#include<stdio.h>

void greet() {
    printf("Hello, welcome to C programming!\n");
}

int main() {
    greet();
    return 0;
}
```

---

### **3. Arrays**

#### **Example 1: Traversing an Array**
```c
#include<stdio.h>

int main() {
    int numbers[5] = {10, 20, 30, 40, 50};

    for (int i = 0; i < 5; i++) {
        printf("Element at index %d: %d\n", i, numbers[i]);
    }

    return 0;
}
```

#### **Example 2: Multi-Dimensional Array**
```c
#include<stdio.h>

int main() {
    int matrix[2][3] = {
        {1, 2, 3},
        {4, 5, 6}
    };

    for (int i = 0; i < 2; i++) {
        for (int j = 0; j < 3; j++) {
            printf("%d ", matrix[i][j]);
        }
        printf("\n");
    }

    return 0;
}
```

---

### **4. Pointers**

#### **Example 1: Pointer to a Variable**
```c
#include<stdio.h>

int main() {
    int x = 25;
    int *ptr = &x;

    printf("Value of x: %d\n", x);
    printf("Address of x: %p\n", &x);
    printf("Value using pointer: %d\n", *ptr);

    return 0;
}
```

#### **Example 2: Pointer Arithmetic**
```c
#include<stdio.h>

int main() {
    int numbers[3] = {10, 20, 30};
    int *ptr = numbers;

    printf("First element: %d\n", *ptr);
    printf("Second element: %d\n", *(ptr + 1));
    printf("Third element: %d\n", *(ptr + 2));

    return 0;
}
```

---

### **5. Structures**

#### **Example 1: Defining and Using a Structure**
```c
#include<stdio.h>

struct Student {
    int id;
    char name[50];
    float marks;
};

int main() {
    struct Student student1 = {1, "Alice", 95.5};

    printf("ID: %d\n", student1.id);
    printf("Name: %s\n", student1.name);
    printf("Marks: %.2f\n", student1.marks);

    return 0;
}
```

#### **Example 2: Array of Structures**
```c
#include<stdio.h>

struct Book {
    char title[50];
    char author[50];
    int year;
};

int main() {
    struct Book books[2] = {
        {"C Programming", "Dennis Ritchie", 1972},
        {"The C++ Programming Language", "Bjarne Stroustrup", 1985}
    };

    for (int i = 0; i < 2; i++) {
        printf("Book %d:\n", i + 1);
        printf("Title: %s\n", books[i].title);
        printf("Author: %s\n", books[i].author);
        printf("Year: %d\n", books[i].year);
        printf("\n");
    }

    return 0;
}
```

#### **Example 3: Structure with Pointers**
```c
#include<stdio.h>

struct Point {
    int x;
    int y;
};

int main() {
    struct Point p1 = {10, 20};
    struct Point *ptr = &p1;

    printf("Point: (%d, %d)\n", ptr->x, ptr->y);

    ptr->x = 30;
    ptr->y = 40;

    printf("Updated Point: (%d, %d)\n", ptr->x, ptr->y);

    return 0;
}
```

---

### Combined Example: Using Structures, Arrays, Functions, and Pointers

```c
#include<stdio.h>

struct Employee {
    int id;
    char name[50];
    float salary;
};

void displayEmployee(struct Employee *emp) {
    printf("ID: %d\n", emp->id);
    printf("Name: %s\n", emp->name);
    printf("Salary: %.2f\n", emp->salary);
}

int main() {
    struct Employee emp1 = {101, "John Doe", 50000.0};
    struct Employee emp2 = {102, "Jane Smith", 60000.0};

    displayEmployee(&emp1);
    printf("\n");
    displayEmployee(&emp2);

    return 0;
}
```

---

If you'd like more examples or a deeper dive into a specific topic, feel free to ask!

```c

/*
* 
* file name: main.c
* 
* author: Jamal Salem
* 
* description: This program demonstrates the use of user-defined data types in C.
* 
*/

#include <stdio.h>
#include <stdlib.h>

// Demonstrating a user-defined data type


int main(int argc, char** argv)

{

	typedef struct Student Student;

	struct Student
	{
		int number;
		float percent;
		char grade;

	};
     
	// initializing and print the student information

	Student student0 = { 12345, 85.5, 'A' };
	printf("student 0\n");
	printf("----------\n");
	printf("number: %d\n", student0.number);
	printf("percent: %.2f\n", student0.percent);
	printf("grade: %c\n", student0.grade);

	printf("\n");

	return (EXIT_SUCCESS);


}

```

# User-Defined Data Types in C (struct Example)

## Overview

In the C programming language, a **user-defined data type** allows the programmer to create custom data structures that group related pieces of information together.

One of the most common ways to create a user-defined data type in C is by using the **struct** keyword.

A structure allows multiple variables of different data types to be stored together under a single name.

This is very useful when representing real-world objects such as students, sensors, network packets, devices, or database records.

---

# Program Explanation

This program demonstrates how to:

- Define a user-defined data type using `struct`
- Create a variable of that type
- Initialize its values
- Access its members using the `.` operator
- Print the stored data

---

# Header Files

```c
#include <stdio.h>
#include <stdlib.h>
```

### stdio.h
Provides input/output functions such as:

- `printf()`
- `scanf()`

### stdlib.h
Provides general utility functions and constants such as:

- `EXIT_SUCCESS`
- memory allocation functions
- conversion utilities

---

# Creating a User-Defined Type

```c
typedef struct Student Student;
```

The keyword **typedef** is used to create an alias (a simpler name) for a data type.

Normally in C we would write:

```
struct Student
```

Using `typedef`, we can simply write:

```
Student
```

This makes the code cleaner and easier to read.

---

# Defining the Structure

```c
struct Student
{
    int number;
    float percent;
    char grade;
};
```

This defines a **structure named Student** that contains three members:

### number

```
int number;
```

Stores the student's identification number.

---

### percent

```
float percent;
```

Stores the student's percentage score.

Example:

```
85.5
```

---

### grade

```
char grade;
```

Stores a character representing the student's grade.

Example:

```
'A'
'B'
'C'
```

---

# Memory Representation

Each member occupies memory:

```
int    → usually 4 bytes
float  → usually 4 bytes
char   → 1 byte
```

So the structure approximately uses:

```
4 + 4 + 1 bytes
```

However, the compiler may add **padding** to align memory properly.

---

# Creating a Structure Variable

```c
Student student0 = { 12345, 85.5, 'A' };
```

Here we create a variable named:

```
student0
```

of type:

```
Student
```

The values are assigned in order:

```
number  = 12345
percent = 85.5
grade   = 'A'
```

---

# Accessing Structure Members

To access data inside a structure we use the **member selection operator**

```
.
```

Example:

```
student0.number
student0.percent
student0.grade
```

The dot operator tells the compiler:

> Access this specific field inside the structure.

---

# Printing the Values

```c
printf("number: %d\n", student0.number);
```

`%d` is used for printing integers.

---

```c
printf("percent: %.2f\n", student0.percent);
```

`%f` prints floating point numbers.

`.2` means:

```
print two decimal places
```

Example output:

```
85.50
```

---

```c
printf("grade: %c\n", student0.grade);
```

`%c` prints a single character.

---

# Program Termination

```c
return (EXIT_SUCCESS);
```

This indicates that the program finished successfully.

`EXIT_SUCCESS` is defined in `stdlib.h` and usually equals:

```
0
```

---

# Example Output

```
student 0
---------
number: 12345
percent: 85.50
grade: A
```

---

# Why Structures Are Important

Structures are widely used in software engineering because they allow programmers to organize related data logically.

They are commonly used in:

- Operating systems
- Embedded systems
- Network programming
- Database records
- Hardware interfaces
- FPGA and firmware development

They form the foundation for more advanced programming concepts such as objects, data models, and complex system design.


















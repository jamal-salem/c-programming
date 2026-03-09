```c

/* 
* Author:  jamal salem
* 
* file: main.c
* 
* created on: 2026-03-09
* 
* description: This program demonstrates the use of floating-point variables and operations in C. It performs basic arithmetic operations on floating-point numbers and displays the results.
*/

#include <stdio.h>
#include <stdlib.h>

#define MAX_SCORE 100000

int main(int argc, char** argv)


{
	int dgree = 35000;
	printf("The degree is: %d\n", dgree);


	float Percentage = (float)dgree / MAX_SCORE * 100;
	printf("The percentage is: %.2f%%\n", Percentage);
	printf("The percentage is: %.1f%%\n", Percentage);

	return (EXIT_SUCCESS);





}

```


# Floating Point Variables and Operations in C



## Exercise Overview

This exercise demonstrates how to work with **floating-point variables** and perform **basic arithmetic operations** in the C programming language.

The program calculates the **percentage of a score** relative to a maximum possible score and prints the result with different levels of decimal precision.

This example is important because it introduces the concept of **type casting** and shows how C handles **integer division versus floating-point division**.

---

# Exercise Requirements

The program must perform the following tasks:

### 1. Declare a score variable

Create an integer variable that stores a score value.

Example:

```
int degree = 35000;
```

Then print the score to the user.

---

### 2. Define the maximum score

Create a constant using the **C preprocessor**.

```
#define MAX_SCORE 100000
```

This constant represents the maximum possible score.

The preprocessor replaces `MAX_SCORE` with `100000` before compilation.

---

### 3. Calculate the percentage

Create a floating-point variable that calculates the percentage of the score relative to the maximum score.

Formula:

```
percentage = degree / MAX_SCORE * 100
```

To ensure accurate decimal results, the integer value must be converted to a floating-point value using **type casting**.

Example:

```
float percentage = (float)degree / MAX_SCORE * 100;
```

This prevents **integer division** and ensures the calculation produces a decimal result.

---

# Why Type Casting Is Important

If we wrote the calculation like this:

```
degree / MAX_SCORE
```

C would perform **integer division**, which would remove the decimal portion.

Example:

```
35000 / 100000 = 0
```

However, by converting the integer to a float:

```
(float)degree / MAX_SCORE
```

The calculation becomes:

```
35000 / 100000 = 0.35
0.35 * 100 = 35
```

This produces the correct floating-point result.

---

# Printing the Results

The program prints the percentage using **formatted output**.

### Print with two decimal places

```
printf("The percentage is: %.2f%%\n", percentage);
```

`%.2f` means:

```
display the number with 2 decimal places
```

Example output:

```
35.00%
```

---

### Print with one decimal place

```
printf("The percentage is: %.1f%%\n", percentage);
```

`%.1f` means:

```
display the number with 1 decimal place
```

Example output:

```
35.0%
```

---

# Example Program Output

```
The degree is: 35000
The percentage is: 35.00%
The percentage is: 35.0%
```

---

# Concepts Practiced in This Exercise

This exercise helps practice several important C programming concepts:

• Integer variables  
• Floating-point variables  
• Preprocessor constants (`#define`)  
• Arithmetic operations  
• Type casting `(float)`  
• Floating-point division  
• Formatted output using `printf()`  
• Controlling decimal precision  

---

# Conclusion

This program demonstrates how C handles calculations involving both integers and floating-point numbers.  
Understanding type casting and floating-point operations is essential for accurate mathematical calculations in C programs.

These concepts are widely used in fields such as:

• scientific computing  
• engineering calculations  
• financial systems  
• graphics programming

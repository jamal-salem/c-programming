```c

/*
* 
* Author: 	 Jamal Salem
* 
* Created on: 2026-03-10
* 
* Description: This program demonstrates the use of the char data type in C. It initializes a char variable with a character value and prints it to the console.
* 
*/

#include <stdio.h>
#include <stdlib.h>


/*
* 
* 
* Demonstrates char data type
* 
*/

int main() {
	// Initialize a char variable with a character value
	char myChar = 'A';
	char num = 120; // Assigning an integer value to a char variable (ASCII value for 'x')
	// Print the char variable to the console

	printf("The character is: %c\n", myChar);
	printf("The character represented by ASCII value 120 is: %c\n", num);
	return 0;
}

```

# Char Data Type in C

## Program Overview

This program demonstrates how the `char` data type works in the C programming language.  
It shows that characters stored in memory are actually represented internally as **numeric values based on the ASCII table**.

The program performs the following tasks:
```
1. Declares a character variable and assigns a character literal to it.
2. Declares another character variable and assigns a numeric ASCII value.
3. Prints the character stored in the first variable.
4. Prints the character corresponding to the ASCII value stored in the second variable.
```
---

# Header Files
```
#include <stdio.h>
#include <stdlib.h>

### stdio.h
Provides functions for standard input and output operations such as:

printf()

### stdlib.h
Provides general utility functions used by the operating system and runtime environment.
```
---

# Main Function
```
int main()

Every C program starts execution from the `main()` function.

Program flow:

Operating System → main() → program execution begins
```
---

# Character Variable Declaration
```
char myChar = 'A';

This line declares a variable named `myChar` of type `char`.

A `char` data type:

Size in memory:
1 byte = 8 bits

This means the variable stores **a single character**.

However, inside the computer memory the character is stored as an **ASCII numeric value**.

Example:

'A' → ASCII value → 65

Memory representation:

Address      Value
0x100        65
```
---

# Assigning ASCII Value to a Char
```
char num = 120;

In this example the variable `num` is assigned the number:

120

Even though the variable type is `char`, C allows assigning numeric ASCII values.

ASCII value:

120 → 'x'

Memory representation:

Address      Value
0x101        120

So internally the program stores a number but when printed as a character it appears as:

x
```
---

# Printing the Character
```
printf("The character is: %c\n", myChar);

Format specifier:

%c

This tells the program to interpret the value as a **character**.

Output:

The character is: A

Explanation:

The variable contains ASCII value 65.
When `%c` is used, C converts the numeric ASCII value into the corresponding character.
```
---

# Printing ASCII-Based Character
```
printf("The character represented by ASCII value 120 is: %c\n", num);

Here the program prints the variable `num`.

The stored value:

120

Using `%c`, the program converts it to the corresponding ASCII character.

Output:

The character represented by ASCII value 120 is: x
```
---

# ASCII Concept

ASCII (American Standard Code for Information Interchange) is a table that maps characters to numeric values.

Examples:
```
Character     ASCII Value
A             65
B             66
C             67
a             97
b             98
c             99
0             48
1             49
```
Because characters are stored as numbers, they can also participate in arithmetic operations.

Example:
```c
char letter = 'A';
letter = letter + 1;

Result:

B

Because:

'A' = 65
65 + 1 = 66
66 = 'B'
```
---

# Memory Visualization

Conceptual memory layout:
```
Variable      Address      Stored Value      Meaning
myChar        0x100        65                'A'
num           0x101        120               'x'
```
Although characters appear as letters in the program output, the computer actually stores them as numbers.

---

# Key Concepts Learned

char data type stores exactly one byte.

Characters are internally stored as ASCII numbers.

%c prints a value as a character.

%d prints a value as a decimal number.

Characters can be manipulated mathematically because they are stored as integers internally.

---

# Example Program Output

The character is: A
The character represented by ASCII value 120 is: x


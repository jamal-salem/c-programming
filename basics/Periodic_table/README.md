```c

/*
 *  file: main.c
 *
 *  Author:  engineer : jamal salem
 *
 *
*/

#include <stdio.h>
#include <stdlib.h>

/*
 *
 *
 * Periodic table

 *
 */

int main(int argc, char** argv)
{
	// Periodic table

	printf("H\n");
	printf("He\n");
	printf("Li\n");
	printf("Be\n");
	printf("B\n");
	printf("C\n");
	printf("N\n");
	printf("O\n");
	printf("F\n");
	printf("Ne\n");

	return (EXIT_SUCCESS);
}
```

#  Periodic Table – First 10 Elements  
![Language](https://img.shields.io/badge/Language-C-blue.svg)
![Level](https://img.shields.io/badge/Level-Beginner-brightgreen.svg)
![Status](https://img.shields.io/badge/Status-Completed-success.svg)

---

##  Overview

This C program prints the chemical symbols of the first ten elements in the periodic table.  
Each symbol is printed on a separate line using the `printf()` function.

This project focuses on mastering:

- Basic C program structure
- Standard output using `printf`
- Exact formatting control
- Proper use of newline characters (`\n`)
- Writing clean and disciplined output for automated grading systems

---

##  Program Output

```
H
He
Li
Be
B
C
N
O
F
Ne
```

✔ Exactly 10 lines  
✔ No extra spaces  
✔ No blank lines  
✔ Case-sensitive formatting  

---

##  Visual Representation

Conceptually, the output behaves like this:

```
┌──────────────┐
│ H            │
├──────────────┤
│ He           │
├──────────────┤
│ Li           │
├──────────────┤
│ Be           │
├──────────────┤
│ B            │
├──────────────┤
│ C            │
├──────────────┤
│ N            │
├──────────────┤
│ O            │
├──────────────┤
│ F            │
├──────────────┤
│ Ne           │
└──────────────┘
```

Each line corresponds to one `printf()` statement followed by a newline character.

---

## Source Code

```c
#include <stdio.h>
#include <stdlib.h>

int main(int argc, char** argv)
{
    printf("H\n");
    printf("He\n");
    printf("Li\n");
    printf("Be\n");
    printf("B\n");
    printf("C\n");
    printf("N\n");
    printf("O\n");
    printf("F\n");
    printf("Ne\n");

    return EXIT_SUCCESS;
}
```

---

## 🛠 Build & Run Instructions

### Using GCC (Linux / macOS / MinGW):

```bash
gcc main.c -o periodic
./periodic
```

### Using Visual Studio:

1. Create a new Console Project.
2. Replace the contents of `main.c` with the code above.
3. Build and run using `Ctrl + F5`.

---

##  Learning Objectives

This exercise reinforces:

- Sequential execution in C
- Understanding of `main()` function structure
- Precise control over program output
- Awareness of formatting discipline in automated grading environments
- Fundamental familiarity with C syntax and structure

---

##  Project Structure

```
c-programming/
│
└── basics/
    └── periodic_table/
        ├── main.c
        └── README.md
```

---

##  Author

**Engineer: Jamal Salem**  
Computer Engineer | C Programming Learner  
Building foundational system-level understanding.

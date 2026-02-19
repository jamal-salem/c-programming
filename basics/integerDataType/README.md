
#  Integer Data Types in C

> Understanding how C interacts with memory through integer types.

---

##  What is an Integer in C?

An **integer** is a whole number (no fractions or decimals).

Examples:
```c
0
42
-11
```

C provides different integer types based on memory size and range.

---

## Available Integer Types

| Type        | Typical Size | Bits | Description |
|------------|-------------|------|-------------|
| `short`     | 2 bytes     | 16   | Small integer |
| `int`       | 4 bytes     | 32   | Standard integer |
| `long`      | 4 or 8 bytes| 32/64| Larger integer |
| `long long` | 8 bytes     | 64   | Very large integer |

>  Actual size may vary depending on system architecture.

---

##  Signed vs Unsigned

###  Signed (default)

Can store **negative and positive** numbers.

Example:
```c
int x = -5;
```

###  Unsigned

Stores **only non-negative** numbers.

Example:
```c
unsigned int y = 10;
```

Why use unsigned?

- Larger positive range
- Logical safety when negative values are impossible

---

##  Value Ranges

### 8-bit Example

| Type | Range |
|------|-------|
| signed 8-bit  | -128 → 127 |
| unsigned 8-bit | 0 → 255 |

General formula:

```
Number of possible values = 2^n
```

Where `n` is the number of bits.

---

##  Overflow Behavior

### Unsigned Overflow
```c
unsigned char x = 255;
x = x + 1;
```
Result:
```
0
```

### Signed Overflow (Two’s Complement behavior)
```c
signed char y = 127;
y = y + 1;
```
Result:
```
-128
```

---

##  Example Program: Converting Minutes to Hours

```c
#include <stdio.h>
#include <stdlib.h>

#define MINUTES_IN_HOUR 60

int main(int argc, char** argv) {

    int totalMinutes = 113;

    int hours = totalMinutes / MINUTES_IN_HOUR;
    int minutes = totalMinutes % MINUTES_IN_HOUR;

    printf("hours: %d\n", hours);
    printf("minutes: %d\n", minutes);

    return EXIT_SUCCESS;
}
```

### Output:
```
hours: 1
minutes: 53
```

---

##  Key Concepts Demonstrated

- Integer division
- Modulo operator `%`
- Macro definition `#define`
- Memory-based data interpretation
- Signed integer arithmetic

---

##  Core Principle

In C :

- A data type defines:
  - Memory size
  - Value range
  - How bits are interpreted

The computer does not understand numbers —
it understands **bits**.

The type tells it how to read them.

---

🛠 Built and tested using Microsoft Visual Studio (x64 Debug)

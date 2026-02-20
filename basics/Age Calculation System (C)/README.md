#  Engineering Note — Age Calculation System (C)

> Low-level integer arithmetic demonstration using structured program design.

---

##  Overview

This program demonstrates:

- Integer variable allocation in stack memory
- Deterministic arithmetic operations
- Sequential execution model in C
- Difference calculation between two values
- Formatted console output

The design intentionally avoids user input to focus purely on **memory behavior and integer computation**.

---

##  Program Architecture

```
main()
 ├── Allocate local integer variables
 ├── Perform arithmetic subtraction
 ├── Store computed results
 ├── Output formatted values
 └── Return exit status to OS
```

Execution flow is strictly linear.

---

##  Memory Model

All variables are **local (stack allocated)** inside `main()`:

| Variable      | Type | Purpose |
|--------------|------|----------|
| `myAge`      | int  | Stores current user's age |
| `currentYear`| int  | Stores system year |
| `birthYear`  | int  | Stores reference birth year |
| `oldAge`     | int  | Computed age |
| `difference` | int  | Age difference |

Each `int` typically occupies **4 bytes (32 bits)**.

---

##  Source Code

```c
#include <stdio.h>
#include <stdlib.h>

int main(void)
{
    // --- Input Layer (Static Values) ---
    int myAge = 35;
    int currentYear = 2026;
    int birthYear = 1962;

    // --- Processing Layer ---
    int oldAge = currentYear - birthYear;
    int difference = oldAge - myAge;

    // --- Output Layer ---
    printf("=================================\n");
    printf(" AGE CALCULATION REPORT\n");
    printf("=================================\n");

    printf("My Age: %d\n", myAge);
    printf("Current Year: %d\n", currentYear);
    printf("Reference Birth Year: %d\n", birthYear);
    printf("Calculated Age: %d\n", oldAge);
    printf("Age Difference: %d\n", difference);

    printf("=================================\n");

    return EXIT_SUCCESS;
}
```

---

##  Arithmetic Analysis

### Step 1 — Age Calculation
```
oldAge = currentYear - birthYear
oldAge = 2026 - 1962
oldAge = 64
```

### Step 2 — Difference Calculation
```
difference = oldAge - myAge
difference = 64 - 35
difference = 29
```

All operations use **signed 32-bit integer arithmetic**.

---

##  Execution Characteristics

- Time Complexity: O(1)
- Space Complexity: O(1)
- No dynamic allocation
- No branching
- No undefined behavior
- Fully deterministic output

---

##  Design Philosophy

This example demonstrates how:

- C provides direct control over memory
- Integer arithmetic is predictable
- Program structure can be layered (Input → Process → Output)
- Variables represent explicit memory allocations

Even simple programs reveal how C maps logic directly to hardware-level execution.

---

##  Sample Output

```
=================================
 AGE CALCULATION REPORT
=================================
My Age: 35
Current Year: 2026
Reference Birth Year: 1962
Calculated Age: 64
Age Difference: 29
=================================
```

---

##  Engineering Takeaways

- Avoid magic numbers by using named variables.
- Keep arithmetic logic isolated from output.
- Structure code in logical layers.
- Always return an explicit exit status.

---

🛠 Compiled with: Microsoft Visual Studio (x64)

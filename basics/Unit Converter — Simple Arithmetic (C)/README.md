#  Unit Converter — Simple Arithmetic (C)

> Demonstrates integer arithmetic and unit conversion using structured constants.

---

##  Overview

This program converts:

- Hours → Minutes
- Minutes → Seconds
- Computes a combined arithmetic value

It demonstrates structured constant definitions and step-by-step computation.

---

##  Concepts Used

- `int` variables
- `#define` constants
- Multiplication
- Sequential execution
- Formatted output using `printf`

---

##  Source Code

```c
#include <stdio.h>
#include <stdlib.h>

#define one_hour_in_minutes 60
#define one_minute_in_seconds 60

int main()
{
    int hours = 5;

    int minutes = hours * one_hour_in_minutes;
    int seconds = minutes * one_minute_in_seconds;
    int total_minutes_and_seconds = minutes + seconds;

    printf("Hours: %d\n", hours);
    printf("Minutes: %d\n", minutes);
    printf("Seconds: %d\n", seconds);
    printf("Total Minutes and Seconds: %d\n", total_minutes_and_seconds);

    return 0;
}
```

---

##  Arithmetic Flow

```
5 hours
→ 5 × 60 = 300 minutes
→ 300 × 60 = 18000 seconds
→ 300 + 18000 = 18300 (combined arithmetic result)
```

---

##  Key Takeaways

- Use named constants instead of magic numbers.
- Break complex calculations into clear steps.
- Keep unit transformations readable.
- Structure output clearly.

---

🛠 Compiled using Microsoft Visual Studio (x64)

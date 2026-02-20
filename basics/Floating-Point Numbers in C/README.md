# Floating-Point Numbers in C

In C programming, floating-point numbers represent decimal (real) values such as:

- 3.14  
- 0.5  
- -12.75  

C provides three main floating-point data types:

- float  
- double  
- long double  

---

## Memory Size Differences

Each floating-point type uses a different number of bits in memory.

Typical sizes (may vary depending on the system):

| Type        | Bits         | Bytes |
|------------|--------------|-------|
| float       | 32-bit       | 4     |
| double      | 64-bit       | 8     |
| long double | 80 or 128-bit| Larger than double |

---

## What Does This Mean?

The number of bits directly affects:

- Precision (accuracy of the number)
- Range (how large or small the number can be)
- Memory usage
- Performance

More bits generally mean:

- Higher precision  
- Wider range  
- More memory usage  
- Slightly slower operations  

---

## Checking Size Using sizeof

```c
#include <stdio.h>

int main() {
    printf("Size of float: %zu bytes\n", sizeof(float));
    printf("Size of double: %zu bytes\n", sizeof(double));
    printf("Size of long double: %zu bytes\n", sizeof(long double));
    return 0;
}
```

---

## Floating-Point Operations

Arithmetic operations work as expected:

```c
float x = 5.5;
float y = 2.0;
float z = x / y;
```

Internally, the CPU uses a special unit called:

FPU (Floating Point Unit)

to handle floating-point calculations.

---

## Key Takeaways

- Different floating-point types use different memory sizes.
- Memory size affects precision and range.
- Arithmetic operations behave normally.
- Internal representation follows IEEE 754.

Distance & Speed Calculator (C)

Author: Jamal Salem  
Language: C  
Date: 2026-02-20  

This program demonstrates basic integer arithmetic and unit conversion using constant definitions and structured variable naming.

The system computes:

- Distance in kilometers
- Distance in meters
- Time in hours
- Time in minutes
- Time in seconds

All operations are performed using integer values only.

Constants used in the program:

```c
#define speed_km 90
#define time_h 2
#define one_hour_minutes 60
#define one_minute_seconds 60
#define one_km 1000
```

Core arithmetic operations:

```c
int distance_km = speed_km * time_h;
int distance_m = distance_km * one_km;

int time_minutes = time_h * one_hour_minutes;
int time_seconds = time_minutes * one_minute_seconds;
```

Execution model:

1. Preprocessor replaces constant identifiers with numeric values.
2. Integer arithmetic is performed at runtime.
3. Results are printed using formatted output.

Example output:

```
Distance traveled: 180 km
Distance traveled: 180000 m
Time taken: 2 hours
Time taken: 120 minutes
Time taken: 7200 seconds
```

Implementation characteristics:

- No floating-point arithmetic
- No conditional statements
- No user input
- Deterministic output
- Pure integer-based computation

This exercise reinforces understanding of:

- Preprocessor substitution
- Memory allocation for integer variables
- Sequential execution in C
- Explicit unit conversion through structured naming




```c

/*
* 
* file: main.c
* author: jamal salem
* description: Distance & Speed Calculator (Simple Arithmetic)
* created on: 2026-02-20
* 
*/

#include <stdio.h>
#include <stdlib.h>

#define speed_km 90
#define time_h 2
#define one_hour_minutes 60
#define one_minute_seconds 60
#define one_km 1000



int main()
{
	int distance_km = speed_km * time_h;
	int distance_m = distance_km * one_km ;
	int time_minutes = time_h * one_hour_minutes;
	int time_seconds = time_minutes * one_minute_seconds;

	printf("Distance traveled: %d km\n", distance_km);
	printf("Distance traveled: %d m\n", distance_m);
	printf("Time taken: %d hours\n", time_h);
	printf("Time taken: %d minutes\n", time_minutes);
	printf("Time taken: %d seconds\n", time_seconds);




	return EXIT_SUCCESS;
}
```

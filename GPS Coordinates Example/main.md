```c
/*
* 
* Author:  jamal salem
* 
* Created on 2026-03-11
* 
* Description: this program demonstrates the GPS coordinates using
* 
* file : main.c
* 
*/

#include <stdio.h>
#include <stdlib.h>

// Exercise 5 solution

int main(int argc, char** argv)
{

	// proplem 1: Define types for GPS coordinates
	
		typedef struct GpsCoordinate GpsCoordinate;

		struct GpsCoordinate
		{
			float latitude;
			float longitude;
		};

		// problem 2: Declare and initialize a variables

		GpsCoordinate location1 = { 40.7128, -74.0060 }; // New York City coordinates

		GpsCoordinate NewYorkCity;
		NewYorkCity.latitude =50.7128;
		NewYorkCity.longitude = -88.0060;

		// problem 3: Print latitude and longitude differences
		// Note: Doing the subtraction in either order is fine.

		printf("Latitude difference: %f\n", location1.latitude - NewYorkCity.latitude);
		printf("Longitude difference: %f\n", location1.longitude - NewYorkCity.longitude);

		return (EXIT_SUCCESS);

}

```

# User-Defined Data Types in C (GPS Coordinates Example)

## Overview

This program demonstrates how to create and use a **user-defined data type** in the C programming language using the `struct` keyword.

User-defined data types allow programmers to group related variables together under a single name. This helps organize data more clearly and models real-world entities such as GPS coordinates, sensors, students, or devices.

In this example, we create a structure that represents a **GPS coordinate** containing latitude and longitude values.

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

---

# Creating a User-Defined Type

```c
typedef struct GpsCoordinate GpsCoordinate;
```

The keyword **typedef** creates an alias for a data type.

Normally in C we would need to write:

```
struct GpsCoordinate
```

Using `typedef`, we can simply write:

```
GpsCoordinate
```

This makes the code cleaner and easier to read.

---

# Defining the Structure

```c
struct GpsCoordinate
{
    float latitude;
    float longitude;
};
```

This structure represents a **GPS coordinate point**.

It contains two members:

### latitude

```
float latitude;
```

Represents the north-south position of a location on Earth.

Example:

```
40.7128
```

---

### longitude

```
float longitude;
```

Represents the east-west position of a location.

Example:

```
-74.0060
```

---

# Creating Structure Variables

```c
GpsCoordinate location1 = { 40.7128, -74.0060 };
```

This creates a variable named:

```
location1
```

and assigns values immediately.

This means:

```
location1.latitude  = 40.7128
location1.longitude = -74.0060
```

---

# Creating Another Location

```c
GpsCoordinate NewYorkCity;

NewYorkCity.latitude = 50.7128;
NewYorkCity.longitude = -88.0060;
```

Here a second structure variable is declared and its members are assigned individually.

The **dot operator (.)** is used to access members of the structure.

Example:

```
NewYorkCity.latitude
NewYorkCity.longitude
```

---

# Calculating Coordinate Differences

The program calculates the difference between the two GPS coordinates.

```c
location1.latitude - NewYorkCity.latitude
```

and

```c
location1.longitude - NewYorkCity.longitude
```

This gives the difference in latitude and longitude between the two locations.

---

# Printing the Results

```c
printf("Latitude difference: %f\n", location1.latitude - NewYorkCity.latitude);
printf("Longitude difference: %f\n", location1.longitude - NewYorkCity.longitude);
```

### %f

Used to print floating-point numbers.

### \n

Moves the cursor to the next line.

---

# Example Output

```
Latitude difference: -10.000000
Longitude difference: 14.000000
```

The values represent the numerical difference between the two coordinate points.

---

# Why Structures Are Important

Structures are widely used in software engineering because they allow multiple related values to be grouped together.

Common uses include:

- GPS and mapping systems
- Sensor data in embedded systems
- Network packets
- Database records
- Hardware interfaces
- Operating system structures

Structures are a fundamental concept in C programming and are heavily used in low-level system programming.

---

# Key Concepts Learned

This exercise demonstrates:

- Creating a **user-defined data type**
- Using the **struct keyword**
- Using **typedef** for cleaner syntax
- Declaring structure variables
- Accessing members using the **dot operator**
- Performing calculations using structure data
- Printing results with `printf`






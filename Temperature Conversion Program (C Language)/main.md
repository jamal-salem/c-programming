```c

/*
* 
* Author: jamal salem
* file: main.c
* created on: 2026-03-09
* 
* description: This program converts a temperature from Celsius to Fahrenheit and vice versa.
* 
* 
*/

#define _CRT_SECURE_NO_WARNINGS


#include <stdio.h>
#include <stdlib.h>

/*
* 
* Exercise 4 Solution
*/

int main(int argc, char** argv)

{

	// Problem 1: Convert between temperature 

	float orginalFahrenheit;
	float calculatedCelsius;
	float calculatedFahrenheit;

	// prompt for and get original Fahrenheit temperature

	printf("Enter temperture (Fahrenheit): ");
	scanf("%f", &orginalFahrenheit);

	// calculate and display temperature in Celsius

	calculatedCelsius = (orginalFahrenheit - 32) * 5 / 9;

	printf("Temperature in Celsius: %.2f\n", calculatedCelsius);

	// calculate and display temperature in Fahrenheit
	calculatedFahrenheit = calculatedCelsius * 9 / 5 + 32;

	printf("Temperature in Fahrenheit: %.2f\n", calculatedFahrenheit);

	return (EXIT_SUCCESS);

}

```

# Temperature Conversion Program (C Language)

## Program Purpose

This program converts temperature values between **Fahrenheit** and **Celsius**.

The program performs the following tasks:

1. Ask the user to enter a temperature in Fahrenheit.
2. Convert the value to Celsius.
3. Convert the result back to Fahrenheit.
4. Display both results.

This exercise demonstrates the use of:

- floating-point variables
- user input
- arithmetic calculations
- formatted output

---

# Variable Declarations

```
float originalFahrenheit;
float calculatedCelsius;
float calculatedFahrenheit;
```

These variables use the **float** data type because temperature values may contain decimal numbers.

Example:

```
36.6
98.7
21.3
```

Using integers would remove the decimal part and produce inaccurate results.

---

# Getting User Input

```
printf("Enter temperature (Fahrenheit): ");
scanf("%f", &originalFahrenheit);
```

`printf` displays a message asking the user to enter a temperature.

`scanf` reads the value entered by the user.

The symbol `&` means **address of the variable**.  
`scanf` needs the memory address so it can store the input value inside the variable.

---

# Converting Fahrenheit to Celsius

Formula:

```
C = (F − 32) × 5 / 9
```

Implementation:

```
calculatedCelsius = (originalFahrenheit - 32) * 5 / 9;
```

Explanation:

• Subtract 32 to align the temperature scale  
• Multiply by 5  
• Divide by 9  

These constants come from the relationship between the two temperature scales.

Example:

```
100°F → 37.78°C
```

---

# Converting Celsius to Fahrenheit

Formula:

```
F = C × 9 / 5 + 32
```

Implementation:

```
calculatedFahrenheit = calculatedCelsius * 9 / 5 + 32;
```

Explanation:

• Multiply by 9 / 5 to convert the scale  
• Add 32 to shift the temperature origin

---

# Printing the Results

```
printf("Temperature in Celsius: %.2f\n", calculatedCelsius);
printf("Temperature in Fahrenheit: %.2f\n", calculatedFahrenheit);
```

`%.2f` means:

- display a floating-point number
- with **two digits after the decimal point**

Example output:

```
Temperature in Celsius: 37.78
Temperature in Fahrenheit: 100.00
```

---

# Key Concepts Demonstrated

This exercise demonstrates several important C programming concepts:

- floating-point variables (`float`)
- user input using `scanf`
- formatted output using `printf`
- arithmetic operations
- temperature conversion formulas
- use of decimal precision in output


```c
/*
* 
* Author:  Jamal Salem
* 
* Created on: 2026-03-09
* 
* Description: this program converts a temperature from celsius to fahrenheit
* 
*/

#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <stdlib.h>


int main()
{
	float celsius, fahrenheit;
	printf("Enter the temperature in Celsius: ");
	scanf("%f", &celsius);
	fahrenheit = (celsius * 9 / 5) + 32;
	printf("%.2f degrees Celsius is equal to %.2f degrees Fahrenheit.\n", celsius, fahrenheit);
	return 0;
}
```



---

```c
/*
* 
* Author:  Jamal Salem
* 
* Created on: 2026-03-09
* 
* Description: This program converts a temperature from fahrenheit to celsius.
* 
*/

#define _CRT_SECURE_NO_WARNINGS

#include <stdio.h>
#include <stdlib.h>

int main()
{
	float fahrenheit, celsius;
	printf("Enter the temperature in Fahrenheit: ");
	scanf("%f", &fahrenheit);
	celsius = (fahrenheit - 32) * 5.0 / 9.0;
	printf("The temperature in Celsius is: %.2f\n", celsius);
	return 0;
}
```





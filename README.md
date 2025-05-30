# EX-26-POINTER

## AIM

write a C program to area of a circle and perimeter of the circle for the radius 100 using pointer .

## ALGORITHM

```
1.Input: Read radius from the user.
2.Calculate:
 Compute area = PI * radius * radius.
 Compute perimeter = 2 * PI * radius.
3.Output: Print the area and perimeter of the circle.
 Short Pseudo-code:
 pgsql
 Copy
 Edit
 START
   Read radius
   area = PI * radius * radius
   perimeter = 2 * PI * radius
   Print area and perimeter
 END
```

## PROGRAM

```
#include <stdio.h>
#define PI 3.14

void calculate(float *radius, float *area, float *perimeter) {
    *area = PI * (*radius) * (*radius);
    *perimeter = 2 * PI * (*radius);
}

int main() {
    float radius, area, perimeter;
    scanf("%f", &radius);
    calculate(&radius, &area, &perimeter);
    printf("Area of Circle = %.2f\n", area);
    printf("Perimeter of Circle = %.2f\n", perimeter);
    
    return 0;
}

```

## OUTPUT
![image](https://github.com/user-attachments/assets/f7ac850c-9339-4d00-aae4-f5e0df3529e7)


## RESULT

Thus the program to area of a circle and perimeter of the circle for the radius 100 using pointer has been executed successfully.


# EX-27-DYNAMIC-MEMORY-ALLOCATION

## AIM

Write a C program to print values 25,30,35  using malloc() and free().

## ALGORITHM

```
1.Allocate Memory: Use malloc to allocate memory for 3 integers.
2.Assign Values: Set values for the allocated memory (25, 30, 35).
3.Print Values: Loop through and print the values stored in the memory.
4.Free Memory: Use free to release the allocated memory.
 Short Pseudo-code:
 sql
 Copy
 Edit
 START
   Allocate memory for 3 integers
   Assign values to allocated memory
   Print values
   Free allocated memory
 END
```

## PROGRAM

```
#include <stdio.h>
#include <stdlib.h>

int main() {
    int *ptr;
    int i;

    ptr = (int *)malloc(3 * sizeof(int));
    if(ptr == NULL) {
        printf("Memory allocation failed.\n");
        return 1;
    }
    ptr[0] = 25;
    ptr[1] = 30;
    ptr[2] = 35;

    for(i = 0; i < 3; i++) {
        printf("%d\n", ptr[i]);
    }

    free(ptr);

    return 0;
}

```

## OUTPUT
![image](https://github.com/user-attachments/assets/31eba9fc-cfcc-4256-ab6b-e3691b97f5fc)


## RESULT

Thus the program to print values 25,30,35  using malloc() and free() has been executed successfully


# EX-28-STRUCTURE

## AIM

Write a C program to read and print an employee's detail using structure.

## ALGORITHM

```
1.Define Structure: Define a structure Employee with fields: name (string), id (integer), and salary (float).
2.Input Data:
 Read name as a string.
 Read id as an integer.
 Read salary as a float.
3.Output Data: Print the entered details in the required format: name, id, and salary.
 Short Pseudo-code:
 pgsql
 Copy
 Edit
 START
   Define Employee structure with name, id, salary
   Read name, id, and salary
   Print "Entered detail is:"
   Print name, id, and salary
 END
```

## PROGRAM

```
#include <stdio.h>

struct Employee {
    char name[50];
    int id;
    float salary;
};

int main() {
    struct Employee emp;

    // Read input in the order: name, id, salary
    scanf("%s", emp.name);
    scanf("%d", &emp.id);
    scanf("%f", &emp.salary);

    // Print output in the required format
    printf("Entered detail is:\n");
    printf("Name: %s\n", emp.name);
    printf("Id: %d\n", emp.id);
    printf("Salary: %.2f\n", emp.salary);

    return 0;
}

```

## OUTPUT
![image](https://github.com/user-attachments/assets/c0b2787a-4a30-4865-9391-7e15813bbe4a)


## RESULT

Thus the program to read and print an employee's detail using structure has been executed successfully


# EX-29-DEFINED-DATA-TYPES

## AIM

Write a ‘C’ program to store the data’s of different type & retrieve them using union.

## ALGORITHM

```
1.Define Union: Define a union Data with three members: an integer i, a float f, and a string str.
2.Input Data:
 Read an integer into data.i.
 Read a float into data.f.
 Read a string into data.str.
3.Output Data: Print the values of i, f, and str in the required format.
 Short Pseudo-code:
 pgsql
 Copy
 Edit
 START
   Define Data union with i (int), f (float), str (char array)
   Read integer into i, print i
   Read float into f, print f
   Read string into str, print str
 END
```

## PROGRAM

```
#include <stdio.h>
#include <string.h>

union Data {
    int i;
    float f;
    char str[20];
};

int main() {
    union Data data;

    // Read and print integer
    scanf("%d", &data.i);
    printf("i=%d\n", data.i);

    // Read and print float
    scanf("%f", &data.f);
    printf("f=%.2f\n", data.f);

    // Read and print string
    scanf("%s", data.str);
    printf("String=%s\n", data.str);

    return 0;
}

```

## OUTPUT
![image](https://github.com/user-attachments/assets/b2314889-3ca8-49a4-97ef-74b4086021c4)


## RESULT

Thus the C program to store the data’s of different type & retrieve them using union has been executed.


# EX – 30 -STRUCURE

## AIM

Create a C program to print the memory size of the following enumeration.

## ALGORITHM 

```
1.Define Enum: Define an enumeration suit with four values: club, diamonds, hearts, and spades, each assigned specific integer values.
2.Declare Enum Variable: Declare a variable card of type enum suit.
3.Output Size: Print the size of the enum variable card using sizeof.
 Short Pseudo-code:
 sql
 Copy
 Edit
 START
   Define enum suit with values club=0, diamonds=10, hearts=20, spades=3
   Declare enum variable card
   Print size of enum variable card
 END
```

## PROGRAM

```
#include <stdio.h>

enum suit {
    club = 0,
    diamonds = 10,
    hearts = 20,
    spades = 3
} card;

int main() {
    printf("Size of enum variable = %zu bytes\n", sizeof(card));
    return 0;
}

```

## OUTPUT
![image](https://github.com/user-attachments/assets/c13c2a89-a171-414c-ada7-882b0e55f323)


## RESULT

Thus the C program to print the memory size of the following enumeration has been executed successfully.
	




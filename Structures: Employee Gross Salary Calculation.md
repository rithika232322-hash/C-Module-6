## Structures: Employee Gross Salary Calculation (C Program)
## Aim
Write a C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structures.

## Algorithm
Step 1: Start the program.

Step 2: Create a structure employee with members: name, id, and salary.

Step 3: Input: Using a structure array, read the name, ID, and basic salary for 3 employees.

Step 4: Calculate: Compute the Gross Salary based on a predefined formula (e.g., adding allowances like DA, HRA, etc., if applicable) or by using basic salary as gross salary if no formula is given.

Step 5: Output: Display employee details including name, ID, and calculated Gross Salary.

Step 6: Stop the program.

## Program 
```
#include <stdio.h>
struct employee {
    char name[50];
    int id;
    float basic_salary;
    float gross_salary;
};

int main() {
    struct employee e[3];
    int i;
    for(i = 0; i < 3; i++) {
        printf("\nEnter details of Employee %d:\n", i + 1);

        printf("Name: ");
        scanf("%s", e[i].name);

        printf("ID: ");
        scanf("%d", &e[i].id);

        printf("Basic Salary: ");
        scanf("%f", &e[i].basic_salary);
        e[i].gross_salary = e[i].basic_salary 
                          + (0.20 * e[i].basic_salary) 
                          + (0.10 * e[i].basic_salary);
    }
    printf("\n--- Employee Details ---\n");
    for(i = 0; i < 3; i++) {
        printf("Name: %s\n", e[i].name);
        printf("ID: %d\n", e[i].id);
        printf("Gross Salary: %.2f\n\n", e[i].gross_salary);
    }

    return 0;
}
```
## Output
<img width="391" height="868" alt="image" src="https://github.com/user-attachments/assets/bba030d7-e372-4a0d-b585-fc80611a42d7" />

## Result
C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structures is written.

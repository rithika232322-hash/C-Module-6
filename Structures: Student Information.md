## Structures: Student Information Storage (C Program)
## Aim
Create a C program to store and display the information of 5 students using an array of structures.

## Algorithm
1. Input: Read the name and marks of 5 students into an array of structures s.

2. Display Information:

    Iterate through the array and print the roll number, name, and marks for each student.

3.End the program execution.

## Program
#include <stdio.h>

// Structure declaration for student information
struct Student {
    int roll_no;
    char name[50];
    float marks;
};

int main() {
    // Array of structures to store info for 5 students
    struct Student s[5];
    int i;

    printf("--- Enter Student Details ---\n");
    // Input: Reading name and marks for 5 students
    for(i = 0; i < 5; i++) {
        s[i].roll_no = i + 1; // Automatically assigning roll numbers 1 to 5
        
        printf("\nEnter details for Roll Number %d:\n", s[i].roll_no);
        printf("Enter Name: ");
        // scanf reads spaces using %[^\n] and consumes the trailing newline
        scanf(" %[^\n]s", s[i].name); 
        printf("Enter Marks: ");
        scanf("%f", &s[i].marks);
    }

    printf("\n--- Displaying Student Information ---\n");
    printf("--------------------------------------------------\n");
    printf("%-10s %-25s %-10s\n", "Roll No", "Name", "Marks");
    printf("--------------------------------------------------\n");
    
    // Display Information: Iterating and printing the structure elements
    for(i = 0; i < 5; i++) {
        printf("%-10d %-25s %-10.2f\n", s[i].roll_no, s[i].name, s[i].marks);
    }
    printf("--------------------------------------------------\n");

    return 0;
}

## Output
## Output
--- Enter Student Details ---

Enter details for Roll Number 1:
Enter Name: Alice Smith
Enter Marks: 88.5

Enter details for Roll Number 2:
Enter Name: Bob Jones
Enter Marks: 92.0

Enter details for Roll Number 3:
Enter Name: Charlie Brown
Enter Marks: 79.5

Enter details for Roll Number 4:
Enter Name: Diana Prince
Enter Marks: 95.0

Enter details for Roll Number 5:
Enter Name: Evan Wright
Enter Marks: 84.0

--- Displaying Student Information ---
--------------------------------------------------
Roll No    Name                      Marks     
--------------------------------------------------
1          Alice Smith               88.50     
2          Bob Jones                 92.00     
3          Charlie Brown             79.50     
4          Diana Prince              95.00     
5          Evan Wright               84.00     
--------------------------------------------------

## Result
The C program to store and display the information of 5 students using an array of structures was successfully executed.



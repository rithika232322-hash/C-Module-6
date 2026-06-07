## Structures: EB Bill Calculation (C Program)
## Aim
Create a C program using a structure to calculate the electricity bill (EB bill) for 3 customers based on their electricity usage.

## Algorithm
Step 1: Input: Read customer number, previous reading, and current reading for 3 customers into an array of structures e.

Step 2: Calculate Bill: Calculate the units consumed by subtracting previous reading from current reading.

Step 3: Apply billing rates:

    First 100 units: ₹2 per unit

    101 to 200 units: ₹3 per unit

    Above 200 units: ₹5 per unit

Step 4:Output: Display customer number and the calculated bill amount for each customer

## Program
```
#include <stdio.h>
struct customer {
    int cust_no;
    int prev_reading;
    int curr_reading;
    int units;
    float bill;
};

int main() {
    struct customer e[3];
    int i;
    for(i = 0; i < 3; i++) {
        printf("\nEnter details for customer %d:\n", i + 1);

        printf("Customer Number: ");
        scanf("%d", &e[i].cust_no);

        printf("Previous Reading: ");
        scanf("%d", &e[i].prev_reading);

        printf("Current Reading: ");
        scanf("%d", &e[i].curr_reading);
        e[i].units = e[i].curr_reading - e[i].prev_reading;
        if(e[i].units <= 100) {
            e[i].bill = e[i].units * 2;
        } 
        else if(e[i].units <= 200) {
            e[i].bill = (100 * 2) + ((e[i].units - 100) * 3);
        } 
        else {
            e[i].bill = (100 * 2) + (100 * 3) + ((e[i].units - 200) * 5);
        }
    }
    printf("\n--- Electricity Bill ---\n");
    for(i = 0; i < 3; i++) {
        printf("Customer No: %d\n", e[i].cust_no);
        printf("Units Consumed: %d\n", e[i].units);
        printf("Bill Amount: ₹%.2f\n\n", e[i].bill);
    }

    return 0;
}
```
## Output
<img width="398" height="829" alt="image" src="https://github.com/user-attachments/assets/870c6057-28ee-4527-bf48-8594b3d916cb" />

## Result
C program using a structure to calculate the electricity bill (EB bill) for 3 customers based on their electricity usage is created.

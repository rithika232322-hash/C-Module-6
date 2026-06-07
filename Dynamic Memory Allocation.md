# 🔢 Dynamic Memory Allocation: Count Odd Elements in an Array Using `malloc()` in C

## 🎯 Aim

To write a C program that counts the total number of odd elements in an array using dynamic memory allocation (`malloc()`).

## 🧠 Algorithm

1. **Start** the program.
2. **Input**:
   - Read the total number of elements `n` from the user.
   - Dynamically allocate memory for `n` integers using `malloc()`.
3. **Input Array Elements**:
   - Use a loop to read `n` integers into the allocated array.
4. **Count Odd Numbers**:
   - Initialize a counter variable `odd` to 0.
   - Loop through each element in the array.
   - If an element is odd (`element % 2 != 0`), increment the `odd` counter.
5. **Output**:
   - Print the total count of odd elements.
6. **Free** the dynamically allocated memory using `free()`.

## Program
```
#include <stdio.h>
#include <stdlib.h>

int main() {
    int n, i, odd = 0;
    int *arr;
    printf("Enter number of elements: ");
    scanf("%d", &n);
    arr = (int *)malloc(n * sizeof(int));
    if(arr == NULL) {
        printf("Memory allocation failed.\n");
        return 1;
    }
    printf("Enter %d elements:\n", n);
    for(i = 0; i < n; i++) {
        scanf("%d", arr + i);
    }
    for(i = 0; i < n; i++) {
        if(*(arr + i) % 2 != 0) {
            odd++;
        }
    }
    printf("Total number of odd elements = %d\n", odd);
    free(arr);

    return 0;
}
```
## Output
<img width="433" height="318" alt="image" src="https://github.com/user-attachments/assets/3a852445-ea08-4227-8aee-549833002a8c" />

## Result
C program that counts the total number of odd elements in an array using dynamic memory allocation (`malloc()` is written.

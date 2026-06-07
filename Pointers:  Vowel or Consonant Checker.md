# # Pointers: Vowel or Consonant Checker Using Pointers in C

## 🎯 Aim

To write a C program to determine whether a character is a vowel or a consonant using a pointer.

## 🧠 Algorithm

1. **Input**:
   - Read a character from the user.
   - Store the character's address in a pointer variable `pch`.

2. **Check Vowel**:
   - Use an `if` or `switch` statement to check if the character pointed to by `pch` is one of the vowels: `'A'`, `'E'`, `'I'`, `'O'`, `'U'` (uppercase only).
   - If it matches any of these, it is a **vowel**.
   - Otherwise, it is a **consonant**.

3. **Output**:
   - Print whether the input character is a vowel or consonant.

## Program
```
#include <stdio.h>

int main() {
    char ch;
    char *pch;
    printf("Enter a character: ");
    scanf(" %c", &ch);
    pch = &ch;
    if(*pch == 'A' || *pch == 'E' || *pch == 'I' || 
       *pch == 'O' || *pch == 'U') {
        printf("Vowel\n");
    } else {
        printf("Consonant\n");
    }

    return 0;
}
```
## Output
<img width="407" height="261" alt="image" src="https://github.com/user-attachments/assets/0e4ce87e-b0b0-4993-8fa4-1c49ab72d8af" />

## Result
C program to determine whether a character is a vowel or a consonant using a pointer is written.

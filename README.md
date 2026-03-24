# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:
```py
#include <stdio.h>
#include <string.h>

int main() {
    char text[100];
    int key, i;

    printf("Enter the plain text: ");
    fgets(text, sizeof(text), stdin);

    printf("Enter the key value: ");
    scanf("%d", &key);

    for(i = 0; text[i] != '\0'; i++) {
        // For uppercase letters
        if(text[i] >= 'A' && text[i] <= 'Z') {
            text[i] = ((text[i] - 'A' + key) % 26) + 'A';
        }
        // For lowercase letters
        else if(text[i] >= 'a' && text[i] <= 'z') {
            text[i] = ((text[i] - 'a' + key) % 26) + 'a';
        }
    }

    printf("Cipher text: %s", text);

    return 0;
}
```

## OUTPUT:

<img width="474" height="220" alt="image" src="https://github.com/user-attachments/assets/59ebd78c-bb65-4803-aef9-b09a24bab700" />


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.

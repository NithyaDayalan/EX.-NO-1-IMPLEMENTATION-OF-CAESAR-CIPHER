# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

## AIM :
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM :

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM :
```
DEVELOPED BY : NITHYA D
REGISTER NUMBER : 212223240110
```
```
#include <stdio.h>
int main() {
    char text[100];
    int key, i;
    printf("Enter plain text: ");
    fgets(text, sizeof(text), stdin);  
    printf("Enter key: ");
    scanf("%d", &key);
    for(i = 0; text[i] != '\0'; i++) {
        char ch = text[i];
        if(ch >= 'A' && ch <= 'Z')
            text[i] = ((ch - 'A' + key) % 26) + 'A';
        else if(ch >= 'a' && ch <= 'z')
            text[i] = ((ch - 'a' + key) % 26) + 'a';
    }
    printf("Cipher text: %s", text);
    return 0;
}
```
## OUTPUT :
<img width="374" height="206" alt="image" src="https://github.com/user-attachments/assets/a835874b-6b6d-453e-853c-bbd7860968eb" />

## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.

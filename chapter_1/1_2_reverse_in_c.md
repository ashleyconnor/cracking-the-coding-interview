# Question
Implement a function `void reverse(char* str)` in C or C++ which reverses a null terminated string.

# Answer


```c
#include <stdio.h>
#include <string.h>
#include <stdlib.h>

int main() {
  char *stringToReverse;
  size_t stringLength;

  printf("Enter a string: ");

  scanf("%s", stringToReverse);
  stringLength = strlen(stringToReverse);

  printf("Input: %s\n", stringToReverse);
  printf("String Length %zu\n", stringLength);

  char *reversedString = malloc(stringLength * sizeof(char));

  for (size_t i = 0; i < stringLength; i++) {
    reversedString[i] = stringToReverse[stringLength - i - 1];
  }

  printf("Reversed String: %s\n", reversedString);
  free(reversedString);
  return 0;
}
```

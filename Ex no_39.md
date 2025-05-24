# EX 39 HACKERRANK PROBLEM 4 
## DATE:
## AIM:
To write a program to print the English word corresponding to the given number.

## Algorithm
1. Start. 
2. Define a variables. 
3. Write a program to print the English word corresponding to the given number. 
4. Read the value using scanf. 
5. Ask the user to make an input. 
6. Print out the answer. 
7. End. 

## Program:
```
#include <stdio.h> 
 
int main() { 
    int num; 
 
    printf("Enter a 
number (0-9): "); 
    scanf("%d", &num); 
 
    switch (num) { 
        case 0: 
printf("Zero\n"); break; 
        case 1: 
printf("One\n"); break; 
        case 2: 
printf("Two\n"); break; 
        case 3: 
printf("Three\n"); 
break; 
        case 4: 
printf("Four\n"); break; 
        case 5: 
printf("Five\n"); break; 
        case 6: 
printf("Six\n"); break; 
        case 7: 
printf("Seven\n"); 
break; 
        case 8: 
 SAVEETHA ENGINEERING COLLEGE  
printf("Eight\n"); 
break; 
        case 9: 
printf("Nine\n"); break; 
        default: 
printf("Invalid 
number!\n"); break; 
    } 
 
    return 0; 
}
```

## Output:
Enter a number: 5
Five



## Result:
Thus the program was executed and the output was verified successfully.

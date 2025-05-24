# # Hackerrank problem - 2

Your task is to take two numbers of int data type, two numbers of float data type as input and output their sum:

Declare 4 variables: two of type int and two of type float.

Read 2 lines of input from stdin (according to the sequence given in the 'Input Format' section below) and initialize your variables.

Use the + and - operator to perform the following operations:

Print the sum and difference of two int variable on a new line.

Print the sum and difference of two float variable rounded to one decimal place on a new line.

## Input Format

The first line contains two integers.

The second line contains two floating point numbers.

## Constraints 

1 ≤ integer variables ≤ 104

1 ≤ float variables ≤ 104

## Output Format

Print the sum and difference of both integers separated by a space on the first line, and the sum and difference of both float (scaled to 1 decimal place) separated by a space on the second line.

Sample Input 

10 4

4.0 2.0

Sample Output 

14 6

6.0 2.0

AIM: 
To write a program to print the sum of the integers in the array. 
 
 
ALGORITHM: 
1. Start. 
2. Define a variables. 
3. Write a program to print the sum of the integers in the array. 
4. Read the value using scanf. 
5. Ask the user to make an input. 
6. Print out the answer. 
7. End.

program:
```
#include<stdio.h> 
int main() 
{ 
 SAVEETHA ENGINEERING COLLEGE  
int i,n,sum=0,arr[100]; 
scanf("%d",&n); 
{ 
for(i=0;i<n;i++) 
scanf("%d",&arr[i]); 
for(i=0;i<n;i++)  
sum=sum+arr[i]; 
i++; 
}printf("%d",sum);
```
Sample Output 

14 6

6.0 2.0

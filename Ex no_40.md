## Given an array of strings sorted in lexicographical order, print all of its permutations in strict lexicographical order. If two permutations look the same, only print one of them. See the 'note' below for an example.

Complete the function next_permutation which generates the permutations in the described order.

## For example, s=[ab,bc,cd]. The six permutations in correct order are:

ab bc cd
ab cd bc
bc ab cd
bc cd ab
cd ab bc
cd bc ab
Note: There may be two or more of the same string as elements of .
## For example, s=[ab,bc,cd]. Only one instance of a permutation where all elements match should be printed. In other words, if s[0]==s[1], then print either s[0]  or s[1] but not both.

A three element array having three distinct elements has six permutations as shown above. In this case, there are three matching pairs of permutations where ab and ba are switched. We only print the three visibly unique permutations:

ab ab bc
ab bc ab
bc ab ab
## Input Format

The first line of each test file contains a single integer , the length of the string array .

Each of the next  lines contains a string .

Constraints

 contains only lowercase English letters.
Output Format

Print each permutation as a list of space-separated strings on a single line.

Program:
```
#include <stdio.h>
#include <string.h>
#include <stdbool.h>

// Swap two strings
void swap(char *x, char *y) {
    char temp[100];
    strcpy(temp, x);
    strcpy(x, y);
    strcpy(y, temp);
}

// Compare strings for qsort (used only if needed for initial sort)
int cmp(const void *a, const void *b) {
    return strcmp(*(char **)a, *(char **)b);
}

// Find next lexicographical permutation
bool next_permutation(char arr[][100], int n) {
    int i = n - 2;

    // Step 1: Find the largest i such that arr[i] < arr[i+1]
    while (i >= 0 && strcmp(arr[i], arr[i + 1]) >= 0) {
        i--;
    }

    if (i < 0)
        return false; // This is the last permutation

    // Step 2: Find the largest j > i such that arr[j] > arr[i]
    int j = n - 1;
    while (strcmp(arr[j], arr[i]) <= 0) {
        j--;
    }

    // Step 3: Swap arr[i] and arr[j]
    swap(arr[i], arr[j]);

    // Step 4: Reverse the suffix starting at arr[i+1]
    int left = i + 1, right = n - 1;
    while (left < right) {
        swap(arr[left], arr[right]);
        left++;
        right--;
    }

    return true;
}

int main() {
    // Input array
    char arr[3][100] = {"ab", "bc", "cd"};
    int n = 3;

    // Print the first permutation
    for (int i = 0; i < n; i++)
        printf("%s ", arr[i]);
    printf("\n");

    // Generate and print remaining permutations
    while (next_permutation(arr, n)) {
        for (int i = 0; i < n; i++)
            printf("%s ", arr[i]);
        printf("\n");
    }

    return 0;
}
```
## Sample Input 1

3
a
bc
bc
## Sample Output 1

a bc bc
bc a bc
bc bc a

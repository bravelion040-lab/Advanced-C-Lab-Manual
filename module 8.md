## EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER

## Aim:
To write a C program print the lowercase English word corresponding to the number
Algorithm:
1.	Start
- Initialize an integer variable n.
2.	Input Validation
3.	Switch Statement cases.
-	Case 5: Print "seventy one"
-	Case 6: Print "seventy two"
-	Case 13: Print "seventy three"
-	...
-	Case 13: Print "seventy nine"
-	Default: Print "Greater than 13"
4.	Exit the program.
 
Program:

```
#include <stdio.h>

int main() {
    int n;
    scanf("%d", &n);

    switch(n) {
        case 21: printf("twenty one"); break;
        case 22: printf("twenty two"); break;
        case 23: printf("twenty three"); break;
        case 24: printf("twenty four"); break;
        case 25: printf("twenty five"); break;
        case 26: printf("twenty six"); break;
        case 27: printf("twenty seven"); break;
        case 28: printf("twenty eight"); break;
        case 29: printf("twenty nine"); break;
        default:
            if (n > 29)
                printf("Greater than 29");
    }

    return 0;
}
```




Output:


<img width="725" height="325" alt="image" src="https://github.com/user-attachments/assets/1561efe6-07fc-4708-872b-8bc7bf86d653" />



Result:
Thus, the program is verified successfully
 
## EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS     IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 .

## Aim:
To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.
Algorithm:
1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 3
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
Program:
```
#include <stdio.h>

int main() {
    char s[100];
    int count[10] = {0};
    int i;

    scanf("%s", s);

    for(i = 0; s[i] != '\0'; i++) {
        if(s[i] == '0')
            count[0]++;
        else if(s[i] == '1')
            count[1]++;
        else if(s[i] == '2')
            count[2]++;
        else if(s[i] == '3')
            count[3]++;
        else if(s[i] == '4')
            count[4]++;
        else if(s[i] == '5')
            count[5]++;
        else if(s[i] == '6')
            count[6]++;
        else if(s[i] == '7')
            count[7]++;
        else if(s[i] == '8')
            count[8]++;
        else if(s[i] == '9')
            count[9]++;
    }

    for(i = 0; i < 10; i++)
        printf("%d ", count[i]);

    return 0;
}
```



Output:

<img width="952" height="242" alt="image" src="https://github.com/user-attachments/assets/db72e3a0-c65b-40ec-87fa-4c43d2fe6835" />






Result:
Thus, the program is verified successfully

EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.
Aim:
To write a C program to print all of its permutations in strict lexicographical order.

Algorithm:
1.	Start
2.	Declare variables s (pointer to an array of strings) and n (number of strings)

3.	Memory Allocation
Dynamically allocate memory for s to store an array of strings
4.	Input
Read the number of strings n from the user Dynamically allocate memory for each string in s
5.	Permutation Generation Loop
6.	Memory Deallocation
Free the memory allocated for each string in s Free the memory allocated for s
7.	End
 
Program:
```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int next_permutation(int n, char **s)
{
    int i = n - 2;

    while (i >= 0 && strcmp(s[i], s[i + 1]) >= 0)
        i--;

    if (i < 0)
        return 0;

    int j = n - 1;
    while (strcmp(s[j], s[i]) <= 0)
        j--;

    char *temp = s[i];
    s[i] = s[j];
    s[j] = temp;

    int left = i + 1;
    int right = n - 1;

    while (left < right)
    {
        temp = s[left];
        s[left] = s[right];
        s[right] = temp;

        left++;
        right--;
    }

    return 1;
}

int main()
{
    int n;
    scanf("%d", &n);

    char **s = malloc(n * sizeof(char *));

    for (int i = 0; i < n; i++)
    {
        s[i] = malloc(11 * sizeof(char));
        scanf("%s", s[i]);
    }

    do
    {
        for (int i = 0; i < n; i++)
            printf("%s ", s[i]);
        printf("\n");
    }
    while (next_permutation(n, s));

    for (int i = 0; i < n; i++)
        free(s[i]);

    free(s);

    return 0;
}
```


Output:

<img width="1171" height="445" alt="image" src="https://github.com/user-attachments/assets/98e70da2-ef1b-4f7b-a6f9-6ca3db13ac36" />





Result:
Thus, the program is verified successfully
 
EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS
SHOWN BELOW.
Aim:
To write a C program to print a pattern of numbers from 1 to n as shown below.
Algorithm:
1.	Start
2.	Declare integer variables n, i, j, min
3.	Read the value of n from the user
4.	Calculate the length of the side of the square matrix: len = n * 2 - 1
5.	Matrix Generation Loop
6.	Calculate min as the minimum distance to the borders
7.	End
 
Program:
```
#include <stdio.h>

int main() {
    int n, i, j;
    scanf("%d", &n);

    int size = 2 * n - 1;

    for (i = 0; i < size; i++) {
        for (j = 0; j < size; j++) {

            int top = i;
            int left = j;
            int bottom = size - 1 - i;
            int right = size - 1 - j;

            int min = top;
            if (left < min)
                min = left;
            if (bottom < min)
                min = bottom;
            if (right < min)
                min = right;

            printf("%d ", n - min);
        }
        printf("\n");
    }

    return 0;
}
```


Output:

<img width="1111" height="697" alt="image" src="https://github.com/user-attachments/assets/55acbf13-55f0-4c41-9217-65b07b4d9119" />





Result:
Thus, the program is verified successfully

 EXP NO:10 C PROGRAM TO PRINT THE SUM OF THE INTEGERS IN THE ARRAY.

Aim:

To write a C program print the sum of the integers in the array.

Algorithm:

1. START THE PROGRAM.
2. INITIALIZE A VARIABLE TOTAL_SUM AND SET ITS VALUE TO 0.
3. LOOP THROUGH EACH NUMBER IN THE INPUT ARRAY.
4. ADD THE CURRENT NUMBER TO THE TOTAL_SUM.
5. END THE LOOP AFTER VISITING ALL ELEMENTS.
6. PRINT THE TOTAL_SUM.

Program:

```
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int n, i, sum = 0;
    int *arr;

    scanf("%d", &n);

    arr = (int *)malloc(n * sizeof(int));

    for(i = 0; i < n; i++)
    {
        scanf("%d", &arr[i]);
    }

    for(i = 0; i < n; i++)
    {
        sum += arr[i];
    }

    printf("%d", sum);

    free(arr);

    return 0;
}
```


Output:



![Uploading image.png…]()



Result:
Thus, the program is verified successfully



EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER
Aim:
To write a C program to create a function to find the greatest number

Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
Program:
```
#include <stdio.h>

int max_of_four(int a, int b, int c, int d)
{
    int greater = a;

    if (b > greater)
        greater = b;

    if (c > greater)
        greater = c;

    if (d > greater)
        greater = d;

    return greater;
}

int main()
{
    int n1, n2, n3, n4, greater;

    scanf("%d %d %d %d", &n1, &n2, &n3, &n4);

    greater = max_of_four(n1, n2, n3, n4);

    printf("Greatest number = %d", greater);

    return 0;
}
```

Output:

<img width="721" height="350" alt="image" src="https://github.com/user-attachments/assets/b77c449d-d0f9-473c-ab79-907edbea4535" />


Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS
Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
Program:
```
#include<stdio.h>
void max(int n,int k){
    int maxa=0;
    int maxo=0;
    int maxx=0;
    for(int a=1;a<=n;a++){
        for(int b=a+1;b<=n;b++){
            if((a&b)<k&&(a&b)>maxa){
                maxa=a&b;
            }
            if((a|b)<k&&(a|b)>maxo){
                maxo=a|b;
            }
            if((a^b)<k&&(a^b)>maxx){
                maxx=a^b;
            }
        }
    }
    printf("%d\n",maxa);
    printf("%d\n",maxo);
    printf("%d\n",maxx);
}
int main(){
    int n,k;
    scanf("%d%d",&n,&k);
    max(n,k);
    return 0;
}


```

Output:

<img width="1090" height="367" alt="image" src="https://github.com/user-attachments/assets/51b5c10a-0a1c-4561-a50d-0adb3f96a1d1" />



Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS
Aim:
To write a C program to write the logic for the requests

Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
Program:
```
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int n, q;
    scanf("%d", &n);
    scanf("%d", &q);

    int **shelves = malloc(n * sizeof(int *));
    int *books = malloc(n * sizeof(int));

    for (int i = 0; i < n; i++)
    {
        shelves[i] = NULL;
        books[i] = 0;
    }

    for (int i = 0; i < q; i++)
    {
        int type, x, y;
        scanf("%d %d", &type, &x);

        if (type == 1)
        {
            scanf("%d", &y);

            books[x]++;

            shelves[x] = realloc(shelves[x], books[x] * sizeof(int));

            shelves[x][books[x] - 1] = y;
        }
        else if (type == 2)
        {
            scanf("%d", &y);
            printf("%d\n", shelves[x][y]);
        }
        else if (type == 3)
        {
            printf("%d\n", books[x]);
        }
    }

    for (int i = 0; i < n; i++)
    {
        free(shelves[i]);
    }

    free(shelves);
    free(books);

    return 0;
}
```


Output:

<img width="592" height="272" alt="image" src="https://github.com/user-attachments/assets/d6131e3f-7785-4e5c-8bc2-d485018b4dd6" />


Result:
Thus, the program to write the logic for the requests is verified successfully.


 
EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.
Aim:
To write a C program print the sum of the integers in the array.

Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



Program:
```
#include <stdio.h>
#include <stdlib.h>
int main() {
    int n;
    int sum = 0;
    scanf("%d", &n);  
    int *arr = (int *)malloc(n * sizeof(int));
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }
    for (int i = 0; i < n; i++) {
        sum += arr[i];
    }
    printf("%d\n", sum);
    free(arr);
    return 0;
}

```

Output:


 <img width="1131" height="370" alt="image" src="https://github.com/user-attachments/assets/a2a28fc0-56c5-4f25-984f-377f6f125b64" />



Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
EXP NO 25: C PROGRAM TO PRINT THE 9TH TERM OF THE SERIES



Aim:

To write a C program print the 9th term of the series,S(n).

Algorithm:

1. Start
2. Read the value of n.
3. Read the first three terms a, b, and c.
4. Define a recursive function series(n, a, b, c).
If n == 1, return a.
If n == 2, return b.
If n == 3, return c.
Otherwise, call the function recursively with:
n - 1
b
c
a + b + c
5. Print the returned value.
6. Stop.

Program:
```
#include<stdio.h>
int series(int n,int n1,int n2,int n3){
    if(n==1)
      return n1;
    if(n==2)
      return n2;
    if(n==3)
      return n3;
    return series(n-1,n1,n2,n3)+series(n-2,n1,n2,n3)+series(n-3,n1,n2,n3);
}
int main(){
    int n,n1,n2,n3;
    scanf("%d%d%d%d",&n,&n1,&n2,&n3);
    printf("%d",series(n,n1,n2,n3));
}
```

Output:

<img width="542" height="177" alt="image" src="https://github.com/user-attachments/assets/dd5f64ca-b7ff-49c5-a3c8-d030d0cd8d7e" />





Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.

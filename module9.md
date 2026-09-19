EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

Aim:
To write a C program to display stack elements using an array.
Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
Program:

```
char stack[100];
int top,i;
void display()
{
    for(i=top;i>=0;i--)
    {
        printf("%c\n",stack[i]);
    }
}
```

Output:

<img width="615" height="577" alt="image" src="https://github.com/user-attachments/assets/3c10aaf8-8ef0-47d4-8a72-7a168e3094bd" />




Result:
Thus, the program to display stack elements using an array is verified successfully.
 

EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
Aim:
To create a C program to push the given element in to a stack using array.
Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
Program:

```
int size=3,top=-1,stack[100];
void push (int data)
{
    if (top == size-1 )
    {
    printf("stack is full");
    }
    else
    {
        top = top +1;
        stack[top] = data;
    }
}
```

Output:


<img width="970" height="545" alt="image" src="https://github.com/user-attachments/assets/799a952e-5a19-4266-87e7-30a9d88f2a8d" />


Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
Aim:
To write a C program to display queue elements using array

Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
Program:

```
int queue[50], rear=-1, front=-1;
int i;
void display()
{
    if(front==-1 || front>rear)
    {
        printf("No elements to display\n");
    }
    else{
        for(i=front;i<=rear;i++)
            printf("%d ",queue[i]);
    }
}
```

Output:

<img width="965" height="527" alt="image" src="https://github.com/user-attachments/assets/0b9efed2-8881-4352-a685-62a5a9c09373" />



Result:
Thus, the program to display queue elements using array is verified successfully.


 
EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
Aim:
To write a C program to insert elements in queue using array.

Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

Program:

```
int queue[50];
int front=-1,rear=-1;
int size=3;
void enqueue(int data)
{
    if(rear<size)
    {
        if(front==-1)
            front=0;
    }
    rear++;
    queue[rear]=data;
    
}
```

Output:

<img width="927" height="467" alt="image" src="https://github.com/user-attachments/assets/80137a79-cbdd-4cad-945c-6239a210968b" />



Result:
Thus, the program to insert elements in queue using array is verified successfully.



 
EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY



Aim:

To create a function in C that deletes an element from a queue implemented using an array.

Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.



Program:

```
int queue[50];
int front, rear;
void dequeue()
{
    if(front==-1)
    {
        printf("No elements to display\n");
    }
    else
    {
        front++;
    }
}
```

Output:

<img width="1002" height="641" alt="image" src="https://github.com/user-attachments/assets/cea4dea4-5f64-425a-a230-abeaa5cba0f8" />




Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.

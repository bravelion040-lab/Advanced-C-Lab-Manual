EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.
Aim:
To write a C program to search a given element in the given linked list.

Algorithm:
1.	Define the structure for a node in a linked list.
2.	Define the search function to find a specific character in the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the search function and perform other linked list operations as needed.
 
Program:

```
struct Node{
    char data; 
    struct Node *next;
}*head;
void search(int data)
{
    struct Node *temp=head;
    int pos=1;
    while(temp!=NULL){
        if(temp->data==data){
            printf("item %c found at location %d\n",temp->data,pos);
            return ;
        }
        temp=temp->next;
        pos++;
    }
    printf("Item not found");
}
```

Output:

<img width="1016" height="500" alt="image" src="https://github.com/user-attachments/assets/73703764-b2ad-4a23-b286-eb5042661791" />




Result:
Thus, the program to search a given element in the given linked list is verified successfully.


 
EXP NO:17  PROGRAM TO INSERT A NODE IN A LINKED LIST.
Aim:
To write a C program to insert a node in a linked list.
Algorithm:
1.	Define the structure for a node in a linked list
2.	Define the insert function to insert a new node with character data at the end of the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the insert function and perform other linked list operations as needed.
 
Program:

```
struct Node{
    int data; 
    struct Node *next;
}*head;


void insert(int data)
{
    struct Node *n = (struct Node *)malloc(sizeof(struct Node));
    struct Node *temp;

    n->data = data;
    n->next = NULL;

    if (head == NULL)
    {
        head = n;
        return;
    }

    temp = head;

    while (temp->next != NULL)
    {
        temp = temp->next;
    }

    temp->next = n;
}
```

Output:

<img width="1021" height="505" alt="image" src="https://github.com/user-attachments/assets/861c99fd-8df0-4cec-8fe7-804564b490d9" />


 
Result:
Thus, the program to insert a node in a linked list is verified successfully.


 
EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST
Aim:
To write a C program to traverse a doubly linked list.

Algorithm:
1.	Initialize a temporary pointer (temp) to the head of the list.
2.	Use a while loop to traverse the list until the end (temp == NULL) is reached.
3.	Inside the loop, print the data of the current node.
4.	Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).
 
Program:

```
struct Node
{
    struct Node *prev;
    struct Node *next;
    float data;
}*head;
void display()
{
    struct Node *temp=head;
    while(temp!=NULL)
    {
        printf("%.2f\n",temp->data);
        temp=temp->next;
    }
}
```

Output:

<img width="815" height="496" alt="image" src="https://github.com/user-attachments/assets/8454b8e1-6685-4a05-910a-42bb2d7ffb4e" />



Result:
Thus, the program to traverse a doubly linked list is verified successfully. 



EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST
Aim:
To write a C program to insert an element in doubly linked list

Algorithm:
1.	Create a new node (newNode) and allocate memory for it.
2.	Set the data of the new node to the provided value.
3.	If the list is empty, set the new node as the head.
4.	If the list is not empty, traverse the list to find the last node.
5.	Set the new node's prev pointer to the last node and update the last node's next pointer to the new node.
 
Program:


```
struct Node
{
    struct Node *prev;
    struct Node *next;
    char data;
}*head;

void insert(char data)
{
    struct Node *n,*temp;
    n=(struct Node*)malloc(sizeof(struct Node*));
    n->data=data;
    n->prev=NULL;
    n->next=NULL;
    if(head==NULL)
    head=n;
    else
    {
        temp=head;
        while(temp->next!=NULL)
        temp=temp->next;
        temp->next=n;
        n->prev=temp;
    }
}
```

Output:


<img width="852" height="475" alt="image" src="https://github.com/user-attachments/assets/ad122bf2-60f7-46de-b0fa-702af6fe7ea1" />


Result:
Thus, the program to insert an element in doubly linked list is verified successfully.




EXP NO:20 C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST


Aim:
To write a C function that deletes a given element from a linked list.

Algorithm:
1.	Check if the Linked List is Empty:
o	If the head of the linked list is NULL, print a message indicating the list is empty and exit the function.
2.	Traverse the Linked List:
o	Start from the head node and iterate through the list to find the node that contains the given element (data).
3.	Handle Deletion of the First Node:
o	If the element to be deleted is found in the head node:
	Update the head of the linked list to point to the next node (i.e., head = head->next).
	Free the memory allocated to the node to be deleted.
	Exit the function.
4.	Traverse and Delete from the Middle or End:
o	If the element is not in the head node, continue traversing the list by checking each node’s next pointer.
o	When the node with the element is found, update the previous node’s next pointer to point to the next node of the node to be deleted (prev->next = current->next).
o	Free the memory allocated to the node to be deleted.
5.	Handle the Case when the Element is Not Found:
o	If the element is not found in any node, print a message indicating the element is not present in the list.
6.	End the Function.


Program:


```
struct Node{
    char data; 
    struct Node *next;
}*head;
void delete()
{
    struct Node *temp=head;
    if(head==NULL){
        printf("List is empty");
        return;
    }
    head=head->next;
    free(temp);
    printf("Node deleted from the begining ...\n");
}
```

Output:

<img width="1072" height="691" alt="image" src="https://github.com/user-attachments/assets/ee2fab8c-91b8-4d63-b1e1-c9cdc0660c7c" />




Result:
Thus, the function that deletes a given element from a linked list is verified successfully.

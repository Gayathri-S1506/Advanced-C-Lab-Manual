

EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.
Aim:
To write a C program to display stack elements using linked list.

Algorithm:
1.	Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.
2.	Declare a global variable head representing the starting node of the linked list.
3.	Define a function display to print the elements of the linked list.
4.	Declare a pointer p and initialize it with the head of the linked list.
5.	Use a while loop to traverse the linked list:
6.	Print the data of the current node.
7.	Move to the next node using the next pointer.
 
Program:

//type your code here
```
struct Node   
{  
    float data;
    struct Node*next;
}*head;
void display()
{
    struct Node *ptr;
    ptr=head;
    while(ptr!=NULL){
        printf("%.3f\n",ptr->data);
        ptr=ptr->next;
    }
}
```

Output:

//paste your output here
<img width="706" height="574" alt="image" src="https://github.com/user-attachments/assets/554b1078-7865-49ea-bb49-a4f26d1606a5" />



Result:
Thus, the program to display stack elements using linked list is verified successfully. 



EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING 
LINKED LIST.
Aim:
To write a C program to pop an element from the given stack using liked list.

Algorithm:
1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
Program:

//type your code here
```
struct Node
{
    int data;
    struct Node *next;
}*head; 
void pop()
{
    if(head==NULL)
    {
        printf("stack is empty");        
    }
    else
    {
        head=head->next;    
    }
}
```

Output:

//paste your output here
<img width="797" height="557" alt="image" src="https://github.com/user-attachments/assets/0628d6a6-07cb-4d82-bfdb-b02a213611d9" />




Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.
Aim:
To write a C program to display queue elements using linked list.
Algorithm:
1.	Check if Queue is Empty
2.	Display Queue Elements
3.	Print the data of the current node pointed to by front
4.	Update front to point to the next node.
5.	End the display function.
 
Program:

//type your code here
```
struct Node
{
   char data;
   struct Node *next;
}*front=NULL,*rear=NULL,*t;
void display()
{
    if(front==NULL){
        printf("queue is empty");
    }else{
       struct Node *t=front;
       printf("queue elements:\n");
        while(t!=NULL){
            printf("%c\n",t->data);
            t=t->next;
        }
    }
}
```



Output:

//paste your output here
<img width="835" height="605" alt="image" src="https://github.com/user-attachments/assets/1fd09ff7-14d2-49f1-827b-3c37e6c9bc93" />


Result:
Thus, the program to display queue elements using linked list is verified successfully.


 
EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

Aim:
To write a C program to insert elements in queue using linked list

Algorithm:
1.	Allocate Memory for New Node
2.	Set Data and Next Pointer
3.	Check if Queue is Empty
4.	Set both front and rear to point to the new node p.
5.	Set the next pointer of the current rear to point to the new node p.
6.	End of Enqueue Operation
 
Program:

//type your code here
```
struct Node
{
   float data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void enqueue(float data)
{
    struct Node*newnode = (struct Node*)malloc(sizeof(struct Node));
    newnode->data = data;
    newnode->next = NULL;
    
    if (front == NULL)
    {
        front = newnode;
        rear = newnode;
    }
    else
    {
        rear->next = newnode;
        rear = newnode;
    }
}
```


Output:

//paste your output here
<img width="734" height="543" alt="image" src="https://github.com/user-attachments/assets/525746a5-e50d-4210-bb68-6f38c576a856" />


Result:
Thus, the program to insert elements in queue using linked list is verified successfully.



EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.


Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

Algorithm:

1.	Check if the queue is empty:
o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
2.	Access the front element:
o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

Program:

//type your code here]
```
struct Node
{
   float data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void peek()
{
    printf("%.2f",front->data);
}
```

Output:

//paste your output here
<img width="614" height="645" alt="image" src="https://github.com/user-attachments/assets/9fede1d2-6611-4781-8770-68e716662bea" />




Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.



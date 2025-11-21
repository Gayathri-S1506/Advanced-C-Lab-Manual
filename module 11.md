

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
//type your code here
```
#include<stdio.h>
int main(){
    int a,b,c,d;
    scanf("%d%d%d%d",&a,&b,&c,&d);
    if(a>b&&a>c&&a>d){
        printf("%d",a);
    }else if(b>a&&b>c&&b>d){
        printf("%d",b);
    }else if(c>a&&c>b&&c>d){
        printf("%d",c);
    }else{
        printf("%d",d);
    }
}
```

Output:
//paste your output here
<img width="536" height="431" alt="image" src="https://github.com/user-attachments/assets/a175019f-90e4-4962-bc50-1e212cb5014b" />

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
//type your code here
```
#include<stdio.h>
int main()
{
    int a,b;
    scanf("%d%d",&a,&b);
    int and=0,or=0,xor=0;
    for(int i=1;i<a;i++){
        for(int j=i+1;j<=a;j++){
            if((i&j)>and&&(i&j)<b){
                and=i&j;
            }
            if((i|j)>or&&(i|j)<b){
                or=i|j;
            }
            if((i^j)>xor&&(i^j)<b){
                xor=i^j;
            }
        }
    }
    printf("%d\n%d\n%d",and,or,xor);
    
}
```

Output:
//paste your output here
<img width="738" height="461" alt="image" src="https://github.com/user-attachments/assets/39d0ff79-565c-4788-abd5-805a46a7b417" />


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
//type your code here
```
#include<stdio.h>
#include<stdlib.h>
int* total_no_of_books;
int** total_no_of_pages;
int main()
{
    int total_no_of_shelves;
    scanf("%d",&total_no_of_shelves);
    
    total_no_of_books=calloc(total_no_of_shelves,sizeof(int));
    
    int total_no_of_queries;
    scanf("%d",&total_no_of_queries);
    
    total_no_of_pages=malloc(total_no_of_shelves*sizeof(int*));
    for(int i=0; i<total_no_of_shelves; i++)
    {
        total_no_of_pages[i]=calloc(1100,sizeof(int));
    }
    while(total_no_of_queries--)
    {
        int type_of_query;
        scanf("%d",&type_of_query);
        if(type_of_query==1)
        {
            int shelf,pages;
            scanf("%d%d",&shelf,&pages);
            total_no_of_books[shelf]++;
            int *book= total_no_of_pages[shelf];
            while(*book!=0)
            book++;
            *book=pages;
        }
        else if(type_of_query==2)
        {
            int x,y;
            scanf("%d%d",&x,&y);
            printf("%d\n",*(*(total_no_of_pages+x)+y));
        }
        else
        {
            int x;
            scanf("%d",&x);
            printf("%d\n",*(total_no_of_books+x));
        }
    }
    if(total_no_of_books)
    {
        free(total_no_of_books);
    }
    for(int i=0;i<total_no_of_shelves;i++)
    {
        if(*(total_no_of_pages+i))
        {
            free(*(total_no_of_pages+i));
        }
    }
    if(total_no_of_pages){
        free(total_no_of_pages);
    }
    return 0;
}
```

Output:
//paste your output here
<img width="509" height="406" alt="image" src="https://github.com/user-attachments/assets/89c409d1-bd43-45be-b947-97071002b5fb" />



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
//type your code here
```
#include<stdio.h>
int main(){
    int a,i,sum=0;
    scanf("%d",&a);
    int b[a];
    for(i=0;i<a;i++){
        scanf("%d",&b[i]);
        sum+=b[i];
    }
    printf("%d",sum);
}
```

Output:
//paste your output here
<img width="695" height="343" alt="image" src="https://github.com/user-attachments/assets/fff37901-ee17-4c90-94f5-d5277dded4d8" />


 


Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A      SENTENCE



Aim:

To write a C program that counts the number of words in a given sentence.

Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



Program:
//type your code here
```
#include<stdio.h>
#include<string.h>
int main()
{
    char str[100];
    fgets(str,sizeof(str),stdin);
    int len=sizeof(str);
    int count=1;
     for(int i=0;i<len-1;i++){
         if(str[i]==' ')
         count++;
         
     }
     printf("Total number of words in the string is :%d",count);
    return 0;
}
```

Output:
//paste your output here
<img width="812" height="148" alt="image" src="https://github.com/user-attachments/assets/6c8e2a8b-d1de-4ddc-bd59-505540f9d057" />






Result:
Thus, the program that counts the number of words in a given sentence is verified successfully.


EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER
Aim:
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

//type your code here
```
#include<stdio.h>
int main()
{
    int a;
    scanf("%d",&a);
    switch(a)
    {
        case 11:
        printf("eleven");
        break;
        case 12:
        printf("twelve");
        break;
        case 13:
        printf("thirteen");
        break;
        case 14:
        printf("fourteen");
        break;
        case 15:
        printf("fifteen");
        break;
        case 16:
        printf("sixteen");
        break;
        case 17:
        printf("seventeen");
        break;
        case 18:
        printf("eighteen");
        break;
        case 19:
        printf("nineteen");
        break;
        default:
        printf("Greater than 19");
        break;
    }
}
```



Output:


//paste your output here
<img width="617" height="332" alt="image" src="https://github.com/user-attachments/assets/5bf9a8e9-20e8-4d32-92fb-f1f30d3cd29f" />



Result:
Thus, the program is verified successfully
 
EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS     IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 .
Aim:
To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.
Algorithm:
1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 3
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
Program:

//type your code here
```
#include<stdio.h>
#include<string.h>
int main()
{
    char num[100];
    int freq[10]={0};
    scanf("%s",num);
    for(int i=0;i<strlen(num);i++)
    {
        if(num[i]>='0'&&num[i]<='9')
        {
            freq[num[i]-'0']++;
        }
    }
    for(int i=0;i<10;i++)
    {
        printf("%d ",freq[i]);
    }
    return 0;
}
```




Output:

//paste your output here

<img width="855" height="306" alt="image" src="https://github.com/user-attachments/assets/aa3ddcec-fa81-4aa9-8ec1-fb8f158f8bb0" />





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

//type your code here
```
#include<stdio.h>
#include<stdlib.h>
#include<string.h>
void swap(char**s,int i,int j)
{
    char*temp=s[i];
    s[i]=s[j];
    s[j]=temp;
}
void reverse(char**s,int start,int end)
{
    while(start<end)
    {
        swap(s,start++,end--);
    }
}
int next(int n,char**s)
{
    for(int i=n-2;i>-1;i--)
    {
        if(strcmp(s[i+1],s[i])>0)
        {
            for(int j=n-1;j>i;j--)
            {
                if(strcmp(s[j],s[i])>0)
                {
                    swap(s,i,j);
                    reverse(s,i+1,n-1);
                    return 1;
                }
            }
        }
    }
    return 0;
}
int main()
{
    int n;
    char **s;
    scanf("%d",&n);
    s=calloc(n,sizeof(char));
    for(int i=0;i<n;i++)
    {
        s[i]=calloc(11,sizeof(char));
        scanf("%s",s[i]);
    }
    do{
        for(int i=0;i<n;i++)
        printf("%s%c",s[i],i==n-1?'\n':' ');
    }while(next(n,s));
    for(int i=0;i<n;i++)
    free(s[i]);
    free(s);
}
```




Output:


//paste your output here
<img width="561" height="462" alt="image" src="https://github.com/user-attachments/assets/8bc410fe-51e3-4699-8c0c-d9a712c9f716" />







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

//type your code here
```
#include<stdio.h>
int main()
{
int a;
scanf("%d",&a);
int n=a;
int l=(n*2)-1;
int i,j;
for(i=0;i<l;i++)
{
for(j=0;j<l;j++)
{
int min=i<j?i:j;
min=min<l-i-1?min:l-i-1;
min=min<l-j-1?min:l-j-1;
printf("%d ",n-min);
}
printf("\n");
} 
return 0;
}
```




Output:


//paste your output here
<img width="752" height="662" alt="image" src="https://github.com/user-attachments/assets/bb050e17-3d71-4a17-ad1d-57dcff4fab96" />







Result:
Thus, the program is verified successfully

EXP NO:10 C PROGRAM TO FIND A SQUARE  OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

Algorithm:

1.	Start.
2.	Define a function square() with no parameters. This function will return an integer value.
3.	Inside the function:
o	Declare an integer variable to store the number.
o	Ask the user to input a number.
o	Calculate the square of the number (multiply the number by itself).
o	Return the squared value.
4.	In the main function:
o	Call the square() function and display the result.
5.	End.

Program:

//type your code here
```
#include <stdio.h>
void square();
int main(){
    
    square();
    return 0;
}
void square(){
    int a;
    scanf("%d",&a);
    float ans = a*a;
    printf("The square of %d is : %.2f",a,ans);
}


```





Output:


//paste your output here

<img width="930" height="296" alt="image" src="https://github.com/user-attachments/assets/3273b12f-e7c9-47ab-a7a3-370f36686df0" />







Result:
Thus, the program is verified successfully




























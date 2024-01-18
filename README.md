Lab Sheet #3 : Arrays, Pointers and Strings
Program 1: Write a Program to reverse the array elements in C
Programming
#include<stdio.h>
void main()
{
int n, arr[100], i, rev[100], j = 0;
printf("Enter the size of the array: ");
scanf("%d", &n);
printf("Enter the elements: ");
for(i = 0; i < n; i++)
{
scanf("%d", &arr[i]);
}
for(i = n-1; i >= 0; i--)
{
rev[j] = arr[i];
j++;
}
printf("The Reversed array: ");
for(i = 0; i < n; i++)
{
printf("%d\t", rev[i]);
}
}
Program 2: Write a Program to delete an element from an array
#include <stdio.h>
Lab Sheet #3 : Arrays, Pointers and Strings
int main()
{
int array[100], position, i, n;
printf("Enter number of elements in array\n");
scanf("%d", &n);
printf("Enter %d elements\n", n);
for ( i= 0 ; i < n ; i++ )
scanf("%d", &array[i]);
printf("Enter the location where you wish to delete element\n");
scanf("%d", &position);
if ( position >= n+1 )
printf("Deletion not possible.\n");
else
{
for ( i = position - 1 ; i < n - 1 ; i++ )
array[i] = array[i+1];
printf("Resultant array is\n");
for( i= 0 ; i < n - 1 ; i++ )
printf("%d\n", array[i]);
}
return 0;
}
Program 3: Sorting an array
#include<stdio.h>
void main ()
{
int i, j,temp;
Lab Sheet #3 : Arrays, Pointers and Strings
int a[10] = { 10, 9, 7, 101, 23, 44, 12, 78, 34, 23};
for(i = 0; i<10; i++)
{
for(j = i+1; j<10; j++)
{
if(a[j] > a[i])
{
temp = a[i];
a[i] = a[j];
a[j] = temp;
}
}
}
printf("Printing Sorted Element List ...\n");
for(i = 0; i<10; i++)
{
printf("%d\n",a[i]);
}
}
Program 4: Write a program to find the largest element in an array and
position of its occurrence
#include<stdio.h>
#include<conio.h>
void main()
{
int a[100];
int largest,position,num,index;
clrscr();
printf("enter number of elements in the array");
scanf("%d",&num);
for(index=0;index<num;index++)
Lab Sheet #3 : Arrays, Pointers and Strings
{
scanf("%d",&a[index]);
}
largest=a[0]; /* assign first element of the array as largest */
position=0; /* position of largest element in the array */
for(index=1; index<num; index++)
{
if(largest<a[index])
{
largest=a[index];
position=index;
}
}
printf("largest element in the array is %d\n",largest);
printf("largest element's position in the array %d\n",position+1);
getch();
}
Program 5: Write a C program for addition of two matrix
#include<stdio.h>
#include<conio.h>
void main()
{
int n,i,j,a[5][5],b[5][5],c[5][5];
clrscr();
printf("Enter the order of matrix:");
scanf("%d",&n);
printf("\nEnter A matrix elements:");
for(i=0;i<n;i++)
{
for(j=0;j<n;j++)
{
scanf("%d",&a[i][j]);
}
}
printf("\nEnter B matrix elements:");
for(i=0;i<n;i++)
{
for(j=0;j<n;j++)
Lab Sheet #3 : Arrays, Pointers and Strings
{
scanf("%d",&b[i][j]);
}
}
printf("\n Addition of matrix are\n");
for(i=0;i<n;i++)
{
for(j=0;j<n;j++)
{
c[i][j]=a[i][j]+b[i][j];
}
}
printf("\n Sum of matrix are\n");
for(i=0;i<n;i++)
{
for(j=0;j<n;j++)
{
printf("%d\t",c[i][j]);
}
printf("\n");
}
getch();
}
Program 6: Write a C program to find Product of two matrix, when different
order is given for both matrix
#include<stdio.h>
#include<conio.h>
void main()
{
int m,n,p,q,i,j,a[5][5],b[5][5],c[5][5],k;
clrscr();
printf("Enter the order of A matrix:");
scanf("%d %d",&m,&n);
printf("\nEnter the order of B martix:");
scanf("%d %d",&p,&q);
if(n==p)
{
printf("\nEnter A matrix elements:");
for(i=0;i<m;i++)
{
for(j=0;j<n;j++)
Lab Sheet #3 : Arrays, Pointers and Strings
{
scanf("%d",&a[i][j]);
}
}
printf("\nEnter B matrix elements:");
for(i=0;i<p;i++)
{
for(j=0;j<q;j++)
{
scanf("%d",&b[i][j]);
}
}
printf("\n Multiplication of matrix are\n");
for(i=0;i<m;i++)
{
for(j=0;j<q;j++)
{
c[i][j]=0;
for(k=0;k<n;k++)
{
c[i][j]=c[i][j]+a[i][k]*b[k][j];
}
}
}
printf("\n Product of matrix are\n");
for(i=0;i<m;i++)
{
for(j=0;j<q;j++)
{
printf("%d\t",c[i][j]);
}
printf("\n");
}
}
else
{
printf("\n invalid order of matrix");
}
getch();
}
Lab Sheet #3 : Arrays, Pointers and Strings
Program 7: Write a C program to find sum of principal diagonal elements.
#include<stdio.h>
#include<conio.h>
void main()
{
int a[10][10],n,i,j,sum=0;
clrscr();
printf("Enter the size of an array:");
scanf("%d",&n);
printf("\n Enter array elements:");
for(i=0;i<n;i++)
{
for(j=0;j<n;j++)
{
scanf("%d",&a[i][j]);
}
}
printf("\n Array elements are:\n");
for(i=0;i<n;i++)
{
for(j=0;j<n;j++)
{
printf("%d\t",a[i][j]);
}
printf("\n");
}
for(i=0;i<n;i++)
{
for(j=0;j<n;j++)
{
if(i==j)
{
sum=sum+a[i][j];
}
}
}
printf("\n sum of principal diagonal = %d",sum);
getch();
}
Lab Sheet #3 : Arrays, Pointers and Strings
Program 8: Example of Pointer demonstrating the use of & and *
#include <stdio.h>
int main()
{
/* Pointer of integer type, this can hold the address of a integer type variable. */
int *p;
int var = 10;
/* Assigning the address of variable var to the pointer * p. The p can hold the
address of var because var is an integer type variable. */
p= &var;
printf("Value of variable var is: %d", var);
printf("\nValue of variable var is: %d", *p);
printf("\nAddress of variable var is: %p", &var);
printf("\nAddress of variable var is: %p", p);
printf("\nAddress of pointer p is: %p", &p);
return 0;
}
Program 9: C program to add two numbers using pointers
#include <stdio.h>
int main()
{
int first, second, *p, *q, sum;
printf("Enter two integers to add\n");
Lab Sheet #3 : Arrays, Pointers and Strings
scanf("%d%d", &first, &second);
p = &first;
q = &second;
sum = *p + *q;
printf("Sum of entered numbers = %d\n",sum);
return 0;
}
Program 10: C program to swap two numbers using pointers
#include <stdio.h>
int main() {
int a, b, temp;
int *ptr1, *ptr2;
printf("Enter the value of a and b: ");
scanf("%d %d", &a, &b);
printf("\nBefore swapping a = %d and b = %d", a, b);
// Assign the memory address of a and b to *ptr1 and *ptr2
ptr1 = &a;
ptr2 = &b;
// Swap the values a and b
temp = *ptr1;
*ptr1 = *ptr2;
*ptr2 = temp;
printf("\nAfter swapping a = %d and b = %d", a, b);
return 0;
}
Lab Sheet #3 : Arrays, Pointers and Strings
Program 11: Write a menu driven program to perform the following operations on
strings using standard library functions: 1. Length of String 2. Connect Two Strings
3. Copy String 4. Compare two strings
#include<stdio.h>
#include<string.h>
#include<stdlib.h>
int main()
{
char str1[20],str2[20];
int ch,i,j;
do
{
printf("\tMENU");
printf("\n------------------------------\n");
printf("1:Find Length of String");
printf("\n2:Concatenate Strings");
printf("\n3:Copy String ");
printf("\n4:Compare Strings");
printf("\n5:Exit");
printf("\n------------------------------\n");
printf("\nEnter your choice: ");
scanf("%d",&ch);
switch(ch)
{
case 1:
printf("Enter String: ");
Lab Sheet #3 : Arrays, Pointers and Strings
scanf("%s",str1);
i=strlen(str1);
printf("Length of String : %d\n\n",i);
break;
case 2:
printf("\nEnter First String: ");
scanf("%s",str1);
printf("Enter Second string: ");
scanf("%s",str2);
strcat(str1,str2);
printf("String After Concatenation : %s\n\n",str1);
break;
case 3:
printf("Enter a String1: ");
scanf("%s",str1);
printf("Enter a String2: ");
scanf("%s",str2);
printf("\nString Before
copied:\nString1=\"%s\",String2=\"%s\"\n",str1,str2);
strcpy(str2,str1);
printf("-----------------------------------------------\n");
printf("\"We are copying string String1 to String2\" \n");
printf("-----------------------------------------------\n");
printf("String After Copied:\nString1=\"%s\", String2=\"%s\"\n\n",str1,str2);
break;
case 4:
printf("Enter First String: ");
scanf("%s",str1);
printf("Enter Second String: ");
Lab Sheet #3 : Arrays, Pointers and Strings
scanf("%s",str2);
j=strcmp(str1,str2);
if(j==0)
{
printf("Strings are Same\n\n");
}
else
{
printf("Strings are Not Same\n\n");
}
break;
case 5:
exit(0);
break;
default:
printf("Invalid Input. Please Enter valid Input.\n\n ");
}
}while(ch!=5);
return 0;
}
Program 12. Write C Program to Count Occurrence of Character
// C Program to Count Occurrence of Character
#include <stdio.h>
int main()
{
int count = 0;
char ch, s[25];
int i = 0;
printf("Enter the string");
Lab Sheet #3 : Arrays, Pointers and Strings
scanf("%s", &s);
printf("String :--> %s", s);
printf("\nEnter Character :--> ");
scanf("%s", &ch);
while(s[i] != '\0')
{
if (s[i] == ch)
count++;
i++;
}
printf("\nOccurrence of character :--> %d", count);
return 0;
}

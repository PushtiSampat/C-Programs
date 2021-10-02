# C-Programs
Any Type of C Programs
C Program to Find ASCII Value of a Character

#include <stdio.h>
int main() {  
    char c;
    printf("Enter a character: ");
    scanf("%c", &c);  
    
    // %d displays the integer value of a character
    // %c displays the actual character
    printf("ASCII value of %c = %d", c, c);
    
    return 0;
}

C Program to Multiply Two Floating-Point Numbers
#include <stdio.h>
int main() {
    double a, b, product;
    printf("Enter two numbers: ");
    scanf("%lf %lf", &a, &b);  
 
    // Calculating product
    product = a * b;

    // %.2lf displays number up to 2 decimal point
    printf("Product = %.2lf", product);
    
    return 0;
}


C Program to Swap Two Numbers
#include<stdio.h>
int main() {
  double first, second, temp;
  printf("Enter first number: ");
  scanf("%lf", &first);
  printf("Enter second number: ");
  scanf("%lf", &second);

  // value of first is assigned to temp
  temp = first;

  // value of second is assigned to first
  first = second;

  // value of temp (initial value of first) is assigned to second
  second = temp;

  // %.2lf displays number up to 2 decimal points
  printf("\nAfter swapping, first number = %.2lf\n", first);
  printf("After swapping, second number = %.2lf", second);
  return 0;
}

C Program to Check Whether a Number is Even or Odd
#include <stdio.h>
int main() {
    int num;
    printf("Enter an integer: ");
    scanf("%d", &num);

    // true if num is perfectly divisible by 2
    if(num % 2 == 0)
        printf("%d is even.", num);
    else
        printf("%d is odd.", num);
    
    return 0;
}

C Program to Check Whether a Number is Prime or not 
#include<stdio.h>  
int main(){    
    int n,i,m=0,flag=0;    
    printf("Enter the number to check prime:");    
    scanf("%d",&n);    
    m=n/2;    
    for(i=2;i<=m;i++)    
    {    
        if(n%i==0)    
        {    
            printf("Number is not prime");    
            flag=1;    
            break;    
        }    
    }    
    if(flag==0)    
    printf("Number is prime");     
    return 0;  
 }    
 
 c program to check Armstrong Number in C
 #include<stdio.h>  
 int main()    
{    
    int n,r,sum=0,temp;    
    printf("enter the number=");    
    scanf("%d",&n);    
    temp=n;    
    while(n>0)    
    {    
        r=n%10;    
        sum=sum+(r*r*r);    
        n=n/10;    
    }    
    if(temp==sum)    
        printf("armstrong  number ");    
    else    
        printf("not armstrong number");    
    return 0;  
}   

 c program to check whether number is palindrome or not
 #include<stdio.h>  
int main()    
{    
    int n,r,sum=0,temp;    
    printf("enter the number=");    
    scanf("%d",&n);    
    temp=n;    
    while(n>0)    
    {    
        r=n%10;    
        sum=(sum*10)+r;    
        n=n/10;    
    }    
    if(temp==sum)    
        printf("palindrome number ");    
    else    
        printf("not palindrome");   
    return 0;  
}

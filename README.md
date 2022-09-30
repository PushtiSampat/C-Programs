# C-Programs

## Any Type of C Programs ##


### C Program to print Alphabet Triangle ###

#include<stdio.h>    
#include<stdlib.h>  
int main(){  
  int ch=65;    
    int i,j,k,m;    
  system("cls");  
    for(i=1;i<=5;i++)    
    {    
        for(j=5;j>=i;j--)    
            printf(" ");    
        for(k=1;k<=i;k++)    
            printf("%c",ch++);    
            ch--;    
        for(m=1;m<i;m++)    
            printf("%c",--ch);    
        printf("\n");    
        ch=65;    
    }    
return 0;  
} 


### C Program to Find ASCII Value of a Character ###

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

### C Program to Multiply Two Floating-Point Numbers ###

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


### C Program to Swap Two Numbers ###

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

### C Program to Check Whether a Number is Even or Odd ###

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

### C Program to Check Whether a Number is Prime or not ###

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
 
 ### c program to check Armstrong Number in C ###
 
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

### c program to check whether number is palindrome or not ###
 
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

### c program for Strings and Pointers ###

    #include <stdio.h>
    int main(void) {
    char name[] = "Harry Potter";

    printf("%c", *name);     // Output: H
    printf("%c", *(name+1));   // Output: a
    printf("%c", *(name+7));   // Output: o

    char *namePtr;

    namePtr = name;
    printf("%c", *namePtr);     // Output: H
    printf("%c", *(namePtr+1));   // Output: a
    printf("%c", *(namePtr+7));   // Output: o
    }

### c program for fibonacci series without recursion.
    #include<stdio.h>    
    int main()    
    {    
        int n1=0,n2=1,n3,i,number;    
        printf("Enter the number of elements:");    
        scanf("%d",&number);    
        printf("\n%d %d",n1,n2);//printing 0 and 1    
        for(i=2;i<number;++i)
        {    
            n3=n1+n2;    
            printf(" %d",n3);    
            n1=n2;    
            n2=n3;    
        }  
        return 0;  
    }   

### c program for fibonacci series with recursion.

    #include<stdio.h>    
    void printFibonacci(int n){    
        static int n1=0,n2=1,n3;    
        if(n>0){    
            n3 = n1 + n2;    
            n1 = n2;    
            n2 = n3;    
            printf("%d ",n3);    
            printFibonacci(n-1);    
        }    
    }    
    int main(){    
        int n;    
        printf("Enter the number of elements: ");    
        scanf("%d",&n);    
        printf("Fibonacci Series: ");    
        printf("%d %d ",0,1);    
        printFibonacci(n-2); 
    return 0;  
    }  

### c program for Sum of digits.
    #include<stdio.h>  
    int main()    
    {    
        int n,sum=0,m;    
        printf("Enter a number:");    
        scanf("%d",&n);    
        while(n>0)    
        {    
            m=n%10;    
            sum=sum+m;    
            n=n/10;    
        }    
        printf("Sum is=%d",sum);    
        return 0;  
    }   
### c program for reverse number.

    #include<stdio.h>  
    int main()    
    {    
    int n, reverse=0, rem;    
    printf("Enter a number: ");    
    scanf("%d", &n);    
    while(n!=0)    
    {    
        rem=n%10;    
        reverse=reverse*10+rem;    
        n/=10;    
    }    
    printf("Reversed Number: %d",reverse);    
    return 0;  
    }   

### C Program to print Number Triangle.
       1
      121
     12321
    1234321

    #include<stdio.h>    
    #include<stdlib.h>  
    int main(){  
        int i,j,k,l,n;    
        system("cls");  
        printf("enter the range=");    
        scanf("%d",&n);    
        
        for(i=1;i<=n;i++)    
        {    
            for(j=1;j<=n-i;j++)    
            {    
                 printf(" ");    
            }    
            for(k=1;k<=i;k++)    
            {    
                printf("%d",k);    
            }    
            for(l=i-1;l>=1;l--)    
            {    
                printf("%d",l);    
            }    
            printf("\n");    
        }    
        return 0;  
    }  
    
### C Program to print Alphabet Triangle.
        A
       ABA
      ABCBA
     ABCDCBA
    ABCDEDCBA

    #include<stdio.h>    
    #include<stdlib.h>  
    int main(){  
    int ch=65;    
        int i,j,k,m;    
    system("cls");  
        for(i=1;i<=5;i++)    
        {    
            for(j=5;j>=i;j--)    
                printf(" ");    
            for(k=1;k<=i;k++)    
                printf("%c",ch++);    
                ch--;    
            for(m=1;m<i;m++)    
                printf("%c",--ch);    
            printf("\n");    
            ch=65;    
        }    
    return 0;  
    }  
### C Program to print Prime Numbers Between Two Integers

    #include <stdio.h>
    int checkPrimeNumber(int n);
    int main() {
        int n1, n2, i, flag;
        printf("Enter two positive integers: ");
        scanf("%d %d", &n1, &n2);
        printf("Prime numbers between %d and %d are: ", n1, n2);
        for (i = n1 + 1; i < n2; ++i) {

            // flag will be equal to 1 if i is prime
            flag = checkPrimeNumber(i);

            if (flag == 1)
                printf("%d ", i);
        }
        return 0;
    }
 
    int checkPrimeNumber(int n) {
        int j, flag = 1;
        for (j = 2; j <= n / 2; ++j) {
            if (n % j == 0) {
                flag = 0;
                break;
            }
        }
        return flag;
    }
### C Program to calculate power using recursion
    #include <stdio.h>
    int power(int n1, int n2);
    int main() {
        int base, a, result;
        printf("Enter base number: ");
        scanf("%d", &base);
        printf("Enter power number(positive integer): ");
        scanf("%d", &a);
        result = power(base, a);
        printf("%d^%d = %d", base, a, result);
        return 0;
    }

    int power(int base, int a) {
        if (a != 0)
            return (base * power(base, a - 1));
        else
            return 1;
    }
### C Program to Concatenate two string
    #include <stdio.h>
    int main() {
      char s1[100] = "programming ", s2[] = "is awesome";
      int length, j;

      // store length of s1 in the length variable
      length = 0;
      while (s1[length] != '\0') {
        ++length;
      }

      // concatenate s2 to s1
      for (j = 0; s2[j] != '\0'; ++j, ++length) {
        s1[length] = s2[j];
      }

      // terminating the s1 string
      s1[length] = '\0';

      printf("After concatenation: ");
      puts(s1);

      return 0;
    }
### C Program to Find Largest Element in an Array
    #include <stdio.h>
    int main() {
      int n;
      double arr[100];
      printf("Enter the number of elements (1 to 100): ");
      scanf("%d", &n);

      for (int i = 0; i < n; ++i) {
        printf("Enter number%d: ", i + 1);
        scanf("%lf", &arr[i]);
      }

      // storing the largest number to arr[0]
      for (int i = 1; i < n; ++i) {
        if (arr[0] < arr[i]) {
          arr[0] = arr[i];
        }
      }

      printf("Largest element = %.2lf", arr[0]);

      return 0;
    }
### C Program to Encrypt text
    #include<stdio.h>
    #include<conio.h>
    void main()
    {
        int i, j, getchar1 = 0, getkey1 = 0, dec;
        char c = 32, input[50], encpy_table[100][100], key[]= "iMpoSSib1eteXtPleaSe#0071998", ENCRPYT[20], DECRYPT[20];
        printf("Enter The String : ");
        scanf("%s",input);
        for( i = 0; i < 91; i++ )
        {
            c = 32+i;
            for( j = 0; j < 91; j++ )
            {	
                encpy_table[i][j] = c;
                /*printf("%c ",encpy_table[i][j]);*/
                if(c == 122)
                    c = 32;
                else
                    c++;
            }
            /*printf("\n");*/
        }
        i=0;
        j=0;
        printf(" Encrypted Text = ");
        while(input[i] != '\0')
        {
            getchar1 = input[i]-32;
            if(key[j] == '\0')
            {
                j = 0;
            }
            else{
                getkey1 = key[j]-32;
            }
            ENCRPYT[i] = encpy_table[getchar1][getkey1];
            printf("%c",ENCRPYT[i]);
            i++;
            j++;
        }
        getch();
    }
### C Program for Matrix multiplication
    #include<stdio.h>
    #include<conio.h>
    void main()
    {
        int i,j,n,m,k,temp=0,mat1[10][10],mat2[10][10],rest[10][10];
        printf("Enter The Matrix : ");
        scanf("%d %d",&n,&m);
        for(i=0;i<n;i++)
        {
            for(j=0;j<m;j++)
            {
                printf("Enter The (%d,%d) of First matrix : ",i,j);
                scanf("%d",&mat1[i][j]);
            }
        }
        for(i=0;i<m;i++)
        {
            for(j=0;j<n;j++)
            {
                printf("Enter The (%d,%d) of Second matrix : ",i,j);
                scanf("%d",&mat2[i][j]);
            }
        }
        printf("The First Matrix\n");
        for(i=0;i<n;i++)
        {
            for(j=0;j<m;j++)
            {
                printf("%3d",mat1[i][j]);
            }
            printf("\n");
        }
        printf("The Second Matrix\n");
        for(i=0;i<m;i++)
        {
            for(j=0;j<n;j++)
            {
                printf("%3d",mat2[i][j]);
            }
            printf("\n");
        }
        printf("The Multiplication Of Both Matrix\n");
        for(i=0;i<n;i++)
        {
            for(j=0;j<n;j++)
            {
                for(k=0;k<m;k++)
                {
                    temp+=mat1[i][k]*mat2[k][j];
                }
                rest[i][j]=temp;
                temp=0;
                printf("%3d",rest[i][j]);
            }
            printf("\n");
        }
        getch();
    }
### C Program for Matrix Addition
    #include<stdio.h>
    #include<conio.h>
    void main()
    {
        int i,j,row,col,mat1[10][10],mat2[10][10],rest[10][10];
        printf("Enter The Matrix Dimension: ");
        scanf("%d %d",&row,&col);
        for(i=0;i<row;i++)
        {
            for(j=0;j<col;j++)
            {
                printf("Enter The (%d,%d) of First matrix : ",i,j);
                scanf("%d",&mat1[i][j]);
            }
        }
        for(i=0;i<row;i++)
        {
            for(j=0;j<col;j++)
            {
                printf("Enter The (%d,%d) of Second matrix : ",i,j);
                scanf("%d",&mat2[i][j]);
            }
        }
        printf("The First Matrix\n");
        for(i=0;i<row;i++)
        {
            for(j=0;j<col;j++)
            {
                printf("%3d",mat1[i][j]);
            }
            printf("\n");
        }
        printf("The Second Matrix\n");
        for(i=0;i<row;i++)
        {
            for(j=0;j<col;j++)
            {
                printf("%3d",mat2[i][j]);
            }
            printf("\n");
        }
        printf("The Addition Of Both Matrix");
        for(i=0;i<row;i++)
        {
            for(j=0;j<col;j++)
            {
                rest[i][j]=mat1[i][j]+mat2[i][j];
                printf("%3d",rest[i][j]);
            }
            printf("\n");
        }
        getch();
    }
### C Program to check if the Matrix is Lower / Upper / Diagonal.
    #include<stdio.h>
    #include<conio.h>
    void main()
    {
        int rows,cols, matrix[10][10], j, i, upper = 1, lower = 1;
        printf("Enter Rows : ");
        scanf("%d",&rows);
        printf("Enter Cols : ");
        scanf("%d",&cols);
        if(rows != cols) 
        {
            printf("\nNo possible Matrix in these rows and cols\n");
        }
        else
        {
            for(i = 0; i < rows; i++) 
            {
                for(j = 0; j < cols; j++) 
                {
                    printf("Enter (%d,%d) Element : ",i,j);
                    scanf("%d",&matrix[i][j]);
                }
            }
            for(i = 0; i < rows; i++) 
            {
                for(j = 0; j < cols; j++) 
                {
                    if(j < i && matrix[i][j] != 0)
                    {
                        upper=0;
                    }
                    if(j > i && matrix[i][j] != 0)
                    {
                        lower=0;
                    }
                }
            }
            if(upper && lower)
            {
                printf("\nThis is Diagonal Matrix");
            }
            else if(upper)
            {
                printf("\nThis is Upper Triangular Matrix\n");
            }
            else if(lower) 
            {
                printf("\nThis is Lower Triangular Matrix\n");
            }
            else
            {
                printf("\n Not Matching Patterns in Matrix \n");
            }
        }
    getch();
    }          
    
### C Program to Find Roots of a Quadratic Equation
    #include <math.h>
    #include <stdio.h>
    int main() {
        double a, b, c, discriminant, root1, root2, realPart, imagPart;
        printf("Enter coefficients a, b and c: ");
        scanf("%lf %lf %lf", &a, &b, &c);

        discriminant = b * b - 4 * a * c;

        // condition for real and different roots
        if (discriminant > 0) {
            root1 = (-b + sqrt(discriminant)) / (2 * a);
            root2 = (-b - sqrt(discriminant)) / (2 * a);
            printf("root1 = %.2lf and root2 = %.2lf", root1, root2);
        }

        // condition for real and equal roots
        else if (discriminant == 0) {
            root1 = root2 = -b / (2 * a);
            printf("root1 = root2 = %.2lf;", root1);
        }

        // if roots are not real
        else {
            realPart = -b / (2 * a);
            imagPart = sqrt(-discriminant) / (2 * a);
            printf("root1 = %.2lf+%.2lfi and root2 = %.2f-%.2fi", realPart, imagPart, realPart, imagPart);
        }

        return 0;
    } 

### C Program to Check Leap Year
    #include <stdio.h>
    int main() {
       int year;
       printf("Enter a year: ");
       scanf("%d", &year);

       // leap year if perfectly divisible by 400
       if (year % 400 == 0) {
          printf("%d is a leap year.", year);
       }
       // not a leap year if divisible by 100
       // but not divisible by 400
       else if (year % 100 == 0) {
          printf("%d is not a leap year.", year);
       }
       // leap year if not divisible by 100
       // but divisible by 4
       else if (year % 4 == 0) {
          printf("%d is a leap year.", year);
       }
       // all other years are not leap years
       else {
          printf("%d is not a leap year.", year);
       }

       return 0;
    }

### C Program to Check Whether a Character is a Vowel or Consonant

    #include <stdio.h>
    int main() {
        char c;
        int lowercase_vowel, uppercase_vowel;
        printf("Enter an alphabet: ");
        scanf("%c", &c);

        // evaluates to 1 if variable c is a lowercase vowel
        lowercase_vowel = (c == 'a' || c == 'e' || c == 'i' || c == 'o' || c == 'u');

        // evaluates to 1 if variable c is a uppercase vowel
        uppercase_vowel = (c == 'A' || c == 'E' || c == 'I' || c == 'O' || c == 'U');

        // evaluates to 1 (true) if c is a vowel
        if (lowercase_vowel || uppercase_vowel)
            printf("%c is a vowel.", c);
        else
            printf("%c is a consonant.", c);
        return 0;
    }

### C Program to find Sum of Natural Numbers

    #include <stdio.h>
    int main() {
        int n, i, sum = 0;

        printf("Enter a positive integer: ");
        scanf("%d", &n);

        for (i = 1; i <= n; ++i) {
            sum += i;
        }

        printf("Sum = %d", sum);
        return 0;
    }

### C program to find LCM of two numbers

    #include <stdio.h>
    int main() {
        int n1, n2, max;
        printf("Enter two positive integers: ");
        scanf("%d %d", &n1, &n2);

        // maximum number between n1 and n2 is stored in max
        max = (n1 > n2) ? n1 : n2;

        while (1) {
            if (max % n1 == 0 && max % n2 == 0) {
                printf("The LCM of %d and %d is %d.", n1, n2, max);
                break;
            }
            ++max;
        }
        return 0;
    }
    
### C program to Convert Decimal to Binary

        #include<stdio.h>    
        #include<stdlib.h>  
            int main(){  
             int a[10],n,i;    
                 system ("cls");  
        printf("Enter the number to convert: ");    
        scanf("%d",&n);    
         for(i=0;n>0;i++)    
         {    
            a[i]=n%2;    
             n=n/2;    
         }    
             printf("\nBinary of Given Number is=");    
          for(i=i-1;i>=0;i--)    
          {    
             printf("%d",a[i]);    
          }    
             return 0;  
        }  
        
 ###  C program to find Area of Equil. Triangle

#include<stdio.h>
#include<math.h>
int main()
{
	float area,a;
	printf("enter side of the triangle: ");
	scanf("%f",&a);
 
	area=(sqrt(3)/4)*a*a;
	printf("AOET:%f\n",area);
	return 0;
}

### C program to find Volume of Cylinder

int main()
{
	
	float vol,r,h;
	printf("enter radius: ");
	scanf("%f",&r);
	printf("enter height: ");
	scanf("%f",&h);
   
	vol=(22*r*r*h)/7;
	printf("VOC: %f\n",vol);
	return 0;
}

## C program to find Volume of Cube

int main()
{
	
	float side,area;
	printf("enter side of cube: ");
	scanf("%f",&side);
	
   
	area=side*side*side;
	printf("VOC: %f\n",area);
	return 0;
}

## C program to find Volume of Cone

int main()
{
	
	float radius,height,volume;
	printf("enter radius : ");
	scanf("%f",&radius);
	printf("enter height : ");
	scanf("%f",&height);
   
	volume=(22*radius*radius*height)/(3*7);
	printf("VOC: %f\n",volume);
	return 0;
}

### C Program to Remove Characters in String Except Alphabets

	#include <stdio.h>
	int main() {
	   char line[150];

	   printf("Enter a string: ");
	   fgets(line, sizeof(line), stdin); // take input


	   for (int i = 0, j; line[i] != '\0'; ++i) {

	      // enter the loop if the character is not an alphabet
	      // and not the null character
	      while (!(line[i] >= 'a' && line[i] <= 'z') && !(line[i] >= 'A' && line[i] <= 'Z') && !(line[i] == '\0')) {
		 for (j = i; line[j] != '\0'; ++j) {

		    // if jth element of line is not an alphabet,
		    // assign the value of (j+1)th element to the jth element
		    line[j] = line[j + 1];
		 }
		 line[j] = '\0';
	      }
	   }
	   printf("Output String: ");
	   puts(line);
	   return 0;
	}
	
### C Program to Store Information of a Student Using Structure

	#include <stdio.h>
	struct student {
	    char name[50];
	    int roll;
	    float marks;
	} s;

	int main() {
	    printf("Enter information:\n");
	    printf("Enter name: ");
	    fgets(s.name, sizeof(s.name), stdin);

	    printf("Enter roll number: ");
	    scanf("%d", &s.roll);
	    printf("Enter marks: ");
	    scanf("%f", &s.marks);

	    printf("Displaying Information:\n");
	    printf("Name: ");
	    printf("%s", s.name);
	    printf("Roll number: %d\n", s.roll);
	    printf("Marks: %.1f\n", s.marks);

	    return 0;
	}

### C Program to Write a Sentence to a File

	#include <stdio.h>
	#include <stdlib.h>

	int main() {
	    char sentence[1000];

	    // creating file pointer to work with files
	    FILE *fptr;

	    // opening file in writing mode
	    fptr = fopen("program.txt", "w");

	    // exiting program 
	    if (fptr == NULL) {
		printf("Error!");
		exit(1);
	    }
	    printf("Enter a sentence:\n");
	    fgets(sentence, sizeof(sentence), stdin);
	    fprintf(fptr, "%s", sentence);
	    fclose(fptr);
	    return 0;
	}
	
### C Program to read the first line from a file

	#include <stdio.h>
	#include <stdlib.h> // For exit() function
	int main() {
	    char c[1000];
	    FILE *fptr;
	    if ((fptr = fopen("program.txt", "r")) == NULL) {
		printf("Error! File cannot be opened.");
		// Program exits if the file pointer returns NULL.
		exit(1);
	    }

	    // reads text until newline is encountered
	    fscanf(fptr, "%[^\n]", c);
	    printf("Data from the file:\n%s", c);
	    fclose(fptr);

	    return 0;
	}

### C Program to Compute Quotient and Remainder

	#include <stdio.h>
	int main() {
	    int dividend, divisor, quotient, remainder;
	    printf("Enter dividend: ");
	    scanf("%d", &dividend);
	    printf("Enter divisor: ");
	    scanf("%d", &divisor);

	    // Computes quotient
	    quotient = dividend / divisor;

	    // Computes remainder
	    remainder = dividend % divisor;

	    printf("Quotient = %d\n", quotient);
	    printf("Remainder = %d", remainder);
	    return 0;
	}

### C Program to copy the contents of one file to another and also print the no. of lines in the first file.

    #include <stdio.h>
    int copyContents(char *, char *);
    void printContents(char *);
    void main(int argc, char *argv[])
    {
        int lines;
        if (argc < 3)
        {
            printf("Too few arguments provided!\n");
        }
        else if (argc > 3)
        {
            printf("Too many arguments provided!\n");
        }
        else
        {
            lines = copyContents(argv[1], argv[2]);
            if (lines == -1)
            {
                printf("An error occoured!\n");
            }
            else
            {
                printf("There are %d lines in \'%s\' file.\n", lines, argv[1]);
                printf("Contents of file 2: \n");
                printContents(argv[2]);
            }
        }
    }
    int copyContents(char *file1, char *file2)
    {
        FILE *src, *dest;
        char ch;
        int lines_count = 0;
        src = fopen(file1, "r");
        if (src == NULL)
        {
            printf("There was a problem while opening \'%s\' file.\n", file1);
            return -1;
        }
        dest = fopen(file2, "w");
        if (dest == NULL)
        {
            printf("There was a problem while opening \'%s\' file.\n", file2);
            return -1;
        }
        while ((ch = getc(src)) != EOF)
        {
            if (ch == '\n')
            {
                lines_count++;
            }
            putc(ch, dest);
        }
        if (!feof(src))
        {
            perror("\nError: ");
            return 
            -1;
        }
        fclose(src);
        fclose(dest);

        return lines_count + 1;
    }

    void printContents(char *filename)
    {
        FILE *fp;
        char ch;
        fp = fopen(filename, "r");
        if (fp == NULL)
        {
            printf("\'%s\' file not found!\n", filename);
        }
        else
        {
            while ((ch = getc(fp)) != EOF)
            {
                printf("%c", ch);
            }
            if (feof(fp))
            {
                printf("\nEnd of \'%s\' file.\n", filename);
            }
            else
            {
                perror("\nError: ");
            }
            fclose(fp);
        }
    }

### C Program to find a word in file and print number of occurances.

    #include <stdio.h>
    #include <string.h>
    int searchWordInFile(char *, char *, int);
    int wordsInFile(char *, char *);
    void main()
    {
        char filename[20], word[20];
        int index, n;
        printf("Enter filename: ");
        scanf("%[^\n]s", filename);
        printf("Enter word to search: ");
        scanf("%s", word);
        index = searchWordInFile(filename, word, 0);
        if (index == -2)
        {
            printf("Unable to open the file\n");
        }
        else if (index == -1)
        {
            printf("Word not found!\n");
        }
        else
        {
            printf("Word found at index %d\n", index);
            n = wordsInFile(filename, word);
            printf("%s occours %d times\n", word, n);
        }
    }
    int searchWordInFile(char *filename, char *word, int startPos)
    {
        FILE *fptr;
        char fileWord[20];
        int fi, i, index = -1, storedIndex;
        fptr = fopen(filename, "r");
        if (!fptr)
        {
            return -2;
        }
        else
        {
            fseek(fptr, startPos, SEEK_SET);
            while (!feof(fptr) && index == -1)
            {
                storedIndex = ftell(fptr);
                fscanf(fptr, "%s", fileWord);
                if (strcmp(fileWord, word) == 0)
                {
                    index = storedIndex;
                }
            }
            fclose(fptr);
        }
        return (index > 0 ? index + 1 : index);
    }
    int wordsInFile(char *filename, char *word)
    {
        int n = 0, index;
        int len = strlen(word);
        index = searchWordInFile(filename, word, 0);
        while (index != -1)
        {
            ++n;
            index = searchWordInFile(filename, word, index + len - 1);
        }
        return n;
    }

### C Program to count number of characters, spaces, tabs & newlines in a file.

    #include <stdio.h>
    void readContents(char *);
    void main()
    {
        readContents("input6.txt");
    }
    void readContents(char *filename)
    {
        FILE *fp = fopen(filename, "r");
        char line[100];
        int i, characters = 0, spaces = 0, tabs = 0, newlines = 0, words = 0;
        if (!fp)
        {
            printf("Cannot open the file \'%s\'\n", filename);
        }
        else
        {
            while (!feof(fp))
            {
                fgets(line, 100, fp);
                i = 0;
                while (line[i] != '\0')
                {
                    ++characters;
                    if (line[i] == '\t')
                    {
                        ++tabs;
                        if (line[i + 1] != ' ' && line[i + 1] != '\n' && line[i + 1] != '\t')
                            ++words;
                    }
                    else if (line[i] == '\n')
                    {
                        ++newlines;
                        if (line[i + 1] != ' ' && line[i + 1] != '\n' && line[i + 1] != '\t')
                            ++words;
                    }
                    else if (line[i] == ' ')
                    {
                        ++spaces;
                        if (line[i + 1] != ' ' && line[i + 1] != '\n' && line[i + 1] != '\t')
                            ++words;
                    }
                    ++i;
                }
            }
            printf("There are %d characters, %d spaces, %d tabs, %d newlines & %d words.\n", characters,
                spaces, tabs, newlines, words + 1);
        }
    }


### C Program to remove all occurances of a specific word from a file.

    #include <stdio.h>
    #include <string.h>
    #define TEMP_FILE "temp7"

    void removeStringFromFile(char *, char *);
    void readContents(char *);

    void main()
    {
        char filename[20], str[10];

        printf("Enter name of the file with data: ");
        scanf("%s", filename);
        printf("Enter string to remove: ");
        scanf("%s", str);

        removeStringFromFile(filename, str);
        printf("Contents of file after removing the string\n");
        readContents(filename);
    }

    void removeStringFromFile(char *filename, char *str)
    {
        FILE *fp = fopen(filename, "r");
        FILE *fp2 = fopen(TEMP_FILE, "w");
        int i, savepoint, length;
        char ch;
        if (!fp)
        {
            printf("Cannot open file \'%s\'\n", filename);
        }
        else
        {
            length = strlen(str);
            while ((ch = getc(fp)) != EOF)
            {
                savepoint = ftell(fp);
                i = 0;
                while(str[i] != '\0') {
                    if(ch != str[i]) {
                        break;
                    }
                    ch = getc(fp);
                    i++;
                }
                
                if (i != length)
                {
                    fseek(fp, savepoint - 1, SEEK_SET);
                    ch = getc(fp);
                }
                putc(ch, fp2);
            }
        fclose(fp);
        fclose(fp2);
        remove(filename);
        rename(TEMP_FILE, filename);
        }
    }

    void readContents(char *filename)
    {
        char ch;
        FILE *fp = fopen(filename, "r");
        while ((ch = getc(fp)) != EOF)
        {
            printf("%c", ch);
        }
        fclose(fp);
    }


### C Program to remove all comment from a C File.

    #include <stdio.h>
    #include <string.h>
    #include <stdlib.h>
    #define TEMP_FILE "temp9"

    void readContents(char *);
    void removeComments(char *);

    void main()
    {
        char filename[20];

        printf("Enter the name of C file: ");
        scanf("%s", filename);
        printf("Before removing comments\n\n");
        readContents(filename);
        removeComments(filename);
        printf("\n\nAfter removing comments\n\n");
        readContents(filename);
    }

    void removeComments(char *filename)
    {
        FILE *fp = fopen(filename, "r");
        FILE *fp2 = fopen(TEMP_FILE, "w");
        char ch;
        if (!fp)
        {
            printf("Cannot open the file \'%s\'\n", filename);
        }
        else
        {
            while ((ch = getc(fp)) != EOF)
            {
                if (ch == '/')
                {
                    ch = getc(fp);
                    if (ch == '/')
                    {
                        while((ch = getc(fp)) != EOF && ch != '\n') {}
                    }
                    
                    if (ch == '*')
                    {
                        while ((ch = getc(fp)) != EOF)
                        {
                            if (ch == '*')
                            {
                                ch = getc(fp);
                                if (ch == '/')
                                {
                                    ch = getc(fp);
                                    break;
                                }
                            }
                        }
                    }
                }
                putc(ch, fp2);
            }
            fclose(fp);
            fclose(fp2);
            remove(filename);
            rename(TEMP_FILE, filename);
        }
    }

    void readContents(char *filename)
    {
        char ch;
        FILE *fp = fopen(filename, "r");
        while ((ch = getc(fp)) != EOF)
        {
            printf("%c", ch);
        }
        fclose(fp);
    }

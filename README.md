***
# C Language Interview Questions and Answer


***
### This interview questions for C language is in it's infantile stage and any contribution is welcome!
<br>:school::blue_book::book:Do not expect advanced content here since I am doing this while I am learning it!!!


***
## 1. What does `#include<stdio.h>` represent in c lan?

Answer: It is a statment which tells the compiler to insert the contents of `stdio(standard input out put)` at the particular place. This is a pre-processor directive. It is not part of our program, it is an instruction to the compiler to make it do something.
It is the pre-processor that is part of the compiler which actually gets your program from the file.
It tells the compiler to inlcude the contents of a file, in this case the system file `stdio.h`.

***
## 2. `< >` means in `<stdio.h>`?

Answer: The compiler knows it's a system file and therefor must be looked for in a special place, by the fact that the name is enclosed in `< >`.

***
## 3. `stdio` means?

Answer: It stands for standard input output because
               <br> :white_check_mark:`printf()` is a Standard Output function.
               <br> :white_check_mark:`scanf()` is a Standard Input function.
       In short, if we want to use `printf()` in a programme then , we need to include `stdio` header file.
***
## 4. If I want to use `getch()`, `clrscr()` etc.. what do I need to include in the header file?

Answer: We need to include `conio` in a header file and similarly if we are using square root function `sqrt()` we need to include `math` in a header file. 

***
## 5. Write a function in C language to generate a prime numbers below 100?

Answer:

```

#include <stdio.h>
#include <stdlib.h>

main(){
  int this_number, divisor, not_prime;
  
  this_number = 3;
  
  while(this_number < 100){
    divisor = this_number / 2;
    not_prime = 0;
    while(divisor > 1) {
      if(this_number % divisor == 0) {
              not_prime = 1;
              divisor = 0;
      }
      else
              divisor = divisor-1;
    }
    
    if(not_prime == 0)
            printf("%d is a prime number\n", this_number);
            this_number = this_number + 1;
  }
  exit(EXIT_SUCCESS);
}
```

```
Answer:
3 is a prime number
5 is a prime number
7 is a prime number
11 is a prime number
13 is a prime number
17 is a prime number
19 is a prime number
23 is a prime number
29 is a prime number
31 is a prime number
37 is a prime number
41 is a prime number
43 is a prime number
47 is a prime number
53 is a prime number
59 is a prime number
61 is a prime number
67 is a prime number
71 is a prime number
73 is a prime number
79 is a prime number
83 is a prime number
89 is a prime number
97 is a prime number
```
***
## 6.  write a program that prints prime pairs — a pair of prime numbers that differ by 2, for example 11 and 13, 29 and 31?

Answer:
```
#include <stdio.h>
#include <stdlib.h>

main(){
   int this_number, divisor, not_prime;
   int last_prime;

   this_number = 3;
   last_prime = 3;

   printf("1, 3 is a prime pair\n");

   while(this_number < 100){
      divisor = this_number / 2;
      not_prime = 0;
      while(divisor > 1){
         if(this_number % divisor == 0){
            not_prime = 1;
            divisor = 0;
         }
         else
            divisor = divisor-1;
      }

      if(not_prime == 0){
         if(this_number == last_prime+2)
            printf("%d, %d is a prime pair\n",
               last_prime, this_number);
         last_prime = this_number;
      }
      this_number = this_number + 1;
   }
   exit(EXIT_SUCCESS);
}
```
```
1, 3 is a prime pair
3, 5 is a prime pair
5, 7 is a prime pair
11, 13 is a prime pair
17, 19 is a prime pair
29, 31 is a prime pair
41, 43 is a prime pair
59, 61 is a prime pair
71, 73 is a prime pair
   
 ```
***
## 7. How to add comment in C language?

Answer: We can add comment by using /*..........*/ in C language.

***
## 8. Write variable naming rules?

Answer:
- name can be any combination of upper and lower case letters(a-z, A-Z), digits(0-9), and the character _ No other characters can be used in a variable name.
- name must start with a letter
- blanks are not allowed
- Upper and lower case are allowed e.g. NUMBER , Number, number, nuMBER are all different.
- should be descriptive (name need to describe the the information that the variable holds)
- no restriction on the length of variables but make it short and precise
- names cannot be reserved words e.g float, this,...

          acceptable e.g. a, b, c, C, SUM, sum, Count, value, Number, x_dot, Salary, Value1, dhgfhL
          not acceptable e.g. 1ab
                                             inte rest
                                             Ca$h
                                             Amount-of-loan (- not allowed)
                                             int (reserved word)
***
## 9. OR is a binary operator and is denoted bu the symbol ||, which is two adjacent pipe symbols. What does `(x || y)` mean?

Answer: The possible output for `(x || Y)` is gonna be true or y is true or both are true.

***
## 10. Why is termination an important characteristic of an algorithm?

Answer:

If we started following an algorithm that did not terminate, we would never finish executing it!

***
## 11. Why is clarity an important characteristic of an algorithm?

Answer:

While executing a step, we should know exactly what must be done. If we did not, then there would be no single specific outcome for a particular step. Another good reason is that algorithms are usually translated into computer programs, and computer programs do not leave room for ambiguity.
***
## 12. Give one example of a variable of each of the following data types:

integers
floating numbers
characters
Booleans
Answer:
These answers are representative of each of the data types.

integers: number of windows in a room, number of words in a memory, or the rounded-off value of the temperature (negative numbers are integers too), and so on
floating numbers: the cost of an item in a store, the precise temperature, and so on
characters: the four directions specified by 'N', 'S', 'E', or 'W', one's letter grade in a class, or gender ('F' or 'M')
Booleans: the answer to the questions, "Are you female?" or "Do you wish to contribute to the XYZ fund?"

***
## 13. Evaluate the results of the following expressions, given the following values for these variables:

      x = true, y = true, z = false

      x && y || z
      !x && y || z
  ```    
  Answer:
  a. true. This expression is interpreted as
(x && y) || z

(true && true) || false

(true) || false

true
```
```
b. false. This expression is interpreted as
((!x) && y) || z

((!true) && true) || false

(false && true) || false

false || false

false
```
***
## 14. Evaluate the results of the following expressions, given the following initial values:
```
     x = 23, y = –10, z = 12

A. x % z
B. x + y*z
C. x/y*z
D. z % z
```
Answer: 
```
A. 11

x % z
23 % 12
23/12 = 1 with a remainder of 11
```
```
B. –97 

The expression is interpreted as

x + (y * z)
23 + (–10 x 12)
23 + (–120)
–97
```
C. –27.6

x / y * z
23/–10 x 12       (remember that / and * are left associative)
–2.3 x 12
–27.6
```
D. 0
z % z
12 % 12
12/12 = 1 with a remainder of 0
```
***
## 15. Starting with the following initial values, specify the value of each variable at the end of each step, in the following pseudocode.
```
x = 10, y = 20, z = 30
Set x = x + 20 
Set y = y * x 
Set y = y % z + x 
Set z = z – 20 
Set z = z ^ 3 ^ 2
```
	Answer:
  
 ![answer](https://user-images.githubusercontent.com/23619819/29866063-395e19ac-8d45-11e7-912b-59312339a18b.JPG)

***
## 16. Determine the total number of bits in a memory whose size is specified as 100MB X 32.

Answer

Remember that "B" stands for "byte" (8 bits). So,

100 MB = 100 * 220 * 8 bits 
              = 100 * 1,048,576 * 8 bits

Thus the 100 MB X 32 memory will contain 100 * 1,048,576 * 8 * 32 or 26,843,545,600 bits.
***
## 17. When a variable has just been declared, what initial value does it contain?

Answer:

No proper initial value exists. Using an uninitialized variable will invariably lead to run-time errors.
***
## 18. What is the difference between: (a) x == y and (b) x = y?

Answer:

The first, x == y, is a Boolean expression whose answer is always either true or false, whereas the second, x = y, is an assignment statement.
***
## 19. What is the difference between an expression and a statement?

Answer:

A statement is the basic unit of execution in a program.

Expressions are usually parts of statements. An expression is something that evaluates to a single valu


	
	int num1, num2, sum;
	sum = num1 + num2;
	
	printf("\nEnter two number : ");
	
	scanf("%d %d", num1,num2);
	
	sum = num1 + num2;
	printf("Sum : " sum);
	
	return(o)
	
}


***
## 21. Write a C program to find area and circumference of a circle?

Answer:
```
#include<stdio.h>

int main() {

	int rad;
	float PI = 3.14, area, ci;
	
	printf("\nEnter your radius : ");
	scanf("%d", &rad);
	
	area = PI * rad * rad;
	printf("\nArea of the circle is : %f ", area);
	
	ci = 2 * PI * rad;
	printf("\nCircumference : %f ", ci);
	return 0;
}
```

***
## 22. Create a program that can add up the number of coins(penny, nickle, dime, quarter);
Answer:

 #include<stdio.h>
   int main() {
    /*variable defination*/
    int penny, nickle, dime, quarter;
    float coinTotal;
    /*prompt for input*/
    printf("\nEnter the number of penny : ");
    scanf("%d", &penny);
    printf("\nEnter the number of nickle you have : ");
    scanf("%d", &nickle);
    printf("\nEnter the number of dime you have : ");
    scanf("%d", &dime);
    printf("\nEnter the number of quarter you have : ");
    scanf("%d", &quarter);
    /*formula to add coin*/
    coinTotal = (penny * 0.01) + (nickle * 0.50) + (dime * 0.10) + (quarter * 0.25);
    /*print out the total*/
    printf("\nThe total coint you entered is : %f", coinTotal);
    return 0;
  }

<img width="737" alt="screen shot 2017-09-06 at 8 44 21 pm" src="https://user-images.githubusercontent.com/23619819/30140685-5212536e-9344-11e7-9fbb-eed94392889e.png">

## 22. Calculate the perimeter of the triangle? And explain your program in detail? 

Answer: 
I have written, the C code for calculating the perimeter of the triangle as follow. I have used float point to inter the sides of the triangle and the base. The perimeter will be a float number.

![image](https://user-images.githubusercontent.com/23619819/30174977-ea483280-93ca-11e7-821e-3c077929d1a7.png)


***
## 23. What is this line of code doing? scanf(“%f”, &height);

Answer:The scanf get value from stdin and put in variables named. This line of code is where we can input the height from the user. The letter f stands for inputting a float number and if we want to input integers we can simply change it to %d.

***
## 23. Write a program to calculate the gross salary of a person?

Answer:
```
#include<stdio.h>
int main() {
	int gross_salary, basic, da, ta;
	
	printf("Enter basic salary : ");
	scanf("%d", &basic);
	
	da = (10 * basic) / 100;
	ta = (12 * basic) /100;
	
	gross_salary = basic + da + ta;
	
	printf("\nGross salary : %d", gross_salary);
	return 0;
}
```
***
## 24. Using C program add two numbers, namely num1 and num2 to print out the result?
Answer:

<img width="523" alt="screen shot 2017-09-10 at 8 34 26 pm" src="https://user-images.githubusercontent.com/23619819/3                    
***
## Create a C program to Enter a number to see if it is an even or odd number?
Answer:
```
#include <stdio.h>
int main () {
        int num;
        printf("\nEnter a number to see if it is even or odd number? : ");
        
        scanf("%d", &num);
        
        if(num %2 == 0)
          printf("%d is an even number.", num);
          
       else printf("%d is an odd number.", num);
        
        return (0);
}
```
***
## 25. Write a C code to add 10 numbers and if the vlaue greater than 100 say it's greater than 100.

Answer:
```
/*The following is the C Code that will compile in execute in the online compilers.*/
/* C code
 This program will calculate the sum of 10 integers.
 Developer: Mohammed Kemal
 Date: Sep 14, 2017 */
#include <stdio.h>
int main () {
    /* variable definition: */
      int value1,value2,value3,value4,value5,value6, value7,value8, value9,value10, sum;
      /* Initialize sum */
      sum = 0;
      printf("Enter an Integer for value1\n");
      scanf("%d", &value1);
      printf("Enter an Integer for value2\n");
      scanf("%d", &value2);
      printf("Enter an Integer for value3\n");
      scanf("%d", &value3);
      printf("Enter an Integer for value4\n");
      scanf("%d", &value4);
      printf("Enter an Integer for value5\n");
      scanf("%d", &value5);
      printf("Enter an Integer for value6\n");
      scanf("%d", &value6);
      printf("Enter an Integer for value7\n");
      scanf("%d", &value7);
      printf("Enter an Integer for value8\n");
      scanf("%d", &value8);
      printf("Enter an Integer for value9\n");
      scanf("%d", &value9);
      printf("Enter an Integer for value10\n");
      scanf("%d", &value10);
      sum = value1 + value2 + value3 + value4 + value5 + value6 + value7 + value8 + value9 + value10;
      printf("Sum is %d\n " , sum );
      
      if (sum >100)
            printf("Sum is over 100\n");
  return 0;
}

```
***
## 26. Create a program to determin wheter you can drive or not by entering your age??

Solution:
```
// C code
// This program will ask your age and determin to drive nor not.
// Developer: Mohammed Kemal
// Date: Sep 24, 2017
#include <stdio.h>
int main(){
        //declaring variable
        int age;
        //prompt the user to enter age
        printf("\nEnter your age to determin whether you can drive or not?");
        while (scanf("%d", &age) !=EOF) {
        // when the age below the cut point let them know they are to Young  
          if( age  < 16 && age > 0) 
          {
            printf("\nToo Young To Drive Car!");
        // Otherwise let them know too old to drive or too young
          }
          else if( age > 80)
          {
            printf("\nToo old to drive car!");
          }
          else if (age < 0 )
          {
            printf("\nYou need to enter positive number!");
          }
          else
          {
            printf("\nYou can drive!");
          }
            printf("Enter another age, or CTRL Z to exit.\n\n");
      } 
    return 0;
}
```

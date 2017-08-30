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



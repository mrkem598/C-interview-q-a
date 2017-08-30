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

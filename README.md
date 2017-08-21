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

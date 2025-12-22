# What is the C Compilation Process?
The C compilation process is the series of steps by which a C program written by a programmer is converted into a machine-executable program that the computer can understand and run.
- Computers understand machine language (0s and 1s), not C language.
- So, the C program must pass through several stages before execution.

## Steps breakdown->
1) Preprocessing
2) Compilation
3) Assembly
4) Linking

### Step1 -> Preprocessing 
The preprocessor prepares the code before actual compilation.
It mainly does 4 things-
- Comments
- ```
  //this a comment
  ```
  remove completely

- Expand macros
```c
#define PI 3.14
 ```
this will replace PI with 3.14 everywhere.

- Include header files
```c
#include <stdio.h>
```
copies contents of <stdio.h> into the program.

- Conditional compilation
```c
#ifdef DEBUG
```
- decides which code to include or exclude.

  ### Basically Preprocessor is like cleaning and organizing ingredients before cooking.

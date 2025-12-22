# What is the C Compilation Process?
The C compilation process is the series of steps by which a C program written by a programmer is converted into a machine-executable program that the computer can understand and run.
- Computers understand machine language (0s and 1s), not C language.
- So, the C program must pass through several stages before execution.

### Steps breakdown->
1) Preprocessing
2) Compilation
3) Assembly
4) Linking

## Step 1 -> Preprocessing 
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

  ### In Simple Words- Preprocessor is like cleaning and organizing ingredients before cooking.

  ## Step 2 -> Compilation
  The Compiler checks -
  - Syntax error
  - Grammar of C
  - convert it into Assembly Language.

#### Important point:
- No machine code yet.
- Only conversion to assembly language.

### In Simple Words- Compiler is like translating English into another language(assembly).

## Step 3 -> Assembly 
The Assembler convert Converts assembly language into machine code (0s and 1s) and Generates an object file.
- obj file contains Machine code But it is not complete,some functions (like printf) may be missing.
#### printf() is missing here because <stdio.h> only declare printf() but the actual implementation of printf is stored in library files and these library files are not added yet at the assembly stage.

### In Simple Words- The assembler converts the program into machine language so the computer can understand and execute it.

## Step 4 -> Linker
- Combines object files with library functions
- Resolves external references - External references are functions or variables that are used in your program but are not written by you in the same file.
```c
printf("Hello");
```
- Here we are using printf
- But we did not write printf
- It already exists in a library.
- #### So printf() is a external reference.
### In Simple Words- The linker joins all parts of the program and library functions to make the final runnable program.


## So This is the whole Summary of how compilation is done in C programming.

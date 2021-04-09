# Compilers-I
## Mini Assignment-1: Compilers and their Options  

### Name: R. Gokul Kannan					              
### Roll No.: CS19BTECH11048

### 1) Write a short note on various options in common compilers: GCC and LLVM.  
Options in GCC: (Here the programs that have to be compiled are taken to be main.c)  
*	The most basic form: gcc main.c  
  This one is just to compile the program main.c and produce an executable file a.out in case of a successful compilation. Or print out the error messages.  
*	gcc main.c –o main  
  This one is to compile the program main.c and produce an executable file in the name we want, in this case main, in case of successful compilation. Or print out the error messages.  
*	gcc –Wall main.c –o main  
  This one is to compile the program main.c and produce an executable file main, while displaying all warnings which may be ignored when –Wall is not mentioned like, uninitialized variables, etc. Executable file main is created only in case of successful compilation or else, error messages are displayed.  
*	gcc –E main.c  
  This one will print the pre-processor output to the terminal upon successful compilation, but compilation stops at the pre-processor state and no output file is produced.  
*	gcc –E main.c>main.i  
  This will do the same thing as (d) but will print the pre-processor output to the file named main.i.  
*	gcc –S main.c and gcc –S main.c>main1.s  
  First one will create an assembly level output and print it to the file main.s and the second one will print to the file main1.s(custom name). This happens only upon successful compilation.  
*	gcc –C main.c  
  This will produce only the compiled code, without any linking. This command will produce the file main.o which will contain the compiled code (machine level code).  
*	gcc –save-temps main.c  
  This will save all the intermediary files, main.i, main.o, main.s and also the executable file a upon successful compilation.  
*	gcc main.c –o main –lfile  
  This command is used to link the code main.c to the shared library file.so to produce the final executable file main.    
*	There are also other options like gcc –help, gcc –version to give information regarding the gcc installed in the system.    
Options in LLVM:  
* The most basic form: clang main.c  
  This one is just to compile the program main.c and produce an executable file a.out in case of successful compilation. Or print the error messages in case of an unsuccessful compilation.  
 * clang main.c -fsyntax-only  
  This one is just to check whether the program main.c is correct or not.  
 * clang main.c -S -emit-llvm -o    
  This one is to print the unoptimized LLVM code.  
 * clang main.c -S -O3 -o  
  This one is to print the native machine code as output.  
 * There are also clang --version, --help, etc. to get help, version number, etc.  
 * There are preprocessor flags like, -C to include comments, -H to show header includes and nesting depths, etc.  
 * There are diagnosit flags like, -R<remark> to enable the specified remark, etc.  
 
 ### 2) Write a note on the various frontends that these compilers support.  
   The main front ends supported by GCC are, C (by gcc), C++ (by g++), Objective C, Fortran, Ada (by GNAT), Go and D. There are also many more front ends supported by GCC, but have not yet been integrated into the main distribution of GCC.  
   The front ends supported by LLVM include Ada, C, C++, D, Delphi, Fortran, Haskell, Julia, Objective C, Rust, Swift, etc.  
   
 ### 3) Use these compilers to generate code for various architectures using its various backends and report your findings.  
  * Clang is faster and uses lesser memory than GCC for compiling the same code.  
  * GCC supports more architectures than LLVM and also has more front end supports.  
  * But GCC is more advantageous than LLVM in performance optimizations.  

 ### 4) Compilers come with various optimization levels: Focusing on options O0, O1, O2, O3  as well as -Os, -Oz, run various codes using these predetermined passes and report your findings.  
 For GCC, LLVM,   
 O0- No optimizations.  
 O1- Resulting executables are smaller and faster than those in O0.  
 O2- Further optimization for O1, this includes instructions scheduling. It provides the maximum optimizations while keeping the executable file size as low as O0.  
 O3- This can increase the size of executable file in order to speed up the execution. But in some cases, its not advisable to use this optimization.
 Os- This is to produce the smallest possible executable file. This is generally used for systems that have limited memory.  
 Oz- Further tries to reduce the size of executable file. 
 
 **Link of .md file in GitHub: ** <>

# Compilers-I
## Mini Assignment-1: Compilers and their Options
Name: R. Gokul Kannan					      Roll No.: CS19BTECH11048

1) Write a short note on various options in common compilers: GCC and LLVM.
Options in GCC: (Here the programs that have to be compiled are taken to be main.c)
a)	The most basic form: gcc main.c
This one is just to compile the program main.c and produce an executable file a.out in case of a successful compilation. Or print out the error messages.
b)	gcc main.c –o main
This one is to compile the program main.c and produce an executable file in the name we want, in this case main, in case of successful compilation. Or print out the error messages.
c)	gcc –Wall main.c –o main
This one is to compile the program main.c and produce an executable file main, while displaying all warnings which may be ignored when –Wall is not mentioned like, uninitialized variables, etc. Executable file main is created only in case of successful compilation or else, error messages are displayed.
d)	gcc –E main.c
This one will print the pre-processor output to the terminal upon successful compilation, but compilation stops at the pre-processor state and no output file is produced.
e)	gcc –E main.c>main.i
This will do the same thing as (d) but will print the pre-processor output to the file named main.i.
f)	gcc –S main.c and gcc –S main.c>main1.s
First one will create an assembly level output and print it to the file main.s and the second one will print to the file main1.s(custom name). This happens only upon successful compilation.
g)	gcc –C main.c
This will produce only the compiled code, without any linking. This command will produce the file main.o which will contain the compiled code (machine level code).
h)	gcc –save-temps main.c
This will save all the intermediary files, main.i, main.o, main.s and also the executable file a upon successful compilation.
i)	gcc main.c –o main –lfile
This command is used to link the code main.c to the shared library file.so to produce the final executable file main.
j)	There are also other options like gcc –help, gcc –version to give information regarding the gcc installed in the system.

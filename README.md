
# TI84 Program Library

In this repository, you may find programs and code that can be built in the TI84 calculator via the language of TI-BASIC. 


For clarification, the "code" may use **//** as comments and aren’t part of the actual code  (Although comments do not actually exist in TI-BASIC)



---
## Quick guide of the TI84 language (TI-BASIC): 
To create a program: **PRGM -> NEW**\
To edit a program: **PRGM -> EDIT**\
To execute a program: **PRGM  -> EXEC**

The line of code \
**Prompt X** \
Gets an input and stores it into variable X, variable X will be initialized automatically and does not require prior initialization

The keyword\
**Disp**\
Prints out a value (printing means displaying something)


The code segment

**Prompt Y\
Disp Y*2**

Receives a value from the user, stores it into Y, and prints out the double of inputted value


\
The keyword\
**If**\
Supports a conditional statement and runs a code block if that condition is true

The keyword\
**End**\
Ends a code block, if you are familiar with programming, you may know that you would usually use indentation or curly braces {} to define a block, but in TI-BASIC (and many other languages) you have to use **End**

The code segment

**Prompt X\
Prompt Y\
If X = Y\
Then\
Disp “They are the same”\
End**

Receives two values, X and Y, and if X is equal to Y, it prints out “They are the same”, notice how I used quotes “ “ to create a string

Also notice how **Then** is used immediately after the **If** statement


\
The keyword\
**While**\
Creates a **while loop** and the keyword\
**Repeat**\
Creates a loop that repeats until a condition becomes true\
**For**\
Creates a **for loop**

**While loops** and **repeat loops** are structured exactly like if statements,
except the **while loop** runs indefinitely until the condition is false,
and the **repeat loop** does so until the condition becomes true.

The code segment

**For(X,0,5,1)\
Disp X\
END**


Iterates (goes through) numbers from 0-5

This is because we first initialize X (the first parameter) as 0 (the second parameter), and as long as X is at most 5 (the third parameter) it runs the code block and X increments by exactly 1 (the fourth parameter).

The keyword\
**Stop**\
Halts the program (it is not needed at the end of the program, as it automatically halts)\
**Pause**\
Pauses the program until the user presses enter, letting the user check things like variables and debug\

The keyword\
**Lbl**\
Creates a label that the program can be sent to (Labels can be 1-2 alphanumeric characters)\
**Goto**\
Causes the program to go to a specified label\

The code segment\
**Prompt P\
If P=265382945\
Then\
Goto 5X\
End\
Disp "FREEZE, WRONG PASSWORD"\
Stop\
Lbl 5X\
Disp "CORRECT PASSWORD"**

Will ask for a password, and will alert whether the password is correct.

Note how Stop is used after saying the wrong password. If it wasn’t used, the program could continue and state your bank account information.

These can be used for advanced loop breaks with checks, or in menus:

The function\
**Menu**\
Can be used to create a set of options for the user, with a menu name and up to 10 options\
It utilizes **Lbl** to send the program to a specified point based off of a user choice\
Example:\
**Menu("THE MENU NAME", "*MATH*", M, "*BYE BYE*", Z)**

This program gives 2 choices:\
*Math*, which will send the program to a **Lbl M**, which should be later defined in the code\
*Bye Bye*, which will send the program to a **Lbl Z**, which should also be later defined in the code\
The Stop keyword should be used between labels to have only one choice, unless you want a program to continue through labels.

The keyword\
**prgm**\
will run another program within the program.

Example:\
**Helper Program B:\
B->A*A**

**Main Program A:\
Prompt A\
prgmB\
Disp B**

In this example B will be written as A\*A, but I wrote the code to change B in Program B. Program B could then be used in multiple programs, making it easier to find A\*A. Menus can use programs within them to have you choose which program to run\
Note that programs with prompts would prompt, even if they are helpers in other programs\
Also note that the Stop keyword would halt the whole program, even if written in a helper program

The keyword\
**ClrHome**\
Clears the calculator screen and resets the cursor to (1,1). It is mainly used for graphics, and should normally not be included in Math or tools where the user might need to check other formulas they input.\
Also, ChatGPT commonly puts ClrHome in things, so programs with ClrHome are more likely to be AI generated than those without.

## Importing Code
If you have a Calculator with the name CE (for example TI-84 Plus CE), you can connect it to a computer and import programs, apps, and variables. Programs come in `.8xp` files.

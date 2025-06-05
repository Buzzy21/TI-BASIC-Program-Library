
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
**For**\
Creates a **for loop**

**While loops** structured exactly like if statements, except the 
while loop runs indefinitely until the condition becomes false

The code segment

**For(X,0,5,1)\
Disp X\
END**


Iterates (goes through) numbers from 0-5

This is because we first initialize X (the first parameter) as 0 (the second parameter), and as long as X is at most 5 (the third parameter) it runs the code block and X increments by exactly 1 (the fourth parameter).

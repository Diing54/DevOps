
2025-02-15 15:14

Level : #baby

Tags :

# Bash Scripting

# Intro
A bash script is a file containing lines of code either simple commands or complex ones that can either navigate directories or create other stuff ; in simple words they can do a series of actions. Basically they can run bash commands eg ls , mkdir, ps, grep ,touch ,rm etc. A bash script can be executed and the lines of code inside it will be run line by line.


# Advantages of bash scripting 
1. Automation - Shell scripts allow a user to automate repetitive tasks hence saving on time and minimizing the risk of human error
2. Portability -  Can run on various OS including windows through VM's
3. HIghly flexible as they can be customized easily
4. Easy to write as they require any special software
5. Integration - Shell scripts can be integrated with other tools and applications and cloud services allowing for more complex automation and system management tasks
6. Debugging - They are easy to debug and most of them have built-in debugging and error-reporting tools
- NOTE : Shell is a program responsible for displaying of an interface for interacting the OS(CLI- Command Line Interface). Bash is a type of shell
## Creating and executing bash scripts
- Bash scripts end with .sh
- A bash script starts with a shebang. This is the first line which must be present in a script which specifies the interpreter that will be used when executing the script. This allows users to leverage the power of different interpreters. Shebang tells the shell to execute it via bash shell
- When saving a script file, its is good practice to place commonly used scripts in the ~/bin/ directory
- The script files also need to have the execute permission to allow them to run
- An example of a shebang statement (#!/bin/bash)
- ![image](https://github.com/user-attachments/assets/9569a3c0-9d0a-4b2a-9eb8-dcd8af079d8c)





- The read command reads the input and stores it in the variable path
- The ls -al command takes the variable with the stored path and displays the details of the path
- We can then run the script using the following commands :
1. sh hello.sh
2. bash hello.sh - These commands(sh hello.sh) must be specified with the directory of the bash script if not in the bash script directory
3. ./hello.sh - ./ tells the bash to execute hello.sh in the current working directory. We can use hello.sh to execute the bash script while on any directory of the terminal if the path of the script file is added to the $PATH variable
## Variables and data types 
- Variables store data which can be read, accessed and manipulated eg : name=John
- $ is required to access the variable's content
- The naming conventions of a variable are :
1. Variable names should start with a letter or an underscore (`_`).
2. Variable names can contain letters, numbers, and underscores (_).
3. Variable names are case-sensitive.
4. Variable names should not contain spaces or special characters.



## References

 Bash scripting by freecodecamp (https://www.freecodecamp.org/news/bash-scripting-tutorial-linux-shell-script-and-command-line-for-beginners/)
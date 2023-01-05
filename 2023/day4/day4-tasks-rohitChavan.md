## Task 1
### Shell Scripting for DevOps
+ Shell scripting is a way to automate tasks in a Unix-based operating system, such as Linux or macOS. 
+ It involves writing a series of commands in a script file, which can then be executed all at once, rather than running each command separately.

## Task 2 
### What is #!/bin/bash
+ This is known as shebang in Unix. Shebang is a collection of characters or letters that consist of a number sign and exclamation mark, that is (#!) at the beginning of a script.
+ Unix consists of numerous shells out of that bash is one of them that is widely used. It is the default shell assigned by Linux-based operating systems. 
+ To explicitly specify the type of shell used by the script, Shebang is used. So we can use shebang, that is, #!/bin/bash at the start or top of the script to instruct our system to use bash as a default shell.
  - Can we also write *#!/bin/sh* -> Yes, you can also use “#!/bin/sh” to specify the “sh” shell as the interpreter. 

## Task 3
### Write a Shell Script which prints I will complete #90DaysOofDevOps challenge
+ This script has a single line of code, which uses the “echo” command to print a message to the terminal.

Shell Script

    #!/bin/bash
    echo "I will complete #90DaysOofDevOps challenge"

## Task 4
### Write a Shell Script to take user input, input from arguments and print the variables.

Shell Script

    #!/bin/bash

    echo "Enter your name: "
    read name

    dream=$1

    # Print the variables
    echo "Name: $name"
    echo "Your dream goal: $position"
    
## Task 5
### Write an Example of If else in Shell Scripting by comparing 2 numbers

Shell Script

    #!/bin/bash

    num1=$1
    num2=$2

    if [ $num1 -gt $num2 ]
    then
      echo "$num1 is greater than $num2"
    else
      echo "$num1 is less than or equal to $num2"
    fi
    

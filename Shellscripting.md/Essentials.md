**Shell** is responsible to take our command as an imput, interact with the OS to obtain the desired output of he user, 


**Shellscripting** has the ability to read and execute commands from a file and that's why it's very used for automating tasks. Bash is the commun shell used in Linux. Exple: l have a task to create 100 files. Instead of doing manually *touch filename - 100 times*, l can wite a script like **For 1 in (1..100); do touch newfile_$1;done
**
**for 1 in (1...100); do touch test_file_$1;done** will create 100 test_file.

## ANATOMY OF A SHELL SCRIPT
**#!/bin/bash** This top line defines the interpretor to be used bt the shell script
**#** These are comments. Comments are not executed as part of the shell script and are used for documentation within the script itself
**echo "Please enter your name "**
**read name**
**echo -e "hello $name!\n"**
     

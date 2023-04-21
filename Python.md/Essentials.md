## What is Python?

Developped in 1990, Python is a high level interpreted language that can be used by many kind of applications. 

## Initial Setup
To set up our environnement, we have 3 ways:

**Python Interpreter**
We will see how to install the python interpreter and how to connect to the python console (where you write the code). If, it's a big file we can put the code inside a file and this file will need to be read by the interpreter console.
**Steps**
**to install python** sudo dnf install python or sudo apt-get install python
**check the version** python --version
**check the directory where python dependencies are located** ls /bin/python
**To have the iteractive mode** python (>>> will appear)
**to exit the iteractive mode** ctrl+l  or exit ().  Keep in mind, when you exit, you lost your previous code. That's why is better to create a filewith the extension **.py** to store our code directly. To run the file, just use **Python filename.py**
**Give the execution permission to the file**   chmod +x filename.py

**Virtual environments and Package Management with pip**

***steps for virtuals environnements***
- sudo dnf install python3-virtualenv -y
- pwd
- python -m venv new_virt
- cd new_virt/
- source new_virt/bin/activate . The prompt changed 

***steps for pip***
- sudo dnf install python3-pip
- python --version and pip --version need to match otherwise python will be not able to communicate with the interpreter 
- pip ls

## Variables, Data types and operators



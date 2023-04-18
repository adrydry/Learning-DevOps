## What is Linux?
Linux is an operating system which enables communications between the users and the computer

## Why Linux is most used today?
- Open source
- Free
- More secure
- Many distributions
- No slow time in production
- Easy to learn


## Linux Distributions
Because Linux is an open source, it has many other flavours. Some of the most popular Linux distributions are:
- Centos;
- Debian;
- Redhat;
- Ubuntu;
- Fedora

## Mains components of Linux or Architecture of Linux
Everytime, we install Linux, we install these main components:
- **kernel**: Is the main components of Linux OS because it etablished communication between hardware and software
- **System Libraries**: it's responsible to execute tasks as change files permissions and ownership, listing directories

## Commands lines basics
 
 In a linux CLI, we have the username and the host and the current working directory represents by a title ~. The command prompt is represents by $ at the end of the script. After the command prompt, we have the command and when we run this command, the **output** will display
 
 ## How to connect from my local desktop to linux?
 ssh username@hostname / ssh username@IP of the host
 to know, the hostname just use the command **hostnamectrl**
 
 ## The root File system OF Linux
 **/** for the root directory;                   **/bin** for users binaries;    **/boot** for static boot files;    **/dev** device files;    **/etc** Configuration files;          **/home**  home directories;         **/lib** shared librairies;    **/mnt** tempory mount points;     **/opt** optional packages;   **/proc** kernel and process files;   **/root** root user home directory;    **/run**  application states files;   **/sbin** system administration binaries;    **/srv** service data;  **/tmp** temporary files;    **/user** user binaries;      **/var** variable data files
   

## Some populars commands to know as DevOps Engineer and their roles
Keep in min that Linux is case sensitive. 
If l use Ubuntu, l can run:
**lsb_release -a**: To know the version of the Ubuntu distributions
- **uname -r**: To check the version of my kernel
- **ls --version**: give the version of the GNU
- **whoami**: Who is the cloud user?
- **ls**: list the file in the directory
- **ls -a**: List all files even the hidden files
- **ls directory name**: To list all the files inside a directory
- **pwd**: To know my current directory
- **last**: Show the last person logging in the system and also the time where yhe system was rebooted
- **uptime**: To see for how long the system is running
- **clear**: To keep your screen empty
- **man (infront a command)**: Open the documentation related to a command
- **info** Provide more informations than Man command
- **tar xzf** : to unzip a file
- **htop**: give information 
- **scp filename**: to copy a file from my computer to my linux cli
- **cat /etc/*release**: to see the list of all the release file
- **cat /etc/*issue*: to see the list of all issues files
- **wc -l**: give a total of lines of a file
- **wc -L**: Give the number of characters of the longest line
- **wc -m**: give the total number of character of the file
- **$HOME**: Environnement variable used to store home directory path   

## Simple Logging

When is time to run commands, remember that we can use simple logging to go faster. For example, if l have a directory Folders with 5 file: file file1 file2 file3 file4

-**ls file?** or **ls ?????** will display all the file with 5 character long, beginning by file and ending by anything: file1 file2 file3 file4
-**ls ????** will display all the file with 4 characters: file
-**ls ????1** will display all the file with 5 characters ending by 1

## Major open sources Applications

1- Desktop Applications
- **Openoffice** and **LibreOffice**: They are open source and like Ms Office, provide applications for writer, spreadsheets,..
- **Web browser** as Firefox;
- **Gimp** as Photoshop

2- Server applications
- **Apache**: It is a very popular web application server. It allows applications to be visible on the internet
- **Nginx**: It also a web server application that can be used for reverse proxy, load balancing, mail proxy and http caching

3- Database applications
- **Mysql**: Is an open source relational database management system. Together with Linux, Apache and PHP/Python, it makes up the popular **LAMP** used to deploy web sites. My SQL is used by many database driven web applications such wordpress and many websites such as Facebook, twitter and youtube;
- **MariaDb**:it's a fork of Mysql but MariaDB claims some performance optimization and speed improvements. 

4- File Sharing applications
- **Samba**: it performs, on local network, files and print services, authentification and authorisation,...
- **NFS**: it is a distributed file protocols permitting client hosts to access files and directoriesover the network as local storage

5- Cloud applications
- **Owncloud** can be used to create our private cloud and use it as Dropbox
- **Nextcloud**: it's forked from owncloud

6- Development languages
- **Shellscripting** has the ability to read and execute commands from a file and that's why it's very used for automating tasks. Bash is the commun shell used in Linux.
- **The C Programming language**
- **Java**: run on any system;
- **Javascript**
- **Perl**
- **Python**
- **PHP**

## Package Management tools
 
 A **package** is a collection of files and dependencies needed to install an application. We have differents types of package management:
 - **Debian Package (dpkg)** : sudo dpkg -i htop deb file, run the application with htop, remove the htop package sudo dpkg --remove htop
 - **apt-get package** for ubuntu
 - **Red hat Package Manager (RPM)**: to install this package: 1- sudo rpm -i htop rpm file, 2- run htop command to run the htop application and 3- remove the htop by using sudo rpm -e htop
 - **yum package** for fedora
 
 
 
 


## Some interesting links to practise all these Linux commands 
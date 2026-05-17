Course

Hands-On Introduction to Linux Commands and Shell Scripting on Coursera

What I Learned Today

Linux Fundamentals
Introduction to Linux
Linux distributions
Linux architecture
Linux terminal overview
Browsing Linux directories with the terminal
Installing software and updates

Linux Commands
Overview of common Linux shell commands
Informational commands
Getting help for Linux commands
File and directory navigation commands
File and directory management commands
Viewing file contents
Useful commands for wrangling text files

Linux Security & Permissions
Managing file permissions and ownership
Understanding read, write, and execute permissions
Using chmod to modify file permissions
Learning about user, group, and others permissions

Networking & Compression
Brief introduction to networking
Networking commands
File archiving and compression
Working with tar, zip, and unzip

Practical Linux Commands Practiced

Directory Navigation
pwd
ls
ls -l
ls -la /etc
cd /home/project

Exploring System Directories
ls /bin
ls /bin/ls
ls /bin/b*
ls /bin/*r

Downloading Files
wget https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-LX0117EN-SkillsNetwork/labs/module%201/usdoi.txt

Checking File Details
ls -l usdoi.txt

Changing File Permissions
chmod -r usdoi.txt
chmod +r usdoi.txt
chmod o-r usdoi.txt

Archiving Files with tar
tar -cvf bin.tar /bin
tar -tvf bin.tar
tar -xvf bin.tar

Compressing Files with zip
zip config.zip /etc/*.conf
zip -ry bin.zip /bin

Extracting and Viewing Zip Files
unzip -l config.zip
unzip -o bin.zip

Key Concepts Understood
Linux File Permissions

I practiced changing file permissions using chmod.

Example:

chmod o-r usdoi.txt

This removes read permission from others.

Permission Example:

-rw-r-----

Meaning:

Owner → read & write
Group → read
Others → no permission

Important Linux Commands Learned
Command	     Purpose
pwd	         Show current directory
ls	         List files and directories
cd	         Change directory
chmod	       Change file permissions
wget	       Download files from the internet
tar	         Archive files
zip	         Compress files
unzip	       Extract zip files
cat	         View file contents
mkdir	       Create directories

Hands-On Lab Activities Completed
Navigated Linux directories
Explored /bin and /etc
Downloaded files using wget
Modified Linux file permissions
Created .tar archives
Compressed files into .zip
Extracted archived files
Practiced Linux command-line operations

Progress Update

Successfully completed practical Linux command exercises and gained hands-on experience working with:

Linux terminal
File permissions
File compression
Directory management
Basic networking commands
Shell command usage

Currently continuing my Linux and Shell Scripting learning journey alongside my cybersecurity path after completing the Google Cybersecurity Professional Certificate.

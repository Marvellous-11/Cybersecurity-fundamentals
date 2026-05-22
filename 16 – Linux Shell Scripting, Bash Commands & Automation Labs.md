Overview

Today, I continued my learning journey in the Hands-on Introduction to Linux Commands and Shell Scripting course on Coursera. I explored Bash shell scripting, Linux command-line automation, text processing, conditionals, arrays, loops, cron jobs, and file manipulation. I also practiced creating executable shell scripts, handling file permissions, parsing CSV files, and working with Linux utilities such as grep, cut, sort, uniq, tr, and wget.

Topics Covered

Shell Scripting Basics

Introduction to Bash shell scripting
Creating shell script files using .sh
Making scripts executable using:
chmod +x filename.sh
Running scripts with:
./filename.sh
Checking Bash location:
which bash

Shell Variables & User Input

Declaring shell variables
Reading user input into variables using:
read variable_name

Example:

echo -n "Enter an integer: "
read n1

Filters, Pipes & Combining Commands

Learned how Linux commands can be chained together
Used commands such as:
sort
uniq
grep
tr
cut
paste

Combined commands using pipes:
command1 | command2

File & String Processing

Using grep
Searching for patterns inside files

Using tr
Translating and replacing characters

Using cut
Extracting columns from CSV files

Example:

cut -d "," -f 1 arrays_table.csv

Bash Metacharacters Learned

Metacharacter	   Meaning
#	               Comment
;	               Command separator
*	               Wildcard
?	               Single-character wildcard
\	               Escape character
" "	             Double quotes
' '	             Single quotes
>	               Redirect output
>>	             Append output
2>	             Redirect standard error
2>>	             Append standard error
<	               Redirect input

Command Substitution

Learned how to store command output inside variables:

files=$(ls)

Conditionals in Bash

Learned how to use:

if
elif
else
fi

Example:

if [ "$response" = "y" ]
then
   echo "You selected yes"
else
   echo "Invalid response"
fi

Arithmetic Calculations in Bash

Performed arithmetic operations:

Addition +
Subtraction -
Multiplication *
Division /

Example:

sum=$(($n1+$n2))
product=$(($n1*$n2))

Arrays in Bash

Worked with arrays and extracted CSV columns into arrays.

Example:

column_0=($(cut -d "," -f 1 $csv_file))

Working with CSV Files

Downloaded a CSV file using wget:

wget $csv_file

Viewed file content:

cat arrays_table.csv

CSV Content:

column_0,column_1,column_2
1,2,3
4,5,6
7,8,9
10,11,12

Parsing CSV Data into Arrays

Example:

csv_file="./arrays_table.csv"

column_0=($(cut -d "," -f 1 $csv_file))
column_1=($(cut -d "," -f 2 $csv_file))
column_2=($(cut -d "," -f 3 $csv_file))

File Permissions Practice

Checked permissions using:

ls -l

Modified permissions using:

chmod +x greet.sh
chmod u+x greet.sh
chmod o-r usdoi.txt

Cron Jobs & Task Scheduling

Learned Linux task scheduling using:

cron
crond
crontab

Useful commands:

crontab -e

Opens the cron editor.

crontab -l

Lists all scheduled cron jobs.

Cron syntax:

m h dom mon dow command

Linux Commands Practiced

pwd
ls
ls -l
ls -la
cat
cut
grep
paste
wget
chmod
which
echo
read
tar
zip
unzip

Challenges & Debugging Experience

During scripting practice, I encountered several Bash syntax and arithmetic errors while combining commands and conditionals. These mistakes helped me better understand:

Proper Bash script structure
Correct use of if/elif/else
Variable handling
Arithmetic expressions
Script execution flow
Input handling

This debugging experience improved my understanding of Linux shell scripting and command-line problem-solving.

Key Skills Gained

Linux terminal navigation
Bash scripting fundamentals
File permission management
User input handling
CSV parsing
Bash arrays
Conditional statements
Linux automation
Cron job scheduling
Command-line debugging
Text processing with Linux utilities

Current Learning Path

I am currently progressing through:

Hands-on Introduction to Linux Commands and Shell Scripting
Linux automation and scripting
Python programming
SQL fundamentals
Cybersecurity operations and SOC analysis

GitHub Documentation Series

This documentation is part of my continuous cybersecurity and Linux learning journey as I build practical hands-on technical skills in:

Linux
Shell scripting
Python
SQL
Cybersecurity
SOC operations
Automation and system administration

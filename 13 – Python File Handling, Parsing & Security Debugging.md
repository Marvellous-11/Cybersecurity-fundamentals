# 13 – Cybersecurity Python Labs & SOC Analyst Projects

## Overview
This project documents my practical learning experience with Python programming, security automation, debugging, file handling, and SOC analyst workflows as part of the Google Cybersecurity Professional Certificate on Coursera.

Python plays a major role in cybersecurity operations, especially in Security Operations Centers (SOC), where analysts automate repetitive tasks, parse security logs, monitor suspicious activity, and improve security workflows.

This project demonstrates how Python can be used for:
- Security automation
- Log analysis
- File handling
- Threat detection
- Access control management
- Debugging security scripts
- CI/CD security automation

---

## Topics Covered

### CI/CD Security Automation
- Automating security tasks in CI/CD pipelines
- Using Python to build security directly into deployment pipelines
- Why security automation is important in CI/CD
- Security testing automation
- Vulnerability scanning automation
- Compliance checks
- Secret management automation
- Policy automation
- Secure release management

### Python Fundamentals
- Variables
- Conditional statements
- Iterative statements (loops)
- Functions
- String handling techniques
- File handling in Python
- Importing files into Python
- Parsing text files
- Updating files using Python algorithms

### Python File Handling Methods
- `with`
- `open()`
- `.read()`
- `.write()`
- `.split()`
- `.join()`

### Debugging & Error Handling
- Debugging strategies
- Learning from mistakes
- Types of errors
- Syntax errors
- Logic errors
- Exceptions
- Index errors

---

## Python in Cybersecurity & SOC Operations

### Applications
- Security automation
- SOC analyst workflows
- Log monitoring
- User access management
- Threat detection
- Security scripting
- Compliance automation
- Security operations support

---

# Practical Lab 1 – Importing & Reading Security Logs

## Objective
Import a security log file into Python and prepare it for analysis.

---

## Opening a Security Log File

```python
import_file = "data/login.txt"

with open(import_file, "r") as file:

Purpose

The with statement safely opens the file and automatically closes it after use.

Reading the Security Log File

import_file = "data/login.txt"

with open(import_file, "r") as file:

    text = file.read()

Observation

The entire security log file was imported as one large string.

Practical Lab 2 – Parsing Security Logs
Splitting Log Data

print(text.split())

Output

['username,ip_address,time,date',
'tshah,192.168.92.147,15:26:08,2022-05-10',
'dtanaka,192.168.98.221,9:45:18,2022-05-09']

Observation

Using .split() converted the large string into a list, making the log easier to analyze line by line.

Practical Lab 3 – Updating Security Logs
Appending Missing Log Entries

import_file = "data/login.txt"

missing_entry = "jrafael,192.168.243.140,4:56:27,2022-05-09"

with open(import_file, "a") as file:

    file.write(missing_entry)

Observation

The missing log entry was successfully appended to the end of the file.

Practical Lab 4 – Creating an Allow List
Creating an Allow List File

import_file = "data/allow_list.txt"

ip_addresses = "192.168.218.160 192.168.97.225 192.168.145.158"

with open(import_file, "w") as file:

    file.write(ip_addresses)
Purpose

This creates a text file containing approved IP addresses allowed to access restricted resources.

Practical Lab 5 – Reading the Allow List

with open(import_file, "r") as file:

    text = file.read()

print(text)

Observation

The allow list file was successfully read into Python for further analysis.

Practical Lab 6 – Removing Unauthorized IP Addresses

Objective

Develop a Python algorithm that removes unauthorized IP addresses from an allow list.

Reading & Parsing the Allow List
with open(import_file, "r") as file:

    ip_addresses = file.read()

ip_addresses = ip_addresses.split()

Purpose

This converts the imported allow list into a Python list for easier processing.

Iterating Through IP Addresses

for element in ip_addresses:

    print(element)

Purpose

The loop processes each IP address individually.

Removing Unauthorized IP Addresses

for element in ip_addresses:

    if element in remove_list:

        ip_addresses.remove(element)

Observation

Unauthorized IP addresses were successfully removed from the allow list.

Updating the Allow List File

ip_addresses = " ".join(ip_addresses)

with open(import_file, "w") as file:

    file.write(ip_addresses)
Purpose

The updated list is converted back into a string and written into the original file.

Practical Lab 7 – Building a Security Automation Function

Creating the update_file() Function

def update_file(import_file, remove_list):

    with open(import_file, "r") as file:

        ip_addresses = file.read()

    ip_addresses = ip_addresses.split()

    for element in ip_addresses:

        if element in remove_list:

            ip_addresses.remove(element)

    ip_addresses = " ".join(ip_addresses)

    with open(import_file, "w") as file:

        file.write(ip_addresses)

Calling the Function
update_file(
    "allow_list.txt",
    ["192.168.25.60", "192.168.140.81", "192.168.203.198"]
)

Observation

The function automated the process of updating the allow list by removing unauthorized IP addresses.

Practical Lab 8 – Debugging Python Security Scripts

Objective

Identify and fix common Python errors used in security scripting.

Types of Errors Covered
Syntax errors
Logic errors
Exceptions
Index errors

Example 1 – Fixing a Syntax Error

Incorrect Code
for i in range(10)
    print("Connection cannot be established")

Corrected Code

for i in range(10):
    print("Connection cannot be established")

Issue Identified

The : symbol was missing from the loop header.

Example 2 – Fixing String & List Syntax Errors

Incorrect Code
usernames_list = ["djames", "jpark", "zdutchma "esmith"]

Corrected Code
usernames_list = ["djames", "jpark", "zdutchma", "esmith"]

Issue Identified
Missing quotation mark
Missing comma between list elements

Example 3 – Fixing a Missing Parenthesis

Incorrect Code
print("update needed".upper()

Corrected Code
print("update needed".upper())

Issue Identified

A closing parenthesis was missing.

Example 4 – Fixing Conditional Statement Errors

Corrected Code
for name in usernames_list:

    if name == username:

        print("The user is an approved user")

Errors Fixed
Replaced = with ==
Corrected indentation
Fixed variable spelling mistake

Example 5 – Fixing an Index Error

Corrected Code
if username == usernames_list[4]:

    print("This username is the final one in the list.")

Issue Identified

Python list indexing starts from 0, so index 4 represents the fifth item in the list.

Security Skills Demonstrated

Technical Skills
Python scripting
Security automation
Log parsing
File handling
Conditional logic
Iterative processing
Debugging security scripts
Threat detection logic
Access control automation
SOC analyst workflows

Learning Outcomes

Learned how to automate security tasks using Python
Understood how Python supports SOC analyst operations
Developed skills in reading and updating files
Applied loops and conditionals in cybersecurity tasks
Learned debugging strategies for security scripts
Practiced parsing and analyzing security logs
Built reusable security automation functions
Improved understanding of CI/CD security automation

Course Information

This project is based on practical labs and exercises completed during the Google Cybersecurity Professional Certificate on Coursera.

📌 This project is part of my cybersecurity portfolio and hands-on SOC analyst learning journey.

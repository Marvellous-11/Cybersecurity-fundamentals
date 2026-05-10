#12 – Python String Operations, Lists & Regex for Cybersecurity

Overview

This project documents my practical understanding of Python string operations, list manipulation, functions, conditionals, and regular expressions (Regex) as part of the Google Cybersecurity Professional Certificate on Coursera.

Python is an important programming language in cybersecurity because it helps automate security tasks, analyze logs, process device information, and detect suspicious activity. This project demonstrates how Python can be used for employee ID management, URL analysis, device authentication, and IP address investigation.

Topics Covered

Python String Operations

String data types
String concatenation
String indices
String slicing
String methods
.upper()
.lower()
len()
Bracket notation

Python Lists

List concatenation
Difference between strings and lists
.append()
.insert()
.remove()
List indexing

Python Programming Concepts

Algorithms
Conditional statements
Functions
Loops
Variables
Data types

Regular Expressions (Regex)

Regex Concepts Learned

import re
re.findall()
\w
\W
+
*
{n}
{n,n}
Pattern construction

Cybersecurity Applications

Practical Security Tasks

Employee ID standardization
Device ID extraction
URL component extraction
User authentication automation
Device verification
IP address extraction
Threat monitoring
Log analysis

Project 1 – Employee ID Standardization

Objective

Convert employee IDs into a standardized five-character format.

Converting Integer to String

employee_id = 4186

print(type(employee_id))

employee_id = str(employee_id)

print(type(employee_id))

Output

<class 'int'>
<class 'str'>

Observation

The employee ID was converted from an integer data type into a string data type for easier manipulation.

Validating Employee ID Length

employee_id = "4186"

if len(employee_id) < 5:
    print("This employee ID has less than five digits.")

Output

This employee ID has less than five digits.

Standardizing Employee ID

employee_id = "4186"

if len(employee_id) < 5:
    employee_id = "E" + employee_id

print(employee_id)

Output

E4186

Observation

String concatenation was used to standardize the employee ID format.

Project 2 – Device ID Analysis

Objective

Extract specific characters from device IDs for investigation and identification.

Extracting a Character from a Device ID

device_id = "r262c36"

print(device_id[3])

Output

2

String Slicing

device_id = "r262c36"

print(device_id[0:3])

Output

r26

Observation

String slicing helps extract important device information from specific positions.

Project 3 – URL Analysis

Objective

Extract website components from URLs using string slicing and indexing.

Extracting URL Protocol

url = "https://exampleURL1.com"

print(url[0:8])

Output

https://

Finding Domain Extension Position

url = "https://exampleURL1.com"

print(url.index(".com"))

Output

19

Extracting Website Name

url = "https://exampleURL1.com"

ind = url.index(".com")

print(url[8:ind])

Output

exampleURL1

Observation

String indexing and slicing can be used to extract useful website information for security investigations.

Project 4 – User & Device Authentication System

Objective

Build a simple authentication system using Python lists and conditionals.

Approved User Lists

approved_users = ["elarson", "bmoreno", "sgilmore"]
approved_devices = ["8rp2k75", "hl0s5o1", "4n482ts"]

Adding a New Approved User

approved_users.append("gesparza")
approved_devices.append("3rcv4w6")

print(approved_users)
print(approved_devices)

Observation

The .append() method allows administrators to add approved users and devices dynamically.

Removing a User

approved_users.remove("sgilmore")
approved_devices.remove("4n482ts")

Observation

The .remove() method helps revoke access for users who leave the organization.

Verifying Approved Users

username = "sgilmore"

if username in approved_users:
    print("User approved.")
else:
    print("User not approved.")

Project 5 – Login Authentication Function

Objective

Create a Python function that automates login verification.

Authentication Function

approved_users = ["elarson", "bmoreno", "sgilmore"]
approved_devices = ["8rp2k75", "hl0s5o1", "4n482ts"]

def login(username, device_id):

    if username in approved_users:

        print("The user", username, "is approved.")

        ind = approved_users.index(username)

        if device_id == approved_devices[ind]:
            print(device_id, "is the assigned device.")
        else:
            print(device_id, "is not the assigned device.")

    else:
        print("User is not approved.")

Function Testing

login("bmoreno", "hl0s5o1")

Output

The user bmoreno is approved.
hl0s5o1 is the assigned device.

Project 6 – Regular Expressions for Device Investigation

Objective

Use Regex to identify device IDs that begin with specific patterns.

Importing Regex Module

import re

Regex Pattern Construction

target_pattern = "r15\w+"

Explanation

r15 → Matches device IDs starting with r15
\w → Matches alphanumeric characters
+ → Matches one or more characters

Extracting Matching Device IDs

devices = "r151dm4 r15xk9h r15u9q5 r159r1u"

print(re.findall(target_pattern, devices))

Output

['r151dm4', 'r15xk9h', 'r15u9q5', 'r159r1u']

Project 7 – IP Address Extraction & Threat Detection

Objective

Extract valid IP addresses from security logs and identify flagged addresses.

Regex Pattern for Valid IP Addresses

pattern = "\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}"

Explanation

\d{1,3} → Matches between 1 and 3 digits
\. → Matches periods between segments

Extracting Valid IP Addresses

valid_ip_addresses = re.findall(pattern, log_file)

print(valid_ip_addresses)

Threat Monitoring System

flagged_addresses = [
    "192.168.190.178",
    "192.168.96.200"
]

for address in valid_ip_addresses:

    if address in flagged_addresses:
        print(address, "has been flagged.")
    else:
        print(address, "does not require investigation.")

Learning Outcomes

Learned Python string manipulation
Applied list operations in authentication systems
Developed conditional logic for security automation
Used Regex for log analysis and threat detection
Built login verification functions
Extracted and analyzed IP addresses
Improved understanding of cybersecurity scripting

Cybersecurity Skills Demonstrated

Python scripting
Security automation
Log analysis
Threat detection
Device authentication
Regex pattern matching
User access management
Network security analysis

Tools & Technologies

Python
Regex (re)
Linux concepts
Security log analysis
Authentication logic

Course Information

This project is based on practical labs and exercises from the Google Google Cybersecurity Professional Certificate on Coursera.

📌 This project is part of my cybersecurity portfolio and demonstrates my hands-on learning in Python programming, security automation, and threat analysis.

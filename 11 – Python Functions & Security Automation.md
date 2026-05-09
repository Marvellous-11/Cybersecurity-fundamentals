# 11 – Python Functions & Security Automation

## Overview
This project documents my understanding of Python functions, automation concepts, and programming fundamentals as part of the Google Cybersecurity Professional Certificate on Coursera.

Python is widely used in cybersecurity for automation, threat analysis, log monitoring, and security operations. This section demonstrates how Python functions, libraries, conditionals, and loops can be applied to cybersecurity-related tasks.

---

## Topics Covered

### Python Functions
- Introduction to functions
- Functions in cybersecurity
- Parameters in functions
- Return statements
- Functions and variables
- Built-in functions

### Built-in Functions Used
- `print()`
- `max()`
- `sorted()`
- `type()`

---

## Modules & Libraries

### Python Standard Library Modules
- `re` (regular expressions)
- `csv`
- `glob`
- `os`
- `time`
- `datetime`

### External Libraries
- Importing libraries
- Using modules in scripts
- Importance of reusable code

---

## Code Readability & Style

### Best Practices
- Proper syntax and formatting
- Code readability
- Indentation
- Comments in Python
- Single-line comments
- Multi-line comments
- Colons in headers

### Style Guide
- Python Enhancement Proposal (PEP 8)

---

## Python in Cybersecurity

### Applications
- Security automation
- Log analysis
- User activity monitoring
- Threat detection
- Security scripting
- Security team operations

---

## Practical Activity – Failed Login Analysis

### Objective
Analyze failed login attempts and identify unusual login activity using Python functions and conditionals.

---

## Sorting Failed Login Attempts

```python
failed_login_list = [119, 101, 99, 91, 92, 105, 108, 85, 88, 90, 264, 223]

print(sorted(failed_login_list))
```

### Output
```python
[85, 88, 90, 91, 92, 99, 101, 105, 108, 119, 223, 264]
```

### Observation
The sorted list revealed unusually high failed login attempts (223 and 264), which may indicate suspicious login activity requiring further investigation.

---

## Finding the Highest Failed Login Attempt

```python
print(max(failed_login_list))
```

### Output
```python
264
```

### Observation
The highest number of failed login attempts was 264.

---

## Creating a Security Monitoring Function

### Function Definition

```python
def analyze_logins(username, current_day_logins, average_day_logins):

    print("Current day login total for", username, "is", current_day_logins)

    print("Average logins per day for", username, "is", average_day_logins)

    login_ratio = current_day_logins / average_day_logins

    return login_ratio
```

---

## Function Call

```python
login_analysis = analyze_logins("ejones", 9, 3)

print("ejones", "logged in", login_analysis, "times as much as they do on an average day.")
```

### Output

```python
Current day login total for ejones is 9
Average logins per day for ejones is 3
ejones logged in 3.0 times as much as they do on an average day.
```

---

## Conditional Security Alert

```python
if login_analysis >= 3:
    print("Alert! This account has more login activity than normal.")
```

### Output

```python
Alert! This account has more login activity than normal.
```

---

## Learning Outcomes
- Developed understanding of Python functions and automation
- Learned how to use parameters and return statements
- Applied conditional statements for security monitoring
- Used built-in Python functions for data analysis
- Improved code readability using proper formatting and comments
- Understood how Python supports cybersecurity operations

---

## Cybersecurity Skills Demonstrated
- Security automation
- Login activity analysis
- Threat detection logic
- Conditional alert generation
- Python scripting fundamentals
- Security-focused programming

---

## Course Information
This project is based on practical learning from the Google Cybersecurity Professional Certificate on Coursera.

---

📌 This project is part of my cybersecurity portfolio and hands-on learning journey.

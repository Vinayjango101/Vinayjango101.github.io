

<h1>Mastering Linux Shells : A TryHackMe Walkthrough</h1>


![Linux Shells Banner](https://private-user-images.githubusercontent.com/193825699/452346786-74753747-4941-4f21-bc0c-2c201c26589d.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NDkyNDIyMTMsIm5iZiI6MTc0OTI0MTkxMywicGF0aCI6Ii8xOTM4MjU2OTkvNDUyMzQ2Nzg2LTc0NzUzNzQ3LTQ5NDEtNGYyMS1iYzBjLTJjMjAxYzI2NTg5ZC5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwNjA2JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDYwNlQyMDMxNTNaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT0yZjU3MGUzN2RkODA1YmUxNDcwNTQ5YzEyZGNkZGFkMDk0Y2ZlMjVlYTg2NTBmYTliN2FhNjlkNjE3MDk4NjFkJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.WXxTnxV0JOBSpGKWKupuumcLLrLrhcbtKU8c7GJi-9s)

## 🧠 Introduction

In this post, I delve into the **Linux Shells** module from TryHackMe's **Cyber Security 101** learning path. This module offers a comprehensive introduction to Linux command-line interfaces, shell scripting, and practical exercises to reinforce learning.

## 📘 Module Overview

The module covers:

- **Understanding Shells**: The interface between the user and the operating system.
- **Interacting with the Shell**: Basic commands and navigation.
- **Types of Linux Shells**: Exploring different shells like Bash, Zsh, and Fish.
- **Shell Scripting**: Writing and executing shell scripts.
- **Practical Exercises**: Hands-on tasks to apply learned concepts.

## 🛠️ Key Scripts from the Module

### 1. The Locker Script

This script simulates a bank locker authentication system, prompting the user for their username, company name, and PIN. If the provided credentials match predefined values, access is granted.

```
#!/bin/bash

# Defining the variables
username=""
companyname=""
pin=""

# Defining the loop
for i in {1..3}; do
    # Defining the conditional statements
    if [ "$i" -eq 1 ]; then
        echo "Enter your Username:"
        read username
    elif [ "$i" -eq 2 ]; then
        echo "Enter your Company name:"
        read companyname
    else
        echo "Enter your PIN:"
        read pin
    fi
done

# Checking if the user entered the correct details
if [ "$username" = "John" ] && [ "$companyname" = "Tryhackme" ] && [ "$pin" = "7385" ]; then
    echo "Authentication Successful. You can now access your locker, John."
else
    echo "Authentication Denied!!"
fi

Note: Ensure you're executing it with Bash and not sh.
```
2. The Flag Hunt Script
This script searches for a specific flag within system logs, demonstrating the use of grep and find commands.

bash
Copy
Edit
#!/bin/bash

# Searching for the flag in system logs
grep -r "flag" /var/log/
Note: The actual script content is not available in the provided resources.

🧪 Practical Exercises
The module includes exercises like:

The Locker Script: A script that authenticates users based on predefined credentials.

Flag Hunt: Searching for a specific flag within system logs.

🔗 Repository Overview
I've documented all the scripts and exercises from this module in my GitHub repository: THM-LinuxShells. The repository includes:

lockerscript.sh: The authentication script.

flag_hunt.sh: The script for searching flags in logs.

shell.sh and shell2.sh: Additional shell scripting exercises.

✅ Conclusion
The Linux Shells module is an excellent starting point for anyone looking to understand Linux command-line operations and scripting. The hands-on exercises provide practical experience, reinforcing the concepts learned.

Feel free to explore the repository and try out the scripts. Happy learning!

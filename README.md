[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/g7QA63Hz)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=15590720&assignment_repo_type=AssignmentRepo)
Git-Related Questions
1. Steps to Install Git on Windows:
Download Git: Visit the official Git website and download the latest version of Git for Windows.
Run the Installer: Execute the downloaded .exe file.
Select Components: During installation, you’ll see options to select additional components, like "Git Bash Here" and "Git GUI Here." It's recommended to include these options for easy access.
Adjusting PATH Environment: Choose the option "Git from the command line and also from 3rd-party software" to add Git to your system PATH, allowing you to use Git commands in the terminal.
Choose HTTPS or SSH: Select HTTPS or SSH as your transport protocol. SSH is generally recommended for security.
Line Ending Conversions: Choose the appropriate line-ending conversion (recommended to keep default settings for Windows).
Finish Installation: Complete the installation by clicking "Finish."
Key Options: Pay attention to adding Git to your PATH for terminal access, and choose SSH if you plan to use it for secure GitHub connections.

2. Purpose of Configuring Username and Email in Git:
Configuring your username and email in Git associates your identity with the commits you make. This information is used in the commit history to show who made specific changes. It’s essential for tracking contributions and collaboration within a team.
Effect on Workflow: If you don't set these, Git may prompt you to configure them before making any commits, potentially interrupting your workflow.

3. SSH Key and Connecting Git to GitHub Using SSH:
An SSH key is a pair of cryptographic keys used to authenticate a user without needing a password. It’s recommended to use SSH with GitHub because it provides a secure and convenient method of authentication.
Steps to Generate and Add an SSH Key:

Step 1: Open Git Bash and generate an SSH key with: ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
Step 2: Press Enter to save the key in the default location.
Step 3: Add the SSH key to your SSH agent: eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa
Step 4: Copy the SSH key to your clipboard: clip < ~/.ssh/id_rsa.pub
Step 5: Go to GitHub > Settings > SSH and GPG keys > New SSH key, and paste your key.
Step 6: Test your connection with: ssh -T git@github.com

4. Git Commands and Explanations: 
Initialize a new Git repository: git init

Creates a new Git repository in the current directory.
Clone an existing repository: git clone <repository-url>

Downloads a repository from GitHub to your local machine.
Add all modified files to the staging area: git add.

Stages all changes for the next commit.
Commit the changes with a message: git commit -m "Your commit message"

Records the changes in the repository with a descriptive message.
Push the changes to the main branch on GitHub: git push origin main
Uploads your local commits to the remote repository.

Verifying Local Git Setup with GitHub:
You can verify the connection by running: git remote -v

Python Navigator Questions
1. Variables and Data Types in Python:
Variables in Python are used to store data values. Each variable can hold data of different types, such as integers, strings, and booleans.

Example:
age = 25               # Integer
name = "John Doe"      # String
is_student = True      # Boolean

2. Control Flow in Python:
Control flow allows you to dictate the order in which your code executes.

Example using if, elif, and else:
number = 10
if number > 0:
    print("Positive")
elif number < 0:
    print("Negative")
else:
    print("Zero")

3. For Loops vs. While Loops in Python:
For Loop: Iterates over a sequence (like a list) and executes code for each item.
While Loop: Repeats as long as a certain condition is true.

Examples:
# For Loop
numbers = [1, 2, 3, 4, 5, 6]
for num in numbers:
    if num % 2 == 0:
        print(num)

# While Loop
i = 0
while i < len(numbers):
    if numbers[i] % 2 == 0:
        print(numbers[i])
    i += 1

4. Functions in Python:
A function is a block of reusable code that performs a specific task.

Example:
def add(a, b):
    return a + b

result = add(3, 4)
print(result)  # Output: 7

5. Lists vs. Dictionaries in Python:
List: Ordered collection of items.
Dictionary: Collection of key-value pairs.

Example:
# List of names
names = ["Alice", "Bob", "Charlie"]

# Dictionary of names and ages
ages = {"Alice": 25, "Bob": 30, "Charlie": 35}

# Accessing data
print(names[0])          # Output: Alice
print(ages["Bob"])       # Output: 30

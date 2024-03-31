# SHELL SCRIPTING

Shell scripting is a powerful tool commonly used across industries to automate tasks, test solutions, and increase efficiency. Shell scripting is a text file with a list of commands that instruct an operating system to perform certain tasks. 

A shell is an interface that interprets, processes, and executes these commands from the shell script. It can be particularly helpful to automate repetitive tasks, helping to save time and reduce human error. 

Shell scripting is primarily used to automate repetitive system tasks, such as backing up files, monitoring system resources, and managing user accounts. By turning a series of commands into a script, system administrators can save time, increase accuracy, and simplify complex tasks.

## USES OF SHELL SCRIPTING

Shell scripting is a valuable tool across several professions and fields due to its flexibility, power, and widespread support of operating systems. The following are some roles that use shell scripting: 

System administrators: System administrators often use shell scripts for automating administrative tasks like backups, system monitoring, user account creation and management, and many more routine activities. This allows for efficiency, consistency, and accuracy.

Developers: Developers often use shell scripting to automate development tasks, like automating file manipulation, deploying software to servers, running test suites, and more.

DevOps professionals: In the world of DevOps, shell scripting can benefit tasks such as automation, configuration management, troubleshooting, and rapid iteration. Shell scripts can run across operating platforms, which can be beneficial for those who work in several environments.

## BASIC SHELL SCRIPTING TERMS

A few definitions may come in handy when exploring this topic: 

- Terminal: A terminal is a program that establishes a connection with the server.

- Shell: This program interprets shell scripting commands from the terminal and runs on the server. This is the command-line user interface you choose and includes shells such as the Bourne shell, Korn shell, Bourne-Again shell, and C shell.

- Script: A script is a short program that performs a specific task.

- Command-line shell: A command-line shell (also known as a command prompt) allows you to instruct your computer through textual commands. 

- Shell script: A shell script is a script run through a command-line shell.

When you create a shell script, you might use text editors like Nano or Vim and save the file with a “.sh” extension. A shell interpreter interprets and executes these scripts; you can run them from the command line whenever necessary.

## TYPES OF SHELLS

Select a shell type that is most appropriate for your applications, as different types have varying capabilities. The shell you select will determine the resources on the system that you can access and how you can run programs. You can select from a variety of common shell types, such as:

1. Bourne shell: The Bourne shell, also known as ‘sh,’ was the original UNIX shell or command-line interpreter developed by Stephen Bourne at AT&T Bell Labs. While known for its high operation speed, this type of shell cannot reference previous commands and has limited built-in functionality. 

2. C shell: The C shell, ‘csh,’ is a shell developed by Bill Joy at the University of California Berkeley. This shell uses a similar syntax as the C programming language and incorporates aliases into the available features.

3. Bash shell: Bash, short for “Bourne Again Shell,” is a shell created by Brian Fox as a combination of sh, csh, and ksh capabilities. Bash is the default shell on Linux and Mac OSX. This type of shell can recall previous commands and edit them.

4. Korn shell: The Korn shell, or ‘ksh,’ is a shell developed by David Korn in the 1980s. It combines features of both the Bourne and C shells, along with its own improvements, such as string and array manipulation.

5. Z shell: The Z shell, or ‘zsh,’ is a modern extension of the sh shell and offers extensive customization. Some notable features include plugins, function indexes, and theming support.

## CAPABILITIES OF SHELL SCRIPT

Shell scripts are extremely flexible; they can be used for text printing, database monitoring, file manipulation, and much more. Although shell scripting allows you to call any program, shell programs are primarily powerful because of their ability to perform conditional operations, looping functions, and command-line arguments. This enables you to create intricate programs that are tailored to your requirements. 

## BENEFITS AND DRAWBACKS OF SHELL SCRIPTING

Shell scripting has strengths and weaknesses, depending on your application and field.

### Benefits   
Professionals, particularly those in system administration, DevOps development, and related fields, can benefit from shell scripting. As mentioned previously, it automates repetitive tasks and can boost productivity.

It’s ideal for rapidly prototyping complex applications. Shell scripts are simple to create, modify, and debug. Additionally, they can run on any UNIX-like system with little to no modification and are incredibly portable.

### Drawbacks

The drawback of shell scripts is that they might not be as efficient for intricate computational tasks as programs written in compiled languages. Scripting languages have a higher potential for expensive mistakes compared to other programming languages.

It might also be more advantageous to use a method other than shell scripting if you are performing database tasks that need for extensive database access. 

## EXAMPLES OF SHELL SCRIPTING

Shell scripting may be used for a variety of purposes, depending on your professional role. The following are some situations where you might decide to make use of shell scripting's capabilities:

1. You have multiple databases on a single machine, or your requirements aren’t specific to a single database: Shell scripting allows you to meet requirements that aren’t advisable or secure to fulfill using a single database

2. You need to perform tasks when the database isn’t running: In such cases, you can utilize a script to start or stop a database, as well as associated processes like listeners, which you can’t initiate from within the database itself.

3. You need to monitor the database’s status to ensure it’s running and ready to process queries: A script can serve this purpose, monitoring not only the database but also other system processes and resources, providing a comprehensive view of the system’s operations.

4. You need to monitor the database’s status to ensure it’s running and ready to process queries: A script can serve this purpose, monitoring not only the database but also other system processes and resources, providing a comprehensive view of the system’s operations.

## PREPARING PREREQUISITES

Git Bash was used for this project.

1. Install Git Bash. 

2. Launch Git Bash and open your selected terminal.

3. Git bash terminal was used for this project.


## INTRODUCTION TO SHELL SCRIPTING AND USER INPUT

Shell scripting helps you automate repititive task. 

Bash scripts are essentially a series of commmands and instructions executed sequentially in a shell. A shell script can be created by saving a collection of commands in a text file with a .sh extension. These scripts can be executed directly from the command line or called from other scripts. 

### Shell Scripting Syntax Elements

1. Variables: Bash allows you to define and work with variables. Variables can store data of various types such as numbers, strings, and arrays. You can assign values to variables using the = operator, and access their values using the variable name preceded by a $ sign. 

Assigning value to a variable, use the command:

```Bash
name="John"
```

Retrieving value from a variable: 

```Bash
echo $name
```

![alt text](<images/assigning and retrieving variables gitbash.png>)

2. Control Flow: Bash provides control flow statements like `if-else`, for loops,while loops , and case statements to control the flow of execution in your scripts. These statements allow decision making, terating over lists, and executing different commands based on conditions. 

Using `if-else` to execute script based on conditions, use command:

```Bash
#!/bin/bash

# Example script to check if a number is positive, negative, or zero

read -p "Enter a number: " num

if [ $num -gt 0 ]; then
    echo "The number is positive."
elif [ $num -lt 0 ]; then
    echo "The number is negative."
else
    echo "The number is zero."
fi
```

The code prompts you to type a number and prints a statement stating if it is a positive or negative number. In this project, 2 was the input number and it was positive.

![alt text](<images/if-else control flow.png>)

Iterating through a list using a `for loop`, run the command:

```Bash
#!/bin/bash

# Example script to print numbers from 1 to 5 using a for loop

for (( i=1; i<=5; i++ ))
do
    echo $i
done
```

![alt text](<images/loop iterating list.png>)

3. Command Substitution: This allows capturing the output of a command and use it as a value within your script. Backtick or the $()syntax can be used for command substitution. 

Using backtick for command substitution, run the command:

```Bash
current_date=`date +%Y-%m-%d`
```

Using `$()` syntax for command substitution, run the command: 

```Bash
current_date=$(date +%Y-%m-%d)
```

![alt text](<images/command substitution.png>)

4. Input and Output: Bash provides various ways to handle input and output. Use the read command to acccept user input, and output text to the console using the echo command. Additionally, you can redirect input and output using operators like > (output to a file), < (input from a file), and (pipe the output of one command as input to another).

Accept user input, run the command:

```Bash
echo "Enter your name:"
read name
```

![alt text](<images/Accept user input.png>)

Output text to terminal, run the command:

```Bash
echo "Hello World"
```

Out the result of a command into a file, run the command:

```Bash
echo "hello world" > index.txt
```

![alt text](<images/otput text & command result.png>)

Pass the content of a file as input to a command, run the command:

```Bash
grep "pattern" < input.txt
```

Pass the result of a command as input to another command, run:

```Bash
echo "hello world" | grep "pattern"
```

![alt text](<images/grep pattern.png>)

5. Functions: Bash allows you to define and use functions to group related commands together. Functions provide a way to modularize your code and make it more reusable. You can define functions using the function keyword or simply by declaring the function name followed by parentheses. Run the command:

```Bash
#!/bin/bash

# Define a function to greet the user
greet() {
    echo "Hello, $1! Nice to meet you."
}

# Call the greet function and pass the name as an argument
greet "John"
```

![alt text](<images/group related commands.png>)

### First Shell Script

1. On the terminal, open a folder called shell-scripting using the command:

```Bash
 mkdir shell-scripting
 ``` 
 
 This will hold all the written script. 

2. Create a file called user-input.sh using the command:

```Bash
touch user-input.sh
```

3. Inside the file copy and paste the block of code below:

```Bash
#!/bin/bash

# Prompt the user for their name
echo "Enter your name:"
read name

# Display a greeting with the entered name
echo "Hello, $name! Nice to meet you."
```
4. Save the file.

![alt text](<images/mkdir & touch user input.png>)

5. Run the command:

```Bash
sudo chmod +x user-input.sh
```

6. Run the script using the command:

```Bash
./user-input.sh
```

![alt text](<images/chmod & run sript.png>)


### Directory Manipulation and Navigation

Directory Manipulation and Navigation of Linux file system. A simple script would be written. 

This script will display the current directory, create a new directory called "my_directory", change to that directory, create two files in it, list the files, move bcak one level up, remove the "my_directory" and its contents, and finally list the files in the current directory again.

The follow steps should be used:

1. Open a file named `navigating-linux-filesystem.sh`.

![alt text](<images/create navigating linux file.png>)

2. Paste the code block below into the file:

```Bash
#!/bin/bash

# Display current directory
echo "Current directory: $PWD"

# Create a new directory
echo "Creating a new directory..."
mkdir my_directory
echo "New directory created."

# Change to the new directory
echo "Changing to the new directory..."
cd my_directory
echo "Current directory: $PWD"

# Create some files
echo "Creating files..."
touch file1.txt
touch file2.txt
echo "Files created."

# List the files in the current directory
echo "Files in the current directory:"
ls

# Move one level up
echo "Moving one level up..."
cd ..
echo "Current directory: $PWD"

# Remove the new directory and its contents
echo "Removing the new directory..."
rm -rf my_directory
echo "Directory removed."

# List the files in the current directory again
echo "Files in the current directory:"
ls
```

![alt text](<images/insert text in navi file .png>)

3. Run the command `sudo chmod +x navigating-linux-filesystem.sh` to set execute permission on the file.

4. Run the script using the command:

```Bash
./navigating-linux-filesystem.sh
```

![alt text](<images/execute permission and run navig script.png>)

### File Operations and Sorting

Write a simple shell script that focuses on File Operations and Sorting. 

This script creates three files (file1.txt, file2.txt, and file3.txt), displays the files in their current order, sorts them alphabetically, saves the sorted files in sorted_files.txt, dispalys the sorted files, removes the original files, renames the sorted file to sorted_files_sorted_alphabetically.txt, and finally displays the contents of the final sorted file. 

Using the steps below to carry out the task.

1. Open the terminal and create a file called "sorting.sh" using the command 

```Bash
touch sorting.sh
```

![alt text](<images/create sorting file.png>)

2. Copy and paste the code block below into the file.

```Bash
#!/bin/bash

# Create three files
echo "Creating files..."
echo "This is file3." > file3.txt
echo "This is file1." > file1.txt
echo "This is file2." > file2.txt
echo "Files created."

# Display the files in their current order
echo "Files in their current order:"
ls

# Sort the files alphabetically
echo "Sorting files alphabetically..."
ls | sort > sorted_files.txt
echo "Files sorted."

# Display the sorted files
echo "Sorted files:"
cat sorted_files.txt

# Remove the original files
echo "Removing original files..."
rm file1.txt file2.txt file3.txt
echo "Original files removed."

# Rename the sorted file to a more descriptive name
echo "Renaming sorted file..."
mv sorted_files.txt sorted_files_sorted_alphabetically.txt
echo "File renamed."

# Display the final sorted file
echo "Final sorted file:"
cat sorted_files_sorted_alphabetically.txt
```

![alt text](<images/nano insert in sorting file.png>)


3. Set execute permission on "sorting.sh" using the command:

```Bash
sudo chmod +x sorting.sh
```

4. Run the script using the command:

```Bash
./sorting.sh
```

![alt text](<images/execute permission and run sorting file  script.png>)

### Working with Numbers and Calculations

The script defines two variables num1 and num2 with nummeric values, performs basic arithmetric operations (addition, subtraction, multiplication, division, and modulus), and displays the results. It also performs more complex calculations such as raising num1 to the power of 2 and calculating the square root of num2, displays those results as well.

Proceed with the steps below:

1. On the terminal create a file called "calculations.sh" using the command:

```Bash
touch calculations.sh
```

![alt text](<images/create calculations file.png>)

2. Copy and paste the code block below:

```Bash
#!/bin/bash

# Define two variables with numeric values
num1=10
num2=5

# Perform basic arithmetic operations
sum=$((num1 + num2))
difference=$((num1 - num2))
product=$((num1 * num2))
quotient=$((num1 / num2))
remainder=$((num1 % num2))

# Display the results
echo "Number 1: $num1"
echo "Number 2: $num2"
echo "Sum: $sum"
echo "Difference: $difference"
echo "Product: $product"
echo "Quotient: $quotient"
echo "Remainder: $remainder"

# Perform some more complex calculations
power_of_2=$((num1 ** 2))
square_root=$(echo "sqrt($num2)" | bc)

# Display the results
echo "Number 1 raised to the power of 2: $power_of_2"
echo "Square root of number 2: $square_root"
```

![alt text](<images/execute permission and run calculations script.png>)

![alt text](<images/Insert text in calculations file.png>)

3. Set execute permission on "calculations.sh" using the command: 

```Bash
sudo chmod +x calculations.sh
```

4. Run your script using the command:

```Bash
./calculations.sh
```

![alt text](<images/execute permission and run calculations script.png>)


### File Backup and Timestamping

This focuses on file backup and timestamp. Backing up databases and other storage devices is a common task to carryout. 

This script defines the source directory and backup directory paths. It creates a timestamp using the current date and time, creates a backup directory with the timestamp appended to its name. The script then copies all files from the source directory to the backup directory using the cp command with the -r option for recursive copying. Finally, it displays a message indicating the completion of the backup process and shows the path of the backup directory with the timestamp.

Proceed using the following steps below:

1. On the terminal open a file "backup.sh" using the command:

```Bash
touch backup.sh
```

2. Copy and paste the code block below into the file. 

```Bash
#!/bin/bash

# Define the source directory and backup directory
source_dir="/path/to/source_directory"
backup_dir="/path/to/backup_directory"

# Create a timestamp with the current date and time
timestamp=$(date +"%Y%m%d%H%M%S")

# Create a backup directory with the timestamp
backup_dir_with_timestamp="$backup_dir/backup_$timestamp"

# Create the backup directory
mkdir -p "$backup_dir_with_timestamp"

# Copy all files from the source directory to the backup directory
cp -r "$source_dir"/* "$backup_dir_with_timestamp"

# Display a message indicating the backup process is complete
echo "Backup completed. Files copied to: $backup_dir_with_timestamp"
```

![alt text](<images/create backup file and insert text2.png>)

![alt text](<images/insert text in backup file.png>)

3. Set execute permission on "backup.sh" using the command:

```Bash
sudo chmod +x backup.sh
```

![alt text](<images/execute permission.png>)

4. Run the script using the command:

```Bash
./backup.sh
```

![alt text](<images/backup script.png>)

Thank you.
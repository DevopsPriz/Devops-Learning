# Devops-Learning

Learning basic commands on Linux

FILE MANIPULATION USING LINUX

SUDO COMMAND 

In Unix-like operating systems, the command sudo , which stands for "superuser do," is used to grant a permitted user the ability to execute commands as the super user. As a result, it's employed for tasks requiring root or administrative access.

The syntax: sudo (command for example; apt ugrade)

It becomes: sudo apt-get upgrade

The installed packages on your system can be upgraded to the their latest versions using this command.

![Sudo command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/ef1dfefd-f30c-4180-8395-00fd2dd4a1f8)

PWD COMMAND

pwd which stands for print working directory, shows the name of the directory you are currently in. To retrieve the entire current path, simply enter pwd, which begins with a forward slash (/). 

"pwd"

![pwd](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/6fba4ed9-e51d-4180-aa94-381e12865c3f)

I has two acceptable options:

* -L: Display the logical current working directory
* -P: Display the physical current working directory

![pwd -L command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/4437a548-21dd-4791-a663-8fb043ad652a)

CD COMMAND

cd stands for change directory, enables changing of directories in Linux. 

To change to a specific directory:

"cd Devops_Folder"

![cd command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/aed968f1-bfaa-4689-a24b-667da4777932)

Some shortcuts can help during directory navigation:

cd .. moves one directory up

cd - moves to your previous directory

![Cd command_1](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/63b9fa4c-a014-44f3-9a38-7bfdf6a92911)

LS COMMAND

The command "ls," which stands for "list," is used for displaying the files and folders in a given location. It displays a directory's entire contents.

To view the content of a directory while you are in it, just type ls like this, for example:

![ls command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/53006c55-3790-43a7-8862-09828ee26d05)

The ls -R command can also be used to list every file inside the subdirectories.

![ls -R](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/8ee01d59-6461-4232-b237-93ee1ebed990)

The ls -a command can be used to show hidden files in addition to visible ones.

The ls -lh command can be used to show files in easily readable formats such as MB and GB

![ls -a, ls -lh command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/de069be5-413b-4ece-ae55-3274f1d1947d)

CAT COMMAND

Concatenate, or cat for short, lists, combines, and writes file contents to the standard output. It is one of the most frequently used Linux commands. 

Type cat, the file name, and the extension to launch the command.

"cat Devops"

![cat command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/0695799b-8653-4544-ae68-7ff4c0eead24)

Two files can also be merged and stored as output in a third file.

"cat new_file2 cat new_file3 > mergedfile"

![cat merge command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/1a8487c1-813c-46ae-8488-22c72e657adf)

CP COMMAND

The command cp, which stands for copy, can be used copy files or directories from one place to another. The basic syntax:

"cp (options) source destination"

- source: the directory or file you wish to copy
- destination: Where the copied file(s) or directory would be placed.

To copy a file to another location

"cp new_file Desktop/"

![cp command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/1127b8bf-0158-424d-8e53-8e4a9b02b6f3)

MV COMMAND

Move, which is short for "mv," is used to move and rename directories and files.
Be aware that: when it is executed, it does not yield an output.

The syntax:
Simply type mv followed by the filename and the destination directory. Example:
"mv new_file Devops_Folder/"

You can also use the mv command to rename a file. Example:
"mv new_file new_file1"

![mv command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/18e2b22c-3b02-41aa-b46b-e91f1c4d83cf)

MKDIR COMMAND

The command "mkdir," which stands for "make directory," can be used to create one or more directories at once and set their respective permissions.

Keep in mind that: in order to avoid receiving a permission denied error, the user running this command needs to have the ability to create new folders in the parent directory.

The syntax:
mkdir (option) directory_name

For example:

1.  Create a directory "Devops_learn"
2.  Create a directory called "class" inside Devops_ learn

![mkdir command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/c9a54f4d-6a67-48c7-b80b-fd128c522c63)

RMDIR COMMAND  

The command rmdir, which stands for remove directory, is used to permanently erase an empty directory.

Keep in mind that: sudo rights in the parent directory are required for the user executing this command to achieve this.

For example: To remove an empty subdirectory named class.
"rmdir Devops_learn/class" was used.

![rmdir command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/7b26d58d-ad91-403f-8608-bc0426e99abe)

RM COMMAND

Files within a directory can be removed using this command.

This can be used to delete files within a directory.

For example: "rm new_file2 new_file3 new_file4"

![rm commands](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/9c022ff7-e5e3-4b9a-9d10-dabf98323dfc)

Some appropriate options that you could include are:

-i: prompts system confirmation before deleting a file.
-f: allows the system to remove without a confirmation.
-r: deletes files and directories recursively.

TOUCH COMMAND

The touch command allows the user to create an empty file or generate and modify a timestamp in the Linux Command Line.

Create an html file named index.html in the Desktop directory

![touch command 2](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/071e7802-ad84-4d0d-95a1-c55c9f03f2ad)

LOCATE COMMAND

The locate command is used to search for a file or a directory.

Adding the -i argument will turn off case sensitivity, to enable the search for files even if you don't remember its exact name.

The command enables quick location of a file path or a directory based on its name. 

Syntax: locate filename
The command above searches for the given filename and prints the path or paths that contain it.

Adding the -i option, makes the search case-insensitive.
Syntax: locate -i filename

![locate command 1](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/6f5e2c7b-2779-45e0-aabf-872d0ec68d8e)

FIND COMMAND

The find command is used for searching and locating files and directories based on various criteria.

![find command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/d60ff50c-8da1-404b-b310-99945ddaa19b)

GREP COMMAND

DF COMMAND

The df command used to display information about the amount of disk space available and used on file systems.

The df -h option displays the current directory's system disk space usage in a human-readable output, showing sizes in kilobytes (KB), megabytes (MB), gigabytes (GB), etc.

![df command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/8025e18f-ccdf-49e4-954b-8d95fc5aa5ab)

DU COMMAND

The du command is used to estimate the disk space used by files and directories.

You can run this command to determine which system part uses storage excessively. 

![du command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/168155ed-ad60-493f-9273-ee2eb890325c)

HEAD COMMAND

The head command is used to display the first lines of a text.

![head command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/5cb0b669-4fc8-459e-8bd9-a214391c3587)

TAIL COMMAND

The tail command is used to display the last part lines of a file.

![tail command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/d78e87cf-9d80-4be5-8f30-27f3d03e2472)

DIFF COMMAND

The command "diff," which stands for "difference,"is used to compare two files and display the differences between them after analyzing them.

![diff command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/ea740352-827b-4fc0-86eb-32adcdf6d3df)

TAR COMMAND

The command "tar" stands for "tape archive", archives mutliple files into a TAR file - a common Linux format similar to ZIP, with optional compression.

![tar command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/3b2764c5-da6d-44e3-815a-51f4438c38b8)

FILE PERMISSIONS AND OWNERSHIP

CHMOD COMMAND


CHOOWN COMMAND


JOBS COMMAND

The jobs command will display all the running processes along with their statuses. 

![jobs command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/c9d2911c-0b3b-4abe-b60e-aabd8b8377cd)

KILL COMMAND

The kill command is used to terminate or send signals to processes manually. It will signal misbehaving applications and instruct them to close their processes. 

![kill command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/88262b7f-5a8f-46e9-a47a-482d89cdea81)

PING COMMAND

The ping command is used to check whether a network or a server is reachable. Additionally, it can be used to troubleshoot various connectivity issues.

For example, ping goggle.com was used to know the connectivity to google and its measured response time.

![ping command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/20d40148-9df6-4a27-a5c1-df324271ccf9)

WGET COMMAND

The wget command is used for downloading files from the internet in Unix-like operating systems, including Linux. It can retrieve files from web servers and FTP servers and supports the HTTP, HTTPS, and FTP protocols.

![wget command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/ef01a925-cc85-4930-a525-3ee16eae6408)

UNAME COMMAND

The uname command will give detailed information about the Linux system and hardware, inclusive of the machine name, operating system, and kernel.

![uname commnad](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/dc2b2155-e59e-4e5f-a968-407e963dfaa3)

TOP COMMAND

In Linux and macOS, as well as other Unix-like operating systems, the top command is a real-time system monitoring tool that offers an interactive, dynamic view of system resource usage.It displays a list of processes and their resource utilization, including CPU, memory, and swap usage. 

Also, the top command helps to identify and terminate processes that may use too many system rseources.

![top command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/6878fff7-6827-4359-9728-7e6818fdce7a)

HISTORY COMMAND

A list of commands that the user has previously typed into the terminal is shown by the history command. It offers a history of recently executed commands, including line numbers, which is helpful for recalling and re-executing commands again. 

![history command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/a106388b-c494-41f4-adc8-f0692a431efd)

MAN COMMAND

The man command
The name "man" stands for "manual", it is used to display the manual pages (documentation) for various commands, utilities, and system functions.

![man command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/c69b833d-9226-463a-8af5-221b4e3e972b)

ECHO COMMAND

The echo command is used to display text or variables to the terminal. The text or value of a variable is output to the standard output using this simple command.

ZIP, UNZIP COMMANNDS

The zip and unzip commands are used for compressing and decompressing files and directories. These commands create and extract ZIP archives files respectively.

![zip, unzip command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/e532c77b-3497-4511-ac53-dfdbb00dce78)

HOSTNAME COMMAND

The hostname command is used for setting or displaying the system's hostname. 

![hostname](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/80efba3d-f4ac-4304-99e1-5cdf16d64cea)

USERADD, USERDEL COMMANDS

Linux is a multi-user system, which means that two or more persons can use it simultaneously. These commands are used to manage user accounts. 

The useradd command is used to create a new user account.

The userdel command is used to delete a user account. 

![useradd command error](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/62b7d7ac-e249-49fd-8b17-7bf20f2dfba8)

APT-GET COMMAND

The apt-get is a command line tool for handling Advanced Package Tool (APT) libraries in Linux. The command allows retrieval of information and bundles from authenticated sources to manage, update, remove, and install software and its dependencies on a system. 

![apt-get command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/b332eda1-1614-43a6-9682-688cb1067ea0)

NANO COMMAND

The nano command for Unix-like operating systems, including Linux, used to edit and manage files via a text editor. The command denotes keywords and can work with most languages. 

![nano command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/430c5381-8c58-4793-9e2d-9853aab0ab47)

VI COMMAND

The vi command is a text editor that functions in two different modes: insert and command.

The insert is used to edit and create a text file while, the command performs operations such as saving, opening, copying and pasting a file.

![vi command 2](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/d2cf1753-85ce-4603-b568-3fdd076f6aa2)

ALIAS, UNALIAS COMMAND 

The alias command allows the creation of a shortcut with the same functionality as a command, file name or text. The command execution instructs the shell to replace one string with another. 

However, the unlias command deletes an existing alias.

![alias, unalias command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/993afae4-7dfa-4631-afc9-f38c9f8e1ce7)

SU COMMAND

The su command, which stands for "substitute user" or "switch user," is used to change the user identity and execute commands with the privileges of a different user. This command is useful for accessing the system using the GUI (Graphical User Interface) display manager whne the root user is unavailable.

![su command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/9bf2d746-cfe6-4052-9bc9-2c570cd8d83a)

HTOP COMMAND

htop command in Linux system is a command line utility that allows the user to interactively monitor the system’s vital resources or server’s processes in real time. 

It provides a visual representation of system resources, such as CPU, memory, and processes, in a user-friendly and customizable format.

In contrast to top command, htop is a more recent program that has numerous advantages over it. Htop provides visual information regarding processor, memory, and swap utilization in addition to supporting mouse operation and using color in its output.

Along with printing complete command lines for processes, htop also provides vertical and horizontal scrolling for processes and command lines, respectively.

![htop command m](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/a55c6a8d-d94d-4234-8138-8df1172ff8ae)

PS COMMAND

The ps command in Unix-like operating systems, such as Linux and macOS, is used to display information regarding the active processes that are running on the system.

It offers a snapshot of the active processes, displaying information about them like PIDs (process IDs), TTYs (type of terminal), TIMEs (running time), and CMDs (commands that start the processes). The virtual files in the /proc file system are where the static results are sourced from.

![ps command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/13891a47-8619-482c-9704-4f6574b5a2a2)



# Devops-Learning

Learning basic commands on Linux

FILE MANIPULATION USING LINUX

SUDO COMMAND 

In Unix-like operating systems, the command sudo , which stands for "superuser do," is used to grant a permitted user the ability to execute commands as the super user. As a result, it's employed for tasks requiring root or administrative access.

The syntax: sudo (command for example; apt ugrade)

It becomes: sudo apt-get upgrade

The installed packages on your system can be upgraded to the their latest versions using this command.

![Screenshot 2024-01-11 114252](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/a3202f21-df94-4d30-9e2e-ec14a0c8bf2c)


PWD COMMAND

pwd which stands for print working directory, shows the name of the directory you are currently in. To retrieve the entire current path, simply enter pwd, which begins with a forward slash (/). 

![pwd](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/6fba4ed9-e51d-4180-aa94-381e12865c3f)

CD COMMAND

cd stands for change directory, enables changing of directories in Linux. 

![cd command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/aed968f1-bfaa-4689-a24b-667da4777932)

LS COMMAND

The command "ls," which stands for "list," is used for displaying the files and folders in a given location. It displays a directory's entire contents.

![ls command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/53006c55-3790-43a7-8862-09828ee26d05)

CAT COMMAND

Concatenate, or cat for short, lists, combines, and writes file contents to the standard output. It is one of the most frequently used Linux commands. 

![cat command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/0695799b-8653-4544-ae68-7ff4c0eead24)

CP COMMAND

The command cp, which stands for copy, can be used copy files or directories from one place to another

![cp command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/1127b8bf-0158-424d-8e53-8e4a9b02b6f3)

MV COMMAND

Move, which is short for "mv," is used to move and rename directories and files.
Be aware that: when it is executed, it does not yield an output.

![mv command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/18e2b22c-3b02-41aa-b46b-e91f1c4d83cf)

MKDIR COMMAND

The command "mkdir," which stands for "make directory," can be used to create one or more directories at once and set their respective permissions.

Keep in mind that: in order to avoid receiving a permission denied error, the user running this command needs to have the ability to create new folders in the parent directory.

![mkdir command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/c9a54f4d-6a67-48c7-b80b-fd128c522c63)

RMDIR COMMAND  

The command rmdir, which stands for remove directory, is used to permanently erase an empty directory.

Keep in mind that: sudo rights in the parent directory are required for the user executing this command to achieve this.

![rmdir command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/7b26d58d-ad91-403f-8608-bc0426e99abe)

RM COMMAND

Files within a directory can be removed using this command.

![rm commands](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/9c022ff7-e5e3-4b9a-9d10-dabf98323dfc)

TOUCH COMMAND

The touch command allows the user to create an empty file or generate and modify a timestamp in the Linux Command Line.

![touch command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/5d4bf0a8-cbac-4582-997b-97383428700c)

LOCATE COMMAND

The locate command is used to search for a file or a directory.

![locate command](https://github.com/DevopsPriz/Devops-Learning/assets/151751244/b8cd04d3-f25b-4756-af38-c68a1e919123)

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






Linux Commands Reference and Practical Lab Report

Student Report – Linux Essentials Learning Path

---

1. Introduction

This report documents the Linux commands I practiced during my Linux Essentials learning path.
The purpose of this practice was to become familiar with basic Linux terminal usage, system information commands, file and directory management, networking tools, environment variables, command documentation, process management, and command history.

Linux is widely used in system administration, cybersecurity, penetration testing, cloud computing, servers, and DevOps environments. Learning how to use the terminal is an important foundation for working with Linux professionally.

During this lab, I practiced commands directly in a Linux environment and documented their purpose, syntax, and usage examples.

---

2. Objectives

The main objectives of this lab were:

- To understand basic Linux command-line usage.
- To practice navigating the Linux filesystem.
- To create, copy, move, rename, and delete files and directories.
- To view system and hardware information.
- To understand environment variables such as "PATH".
- To use Linux help and documentation tools.
- To practice basic networking commands.
- To understand basic process management.
- To build confidence using the Linux terminal.

---

3. Lab Environment

The commands were practiced in a Linux desktop environment using the terminal.

General lab environment:

- Operating System: Linux
- Interface: Graphical desktop environment and terminal
- Text Editor: Nano
- Shell: Bash-compatible terminal
- Learning Path: Linux Essentials

---

4. System Information Commands

System information commands are used to display details about the operating system, kernel, hardware, disks, and partitions.

4.1 "uname -a"

The "uname -a" command displays detailed system information, including the kernel version, hostname, system architecture, and operating system details.

Example:

uname -a

This command is useful when checking the system kernel version or identifying the type of Linux system being used.

---

4.2 "cat /proc/cpuinfo"

The "cat /proc/cpuinfo" command displays detailed CPU information such as CPU model name, number of cores, CPU flags, cache size, and processor details.

Example:

cat /proc/cpuinfo

This command is useful for checking processor information directly from the Linux virtual filesystem.

---

4.3 "lspci"

The "lspci" command lists PCI devices connected to the system, such as network cards, graphics cards, audio devices, and storage controllers.

Example:

lspci

This command is helpful for identifying hardware devices installed on the system.

---

4.4 "lsblk -f"

The "lsblk -f" command displays block devices, partitions, filesystems, UUIDs, labels, and mount points.

Example:

lsblk -f

This command is useful for understanding disk layout and mounted partitions.

---

4.5 "fdisk -l"

The "fdisk -l" command lists available disks and partition tables on the system.
This command usually requires root privileges.

Example:

sudo fdisk -l

This command is commonly used when checking disk partitions and storage devices.

---

4.6 "gparted"

The "gparted" command opens a graphical partition editor used for creating, deleting, resizing, and managing disk partitions.

Example:

sudo gparted

GParted is useful when a graphical tool is preferred for disk and partition management.

---

5. File and Directory Management Commands

File and directory management commands are essential for working with files, folders, and paths in Linux.

5.1 "pwd"

The "pwd" command displays the absolute path of the current working directory.

Example:

pwd

This helps the user know exactly where they are in the filesystem.

---

5.2 "ls"

The "ls" command lists files and directories in the current directory.

Example:

ls

Other useful options include:

ls -l
ls -a
ls -al

Explanation:

- "ls -l" displays detailed information.
- "ls -a" shows hidden files.
- "ls -al" combines detailed listing with hidden files.

---

5.3 "cd"

The "cd" command changes the current working directory.

Example:

cd /home/user

To return to the home directory:

cd ~

The "cd" command is one of the most frequently used commands for terminal navigation.

---

5.4 "touch"

The "touch" command creates an empty file or updates the timestamp of an existing file.

Example:

touch notes.txt

Another example used during practice:

touch -c file57.txt

The "-c" option prevents creating the file if it does not already exist.

Timestamp example:

touch -d "Jun 19 2018" file57.txt

This changes the timestamp of the file to a specific date.

---

5.5 "nano"

The "nano" command opens a file in the Nano text editor.

Example:

nano notes.txt

Nano is a simple terminal-based text editor used for creating and editing text files.

---

5.6 "cat"

The "cat" command displays the contents of a file in the terminal.

Example:

cat notes.txt

This command is useful for quickly reading small text files.

---

5.7 "mkdir"

The "mkdir" command creates a new directory.

Example:

mkdir folder1

To create nested directories, the "-p" option can be used:

mkdir -p folder1/folder2

This creates both "folder1" and "folder2" if they do not already exist.

---

5.8 "cp"

The "cp" command copies files and directories.

Example:

cp file1.txt folder1/copy2.txt

Copying a file to the Desktop:

cp copy2.txt ~/Desktop/

Copying directories recursively:

cp -r videos/ desktop

Useful options:

cp -f
cp -i
cp -u
cp -p

Explanation:

- "cp -f" forces overwrite.
- "cp -i" asks before overwriting.
- "cp -u" copies only when the source file is newer.
- "cp -p" preserves file attributes such as timestamps and permissions.

---

5.9 "rm"

The "rm" command removes files.

Example:

rm file1.txt file.txt

Removing files with wildcard:

rm *

Recursive removal:

rm -r folder2

Force recursive removal:

rm -rf folder2

Important note:

The "rm -rf" command is dangerous if used incorrectly because it can delete files and directories without confirmation.

---

5.10 "rmdir"

The "rmdir" command removes empty directories.

Example:

rmdir folder1

Unlike "rm -r", this command only works on empty directories.

---

5.11 "mv"

The "mv" command moves or renames files.

Move a file into a directory:

mv file1.txt folder1

Rename a file:

mv file1.txt file4.txt

Move a file to the parent directory:

mv file1.txt ..

Rename a file as a hidden file:

mv 1.txt .1.txt

In Linux, files starting with a dot "." are hidden files.

---

6. Virtual Terminal Commands

Linux supports virtual terminals that allow users to switch between graphical and text-based sessions.

6.1 "Ctrl + Alt + F1"

This key combination switches to a virtual terminal or login screen, depending on the Linux distribution and desktop environment.

6.2 "Ctrl + Alt + F7"

On older Linux systems, this often returns to the graphical desktop environment.
On modern Linux distributions, the graphical session may be on "F1", "F2", or another function key.

---

7. Networking Commands

Networking commands are used to test connectivity and view network configuration.

7.1 "ping"

The "ping" command tests network connectivity and measures latency to a remote host.

Example:

ping google.com

This command sends packets to a remote host and shows whether the host is reachable.

---

7.2 "ip addr"

The "ip addr" command displays network interface information and assigned IP addresses on Linux systems.

Example:

ip addr

Short version:

ip a

Note:

"ipconfig" is commonly used on Windows.
On Linux, "ip addr" or "ip a" is the modern alternative.

---

8. Environment Variable Commands

Environment variables store system and shell information that can be used by programs and commands.

8.1 "echo $PATH"

The "echo $PATH" command displays the directories that the shell searches when executing commands.

Example:

echo $PATH

Example output:

/bin:/usr/bin:/usr/local/bin

The "PATH" environment variable allows commands to run without typing their full path.

Common user command paths:

/bin
/usr/bin
/usr/local/bin

Common administrator command paths:

/sbin
/usr/sbin
/usr/local/sbin

---

8.2 "printenv"

The "printenv" command displays environment variables.

Example:

printenv

This command is useful for viewing shell environment settings.

---

8.3 Shell Variables

Examples practiced:

echo $a
echo $a$b
echo $a; echo $b

These commands show how shell variables can be displayed and combined.

---

9. Command Information and Help

Linux provides several tools for learning about commands and finding documentation.

9.1 "type"

The "type" command shows how the shell interprets a command and where the executable is located.

Example:

type ping

This command helps determine whether a command is built into the shell, an alias, or an external executable.

---

9.2 "man"

The "man" command opens the manual page for a command or system utility.

Example:

man ls

Manual pages provide detailed explanations, options, and usage examples.

---

9.3 "whatis"

The "whatis" command displays a short description of a command.

Example:

whatis ping

This is useful for quickly understanding what a command does.

---

9.4 "whereis"

The "whereis" command locates the binary, source, and manual page files for a command.

Example:

whereis ping

---

9.5 "apropos"

The "apropos" command searches manual page names and descriptions.

Example:

apropos network

This is useful when the exact command name is not known.

---

9.6 "man -k"

The "man -k" command works similarly to "apropos".

Example:

man -k ping

---

9.7 "info"

The "info" command opens GNU Info documentation.

Example:

info ping

---

9.8 "makewhatis"

The "makewhatis" command creates or updates the database used by "whatis".

Example:

makewhatis

This command may require administrator privileges depending on the system.

---

10. Process Management Commands

Process management commands help control running programs and background jobs.

10.1 "firefox &"

The ampersand "&" runs a program in the background.

Example:

firefox &

This allows the terminal to remain usable while Firefox runs.

---

10.2 "bg"

The "bg" command moves a suspended job to the background.

Example:

bg %1

This is useful when managing jobs from the terminal.

---

11. Command History

11.1 "history"

The "history" command displays previously executed commands in the current shell session.

Example:

history

This helps review commands that were practiced or previously executed.

---

12. Practical Lab Evidence

Screenshot 1 – File and Directory Management Practice

In this practical exercise, I practiced Linux commands related to file and directory management.

Commands practiced in this section included:

ls -l
touch -c file57.txt
touch -d "Jun 19 2018" file57.txt
touch "c h"
mkdir folder1/folder2
mkdir folder1/folder2 -p

cp file1.txt folder1/copy2.txt
cp copy2.txt ~/Desktop/
cp -r videos/ desktop

cp -f
cp -i
cp -u
cp -p

rm
rm file1.txt file.txt
rmdir
touch .x
rm -rf folder2
rm *
rm * -rf

mv file1.txt folder1
mv file1.txt file4.txt
mv file1.txt ..
mv 1.txt .1.txt

Topics covered:

- Creating files using "touch"
- Modifying file timestamps
- Creating files with spaces in their names
- Creating nested directories using "mkdir -p"
- Copying files and folders
- Using different "cp" options
- Removing files and directories
- Using recursive and force deletion carefully
- Moving and renaming files
- Creating hidden files

Learning outcome:

This exercise helped me understand how to manage files and directories from the Linux command line. I learned how to create, copy, move, rename, and delete files and directories using different command options.

Insert Screenshot 1 here.

---

Screenshot 2 – Linux Essentials Command Practice

In this practical exercise, I practiced general Linux Essentials commands, including navigation, environment variables, help tools, networking, and process management.

Commands practiced in this section included:

gparted
cd
ls
exit
~

touch x
nano x

Ctrl + Alt + F1
Ctrl + Alt + F7

ping
ipconfig

type ping
cd /ping
ls

echo $PATH
cat
man

bg firefox
pwd
history
mkdir

ls -al
ls -a
ls -l
ls -l folder11/

rm
rmdir
rm -r

echo $a
echo $a$b
echo $a; echo $b
echo $PATH

printenv
ls folder*

echo "hello, pipi"
echo "mysaleary is $2000 per mount"

whatis ping
whatis
makewhatis
whereis
apropos
man
man -k
info ping

Topics covered:

- Terminal navigation
- File creation and editing
- Virtual terminal switching
- Network connectivity testing
- Environment variables
- Command documentation
- Command history
- File listing options
- Directory creation and deletion
- Shell variable usage
- Searching command manuals
- Background process usage

Learning outcome:

This exercise helped me build a stronger foundation in Linux terminal usage. I practiced important commands that are commonly used in system administration, cybersecurity, and troubleshooting.

Insert Screenshot 2 here.

---

13. Important Notes and Corrections

During the lab, some commands were written as notes or practice examples. A few important corrections are listed below:

"ipconfig"

"ipconfig" is a Windows command.
On Linux, the modern equivalent is:

ip addr

or:

ip a

"rm -rf"

The command:

rm -rf

must be used carefully because it can permanently delete files and directories without asking for confirmation.

File Names with Spaces

When creating or accessing files with spaces in their names, quotes should be used.

Example:

touch "c h"

Hidden Files

Files starting with a dot are hidden in Linux.

Example:

mv 1.txt .1.txt

To view hidden files:

ls -a

---

14. Summary of Skills Practiced

Through this Linux Essentials lab, I practiced the following skills:

- Viewing system and hardware information
- Checking disks and partitions
- Navigating directories
- Creating and editing files
- Displaying file contents
- Creating directories
- Copying files and directories
- Moving and renaming files
- Removing files and directories
- Working with hidden files
- Understanding environment variables
- Viewing command documentation
- Searching Linux manuals
- Testing network connectivity
- Managing background processes
- Reviewing command history

---

15. Conclusion

This lab helped me gain practical experience with essential Linux commands.
By practicing these commands directly in the terminal, I became more comfortable with the Linux command-line environment.

The exercises covered system information, file and directory management, networking, environment variables, help tools, command history, and process management. These are important skills for anyone who wants to continue learning Linux administration, cybersecurity, penetration testing, Red Team operations, or system troubleshooting.

Overall, this practice provided a strong foundation for future Linux learning and helped me understand how Linux commands are used in real-world technical tasks.

---

16. Future Learning Goals

After completing this lab, the next topics I should practice are:

- Linux users and groups
- File permissions
- "chmod", "chown", and "chgrp"
- Bash scripting basics
- Package management
- Services and processes
- Networking tools
- SSH usage
- Log files
- Basic Linux security
- Home lab setup for cybersecurity practice

These topics will help me move from basic Linux usage toward more advanced Linux administration and cybersecurity skills.

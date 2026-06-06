Linux Commands Reference

This file contains Linux commands I practiced during my Linux Essentials learning path.
Each command includes a short explanation and a basic example.

---

System Information Commands

"uname -a"

Displays detailed system information, including the kernel version, hostname, system architecture, and operating system details.

uname -a

"cat /proc/cpuinfo"

Displays detailed CPU information such as model name, number of cores, CPU flags, cache size, and processor details.

cat /proc/cpuinfo

"lspci"

Lists PCI devices connected to the system, such as network cards, graphics cards, audio devices, and storage controllers.

lspci

"lsblk -f"

Displays block devices, partitions, filesystems, UUIDs, labels, and mount points.

lsblk -f

"fdisk -l"

Lists available disks and partition tables on the system. This command usually requires root privileges.

sudo fdisk -l

"gparted"

Opens a graphical partition editor used for creating, deleting, resizing, and managing disk partitions.

sudo gparted

---

File and Directory Management Commands

"pwd"

Displays the absolute path of the current working directory.

pwd

"ls"

Lists files and directories in the current directory.

ls

"cd"

Changes the current working directory.

cd /home/user

"cd ~"

Moves to the current user's home directory.

cd ~

"touch"

Creates an empty file or updates the timestamp of an existing file.

touch notes.txt

"nano"

Opens a file in the Nano text editor.

nano notes.txt

"cat"

Displays the contents of a file in the terminal.

cat notes.txt

"exit"

Closes the current shell session.

exit

---

Virtual Terminal Commands

"Ctrl + Alt + F1"

Switches to a virtual terminal or login screen, depending on the Linux distribution and desktop environment.

"Ctrl + Alt + F7"

Often returns to the graphical desktop environment on older Linux systems. On modern Linux distributions, the graphical session may be on "F1", "F2", or another function key.

---

Networking Commands

"ping"

Tests network connectivity and measures latency to a remote host.

ping google.com

"ip addr"

Displays network interface information and assigned IP addresses on Linux systems.

ip addr

Short version:

ip a

«Note: "ipconfig" is commonly used on Windows. On Linux, "ip addr" or "ip a" is the modern alternative.»

---

Environment Variable Commands

"echo $PATH"

Displays the directories that the shell searches when executing commands.

echo $PATH

Example output:

/bin:/usr/bin:/usr/local/bin

"$PATH"

"PATH" is an environment variable that stores directories containing executable programs. It allows commands to run without typing their full path.

Common user command paths:

/bin
/usr/bin
/usr/local/bin

Common administrator command paths:

/sbin
/usr/sbin
/usr/local/sbin

---

Command Information and Help

"type"

Shows how the shell interprets a command and where the executable is located.

type ping

"man"

Opens the manual page for a command or system utility.

man ls

---

Process Management Commands

"bg"

Moves a suspended job to the background.

bg %1

"firefox &"

Starts Firefox directly in the background.

firefox &

---

Command History

"history"

Displays previously executed commands in the current shell session.

history

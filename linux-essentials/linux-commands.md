
Day 01 - Linux Commands

System Information

"uname -a"

Displays detailed system information, including the kernel version, hostname, system architecture, and operating system details.

"cat /proc/cpuinfo"

Shows detailed information about the CPU, including model name, number of cores, cache size, and supported CPU features.

"lspci"

Lists PCI devices connected to the system, such as network cards, graphics cards, audio devices, and storage controllers.

"lsblk -f"

Displays block devices, partitions, filesystems, UUIDs, labels, and mount points.

"fdisk -l"

Lists available disks and partition tables on the system. This command may require root privileges.

Example:

sudo fdisk -l

"gparted"

Opens a graphical partition editor used for creating, deleting, resizing, and managing disk partitions. It may need to be installed separately and usually requires administrative privileges.

---

File and Directory Management

"cd"

Changes the current working directory.

Example:

cd /home/user

"ls"

Lists files and directories in the current location.

Example:

ls

"pwd"

Displays the absolute path of the current working directory.

Example:

pwd

"touch file"

Creates an empty file or updates an existing file's timestamp.

Example:

touch notes.txt

"nano file"

Opens a file in the Nano text editor for editing.

Example:

nano notes.txt

"exit"

Closes the current shell session.

---

Virtual Terminals (TTY)

"Ctrl + Alt + F1"

Switches to a virtual terminal or login screen, depending on the Linux distribution and desktop environment.

"Ctrl + Alt + F7"

Often returns to the graphical desktop environment on older Linux systems, but this may vary depending on the distribution. On some modern systems, the graphical session may be on "F1", "F2", or another function key.

---

Networking

"ping"

Tests network connectivity and measures latency to a remote host.

Example:

ping google.com

"ip addr"

Displays network interface information and IP addresses on Linux systems.

Example:

ip addr

Short version:

ip a

---

Environment Variables

"echo $PATH"

Displays the directories searched by the shell when executing commands.

Example:

echo $PATH

Example output:

/bin:/usr/bin:/usr/local/bin

"PATH"

Stores the locations of executable files that can be run directly from the terminal without typing their full path.

---

Command Information

"type ping"

Shows how the shell interprets the "ping" command and where the executable is located.

Example:

type ping

"man"

Opens the manual pages for commands and system utilities.

Example:

man ls

---

Process Management

"bg"

Moves a suspended job to the background.

Example:

bg %1

Another common way to start a program directly in the background is:

firefox &

---

Command History

"history"

Displays previously executed commands in the current shell session.

Example:

history

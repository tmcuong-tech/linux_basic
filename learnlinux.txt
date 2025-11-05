LINUX

NETWORKING
dig -x [ip] : Reverse lookup of an IP address
dig [domain] : Show DNS information for a domain
host [domain] : Resolve a domain to IP address
curl -O [file-url] : Download a file from a URL
ifconfig : Show all network interfaces (legacy, use ip addr show)
ip addr show : Show IP addresses of all interfaces
ip address add [ip] dev [interface] : Assign IP address to interface
netstat -tulnp : Show active listening ports
nslookup [domain] : Show domain information
ping [hostname] : Check network connectivity
wget [file_url] : Download a file from a URL
whois [domain] : Show domain registration information

USERS AND GROUPS
adduser [user] : Add a new user
chgrp [group] [directory] : Change directory group ownership
groupadd [group] : Add a new group
id : Show active user details
last : Show last system logins
passwd [username] : Change password for the user
userdel [user] : Delete a user
usermod [options] [user] : Modify user information
usermod -aG [group] [user] : Add user to a group
w : Show logged-in users and their activity
who : Show who is logged in

FILE COMMANDS
awk '{pattern} {print $0}' [file] : Print line matching a pattern
cp [file1] [file2] : Copy file1 to file2
cp -r [directory1] [directory2] : Copy directory recursively
cut -d [delimiter] -f [field] [file] : Cut file sections and print
diff [file1] [file2] : Compare two files
gpg [file.gpg] : Decrypt a file
gpg -c [file] : Encrypt a file
head [file] : Show first 10 lines of a file
less [file] : View text with scrolling
ln -s [/path/file] [link] : Create symbolic link to file
ls : List files in directory
ls | xargs wc : Count words / lines / bytes in all files in directory
ls -a : List files including hidden ones
mkdir [name] : Create a new directory
more [file] : Show file contents (page by page)
mv [filename1] [filename2] : Rename or move a file
pwd : Show current working directory
rm [file] : Remove a file
rm -r [directory] : Remove a directory recursively
rm -rf [directory] : Force remove directory recursively
shred -u [file] : Overwrite and delete a file
source [file] : Run commands from a file in the current shell
sudo [command] : Run command with superuser privileges
tail [file] : Show last 10 lines of a file
touch [file] : Create an empty file or update timestamp
wc [file] : Count words / lines / bytes in a file
[command] | tee [file] > /dev/null : Store command output to a file and suppress terminal output
[data] | cut -d [delimiter] -f [field] : Cut data section and print

DIRECTORY NAVIGATION
cd .. : Move up one level
cd : Change to home directory ($HOME)
cd [directory] : Change to specified directory

HARDWARE INFORMATION
cat /proc/cpuinfo : Show CPU information
dmesg : Show bootup messages
dmidecode : Show BIOS hardware information
free -h : Show free and used memory
lsblk : Show block devices information
lshw : Show hardware configuration information
lspci -tv : Tree diagram of PCI devices
lsusb -tv : Tree diagram of USB devices
neofetch : Display OS & hardware information
hdparm -i /dev/[disk] : Show disk information
hdparm -tT /dev/[disk] : Test disk read speed
badblocks -s /dev/[disk] : Check unreadable disk blocks

FILE COMPRESSION
gzip [file] : Create a .gz compressed file
tar -xf [file.tar] : Extract archived file
zip [file.zip] [files...] : Create a zip archive
unzip [file.zip] : Extract a zip archive
tar -cf [file.tar] [file] : Create a tar archive from a file
tar -caf [file.tar.gz] [file] : Create a gzipped tar archive

PACKAGE INSTALLATION
apt-get : Search for and install software packages
apt install [package] : Install a package with APT
dnf install [package.rpm] : Install a package with DNF
rpm -e [package] : Remove an rpm package
rpm -i [package.rpm] : Install a local rpm package
yum info [package] : Show package information & summary
yum install [package.rpm] : Install a package with YUM
yum search [package] : Search for a package by keyword
tar -xzf [source_code.tar.gz] : Extract source code archive
cd [source_code] : Enter source code directory
./configure : Configure software before build
make : Compile software from source code
make install : Install compiled software

SYSTEM MANAGEMENT
cal : Show a calendar (current month by default)
date : Show or set the system date and time
finger [username] : Show information about a user
hostname : Show the system hostname
hostname -I : Show system IP addresses
last reboot : Show system reboot history
modprobe [module-name] : Add or remove a kernel module
shutdown [hh:mm] : Schedule a system shutdown at specified time
shutdown now : Shut down the system immediately
timedatectl : Control and display system date, time, and time zone
ulimit [options] [limit] : Set or view user resource limits
uname -a : Show all system information (kernel, version, architecture, etc.)
uname -r : Show kernel release version
uptime : Show system uptime and load averages
whoami : Show the current logged-in user

FILE PERMISSION
chmod 755 [file] : Owner has full permissions; group and others have read and execute
chmod 766 [file] : Owner has full permissions; group and others have read and write
chmod 777 [file] : Everyone has full read, write, and execute permissions
chown [user] [file] : Change file ownership (user)
chown [user]:[group] [file] : Change file owner and group

SSH LOGIN
ssh [user]@[host] : Connect to a host as a specified user
ssh [host] : Connect to a host using default SSH port 22
telnet [host] : Connect to a Telnet server on default port 23
ssh -p [port] [user]@[host] : Connect to a host via SSH using a custom port

VARIABLES
declare variable="value" : Declare and initialize a Bash variable
echo $variable : Display the value of a variable
export variable : Export a Bash variable to the environment
let variable=value : Assign an integer value or perform arithmetic with a variable
set : List shell variables and functions

FILE TRANSFER
scp file.txt user@server:/tmp : Securely transfer a file to a remote server using SSH
rsync -a /location/ /backup/ : Synchronize the contents of a local directory with a backup directory

DISK USAGE
fdisk -l : List disk partitions, types, and sizes
df -h : Show disk space usage in a human-readable format
df -l : Show inode usage on the system
du -ah : Show disk usage for all files and directories
du -sh : Show total disk usage of the current directory in a human-readable format
findmnt : Show all mounted filesystems and their mount points
mount [device] [mountpoint] : Mount a device to a directory (mount point)

PROCESS RELATED
bg : Resume a suspended job in the background
clear : Clear the terminal screen
fg [job] : Bring a background job to the foreground
kill [process_id] : Terminate a process by its PID
pkill [process_name] : Terminate processes by name
killall [process_name] : Terminate all processes matching the given name
lsof : List open files and the processes using them
trap "[commands]" [signal] : Run commands when the specified signal is received
nohup [command] & : Run a command immune to hangups, in the background
pmap : Show memory usage of a process
ps : Show a snapshot of active processes
pstree : Show processes as a tree
top : Show real-time system processes and resource usage
wait : Wait for a process to complete
nice : Start a process with a given priority
ps -p [PID] : Show the status of a specific process
renice : Change the priority of a running process

SHELL COMMAND
alias [alias]='[command]' : Create a command alias
at [hh:mm] : Schedule a one-time job at a specific time
history : Print command history
jobs : Display current jobs and their status
man [command] : Display the manual page for a command
unalias [alias] : Remove an alias
watch -n [interval] [command] : Run a command repeatedly at fixed intervals
sleep [interval] && [command] : Delay execution of a command

SEARCHING
find [location] -name "[pattern]" : Search for files matching a name pattern
find [location] -size +100M : Find files larger than 100MB
grep [pattern] [file] : Search for a pattern in a file
grep -r [pattern] [directory] : Search for a pattern recursively in all files within a directory
locate [name] : Search for files and directories by name (using a database)
which [command] : Show the full path of a command
whereis [command] : Locate the binary, source, and manual page files for a command

SHORTCUT KEYS
!! : Repeat the last command
exit : Log out of the session

Ctrl + A : Move the cursor to the beginning of the line
Ctrl + E : Move the cursor to the end of the line
Ctrl + C : Interrupt/terminate the current process
Ctrl + D : Log out of the session or send EOF (end-of-file)
Ctrl + G : Cancel the current search or operation
Ctrl + H : Delete the character before the cursor (like Backspace)
Ctrl + K : Cut (kill) the text after the cursor
Ctrl + L : Clear the screen (same as the 'clear' command)
Ctrl + N : Recall the next command in history
Ctrl + O : Execute the current command in history and continue searching
Ctrl + P : Recall the previous command in history
Ctrl + Q : Resume terminal output (after Ctrl+S)
Ctrl + R : Search backward through command history
Ctrl + S : Pause terminal output (can be resumed with Ctrl+Q)
Ctrl + T : Swap the last two characters before the cursor
Ctrl + U : Cut (kill) the text before the cursor
Ctrl + W : Cut (kill) the word before the cursor
Ctrl + Y : Paste the most recently cut (yanked) text
Ctrl + Z : Suspend the current process (resume with fg/bg)

Alt + B : Move back one word
Alt + D : Delete the word after the cursor
Alt + F : Move forward one word
Alt + U : Uppercase from cursor to end of word
Alt + L : Lowercase from cursor to end of word
Alt + . : Insert the last argument from the previous command

Ctrl + Alt + F1 to F6 : Switch to virtual consoles (TTYs)
Ctrl + Alt + F7 (or F1/F2 on modern distros) : Switch back to the graphical session

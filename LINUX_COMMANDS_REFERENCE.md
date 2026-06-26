# Linux Commands Reference Guide 🐧

A comprehensive guide to essential Linux commands with examples and explanations. Perfect for beginners and intermediate users.

**Table of Contents**
- [Navigation & File Viewing](#navigation--file-viewing)
- [File Operations](#file-operations)
- [System Monitoring](#system-monitoring)
- [User & Group Management](#user--group-management)
- [Network Commands](#network-commands)
- [Package Management](#package-management)
- [Text Editors](#text-editors)
- [Archive & Backup](#archive--backup)
- [File Permissions](#file-permissions)
- [Additional Utilities](#additional-utilities)
- [Quick Tips](#quick-tips)

---

## Navigation & File Viewing

### 1. `pwd` - Print Working Directory
**Purpose:** Shows the full path of the current folder you're in
```bash
pwd
# Output: /home/user/documents
```

### 2. `cd` - Change Directory
**Purpose:** Navigate to a different folder
```bash
cd /var              # Go to /var directory
cd ..                # Go to parent directory
cd ~                 # Go to home directory
cd -                 # Go back to previous directory
```

### 3. `ls` - List
**Purpose:** Shows files and folders in current directory
```bash
ls                   # Simple listing
ls -l                # Detailed listing (long format)
ls -la               # Detailed + hidden files
ls -h                # Human-readable file sizes
ls -S                # Sort by file size
```

### 4. `cat` - Concatenate
**Purpose:** Display entire file contents on screen
```bash
cat file.txt         # Display file content
cat file1 file2      # Display multiple files
cat file.txt | grep error  # Find lines with "error"
```

### 5. `more` - More Pager
**Purpose:** Display file contents page-by-page
```bash
more file.txt        # View file page by page
# Use Space for next page, 'b' for previous, 'q' to quit
```

### 6. `head` - Show File Beginning
**Purpose:** Show first N lines of a file
```bash
head file.txt        # Show first 10 lines (default)
head -20 file.txt    # Show first 20 lines
head -5 file.txt     # Show first 5 lines
```

### 7. `tail` - Show File End
**Purpose:** Show last N lines of a file
```bash
tail file.txt        # Show last 10 lines (default)
tail -20 file.txt    # Show last 20 lines
tail -f file.txt     # Follow file in real-time (useful for logs)
tail -20f file.txt   # Show last 20 lines and follow
```

### 8. `grep` - Global Regular Expression Print
**Purpose:** Search for text patterns in files
```bash
grep "error" file.txt              # Find lines with "error"
grep -i "error" file.txt           # Case-insensitive search
grep -r "error" /path/             # Recursively search in folder
cat file.txt | grep "failed"       # Search in piped output
grep -v "error" file.txt           # Show lines WITHOUT "error"
grep -c "error" file.txt           # Count matching lines
```

### 9. `history` - Command History
**Purpose:** Shows list of all previously executed commands
```bash
history              # Show all command history
history 10           # Show last 10 commands
!50                  # Execute command #50 from history
!!                   # Execute previous command again
```

---

## File Operations

### 10. `mkdir` - Make Directory
**Purpose:** Create a new folder
```bash
mkdir newfolder           # Create single folder
mkdir -p path/to/folder   # Create nested folders
mkdir folder1 folder2     # Create multiple folders
```

### 11. `touch` - Create Empty File
**Purpose:** Create an empty file or update timestamp
```bash
touch file.txt            # Create empty file
touch file1 file2 file3   # Create multiple files
```

### 12. `cp` - Copy
**Purpose:** Copy files or folders
```bash
cp source.txt destination.txt        # Copy file
cp -r folder1 folder2                # Copy folder recursively
cp file.txt /path/to/destination/    # Copy to another directory
cp -v file.txt file_backup.txt       # Copy with verbose output
```

### 13. `mv` - Move/Rename
**Purpose:** Move or rename files
```bash
mv oldname.txt newname.txt           # Rename file
mv file.txt /path/to/destination/    # Move file
mv folder1 folder2                   # Move/rename folder
```

### 14. `rm` - Remove
**Purpose:** Delete files permanently
```bash
rm file.txt                 # Delete file
rm file1.txt file2.txt      # Delete multiple files
rm -r folder                # Delete folder and contents
rm -rf folder               # Force delete folder
rm -i file.txt              # Interactive - ask for confirmation
```

### 15. `vi` / `vim` - Text Editor
**Purpose:** Text editor for creating/editing files
```bash
vi file.txt                 # Open file in vi editor

# Basic commands:
# i = Insert mode (type text)
# Esc = Exit insert mode
# :wq = Save and quit
# :q! = Quit without saving
# :w = Save only
# dd = Delete line
# u = Undo
```

---

## System Monitoring

### 16. `df` - Disk Free
**Purpose:** Shows disk space usage of all mounted filesystems
```bash
df               # Show disk usage in blocks
df -h            # Human-readable format (GB/MB)
df -m            # Show in MB
df -i             # Show inode usage
```

### 17. `free` - Free Memory
**Purpose:** Shows RAM usage
```bash
free             # Show memory in KB
free -h          # Human-readable format
free -m          # Show in MB
free -g          # Show in GB
free -t          # Show total row
```

### 18. `du` - Disk Usage
**Purpose:** Shows size of files/directories
```bash
du folder        # Show folder size
du -h folder     # Human-readable format
du -sh folder    # Show summary (total only)
du -s *          # Show size of each item in current directory
```

### 19. `ps` - Process Status
**Purpose:** Lists running processes
```bash
ps               # Show processes for current user
ps -ef           # Show all processes with details
ps -aux          # Show all processes (BSD format)
ps -ef | grep nginx  # Find specific process
```

### 20. `top` - Real-time Process Monitor
**Purpose:** Real-time monitoring of processes and system resources
```bash
top              # Interactive real-time monitoring
top -n 1         # Show once and exit
# Press 'q' to quit, 'k' to kill process, 'M' to sort by memory
```

### 21. `htop` - Enhanced Process Monitor
**Purpose:** Improved version of `top` with better interface
```bash
htop             # Launch interactive monitor
# Use arrow keys to navigate, 'k' to kill, 'q' to quit
# Better interface than top
```

### 22. `uptime` - System Uptime
**Purpose:** Shows how long the system has been running
```bash
uptime
# Output: 12:30:45 up 5 days, 3:12, 2 users, load average: 0.15, 0.10, 0.08
```

### 23. `uname` - Unix Name
**Purpose:** Shows system information
```bash
uname            # Show kernel name
uname -a         # Show all info (kernel, version, architecture, OS)
uname -s         # Show kernel name
uname -r         # Show kernel release
uname -m         # Show hardware platform
```

### 24. `hostname` - System Hostname
**Purpose:** Shows the computer's network name
```bash
hostname         # Show hostname
hostname -i      # Show IP address
sudo hostnamectl set-hostname newname  # Change hostname
```

---

## User & Group Management

### 25. `whoami` - Current User
**Purpose:** Shows the currently logged-in username
```bash
whoami
# Output: john
```

### 26. `w` - Logged in Users Activity
**Purpose:** Shows who is logged in and what they're doing
```bash
w
# Shows detailed info about logged-in users
```

### 27. `who` - Logged in Users
**Purpose:** Simpler version of `w`, shows logged-in users
```bash
who
# Output: john  tty1  2024-01-15 09:00
```

### 28. `adduser` - Add User
**Purpose:** Create a new user account
```bash
sudo adduser john           # Interactive user creation
# Prompts for password and user details
```

### 29. `passwd` - Change Password
**Purpose:** Change password for a user
```bash
passwd                      # Change your own password
sudo passwd john            # Change john's password
sudo passwd -l john         # Lock user account
sudo passwd -u john         # Unlock user account
```

### 30. `userdel` - Delete User
**Purpose:** Delete/remove a user account
```bash
sudo userdel john           # Delete user (keep home directory)
sudo userdel -r john        # Delete user and home directory
```

### 31. `addgroup` - Add Group
**Purpose:** Create a new user group
```bash
sudo addgroup developers    # Create new group
sudo addgroup dev           # Create 'dev' group
```

### 32. `usermod` - Modify User
**Purpose:** Modify user properties
```bash
sudo usermod -a -G dev john         # Add john to 'dev' group
sudo usermod -g groupname john      # Change primary group
sudo usermod -s /bin/bash john      # Change shell
sudo usermod -d /home/newdir john   # Change home directory
```

### 33. `getent` - Get Entries
**Purpose:** View user/group database
```bash
getent passwd               # Show all users
getent group                # Show all groups
getent group dev            # Show members of 'dev' group
```

### 34. `cat /etc/passwd` - View Users File
**Purpose:** Shows all user accounts on system
```bash
cat /etc/passwd
# Format: username:password:UID:GID:gecos:home:shell
```

### 35. `cat /etc/shadow` - View Password Hashes
**Purpose:** Shows password hashes (only root can view)
```bash
sudo cat /etc/shadow
# ⚠️ Warning: Only root can read this file
```

### 36. `cat /etc/group` - View Groups File
**Purpose:** Shows all groups and their members
```bash
cat /etc/group
# Format: groupname:password:GID:userlist
```

### 37. `chage` - Change Password Age
**Purpose:** Manage password expiry and aging policies
```bash
sudo chage john                     # Interactive mode
sudo chage -l john                  # List password aging
sudo chage -M 90 john               # Set max days to 90
sudo chage -m 1 john                # Set min days to 1
sudo chage -W 7 john                # Warn 7 days before expiry
```

---

## Network Commands

### 38. `ping` - Test Connectivity
**Purpose:** Test if host is reachable
```bash
ping google.com              # Ping domain
ping 8.8.8.8                 # Ping IP address
ping -c 4 google.com         # Send 4 ping packets
ping -i 2 google.com         # Wait 2 seconds between pings
```

### 39. `curl` - Fetch URLs
**Purpose:** Fetch data from web URLs
```bash
curl https://google.com              # Fetch webpage
curl -I https://google.com           # Fetch headers only
curl ifconfig.me                     # Show your public IP
curl -O https://example.com/file.zip # Download file
```

### 40. `ifconfig` - Network Interface Configuration
**Purpose:** Show IP address, MAC address, network interface details
```bash
ifconfig                    # Show all interfaces
ifconfig eth0               # Show specific interface
sudo ifconfig eth0 down     # Disable interface
sudo ifconfig eth0 up       # Enable interface
```

### 41. `netstat` - Network Statistics
**Purpose:** Show active connections, listening ports, routing table
```bash
netstat                     # Show all connections
netstat -a                  # Show all sockets (listening + established)
netstat -an                 # Show numeric IP addresses
netstat -l                  # Show listening ports
netstat -tulpn              # Show TCP/UDP ports with programs
```

### 42. `ss` - Socket Statistics
**Purpose:** Modern replacement for netstat
```bash
ss                          # Show all sockets
ss -a                       # Show all sockets (listening + established)
ss -l                       # Show listening sockets
ss -tulpn                   # Show TCP/UDP ports with programs
ss -s                       # Show socket statistics summary
```

### 43. `nslookup` - DNS Lookup
**Purpose:** Query DNS servers to get IP address from domain
```bash
nslookup google.com         # Get IP of google.com
nslookup 8.8.8.8            # Reverse DNS lookup
nslookup google.com 1.1.1.1 # Query specific DNS server
```

### 44. `dig` - Domain Information Groper
**Purpose:** Detailed DNS lookup showing all DNS records
```bash
dig google.com              # Get all DNS records
dig google.com A            # Get A record only
dig google.com MX           # Get Mail Exchange records
dig -x 8.8.8.8              # Reverse DNS lookup
```

### 45. `route` - Routing Table
**Purpose:** Show or manage routing table
```bash
route                       # Show routing table
route -n                    # Show numeric IP addresses
sudo route add default gw 192.168.1.1  # Add default gateway
```

### 46. `traceroute` - Trace Network Path
**Purpose:** Shows path/hops packets take to reach destination
```bash
traceroute google.com       # Trace route to google.com
traceroute -m 15 google.com # Max 15 hops
traceroute -I google.com    # Use ICMP instead of UDP
```

### 47. `whois` - Domain Lookup
**Purpose:** Shows domain registration info and owner details
```bash
whois google.com            # Get domain info
whois 8.8.8.8               # Get IP owner info
```

### 48. `ifplugstatus` - Network Cable Status
**Purpose:** Check if network cable is connected/disconnected
```bash
ifplugstatus                # Show cable status
ifplugstatus eth0           # Check specific interface
```

---

## Package Management

### 49. `apt-get` - Package Manager (Legacy)
**Purpose:** Debian/Ubuntu package manager for installing/removing software
```bash
sudo apt-get update                 # Update package list
sudo apt-get install nginx          # Install package
sudo apt-get remove nginx           # Remove package
sudo apt-get upgrade                # Upgrade all packages
sudo apt-get dist-upgrade           # Major upgrade
sudo apt-get autoremove             # Remove unused packages
```

### 50. `apt` - Package Manager (Modern)
**Purpose:** Newer version of apt-get with simplified syntax
```bash
sudo apt update                     # Update package list
sudo apt install nginx              # Install package
sudo apt remove nginx               # Remove package
sudo apt upgrade                    # Upgrade packages
sudo apt search nginx               # Search for package
sudo apt show nginx                 # Show package details
```

---

## User Switching

### 51. `su` - Switch User
**Purpose:** Switch to another user account
```bash
su - john                   # Switch to john (login shell)
su john                     # Switch to john (non-login shell)
sudo su -                   # Switch to root with sudo
exit                        # Exit switched user and return
```

### 52. `sudo` - Super User Do
**Purpose:** Execute command with admin/root privileges
```bash
sudo apt install nginx              # Run command as root
sudo -i                             # Launch root shell
sudo -u username command            # Run as specific user
sudo !!                             # Run previous command as root
```

---

## Text Editors

### 53. `vi` / `vim` - Vi Editor
**Purpose:** Text editor for creating/editing files

**Basic Commands:**
```bash
# Entering insert mode:
i       # Insert before cursor
a       # Insert after cursor
o       # New line below
O       # New line above

# Exit insert mode:
Esc     # Return to command mode

# Saving & quitting:
:w      # Save file
:q      # Quit
:wq     # Save and quit
:q!     # Quit without saving
:x      # Save and quit

# Editing:
dd      # Delete line
u       # Undo
Ctrl+r  # Redo
yy      # Copy line
p       # Paste
```

---

## Archive & Backup

### 54. `tar` - Tape Archive
**Purpose:** Create/extract compressed archives
```bash
# Create archive:
tar -cvf archive.tar folder/            # Create tar
tar -czvf archive.tar.gz folder/        # Create compressed (gzip)
tar -cjvf archive.tar.bz2 folder/       # Create compressed (bzip2)

# Extract archive:
tar -xvf archive.tar                    # Extract tar
tar -xzvf archive.tar.gz                # Extract gzip
tar -xjvf archive.tar.bz2               # Extract bzip2

# Options:
-c = create
-x = extract
-v = verbose (show files)
-f = filename
-z = gzip compression
-j = bzip2 compression
-l = preserve links
```

---

## File Permissions

### 55. `chmod` - Change Mode (Permissions)
**Purpose:** Change file/folder read/write/execute permissions

**Numeric Format:**
```bash
chmod 755 script.sh          # rwxr-xr-x (execute)
chmod 644 file.txt           # rw-r--r-- (read/write)
chmod 777 file.txt           # rwxrwxrwx (full access)
chmod 000 file.txt           # --------- (no access)
chmod -R 755 folder/         # Recursive change
```

**Letter Format:**
```bash
chmod +x script.sh           # Add execute permission
chmod -x script.sh           # Remove execute permission
chmod +r file.txt            # Add read permission
chmod +w file.txt            # Add write permission
chmod u+x script.sh          # Add execute for user
chmod g+r file.txt           # Add read for group
chmod o-r file.txt           # Remove read for others
```

### 56. `chown` - Change Owner
**Purpose:** Change file/folder owner and group
```bash
sudo chown john file.txt                    # Change owner
sudo chown john:dev file.txt                # Change owner and group
sudo chown -R john:dev folder/              # Recursive change
```

---

## Additional Utilities

### 57. `echo` - Print Text
**Purpose:** Print text on screen or to file
```bash
echo "Hello World"           # Print text
echo $PATH                   # Print environment variable
echo "text" > file.txt       # Write to file
echo "text" >> file.txt      # Append to file
```

### 58. `man` - Manual Pages
**Purpose:** Display help documentation for commands
```bash
man ls                       # Show manual for ls command
man -k keyword               # Search for keyword
man 5 passwd                 # Show manual section 5 for passwd
```

### 59. `which` - Find Command Location
**Purpose:** Show where a command is located
```bash
which python                 # Show python location
which java                   # Show java location
```

### 60. `find` - Find Files
**Purpose:** Search for files in directory tree
```bash
find / -name "filename"              # Find file by name
find /home -type f -name "*.txt"     # Find all .txt files
find /home -type d -name "folder"    # Find directories
find /home -size +100M               # Find files larger than 100MB
```

---

## Quick Tips & Tricks

### Pipe Operator (|)
Combine commands by sending output of one to another:
```bash
cat file.txt | grep "error"          # Search in file
ps -ef | grep nginx                  # Find specific process
ls -l | wc -l                        # Count files
```

### Redirection
```bash
command > file.txt                   # Redirect output to file (overwrite)
command >> file.txt                  # Append to file
command < file.txt                   # Use file as input
command 2> error.txt                 # Redirect errors to file
```

### Multiple Commands
```bash
command1 ; command2                  # Run commands one after another
command1 && command2                 # Run command2 only if command1 succeeds
command1 || command2                 # Run command2 only if command1 fails
```

### Useful Shortcuts
```bash
Ctrl + C                    # Kill running command
Ctrl + Z                    # Suspend command (use 'fg' to resume)
Ctrl + L                    # Clear screen
Ctrl + A                    # Go to beginning of line
Ctrl + E                    # Go to end of line
Ctrl + R                    # Search command history
Tab                         # Auto-complete command/filename
!!                          # Run previous command
!$                          # Last argument of previous command
```

### File Globbing (Wildcards)
```bash
*                           # Match any characters
?                           # Match single character
[abc]                       # Match a, b, or c
[a-z]                       # Match any letter
{file1,file2}               # Match file1 or file2
```

---

## Learning Path

**Beginner (Start here):**
1. Navigation: `pwd`, `cd`, `ls`, `mkdir`, `rmdir`
2. File viewing: `cat`, `head`, `tail`, `more`
3. File operations: `cp`, `mv`, `rm`, `touch`
4. System info: `uname`, `hostname`, `whoami`

**Intermediate:**
5. Text search: `grep`, `find`
6. System monitoring: `df`, `free`, `ps`, `top`
7. User management: `adduser`, `passwd`, `usermod`
8. Permissions: `chmod`, `chown`

**Advanced:**
9. Network tools: `ifconfig`, `netstat`, `ping`, `traceroute`
10. Archives: `tar`
11. Text editing: `vi`/`vim`
12. Package management: `apt`, `apt-get`

---

## Troubleshooting Tips

| Problem | Solution |
|---------|----------|
| Command not found | Check spelling, or use `which` to find it |
| Permission denied | Use `sudo` or check file permissions with `ls -l` |
| Disk full | Use `df -h` to find culprit, then `du -h` to check folders |
| Slow system | Use `top` to check CPU/RAM, `ps -ef` to find process |
| Can't access file | Check permissions with `ls -l`, change with `chmod` |
| Lost in directory | Use `pwd` to see where you are, `cd /` to go to root |

---

## Resources

- [Linux Manual Pages](https://man7.org/)
- [Ubuntu Documentation](https://help.ubuntu.com/)
- [GNU Coreutils](https://www.gnu.org/software/coreutils/manual/)

---

**Last Updated:** January 2025  
**Total Commands:** 60  
**License:** MIT  
**Author:** Your Name

---

## Contributing

Feel free to submit issues and enhancement requests to improve this guide!

```
Happy Learning! 🚀
```

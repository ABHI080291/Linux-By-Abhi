# Linux-Command

**NAVIGATION & FILE VIEWING (9 Commands)
#CommandWhat it does**

1 pwd - Print Working Directory - Shows the full path of the current folder you're in

2 cd - Change Directory - Navigate to a different folder (e.g., cd /var, cd .., cd ~)

3 ls - List - Shows files and folders in current directory. Options: ls -la (detailed), ls -h (human readable)

4 cat - Concatenate - Display entire file contents on screen (e.g., cat file.txt)

5 more - More - Display file contents page-by-page (press Space for next page, Q to quit)

6 head - Head - Show first N lines of a file (e.g., head -20 file.txt shows first 20 lines)

7 tail - Tail - Show last N lines of a file (e.g., tail -20 file.txt shows last 20 lines)

8 grep - Global Regular Expression Print - Search for text patterns in files (e.g., cat file.txt | grep error finds lines with "error")

9 history -  History - Shows list of all previously executed commands with line numbers

**FILE OPERATIONS (6 Commands)**

10 mkdir - Make Directory - Create a new folder (e.g., mkdir newfolder)

11 touch - Touch - Create an empty file (e.g., touch file.txt)

12 cp - Copy - Copy files or folders (e.g., cp source.txt destination.txt, cp -r folder1 folder2)

13 mv - Move - Move or rename files (e.g., mv oldname.txt newname.txt)

14 rm - Remove - Delete files permanently (e.g., rm file.txt, rm -rf folder to delete folder with contents)

15 vi/vim - Vi Editor - Text editor for creating/editing files (press i to insert, Esc to exit, :wq to save)


**SYSTEM MONITORING (9 Commands)** 

16 df-  Disk Free - Shows disk space usage of all mounted filesystems (e.g., df -h shows in human-readable format like GB/MB)

17 free - Free Memory - Shows RAM usage (total, used, available). Options: free -h (human readable), free -m (MB), free -g (GB)

18 du - Disk Usage - Shows size of files/directories (e.g., du -h folder shows folder size in human readable format)

19 ps - Process Status - Lists running processes. ps -ef shows all processes with details (PID, user, command)

20 top - Top - Real-time monitoring of processes and system resources (CPU, RAM usage). Press Q to quit

21 htop - HTop - Improved version of top with better interface and interactive controls

22 uptime - Uptime - Shows how long the system has been running since last restart

23 uname Unix Name - Shows system information. uname -a displays all info (kernel name, version, hardware platform)

24 hostname - Hostname - Shows the computer's network name. hostname -i shows IP address

**USER & GROUP MANAGEMENT (8 Commands)**

25 whoami - Who Am I - Shows the currently logged-in username

26 w - Who - Shows who is logged in and what they're doing on the system

27 who - Who - Simpler version of w, shows logged-in users

28 adduser - Add User - Create a new user account (interactive, asks for password) (e.g., adduser john)

29 passwd - Password - Change password for a user (e.g., passwd username to change someone's password)

30 userdel - User Delete - Delete/remove a user account (e.g., userdel john removes user john)

31 addgroup - Add Group - Create a new user group (e.g., addgroup developers creates developers group)

32 usermod - User Modify - Modify user properties (e.g., usermod -a -G dev shalini adds shalini to dev group)


**USER & GROUP FILE VIEWING (4 Commands)**
#CommandWhat it does33getentGet Entries - View user/group database (e.g., getent group shows all groups, getent passwd shows all users)34cat /etc/passwdShows all user accounts on system (contains: username, UID, GID, home directory, shell)35cat /etc/shadowShows password hashes (only root can view). Contains encrypted passwords and age info36cat /etc/groupShows all groups and their members

PASSWORD & ACCOUNT POLICIES (1 Command)
#CommandWhat it does37chageChange Age - Manage password expiry and aging policies (e.g., chage shalini shows/changes password expiry for shalini)

NETWORK TOOLS (2 Commands)
#CommandWhat it does38pingPing - Test connectivity to a host (e.g., ping google.com checks if google.com is reachable)39curlClient URL - Fetch data from web URLs (e.g., curl ifconfig.me shows your public IP address)

PACKAGE MANAGEMENT (2 Commands)
#CommandWhat it does40apt-getAPT Get - Debian/Ubuntu package manager for installing/removing software (e.g., apt-get update updates package list, apt-get install nginx installs nginx)41aptAPT - Newer version of apt-get with simplified syntax (e.g., apt install nginx)

USER SWITCHING (1 Command)
#CommandWhat it does42suSwitch User - Switch to another user account (e.g., su aditya switches to aditya user, needs password)

ARCHIVE/BACKUP (1 Command)
#CommandWhat it does43tarTape Archive - Create/extract compressed archives. tar -cvf file.tar folder (create), tar -xvf file.tar (extract). Options: -c create, -x extract, -v verbose, -f filename

MISCELLANEOUS (1 Command)
#CommandWhat it does44echoEcho - Print text on screen (e.g., echo "Hello World" displays Hello World)

BONUS: ADVANCED OPTIONS YOU USED

tail -20f = Follow file in real-time (useful for log monitoring)
grep fail = Search for lines containing "fail"
ps -ef | grep jbd2 = Pipe output of one command to another (find specific process)
mkdir rakesh ; touch myfiles/{a.txt,b.txt,c.txt} = Multiple commands in one line
rm -rf folder = Force remove folder with all contents


**Top 50 Linux Interview Questions and Answers**

1. What is Linux?
Answer:
Linux is an open-source operating system used to run servers, desktops and cloud systems.

3. What is Kernel?
Answer:
Kernel is the core of Linux. It manages CPU, memory, devices and processes.

5. What is Shell?
Answer:
Shell is a command-line interface that lets users interact with the kernel.

7. Linux boot process?
Answer:
BIOS/UEFI -> GRUB -> Kernel -> systemd/init -> Services -> Login.

9. Linux architecture?
Answer:
Hardware, Kernel, Shell, Applications.

11. File system hierarchy?
Answer:
/ root, /home users, /etc config, /var logs, /tmp temp, /opt apps.

13. Hard vs Soft link?
Answer:
Hard link shares inode; soft link points to path and breaks if target is removed.

15. File permissions?
Answer:
Read(r), Write(w), Execute(x) for owner, group and others.

17. chmod?
Answer:
Changes file permissions. Example: chmod 755 file

19. chown?
Answer:
Changes file owner. Example: chown user:user file

21. SUID?
Answer:
Runs file with owner's permissions.

23. SGID?
Answer:
Runs with group's permissions or inherits group on directories.

25. Sticky Bit?
Answer:
Only file owner can delete files in shared directory like /tmp.

27. Create user?
Answer:
useradd username then passwd username.

29. Process?
Answer:
A running program.

31. Thread?
Answer:
A lightweight unit inside a process.

33. Zombie process?
Answer:
Finished child process waiting for parent to collect exit status.

35. Orphan process?
Answer:
Child whose parent exited; adopted by init/systemd.

37. Daemon process?
Answer:
Background service like sshd.

39. Find process?
Answer:
ps -ef | grep name or pgrep name.

41. Kill process?
Answer:
kill PID, use kill -9 only if needed.

43. Check CPU?
Answer:
top or htop.

45. Check memory?
Answer:
free -h.

47. Check disk?
Answer:
df -h.

49. Find large files?
Answer:
du -sh * or find / -size +500M.

51. Inode?
Answer:
Stores file metadata. If inodes are full, new files cannot be created.

53. LVM?
Answer:
Logical Volume Manager allows flexible disk resizing.

55. Swap?
Answer:
Disk space used when RAM is full.

57. Check logs?
Answer:
journalctl or /var/log.

59. Service status?
Answer:
systemctl status service.

61. Restart service?
Answer:
systemctl restart service.

63. Network IP?
Answer:
ip addr.

65. Open ports?
Answer:
ss -tuln.

67. DNS check?
Answer:
nslookup or dig.

69. TCP vs UDP?
Answer:
TCP is reliable; UDP is faster without guaranteed delivery.

71. Cron?
Answer:
Schedules jobs automatically.

73. Environment variable?
Answer:
Stores system/user values. View with printenv.

75. Package install?
Answer:
apt install or yum/dnf install.

77. Server slow?
Answer:
Check CPU, memory, disk, logs and processes.

79. Disk full?
Answer:
Use df -h, du -sh, remove unwanted files.

81. Permission denied?
Answer:
Check ls -l, then chmod/chown.

83. Service not starting?
Answer:
Check systemctl status and journalctl -u service.

85. SSH not working?
Answer:
Check sshd service, firewall, logs and port 22.

87. High CPU?
Answer:
Use top, identify process, optimize or stop it.

89. High memory?
Answer:
Use free -h and top, identify memory-hungry process.

91. Hardware issue?
Answer:
Use dmesg, lscpu, lsblk, smartctl.

93. System performance?
Answer:
Use top, vmstat, iostat, free -h, df -h.

95. Debug error?
Answer:
Read logs, verify service, reproduce issue, fix root cause.

97. Filesystem read-only?
Answer:
Check dmesg, remount if safe, run fsck during maintenance.

99. Best troubleshooting approach?
Answer:
Understand issue, check logs, services, CPU, memory, disk, network, fix and validate.

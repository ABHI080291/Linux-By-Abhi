# 🐧 Linux Commands Reference Guide

A **comprehensive, beginner-friendly** guide to 60+ essential Linux commands with practical examples and detailed explanations. Perfect for anyone learning Linux from scratch.

![Linux](https://img.shields.io/badge/Linux-Important-red)
![Commands](https://img.shields.io/badge/Commands-60%2B-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)

---

## 📖 Features

✅ **60+ Essential Linux Commands**  
✅ **Organized by Categories** (Navigation, Files, System, Network, User Management, etc.)  
✅ **Practical Examples** for every command  
✅ **Quick Tips & Tricks** section  
✅ **Beginner to Advanced** learning path  
✅ **Troubleshooting Guide** for common issues  
✅ **Easy to Read** Markdown format  
✅ **Regularly Updated**

---

## 📚 Table of Contents

- [Navigation & File Viewing](#navigation--file-viewing) (9 commands)
- [File Operations](#file-operations) (6 commands)
- [System Monitoring](#system-monitoring) (9 commands)
- [User & Group Management](#user--group-management) (13 commands)
- [Network Commands](#network-commands) (11 commands)
- [Package Management](#package-management) (2 commands)
- [User Switching](#user-switching) (2 commands)
- [Text Editors](#text-editors) (1 command)
- [Archive & Backup](#archive--backup) (1 command)
- [File Permissions](#file-permissions) (2 commands)
- [Additional Utilities](#additional-utilities) (3 commands)
- [Quick Tips & Tricks](#quick-tips--tricks)
- [Learning Path](#learning-path)

---

## 🚀 Quick Start

### View the Full Guide

```bash
# Clone this repository
git clone https://github.com/yourusername/linux-commands-guide.git

# Navigate to repository
cd linux-commands-guide

# View the guide
cat LINUX_COMMANDS_REFERENCE.md

# Or open in your favorite editor
vim LINUX_COMMANDS_REFERENCE.md
```

### Commands by Priority

**🔴 CRITICAL (Learn First)**
- `pwd`, `cd`, `ls` - Navigation
- `cat`, `grep` - File viewing & search
- `mkdir`, `touch`, `rm` - File operations
- `sudo` - Admin privileges

**🟡 VERY IMPORTANT**
- `df`, `free`, `ps`, `top` - System monitoring
- `adduser`, `passwd`, `usermod` - User management
- `chmod` - File permissions
- `apt`, `apt-get` - Package management

**🟠 IMPORTANT**
- `ping`, `ifconfig`, `netstat` - Network tools
- `tar` - Archiving
- `vi`/`vim` - Text editing

---

## 💡 Command Categories

### Navigation & File Viewing
Basic commands to navigate the filesystem and view file contents.

```bash
pwd                  # Show current directory
cd /path/to/dir      # Change directory
ls -la               # List files (detailed)
cat file.txt         # View file contents
grep "text" file     # Search for text in file
```

### System Monitoring
Monitor system resources like disk, memory, and running processes.

```bash
df -h                # Disk usage (human-readable)
free -h              # Memory usage
ps -ef               # List all processes
top                  # Real-time process monitor
uptime               # System uptime
```

### Network Commands
Network connectivity and troubleshooting tools.

```bash
ping google.com           # Test connectivity
ifconfig                  # Show network interfaces
netstat -tulpn            # Show network connections
traceroute google.com     # Trace network path
nslookup google.com       # DNS lookup
```

### User Management
Create and manage user accounts and permissions.

```bash
sudo adduser john         # Create new user
passwd john               # Change password
usermod -a -G dev john    # Add to group
chmod 755 script.sh       # Change permissions
```

---

## 📖 Full Command Reference

This repository contains a complete guide with:

- ✏️ **Detailed descriptions** of each command
- 📝 **Practical examples** showing real usage
- 🔧 **Command options** and flags
- 💬 **Sample output** for reference
- 📌 **Tips & tricks** for efficiency
- 🚨 **Warnings** for dangerous commands

### View Full Guide

👉 **[LINUX_COMMANDS_REFERENCE.md](./LINUX_COMMANDS_REFERENCE.md)** - Complete guide with all details

---

## 🎓 Learning Path

### Beginner Level (Week 1-2)
Start with these essential commands:
1. Navigation: `pwd`, `cd`, `ls`
2. File viewing: `cat`, `head`, `tail`
3. File operations: `mkdir`, `touch`, `cp`, `mv`, `rm`
4. System info: `uname`, `whoami`, `hostname`

### Intermediate Level (Week 3-4)
Expand your knowledge:
1. Text search: `grep`, `find`
2. System monitoring: `df`, `free`, `ps`, `top`
3. User management: `adduser`, `passwd`
4. Permissions: `chmod`, `chown`

### Advanced Level (Week 5+)
Master advanced topics:
1. Network tools: `ifconfig`, `netstat`, `netstat`, `traceroute`
2. Archives: `tar`
3. Text editing: `vi`/`vim`
4. Package management: `apt`, `apt-get`

---

## 🔍 Search Tips

To find a specific command in this guide:

1. **On GitHub**: Use Ctrl+F to search within the file
2. **Using grep**: 
   ```bash
   grep "command-name" LINUX_COMMANDS_REFERENCE.md
   ```
3. **Using less**:
   ```bash
   less LINUX_COMMANDS_REFERENCE.md
   # Then type / and search term
   ```

---

## 📋 Command Statistics

| Category | Count |
|----------|-------|
| Navigation & File Viewing | 9 |
| File Operations | 6 |
| System Monitoring | 9 |
| User & Group Management | 13 |
| Network Commands | 11 |
| Package Management | 2 |
| User Switching | 2 |
| Text Editors | 1 |
| Archive & Backup | 1 |
| File Permissions | 2 |
| Additional Utilities | 3 |
| **TOTAL** | **60+** |

---

## 🛠️ How to Use This Guide

### 1. **For Daily Reference**
Save this repository and refer to it while learning or working with Linux.

### 2. **For Interview Prep**
Use the organized structure to prepare for Linux/DevOps interviews.

### 3. **For Teaching**
Share this guide with friends or colleagues learning Linux.

### 4. **For Quick Lookup**
Use `grep` or `find` commands to quickly locate specific commands.

---

## ⚠️ Important Warnings

Some commands are **destructive** and can permanently delete data:

```bash
rm -rf /                    # ❌ DO NOT RUN - Deletes entire system!
mkfs.ext4 /dev/sda          # ❌ DO NOT RUN - Formats drive
dd if=/dev/zero of=/dev/sda # ❌ DO NOT RUN - Destroys data
```

**Always double-check before running commands with:**
- `sudo`
- `rm` with `-r` or `-f`
- `mkfs`, `dd`, `format` commands

---

## 🤝 Contributing

We welcome contributions! Here's how you can help:

### Add New Content
Want to add new commands? Follow the existing format and submit a PR.

### Steps to Contribute
1. Fork the repository
2. Create a branch (`git checkout -b feature/improvement`)
3. Make your changes
4. Commit (`git commit -am 'Add improvement'`)
5. Push (`git push origin feature/improvement`)
6. Open a Pull Request

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
MIT License

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, and distribute...
```

---

## 👤 Author

**Created for Linux learners everywhere** 🐧

- 📧 Contact: [your-email@example.com](mailto:abhivg4784@gmail.com)
- 💼 LinkedIn: [your-profile](https://linkedin.com/in/abhishekkumar-cloud)

---

## 🙏 Acknowledgments

- Inspired by real-world Linux usage
- Built from hands-on lab sessions
- Refined through community feedback

---

## 📚 Additional Resources

### Learning Platforms

- https://youtu.be/e01GGTKmtpc?si=Yq45QlZHJiGsaHg6
- https://youtu.be/29eDuMjsEF8?si=ipkfjI-GvADSGbQT
- [Linux Academy](https://linuxacademy.com/)
- [Udemy Linux Courses](https://www.udemy.com/courses/search/?q=linux)
- [Coursera Linux Courses](https://www.coursera.org/search?query=linux)


### Cheat Sheets
- [Linux Cheat Sheet](https://www.cheatsheet.guru/linux.html)
- [Command Line Cheat Sheet](https://www.git-tower.com/blog/command-line-cheat-sheet/)

---

## 📊 Repository Stats

- ⭐ **Stars**: Please star if you find this helpful!
- 🍴 **Forks**: Feel free to fork for personal use
- 📝 **Issues**: Report problems and suggestions
- 🔧 **Contributions**: All contributions welcome!

---


### FAQ

**Q: What Linux distribution is this for?**  
A: These commands work on all Linux distributions. Some package managers vary (apt vs yum), but core commands are universal.

**Q: Can I use this for interviews?**  
A: Yes! This guide is perfect for interview preparation. It covers all commonly asked Linux commands.

**Q: Are these commands safe?**  
A: Most commands are safe. Always be careful with `rm`, `mkfs`, and `dd`. This guide includes warnings.

**Q: How often is this updated?**  
A: We aim to update weekly with new examples and clarifications.

---

## 🎉 Getting Started

```bash
# 1. Clone the repository
git clone https://github.com/yourusername/linux-commands-guide.git

# 2. Navigate to directory
cd linux-commands-guide

# 3. Open the guide
cat LINUX_COMMANDS_REFERENCE.md

# 4. Star the repository ⭐
# (Click the star button on GitHub)

# 5. Share with others 🚀
```

---

## 📌 Latest Updates

- **v1.0.0** (June 2026) - Initial release with 60+ commands
- **v1.1.0** (Planned) - Add advanced networking section
- **v1.2.0** (Planned) - Add system administration section

---

**Happy Learning! 🚀**

Last updated: June 2026
Made with ❤️ for Linux learners

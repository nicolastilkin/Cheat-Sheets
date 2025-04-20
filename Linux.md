# 🐧 Linux

## 📁 File & Directory Commands

| Action                  | Command                     |
| ----------------------- | --------------------------- |
| List files              | `ls -l`                     |
| List hidden files       | `ls -a`                     |
| Change directory        | `cd <directory>`            |
| Go back one directory   | `cd ..`                     |
| Print working directory | `pwd`                       |
| Copy file               | `cp <source> <destination>` |
| Move or rename file     | `mv <source> <destination>` |
| Remove file             | `rm <file>`                 |
| Remove directory        | `rm -r <directory>`         |
| Create directory        | `mkdir <name>`              |
| Create empty file       | `touch <file>`              |

---

## 📄 File Viewing & Editing

| Action               | Command          |
| -------------------- | ---------------- |
| View file content    | `cat <file>`     |
| View with pagination | `less <file>`    |
| View start of file   | `head <file>`    |
| View end of file     | `tail <file>`    |
| Real-time log view   | `tail -f <file>` |
| Edit file with nano  | `nano <file>`    |
| Edit file with vim   | `vim <file>`     |

---

## 🔍 Search & Find

| Action               | Command                        |
| -------------------- | ------------------------------ |
| Find files           | `find /path -name "<name>"`    |
| Search inside files  | `grep "<text>" <file>`         |
| Recursive grep       | `grep -r "<text>" <directory>` |
| Find process by name | `ps aux | grep <name>`         |

---

## 🧪 File Permissions

| Action                | Command                   |
| --------------------- | ------------------------- |
| Show permissions      | `ls -l`                   |
| Change permissions    | `chmod 755 <file>`        |
| Change ownership      | `chown user:group <file>` |
| Add execute to script | `chmod +x <script.sh>`    |

---

## 👥 Users & Groups

| Action       | Command                   |
| ------------ | ------------------------- |
| Current user | `whoami`                  |
| Switch user  | `su - <username>`         |
| Become root  | `sudo -i`                 |
| Add user     | `sudo adduser <name>`     |
| Delete user  | `sudo deluser <name>`     |
| List users   | `cut -d: -f1 /etc/passwd` |

---

## 📦 Package Management

### Debian/Ubuntu (APT)
| Action           | Command                      |
| ---------------- | ---------------------------- |
| Update repos     | `sudo apt update`            |
| Upgrade packages | `sudo apt upgrade`           |
| Install package  | `sudo apt install <package>` |
| Remove package   | `sudo apt remove <package>`  |

### RHEL/CentOS (YUM/DNF)
| Action          | Command                                                      |
| --------------- | ------------------------------------------------------------ |
| Install package | `sudo yum install <package>` or `sudo dnf install <package>` |

---

## 📶 Networking

| Action             | Command                       |
| ------------------ | ----------------------------- |
| Show IP address    | `ip a` or `ifconfig`          |
| Check connectivity | `ping <host>`                 |
| DNS lookup         | `nslookup <domain>`           |
| Download file      | `wget <url>`                  |
| Network ports      | `netstat -tuln` or `ss -tuln` |

---

## 🧠 System Info

| Action             | Command         |
| ------------------ | --------------- |
| Show current time  | `date`          |
| Show system uptime | `uptime`        |
| Show system info   | `uname -a`      |
| Memory usage       | `free -h`       |
| Disk usage         | `df -h`         |
| Top processes      | `top` or `htop` |

---

## 🔥 Processes & Services

| Action                 | Command                           |
| ---------------------- | --------------------------------- |
| List all processes     | `ps aux`                          |
| Kill a process         | `kill <pid>`                      |
| Force kill             | `kill -9 <pid>`                   |
| Start service          | `sudo systemctl start <service>`  |
| Stop service           | `sudo systemctl stop <service>`   |
| Enable service on boot | `sudo systemctl enable <service>` |
| Check service status   | `sudo systemctl status <service>` |

---

## 🔁 Archive & Compression

| Action                 | Command                       |
| ---------------------- | ----------------------------- |
| Create tar.gz archive  | `tar -czvf file.tar.gz <dir>` |
| Extract tar.gz archive | `tar -xzvf file.tar.gz`       |
| Unzip .zip file        | `unzip file.zip`              |

---

## 📝 File Redirection & Pipes

| Action                  | Command                |
| ----------------------- | ---------------------- |
| Redirect output to file | `command > file`       |
| Append output to file   | `command >> file`      |
| Redirect stderr         | `command 2> error.log` |
| Pipe output             | `command1 \| command2` |
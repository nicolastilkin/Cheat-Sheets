# 🔴 RHEL

## 📦 Package Management with DNF/YUM

| Action                  | Command                      |
| ----------------------- | ---------------------------- |
| Update system           | `sudo dnf update`            |
| Install package         | `sudo dnf install <package>` |
| Remove package          | `sudo dnf remove <package>`  |
| Search for package      | `dnf search <package>`       |
| List installed packages | `dnf list installed`         |
| Clean cache             | `sudo dnf clean all`         |

> 🧠 Note: `dnf` is the modern replacement for `yum`. You can often use them interchangeably.

---

## 🔧 System Services (systemd)

| Action                 | Command                            |
| ---------------------- | ---------------------------------- |
| Start a service        | `sudo systemctl start <service>`   |
| Stop a service         | `sudo systemctl stop <service>`    |
| Restart a service      | `sudo systemctl restart <service>` |
| Enable service at boot | `sudo systemctl enable <service>`  |
| Disable service        | `sudo systemctl disable <service>` |
| Check service status   | `systemctl status <service>`       |

---

## 🔐 SELinux (Security-Enhanced Linux)

| Action                        | Command                  |
| ----------------------------- | ------------------------ |
| Check status                  | `sestatus`               |
| Set SELinux to permissive     | `sudo setenforce 0`      |
| Set SELinux to enforcing      | `sudo setenforce 1`      |
| View SELinux context of files | `ls -Z`                  |
| Change file context           | `chcon -t <type> <file>` |

> ⚠️ Permanent changes require modifying `/etc/selinux/config`.

---

## 🔥 Firewall (firewalld)

| Action              | Command                                             |
| ------------------- | --------------------------------------------------- |
| Check status        | `sudo systemctl status firewalld`                   |
| Start/Stop firewall | `sudo systemctl start/stop firewalld`               |
| Add port            | `sudo firewall-cmd --add-port=8080/tcp --permanent` |
| Add service         | `sudo firewall-cmd --add-service=http --permanent`  |
| Reload firewall     | `sudo firewall-cmd --reload`                        |
| List rules          | `sudo firewall-cmd --list-all`                      |

---

## 🧱 User & Group Management

| Action                 | Command                           |
| ---------------------- | --------------------------------- |
| Add user               | `sudo useradd <username>`         |
| Set password           | `sudo passwd <username>`          |
| Add user with home dir | `sudo adduser <username>`         |
| Delete user            | `sudo userdel <username>`         |
| Add to group           | `sudo usermod -aG <group> <user>` |
| List users             | `getent passwd`                   |
| List groups            | `getent group`                    |

---

## 🧠 System Info

| Action               | Command                   |
| -------------------- | ------------------------- |
| OS release           | `cat /etc/redhat-release` |
| Kernel version       | `uname -r`                |
| CPU info             | `lscpu`                   |
| Memory info          | `free -h`                 |
| Disk usage           | `df -h`                   |
| Mounted file systems | `mount`                   |

---

## 🌐 Networking

| Action             | Command                                 |
| ------------------ | --------------------------------------- |
| Show IP address    | `ip a`                                  |
| Restart networking | `sudo systemctl restart NetworkManager` |
| View routes        | `ip r`                                  |
| Test connection    | `ping <host>`                           |
| DNS lookup         | `dig <domain>` or `nslookup <domain>`   |
| Check open ports   | `ss -tuln`                              |

---

## 🔁 Archives & Compression

| Action         | Command                               |
| -------------- | ------------------------------------- |
| Create tar.gz  | `tar -czvf file.tar.gz <dir>`         |
| Extract tar.gz | `tar -xzvf file.tar.gz`               |
| Extract .rpm   | `rpm2cpio <package>.rpm | cpio -idmv` |

---

## 🧰 RPM Package Management (Low-level)

| Action                   | Command                       |
| ------------------------ | ----------------------------- |
| Install .rpm file        | `sudo rpm -ivh <package>.rpm` |
| Remove package           | `sudo rpm -e <package>`       |
| Query installed packages | `rpm -qa`                     |
| Info about package       | `rpm -qi <package>`           |

---

## 📝 File Permissions

| Action             | Command                   |
| ------------------ | ------------------------- |
| Change owner       | `chown user:group <file>` |
| Change permissions | `chmod 755 <file>`        |
| View permissions   | `ls -l`                   |

---

## 🔧 Useful Tools

| Tool                 | Install Command              |
| -------------------- | ---------------------------- |
| curl                 | `sudo dnf install curl`      |
| wget                 | `sudo dnf install wget`      |
| git                  | `sudo dnf install git`       |
| htop                 | `sudo dnf install htop`      |
| net-tools (ifconfig) | `sudo dnf install net-tools` |
| unzip                | `sudo dnf install unzip`     |

---
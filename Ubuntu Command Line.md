# 🐧 Ubuntu Command Line

## 📦 Package Management (APT)

| Action                            | Command                                 |
| --------------------------------- | --------------------------------------- |
| Update package list               | `sudo apt update`                       |
| Upgrade installed packages        | `sudo apt upgrade`                      |
| Full upgrade (including removals) | `sudo apt full-upgrade`                 |
| Install a package                 | `sudo apt install <package>`            |
| Remove a package                  | `sudo apt remove <package>`             |
| Purge (remove with config files)  | `sudo apt purge <package>`              |
| Search for package                | `apt search <name>`                     |
| Show package info                 | `apt show <package>`                    |
| Clean up cache                    | `sudo apt autoremove && sudo apt clean` |

---

## 🐚 System Management (systemd)

| Action                 | Command                            |
| ---------------------- | ---------------------------------- |
| Check service status   | `sudo systemctl status <service>`  |
| Start a service        | `sudo systemctl start <service>`   |
| Stop a service         | `sudo systemctl stop <service>`    |
| Restart a service      | `sudo systemctl restart <service>` |
| Enable service at boot | `sudo systemctl enable <service>`  |
| Disable service        | `sudo systemctl disable <service>` |

---

## 🧱 Snap Package Manager

| Action               | Command                       |
| -------------------- | ----------------------------- |
| Find snaps           | `snap find <package>`         |
| Install snap         | `sudo snap install <package>` |
| Remove snap          | `sudo snap remove <package>`  |
| List installed snaps | `snap list`                   |
| Refresh snaps        | `sudo snap refresh`           |

---

## 🖥️ Ubuntu Desktop Shortcuts

| Action            | Shortcut                                 |
| ----------------- | ---------------------------------------- |
| Open terminal     | `Ctrl + Alt + T`                         |
| Open app launcher | `Super (Windows key)`                    |
| Lock screen       | `Super + L`                              |
| Switch workspaces | `Ctrl + Alt + Arrow keys`                |
| Screenshot        | `PrtSc` or `Shift + PrtSc` for selection |

---

## 🌐 Networking & Connectivity

| Action                 | Command                                                      |
| ---------------------- | ------------------------------------------------------------ |
| Show IP address        | `ip a` or `hostname -I`                                      |
| Test connectivity      | `ping <host>`                                                |
| Check open ports       | `ss -tuln`                                                   |
| Restart networking     | `sudo systemctl restart NetworkManager`                      |
| Connect to Wi-Fi (CLI) | `nmcli dev wifi` & `nmcli dev wifi connect <SSID> password <pass>` |

---

## 🛠 System Info & Hardware

| Action         | Command    |
| -------------- | ---------- |
| Kernel version | `uname -r` |
| CPU info       | `lscpu`    |
| Memory info    | `free -h`  |
| Disk usage     | `df -h`    |
| Block devices  | `lsblk`    |
| USB devices    | `lsusb`    |
| PCI devices    | `lspci`    |

---

## 🔐 Users, Groups, Permissions

| Action                | Command                            |
| --------------------- | ---------------------------------- |
| Create user           | `sudo adduser <username>`          |
| Add user to group     | `sudo usermod -aG <group> <user>`  |
| List groups           | `groups <username>`                |
| Change file ownership | `sudo chown <user>:<group> <file>` |
| Modify permissions    | `chmod 755 <file>`                 |

---

## 🧰 Common Tools

| Tool                             | Install                            |
| -------------------------------- | ---------------------------------- |
| curl                             | `sudo apt install curl`            |
| wget                             | `sudo apt install wget`            |
| git                              | `sudo apt install git`             |
| htop                             | `sudo apt install htop`            |
| net-tools (ifconfig, netstat)    | `sudo apt install net-tools`       |
| build-essential (compiler tools) | `sudo apt install build-essential` |

---

## 🧹 System Cleanup

| Action             | Command                       |
| ------------------ | ----------------------------- |
| Clean cache        | `sudo apt clean`              |
| Remove unused deps | `sudo apt autoremove`         |
| Remove old kernels | `sudo apt --purge autoremove` |

---

## 🔄 Software & Updates GUI

| Task                    | Location                               |
| ----------------------- | -------------------------------------- |
| Software Updater        | Applications Menu > Software Updater   |
| Additional Drivers      | Settings > About > Additional Drivers  |
| Change software sources | Applications Menu > Software & Updates |

---
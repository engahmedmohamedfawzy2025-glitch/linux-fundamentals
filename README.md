# Linux Fundamentals Documentation

This document contains clear and practical notes covering essential Linux administration skills.  
It is designed to help you revise, practice, and build a strong foundation.

---

# 📁 1. Linux File System & Navigation

## **1.1 Linux Directory Structure**
| Directory | Description |
|----------|-------------|
| `/` | Root directory of the entire system |
| `/home` | User home directories |
| `/etc` | Configuration files for services and system |
| `/var` | Logs and variable data (changes often) |
| `/bin` | Essential user commands (ls, cp, rm…) |
| `/usr` | User programs, binaries, and libraries |
| `/opt` | Optional third-party software |

---

## **1.2 Basic Navigation Commands**

ls              # list files
ls -l           # long detailed list
ls -a           # show hidden files
cd /path        # change directory
cd ..           # go up one directory
pwd             # show current directory path



1.3 File Operations

cp file1 file2          # copy file
mv file1 file2          # move/rename file
rm file.txt             # delete file
rm -r folder            # remove directory recursively
mkdir newfolder         # create folder
touch newfile           # create empty file


1.4 Viewing File Content

cat file.txt
head file.txt
tail file.txt
tail -f /var/log/syslog     # live log view
less file.txt               # scroll through file



👤 2. User & Group Management
2.1 Create, Modify, Delete Users

sudo useradd username
sudo passwd username            # set password
sudo userdel username
sudo userdel -r username        # delete with home directory

2.2 Group Management

sudo groupadd devops
sudo gpasswd -a user devops     # add user to group
groups username                 # view user groups

2.3 Modify User Properties
د
sudo usermod -aG sudo username   # add to sudo group
sudo usermod -d /new/home user   # change home directory
🔐 3. Permissions & Ownership

3.1 Permission Types
Symbol	Meaning
r	Read
w	Write
x	Execute

3.2 Numeric Permission Values
Permission	Value
r	4
w	2
x	1

3.3 Examples Using chmod

chmod 755 file    # rwx r-x r-x
chmod 644 file    # rw- r-- r--
chmod 700 file    # rwx --- ---
chmod 600 file    # rw- --- ---
3.4 Change File Ownership

sudo chown user file
sudo chown user:group file


🔧 4. Managing Services (systemctl)
4.1 Basic Service Commands

sudo systemctl start nginx
sudo systemctl stop nginx
sudo systemctl restart nginx
sudo systemctl status nginx

4.2 Enable or Disable Services at Boot

sudo systemctl enable nginx
sudo systemctl disable nginx


🌐 5. Networking Basics
5.1 Check Network Interfaces
ip a


5.2 View Routing Table

ip r


5.3 Test Connectivity
ping 8.8.8.8
ping google.com

5.4 Check Listening Ports
ss -tulnp


🖥️ 6. System Monitoring Commands

top             # CPU and memory usage
htop            # advanced monitor (if installed)
df -h           # disk usage
du -sh *        # folder sizes
free -h         # RAM usage
uptime          # load average

# Linux Fundamentals Documentation

Clear and practical notes covering essential Linux administration skills.

---

## 1. Linux File System & Navigation

### Linux Directory Structure

| Directory | Description                   |
| --------- | ----------------------------- |
| `/`       | Root directory                |
| `/home`   | User home directories         |
| `/etc`    | System configuration files    |
| `/var`    | Logs and variable data        |
| `/bin`    | Essential user commands       |
| `/usr`    | User programs and libraries   |
| `/opt`    | Optional third-party software |

---

### Basic Navigation Commands

```bash
ls
ls -l
ls -a
cd /path
cd ..
pwd
```

---

### File Operations

```bash
cp file1 file2
mv file1 file2
rm file.txt
rm -r folder
mkdir newfolder
touch newfile
```

---

### Viewing File Content

```bash
cat file.txt
head file.txt
tail file.txt
tail -f /var/log/syslog
less file.txt
```

---

## 2. User & Group Management

### User Management

```bash
sudo useradd username
sudo passwd username
sudo userdel username
sudo userdel -r username
```

---

### Group Management

```bash
sudo groupadd devops
sudo gpasswd -a user devops
groups username
```

---

### Modify User Properties

```bash
sudo usermod -aG sudo username
sudo usermod -d /new/home user
```

---

## 3. Permissions & Ownership

### Permission Types

| Symbol | Meaning |
| ------ | ------- |
| r      | Read    |
| w      | Write   |
| x      | Execute |

---

### Numeric Permission Values

| Permission | Value |
| ---------- | ----- |
| r          | 4     |
| w          | 2     |
| x          | 1     |

---

### chmod Examples

```bash
chmod 755 file
chmod 644 file
chmod 700 file
chmod 600 file
```

---

### Change Ownership

```bash
sudo chown user file
sudo chown user:group file
```

---

## 4. Managing Services (systemctl)

```bash
sudo systemctl start nginx
sudo systemctl stop nginx
sudo systemctl restart nginx
sudo systemctl status nginx
sudo systemctl enable nginx
sudo systemctl disable nginx
```

---

## 5. Networking Basics

```bash
ip a
ip r
ping 8.8.8.8
ping google.com
ss -tulnp
```

---

## 6. System Monitoring

```bash
top
htop
df -h
du -sh *
free -h
uptime
```

# 🐧 Day01 – Linux Basics & File System Overview

---

## 🎯 Objective  
Get comfortable with basic Linux file operations, file permissions, directory structure, and system commands.

---

## 📁 File & Directory Operations  
- Create directory:
  ```bash
  mkdir project

Change directory:
  ```bash
  cd project
```
Create file:
  ```bash
  touch file.txt
```
List files (detailed):
  ```bash
  ls -l
```
Delete file:
```
rm filename
```
Delete folder and everything in it:
```
rm -rf foldername
```
## Wildcard usage:
```bash
rm *.txt    # removes all .txt files
```

---
## 🗂️ Linux File System Structure

- / → root directory
- /home → user directories
- /etc → configuration files
- /var → logs, temp files
- /var/log/auth.log → authentication logs
- /var/tmp → temporary files
- /bin, /sbin → system binaries

--- 


## 🔐 File Permissions – rwx

r = read

w = write

x = execute

Example:
```
chmod +x script.sh     # give execute permission
chmod 755 filename      # rwxr-xr-x
chown user:group file   # change owner and group
```
---
## 🧮 Numeric Permissions

### Symbolic	Binary	Numeric

|---|	000|	0|
|---|----|---|
|--x|	001|	1|
|---|----|---|
|-w-|	010|	2|
|---|----|---|
|-wx|	011|	3|
|---|----|---|
|r--|	100|	4|
|---|----|---|
|r-x|	101|	5|
|---|----|---|
|rw-|	110|	6|
|---|----|---|
|rwx|	111|	7|

---
### 👤 Users, Groups & Privileges

User types:

Root (admin)

Normal user

System users (services)

Use ***groups*** to see current user's groups

Use ***sudo*** for admin-level actions

---
## 📡 Network Commands

DNS = Domain Name System (translates domain names to IPs)

ping = test network connectivity
```bash
ping google.com
```
---
## 📦 Disk Usage & File Types

file → check file type:
```bash
file <filename>
```
```
df -h → disk free (human-readable)
```
```
du -h filename → disk usage of a file or folder
```
---
## 📚 man – Manual Pages
View command manual:
```
man ls
```

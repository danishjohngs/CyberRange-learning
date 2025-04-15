# 🛠️ Day02 – Custom Commands with Shell Script

---

## 🎯 Objective  
Learn about `ifconfig`, extract IPv4 addresses using custom commands, and explore tools like `awk`, `grep`, and shell scripting.

---

## 🌐 What is `ifconfig`?  
- Used to display network interface configuration  
- Shows IP address, MAC, interface status, etc.  
- **IPv4** = 32-bit address (e.g., `192.168.1.1`)  
- **IPv6** = 128-bit address (longer, more secure, used for modern networking)

---

## 🏠 What is `localhost` (127.0.0.1)?  
- Your own computer (loopback address)  
- Used for testing or accessing services running locally  

---

## 🧠 `awk` Command Basics  
- Used for text processing and column-based extraction  
- Example:
  ```bash
  awk '{print $1}'      # Prints the first column
  ```
---

## 🔍 grep Command Basics
Search and filter text using patterns

Examples:
```bash
grep -h "pattern" <filename>    # Search without printing filenames
grep -v inet6                 # Exclude lines containing 'inet6'
```
---

## 🛠️ Creating a Custom Command: myip

### Goal: Show only the IPv4 address using a single custom command

🧾 Steps:

Create a shell script file:
```bash
nano myip
```
Add the following content:
```bash
ifconfig | grep inet | grep -v inet6 | awk '{print $2}'
```
Make it executable:
```bash
chmod +x myip
```
Move it to a directory in your PATH (optional but useful):
```bash
sudo mv myip /usr/local/bin/
```
Now you can just type:
```bash
myip
```
---

## 🖥️ Shell Types
sh → Bourne shell (basic)

bash → Bourne Again SHell (more powerful, default on most systems)

To execute:
```bash
sh script.sh
bash script.sh
./script.sh
```
--- 

### 💡 Show Only IPv4 Address from ifconfig
```bash
ifconfig | grep inet | grep -v inet6 | awk '{print $2}'
```

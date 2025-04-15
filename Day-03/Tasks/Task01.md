# 🔒 Apache2 Setup & Basic Authentication - Cybersecurity Web Page

This project automates the setup of an `Apache2` web server, serves a simple Cybersecurity-themed HTML page, and applies Basic Authentication for password protection.

---

## 🛠️ Task Overview

1. Install Apache2  
2. Check Apache2 service status and start if inactive  
3. Remove default Apache `index.html`  
4. Add a custom Cybersecurity homepage  
5. Enable Basic Authentication for password-protected access  

---

## 🚀 Setup Instructions

### 1️⃣ Install Apache2
```bash
sudo apt update
sudo apt install apache2 -y
```
---
### 2️⃣ Check Apache2 Service Status
```bsh
sudo systemctl status apache2
```

If it’s inactive (dead), start the service:
```bash
sudo systemctl start apache2
```
---
### 3️⃣ Navigate to Web Root
```bash
cd /var/www/html
```
---

### 4️⃣ Remove Default index.html
```bash
sudo rm index.html
```

### 5️⃣ Add New Cybersecurity Page
Create a new index.html file:
```bash
sudo nano index.html\
```
Paste the HTML:
```bash
html
Copy
Edit
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Cybersecurity Portal</title>
  <style>
    body {
      background-color: #0d1117;
      color: #c9d1d9;
      font-family: monospace;
      text-align: center;
      padding-top: 100px;
    }
    h1 {
      color: #58a6ff;
    }
  </style>
</head>
<body>
  <h1>Welcome to the Cybersecurity Hub 🔐</h1>
  <p>Your connection is secure. Stay safe online!</p>
</body>
</html>
```
Save and exit with CTRL + O, ENTER, and CTRL + X.


### 6️⃣ Enable Password Protection (Basic Authentication)
Step A: Enable htpasswd tool
```bash
sudo apt install apache2-utils -y
```
Step B: Create a .htpasswd file
```bash
sudo htpasswd -c /etc/apache2/.htpasswd <username>
```
Step C: Configure Apache Directory Protection

Edit the Apache default configuration:
```bash
sudo nano /etc/apache2/sites-available/000-default.conf
```
Inside the <VirtualHost *:80> block, add:
```bash
<Directory "/var/www/html">
    AuthType Basic
    AuthName "Restricted Access"
    AuthUserFile /etc/apache2/.htpasswd
    Require valid-user
</Directory>
```
### 7️⃣ Restart Apache2 to Apply Changes
```bash
sudo systemctl restart apache2
```

# 📝 Day03 – Service Commands & Web Server Notes

---

## 🎯 Objective  
Learn service-related commands, understand SSH, Apache, ports, and create a basic web page using Apache.

---

## 🔐 SSH – Secure Shell  
- Used to connect to remote systems securely  
- Default **port**: `22`  
- Protocol: **TCP only**  
- Command:
  ```bash
  ssh username@ip_address <service>
```
```
## 🔧 Service Management with systemctl

### Check service status:
```
sudo systemctl status <service>
```
### Start Apache service:
```
sudo systemctl start <service>
```

## 🌍 What is Apache2?

Apache is a web server that hosts websites
```
Default web directory: /var/www/html/

Default port: 80 (HTTP)

Starts serving files from: index.html inside that directory
```

## 🌐 What are Ports?

Ports = Communication endpoints
```
Common ports:

22 – SSH

80 – HTTP

443 – HTTPS

TCP = Reliable, connection-based

UDP = Faster, no connection required
```

## 🔎 Nmap – Network Scanner

Used to scan ports and check open services
```
nmap -p- <ip_address>
```

## 🌐 Create a Simple Apache Web Page

### Go to Apache root:
```
cd /var/www/html/
```
### Edit or create index.html:
```
sudo nano index.html
```
### Sample content:
```
<html>
  <head><title>Danish text</title></head>
  <body>
    <h1>Hello Danish!</h1>
  </body>
</html>
```
### Open browser:
```
http://localhost
or
<ip-address>
```

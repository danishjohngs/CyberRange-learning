# 📅 Day 05 – Footprinting & Reconnaissance  
🛡️ **Cybersecurity Internship Documentation** | Kali Linux | OSINT | Spiderfoot  

---

## 📌 Daily Objective

Understand the core concepts of **Footprinting** and **Reconnaissance** in ethical hacking.  
Learn to distinguish between **Passive** and **Active** techniques, use **Spiderfoot** for OSINT, and analyze intelligence such as domains, subdomains, WHOIS data, and open ports.

---

## 🧠 Topics Covered

### 📖 What is Footprinting?
Footprinting is the **first phase of ethical hacking**, focused on collecting as much data as possible about a target.

---

### 🕵️ Passive Footprinting
Gathering information **without directly interacting** with the target.

**Examples**:
- 🔎 Google Dorking → `site:<site_name> "<data>"`
- 🗃️ Public data leaks, social media
- 📚 Exploit-DB searches

---

### 🔍 Active Footprinting
Involves **direct interaction** with the target system to gather information.

**Tools & Commands**:
- `whois <domain/ip>`
- `nslookup <domain>`
- `dig <domain>`
- 🔗 Spiderfoot Active Scan

---

### 🌐 Domain vs Subdomain
- **Domain** → Main address: `example.com`
- **Subdomain** → Extended services: `admin.example.com`, `mail.example.com`

Subdomains often reveal additional infrastructure or exposed services.

---

### 🏢 SOC & SIEM Overview

- **SOC (Security Operations Center)**: Team that monitors, detects, and responds to cybersecurity incidents.  
- **SIEM (Security Information and Event Management)**: Technology used for log collection, monitoring, and alerts.

**🔧 Example SIEM Tool**:  
- `Splunk` – Powerful log analysis and threat detection system.

---

## 🛠️ New Methods Practiced

✔️ Utilized **OSINT** to gather intelligence from public sources  
✔️ Collected:
- WHOIS details  
- Subdomain & DNS records  
- Open ports

✔️ Used **Spiderfoot** to automate reconnaissance  
✔️ Analyzed vulnerability reports in detail

---

## 💻 Tool Spotlight: Spiderfoot

**Spiderfoot** is an automated OSINT tool that collects information on:
- 🧾 WHOIS info  
- 🌐 Subdomains  
- 🛡️ Open ports  
- 🧠 DNS records  
- 💬 Leaked credentials, IP reputation, and more

# 🧪 Spiderfoot Example Commands

## Launch the local web interface on port 5001
```
spiderfoot -l 127.0.0.1:5001
```

## Run CLI scan for a domain
```
spiderfoot -d example.com
```
## 📝 Summary

Today's session focused on real-world **reconnaissance** techniques used during ethical hacking assessments.
By practicing both passive and active information gathering methods, I developed a strong understanding of how to collect, organize, and analyze open-source intelligence effectively.

## ✅ Conclusion

I now understand the importance of footprinting in the hacking lifecycle.
Using tools like Spiderfoot, combined with manual recon like whois, nslookup, and Google Dorking, creates a solid foundation for upcoming penetration testing tasks.
I also explored how SOC teams use SIEM tools like Splunk to detect and monitor similar scanning activity from attackers.

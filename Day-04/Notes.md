# 📅 Day 04 – Cybersecurity Lab Setup & GitHub Integration

## 🔔Objective:

- Set up the cybersecurity lab environment using VMware and Kali Linux  
- Connect Kali terminal to GitHub using SSH authentication  
- Practice pushing project files from Kali to GitHub via terminal  
- Install and configure Visual Studio Code on Kali Linux for efficient code editing  



## 🧠 Topics Learned:

- 🔐 SSH Key Authentication with GitHub from Kali Linux  
- 🧭 Navigating GitHub via terminal in a Linux environment  
- ⚙️ Initial Kali setup steps and VMware environment configuration  
- 🛠️ Terminal-based Git workflows and secure code versioning practices  



## 🧪 Methods Practiced:

- Generating and adding SSH keys to GitHub for passwordless access  
- Using SSH instead of HTTPS for more secure GitHub interaction  
- Cloning, pushing, and managing repositories directly from Kali’s terminal  
- Linking Kali tools/scripts to GitHub repos for backup and version tracking  

---
## 💻 Key Commands:

# Generate a new SSH key (ed25519 is a modern secure algorithm)
```
ssh-keygen -t ed25519 -C "my_email@example.com"
```

# View and copy your public key (to paste into GitHub → Settings → SSH Keys)
```
cat ~/.ssh/id_ed25519.pub
```

# Initialize a new Git repository and link with GitHub (SSH)
```
git init  
git remote add origin git@github.com:username/repo.git  
git add .  
git commit -m "Initial commit"  
git push -u origin main  
```
---
## 📦 Tools & Platforms Used:
- 🐧 Kali Linux (installed on VMware)  
- 🖥️ GitHub (SSH integration for terminal-based Git operations)  
- 🛠️ Git CLI (preinstalled on Kali)  
- 💡 Visual Studio Code (Linux version installed on Kali)  


## 🎯 Key Outcome:

A fully operational ethical hacking lab with GitHub integration is now set up. I can now push my tools, scripts, recon results, and automation projects directly from the Kali terminal to GitHub. This is an essential skill for penetration testers and bug bounty hunters.

---
## 📌 Closing Note:

This marks the beginning of a version-controlled ethical hacking workflow. I now understand the importance of secure GitHub access, code backups, and daily practice in a Linux environment, even from a Windows host.



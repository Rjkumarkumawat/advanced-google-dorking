```markdown
# 🔍 Advanced Google Dorking for Target Reconnaissance  
*By Rajkumar Kumawat*  
*A practical guide for ethical hackers, penetration testers, and security enthusiasts*  

---

## 📜 Introduction  
Hello fellow hackers! I'm **Rajkumar Kumawat**, and today we're diving deep into **Google Dorking** — the art of using Google's search operators to uncover hidden vulnerabilities and sensitive information.  

> ⚠️ **Ethical Disclaimer**:  
> This guide is for **educational purposes only**. Always get proper authorization before testing any system. Unauthorized access is illegal!  

---

## 🧠 Why Google Dorking Matters  
Google Dorking helps you:  
- Find exposed sensitive files (databases, passwords)  
- Discover hidden admin panels  
- Identify outdated software with known vulnerabilities  
- Gather intelligence for penetration testing  

---

## 🛠️ Core Techniques (With Examples)  

### 1️⃣ Finding Exposed Documents  
```google
site:example.com ext:pdf OR ext:docx "confidential"
site:example.com intitle:"index of" "backup"
```
**Raj's Tip**: Try replacing `example.com` with your target domain. You might find juicy files!  

### 2️⃣ Discovering Login Portals  
```google
site:example.com intitle:"login" OR "admin"
site:example.com inurl:/wp-admin
```
**Found something?** Check for default credentials!  

### 3️⃣ GitHub Secrets Hunting  
```google
site:github.com "example.com" AND ("api_key" OR "password")
```
**Raj's Experience**: I once found AWS keys exposed in a public GitHub repo!  

### 4️⃣ Network Device Discovery  
```google
intitle:"RouterOS" "Winbox"
inurl:/webui/login.jsp
```
These can reveal unprotected network devices.  

---

## 🔥 Pro-Level Dork Combos  
Here are some of my favorite advanced queries:  

| Purpose | Dork Query |
|---------|-----------|
| Find PHP errors | `site:example.com "PHP Error" intext:"line"` |
| Open cameras | `intitle:"webcamXP 5"` |
| Exposed DBs | `filetype:sql "INSERT INTO"` |

---

## 🛡️ Defense Strategies  
As a security professional, I recommend:  
1. **Regularly Google yourself**: `site:yourdomain.com`  
2. **Use robots.txt** to block sensitive paths  
3. **Monitor GitHub** for accidental leaks  

---

## 📚 Resources & Tools  
- [Google Hacking Database (GHDB)](https://www.exploit-db.com/google-hacking-database)  
- [Foca.sh](https://fofa.so) - Advanced search engine  
- [Raj's GitHub](https://github.com/Rjkumarkumawat/) *(Add your real GitHub link)*  

---

## 🎯 Final Challenge  
Try this on **your own website**:  
```google
site:yourdomain.com ext:env OR ext:sql
```
Document your findings and share them with me!  

---

## 💬 About the Author  
**Rajkumar Kumawat** is a cybersecurity enthusiast passionate about ethical hacking and open-source intelligence. Connect with me on [LinkedIn](https://www.linkedin.com/in/rajkumar-kumawat-66072b199/) *(add your real LinkedIn link)*.  

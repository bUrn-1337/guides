# Getting Started with Web Exploitation

Web exploitation is a core category in Capture the Flag (CTF) competitions and real-world security testing.  
This guide will walk you through the basics, common vulnerabilities, and essential tools to help you get started.

---

## 🌐 What is Web Exploitation?
Web exploitation involves finding and leveraging vulnerabilities in web applications.  
The goal is usually to **gain unauthorized access, extract hidden data, or bypass protections**.

---

## How to get Started
Before diving in, make sure you are comfortable with:
- Watch CS50's lectuce 6, 7, 8, 9 and complete the assignments to get a basic knowledge of web 
- Understanding of **HTTP (requests, responses, headers, cookies)** refer: [TOP's lesson](https://www.theodinproject.com/lessons/foundations-how-does-the-web-work)
- Using a browser’s **developer tools** 
- Complete [Linux Luminarium](https://pwn.college/linux-luminarium/) to get comfortable with the terminal (linux or macos)
- Start solving challenges on [PicoCTF](https://play.picoctf.org/practice)
- Explore vulnerabilites on [Portswigger Web Security Academy](https://portswigger.net/web-security/learning-paths), start with xss, sqli, file upload vulnerabilites,authentication vulnerabilites and gradually dig deeper into those topics.
- Give beginner level CTFs from [CTFtime](https://ctftime.org/)
- Read writeups for CTFs and read bug bounty reports.
---



## 🔎 Common Vulnerabilities

### 1. **Information Disclosure**
- Hidden files (`robots.txt`, `.git/`, `.env`)
- Misconfigured error messages
- Directory traversal (`../../etc/passwd`)

### 2. **SQL Injection (SQLi)**
- Example payload: `' OR '1'='1`
- Tools: `sqlmap`

### 3. **Cross-Site Scripting (XSS)**
- Injecting malicious JavaScript
- Example: `<script>alert(1)</script>`
- Used to steal cookies or perform actions on behalf of a victim
- Amazing resource: [text](https://aszx87410.github.io/beyond-xss/en/)

### 4. **Command Injection**
- Input directly executed on the server
- Example: user input directly appended to os command like `curl user_input`

### 5. **Authentication Bypasses**
- Default credentials
- Insecure session handling
- JWT vulnerabilities

---

## ⚒️ Essential Tools
- **Burp Suite / OWASP ZAP** – Intercept & manipulate requests
- **cURL / Postman** – Quick API testing
- **sqlmap** – Automated SQLi exploitation
- **gobuster / dirsearch** – Directory brute-forcing
- **Browser DevTools** – Inspect & manipulate frontend code

---

## 🚀 Methodology
1. **Reconnaissance** – Look for endpoints, parameters, hidden files, sinks where user input is going.
2. **Input Testing** – Look at the source code, try to find where input is going and try payloads related to the sink
3. **Manipulate Requests** – Modify headers, cookies, and payloads.
4. **Identify Vulnerabilities** – See how the application responds.
5. **Exploit & Extract** – Use tools or manual techniques to retrieve sensitive data.

---

## 📚 Learning Resources
- [PortSwigger Web Security Academy](https://portswigger.net/web-security)
- [OWASP Top Ten](https://owasp.org/www-project-top-ten/)
- [HackTricks](https://book.hacktricks.xyz/)
- CTF Platforms: [picoCTF](https://picoctf.org/)
- [PayloadAllTheThings](https://github.com/swisskyrepo/PayloadsAllTheThings)
- Search on [google](https://www.google.com/) for CTF writups and bug bounty reports for any topic you wish to learn
- For totally new topics, google them and learn about the technology before its vulnerabilities, for 
---

## ✅ Tips for Beginners
- Always start with **manual testing** before automated tools.
- Learn to read error messages carefully.
- Keep practicing on CTF platforms.
- Google more than you chatgpt, as you get more advanced, google will always be the one to come in clutch, not chatgpt.

---

## Some interesting writeups/ bug bounty reports:
- [pyjail](https://halb.it/posts/bluehens-pyjail/)
- [Proton mail vulnerability](https://www.sonarsource.com/blog/code-vulnerabilities-leak-emails-in-proton-mail/)
- [Double Dash SQLi](https://www.sonarsource.com/blog/double-dash-double-trouble-a-subtle-sql-injection-flaw/)
- [PHP Object Injection](https://www.vaadata.com/blog/what-is-object-injection-exploitations-and-security-best-practices/)
- [Prototype Pollution in Python](https://blog.abdulrah33m.com/prototype-pollution-in-python/)
- Discover more for yourself!
---

## ⚠️ Disclaimer
This guide is for **educational purposes only**.  
Do not attempt to exploit systems without **explicit permission**.

---

### 🎯 Next Steps
- Practice on free platforms like **picoCTF**.
- Start with simple challenges (info disclosure, basic SQLi).
- Slowly progress to advanced topics (blind SQLi, chained XSS, logic flaws).
- Find people 
---

Happy hacking! 🕵️‍♂️

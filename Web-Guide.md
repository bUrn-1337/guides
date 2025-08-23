# Getting Started with Web Exploitation

Web exploitation is a core category in Capture the Flag (CTF) competitions and real-world security testing.  
This guide will walk you through the basics, common vulnerabilities, and essential tools to help you get started.

---

## 🌐 What is Web Exploitation?
Web exploitation involves finding and leveraging vulnerabilities in web applications.  
The goal is usually to **gain unauthorized access, extract hidden data, or bypass protections**.

---

## How to get Started
There is no hard and fast rule to follow the order, but roughly, do these in the given order
- Watch CS50's lectures of weeks 6, 7, 8, 9, and complete the assignments to get a basic knowledge of web 
- Understanding of **HTTP (requests, responses, headers, cookies)** refer: [TOP's lesson](https://www.theodinproject.com/lessons/foundations-how-does-the-web-work)
- Using a browser’s **developer tools** 
- Complete [Linux Luminarium](https://pwn.college/linux-luminarium/) to get comfortable with the terminal (Linux or macOS)
- Start solving challenges on [PicoCTF](https://play.picoctf.org/practice)
- Explore vulnerabilities on [Portswigger Web Security Academy](https://portswigger.net/web-security/learning-paths), start with XSS, SQLi, file upload vulnerabilities, and authentication vulnerabilities, and gradually dig deeper into those topics.
- Give beginner-level CTFs from [CTFtime](https://ctftime.org/)
- Read write-ups for CTFs and read bug bounty reports.
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
1. **Reconnaissance** – Look for endpoints, parameters, hidden files, and sinks on the GUI where user input is going.
2. **Input Testing** – Look at the source code, try to code that deals with the input, and try payloads related to the sink
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
- Search on [Google](https://www.google.com/) for CTF write-ups and bug bounty reports for any topic you wish to learn
- For totally new topics, Google them and learn about the technology before its vulnerabilities, for 
---

## ✅ Tips for Beginners
- Always start with **manual testing** before automated tools.
- Learn to read error messages carefully.
- Keep practicing on CTF platforms.
- Use Google more than ChatGPT, as you get more advanced, Google will always be the one to come in clutch, not ChatGPT.

---

## Some interesting write-ups/ bug bounty reports:
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
---

This might seem a lot, but you don't have to do all this in a single day or a single month. It is all about starting, you might even find a new hobby, who knows?
Find people who share the same interest, this will give you motivation to keep going. Form a team and play CTFs with them.
If you really want to go deep into this, get more experience with web dev as well.
I would suggest [TOP](https://www.theodinproject.com) for the same, first complete the foundations, in 1 month or so, then move on to databases and node/express course. Do the others if you really wish to.
Happy hacking! 🕵️‍♂️

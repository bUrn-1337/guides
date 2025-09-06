# Getting Started with Web Exploitation

Web exploitation is a core category in [CTFs](https://dev.to/atan/what-is-ctf-and-how-to-get-started-3f04) and real-world security testing.  
This guide will walk you through the basics, common vulnerabilities, and essential tools to help you get started.

---

## 🌐 What is Web Exploitation?
[Web exploitation](https://ctf101.org/web-exploitation/overview/) involves finding and leveraging vulnerabilities in web applications.  
The goal is usually to **gain unauthorized access, extract hidden data, or bypass protections**.

---

## How to get Started
There is no hard and fast rule to follow the order, but roughly, do these in the given order
- Watch [CS50](https://cs50.harvard.edu/x/)'s lectures of weeks 6, 7, 8, 9, and complete the assignments to get a basic knowledge of web 
- Understanding of **HTTP (requests, responses, headers, cookies)** refer: [TOP's lesson](https://www.theodinproject.com/lessons/foundations-how-does-the-web-work)
- Understanding **frontend and backend** [TOP's lesson](https://www.theodinproject.com/lessons/nodejs-introduction-to-the-back-end)
- Using a browser’s **developer tools** 
- Complete [Linux Luminarium](https://pwn.college/linux-luminarium/) to get comfortable with the terminal (Linux or macOS)
- Read about what a CTF is [atan's blog](https://dev.to/atan/what-is-ctf-and-how-to-get-started-3f04)
- See what Web Exploitation is [ctf101](https://ctf101.org/web-exploitation/overview/)
- Start solving challenges on [PicoCTF](https://play.picoctf.org/practice), [websec.fr](https://websec.fr/)
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
- Amazing resource: [XSS series by Huli](https://aszx87410.github.io/beyond-xss/en/)

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
2. **Input Testing** – Look at the [source code](https://www.sonarsource.com/learn/source-code/), try to code that deals with the input, and try payloads related to the sink
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
- [Jorian's book](https://book.jorianwoltjer.com/web/enumeration)
Ye dono are good starting points if you don't know the theory yet
- Search on [Google](https://www.google.com/) for CTF write-ups and bug bounty reports for any topic you wish to learn
- For totally new topics, Google them and learn about the technology before its vulnerabilities, for 
---

## ✅ Tips for Beginners
- Always start with **manual testing** before automated tools.
- Learn to read error messages carefully.
- Keep practicing on CTF platforms.
- Use Google more than ChatGPT, as you get more advanced, Google will always be the one to come in clutch, not ChatGPT.
---

## 🔑 Challenge Solving Tips

### 🔍 Look for Hints
- Check the **challenge name** and **description** for clues.  
  - Example:  
    - A challenge named **"jawt"** may indicate a **JWT vulnerability**.  
    - A challenge with **"sql"** in the name may point to **SQL injection**.  

### 📦 Frameworks & Versions
- Pay attention to framework or library versions (if revealed in source code).  
- Older or unpatched versions often have **known vulnerabilities**.  

### ⚠️ Common Vulnerable Practices
Be on the lookout for insecure coding patterns such as:  

1. **XSS (Cross-Site Scripting)** → Direct concatenation of user input into HTML (e.g., `innerHTML`).  
2. **SQL Injection** → Direct concatenation of user input into database queries.  
3. **Command Injection** → Direct concatenation of user input into OS commands.  
4. **SSTI (Server-Side Template Injection)** → Use of functions like `render_template_string` or similar in other frameworks.  
5. **Prototype Pollution** → Using deep merge with unvalidated user input.  

### 🧠 Logic Flaws
- In better challenges, the vulnerability may be a **logic flaw** rather than a direct injection.  
- Examples: authentication bypass, role misconfiguration, race conditions, or unintended workflow abuse.  

### Run the Challenge Locally
- Get an understanding of dockerfile and docker-compose to run the challenge locally after you get some experience.
- It can help you debug the exploit properly.
---

## Some interesting write-ups/ bug bounty reports:
- [SMP vulnerability exploit by InfoSecIITR](https://infoseciitr.in/2022-06-05-exploitation-at-smp-iitr/)
- [pyjail](https://halb.it/posts/bluehens-pyjail/)
- [Proton mail vulnerability](https://www.sonarsource.com/blog/code-vulnerabilities-leak-emails-in-proton-mail/)
- [Double Dash SQLi](https://www.sonarsource.com/blog/double-dash-double-trouble-a-subtle-sql-injection-flaw/)
- [PHP Object Injection](https://www.vaadata.com/blog/what-is-object-injection-exploitations-and-security-best-practices/)
- [Prototype Pollution in Python](https://blog.abdulrah33m.com/prototype-pollution-in-python/)
- Discover more for yourself!
---

### 🎯 Next Steps
- Practice on free platforms like **picoCTF**.
- Start with simple challenges (info disclosure, basic SQLi).
- Slowly progress to advanced topics (blind SQLi, chained XSS, logic flaws).
- Getting started with docker, start when you have had some experience. [Docker tutorial for beginners](https://www.youtube.com/watch?v=b0HMimUb4f0), [Docker Documentation](https://docs.docker.com/) 
---

### Why run the challenge locally? (for intermediate skill players)
- Can tweak the server code to debug your exploit.
- Lets you add debugging prints/logs to see how inputs are being processed.
- When there are many filters, you can test your exploit for each filter one by one before combining them.
- Many a times, the CTF platform allows you to access the challenge site by making an instance which expires in some amount of time, so it is more convenient to run the challenge on your own machine without any such time limit. 
---

### Writing solve scripts (for intermediate-advanced players)
- Sometimes it becomes too tedious to give inputs to the site, this is where the power of python comes handy.
- For example, you might have to send a json, which must be inside quotes, and the keys are integer strings, for some other non sense, this is very difficult to craft by hand.
- You can use python to craft your payloads and also send them.
- Resources: [realpython's guide](https://realpython.com/python-requests), [requests documentation](https://requests.readthedocs.io/en/latest/user/quickstart/)


This might seem a lot, but you don't have to do all this in a single day or a single month. It is all about starting, you might even find a new hobby, who knows?
Find people who share the same interest, this will give you motivation to keep going. Form a team and play CTFs with them.
If you really want to go deep into this, get more experience with web dev as well.
I would suggest [TOP](https://www.theodinproject.com) for the same, first complete the foundations, in 1 month or so, then move on to databases and node/express course. Do the others if you really wish to.
Happy hacking! 🕵️‍♂️

## ⚠️ Disclaimer
This guide is for **educational purposes only**.  
Do not attempt to exploit systems without **explicit permission**.

---

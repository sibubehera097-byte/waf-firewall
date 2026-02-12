# WAF Firewall – Python Web Application Firewall

A lightweight and extensible **Web Application Firewall (WAF)** built using **Python and Flask**.  
This project inspects incoming HTTP requests and blocks malicious payloads such as SQL Injection, XSS, and directory traversal attacks in real time.

---

## 📌 Overview

Web applications are often targeted by attackers using injection and scripting attacks.  
This project acts as a **protective layer** between users and the web application, detecting and blocking suspicious input before it reaches the backend.

---

## 🔐 Security Features

- SQL Injection protection  
- Cross-Site Scripting (XSS) detection  
- Path Traversal attack blocking  
- URL-encoded attack detection  
- Regex-based rule engine  
- IP-based attack logging  
- SQLite database for storing attack logs  

---

## 🏗️ Project Architecture

waf-firewall/
│
├── app.py → Flask web application
├── waf.py → Core WAF engine
├── rules.py → Attack detection rules
├── database.db → SQLite attack log database
└── templates/
└── login.html → Secure login page


## ⚙️ Installation & Setup

### 1️⃣ Clone the repository

bash:-

git clone https://github.com/sibubehera097-byte/waf-firewall.git
cd waf-firewall

2️⃣ Create virtual environment

base:-

python3 -m venv venv
source venv/bin/activate

3️⃣ Install dependencies

base:-

pip install flask

4️⃣ Run the application

base:-

python app.py

Open your browser:

code:-

http://127.0.0.1:5000

🧪 Testing the Firewall

Try this SQL injection payload in the login form:

code:-

admin' OR 1=1 --

Expected response:

🚫 Attack Blocked by WAF
📊 View Attack Logs

base:-

sqlite3 database.db
SELECT * FROM logs;

This shows attacker IPs, payloads, and timestamps.

                                                   "THANK💗YOU"

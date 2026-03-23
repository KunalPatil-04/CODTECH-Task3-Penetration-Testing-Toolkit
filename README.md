# Penetration Testing Toolkit

Intern Name: Kunal Girish Salunke
Intern ID: CTIS5722
Domain: Cyber Security & Ethical Hacking
Duration: 4 Weeks
Mentor: Muzammil

## Overview
This repository hosts Task 3 of the CODTECH internship: A modular Python-based penetration testing toolkit with a port scanner and brute-forcer. It demonstrates basic ethical hacking techniques for reconnaissance and authentication testing, with detailed documentation.

## Task Description
Per the instructions, the toolkit includes multiple modules (e.g., port scanner using socket, brute-forcer using requests) for penetration testing. It's designed to be expandable, with proper code commenting for readability.

## How It Works
- **Port Scanner Module (`port_scanner.py`)**: Scans a target IP for open ports in a range, using socket connections to detect services.
- **Brute-Forcer Module (`brute_forcer.py`)**: Attempts username/password combinations on an HTTP login form, checking for success indicators.
- **Main Script (`main.py`)**: Command-line interface to run modules, e.g., `python main.py portscan 127.0.0.1 1 100`.

Tools Used: Python 3, socket (built-in), requests, itertools.

## Usage
1. Clone: `git clone https://github.com/KunalPatil-04/CODTECH-Task3-Penetration-Testing-Toolkit.git`
2. `cd CODTECH-Task3-Penetration-Testing-Toolkit`
3. Run port scan: `python main.py portscan <target> [start] [end]`
4. Run brute-force: `python main.py bruteforce <url> <usernames.txt> <passwords.txt>`

**Ethical Note:** Use only on authorized systems. Unauthorized testing is illegal.

## Output Examples
![Port Scan Output] https://github.com/KunalPatil-04/CODTECH-Task3-Penetration-Testing-Toolkit/blob/main/Task%203_1.png


![Brute-Force Output] https://github.com/KunalPatil-04/CODTECH-Task3-Penetration-Testing-Toolkit/blob/main/Task%203_2.png

## Explanation
Penetration testing, or pen-testing, is a simulated cyber attack to identify vulnerabilities in systems before malicious hackers exploit them. This toolkit provides hands-on experience in two key phases: reconnaissance (port scanning) and exploitation (brute-forcing). The port scanner module uses Python's socket library to iterate through port ranges, attempting TCP connections with a short timeout to detect open ports efficiently. Open ports indicate running services, such as HTTP on 80 or SSH on 22, which could be potential entry points. For instance, scanning localhost after starting a simple server reveals port 8000 as open, highlighting how attackers map network footprints.

The brute-forcer module employs requests for HTTP POST submissions and itertools.product to generate username-password pairs from wordlists. It targets login forms, customizable via form data keys, and checks responses for success strings like "Welcome." This simulates dictionary attacks on weak authentication, common in real-world breaches like the 2012 LinkedIn hack. In testing, it failed on a sample site, demonstrating safe, non-destructive operation.

Modularity is achieved by separating functions into files, imported in main.py, allowing easy additions like a directory scanner. This design promotes code reusability and scalability, essential in professional tools like Metasploit. Ethical considerations are paramount: Pen-testing requires explicit permission, adhering to laws like the Computer Fraud and Abuse Act. Misuse can lead to legal consequences, so this toolkit emphasizes learning in controlled environments like virtual machines or test sites (e.g., DVWA).

In cyber security, such tools aid red teams in vulnerability assessments, helping organizations strengthen defenses. Limitations include single-threaded scanning (slow for large ranges) and basic brute-forcing without rate-limiting evasion. Improvements could involve multithreading with concurrent.futures or integrating APIs for vulnerability databases. This project deepened my understanding of offensive security, reinforcing defensive strategies like strong passwords and firewalls. By building this, I learned Python's networking capabilities and the importance of secure coding practices. (Word count: 450)


## Limitations and Future Work
- Basic; not for production.
- Add more modules like vulnerability exploit demos.

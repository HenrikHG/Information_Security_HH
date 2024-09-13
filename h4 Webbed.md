# h4 Webbed

---

## OWASP Top 10 Summary

### **A01:2021 – Broken Access Control**
- Access control failures can lead to unauthorized data access or privilege escalation.
- Common issues: URL manipulation, insecure direct object references (IDOR), and missing API controls.
- Affects 94% of applications with over 318k occurrences.
- **Prevention**: Deny access by default, reuse access control mechanisms, enforce proper session management.

---

### **A03:2021 – Injection**
- Injection vulnerabilities occur when untrusted data is handled in queries/commands (e.g., SQL, NoSQL, OS commands).
- Common types: SQL Injection (CWE-89), Cross-Site Scripting (CWE-79).
- Affects 94% of applications with over 274k occurrences.
- **Prevention**: Use parameterized queries, validate inputs, limit query outputs.

---

### **A05:2021 – Security Misconfiguration**
- Misconfigurations include leaving unnecessary features enabled, using default credentials, and improper error handling.
- Affects 90% of applications with over 208k occurrences.
- Vulnerabilities arise from weak configurations or outdated components.
- **Prevention**: Harden environments, regularly update settings, remove unused features.

---

### **A06:2021 – Vulnerable and Outdated Components**
- Outdated or unsupported components pose serious security risks.
- Affects 27.96% of applications with over 30k occurrences.
- Vulnerabilities often arise from unmaintained software or unpatched components (e.g., Struts 2 CVE-2017-5638).
- **Prevention**: Continuously inventory components, maintain patch management, monitor for vulnerabilities.

---

# Task Solutions Report

## a) Goat: WebGoat 2023.4 Installation
WebGoat 2023.4 was successfully installed.

---

## b) F12: WebGoat 2023.4 - General: Developer Tools

  1. 1st task has been successfully solved
     ![Screenshot 2024-09-12 001351](https://github.com/user-attachments/assets/4b9fc7ef-c647-40e8-944e-3ee2fddfdf43)

  2. 2nd task has been successfully solved
     ![Screenshot 2024-09-12 002325](https://github.com/user-attachments/assets/84153563-d74c-45b8-bd57-ab35bb91940f)
     ![Screenshot 2024-09-12 002354](https://github.com/user-attachments/assets/fa9e1da9-18a4-43bf-aa9a-a0a2139844f0)

---

## c) Not outdated: Update all operating systems and applications on Linux

  1. Run the following commands to update the OS:
     ```bash
     sudo apt update && sudo apt upgrade
     ```
  2. Check for any outdated applications or packages:
     ```bash
     sudo apt list --upgradable
     ```
  3. Perform the updates as necessary:
     ```bash
     sudo apt full-upgrade
     ```
     NOTE: THE FULL UPGRADE MAY TAKE LONGER!
     
![Screenshot 2024-09-12 002729](https://github.com/user-attachments/assets/ce415945-a3ce-4a0d-aac8-d887c84e5bd1)

![Screenshot 2024-09-12 002817](https://github.com/user-attachments/assets/49a4770b-023e-479f-b674-55c7a168f20e)

---

## d) Sequel: SQLZoo - SELECT Basics & World
### 0 SELECT Basics
1)
![Screenshot 2024-09-12 003834](https://github.com/user-attachments/assets/9f20d1c0-aca6-4dcc-8327-ba1f8a17d4be)

2)
![Screenshot 2024-09-12 003920](https://github.com/user-attachments/assets/2bd2263b-08be-4361-b927-85b62dfa9215)

3)
![Screenshot 2024-09-12 004000](https://github.com/user-attachments/assets/b61fd138-4b34-426c-9c71-d67c83741ba1)


### 2 SELECT from World - First Two Subtasks
1)
![Screenshot 2024-09-12 004132](https://github.com/user-attachments/assets/dd87f296-c62d-4f99-8a7e-2471f259e1af)

2)
![Screenshot 2024-09-12 004530](https://github.com/user-attachments/assets/9e8e4272-e1ce-4558-a942-2fc32f047801)

3)
![Screenshot 2024-09-12 004934](https://github.com/user-attachments/assets/128d55ee-0adb-461a-8b22-3aab3b563291)

4)
![Screenshot 2024-09-12 005127](https://github.com/user-attachments/assets/ced56813-ac82-4f5b-a6a5-2895613c60dc)

5)
![Screenshot 2024-09-12 005453](https://github.com/user-attachments/assets/8e9661ed-a42f-4123-a41f-cac46722b472)

6)
![Screenshot 2024-09-12 005702](https://github.com/user-attachments/assets/fe3e4730-fe1e-405a-b70b-a585b6894b63)

7)
![Screenshot 2024-09-12 005959](https://github.com/user-attachments/assets/c7f73689-5043-4176-96f2-6971fd38791b)

8)
![Screenshot 2024-09-12 010057](https://github.com/user-attachments/assets/e8b0a05f-7b9f-43ad-b04a-e00a16d6b15d)

9)
![Screenshot 2024-09-12 010650](https://github.com/user-attachments/assets/9d5fb8eb-5ebe-48e2-9d53-b39e3d65787a)

10)
![Screenshot 2024-09-12 011154](https://github.com/user-attachments/assets/3ce85cc1-d3ba-47b3-9d84-667e5ccb8697)

11)
![Screenshot 2024-09-12 011450](https://github.com/user-attachments/assets/9922c30a-9e88-4ce8-9a94-0eabc4d7499e)

12)
![Screenshot 2024-09-12 011726](https://github.com/user-attachments/assets/82ee2526-d910-4480-b233-4b3d09cb00bf)

13)
![Screenshot 2024-09-12 012013](https://github.com/user-attachments/assets/9a5efe17-c031-47cc-9a61-611f424747aa)

---

## e) Johnny Tables: PortSwigger Labs - SQL Injection in WHERE Clause

  1. Identify the vulnerable input field and inject SQL code to modify the query.
  2. Example solution:
     ```sql
     ' OR+1=1--;
     ```
![Screenshot 2024-09-12 110303](https://github.com/user-attachments/assets/ffe5d83c-0850-48c0-a9ab-dbc042279534)

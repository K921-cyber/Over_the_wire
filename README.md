## 🏗️ Overall System Architecture

```mermaid
flowchart TB
    U[User] --> UI[Web Interface / CLI]

    UI --> VE[Input Validation Layer]

    VE --> SE[Scanner Engine]

    SE --> SQLI[SQL Injection Detection Module]
    SE --> XSS[Cross-Site Scripting Detection Module]
    SE --> CSRF[CSRF Protection Check Module]
    SE --> OR[Open Redirect Detection Module]

    SQLI --> AGG[Result Aggregator]
    XSS --> AGG
    CSRF --> AGG
    OR --> AGG

    AGG --> SC[Severity Classification]
    SC --> OWASP[OWASP Top 10 Mapping]

    OWASP --> REP[PDF Report Generator]

    REP --> UI

```

<div align="center">

# **OverTheWire Wargame Walkthroughs**

A structured and professionally documented collection of walkthroughs for the **OverTheWire** cybersecurity wargames.  
Focused on clarity, accuracy, and long-term learning value.

---

![Stars](https://img.shields.io/github/stars/K921-cyber/Over_the_wire?style=for-the-badge)
![Forks](https://img.shields.io/github/forks/K921-cyber/Over_the_wire?style=for-the-badge)
![Last Commit](https://img.shields.io/github/last-commit/K921-cyber/Over_the_wire?style=for-the-badge)
![Issues](https://img.shields.io/github/issues/K921-cyber/Over_the_wire?style=for-the-badge)

---

### **Wargame Index**

| Wargame | Directory | Status |
|--------|-----------|--------|
| **Bandit** | [`/Bandit`](./Bandit) | ✔ Available |
| **Leviathan** | [`/Leviathan`](./Leviathan) | ⏳ In Progress |
| **Narnia** | [`/Narnia`](./Narnia) | ⏳ In Progress |
| **Krypton** | [`/Krypton`](./Krypton) | ⏳ In Progress |

</div>

---

## **Overview**

This repository provides **clean, structured, and technically accurate walkthroughs** for the OverTheWire wargames.  
The goal is to help learners:

- Understand the *reasoning* behind each step  
- Build a solid foundation in Linux, security concepts, and problem-solving  
- Develop the mindset required for CTFs and real-world cybersecurity tasks  

Each walkthrough is created with an emphasis on:

- Clear explanations  
- Reproducible commands  
- Educational breakdowns  
- No shortcuts, no guesswork  

---

## **Purpose**

OverTheWire is one of the most recommended starting points for aspiring cybersecurity professionals.  
This repository exists to:

- Document personal progress  
- Provide high-quality references for others  
- Maintain an open-source learning resource  
- Encourage ethical, hands-on security practice  

It is designed with the standards of documentation used in professional open-source projects.

---

## **Learning Outcomes**

| Area | Description |
|------|-------------|
| **Linux Fundamentals** | Shell navigation, file handling, permissions, processes |
| **Enumeration Techniques** | Searching, filtering, decoding, hidden files |
| **Privilege Mechanics** | SUID/SGID, ownership, execution rights |
| **Basic Cryptography** | Encodings, classic ciphers, data transformations |
| **Binary Interaction** | Executables, permissions, basic debugging logic |

---

## **Getting Started**

To begin with **Bandit Level 0**, use:

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
# Password: bandit0

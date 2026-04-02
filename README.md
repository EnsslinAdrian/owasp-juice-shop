# Juice Shop Master

A structured security research project documenting common web application vulnerabilities using [OWASP Juice Shop](https://owasp.org/www-project-juice-shop/) in an isolated Oracle VirtualBox environment. Each challenge is hands-on explored, exploited, and documented — covering real-world attack vectors from injection to sensitive data exposure.

> **Educational Disclaimer:** This project is strictly for educational and research purposes. All techniques are practiced in an isolated, local environment. No real systems, applications, or user data are targeted or harmed. Unauthorized use of these techniques against live systems is illegal.

---

## Table of Contents

1. [Prerequisites](#prerequisites)
2. [Quickstart](#quickstart)
3. [Project Structure](#project-structure)
4. [Challenges](#challenges)
5. [Security Impact](#security-impact)
6. [Author](#author)

---

## Prerequisites

| Requirement | Description |
|---|---|
| [Oracle VirtualBox](https://www.virtualbox.org/) | Virtualization environment to run the isolated lab |
| [OWASP Juice Shop](https://github.com/juice-shop/juice-shop) | Intentionally vulnerable web application |
| [Node.js](https://nodejs.org/) or [Docker](https://www.docker.com/) | Runtime to start Juice Shop locally |
| Basic Web Security Knowledge | Understanding of HTTP, cookies, and common vulnerabilities |

---

## Quickstart

**1. Start Oracle VirtualBox and boot your lab VM.**

**2. Launch Juice Shop:**

```bash
# Option A — Docker
docker pull bkimminich/juice-shop
docker run --rm -p 3000:3000 bkimminich/juice-shop

# Option B — Node.js
git clone https://github.com/juice-shop/juice-shop.git
cd juice-shop
npm install
npm start
```

**3. Open your browser and navigate to:**

```
http://localhost:3000
```

**4. Pick a challenge from the [Challenges](#challenges) section and follow the documentation.**

---

## Project Structure

```
owasp/
|-- 📁 Broken_Access_Control
|   |-- 📁 img/
|   |-- ℹ️ MANIPULATE_BASKET.md
|-- 📁 Improper_Input_Validation/
|   |-- 📁 img/
|   |-- ℹ️ UPLOAD_SIZE.md
|-- 📁 Injection/
|   |-- 📁 img/
|   |-- ℹ️ NOSQL_DOS.md
|-- 📁 Sensitive_Data_Exposure/
|   |-- 📁 img/
|   |-- ℹ️ FORGOTTEN_DEVELOPER_BACKUP.md
|-- ℹ️ README.md
```

---

## Challenges

Each category below corresponds to a documented challenge with step-by-step exploitation, proof of concept, and mitigation strategies.

### Broken Access Control

Broken Access Control allows users to act outside of their intended permissions. This category covers challenges where attackers manipulate requests to access unauthorized resources, modify other users' data, or bypass access restrictions.

➜ [View Challenge Documentation](./Broken_Access_Control/MANIPULATE_BASKET.md)

---

### Injection

SQL Injection and related injection flaws occur when untrusted user input is interpreted as part of a query or command. An attacker can manipulate database queries to bypass authentication, extract data, or destroy records.

➜ [View Challenge Documentation](./Injection/README.md)

---

### Improper Input Validation

Applications that fail to properly validate or sanitize user-supplied input are vulnerable to a wide range of attacks — including bypassing business logic, manipulating order values, or submitting malformed data that the backend processes incorrectly.

➜ [View Challenge Documentation](./Improper_Input_Validation/UPLOAD_SIZE.md)

---

### Sensitive Data Exposure

When applications store or transmit sensitive data (credentials, tokens, PII) without adequate protection, attackers can retrieve it through unprotected endpoints, insecure storage, or predictable file locations.

➜ [View Challenge Documentation](./Sensitive_Data_Exposure/FORGOTTEN_DEVELOPER_BACKUP.md)

---

## Security Impact

The vulnerabilities documented in this project represent some of the most critical risks in modern web applications:

| Risk | Consequence |
|---|---|
| **Data Leakage** | Exposure of credentials, PII, and confidential business data |
| **Account Takeover** | Authentication bypass grants unauthorized access to user and admin accounts |
| **System Compromise** | Successful exploitation can lead to full application or server control |
| **Compliance Violations** | Unmitigated vulnerabilities violate GDPR, PCI-DSS, and similar regulations |
| **Undetected Attacks** | Missing observability allows breaches to go unnoticed for extended periods |

---

## Author

**Adrian Enßlin**
DevSecOps Engineer

[![GitHub](https://img.shields.io/badge/GitHub-AdrianEnsslin-181717?style=flat&logo=github)](https://github.com/AdrianEnsslin)

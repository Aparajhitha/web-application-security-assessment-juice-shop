#  Web Application Security Assessment – OWASP Juice Shop

##  Project Overview

This project presents a structured security assessment of **OWASP Juice Shop**, an intentionally vulnerable web application designed for security training.

The application was deployed locally using Docker and evaluated using black-box web application testing techniques to identify common security vulnerabilities.

---

##  Objectives

- Analyze authentication mechanisms
- Test access control enforcement
- Identify client-side vulnerabilities
- Evaluate API endpoint security
- Assess business logic weaknesses

---

##  Tools & Environment

- Docker (Local Deployment)
- Ubuntu (WSL)
- Browser Developer Tools
- Manual HTTP Request Analysis
- JWT Decoding Tools

---

##  Key Vulnerabilities Identified

| #  | Vulnerability                     | Severity     |
|----|----------------------------------|-------------|
| 1  | DOM-Based Cross-Site Scripting   | High        |
| 2  | JWT Storage in localStorage      | Medium      |
| 3  | Business Logic Manipulation      | Medium      |
| 4  | IDOR Testing Observations        | Low–Medium  |

---

##  Repository Structure

- `/report` → Full security assessment PDF
- `/findings` → Detailed vulnerability write-ups
- `/screenshots` → Proof-of-concept evidence
- `/methodology.md` → Testing methodology explanation

---

##  Skills Demonstrated

- Web Application Penetration Testing
- JWT Security Analysis
- Access Control Testing
- Client-Side Vulnerability Exploitation
- Vulnerability Documentation & Risk Assessment

---

##  Conclusion

This project strengthened foundational knowledge in offensive web security by applying structured testing methodologies to a real-world vulnerable application. It demonstrates practical understanding of authentication, authorization, input validation, and client-side security risks.

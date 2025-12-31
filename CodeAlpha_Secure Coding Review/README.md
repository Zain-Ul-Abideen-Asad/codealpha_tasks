Task 3 – Secure Coding Review

Internship Details

Intern Name: Zain Ul Abideen
Internship Provider: CodeAlpha
Domain: Cybersecurity

Task Overview

The objective of **Task 3: Secure Coding Review** is to analyze application source code to identify security vulnerabilities and recommend secure coding practices. This task focuses on improving application security by applying industry-standard defensive coding techniques.

Selected Technology

* Programming Language: Python
* Application Type: Simple Web Application (User Login System)
* Framework: Flask

The reviewed application performs user authentication using username and password inputs and interacts with a backend database.

Scope of Code Review

The review covered the following security areas:

* Input validation
* Authentication and authorization
* Data handling
* Error handling
* General secure coding practices

Both **manual inspection** and **static analysis concepts** were applied during the review process.

Identified Security Vulnerabilities

SQL Injection

User input was directly concatenated into SQL queries.
* Risk: Authentication bypass and data leakage.

Plaintext Password Storage

Passwords were stored and compared in plaintext.
* Risk: Full credential exposure if the database is compromised.

Lack of Input Validation

* No sanitization or validation of user input.
* Risk: Injection attacks and unstable application behavior.

Missing Error Handling

Database errors were not handled securely.
* Risk: Application crashes or information leakage.

No Authentication Rate Limiting

Unlimited login attempts allowed.
* Risk: Brute-force attacks.

Tools and Techniques Used

Manual Review

* Line-by-line code inspection
* Identification of insecure coding patterns
* Mapping issues to **OWASP Top 10** vulnerabilities

### Static Analysis Tools

* Bandit – Python security linter
* SonarQube – Code quality and security analysis
* Semgrep – Pattern-based static analysis

Recommendations & Best Practices

* Use parameterized queries to prevent SQL Injection
* Store passwords using bcrypt or Argon2 hashing
* Apply strict input validation and sanitization
* Implement secure error handling mechanisms
* Enable rate limiting and account lockout for authentication

Remediation Summary

| Vulnerability       | Risk Level | Mitigation Applied    |
| ------------------- | ---------- | --------------------- |
| SQL Injection       | High       | Parameterized Queries |
| Plaintext Passwords | High       | Password Hashing      |
| Input Validation    | Medium     | Validation Rules      |
| Error Handling      | Medium     | Secure Error Messages |
| Brute Force Risk    | Medium     | Rate Limiting         |

---

Files Included

Secure_Coding_Review_Report.pdf
Source code snippets (vulnerable and remediated examples)

📌 *Submitted as part of the CodeAlpha Cybersecurity Internship – Task 3*

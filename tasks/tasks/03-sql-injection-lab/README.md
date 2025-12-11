# Task 3 – SQL Injection (Vulnerable Test Application)

## Challenge

Use SQL Injection against a deliberately vulnerable web application and extract information from the backend database.

Target (training environment):
http://testphp.vulnweb.com/search.php?test=query

This site is intentionally insecure and used globally for ethical hacking practice.

---

## Approach (High-Level, Ethical Summary)

> ⚠️ Only use SQL Injection techniques on authorized lab targets.

1. Identify an input parameter that is reflected in a database query.
2. Test for SQL Injection using:
   - `'` to trigger SQL errors
   - `' OR 1=1 --` for boolean-based testing
3. Confirm that the application does not sanitize user input.
4. Use safe enumeration (no exploitation) to understand the database behavior.

---

## Example Payloads

' OR 'a'='a

Tools Used

Browser Developer Tools

Kali Linux

Basic SQL Injection payloads

Key Learning

How SQL Injection vulnerabilities form

Why user input must be sanitized

Importance of using prepared statements
```sql
' OR 1=1 --

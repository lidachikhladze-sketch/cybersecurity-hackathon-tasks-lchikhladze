# Task 3 – SQL Injection (Vulnerable Test Application)

## Challenge

Use SQL Injection against a deliberately vulnerable web application and extract information from the backend database.

Target (training environment): http://testphp.vulnweb.com/search.php?test=query


This site is intentionally insecure and used globally for ethical hacking practice.

---

## Approach (High-Level, Ethical Summary)

> ⚠️ Only use SQL Injection techniques on *authorized* lab targets.

1. Identify an input parameter that is reflected in a database query:
   - Example: `search.php?test=book`

2. Test for SQL Injection indicators:
   - Add a `'` character → see if an SQL error occurs.
   - Try boolean-based tests:
     - `' OR '1'='1`
     - `' OR 1=1 --`

3. Determine whether the application fails to sanitize user-controlled input.

4. Confirm injection by manipulating query logic and observing changed results.

5. Use the vulnerability to enumerate database information  
   (tables, columns, or data — depending on what the training environment allows).

---

## Example Test Payloads


```sql
' OR 1=1 --

' OR 'a'='a

Tools Used

Browser Developer Tools

Kali Linux

Basic SQL Injection payload testing

Key Learning

How SQL Injection works in vulnerable systems

How input validation failures allow attackers to alter database queries

Importance of:

using prepared statements,

parameterized queries,

proper sanitization

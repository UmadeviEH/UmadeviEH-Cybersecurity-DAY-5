# UmadeviEH-Cybersecurity-DAY-5

TOPIC : SQL(Structured Query Language)

What is SQL?

📚 SQL – Important Theory Notes

🔹 1. What is SQL?
SQL (Structured Query Language) is the standard language for storing, managing, and retrieving data from relational databases.

It’s declarative, meaning you describe what you want, not how to do it.

SQL is supported by almost all major RDBMSs like MySQL, PostgreSQL, Oracle, Microsoft SQL Server, and SQLite.


| Command  | Purpose       | Example                                    |
| -------- | ------------- | ------------------------------------------ |
| `SELECT` | Retrieve data | `SELECT name FROM users;`                  |
| `INSERT` | Add new data  | `INSERT INTO users(name) VALUES('John');`  |
| `UPDATE` | Modify data   | `UPDATE users SET name='Jane' WHERE id=1;` |
| `DELETE` | Remove data   | `DELETE FROM users WHERE id=1;`            |

WHERE → Filters data
SELECT * FROM users WHERE age > 18;

ORDER BY → Sorts results
SELECT * FROM users ORDER BY age DESC;

GROUP BY → Groups rows by column
SELECT department, COUNT(*) FROM employees GROUP BY department;

HAVING → Filters groups
SELECT department, COUNT(*) FROM employees GROUP BY department HAVING COUNT(*) > 5;

READ →
SELECT name, email FROM users WHERE active = 1 ORDER BY created_at DESC;

INSERT →
INSERT INTO users(name, email) VALUES ('Asha', 'asha@example.com');

UPDATE →
UPDATE users SET last_login = NOW() WHERE id = 42;

DELETE →
DELETE FROM users WHERE id = 999;

🔹 SQL in Cybersecurity
SQL is often a target for SQL Injection attacks.

Understanding SQL is crucial for penetration testing, secure coding, and data forensics.

Ethical hackers use SQL knowledge to identify vulnerabilities, while developers use it to fix them.

🔹What: SQLi happens when user input is concatenated into SQL and executed — attacker manipulates the query.

→ Principles to prevent:

Always use parameterized queries / prepared statements (never string-concatenate user input).

Least privilege: app DB user should have only needed permissions (no DROP, no SUPER).

Input validation & output encoding: validate types/lengths; escape only where necessary.

Use ORM or safe DB libs but still parameterize raw queries.

Hide verbose DB errors from users; log them securely instead.

WAF & rate limits: layer defense for volumetric attacks.

Audit & monitoring: detect odd queries, sudden dumps, or abnormal patterns.

Transport security: use TLS for DB connections where available.







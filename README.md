### Vulnerable SQL statement with concatenated strings:

``` sql
"SELECT * FROM users WHERE username = '" + username + "' AND password = '" + password + "'";
```
This type of SQL statement is vulnerable to SQL injection if the input values for username and password are not properly sanitized or validated before being concatenated into the query string. An attacker can manipulate the input values to inject malicious SQL code and potentially gain unauthorized access to the database.

### Vulnerable SQL statement with unsanitized input:

``` sql
"SELECT * FROM users WHERE username = '" + username + "'";
```
his type of SQL statement is vulnerable to SQL injection if the input value for 'username' is not properly sanitized or validated before being used in the query. An attacker can manipulate the username input to inject malicious SQL code and potentially gain unauthorized access to the database.

### Vulnerable SQL statement using outdated and vulnerable functions:

``` sql
"SELECT * FROM users WHERE username = '" + username + "' AND password = MD5('" + password + "')";
```
This type of SQL statement is vulnerable to SQL injection if it uses outdated and vulnerable functions like 'MD5' for hashing passwords. These functions are considered weak and can be easily exploited by attackers using various techniques, including brute force and rainbow table attacks.

It's important to note that intentionally exploiting vulnerabilities in any system without proper authorization is illegal and unethical. Always follow ethical guidelines and obtain proper authorization before performing any security testing or penetration testing activities. If you suspect a vulnerability in a system, report it to the system owner or administrator immediately.

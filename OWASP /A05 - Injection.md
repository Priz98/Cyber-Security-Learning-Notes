# A05 - Injection

## What is an Injectionin Attack?

Injection attacks occur when a vulnerable input field allows an attacker to send malicious input to an application's interpreter.
The application mistakenly treats the attacker's input as a command or part of a command instead of normal data.
This can allow attackers to perform unintended actions such as reading data, modifying data, bypassing authentication, or executing commands.

## An application is vulnerable to attack when:

1. Potentially hostile user input is directly concatenated into SQL queries, commands, or stored procedures.

2. Dynamic queries are created using user input instead of parameterized queries or prepared statements.
3. User-controlled data is passed directly to an interpreter without proper validation or sanitization.
4. Non-parameterized database calls are used, allowing attacker input to alter the structure of a query.
5. Unsanitized data is used within Object Relational Mapping (ORM) search parameters, potentially exposing additional sensitive records.
6. Special characters and commands are not properly escaped before being processed by the interpreter.
7. The application fails to distinguish between user data and executable commands.
8. Input validation is missing, weak, or inconsistent across different parts of the application.
9. Stored procedures or commands dynamically generate queries using user input.
10. User input reaches SQL databases, operating system commands, LDAP queries, NoSQL queries, or other interpreters without proper protections.

## Prevention Measures for Injection Vulnerabilities

1. Keep user data separate from commands and queries at all times.

2. Use parameterized queries or prepared statements to ensure user input is treated as data and not executable commands.
3. Use safe APIs that avoid direct interaction with interpreters whenever possible.
4. Use Object Relational Mapping (ORM) frameworks correctly to reduce the risk of injection vulnerabilities.
5. Stored procedures should not dynamically generate queries using user input, as they can still be vulnerable to injection attacks.
6. Apply positive server-side input validation to ensure only expected input formats are accepted.
7. Validate all user input before it reaches an interpreter.
8. Escape special characters using the correct escaping mechanism for the specific interpreter when dynamic queries cannot be avoided.
9. Never allow user input to define SQL structures such as table names, column names, or other query components.
10. Treat escaping and filtering as additional protection rather than the primary defense, as they can be error-prone and may fail when applications or systems change.
11. Ensure that user input reaching SQL databases, operating system commands, LDAP queries, NoSQL queries, or other interpreters is properly validated and protected.
12. Always ensure the interpreter can distinguish between user data and executable commands.


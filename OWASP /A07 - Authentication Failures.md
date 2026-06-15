# A07 - Authentication Failures

## What is an Authentication Failures 

When an attacker tricks the system into recognizing an invalid or inccorect user as legitimate, then it is considered as Authentication Failure.

## The ways in which an Authentication Failures may occurs are : 

1. The application allows automated attacks such as credential stuffing, where attackers use usernames and passwords leaked from previous data breaches to gain unauthorized access.

2. The application allows hybrid password attacks, where attackers try common password variations such as Password1!, Password2!, Password3!, and so on.

3. The application does not properly detect or block brute force attacks and other automated login attempts.

4. Weak, default, or commonly used credentials such as "admin/admin" or "Password1" are permitted.

5. Users are allowed to create accounts using passwords that are already known to have been exposed in previous data breaches.

6. Password recovery mechanisms rely on weak methods such as security questions or knowledge-based answers, which may be guessed or discovered through OSINT.

7. Passwords are stored in plaintext, encrypted form, or using weak hashing algorithms instead of strong adaptive hashing functions.

8. Multi-Factor Authentication (MFA) is missing or implemented ineffectively.

9. Weak fallback mechanisms allow authentication even when MFA is unavailable, reducing the effectiveness of MFA.

10. Session identifiers are exposed through URLs, hidden fields, or other insecure locations accessible to clients.

11. The application reuses the same session identifier after successful authentication, increasing the risk of session fixation attacks.

12. User sessions or authentication tokens are not properly invalidated after logout or long periods of inactivity.

13. Credentials or tokens are accepted without verifying their intended audience, scope, or issuer, potentially allowing unauthorized access across different services.

## Prevention Measures for Authentication Failures

1. Implement and enforce Multi-Factor Authentication (MFA) wherever possible to reduce the risk of credential stuffing, brute force attacks, and stolen credential reuse.

2. Encourage and support the use of password managers so users can generate and store strong, unique passwords.

3. Do not deploy applications with default credentials, especially for administrative accounts.

4. Implement weak password checks and block commonly used passwords such as those found in lists of the top 10,000 worst passwords.

5. Validate new or changed passwords against databases of known breached credentials to prevent password reuse.

6. Follow modern password policies such as NIST guidelines regarding password length, complexity, and storage.

7. Do not force periodic password changes unless there is evidence or suspicion of a credential compromise.

8. Registration, login, and password recovery processes should use generic error messages to prevent account enumeration attacks.

9. Limit or delay repeated failed login attempts to reduce brute force attacks while avoiding denial-of-service scenarios.

10. Log authentication failures and alert administrators when suspicious login activity or automated attacks are detected.

11. Use secure server-side session management that generates new random session identifiers after successful login.

12. Session identifiers should be stored in secure cookies and should never be exposed in URLs or other insecure locations.

13. Invalidate sessions and authentication tokens after logout, inactivity, or timeout periods.

14. Use trusted and well-tested authentication and identity management solutions whenever possible.

15. Verify the issuer, audience, scope, and intended use of credentials or tokens before granting access.




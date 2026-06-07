# A01 - Broken Access Control. 

## What is A01 ? 

Broken Access Control is where a user gets access of a data or service that they should not have the access of normally. Which is an anomily
Also, 100% of the applications tested by OWASP were found to have some form of broken access control.

Notable CWE (The weakness that can be exploited were)

## There are various ways that can cause a Broken Access Control

1. Violation following the principle of least privilege.
2. URL tampering to access unauthorized objects or pages.
3. Accessible API with missing access controls for POST, PUT, and DELETE.
4. Tampering and Misusing JWTs.
5. CORS misconfiguration allows API access from unauthorized or untrusted origins.
6. Force browsing

## Prevention

1. Deny access by default.
2. Enforce server-side access control checks.
3. Follow the principle of least privilege.
4. Disable directory listing and metadata exposure.
5. Log access control failures and monitor them.

## Attack Example

An application puts all of their access control in their front-end. While the attacker cannot get to https://example.com/app/admin_getappInfo due to JavaScript code running in the browser, they can simply execute:

$ curl https://example.com/app/admin_getappInfo
from the command line.

## CWE References

CWE 200, CWE 201, CWE 918, CWE 352 and etc 


ref page. https://owasp.org/Top10/2025/A01_2025-Broken_Access_Control/

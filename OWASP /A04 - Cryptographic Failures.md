# A04 : Cryptographic Failures

## What is Cryptographic Failure

Cryptographic Failure is considered when there is a lack of Encryption, Insuffiently Strong Encrpytion, Lack for Proper Key Management, and etc.

## What causes Cryptographic Failures?

1. Old or Weak cryptographic Encryptions or Protocols still being used by defualt or in older codes.
2. Usage of old or weak keys, Reusing exact same keys at multiple places. Or Usage of default keys.
3. Lack of Proper Key Management or key rotation.
4. Encryption keys should never be stored directly inside source code repositories.
5. Even if encryption exists, it must be enforced. Security headers such as HSTS should be used to ensure browsers always communicate using HTTPS and do not fall back to insecure HTTP connections.
6. The received server certificate and the **trust chain** should come from a valid Source.
7. Are **initialization vectors** ignored, reused, or not generated sufficiently secure for the cryptographic mode of operation?
8. Is an insecure mode of operation such as ECB in use? Is encryption used when authenticated encryption is more appropriate?
9. Passwords should not be used directly as cryptographic keys because passwords are often weak and predictable. A Key Derivation Function (KDF) such as PBKDF2, bcrypt, scrypt, or Argon2 should be used to convert the password into a stronger cryptographic key and make brute-force attacks more difficult.

10. Are deprecated hash functions such as MD5 or SHA1 in use, or are non-cryptographic hash functions used when cryptographic hash functions are needed?
11. Are cryptographic error messages or side channel information exploitable, for example in the form of padding oracle attacks?
12. Can the cryptographic algorithm be downgraded or bypassed?
13. Cryptographic systems should use cryptographically secure random number generators. Predictable values such as timestamps, user IDs, or manually chosen seeds should not be used because attackers may be able to predict encryption keys, tokens, IVs, or other security-related values. The operating system's secure randomness should generally be trusted instead of replacing it with weaker custom seeds.

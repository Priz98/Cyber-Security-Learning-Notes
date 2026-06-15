# A08 -  Software and Data Integrity Failure 

## What is Software and Data Integrity Failure?

Software or Data Integrity Failures occur when an application assumes that software, updates, code, or data are trustworthy without properly verifying them. If attackers are able to modify or tamper with these components, the application may execute malicious code or use altered data, resulting in security vulnerabilities.

# Software or Data Integrity Failures may cause if 

1. Software updates, plugins, or packages are installed without verifying their integrity or authenticity using digital signatures or hashes.

2. Applications automatically download and execute software updates from untrusted or compromised sources.

3. Code or scripts are loaded from third-party or untrusted locations without proper verification.

4. Applications blindly trust data received from clients, APIs, or external systems without validating its integrity.

5. Serialized data from untrusted sources is deserialized without validation, potentially leading to malicious code execution.

6. Integrity checks such as hashes, checksums, or digital signatures are missing or not properly verified.

7. CI/CD pipelines are insecure, allowing attackers to modify build artifacts or deployed applications.

8. Sensitive software artifacts, packages, or repositories can be modified by unauthorized users.

9. Applications permit mass assignment or uncontrolled modification of object attributes based on user input.

10. Security boundaries between trusted and untrusted systems are not properly enforced.

11. Configuration files, dependencies, or critical data can be modified without detection.

12. Applications assume software, updates, or data are trustworthy without verifying their origin and integrity.

## Prevention Measures for Software or Data Integrity Failures

1. Use digital signatures, hashes, or similar integrity mechanisms to verify that software or data comes from a trusted source and has not been modified.

2. Obtain libraries, packages, and dependencies only from trusted repositories and official sources. High-risk environments should consider maintaining an internal trusted repository.

3. Establish a review and approval process for code and configuration changes to reduce the risk of introducing malicious or unauthorized modifications.

4. Secure the CI/CD pipeline using proper access controls, segregation of duties, and secure configurations to maintain the integrity of software throughout the build and deployment process.

5. Do not accept or process unsigned or unverified serialized data from untrusted sources. Integrity checks or digital signatures should be used to detect tampering or replay attacks.

6. Verify the integrity of software updates, build artifacts, and critical files before execution or deployment.

7. Enforce trust boundaries between trusted and untrusted systems and validate data crossing those boundaries.

8. Continuously monitor and protect repositories, artifacts, and critical data against unauthorized modifications.


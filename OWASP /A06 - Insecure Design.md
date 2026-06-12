# A06 - Insecure Design

## What is Insecure Design?

Insecure Design occurs when security requirements and business risks are not properly considered during the design phase of a software or system. 
As a result, necessary security controls are never created to defend against potential attacks.
Unlike implementation flaws, insecure design cannot be fixed by writing perfect code, 
because the required security mechanisms were never included in the design itself.

## Three key parts of having a secure design are:

1. Gathering Requirements and Resource Management
 
2. Creating a Secure Design

3. Having a Secure Development Lifecycle

## Gathering Requirements and Resource Management

1. Collect and negotiate the business requirements for an application with the business.
2. Take into account how exposed your application will be and if you need segregation of tenants.
3. Compile the technical requirements, including functional and non-functional security requirements.

## Secure Design

1. Secure design is a security-first culture and methodology in which threats, risks, and possible attack paths are continuously evaluated during the software development lifecycle.
2. Security should be considered from the design phase itself rather than being added later as an afterthought.
3. Threat modeling should be performed regularly to identify possible attacks, changes in data flow, access controls, and other security mechanisms.
4. During feature development, both expected behavior and failure scenarios should be identified and agreed upon by all stakeholders.
5. Assumptions made during development should be validated to ensure that the application behaves securely even under unexpected conditions.
6. Security requirements, controls, and decisions should be properly documented throughout the development process.
7. Teams should continuously learn from past mistakes and improve their security practices.
8. Secure design is not a tool or an add-on that can be added later; it is a continuous process and culture that must be integrated throughout the entire software development lifecycle.

## Secure Software Development

1. Secure software requires a secure Software Development Lifecycle (SDLC), where security is considered at every stage of development, deployment, and maintenance.
2. Secure design patterns should be used to implement common functionalities in a secure and standardized manner.
3. A paved road methodology should be followed, where developers are provided with secure and approved tools, frameworks, and processes by default.
4. Use trusted and secure component libraries to reduce the risk of introducing vulnerabilities into the application.
5. Appropriate security tools such as static analysis, dependency scanning, and monitoring tools should be integrated into the development process.
6. Threat modeling should be performed regularly to identify possible attack paths and security weaknesses before implementation.
7. Incident post-mortems should be conducted after security incidents to understand their root cause and improve future security practices.
8. Security specialists should be involved from the beginning of the project, throughout development, and during ongoing maintenance.
9. Security is a continuous process and should be maintained throughout the entire lifecycle of the software.
10. Consider using the OWASP Software Assurance Maturity Model (SAMM) to help structure your secure software development efforts.

## Prevention Measures for Insecure Design

1. Establish and follow a secure Software Development Lifecycle (SDLC) with security professionals involved in designing and reviewing security controls.
2. Use secure design patterns and approved secure components to ensure common functionalities are implemented safely.
3. Perform threat modeling for critical areas such as authentication, access control, business logic, and important data flows.
4. Use threat modeling as a learning tool to build a security-first mindset among developers.
5. Integrate security requirements and controls into user stories during feature planning and development.
6. Apply plausibility checks and validations at every layer of the application, from the frontend to the backend.
7. Write unit tests and integration tests to verify that important workflows remain secure against expected threats and misuse cases.
8. Segregate application tiers and network layers based on their security and exposure requirements.
9. Isolate tenants and customer data throughout all layers of the system to prevent unauthorized access between users or organizations.

## OWASP's Attack Scenario 

A retail chain’s e-commerce website does not have protection against bots run by scalpers buying high-end video cards to resell on auction websites. This creates terrible publicity for the video card makers and retail chain owners, and enduring bad blood with enthusiasts who cannot obtain these cards at any price. Careful anti-bot design and domain logic rules, such as purchases made within a few seconds of availability, might identify inauthentic purchases and reject such transactions.

## My undertanding

Due to the improperly designed software logic the application allowed bots to make instanious purchases. Which later created bad relation between the products manifaturer and the application's company.


# A03 Software Suppy Chain Failure

A Software supply chain failure occurs where any used component is vulnerable or compromised in any phase of the SDLC, namely production, deployment, or updatation of the software, Which later cause a vulnerabilty.

## Causes of Software Suppy Chain Failure

1. Not properly tracking all components and dependencies used in the application, including both direct and transitive dependencies.
2. Using outdated, unsupported, vulnerable, or legacy software components such as operating systems, frameworks, libraries, APIs, databases, and runtime environments.
3. Poor change management. Changes to repositories, IDEs, extensions, build environments, libraries, and other supply chain components are not properly tracked or documented.
4. Not regularly scanning components for known vulnerabilities or keeping track of security advisories and bulletins.
5. Lack of proper hardening throughout the supply chain.
6. Lack of separation of duties.
7. Delayed patching and upgrades, leaving known vulnerabilities exposed for long periods of time.
8. Using components, libraries, services, or tools from untrusted sources.
9. Updated or patched components are deployed without testing compatibility with the existing application.
10. Security configurations are not properly maintained across all parts of the system.
11. The CI/CD pipeline is less secure than the systems it builds and deploys, making it a potential target for attackers.

## Prevention Measures for these Vulnerabilites

1. Make a log of all the applications, products, frameworks, dependencies, directories and everything used to create the software, this is called a SBOM. Software Bill of Materiale. It helps organizations quickly identify whether they are affected when a vulnerability is discovered in a component and makes dependency tracking and security management easier.

2. Track not just your direct dependencies, but their (transitive) dependencies, and so on.
3. Reduce attack surface by removing unused dependencies, unnecessary features, components, files, and documentation.
4. Continuously check the versions of both client-side and server-side components and their dependencies using tools like OWASP Dependency Track.
5. Continuously monitor sources like Common Vulnerability and Exposures for vulnerabilities in the components you use.
6. Only obtain components from official sources over secure links. Prefer signed packages to reduce the chance of including a modified, malicious component.
7. Update your CI/CD, IDE, and any other developer tooling regularly.
8. Avoid deploying updates to all systems simultaneously. Use staged rollouts or canary deployments to limit exposure in case a trusted vendor is compromised.
9. There should be a change management process or tracking system in place to track changes to:

    a. CI/CD settings (all build tools and pipelines)

    b. Code repositories

    c. Sandbox areas

        Developer IDEs

        SBOM tooling, and created artifacts

        Logging systems and logs

        Third party integrations, such as SaaS

        Artifact repositories

        Container registries

10. Hardening the following systems are neccessary requirements:

Code repository

Developer workstations

Built server & CI/CD

Artifacts (ensure integrity via provenance, signing, and time stamping, promote artifacts rather than rebuilding for each environment, ensure 
builds are immutable)


# **Build In Security**

## Definition

Teams that build security in have security requirements written into user stories' acceptance criteria not added later and a separate story.  They work to address security risks is prioritized and completed effectively.  

## How to I achieve Build In Security?

Because the bad guys are always working harder to find new ways to attack us security efforts always need to be reviewed. While this list is not comprehensive and does not replace vigilance, it is important that:

1. Secrets are managed with a secrets management service.
2. Dependencies in platform, code, and tooling are patched regularly, preferably using an automated dependency checker.
3. The principle of least privilege is followed, ensuring identities only have the minimal set of permissions necessary to complete their required tasks.
4. Systems are analyzed to ensure threats have compensating controls to prevent unintended usage.
5. Complexity in configuration is addressed by building best practices into reusable templates or platform offerings.

## How do I measure outcomes of Build In Security?

## Crawl - Walk - Run

| Phase | Activity | Measure |
| ----- | -------- | ------- |
| **Crawl** | * Secrets are managed in the secrets management service. |  |
| **Walk** | * Repositories are configured to have security vulnerabilities scanned. |  |
| **Run** | * Team regularly reviews the security advisories for the technologies their components use. |  |

Team implements a baseline of security controls e.g. OWASP ASVS or a Grainger Secure Delivery Checklist

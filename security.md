# FBSPL Frontend Security Policy

## Supported Versions

Security fixes are applied to the actively maintained production version
and supported development branches.

| Version | Supported |
|--------|-----------|
| Production | Yes |
| Development | Yes |
| Older releases | No |

---

## Reporting a Vulnerability

If you discover a security vulnerability, do not create a public GitHub issue.

Report the vulnerability privately to the FBSPL IT/Security team.

Include:

- Vulnerability description
- Affected component
- Affected version/commit
- Steps to reproduce
- Proof of concept, if available
- Potential impact
- Suggested remediation, if known

---

## Security Issues

Examples include:

- Authentication bypass
- Authorization problems
- SQL injection
- Cross-site scripting
- Remote code execution
- Sensitive information disclosure
- Exposed credentials
- API security issues
- Dependency vulnerabilities
- Container vulnerabilities
- CI/CD security issues
- Infrastructure security issues

---

## Secret Exposure

If a password, API key, private key, AWS credential, token, or other secret
is accidentally committed:

1. Do not reuse the exposed credential.
2. Immediately revoke or rotate it.
3. Notify the FBSPL IT/Security team.
4. Remove the secret from the repository.
5. Review GitHub audit logs.
6. Check whether the credential was accessed or abused.

Deleting the secret from the latest commit alone is not sufficient if it
exists in Git history.

---

## Security Scanning

The repository uses security controls including:

- GitHub CodeQL
- GitHub Dependabot
- GitHub Dependency Review
- Gitleaks
- pnpm audit
- Trivy filesystem scanning
- Trivy configuration scanning
- Trivy container image scanning

Critical and high-risk findings should be remediated before production
deployment according to the organization's security policy.

---

## Production Deployment

Production deployment requires:

1. Pull request review
2. Required security checks
3. Required code-owner approval where applicable
4. Production environment approval
5. Successful deployment health check

---

## Responsible Disclosure

Security vulnerabilities should be reported privately so that the FBSPL
team has an opportunity to investigate and remediate the issue before
public disclosure.

# Security Policy

## 🔒 Repository Access

This is an **invite-only** repository. Access is restricted to:
- Vetted Columbia University students
- Approved external collaborators
- Faculty advisors

**Unauthorized access attempts will be reported to Columbia University's security team.**

## 🛡️ Reporting Security Vulnerabilities

If you discover a security vulnerability in this repository:

### For Members

1. **Do NOT** open a public issue
2. **Do NOT** commit sensitive information
3. **Do** contact the core team privately through:
   - Direct message to core team members
   - Email to repository maintainers
   - Columbia University security channels

### What to Report

Report any of the following:
- Code vulnerabilities that could be exploited
- Exposed credentials or API keys
- Insecure data handling
- Dependency vulnerabilities
- Access control issues

### Response Timeline

- **Initial Response:** Within 48 hours
- **Status Update:** Within 1 week
- **Resolution Target:** Depends on severity

## 🔐 Security Best Practices

All members must follow these security practices:

### Code Security

- **Never** commit credentials, API keys, or secrets
- Use environment variables for sensitive configuration
- Review dependencies for known vulnerabilities
- Keep dependencies up to date
- Use `.gitignore` to exclude sensitive files

### Data Security

- **Never** commit personally identifiable information (PII)
- Anonymize datasets before committing
- Store large or sensitive datasets externally
- Use encryption for sensitive data at rest
- Follow Columbia's data handling policies

### Access Security

- **Never** share your GitHub credentials
- **Never** grant repository access to non-members
- Use strong, unique passwords
- Enable two-factor authentication (2FA)
- Revoke access immediately when leaving the project

### Research Data

- Follow IRB protocols if working with human subjects data
- Respect data use agreements and licenses
- Document data provenance and handling
- Secure API keys for LLM services

## 🚨 Incident Response

If a security incident occurs:

1. **Immediate:** Revoke compromised credentials
2. **Notify:** Alert core team and affected parties
3. **Assess:** Determine scope and impact
4. **Remediate:** Fix vulnerabilities
5. **Document:** Record incident and response
6. **Report:** File reports with Columbia if required

## 🔍 Security Audits

The repository undergoes regular security reviews:
- Code reviews for all pull requests
- Dependency vulnerability scans
- Access audit quarterly
- Security training for new members

## 📋 Compliance

All members must comply with:
- Columbia University Information Security Policy
- Columbia University Acceptable Use Policy
- FERPA (if handling student data)
- GDPR/CCPA (if handling EU/CA resident data)
- Export control regulations (for certain AI technologies)

## 🚫 Prohibited Actions

The following are strictly prohibited:
- Committing secrets or credentials
- Sharing repository access
- Bypassing security controls
- Using the repository for unauthorized purposes
- Storing regulated data without proper controls

## 📞 Security Contacts

- **Core Team:** See CONTRIBUTORS.md
- **Columbia IT Security:** https://cuit.columbia.edu/security
- **GitHub Security:** security@github.com (for platform issues)

## ✅ Security Checklist for Contributors

Before committing code:
- [ ] No secrets or credentials in code
- [ ] No PII or sensitive data
- [ ] Dependencies are up to date
- [ ] Code follows secure coding practices
- [ ] `.env` files are in `.gitignore`
- [ ] API keys use environment variables

## 🔄 Updates to This Policy

This security policy may be updated as needed. Members will be notified of significant changes.

---

**Last Updated:** 2025-11-11

**Remember:** Security is everyone's responsibility. When in doubt, ask!

*Roar, Lions, Roar! 🦁*

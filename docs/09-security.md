# Security

Backup infrastructure protects the organization's most valuable asset—its data. As a result, backup systems have become a primary target for ransomware groups and other malicious actors.

If an attacker compromises both the production environment and the backup infrastructure, recovery may become impossible.

For this reason, backup security should be treated with the same level of importance as identity management, virtualization platforms and firewalls.

---

## Security by Design

Backup security should be incorporated into the architecture from the beginning rather than added later.

Enterprise backup environments should be designed around:

- least privilege;
- defense in depth;
- network segmentation;
- immutable storage;
- strong authentication;
- continuous monitoring.

A secure backup environment assumes that production systems may eventually be compromised.

---

## Ransomware Protection

Modern ransomware rarely encrypts only production systems.

Attackers increasingly attempt to:

- delete backup jobs;
- encrypt repositories;
- remove restore points;
- steal credentials;
- disable monitoring;
- destroy recovery infrastructure.

Organizations should therefore design backup systems assuming that backup infrastructure itself will become a target.

---

## Immutable Backups

Immutable storage is one of the most effective defenses against ransomware.

An immutable backup cannot be modified or deleted before its retention period expires.

Benefits include:

- protection against malicious deletion;
- protection against compromised administrator accounts;
- improved compliance;
- guaranteed recovery points.

Where supported, immutable repositories should become part of every enterprise backup architecture.

---

## Multi-Factor Authentication

Administrative accounts should always be protected by Multi-Factor Authentication (MFA).

Passwords alone are no longer sufficient.

MFA significantly reduces the risk of:

- credential theft;
- phishing;
- password reuse;
- brute-force attacks.

Administrative access to backup infrastructure should follow the same security standards as identity services and virtualization platforms.

---

## Least Privilege

Backup administrators should receive only the permissions necessary to perform their responsibilities.

Examples include:

- backup operators;
- repository administrators;
- infrastructure administrators;
- auditors.

Separating responsibilities reduces the impact of compromised accounts and accidental configuration changes.

---

## Network Segmentation

Backup infrastructure should be isolated from user and production networks whenever practical.

A common enterprise architecture is:

```text
Users
   │
Production Network
   │
Firewall
   │
Backup Network
   │
Backup Infrastructure
```

Limiting network exposure reduces the attack surface and simplifies access control.

---

## Encryption

Backup data frequently contains confidential business information.

Organizations should encrypt:

- backup repositories;
- backup traffic;
- archive media;
- cloud repositories.

Encryption keys should be protected separately from the backup data itself.

Losing encryption keys may render backups permanently unrecoverable.

---

## Credential Protection

Backup systems often require privileged credentials.

Examples include:

- virtualization accounts;
- Microsoft 365 accounts;
- database credentials;
- cloud access keys;
- storage authentication.

Credentials should never be:

- hardcoded into scripts;
- shared between administrators;
- stored in plain text.

Regular credential rotation should form part of normal operational procedures.

---

## Monitoring Backup Security

Backup environments should be monitored continuously.

Important security events include:

- failed login attempts;
- repository changes;
- disabled backup jobs;
- deleted restore points;
- storage capacity anomalies;
- failed replication.

Early detection allows administrators to respond before backup integrity is affected.

---

## Backup Infrastructure Updates

Keeping backup software up to date reduces exposure to known vulnerabilities.

Updates should follow a structured process:

1. Review release notes.
2. Test updates where possible.
3. Verify backups.
4. Schedule a maintenance window.
5. Validate backup operations after completion.

Regular maintenance improves both security and operational stability.

---

## Incident Response

If backup infrastructure is suspected of being compromised:

1. Isolate affected systems.
2. Preserve forensic evidence.
3. Protect immutable repositories.
4. Verify backup integrity.
5. Restore only after the environment has been secured.

Recovering from compromised backups without understanding the cause may reintroduce the original threat.

---

## Common Mistakes

Frequently encountered security weaknesses include:

- storing backups on production servers;
- sharing administrative accounts;
- disabling MFA;
- exposing repositories directly to users;
- failing to implement immutable storage;
- never reviewing backup logs.

Most successful attacks exploit operational weaknesses rather than backup software vulnerabilities.

---

## Enterprise Recommendation

Assume that attackers will eventually reach your backup environment.

Design backup infrastructure so that compromising a single administrator account, server or repository cannot destroy every recovery point.

Security should delay attackers, limit their impact and preserve the organization's ability to recover.

---

## Enterprise Checklist

- [ ] MFA enabled
- [ ] Least-privilege access implemented
- [ ] Backup network segmented
- [ ] Immutable storage configured
- [ ] Repository encryption enabled
- [ ] Credentials protected
- [ ] Security monitoring implemented
- [ ] Software updated regularly
- [ ] Incident response procedures documented

---

## Summary

Backup security is fundamental to organizational resilience.

By combining immutable storage, strong authentication, least-privilege access, encryption and continuous monitoring, organizations can significantly reduce the risk of losing both production systems and recovery capabilities during a cyberattack.

The next chapter explores monitoring and explains how backup infrastructure should be continuously observed to ensure successful protection and rapid incident response.

[Next: Monitoring →](10-monitoring.md)

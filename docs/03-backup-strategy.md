# Backup Strategy

A backup strategy defines how an organization protects its data against loss, corruption and unplanned outages. It determines what should be backed up, how often backups should occur, where backup copies are stored and how recovery will be performed when an incident occurs.

Without a documented strategy, backups often become inconsistent, difficult to verify and unreliable during emergencies.

An effective backup strategy balances business requirements, operational costs and acceptable recovery objectives.

---

## Defining Backup Objectives

Every backup strategy should begin with business requirements rather than technical capabilities.

Before selecting software or storage, organizations should answer questions such as:

- Which systems are business-critical?
- How much data loss is acceptable?
- How quickly must systems be restored?
- How long should backup copies be retained?
- Which legal or regulatory requirements apply?

These objectives influence every architectural decision that follows.

---

## The 3-2-1 Rule

The **3-2-1 Rule** has long been considered the foundation of enterprise backup design.

It recommends maintaining:

- **3 copies** of data
- stored on **2 different media**
- with **1 copy kept off-site**

A simplified example:

```text
Production Data
      │
      ├── Primary Backup (Local Repository)
      │
      └── Secondary Backup (Off-site Repository)
```

This approach protects against hardware failures, accidental deletion and site-level disasters.

Although introduced many years ago, the principle remains relevant today.

---

## The Modern 3-2-1-1-0 Rule

Modern cyber threats require additional protection.

The enhanced **3-2-1-1-0 Rule** extends the traditional model:

- **3** copies of data
- **2** different storage media
- **1** off-site copy
- **1** immutable or offline copy
- **0** backup verification errors

The additional immutable copy protects backup data from ransomware and malicious deletion, while the zero-error principle emphasizes continuous backup validation.

This model is now widely regarded as the enterprise best practice.

---

## Backup Types

Most organizations combine multiple backup methods.

### Full Backup

A full backup copies all selected data.

Advantages:

- simplest recovery;
- complete backup set;
- independent restore.

Disadvantages:

- longest backup window;
- highest storage consumption.

---

### Incremental Backup

An incremental backup stores only changes since the previous backup.

Advantages:

- fast backups;
- reduced storage usage;
- efficient daily operation.

Disadvantages:

- recovery depends on multiple backup points.

Incremental backups are commonly used for daily protection.

---

### Differential Backup

A differential backup stores all changes since the last full backup.

It represents a compromise between full and incremental approaches.

Although less common in modern enterprise environments, it remains useful in specific operational scenarios.

---

## Backup Frequency

Backup schedules should align with Recovery Point Objectives.

Examples include:

| Workload | Typical Frequency |
|----------|-------------------|
| Financial databases | Every 15–30 minutes |
| Virtual machines | Hourly or daily |
| File servers | Daily |
| Microsoft 365 | Multiple times per day |
| Archive systems | Weekly |

There is no universal schedule.

Frequency should always reflect business requirements.

---

## Retention Policies

Retention determines how long backup data remains available.

A common enterprise policy might include:

- daily backups retained for 30 days;
- weekly backups retained for 3 months;
- monthly backups retained for 12 months;
- yearly archives retained for several years.

Retention should satisfy both operational and regulatory requirements while remaining financially sustainable.

---

## Immutable Backups

One of the most significant developments in backup strategy is immutable storage.

Immutable backups cannot be modified or deleted during a predefined retention period.

This provides strong protection against:

- ransomware;
- accidental deletion;
- insider threats;
- compromised administrative accounts.

Where possible, immutable storage should become a standard component of enterprise backup architecture.

---

## Offline and Off-site Protection

Local backups alone are insufficient.

Organizations should maintain copies outside the production environment.

Examples include:

- secondary data centers;
- cloud object storage;
- offline storage;
- removable media stored securely.

Physical separation reduces the impact of fire, theft, flooding and site-wide disasters.

---

## Encryption

Backup data often contains sensitive information.

Encryption should therefore be considered throughout the backup lifecycle.

Recommended practices include:

- encrypting backup repositories;
- encrypting data during transmission;
- protecting encryption keys;
- restricting administrative access.

Security should extend to backup infrastructure just as it does to production systems.

---

## Automation

Manual backup processes introduce unnecessary operational risk.

Enterprise backup strategies should automate:

- scheduled backups;
- retention enforcement;
- copy jobs;
- verification tasks;
- reporting;
- alerting.

Automation improves consistency while reducing administrative effort.

---

## Documentation

Every backup strategy should be documented.

Documentation should include:

- protected workloads;
- backup schedules;
- retention policies;
- storage locations;
- recovery procedures;
- responsible personnel.

Well-maintained documentation simplifies audits, troubleshooting and disaster recovery.

---

## Common Mistakes

Common weaknesses include:

- relying on a single backup copy;
- storing backups beside production systems;
- never testing restores;
- keeping administrator credentials unsecured;
- using outdated retention policies;
- assuming RAID replaces backup.

Technology alone cannot compensate for poor planning.

---

## Enterprise Recommendation

Design backup strategies around recovery objectives rather than storage capacity.

A backup solution should always answer two questions:

- **Can the data be recovered?**
- **Can it be recovered within the required business timeframe?**

If either answer is uncertain, the backup strategy should be reviewed before deployment.

---

## Enterprise Checklist

- [ ] Recovery objectives documented
- [ ] 3-2-1-1-0 strategy implemented
- [ ] Appropriate backup types selected
- [ ] Backup schedules aligned with RPO
- [ ] Retention policies documented
- [ ] Immutable storage implemented
- [ ] Off-site backup maintained
- [ ] Encryption enabled
- [ ] Backup processes automated
- [ ] Restore procedures documented

---

## Summary

A successful backup strategy is built on business requirements rather than technology alone.

By combining multiple backup copies, immutable storage, appropriate retention policies and automated operations, organizations can significantly improve resilience against hardware failures, cyber threats and human error.

The next chapter examines backup architecture and explains how enterprise backup environments are designed to provide scalability, resilience and efficient disaster recovery.

[Next: Backup Architecture →](04-backup-architecture.md)

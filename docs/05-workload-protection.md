# Workload Protection

Modern organizations operate a diverse range of workloads across physical servers, virtual machines, cloud platforms and Software-as-a-Service (SaaS) environments. Each workload has different recovery requirements, dependencies and protection challenges.

A successful backup strategy recognizes these differences and applies appropriate protection methods rather than treating every workload identically.

The objective is not to back up every system in the same way, but to recover every critical service when required.

---

## Identifying Critical Workloads

Not every workload contributes equally to business operations.

A practical classification includes:

| Priority | Typical Workloads |
|----------|-------------------|
| Critical | Active Directory, Databases, ERP, Firewalls |
| High | Virtualization Hosts, Email, File Servers |
| Medium | Application Servers, Internal Services |
| Low | Development Systems, Test Environments |

Understanding workload priority allows organizations to allocate storage, recovery resources and backup frequency appropriately.

---

## Physical Servers

Although virtualization has become the standard in many environments, physical servers remain common.

Typical examples include:

- database servers;
- backup appliances;
- storage systems;
- industrial control systems;
- legacy applications.

Protection should include:

- image-level backup where possible;
- application-aware backup;
- system state protection;
- configuration backups.

Hardware replacement should never become a prerequisite for successful recovery.

---

## Virtual Machines

Virtualization platforms have transformed enterprise backup.

Instead of protecting individual files, backup software can protect complete virtual machines.

Advantages include:

- rapid recovery;
- image-based backup;
- instant restore capabilities;
- simplified replication;
- sandbox testing.

Virtual machine protection should also include application consistency where required.

---

## Linux Servers

Linux workloads often host critical enterprise services.

Typical examples include:

- web servers;
- databases;
- container hosts;
- monitoring platforms;
- authentication services.

Protection strategies should include:

- operating system configuration;
- application data;
- databases;
- certificates;
- scheduled tasks.

Configuration files are frequently just as important as user data.

---

## Windows Servers

Windows environments often support business-critical infrastructure.

Examples include:

- Active Directory;
- File Services;
- Microsoft SQL Server;
- Remote Desktop Services;
- Microsoft Exchange;
- Print Services.

Application-aware backup is particularly important for Windows workloads to ensure transactional consistency.

---

## Databases

Databases require special consideration.

Simply copying database files may not produce a consistent backup.

Enterprise backup solutions should support:

- transaction consistency;
- log handling;
- point-in-time recovery;
- application awareness.

Examples include:

- Microsoft SQL Server;
- PostgreSQL;
- MySQL;
- MariaDB;
- Oracle Database.

Databases frequently represent the most valuable information within an organization.

---

## Microsoft 365

Many organizations assume that Microsoft automatically protects all Microsoft 365 data indefinitely.

In reality, Microsoft follows a **Shared Responsibility Model**.

Organizations remain responsible for protecting:

- Exchange Online;
- OneDrive;
- SharePoint;
- Microsoft Teams.

Dedicated Microsoft 365 backup should therefore form part of the overall enterprise backup strategy.

---

## NAS Systems

Network Attached Storage frequently contains:

- shared documents;
- engineering data;
- multimedia;
- departmental archives;
- project files.

NAS protection should include:

- snapshot technology;
- scheduled backups;
- off-site replication;
- immutable storage where available.

Snapshots alone should never be considered a complete backup strategy.

---

## Containers

Containerized applications introduce new backup considerations.

Protecting containers involves more than saving container images.

Organizations should also preserve:

- persistent volumes;
- configuration files;
- orchestration settings;
- secrets where appropriate;
- application databases.

Stateless containers are relatively easy to recreate.

Persistent application data remains the primary recovery concern.

---

## Cloud Workloads

Cloud infrastructure does not eliminate backup requirements.

Organizations should protect:

- virtual machines;
- cloud storage;
- managed databases;
- SaaS platforms;
- configuration data.

Cloud providers ensure platform availability, but customers remain responsible for protecting their own business data.

---

## Backup Frequency by Workload

Different workloads require different protection schedules.

| Workload | Typical Backup Frequency |
|----------|--------------------------|
| Domain Controller | Daily |
| SQL Database | Every 15–30 minutes |
| Virtual Machines | Daily or Hourly |
| File Server | Daily |
| Microsoft 365 | Multiple times per day |
| NAS | Daily |
| Archive Storage | Weekly |

Frequency should always align with business-defined Recovery Point Objectives.

---

## Dependency Awareness

Applications rarely operate independently.

For example:

```text
Web Application
      │
      ├── Database
      ├── Authentication
      └── File Storage
```

Protecting only one component does not guarantee successful recovery.

Backup planning should consider the complete service rather than isolated systems.

---

## Common Mistakes

Frequently encountered issues include:

- protecting operating systems but not application data;
- assuming snapshots replace backups;
- ignoring SaaS workloads;
- backing up virtual machines without application consistency;
- forgetting configuration files;
- treating every workload identically.

Effective backup strategies recognize that different systems require different recovery methods.

---

## Enterprise Recommendation

Classify workloads according to business value rather than technical characteristics.

A domain controller, database server and Microsoft 365 tenant may require completely different protection strategies, yet all may be equally critical to business operations.

Recovery planning should therefore focus on business services rather than individual servers.

---

## Enterprise Checklist

- [ ] Critical workloads identified
- [ ] Physical servers protected
- [ ] Virtual machines backed up
- [ ] Linux and Windows systems covered
- [ ] Databases protected with application awareness
- [ ] Microsoft 365 included
- [ ] NAS protection implemented
- [ ] Container workloads evaluated
- [ ] Cloud workloads included
- [ ] Workload dependencies documented

---

## Summary

Every workload presents unique protection requirements.

By selecting backup methods based on business importance, application consistency and recovery objectives, organizations can build a resilient backup environment that protects both traditional infrastructure and modern cloud-native services.

The next chapter explores storage design and explains how repositories, immutable storage, cloud services and long-term retention contribute to a scalable enterprise backup architecture.

[Next: Storage Design →](06-storage-design.md)

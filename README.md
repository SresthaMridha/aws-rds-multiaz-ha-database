# AWS RDS Multi-AZ High Availability Deployment  
### MySQL 8.4 | Encrypted | Automated Backups | Snapshot Strategy

---

## 📌 Architecture Overview

This project demonstrates a production-style **highly available relational database deployment** using **Amazon RDS (MySQL 8.4)**.  
The database is deployed in **Multi-AZ** mode with **synchronous replication**, **automated backups**, **manual snapshot capability**, **encryption at rest**, and **enhanced monitoring** enabled.

---

## 🏗 Architecture Flow

**Application Layer → RDS Primary (AZ-a)**  
**Synchronous Replication → Standby (AZ-b)**  

- **Automatic failover** enabled.

---

## 🔹 Key Features

- **Engine**: MySQL 8.4.7
- **Instance class**: db.m7g.large
- **Multi-AZ**: Enabled (Primary + Standby)
- **Replication**: Synchronous standby replication
- **Failover**: Automatic failover enabled
- **Storage**: 200 GiB gp3
  - **Provisioned IOPS**: 3000 IOPS
  - **Storage Throughput**: 125 MiB/s
  - **Storage Autoscaling**: Enabled
- **Encryption**: Encryption at rest (AWS KMS)
- **Deletion Protection**: Enabled
- **Public Access**: Disabled
- **Monitoring**: Enhanced Monitoring enabled
- **Performance Insights**: Enabled

---

## 🔐 Backup & Recovery Strategy

### Automated Backups
- **Retention period**: 7 days
- **Point-in-Time Recovery (PITR)**: Enabled
- **Backup window**: Configured for minimal downtime

### Manual Snapshot
- **On-demand snapshot**: Created for backup & disaster recovery
- **Snapshot status**: Verified & validated for recovery test

---

## 📊 Monitoring Configuration

- **Enhanced Monitoring**: 60 sec granularity
- **Performance Insights**: Enabled
- **Monitoring Role**: Attached
- **Database Insights**: Standard enabled

---

## 🧠 High Availability Design Principle

- **Primary** instance handles **read/write** traffic
- **Standby** instance is **not directly accessible** by application
- **Synchronous replication** ensures data durability
- **Automatic failover** minimizes downtime
- Designed for **infrastructure-level resilience** in production environments

---

## 📸 Screenshots

Here are the screenshots showing the architecture, configuration, backups, and monitoring setup:

- ![Architecture Diagram](screenshots/01-architecture-diagram.png)
- ![DB Instance Summary](screenshots/02-db-summary.png)
- ![Instance Configuration](screenshots/03-configuration.png)
- ![Multi-AZ Enabled](screenshots/04-multi-az-enabled.png)
- ![Monitoring Performance Insights](screenshots/05-monitoring-performance-insights.png)
- ![Backup Settings](screenshots/06-backup-settings.png)
- ![Manual Snapshot](screenshots/07-manual-snapshot.png)
- ![Automated Snapshot](screenshots/08-automated-snapshot.png)

---

## 🚀 Real-World Relevance

This architecture reflects a **production-ready, high availability database** that can handle large-scale applications, ensuring zero downtime with automatic failover, data durability, and efficient monitoring.

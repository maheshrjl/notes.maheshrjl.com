---
description: Storage options for EC2 instances
---

# 🗳 Storage

## Instance Store

* Instance store are hardware device  (physical connection) connected directly to Ec2 instance
* Better I/O performance compared to EBS Volume
* Instance Store are ephemeral i.e. Loose data if they are stopped
* Use case: Good for buffer/cache/temporary data
* Risk of data loss if hardware (EC2 instance) fails

## EBS Volume

* Elastic Block Store (EBS) is block level storage device attached to EC2 instance
* EBS volume persist data even after instance termination (Unless delete on termination is set)
* EBS can be mounted to 1 instance at a time
* Volumes are bound to specific (Cannot be attached to instance in another AZ)
* It's a network drive (Not a physical drive)
* Capacity & IOPS must be provisioned in advance&#x20;

#### Types of EBS Volume

Amazon EBS volume types are broken into two main categories:&#x20;

* **SSD-backed volumes** are optimized for IOPS, which are best for workloads involving frequent read/write operations with small I/O size.
* **HDD-backed volumes** are optimized for throughput (measured in MiB/s) for large streaming workloads. Cannot include boot volumes.

Within each of those groups are two options. The default type is General Purpose SSD (gp2), and there are 3 others available:

* **General Purpose SSD (gp2) – general purpose, balances price and performance.**
  * **Use cases:** Most workloads such as virtual desktops, dev and test environments, and low-latency interactive apps.
* **Provisioned IOPS SSD (io1)** – highest-performance SSD volume for mission-critical low-latency or high-throughput workloads that require sustained IOPS performance, or more than 16,000 IOPS or 250 MiB/s of throughout per volume.
  * **Use cases:** Mission-critical applications, large database workloads such as MongoDB, Microsoft SQL Server, Cassandra, Oracle, MySQL, and PostgreSQL
* **Throughput Optimized HDD (st1)** – low-cost HDD volume for frequently accessed workloads with high throughput.
  * **Use cases:** Streaming workloads, big data, data warehouses, log processing.
* **Cold HDD (sc1)** – _lowest_ cost HDD volume for less-frequently accessed workloads
  * **Use cases:** Throughput-oriented storage for large volumes of data that is infrequently accessed

{% hint style="info" %}
Only gp2/gp3 & io1/io2 can be used as boot volumes
{% endhint %}

### EBS Snapshot

* Creating a backup (snapshot) of EBS volume
* Not necessary to detach volume but recommended
* Snapshot can by copied across AZ & Region


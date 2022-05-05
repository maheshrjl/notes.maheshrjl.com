---
description: Storage options for EC2 instances
---

# 🗳 Storage

## EBS Volume:

* Elastic Block Store (EBS) is block level storage device attached to EC2 instance
* EBS volume persist data even after instance termination (Unless delete on termination is set)
* EBS can be mounted to 1 instance at a time
* Volumes are bound to specific (Cannot be attached to instance in another AZ)
* It's a network drive (Not a physical drive)
* Capacity & IOPS must be provisioned in advance&#x20;

### EBS Snapshot:

* Creating a backup (snapshot) of EBS volume
* Not necessary to detach volume but recommended
* Snapshot can by copied across AZ & Region


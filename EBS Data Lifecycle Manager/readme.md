# AWS EBS Data Lifecycle Manager (DLM) Lab

## Objective
This lab demonstrates how to automate Amazon EBS snapshot and AMI creation using AWS Data Lifecycle Manager (DLM).

AWS DLM helps automate backup management by creating lifecycle policies that automatically generate, retain, and delete EBS snapshots and AMIs based on schedules.

---

# AWS Services Used
- Amazon EC2
- Amazon EBS
- AWS Data Lifecycle Manager (DLM)
- Amazon Machine Images (AMI)

---

# How This Lab Works

AWS Data Lifecycle Manager (DLM) automates backup operations for EBS volumes and EC2 instances.

In this lab:
1. A Linux EC2 instance is launched.
2. A DLM lifecycle policy is created.
3. The policy targets EBS volumes using tags.
4. Automated snapshots and AMIs are created based on schedules.
5. Retention policies manage backup lifecycle automatically.

This helps organizations:
- Automate backup operations
- Reduce manual administrative tasks
- Improve disaster recovery readiness
- Maintain backup compliance

---

# Lab Architecture

![Architecture Diagram](Architecture%20diagram.png)

---

# Step 1: Launch Linux EC2 Instance

A Linux EC2 instance was launched in AWS with attached EBS storage.

The EC2 instance acts as the source resource for automated snapshot and AMI creation.

## Linux Instance
![Linux Instance](Linux%20instance.png)

---

# Step 2: Configure Policy Creation

The DLM policy configuration includes:
- Target resource selection
- Backup schedule definition
- Snapshot timing
- Retention count

## Step 1 Policy Creation
![Step 1](step-1%20policy%20creation.png)

---

## Step 2 Policy Creation
![Step 2](step-2Policy%20creation.png)

---

## Step 3 Policy Creation
![Step 3](step-3%20policy%20creation.png)

---

# Step 3: Create DLM Lifecycle Policy

AWS Data Lifecycle Manager was configured to automate backup operations.

The lifecycle policy was configured with:
- Policy type
- Target resource tags
- Schedule frequency
- Snapshot retention rules

## Lifecycle Policy
![Lifecycle Policy](Lifecycle%20policy.png)

---


# Step 4: Automated Snapshot Creation

After the lifecycle policy becomes active, AWS automatically creates EBS snapshots according to the configured schedule.

Benefits:
- Automated backups
- Reduced manual effort
- Consistent recovery points
- Improved disaster recovery

## Automated Snapshots
![DLM Snapshots](DLM%20created%20snapshots.png)

---

# Step 5: Automated AMI Creation

AWS DLM can also automate Amazon Machine Image (AMI) creation for EC2 instances.

AMI backups help quickly restore entire servers during failures or migrations.

## Automated AMI
![DLM AMI](DLM%20created%20AMI.png)

---

# Key Learnings
- Launching Linux EC2 instances
- Understanding AWS DLM
- Automating EBS snapshots
- Automating AMI backups
- Using lifecycle policies
- Managing backup retention
- Implementing disaster recovery strategies

---

# Real-World Use Case

Organizations use AWS DLM to:
- Automate daily backups
- Maintain backup compliance
- Protect production workloads
- Reduce operational overhead
- Implement disaster recovery solutions

Example:
If an EC2 instance fails unexpectedly, administrators can restore:
- EBS volumes using snapshots
- Entire servers using automated AMIs

This minimizes downtime and improves business continuity.

---

# Conclusion

This lab successfully demonstrated:
- AWS Data Lifecycle Manager configuration
- Automated EBS snapshot management
- Automated AMI creation
- Lifecycle policy scheduling
- Backup retention automation

AWS DLM provides a scalable and efficient solution for automating backup and recovery operations in cloud environments.

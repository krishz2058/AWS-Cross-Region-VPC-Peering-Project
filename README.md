# AWS Cross-Region VPC Peering Project

## Overview

This project demonstrates secure communication between private EC2 instances deployed in different AWS regions using Cross-Region VPC Peering.

The architecture connects an Amazon VPC in the India Region (ap-south-1) with another Amazon VPC in the US East Region (us-east-1), allowing private communication over the AWS global network without exposing the servers to the public internet.

---

## Architecture

### India Region (ap-south-1)

- VPC: 192.168.0.0/24
- Private Subnet
- EC2 Instance (No Public IP)
- VPC Endpoint for Session Manager Access

### US East Region (us-east-1)

- VPC: 192.168.1.0/24
- Private Subnet
- EC2 Instance (No Public IP)

### Connectivity

- Cross-Region VPC Peering Connection
- Route Tables Configured on Both VPCs
- Secure Private Communication Between Regions

---

## AWS Services Used

- Amazon VPC
- Amazon EC2
- VPC Peering
- Route Tables
- Security Groups
- AWS Systems Manager Session Manager
- VPC Endpoint

---

## Project Implementation

### Step 1: Create India Infrastructure

- Created VPC (192.168.0.0/24)
- Created Private Subnet
- Launched EC2 Instance without Public IP

### Step 2: Create US Infrastructure

- Created VPC (192.168.1.0/24)
- Created Private Subnet
- Launched EC2 Instance without Public IP

### Step 3: Configure Secure Access

- Created VPC Endpoint
- Connected to EC2 using AWS Systems Manager Session Manager

### Step 4: Create Cross-Region VPC Peering

- Sent Peering Request from India VPC
- Accepted Request in US Region

### Step 5: Configure Route Tables

#### India VPC Route

Destination: 192.168.1.0/24

Target: VPC Peering Connection

#### US VPC Route

Destination: 192.168.0.0/24

Target: VPC Peering Connection

### Step 6: Validate Connectivity

- Connected to India EC2 through Session Manager
- Verified communication between India and US EC2 instances

---

## Real-World Banking Use Case

A banking organization hosts its primary application infrastructure in the India Region and maintains a Disaster Recovery (DR) environment in the US Region.

Using Cross-Region VPC Peering:

- Secure private communication between banking servers
- No public internet exposure
- Reliable disaster recovery architecture
- Secure replication of critical business data
- Enhanced security and compliance

---

## Key Learnings

- AWS Networking
- Cross-Region VPC Peering
- Private Cloud Connectivity
- Route Table Management
- AWS Systems Manager
- VPC Endpoints
- Multi-Region Architecture
- Disaster Recovery Design

---

## Benefits

✅ Secure Communication

✅ No Public IP Exposure

✅ Low-Latency AWS Backbone Connectivity

✅ Multi-Region Architecture

✅ Disaster Recovery Readiness

✅ Improved Security Posture

---

## Project Demonstration Video

🎥 LinkedIn Video:

https://www.linkedin.com/posts/krishzalavadiya_aws-cloudcomputing-awscloud-ugcPost-7471460318729338880-qYn3/?utm_source=share&utm_medium=member_desktop&rcm=ACoAAE9h_WkBEi-m86kaAEdyLJq4TMB6q4c4ovY


## Author
KRISH ZALAVADIYA

**Krish Zala**

Aspiring Cloud Engineer | AWS Enthusiast | Hands-On AWS Projects

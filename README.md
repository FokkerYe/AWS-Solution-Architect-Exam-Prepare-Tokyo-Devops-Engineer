# AWS-Solution-Architect-Exam-Prepare-Tokyo-Devops-Engineer


# IAM - Identity and Access Management

## Authentication & Authorization

### Overview

**Principal**  
→ **AWS IAM** (using IAM policies)  
→ **Access**  
→ **AWS Resources**

---

## Authentication Methods

1. **Username & Password**
2. **Access Key & Secret Access Key**

---

## Accessing IAM

You can access IAM through the following methods:

1. **AWS Management Console**  
   - Uses: *AWS username & password*

2. **AWS CLI (Command Line Interface)**  
   - Uses: *Access key & secret access key*

3. **AWS SDKs (Software Development Kits)**  
   - Uses: *Access key & secret access key*

4. **IAM HTTPS API**  
   - Uses: *Access key & secret access key*
     # AWS Supported Policy Types

AWS IAM supports several types of policies to manage access control:

1. **Identity-based Policies**
2. **Resource-based Policies**
3. **Permissions Boundaries**
4. **Service Control Policies (SCPs)** — used with AWS Organizations
5. **Access Control Lists (ACLs)** — primarily for Amazon S3
6. **Session Policies** — advanced use with temporary credentials

---

## 1. Identity-based Policies

Identity-based policies are attached directly to IAM identities (users, groups, roles).

### a. **Managed Policies**

- **AWS Managed Policies**  
  Predefined and maintained by AWS for common use cases.

- **Customer Managed Policies**  
  Created and managed by you to meet specific access requirements.

### b. **Inline Policies**

- One-to-one relationship with a single IAM identity.
- Embedded directly within the user, group, or role.
- Useful for tightly scoped, identity-specific permissions.

---

## 2. Resource-based Policies

- Attached directly to AWS resources (e.g., S3 buckets, SNS topics, SQS queues).
- Define who (which principal) can access the resource and what actions they can perform.
- Supports cross-account access.

---

## 3. Permissions Boundaries

- Advanced feature to set the **maximum permissions** an IAM role or user can have.
- Used to delegate permission management safely.

---

## 4. Service Control Policies (SCPs)

- Used in **AWS Organizations**.
- Control maximum available permissions for accounts in an organizational unit (OU).
- Do **not** grant permissions — only restrict.

---

## 5. Access Control Lists (ACLs)

- Legacy access control mechanism, mainly for **Amazon S3** and **Amazon VPC**.
- Assigns **basic allow/deny permissions** to other AWS accounts or predefined groups.

---

## 6. Session Policies

- Passed when **assuming a role** or requesting **temporary credentials** via STS.
- Only effective for the session duration.
- Further restricts the permissions granted by identity-based policies.


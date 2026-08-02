# Amazon Machine Image (AMI) – Short Notes

## Definition

**Amazon Machine Image (AMI)** is a **pre-configured template** used to launch an **Amazon EC2 instance**. It contains everything required to create a virtual server.

> **AMI = Blueprint**  
> **EC2 Instance = Virtual Machine created from the blueprint**

---

## AMI Contains

- 🖥️ **Operating System**
    
    - Amazon Linux
        
    - Ubuntu
        
    - Windows Server
        
    - Red Hat, etc.
        
- 📦 **Installed Software**
    
    - Apache
        
    - Nginx
        
    - Docker
        
    - Python
        
    - Java, etc.
        
- ⚙️ **Configurations**
    
    - System settings
        
    - Environment variables
        
    - Startup scripts
        
- 💾 **Root Volume Snapshot**
    
    - Storage containing the OS, applications, and data needed to boot the instance.
        

---

## Working of AMI

```text
             AMI (Template)
        -----------------------
        | Ubuntu             |
        | Docker             |
        | Python             |
        | Nginx              |
        -----------------------
                  │
                  ▼
         Launch EC2 Instance
                  │
                  ▼
     Running Virtual Machine
```

---

## Types of AMI

### 1. Public AMI

- Created by AWS or the community.
    
- Available to everyone.
    

**Examples:** Amazon Linux, Ubuntu, Windows Server

---

### 2. Private AMI

- Created by an individual or organization.
    
- Accessible only within the owner's AWS account (unless shared).
    

---

### 3. AWS Marketplace AMI

- Created by third-party vendors.
    
- May include licensed software.
    

**Examples:** Oracle Database, Microsoft SQL Server, WordPress

---

## AMI vs EC2 Instance

|AMI|EC2 Instance|
|---|---|
|Template / Blueprint|Running Virtual Machine|
|Used to create instances|Created from an AMI|
|Read-only image|Read/write machine|
|Cannot execute applications|Runs applications|

---

## Advantages of AMI

- ✅ Quick server deployment
    
- ✅ No need to install software repeatedly
    
- ✅ Ensures identical server configurations
    
- ✅ Easy backup and recovery
    
- ✅ Supports scalability by launching multiple identical instances
    

---

## Real-Life Analogy

```text
House Blueprint  →  House
       │
       ▼
AMI (Template)  →  EC2 Instance
```

A single blueprint can be used to build many identical houses. Similarly, one AMI can be used to launch many identical EC2 instances.

---

# Exam Definition (3–5 Marks)

**Amazon Machine Image (AMI)** is a **pre-configured template** that contains the **operating system, application software, system configurations, and root volume snapshot** required to launch an Amazon EC2 instance. It acts as a blueprint for creating identical virtual servers in AWS.

---

# One-Line Revision

- **AMI = Amazon Machine Image**
    
- **AMI is a template, EC2 is a running virtual machine.**
    
- **Contains OS + Software + Configuration + Root Volume Snapshot.**
    
- **One AMI can launch multiple EC2 instances.**
    
- **Types:** Public, Private, AWS Marketplace.
    
- **Purpose:** Fast deployment, consistency, backup, and scalability.
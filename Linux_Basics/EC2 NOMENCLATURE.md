
---

# AWS EC2 Instance Nomenclature

Every EC2 instance follows this format:

> **Family + Generation + Additional Feature**

**Example:** `t3.micro`

- **t** → Instance Family
    
- **3** → Generation
    
- **micro** → Instance Size
    

---

# 1. General Purpose Instances

## T Series (Burstable Performance)

Examples:

- **T2**
    
- **T3**
    
- **T3a**
    
- **T4g**
    

### Nomenclature

### T2

- **T** = Burstable General Purpose family
    
- **2** = 2nd Generation
    

### T3

- **T** = Burstable General Purpose
    
- **3** = 3rd Generation
    

### T4g

- **T** = Burstable General Purpose
    
- **4** = 4th Generation
    
- **g** = AWS Graviton (ARM-based processor)
    

> **Graviton processors** are AWS-designed ARM CPUs that provide better price-performance and lower power consumption than comparable x86 processors for many workloads.

---

## M Series (Balanced General Purpose)

Examples:

- **M5**
    
- **M6i**
    

### M5

- **M** = Main (General Purpose family)
    
- **5** = 5th Generation
    

### M6i

- **M** = Main General Purpose
    
- **6** = 6th Generation
    
- **i** = Intel Xeon processor
    

---

# 2. Compute Optimized Instances

Examples:

- **C5**
    
- **C6i**
    

### C5

- **C** = Compute Optimized
    
- **5** = 5th Generation
    

### C6i

- **C** = Compute Optimized
    
- **6** = 6th Generation
    
- **i** = Intel processor
    

---

# 3. Memory Optimized Instances

Examples:

- **R5**
    
- **R6i**
    
- **X2**
    

---

### R5

- **R** = RAM (Memory Optimized)
    
- **5** = 5th Generation
    

### R6i

- **R** = Memory Optimized
    
- **6** = 6th Generation
    
- **i** = Intel processor
    

---

### X2

- **X** = Extra Large Memory
    
- **2** = 2nd Generation
    

Used for applications requiring **extremely large amounts of RAM**, such as SAP HANA and very large in-memory databases.

---

# 4. Storage Optimized Instances

Examples:

- **i3**
    
- **i4**
    
- **d2**
    

### i3

- **i** = High IOPS Storage
    
- **3** = 3rd Generation
    

### i4

- **i** = High IOPS Storage
    
- **4** = 4th Generation
    

### d2

- **d** = Dense Storage (high storage capacity)
    
- **2** = 2nd Generation
    

---

# 5. Accelerated Computing Instances

Examples:

- **P4**
    
- **G5**
    
- **Inf1**
    

### P4

- **P** = GPU for Parallel Processing (NVIDIA GPUs)
    
- **4** = 4th Generation
    

### G5

- **G** = Graphics/GPU
    
- **5** = 5th Generation
    

### Inf1

- **Inf** = Inferentia (AWS AI inference chips)
    
- **1** = 1st Generation
    

Used to **run trained AI models efficiently** (AI inference).

---

# Common Suffixes in AWS Instance Names

|Suffix|Meaning|Example|
|---|---|---|
|**i**|Intel processor|M6i, C6i, R6i|
|**a**|AMD processor|T3a, M5a|
|**g**|AWS Graviton (ARM) processor|T4g, M7g|
|**d**|Local NVMe SSD storage|M5d, C5d|
|**n**|Enhanced networking|C5n|
|**e**|Extra memory or storage (family-dependent)|R6e|
|**b**|High EBS bandwidth|M7b|

> **Note:** The meaning of some suffixes (such as **e**) can vary slightly depending on the instance family, but the ones above are the most common and exam-relevant.

---

# Complete Revision Table

|Instance|Meaning|
|---|---|
|**T2**|Burstable General Purpose, 2nd Gen|
|**T3**|Burstable General Purpose, 3rd Gen|
|**T4g**|Burstable General Purpose, 4th Gen, Graviton CPU|
|**M5**|Main General Purpose, 5th Gen|
|**M6i**|Main General Purpose, 6th Gen, Intel CPU|
|**C5**|Compute Optimized, 5th Gen|
|**C6i**|Compute Optimized, 6th Gen, Intel CPU|
|**R5**|Memory Optimized, 5th Gen|
|**R6i**|Memory Optimized, 6th Gen, Intel CPU|
|**X2**|Extra Large Memory, 2nd Gen|
|**i3**|High IOPS Storage, 3rd Gen|
|**i4**|High IOPS Storage, 4th Gen|
|**d2**|Dense Storage, 2nd Gen|
|**P4**|GPU (Parallel Processing), 4th Gen|
|**G5**|Graphics/GPU, 5th Gen|
|**Inf1**|Inferentia AI Inference Chip, 1st Gen|

### Exam Tip

When you see an EC2 instance name:

1. **First letter(s)** → Identify the **instance family** (T, M, C, R, X, I, D, P, G, Inf).
    
2. **Number** → Indicates the **generation** (higher generally means newer hardware).
    
3. **Suffix** (i, a, g, d, etc.) → Indicates the **processor type or special feature**. This naming pattern is frequently tested in AWS certification exams and interviews.
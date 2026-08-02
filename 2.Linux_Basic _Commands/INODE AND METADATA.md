# 📂 Metadata

## Definition

**Metadata** means **"data about data."**

It describes a file but is **not the file's actual content**.

## Real-Life Analogy 🪪

Think of an **Aadhaar Card**.

The Aadhaar card contains:

- Name
    
- Date of Birth
    
- Address
    
- Gender
    

But **it is not the person**.

Similarly, metadata describes a file but **is not the file itself**.

## Examples of Metadata

- File size
    
- Owner
    
- Permissions (`rwx`)
    
- Creation date
    
- Modification date
    
- File type
    

> **Memory Trick:**  
> **Metadata = Information about a file, not the file's content.**

---

# 📦 Inode (Index Node)

## Definition

An **inode** is a data structure that stores a file's **metadata** and tells Linux where the file's data is stored on the disk.

It **does not** store:

- ❌ Filename
    
- ❌ File content
    

## Real-Life Analogy 🆔

Think of a **Student ID Card**.

```text
Student Name
      │
      ▼
Student ID (101)
      │
      ▼
Student Details
```

- Student Name = **Filename**
    
- Student ID = **Inode**
    
- Student Details = **Metadata**
    

Even if the student's **name changes**, the **Student ID remains the same**.

Similarly, changing a filename does **not** change the inode.

---

## Linux Flow

```text
Filename
    │
    ▼
Inode
    │
    ▼
Metadata + Location of Data
    │
    ▼
Actual File Content
```

---

# 📝 Exam One-Liners

### Metadata

> **Metadata is information that describes a file, such as its size, permissions, owner, and timestamps.**

### Inode

> **An inode is a data structure that stores a file's metadata and pointers to its data blocks, but not the filename or the file content.**

---

# ⭐ Quick Revision

|Term|Easy Meaning|Real-Life Analogy|
|---|---|---|
|**Metadata**|Information about a file|🪪 Aadhaar Card details|
|**Inode**|File's identity that stores metadata and points to data|🆔 Student ID|
|**Filename**|Human-readable name|👤 Student's Name|
|**File Content**|Actual data inside the file|📖 Student's Knowledge|

## 💡 Memory Trick

- **Metadata = Details about the file.**
    
- **Inode = The file's identity card (stores metadata + location of data).**
    
- **Filename = Just the label humans use to identify the file.**
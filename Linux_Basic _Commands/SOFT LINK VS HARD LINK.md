


# 🔗 What is a Link?

A **link** is another way to access a file.

There are two types:

1. **Hard Link**
    
2. **Soft Link (Symbolic Link / Symlink)**
    

---

# 🟢 Soft Link (Symbolic Link)

## Definition

A **soft link** is a special file that stores the **path (address)** of another file.

It is similar to a **shortcut** in Windows.

## Real-Life Analogy 🏠

Imagine your friend gives you his home address on a sticky note.

```text
Sticky Note
     |
     | "House No. 25"
     |
     ▼
Actual House
```

- The sticky note **isn't the house**.
    
- It only tells you **where the house is**.
    
- If the house is demolished or moved, the address becomes useless.
    

Exactly the same happens with a soft link.

## Characteristics

- Stores the **path** of the original file.
    
- Has its **own inode**.
    
- Breaks if the original file is deleted or moved.
    
- Can link directories.
    
- Can span different file systems.
    

## Command

```bash
ln -s original_file softlink_name
```

Example:

```bash
ln -s notes.txt shortcut.txt
```

---

# 🔵 Hard Link

## Definition

A **hard link** is another **name** for the same file.

Both filenames point to the **same inode** and the **same data**.

## Real-Life Analogy 👤

Imagine a person has two legal names.

```text
Akash  ───┐
          │
          ▼
     Same Person
          ▲
          │
Sky    ───┘
```

- Both names refer to the **same person**.
    
- Removing one name doesn't remove the person.
    
- The person disappears only when **all names are removed**.
    

This is exactly how hard links work.

## Characteristics

- Shares the **same inode** as the original file.
    
- Acts as another name for the same file.
    
- Editing one reflects in the other.
    
- Deleting one filename does **not** delete the file.
    
- File is deleted only when **all hard links are removed**.
    
- Cannot normally link directories.
    
- Cannot span different file systems.
    

## Command

```bash
ln original_file hardlink_name
```

Example:

```bash
ln notes.txt backup.txt
```

---

# 🆚 Hard Link vs Soft Link

|Feature|Hard Link|Soft Link|
|---|---|---|
|Meaning|Another name for the same file|Shortcut to a file|
|Stores|Same inode|File path|
|Inode|Same|Different|
|If original file is deleted|✅ Still works|❌ Breaks|
|Can link directories|❌ No (normally)|✅ Yes|
|Cross file systems|❌ No|✅ Yes|

---

# 💡 Memory Trick

### 🟢 Soft Link

> **"I know where the file lives."**

(Like a sticky note with someone's address.)

### 🔵 Hard Link

> **"I am another name for the same file."**

(Like one person having two legal names.)

---

# 📝 Exam One-Liners

- **Soft Link:** A shortcut that stores the **path** of another file.
    
- **Hard Link:** Another filename that points to the **same inode** as the original file.
    

---

# ⭐ Quick Revision

```text
Soft Link
Shortcut ➜ Original File

Hard Link
Name 1 ──┐
          ├── Same File
Name 2 ──┘
```

> **Golden Rule:**  
> **Soft Link = Shortcut (stores address).**  
> **Hard Link = Another name for the same file (shares identity/inode).**
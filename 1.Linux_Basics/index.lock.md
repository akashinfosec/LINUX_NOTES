# 🔒 Git `index.lock`

`index.lock` is a **temporary lock file** created by Git while it updates the **staging area (index)**.

It prevents **multiple Git processes** from modifying the repository at the same time.

---

## Normal Workflow

```text
git add .
      │
      ▼
Creates index.lock
      │
      ▼
Updates the index (staging area)
      │
      ▼
Deletes index.lock
```

---

## Why the Error Occurs

If Git is interrupted (e.g., terminal closed, VS Code crashed, `Ctrl + C`, power failure), the lock file may remain.

Error:

```text
fatal: Unable to create '.git/index.lock': File exists.
Another git process seems to be running in this repository.
```

Git refuses to continue because it assumes another Git process is still using the repository.

---

## Solution

1. Ensure **no Git process is running**.
2. Delete the stale lock file:

```bash
rm -f .git/index.lock
```

or (Windows CMD)

```cmd
del .git\index.lock
```

3. Retry the Git command:

```bash
git add .
git commit -m "Update notes"
git push
```

---

## Summary

| File | Purpose |
|------|---------|
| `.git/index` | Stores the staging area (files added using `git add`). |
| `.git/index.lock` | Temporary lock file created while Git updates the index. |

---

## Quick Revision

- `index` → Git's **staging area**.
- `index.lock` → Temporary lock file.
- Prevents multiple Git processes from modifying the repository simultaneously.
- Normally created **automatically** and deleted after the operation completes.
- If Git is interrupted, delete the stale `index.lock` only after confirming no Git process is running.
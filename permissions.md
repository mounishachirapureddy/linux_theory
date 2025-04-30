# 📚 Linux File Permissions and Ownership - Easy and Technical Guide

---

# 🔥 What are File Permissions?

In Linux, **every file and folder** has **permissions** that control **who** can:

- **Read** it (r) — 📖 Like reading a book
- **Write** it (w) — ✍️ Like writing in a notebook
- **Execute** it (x) — 🎮 Like running a game

---

# 👥 Who Can Access a File?

Each file belongs to:

| Who       | Who are they?            | Easy Example |
|-----------|---------------------------|--------------|
| **User**  | File's creator/owner       | You (the student) |
| **Group** | A group of users           | Your classmates |
| **Others**| Everyone else (public)     | Strangers visiting your school |

---

# 🔐 Permission Layout Explained

Example of file permission:

```
-rwxr-xr--
```

| Part           | Meaning |
|----------------|---------|
| `-`            | It's a file (`d` means directory) |
| `rwx`          | User: Read, Write, Execute |
| `r-x`          | Group: Read, Execute (no Write) |
| `r--`          | Others: Read only |

---

# 🛠️ Important Commands

---

## 1. `chmod` — Change Permissions

**chmod** is used to change what **User**, **Group**, and **Others** can do with a file.

### Syntax:
```bash
chmod [permissions] [file_name]
```

---

### 📗 Examples:

✅ Give only **read and write** permissions to the owner:
```bash
chmod 600 homework.txt
```
- User: read and write
- Group: no access
- Others: no access

✅ Make a script **executable**:
```bash
chmod +x game.sh
```
- Now you can **run** it like a game!

✅ Remove **write** permission from a file:
```bash
chmod -w story.txt
```
- Now you can **read** but **not change** the story.

---

## 2. `chown` — Change Ownership (User)

**chown** is used to give the file to a new owner.

### Syntax:
```bash
chown [new_owner] [file_name]
```

---

### 📗 Example:

✅ Give your homework to your friend **Mary**:
```bash
chown mary homework.txt
```
- Now **Mary** owns the file!

---

## 3. `chgrp` — Change Group Ownership

**chgrp** is used to change which group owns the file.

### Syntax:
```bash
chgrp [new_group] [file_name]
```

---

### 📗 Example:

✅ Move your project to the **science_club** group:
```bash
chgrp science_club project.doc
```
- Now all science club members can access it!

---

# 📋 Summary Table

| Command | What it Does | Simple Meaning |
|---------|--------------|----------------|
| `chmod` | Change file permissions | Give/remove keys to a file |
| `chown` | Change file owner | Hand over your file to someone else |
| `chgrp` | Change file's group | Move file to a new group |

---

# 🎯 Real-Life Analogy

Imagine your **school locker**:

- You (User) have **full keys** (read/write/execute)
- Your friends (Group) may **open and look** but **can't change** anything
- Strangers (Others) may **only see outside** but **can't touch** anything

🔐 **chmod** = Deciding who has keys 🔑  
🏷 **chown** = Giving locker to another person  
👥 **chgrp** = Moving locker under another club's control  

---

# 🚀 Important Tips

- Always give the **minimum necessary permissions** (for security).
- **Don't** give **write** permission to **Others** unless needed!
- Always **test** permissions with:
```bash
ls -l
```
It shows current permissions and ownership of files.

---

# ✨ Example Screenshot (Optional)

```bash
$ ls -l homework.txt
-rw-r--r-- 1 john students 200 Apr 30 10:00 homework.txt
```

Here:
- `rw-` for User (read, write)
- `r--` for Group (read only)
- `r--` for Others (read only)
- Owned by **john** in group **students**


# 📚 Daily Linux Commands 

---

## 📂 1. `ls` - List Files and Folders
- **Show files/folders in the current place.**

- **Options:**
  - `ls -l` → Show details (permissions, size, date).
  - `ls -a` → Show hidden files.
  - `ls -t` → Sort by last modified time.
  - Combine like: `ls -alt`

- **Examples:**
  ```bash
  ls
  ls -l
  ls -a
  ls -al
  ls -t
  ls -alt
  ```

---

## 📂 2. `cd` - Change Directory
- **Go into a folder.**

- **Types:**
  - `cd foldername` → Enter a folder.
  - `cd ..` → Go back one folder.
  - `cd /` → Go to root.
  - `cd ~` → Go to home folder.

- **Examples:**
  ```bash
  cd myfolder
  cd ..
  cd /
  cd ~
  ```

---

## 📂 3. `pwd` - Print Working Directory
- **Where you are right now (full path).**

- **Example:**
  ```bash
  pwd
  ```

---

## 📂 4. `touch` - Create a File
- **Make a new file.**

- **Example:**
  ```bash
  touch file.txt
  ```

---

## 📂 5. `mkdir` - Make a Directory
- **Make a new folder.**

- **Example:**
  ```bash
  mkdir myfolder
  ```

---

## 📂 6. `rm` - Remove Files or Folders
- **Delete stuff!**

- **Options:**
  - `rm filename` → Remove file.
  - `rm -r folder` → Remove folder and inside files.
  - `rm -f filename` → Force remove file without asking.
  - `rm -rf folder` → Force remove folder and everything.

- **Examples:**
  ```bash
  rm file.txt
  rm -r foldername
  rm -f file.txt
  rm -rf foldername
  ```

---

## 📂 7. `cp` - Copy Files or Folders
- **Duplicate files/folders.**

- **Examples:**
  ```bash
  cp file1.txt file2.txt
  cp -r folder1 folder2
  ```

---

## 📂 8. `mv` - Move or Rename
- **Move or rename files/folders.**

- **Examples:**
  ```bash
  mv oldname.txt newname.txt
  mv file.txt /home/user/Documents/
  ```

---

## 📂 9. `cat` - View File Contents
- **See what's inside a file.**

- **Options:**
  - `cat filename` → See contents.
  - `cat -b filename` → See with line numbers.

- **Examples:**
  ```bash
  cat file.txt
  cat -b file.txt
  ```

---

## 📂 10. `head` - Top Lines of a File
- **See first few lines.**

- **Examples:**
  ```bash
  head file.txt
  head -n 5 file.txt
  ```

---

## 📂 11. `tail` - Bottom Lines of a File
- **See last few lines.**

- **Examples:**
  ```bash
  tail file.txt
  tail -n 5 file.txt
  ```

---

## 📂 12. `echo` - Print Text
- **Print words on screen.**

- **Examples:**
  ```bash
  echo Hello World
  echo $USER
  ```

---

## 📂 13. `|` (Pipe) - Connect Commands
- **Send output of one command to another.**

- **Example:**
  ```bash
  ls -l | grep file
  ```

---

## 📂 14. `grep` - Search Text
- **Find words in files.**

- **Example:**
  ```bash
  grep "word" file.txt
  ```

---

## 📂 15. `find` - Find Files or Folders
- **Search by name/location.**

- **Example:**
  ```bash
  find /home/user -name file.txt
  ```

---

## 📂 16. `tar` - Pack/Unpack Files
- **Create or extract `.tar` archive files.**

- **Examples:**
  ```bash
  tar -cvf archive.tar folder/
  tar -xvf archive.tar
  ```

---

## 📂 17. `df` - Disk Space
- **Check how much space is left.**

- **Example:**
  ```bash
  df -h
  ```

---

## 📂 18. `ps` - Show Running Programs
- **See which apps are running.**

- **Example:**
  ```bash
  ps
  ```

---

## 📂 19. `top` - Live System Info
- **See CPU, memory, processes live.**

- **Example:**
  ```bash
  top
  ```

---

# 🔐 File Permissions and Ownership (Easy)

---

## 📘 What are Permissions?
- Linux controls **who can do what** with a file/folder.

| Symbol | Meaning  |
|:------|:---------|
| r | read (can view) |
| w | write (can edit) |
| x | execute (can run/enter) |

---

## 📘 Who are the Users?

| User Type | Meaning |
|:----------|:--------|
| User (u) | Owner of the file |
| Group (g) | A team/group of users |
| Others (o) | Everyone else |

---

## 📘 Commands to Manage Permissions

| Command | Purpose |
|:--------|:--------|
| `chmod` | Change permissions |
| `chown` | Change owner |
| `chgrp` | Change group |

---

### 📂 `chmod` Examples:
```bash
chmod 755 file.txt
chmod u+x script.sh
```

**Numbers meaning:**
- `7` → read + write + execute
- `6` → read + write
- `5` → read + execute
- `4` → read

---

### 📂 `chown` Examples:
```bash
chown user1 file.txt
```

Change owner of file.

---

### 📂 `chgrp` Examples:
```bash
chgrp group1 file.txt
```

Change group of file.

---

# ✍️ VIM Editor (Basics)

---

## 📘 What is VIM?
- **VIM** is a **text editor** used to create, edit, and save files inside terminal.

---

## 📘 How to Open VIM
- **Create or Edit a file:**
  ```bash
  vim filename.txt
  ```

---

## 📘 Modes in VIM

| Mode | What You Do |
|:-----|:------------|
| Normal Mode | Move around, delete, copy |
| Insert Mode | Type normally |
| Command Mode | Save, quit, etc |

---

## 📘 How to Switch Modes

| Key | Action |
|:----|:-------|
| `i` | Insert mode |
| `Esc` | Back to Normal mode |
| `:` | Command mode |

---

## 📘 Important Commands Inside VIM

| Command | Meaning |
|:--------|:--------|
| `:w` | Save file |
| `:q` | Quit |
| `:wq` | Save and Quit |
| `:q!` | Quit without saving |
| `:set number` | Show line numbers |
| `:set nonumber` | Hide line numbers |
| `dd` | Delete line |
| `yy` | Copy (yank) line |
| `p` | Paste line |
| `/word` | Search for word |
| `:help` | Get help |

---

## 📘 Example - Create and Save a File in VIM

1. Open VIM:
   ```bash
   vim myfile.txt
   ```
2. Press `i` → Start typing
3. Write something
4. Press `Esc`
5. Type `:wq` → Save and exit

🎉 Done!

---

# 🧠 Linux Quick CheatSheet Table

| Command | Purpose |
|:--------|:--------|
| `ls` | List files |
| `cd` | Change directory |
| `pwd` | Show current path |
| `touch` | Create file |
| `mkdir` | Create folder |
| `rm` | Remove file/folder |
| `cp` | Copy |
| `mv` | Move/Rename |
| `cat` | View file |
| `head` | First lines |
| `tail` | Last lines |
| `echo` | Print text |
| `|` | Pipe |
| `grep` | Search text |
| `find` | Find files |
| `tar` | Pack/Unpack |
| `df` | Disk usage |
| `ps` | Running processes |
| `top` | Live system usage |
| `vim` | Edit files |

---

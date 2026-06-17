# Linux Permissions

## Introduction

Linux permissions control who can read, write, and execute files and directories. They are an essential part of Linux security and system administration.

---

# Permission Types

There are three basic permissions:

| Permission | Symbol | Meaning                 |
| ---------- | ------ | ----------------------- |
| Read       | r      | View file contents      |
| Write      | w      | Modify file contents    |
| Execute    | x      | Run a file as a program |

---

# Permission Groups

Permissions are assigned to three categories:

| Group      | Meaning                     |
| ---------- | --------------------------- |
| User (u)   | Owner of the file           |
| Group (g)  | Members of the file's group |
| Others (o) | Everyone else               |

---

# Viewing Permissions

Use the following command:

```bash
ls -l
```

Example:

```bash
-rwxr-xr-- 1 user user 1024 Jun 16 script.sh
```

Breakdown:

```text
-rwxr-xr--
│ │  │  │
│ │  │  └── Others
│ │  └───── Group
│ └──────── User
└────────── File Type
```

---

# File Types

| Symbol | Type          |
| ------ | ------------- |
| -      | Regular File  |
| d      | Directory     |
| l      | Symbolic Link |

Example:

```bash
drwxr-xr-x Documents
```

The "d" indicates a directory.

---

# Changing Permissions

## chmod

Used to change file permissions.

Syntax:

```bash
chmod permissions filename
```

Example:

```bash
chmod 755 script.sh
```

---

# Numeric Permissions

| Number | Permission |
| ------ | ---------- |
| 7      | rwx        |
| 6      | rw-        |
| 5      | r-x        |
| 4      | r--        |
| 3      | -wx        |
| 2      | -w-        |
| 1      | --x        |
| 0      | ---        |

Common examples:

```bash
chmod 755 script.sh
chmod 644 file.txt
chmod 700 secret.txt
```

---

## Meaning of Common Values

### 755

```text
rwxr-xr-x
```

Owner:

* Read
* Write
* Execute

Others:

* Read
* Execute

Common for scripts and directories.

---

### 644

```text
rw-r--r--
```

Owner:

* Read
* Write

Others:

* Read only

Common for text files.

---

### 700

```text
rwx------
```

Only owner has access.

Useful for private files.

---

# Symbolic Mode

Instead of numbers:

```bash
chmod u+x script.sh
```

Adds execute permission for owner.

Examples:

```bash
chmod g+w file.txt
chmod o-r file.txt
chmod u+x script.sh
```

---

# Changing Ownership

## chown

Change file owner.

Syntax:

```bash
chown username filename
```

Example:

```bash
sudo chown abhinav notes.txt
```

---

# Changing Group Ownership

## chgrp

Change group ownership.

Syntax:

```bash
chgrp groupname filename
```

Example:

```bash
chgrp developers app.py
```

---

# Useful Commands

View permissions:

```bash
ls -l
```

Add execute permission:

```bash
chmod +x script.sh
```

Remove write permission:

```bash
chmod -w file.txt
```

Change owner:

```bash
sudo chown user file.txt
```

Change group:

```bash
chgrp developers file.txt
```

---

# Key Takeaways

* Linux permissions follow the rwx model.
* Permissions are assigned to User, Group, and Others.
* chmod changes permissions.
* chown changes ownership.
* chgrp changes group ownership.
* 755 and 644 are the most commonly used permission sets.
* Proper permissions improve system security and reduce unauthorized access.


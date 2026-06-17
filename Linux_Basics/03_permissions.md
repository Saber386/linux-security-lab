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

```text
[Owner][Group][Others]

755
│ │ │
│ │ └─ Others
│ └─── Group
└───── Owner
```

---

Common examples:

```bash
chmod 755 script.sh
chmod 644 file.txt
chmod 700 secret.txt
```

Each digit is made up of:

Read (r)    = 4
Write (w)   = 2
Execute (x) = 1

---

## Meaning of Common Values

### 755
So if the digit is 755 then 
Owner = (4+3) .i.e r+w (Owner can read and write in this Document) 

Group = (3+2) .i.e r+x (Group members can read and execute in this document) 

Others = (3+2) .i.e r+x (Others can also read and execute in this document) 

```text
rwxr-xr-x
```
Almost never used

---

### 644

So if the digit is 644 then
Owner = (4+2) .i.e r+w (Owner can read and write in this document)

Group = (4) .i.e r (Group members can only read this document)

Others = (4) .i.e r (Others can only read this document)

```text
rw-r--r--
```
Common for text files.

---

### 700

So if the digit is 700 then
Owner = (4+2+1) .i.e r+w+x (Owner can read, write and execute this document)

Group = (0) .i.e --- (Group members have no permissions)

Others = (0) .i.e --- (Others have no permissions)

```text
rwx------
```
Personal folders
Security-related directories
Hidden config directories

---

### 666

So if the digit is 666 then

Owner = (4+2) .i.e r+w (Owner can read and write in this document)

Group = (4+2) .i.e r+w (Group members can read and write in this document)

Others = (4+2) .i.e r+w (Others can read and write in this document)

```text
rw-rw-rw-
```
Used occasionally for:
Shared temporary files
Testing

---

# Symbolic Mode in Linux

Symbolic mode allows permissions to be modified using letters instead of numeric values.

Syntax:

```bash
chmod [who][operator][permission] filename
```

## Symbols

### Who

| Symbol | Meaning |
|---------|---------|
| u | User (Owner) |
| g | Group |
| o | Others |
| a | All |

### Operators

| Symbol | Meaning |
|---------|---------|
| + | Add Permission |
| - | Remove Permission |
| = | Set Exact Permission |

### Permissions

| Symbol | Meaning |
|---------|---------|
| r | Read |
| w | Write |
| x | Execute |

---

## Example

Command:

```bash
chmod u+x script.sh
```

Breakdown:

```text
u = User (Owner)
+ = Add
x = Execute
```

Meaning:

> Add execute permission to the owner of the file.

Before:

```text
-rw-r--r--
```

After:

```text
-rwxr--r--
```

The owner can now execute the file while all other permissions remain unchanged.

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


# Linux File Operations

## Overview

File operation commands allow users to create, copy, move, delete, and inspect files and directories. These commands are heavily used in system administration, log analysis, incident response, and digital forensics.

---

## touch

### Purpose

Creates a new empty file.

### Syntax

```bash
touch filename.txt
```

### Example

```bash
touch notes.txt
```

### Cybersecurity Use Case

Used to create investigation notes, test files, and scripts during security analysis.

---

## mkdir

### Purpose

Creates a new directory.

### Syntax

```bash
mkdir directory_name
```

### Example

```bash
mkdir logs
```

### Cybersecurity Use Case

Analysts often organize evidence, logs, and reports into dedicated directories.

---

## cp

### Purpose

Copies files or directories.

### Syntax

```bash
cp source destination
```

### Example

```bash
cp auth.log backup_auth.log
```

### Cybersecurity Use Case

Before analyzing a log file or suspicious file, analysts often create a copy to preserve the original.

---

## cp -r

### Purpose

Copies directories recursively.

### Syntax

```bash
cp -r source_directory destination
```

### Example

```bash
cp -r logs logs_backup
```

### Cybersecurity Use Case

Useful when preserving entire directories during investigations.

---

## mv

### Purpose

Moves or renames files and directories.

### Syntax

```bash
mv old_name new_name
```

### Example

```bash
mv report.txt incident_report.txt
```

### Cybersecurity Use Case

Used to organize investigation artifacts and rename files for clarity.

---

## rm

### Purpose

Deletes files.

### Syntax

```bash
rm filename
```

### Example

```bash
rm temp.txt
```

### Cybersecurity Use Case

Used carefully when removing temporary files or malicious artifacts.

⚠️ Deleted files generally cannot be recovered easily.

---

## rm -r

### Purpose

Deletes directories and their contents.

### Syntax

```bash
rm -r directory_name
```

### Example

```bash
rm -r old_logs
```

### Cybersecurity Use Case

Used during cleanup of test environments and labs.

---

## cat

### Purpose

Displays file contents.

### Syntax

```bash
cat filename
```

### Example

```bash
cat auth.log
```

### Cybersecurity Use Case

Quickly view logs, configuration files, and scripts.

---

## less

### Purpose

Views large files page by page.

### Syntax

```bash
less filename
```

### Example

```bash
less auth.log
```

### Cybersecurity Use Case

Extremely useful when reviewing large log files during investigations.

---

## head

### Purpose

Displays the first lines of a file.

### Syntax

```bash
head filename
```

### Example

```bash
head auth.log
```

### Cybersecurity Use Case

Allows analysts to quickly inspect the beginning of logs.

---

## tail

### Purpose

Displays the last lines of a file.

### Syntax

```bash
tail filename
```

### Example

```bash
tail auth.log
```

### Cybersecurity Use Case

Used to view the most recent events in logs.

---

## tail -f

### Purpose

Monitors files in real time.

### Syntax

```bash
tail -f filename
```

### Example

```bash
tail -f /var/log/auth.log
```

### Cybersecurity Use Case

SOC analysts use this to watch authentication logs and monitor ongoing activity.

---

## Key Takeaways

* touch creates files.
* mkdir creates directories.
* cp copies files.
* mv moves or renames files.
* rm deletes files.
* cat displays file contents.
* less helps inspect large files.
* tail -f enables real-time monitoring.

These commands are foundational for Linux administration, SOC operations, incident response, and forensic investigations.

# Process Management in Linux

## Introduction

A process is a running instance of a program.

Whenever an application is started, Linux creates a process for it.

Examples:

- Firefox
- Terminal
- VS Code
- SSH Service

All of these run as processes.

---

# Viewing Running Processes

## ps

Displays currently running processes.

Command:

```bash
ps
```

Example Output:

```text
PID TTY          TIME CMD
1234 pts/0    00:00:00 bash
5678 pts/0    00:00:00 ps
```

---

# Viewing Detailed Processes

## ps aux

Displays all running processes with detailed information.

Command:

```bash
ps aux
```

Information displayed:

- User
- Process ID (PID)
- CPU Usage
- Memory Usage
- Command

---

# Real-Time Process Monitoring

## top

Displays processes in real time.

Command:

```bash
top
```

Shows:

- CPU Usage
- Memory Usage
- Running Processes
- System Load

Press:

```text
q
```

to exit.

---

# Finding a Process

## pidof

Displays the PID of a process.

Command:

```bash
pidof firefox
```

Example Output:

```text
2456
```

---

# Terminating a Process

## kill

Stops a running process using its PID.

Command:

```bash
kill PID
```

Example:

```bash
kill 2456
```

---

# Force Terminating a Process

## kill -9

Forces a process to stop immediately.

Command:

```bash
kill -9 PID
```

Example:

```bash
kill -9 2456
```

---

# Viewing Process Hierarchy

## pstree

Displays processes in a tree structure.

Command:

```bash
pstree
```

Example Output:

```text
systemd
├── NetworkManager
├── firefox
├── bash
└── sshd
```

---

# Example

Create a process:

```bash
sleep 1000
```

Open another terminal and find the process:

```bash
ps aux | grep sleep
```

Output:

```text
abhinav  4521  sleep 1000
```

Terminate the process:

```bash
kill 4521
```

Verify:

```bash
ps aux | grep sleep
```

The process will no longer appear.

---

# Cybersecurity Relevance

Process management is important in cybersecurity because:

- Malware runs as processes.
- Attackers often create hidden processes.
- Security analysts monitor suspicious processes.
- Incident responders investigate running processes during security incidents.
- High CPU or memory usage may indicate malicious activity.

---

# Summary

- A process is a running program.
- `ps` displays running processes.
- `ps aux` displays detailed process information.
- `top` provides real-time monitoring.
- `pidof` finds process IDs.
- `kill` terminates a process.
- `kill -9` forcefully terminates a process.
- `pstree` displays process hierarchy.
- Process monitoring is an important cybersecurity skill.

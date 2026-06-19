# Networking Basics in Linux

## Introduction

Networking allows devices to communicate and exchange data over a network. In Linux, networking commands are used to view IP addresses, test connectivity, troubleshoot issues, and inspect network services.

Networking knowledge is essential for system administration, cybersecurity, and troubleshooting.

---

## IP Address

An IP address is a unique identifier assigned to a device on a network.

Example:

```text
192.168.1.10
```

To view IP addresses assigned to your system:

```bash
ip a
```

This command displays:

- IP Address
- Network Interface
- MAC Address
- Interface Status

---

## Network Interfaces

A network interface is a connection point between a device and a network.

Common interfaces:

```text
eth0   -> Ethernet
wlan0  -> Wireless Network
lo     -> Loopback Interface
```

View available interfaces:

```bash
ip link
```

---

## Loopback Interface

The loopback interface allows a device to communicate with itself.

Loopback Address:

```text
127.0.0.1
```

Also known as:

```text
localhost
```

Test it using:

```bash
ping 127.0.0.1
```

---

## Testing Connectivity

The `ping` command is used to check whether another device or website is reachable.

Example:

```bash
ping google.com
```

Example Output:

```text
64 bytes from google.com: icmp_seq=1 ttl=117 time=25 ms
```

Useful for:

- Checking internet access
- Troubleshooting network issues
- Verifying host availability

---

## Routing

A routing table determines where network traffic is sent.

View routing information:

```bash
ip route
```

Example Output:

```text
default via 192.168.1.1 dev wlan0
```

This shows the default gateway used to access external networks.

---

## DNS (Domain Name System)

DNS converts domain names into IP addresses. Its like the internets phonebook, It translates Human readable domain name into machine-readable numeric IP addresses (like 192.0.2.1)

Example:

```text
google.com
      ↓
142.250.183.206
```

Check DNS resolution:

```bash
nslookup google.com
```

or

```bash
dig google.com
```

---

## Open Ports

An open port is a virtual communication endpoint on a device that actively accepts incoming TCP(Transmission Control Protocol) or UDP (User Datagram Protocol)  network traffic. Ports allow applications and services to communicate over a network.

Common Ports:

| Port | Service |
|--------|----------|
| 22 | SSH |
| 53 | DNS |
| 80 | HTTP |
| 443 | HTTPS |

View listening ports:

```bash
ss -tuln
```

This command displays active services waiting for connections.

---

## Active Network Connections

To view active network connections:

```bash
netstat -an
```

This displays:

- Active Connections
- Listening Ports
- Protocol Information

---

## Hostname

A hostname is the name assigned to a device on a network.

View hostname:

```bash
hostname
```

Example Output:

```text
linuxmint
```

---

## Cybersecurity Relevance

Networking is one of the most important areas in cybersecurity.

Security professionals use networking knowledge for:

- Network Reconnaissance
- Port Scanning
- Service Enumeration
- Traffic Analysis
- Incident Response
- Threat Hunting

Understanding networking fundamentals helps identify suspicious connections, exposed services, and potential security risks.

---

## Commands Summary

```bash
ip a
ip link
ping google.com
ip route
nslookup google.com
dig google.com
ss -tuln
netstat -an
hostname
```

---

## Summary

- Every device on a network has an IP address.
- Network interfaces connect devices to networks.
- The loopback address is 127.0.0.1.
- Ping is used to test connectivity.
- Routing determines where traffic is sent.
- DNS converts domain names into IP addresses.
- Ports enable network communication.
- Networking knowledge is essential for Linux administration and cybersecurity.

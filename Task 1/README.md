# Task 1: Basic Network Scanning with Nmap

## Objective:
The objective of this task is to perform a basic network scan using **Nmap** (Network Mapper) on a local machine or virtual machine (VM). The goal is to identify open ports, services running on those ports, and any potential security weaknesses related to those services. This task helps to understand how network scanning works and its importance in identifying vulnerabilities within a network environment.

## Tools Used:
- **Nmap**: A powerful open-source network scanning tool used to discover hosts and services on a computer network. It is widely used for network inventory, managing service upgrade schedules, and monitoring host or service uptime.

## Prerequisites:
- **Kali Linux** or any other Linux distribution should be installed.
- **Nmap** must be installed.

To install **Nmap** on Kali Linux, use the following command:
```bash
sudo apt update
sudo apt install nmap
````

## Steps:

### 1. Install Nmap:

First, we need to install **Nmap**. On Kali Linux, this can be done via the package manager:

```bash
sudo apt update
sudo apt install nmap
```

### 2. Perform a Basic Network Scan:

Once **Nmap** is installed, we can perform a basic scan. Open a terminal and run the following command to scan a target machine:

```bash
nmap <target_ip_address>
```

For example, if you want to scan your own machine (localhost), run:

```bash
nmap 127.0.0.1
```

### 3. Analyze Nmap Output:

The output will display the open ports and services associated with them. A sample output might look like this:

```bash
Starting Nmap 7.80 ( https://nmap.org ) at 2023-10-25 19:00 UTC
Nmap scan report for 127.0.0.1
Host is up (0.00013s latency).
Not shown: 998 closed ports
PORT   STATE SERVICE
22/tcp open  ssh
80/tcp open  http
443/tcp open https
```

This indicates that the target machine has:

* **SSH** running on port 22
* **HTTP** running on port 80
* **HTTPS** running on port 443

### 4. Save the Scan Results:

To save the Nmap output for later reference, use the `-oN` flag:

```bash
nmap -oN nmap_scan_results.txt <target_ip_address>
```

This command saves the scan results to a file named `nmap_scan_results.txt`.

### 5. Interpret the Findings:

The scan results show open ports and services:

* **Port 22 (SSH)**: Secure Shell, typically used for secure remote login.
* **Port 80 (HTTP)**: HyperText Transfer Protocol, commonly used for web servers.
* **Port 443 (HTTPS)**: Secure version of HTTP, used for encrypted communication.

These services are standard for most systems, but they could also represent potential attack points if not properly secured. Regular network scanning is essential to detect unauthorized services or open ports that may have been overlooked.
## Conclusion:

By performing this basic network scan using **Nmap**, we were able to identify the open ports and services running on a target machine. The results highlight the need to secure these services to avoid potential security risks. Regular network scanning is an important part of network maintenance and security practices to ensure systems are not vulnerable to unauthorized access.

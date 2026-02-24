# Task 8: Capture Network Traffic with Wireshark

## Objective:
The objective of this task is to capture and analyze network traffic using **Wireshark**, a powerful network protocol analyzer. This will help you understand how data is transmitted across networks and enable you to identify potential network issues or security vulnerabilities. 

## Tools Used:
- **Wireshark**: A network protocol analyzer that allows you to capture and inspect network traffic in real time.
- **Kali Linux**: A Debian-based Linux distribution for penetration testing, where Wireshark is already available.

## Prerequisites:
- A system running **Wireshark**. In **Kali Linux**, Wireshark is pre-installed, but if needed, it can be installed using:
  ```bash
  sudo apt install wireshark
````

* Root or superuser permissions to capture packets. You can use `sudo` to run Wireshark with necessary privileges:

  ```bash
  sudo wireshark
  ```

## Steps:

### 1. Install Wireshark (if not already installed):

Wireshark is usually pre-installed in Kali Linux. If not, use the following command to install it:

```bash
sudo apt update
sudo apt install wireshark
```

### 2. Start Wireshark:

To start Wireshark with root privileges, run the following command:

```bash
sudo wireshark
```

Alternatively, if you're using a graphical interface, you can find Wireshark in your application menu.

### 3. Select Network Interface:

Upon opening Wireshark, you'll see a list of available network interfaces (Ethernet, Wi-Fi, etc.). Select the network interface that corresponds to your active network connection. Common interface names are:

* **eth0** for Ethernet
* **wlan0** for Wi-Fi

Click on the interface to start capturing packets.

### 4. Start Packet Capture:

Click the **Start** button (green shark fin) to begin capturing packets from the selected network interface.

### 5. Apply Filters:

Wireshark captures all network traffic, which can be overwhelming. To focus on specific types of traffic, you can apply filters. Some common filters include:

* **HTTP traffic**: `http`
* **TCP traffic**: `tcp`
* **DNS queries**: `dns`
* **Traffic from a specific IP**: `ip.addr == 192.168.1.1`

Apply the filters by typing them in the display filter box at the top.

### 6. Analyze Captured Packets:

Click on any packet in the capture list to view detailed information about it. Each packet is broken down into multiple layers:

* **Frame**: The Ethernet layer, including source and destination MAC addresses.
* **IP**: The network layer, which contains source and destination IP addresses.
* **TCP/UDP**: The transport layer, where source and destination port numbers are found.
* **Payload**: The application layer, where the data being transmitted (e.g., HTTP request/response) is displayed.

### 7. Stop the Capture:

Once enough data is captured, click the **Stop** button (red square) to halt the capture.

### 8. Save Your Capture:

To save your packet capture for later analysis, click **File** -> **Save As** and choose a file name and format. Wireshark saves the capture in **PCAP** format, which is commonly used for packet captures.

## Conclusion:

In this task, you learned how to use **Wireshark** to capture and analyze network traffic. By filtering traffic and inspecting specific packets, you can troubleshoot network issues and identify potential security risks such as unencrypted data transmission or unauthorized network access. Regular use of network traffic analysis tools like Wireshark is essential for maintaining secure and optimized network environments.

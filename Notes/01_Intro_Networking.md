# 01 - Introduction to Networking

## 🌐 Why Networking Is Important
- Enables communication between computers and devices.
- Powers the internet, cloud computing, email, file sharing, streaming, etc.
- Core to business operations: data access, remote work, collaboration.
- Efficient resource sharing (e.g., printers, storage).

---

## 🏠 LAN vs. WAN

| Term | Full Form        | Description |
|------|------------------|-------------|
| LAN  | Local Area Network | Covers a small geographic area (e.g., home, office). High speed, low latency. |
| WAN  | Wide Area Network  | Covers a large area (e.g., the internet). Lower speed, higher latency. |

---

## 🔌 Networking Devices

### Switch
- Connects devices within a LAN.
- Operates at Layer 2 (Data Link Layer).
- Uses MAC addresses to forward data to the correct device.

### Router
- Connects multiple networks (e.g., LAN to the internet).
- Operates at Layer 3 (Network Layer).
- Assigns IP addresses and performs routing.

### Firewall
- Controls incoming/outgoing traffic based on security rules.
- Can be hardware or software.
- Protects the network from unauthorized access.

---

## 🧠 IP Address vs MAC Address

| Aspect      | IP Address                        | MAC Address                      |
|-------------|------------------------------------|----------------------------------|
| Purpose     | Logical address for routing       | Physical address for identification |
| Format      | IPv4: `192.168.1.1`<br>IPv6: `2001:db8::1` | `00:1A:2B:3C:4D:5E` (hexadecimal) |
| Changeable  | Yes (dynamic or static)           | No (burned into NIC)             |
| Used By     | Routers (Layer 3)                 | Switches (Layer 2)               |

---

## 🔌 Ports and Protocols

### What Are Ports?
- Logical endpoints for communication.
- Allow multiple services to run on a single IP.
- Example:  
  - HTTP: port 80  
  - HTTPS: port 443  
  - SSH: port 22

---

## 🛰️ Protocols: TCP vs. UDP

| Feature        | TCP                            | UDP                         |
|----------------|----------------------------------|-----------------------------|
| Connection     | Connection-oriented             | Connectionless              |
| Reliability    | Guarantees delivery, order      | No delivery guarantee       |
| Speed          | Slower (more overhead)          | Faster (less overhead)      |
| Use Cases      | Web, Email, File transfer       | Video streaming, Gaming     |
| Example Ports  | HTTP (80), HTTPS (443), FTP (21) | DNS (53), VoIP (5060)       |

---

✅ **Tip:** Use `ipconfig`/`ifconfig`, `ping`, and `traceroute` to explore network interfaces and paths.

### 🧠 05 – Subnetting & NAT

---

#### 📌 What is Subnetting?

Subnetting is the process of dividing a large network into smaller subnetworks. This helps:
- Improve routing efficiency
- Enhance security
- Minimize broadcast traffic

Each subnet has:
- **Network Address**: Identifies the subnet
- **First Usable IP**: First IP available for a device
- **Last Usable IP**: Last IP available for a device
- **Broadcast Address**: Used to send data to all hosts in the subnet
- **Total IPs**: All IPs in the subnet (usable + reserved)
- **Usable IPs**: Total IPs minus 2 (network + broadcast)

---

#### 🔢 IP Address and Binary Conversion

Every IPv4 address is 32 bits long, split into four 8-bit segments called **octets**.

To convert any octet into binary, use the following place values:
128  64  32  16  8  4  2  1
Example: Convert `192` to binary  
192 = 128 + 64 → so mark 1 under 128 and 64
192 → 11000000
So, IP `192.168.1.0` in binary = `11000000.10101000.00000001.00000000`

---

#### 🧮 CIDR Notation (Classless Inter-Domain Routing)

CIDR defines how many bits are used for the **network** portion of an address.

Example:  
`192.168.1.0/26` means:
- First 26 bits = network
- Remaining 6 bits = hosts
2^6 = 64 total IPs
64 - 2 = 62 usable IPs

---

#### 🧾 Subnet Details Calculation

For any subnet like `192.168.1.0/26`, here’s how to break it down:

| Item              | Calculation                   | Result               |
|------------------|-------------------------------|----------------------|
| **Total IPs**     | 2^(32 - subnet bits)          | 2^(32-26) = 64       |
| **Usable IPs**    | Total IPs - 2 (net & broadcast)| 64 - 2 = 62          |
| **Network Address**| First IP in subnet            | 192.168.1.0          |
| **First Usable IP**| Network + 1                   | 192.168.1.1          |
| **Last Usable IP**| Broadcast - 1                 | 192.168.1.62         |
| **Broadcast IP**  | Last IP in subnet             | 192.168.1.63         |

---

#### 🔁 NAT (Network Address Translation)

NAT translates private IPs (like `192.168.x.x`) to public IPs so devices can communicate with the internet.

Types of NAT:
- **Static NAT**: One private IP maps to one public IP
- **Dynamic NAT**: Maps private IPs to a pool of public IPs
- **PAT (Port Address Translation)**: Many private IPs share one public IP, differentiated by port numbers (used in home routers)

**Why NAT is important:**
- Conserves public IPs
- Adds a layer of security
- Allows internal devices to access external networks

---

#### 🧪 Subnetting Example: 192.168.10.0/28

Let’s break it down:
- Subnet mask: `255.255.255.240`
- Bits for hosts: 32 - 28 = 4 bits
- Total IPs = 2^4 = 16
- Usable IPs = 16 - 2 = 14

| Address Type       | IP Address         |
|--------------------|--------------------|
| Network Address     | 192.168.10.0       |
| First Usable IP     | 192.168.10.1       |
| Last Usable IP      | 192.168.10.14      |
| Broadcast Address   | 192.168.10.15      |
| Total IPs           | 16                 |
| Usable IPs          | 14                 |

---

✅ Subnetting helps in designing efficient and secure networks. Mastering subnet math, binary, and CIDR will make you confident in configuring and troubleshooting networks.

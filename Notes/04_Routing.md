# 04 - Routing

## 🚦 What is Routing?

- **Routing** is the process of selecting a path for traffic to travel from a source to a destination across networks.
- Routers use **routing tables** to determine the next hop for a packet.
- Essential for communication between **different subnets or networks**.

---

## 🔧 Static vs. Dynamic Routing

| Type             | Description |
|------------------|-------------|
| Static Routing   | Routes are manually configured by an admin. Best for small, predictable networks. |
| Dynamic Routing  | Routers exchange route info automatically using routing protocols. Adapts to changes. |

---

## 🧠 Common Routing Protocols

| Protocol | Type     | Use Case |
|----------|----------|----------|
| OSPF     | Link-state      | Internal networks (enterprise), fast convergence |
| BGP      | Path-vector     | Internet routing between ISPs, scalable, policy-based |

### ✅ OSPF (Open Shortest Path First)
- Internal Gateway Protocol (IGP)
- Uses cost as a metric
- Fast, loop-free, uses Dijkstra’s algorithm

### 🌐 BGP (Border Gateway Protocol)
- External Gateway Protocol (EGP)
- Used for routing between organizations (ISPs)
- Policy and path-based decisions

---

## 🗺️ Routing Decision Factors
- Destination IP
- Subnet mask
- Route metrics (cost, hop count)
- Static/manual overrides

📘 Lab 01: Basic Network Setup

🎯 Objective

To configure a basic network using a router, switch, and PCs, and verify connectivity.

---

🧱 Topology

* 1 Router (R1)
* 1 Switch
* 2 PCs

---

🌐 IP Addressing

| Device | Interface | IP Address   |
| ------ | --------- | ------------ |
| R1     | G0/0      | 192.168.1.1  |
| PC1    | NIC       | 192.168.1.10 |
| PC2    | NIC       | 192.168.1.20 |

---

⚙️ Configuration

 Router R1

```bash
enable
configure terminal
hostname R1

interface g0/0
ip address 192.168.1.1 255.255.255.0
no shutdown
```

---

🖥 PC Configuration

* Default Gateway: 192.168.1.1

---

✅ Verification

Ping from PC1 to PC2:

```bash
ping 192.168.1.20
```

---

📸 Screenshots

* Topology diagram
* Ping result

---

🧠 Key Concepts

* Basic Networking
* IP Addressing
* Default Gateway
* Connectivity Testing



🎯 Result

All devices successfully communicate within the network.

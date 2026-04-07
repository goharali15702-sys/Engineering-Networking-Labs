 📘 Lab 02: Router-on-a-Stick (Inter-VLAN Routing)

🎯 Objective

To configure inter-VLAN routing using a single router interface with subinterfaces.

---
 🧱 Topology

* 1 Router
* 1 Switch
* 4 PCs
* VLAN 10 and VLAN 20

---

🌐 VLAN Design

| VLAN    | Network        |
| ------- | -------------- |
| VLAN 10 | 192.168.1.0/24 |
| VLAN 20 | 192.168.2.0/24 |

---

 ⚙️ Configuration

 Router

```bash id="h4n1k3"
interface g0/0
no shutdown

interface g0/0.10
encapsulation dot1Q 10
ip address 192.168.1.1 255.255.255.0

interface g0/0.20
encapsulation dot1Q 20
ip address 192.168.2.1 255.255.255.0
```

---

 Switch

* VLAN 10 and VLAN 20 created
* Ports assigned to VLANs
* Fa0/5 configured as trunk

---

🖥 Verification

```bash id="t5p8w1"
ping 192.168.2.10
```

---

🧠 Key Concepts

* VLAN
* Trunking
* Subinterfaces
* Inter-VLAN Routing

---
 🎯 Result

Devices in different VLANs successfully communicate through the router.

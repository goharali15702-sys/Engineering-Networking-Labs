📘 Lab 03: Device Configuration & Security

 🎯 OBJECTIVE
Configure basic security on router & switch
Set hostname
Configure passwords
Enable secure remote access (console + vty(Telnet))
Add banner message


---

 🧱 Topology

* Router and Switch
* Reused from previous lab 02 toplogy to done this too

---

⚙️ Configuration

 Router

```bash
enable
configure terminal
hostname R1

enable secret cisco123

Remember : this configuration apply the entire router to not access unauthorized (who does't has password).
line console 0
password admin123
login

Remember : this configuration apply the entire router not on router's interfaces.And this for who access router's CLI remotely.
line vty 0 1
password admin123
login


service password-encryption

banner motd # Unauthorized access is prohibited #
```

---

Switch

```bash
enable
configure terminal
hostname S1

enable secret cisco123

line console 0
password admin123
login

service password-encryption

banner motd # Authorized users only #
```

---

✅ Verification

* Password required on login
* Banner message displayed
* Config verified using:

```bash
show running-config
```

---

 🧠 Key Concepts

* Device Security
* Console Access
* VTY Access
* Password Encryption
* Banner Message

---

🎯 Result

Devices are secured with passwords and unauthorized access is restricted.

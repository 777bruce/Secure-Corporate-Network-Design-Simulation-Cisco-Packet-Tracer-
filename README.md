# 🔐 Secure Corporate Network Simulation (Cisco Packet Tracer)

A fully configured enterprise-style network designed using **Cisco Packet Tracer**, showcasing VLANs, Inter-VLAN routing, DHCP, ACLs, Port Security, and network troubleshooting skills.  
This project demonstrates practical, job-ready networking skills suitable for **Network Engineer Intern** roles.

---

## 🚀 Features Implemented

### 🔸 1. VLAN Segmentation
- VLAN 10 – Admin Dept  
- VLAN 20 – HR Dept  
- VLAN 30 – IT Dept  
- VLAN 40 – Guest Network (Optional)

### 🔸 2. Inter-VLAN Routing (Router-on-a-Stick)
- Sub-interfaces for each VLAN  
- Dot1Q encapsulation  
- Gateway assignment  

### 🔸 3. DHCP Server
Automatically assigns IPs to all VLAN clients.

### 🔸 4. Access Control List (ACL)
- HR Department **blocked** from accessing Admin Department  
- Company-wide internet access enabled  

### 🔸 5. Port Security
- Sticky MAC  
- Max 2 MAC per port  
- Restrict mode  

### 🔸 6. Packet Tracer Network Topology
(Add your topology screenshot here)

---

## 🧱 Network Topology (Diagram)

```
                    ┌────────────────────┐
                    │     Internet       │
                    └─────────┬──────────┘
                              │
                        [ ISP Router ]
                              │
                        [ Core Router ]
                              │
                      ┌───────┴────────┐
                      │                │
                [Switch-1]        [Switch-2]
```

Departments:
- Admin – VLAN 10 – 192.168.10.0/24  
- HR – VLAN 20 – 192.168.20.0/24  
- IT – VLAN 30 – 192.168.30.0/24  

---

## 🛠️ Configuration Files

All detailed CLI configs are stored in the **/configs** folder.

Example (router-config.txt):

```bash
interface g0/0.10
 encapsulation dot1Q 10
 ip address 192.168.10.1 255.255.255.0
```

---

## 🖼️ Screenshots

Screenshots included in `/screenshots`:
- Topology  
- VLAN config  
- Router sub-interfaces  
- Ping test  
- ACL verification  
- Port security  

---

## 🧪 Testing & Verification

### ✔️ DHCP Test
All PCs receive automatic IP addressing.

### ✔️ ACL Test
HR → Admin = ❌ Blocked  
IT → Admin = ✔️ Allowed

### ✔️ Connectivity Test
```bash
ping 192.168.20.1
ping 192.168.10.1
ping 8.8.8.8
```

---

## 📂 Files in This Project

```
README.md  
configs/ (All router & switch configs)  
packet-tracer/secure-network.pkt  
screenshots/ (All images)  
notes/troubleshooting-notes.md  
```

---

## 🧑‍💻 Author

**Chinmay P Gowda**  
Network Engineer | CSE Student  
GitHub: https://github.com/777bruce
LinkedIn:www.linkedin.com/in/chinmayygowda

---

<img width="800" src="https://github.com/abdullaah019/Ethernet-LAN-Switching-Lab-Cisco-Packet-Tracer-/blob/main/Scenario%202_%20PowerShell%20Suspicious%20Web%20Request.png" alt="Ethernet-LAN-Switching-Lab-Cisco-Packet-Tracer-"/>
# 🔄 Ethernet LAN Switching Lab (Cisco Packet Tracer)

## 🎯 Objective
Build a basic Ethernet LAN topology using switches and PCs to understand MAC address learning, VLAN segmentation, and basic frame forwarding behavior in a switched environment.

---

## 🛠 Requirements
- Cisco Packet Tracer
- Lab File: `Ethernet LAN Switching.pkt`

---

## 🧪 Lab Tasks & Commands

### 1. Build the Topology
- Connect PC0, PC1, and PC2 to separate switches (SW1, SW2, SW3)
- Interconnect switches in a triangle to observe MAC address learning across links

---

### 2. Configure Hostnames
```bash
Switch> enable
Switch# configure terminal
Switch(config)# hostname SW1
# Repeat on other switches: SW2, SW3
```

---

### 3. Assign Access Ports to VLANs
```bash
SW1(config)# interface fastEthernet 0/1
SW1(config-if)# switchport mode access
SW1(config-if)# switchport access vlan 10
```
- Use VLAN 10 for PC0, VLAN 20 for PC1, VLAN 30 for PC2

---

### 4. Verify MAC Address Table
```bash
SW1# show mac address-table
```
- Use this to confirm MAC address learning on each switch

---

### 5. Test Connectivity
- Ping from PC0 to PC1 and PC2
- Document which hosts can communicate (same VLAN = success)

---

## 🔍 Observation Points
- Switches learn MAC addresses dynamically
- Hosts in different VLANs cannot communicate without a Layer 3 device
- Frame forwarding is based on MAC address tables

---

## 📁 Files
- `Ethernet LAN Switching.pkt`

---

## 🧠 Key Concepts
- VLANs segment traffic on a switch
- Access ports assign hosts to VLANs
- MAC tables are critical to switch forwarding behavior

---

## ✅ Bonus Challenge
Try adding a Layer 3 switch or router-on-a-stick setup to enable inter-VLAN routing.

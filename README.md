# 🛡️🏫 Secure Campus Network Design (CIS 192 Project)

A practical implementation of a secure, scalable, and efficient campus network. Designed with a layered architecture, VLAN segmentation, and security-first principles using industry-standard devices.

---

## 📚 Project Overview

This project focuses on the **design and implementation of a secure network infrastructure** for a fictional campus setup with four core departments, using hierarchical design principles and robust security configurations.

✅ Includes Cisco Packet Tracer file: `Assignment2.pkt`  
✅ Includes full CLI configuration: [`COMMANDS.docx`](./COMMANDS.docx)

---

## 🏢 Network Design & Devices

### 🧱 Layered Architecture

- **Core Layer**: Router, Firewall, Multilayer Switch  
- **Distribution Layer**: Switches for each department  
- **Access Layer**: PCs, Laptops, Printers  

### 🧰 Devices Used

- 🔌 **4 departmental switches** (Cisco 2960)
- 🌐 **2 multilayer switches** (Cisco 3560)
- 🔥 **1 Firewall**
- 📡 **1 Router**
- 🖥️ **Computers & Laptops** per department
- 🖨️ **Printers**
- 🗃️ **DMZ** with:
  - 1 Switch
  - 2 Servers (DHCP & DNS)

---

## 🧩 Departments & VLAN Configuration

Each department is logically segmented using **VLANs** to enhance performance and security.

| Department     | VLAN ID | IP Range            |
|----------------|---------|---------------------|
| Administration | VLAN 10 | 192.168.10.0/24     |
| Classroom      | VLAN 20 | 192.168.20.0/24     |
| Library        | VLAN 30 | 192.168.30.0/24     |
| IT             | VLAN 40 | 192.168.40.0/24     |

### 🔐 Special Subnets

- **DMZ Subnet**: `10.20.20.0/27`  
- **Firewall-DMZ**: `10.20.20.32/30`  
- **Firewall-Multilayer**: `10.20.20.36/30`  
- **Firewall-Router**: `105.100.50.0/30`  

---

## 🛠️ Network Features

### ⚙️ Routing & Switching

- 🧭 **Multilayer Switches** handle Inter-VLAN routing  
- 🔁 Supports static or dynamic routing protocols (e.g., OSPF)  
- 🔌 Access switches manage end-user devices  

### 🔒 Network Security

- 📋 **Access Control Lists (ACLs)** filter and control inter-VLAN traffic  
- 🔐 **Port Security**: restricts unauthorized access  
- 🔥 **Firewall** defends against external threats  
- 📡 **SSH** enabled on all network devices for secure remote access  
- ⚠️ Unused ports/protocols are disabled  

---

## 📊 Performance Testing (Latency)

Latency between various departments was tested and results showed minimal delay:

| Source          | Destination       | Avg Latency (ms) | Observation        |
|------------------|------------------|------------------|--------------------|
| IT-PC1           | Admin-PC1        | 1                | No significant delay |
| Admin-PC1        | Classroom-PC1    | 4                | No significant delay |
| Library-PC1      | IT-PC1           | 0                | No significant delay |
| (others...)      | ...              | ...              | No significant delay |

> The network is optimized for performance due to its size and efficient routing paths.

---

## ✅ Conclusion

- ✅ **Hierarchical Design** supports scalability and reliability  
- ✅ **VLANs** improve performance and enforce logical segmentation  
- ✅ **Security features** ensure robust protection from external and internal threats  
- ✅ **Minimal Latency** indicates proper routing and switching setup  
- ✅ **Scalable Infrastructure** allows for easy expansion in future  

---

## 👨‍💻 Author

**Tejas Pathange**  
🛠️ [GitHub Profile](https://github.com/Code-Tejas-P)

---

Let me know if you'd like to add:
- Diagrams (topology image, VLAN map)  
- Packet Tracer or Cisco config files  
- Presentation-ready visuals or PDF summary  

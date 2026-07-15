# Home Lab Setup - Cybersecurity & Networking Project

## 📋 Project Overview

This project documents the complete setup of a home lab environment for learning cybersecurity and networking. The lab includes virtual machines running different operating systems, firewall configurations, network simulations using Cisco Packet Tracer, and practical hands-on experience with enterprise networking tools.

**Purpose:** Build hands-on skills in network administration, firewall configuration, network design, and Linux/Windows server management.

---

## 🎯 Project Goals

- ✅ Set up virtualization environment (VirtualBox)
- ✅ Install and configure multiple virtual machines (Windows Server, Linux, pfSense)
- ✅ Design and simulate enterprise networks using Cisco Packet Tracer
- ✅ Create functional network topologies
- ✅ Document firewall rules and network configurations
- ✅ Practice network security fundamentals

---

## 🛠️ Technologies & Tools Used

| Tool/OS | Purpose | Version |
|---------|---------|---------|
| **VirtualBox** | Virtualization platform | TBD |
| **Windows Server** | Active Directory & testing | TBD |
| **Ubuntu/Linux** | Server OS & security tools | TBD |
| **pfSense** | Firewall & network management | TBD |
| **Wireshark** | Network traffic analysis | TBD |
| **Cisco Packet Tracer** | Network simulation & design | TBD |
| **Cisco Cybersecurity LabVM** | Security lab environment | Workstation |

---

## 📐 Network Topology - VirtualBox Environment

```
┌─────────────────────────────────────────┐
│         Host Computer (Your PC)         │
├─────────────────────────────────────────┤
│                VirtualBox               │
│  ┌──────────────────────────────────┐  │
│  │      pfSense Firewall (Router)   │  │
│  │    192.168.1.1 / 10.0.0.1        │  │
│  └──────────────────────────────────┘  │
│            │        │         │         │
│    ┌───────┴───┐    │    ┌────┴──────┐ │
│    │           │    │    │           │ │
│  ┌─┴──┐    ┌──┴─┐  │  ┌─┴──┐    ┌──┴─┐│
│  │ Win│    │Ubu │  │  │Kali│    │DNS ││
│  │Srv │    │ntu │  │  │Lnx │    │Srv ││
│  └────┘    └────┘  │  └────┘    └────┘│
│                    │                   │
└─────────────────────────────────────────┘
```

*(Update this diagram as you build your lab)*

---

## 📝 Setup Instructions

### Prerequisites
- [ ] Host computer with at least 8GB RAM (16GB recommended)
- [ ] VirtualBox installed
- [ ] ISO files downloaded:
  - Windows Server
  - Ubuntu Linux
  - pfSense
- [ ] Cisco Packet Tracer installed
- [ ] Cisco Cybersecurity LabVM Workstation downloaded

### Phase 1: Firewall Setup (VirtualBox)

1. **Create pfSense VM**
   - Allocate: 2 cores, 2GB RAM
   - Network: 2 adapters (WAN & LAN)
   - [Detailed steps coming]

2. **Configure pfSense**
   - Set WAN interface to NAT
   - Set LAN interface to 10.0.0.0/24
   - [Configuration details coming]

### Phase 2: Server Setup (VirtualBox)

1. **Windows Server VM**
   - Allocate: 2-4 cores, 4GB RAM
   - [Details coming]

2. **Ubuntu Linux VM**
   - Allocate: 2 cores, 3GB RAM
   - [Details coming]

### Phase 3: Security Tools (VirtualBox)

1. **Kali Linux VM** (for testing)
   - Allocate: 2 cores, 3GB RAM
   - [Details coming]

### Phase 4: Cisco Packet Tracer - Small Office Network

#### 4.1 Installation & Setup
- [x] Installed Cisco Packet Tracer
- [x] Launched simulator environment
- [x] Created small office network simulation

#### 4.2 Network Devices Configured
| Device Type | Quantity | Model | Purpose |
|-------------|----------|-------|---------|
| **PCs** | 2-3 | Generic | Workstations |
| **Laptops** | 1-2 | Generic | Mobile workstations |
| **Switches** | 1-2 | Cisco 2960 | LAN connectivity |
| **Routers** | 1 | Cisco 1841/2911 | Internet gateway |
| **Access Points** | 1 | Cisco WAP | WiFi connectivity |
| **Servers** | 1 | Generic | File/DHCP server |

#### 4.3 Network Design

```
┌─────────────────────────────────────────────────────┐
│          SMALL OFFICE NETWORK (Packet Tracer)       │
├─────────────────────────────────────────────────────┤
│                                                     │
│  ┌──────────────────────────────────────────────┐  │
│  │         Cisco Router (Internet Gateway)      │  │
│  │              192.168.1.1                     │  │
│  └──────────────────────────────────────────────┘  │
│         │ (WAN)              │ (LAN)               │
│         │                    └─────────────────┐   │
│         │                                      │   │
│  ┌──────┴──────────────────────────────────────┴──┐│
│  │     Cisco Switch                               ││
│  │     (VLAN 10 - Management)                     ││
│  └──────┬──────┬──────┬──────┬──────┬──────────────┘
│         │      │      │      │      │              │
│    ┌────┴──┐ ┌─┴─────┐ │  ┌──┴──┐  │         ┌────┴──┐
│    │  PC1  │ │  PC2  │ │  │ Lap │  │         │WAP    │
│    │       │ │       │ │  │ top │  │         │(WiFi) │
│    └───────┘ └───────┘ │  └─────┘  │         └───────┘
│                         │           │           (WiFi)
│                    ┌────┴──┐   ┌────┴──┐      Clients
│                    │Server │   │Laptop2│
│                    │ DHCP  │   │ WiFi  │
│                    └───────┘   └───────┘
│                                                     │
└─────────────────────────────────────────────────────┘
```

#### 4.4 Logical Mode (Network Topology)
- [ ] Viewed logical network topology
- [ ] Identified device connections and relationships
- [ ] Documented IP addressing scheme:
  - Router: 192.168.1.1/24
  - Servers: 192.168.1.10-20
  - Workstations: 192.168.1.30-100 (DHCP)
- [ ] Noted routing protocols
- [ ] Documented VLAN assignments (if applicable)

#### 4.5 Physical Mode (Device Layout)
- [ ] Switched to physical network view
- [ ] Observed actual device placement and connections
- [ ] Documented cable connections:
  - Switch to Router (Uplink)
  - PCs to Switch (Access)
  - Laptops to Access Point
- [ ] Identified physical locations in office
- [ ] Noted power connections and cable management

#### 4.6 Key Differences Learned

| Aspect | Logical Mode | Physical Mode |
|--------|--------------|---------------|
| **Focus** | Network topology & connections | Physical layout & locations |
| **View** | Devices & logical relationships | Cable runs & device placement |
| **Use Case** | Planning & troubleshooting | Installation & documentation |
| **Shows** | IP addresses, protocols, services | Devices, cables, locations |
| **Helps With** | Network design, connectivity | Physical deployment, setup |

### Phase 5: Cisco Cybersecurity LabVM Workstation Integration

#### 5.1 Installation & Setup
- [x] Downloaded Cisco Cybersecurity LabVM Workstation
- [x] Installed in VirtualBox environment
- [x] Configured network access to lab environment
- [ ] Started security lab exercises

#### 5.2 Lab VM Features
- Integrated security tools and utilities
- Pre-configured vulnerable applications for practice
- Access to Cisco security training materials
- Integration with main home lab network

---

## 🔒 Security Configurations

### Firewall Rules (pfSense)
| Source | Destination | Port | Action | Purpose |
|--------|------------|------|--------|---------|
| LAN | WAN | Any | Allow | Internet access |
| WAN | LAN | Any | Block | Inbound protection |
| [Add more] | | | | |

### Network Policies
- [ ] DHCP configured on pfSense
- [ ] DNS configured
- [ ] Inter-VM communication tested
- [ ] Internet access verified from VMs
- [ ] Packet Tracer network functioning properly

---

## 📊 Current Progress

### VirtualBox Environment
- [ ] VirtualBox installed
- [ ] pfSense VM created & configured
- [ ] Windows Server VM created & configured
- [ ] Ubuntu VM created & configured
- [ ] Kali Linux VM created & configured
- [ ] Network connectivity verified
- [ ] Firewall rules documented

### Cisco Packet Tracer
- [x] Cisco Packet Tracer installed
- [x] Small office network created
- [x] Devices connected (PCs, Switches, Routers, APs)
- [x] Logical mode topology documented
- [x] Physical mode layout documented
- [ ] Network testing completed
- [ ] Screenshots & documentation complete

### Cisco Cybersecurity LabVM
- [x] Cybersecurity LabVM downloaded
- [x] Installed in VirtualBox
- [x] Integrated with home lab network
- [ ] Security labs started
- [ ] Exercises completed

---

## 📚 Resources & Documentation

### Setup Guides
- [VirtualBox Installation Guide](https://www.virtualbox.org/manual/ch01.html)
- [pfSense Getting Started](https://docs.netgate.com/)
- [Ubuntu Server Installation](https://ubuntu.com/server/docs)
- [Cisco Packet Tracer Official](https://www.netacad.com/portal/resources/packet-tracer)
- [Cisco Cybersecurity Academy](https://www.cisco.com/c/en/us/training-events/training-certifications/certifications/entry-level.html)

### Tools & Commands Used

#### Network Commands
```bash
# Linux network info
ip addr show
ip route show
netstat -an

# Network testing
ping 8.8.8.8
traceroute google.com
nslookup example.com
```

#### Packet Tracer Operations
```
- Logical Topology View: Click "Logical" tab
- Physical Topology View: Click "Physical" tab
- Device Configuration: Double-click device
- Network Testing: Simulation mode > PDU creation
- Cable management: Add/modify connections in workspace
```

---

## 📸 Screenshots & Diagrams

*Screenshots of your setup will go here:*

### VirtualBox
- [ ] VirtualBox VM list
- [ ] Network topology diagram
- [ ] pfSense dashboard
- [ ] Network configuration screenshots

### Cisco Packet Tracer
- [ ] Small office network - Logical view
- [ ] Small office network - Physical view
- [ ] Device configuration screens
- [ ] Network testing results

### Cisco LabVM
- [ ] VM running in VirtualBox
- [ ] Lab interface screenshot
- [ ] Security tools overview

---

## 🔍 Testing & Validation

### Cisco Packet Tracer Testing
- [ ] Ping test between all devices
- [ ] PC-to-Server connectivity
- [ ] WiFi client connectivity
- [ ] DHCP assignment verification
- [ ] Router internet gateway test
- [ ] Network traffic simulation

### VirtualBox Testing
- [ ] Ping test between VMs
- [ ] Internet connectivity test
- [ ] DNS resolution test
- [ ] Firewall rule validation
- [ ] Performance baseline

### Test Results
```
Date: [When you run tests]
Environment: Packet Tracer v[X.X] & VirtualBox v[X.X]

Packet Tracer Tests:
- PC1 to PC2 connectivity: ✓
- Laptop WiFi connection: ✓
- Server DHCP assignment: ✓

[Add more results...]
```

---

## 🚀 What I Learned

### Networking Fundamentals
- [x] Virtual network environments and simulation
- [x] Network device roles (routers, switches, APs)
- [x] Physical vs. Logical network topology differences
- [x] Network design principles for small offices
- [x] Device connectivity and cable management

### Cisco Packet Tracer Specific Skills
- [x] Device configuration in simulator
- [x] Network topology visualization
- [x] Logical mode for planning and troubleshooting
- [x] Physical mode for deployment and documentation
- [x] Network connectivity testing and validation

### Security & Best Practices
- [x] Network segmentation concepts
- [x] Access point configuration
- [x] DHCP and DNS basics
- [x] Firewall rule configuration
- [ ] Security lab exercises (in progress)

### Key Takeaways
1. **Logical vs Physical**: Understanding both views is crucial for network design, deployment, and troubleshooting
2. **Hands-on Practice**: Simulations provide safe environment to learn before real-world implementation
3. **Device Roles**: Different devices (switches, routers, APs) serve specific purposes in a network
4. **Network Design**: Small office networks require careful planning for scalability and security

---

## 🔗 Next Steps / Future Improvements

### Short Term
- [ ] Complete all Cisco security labs
- [ ] Document network testing results with screenshots
- [ ] Add IP addressing configuration details
- [ ] Create network troubleshooting guide

### Medium Term
- [ ] Implement VPN connectivity between lab environments
- [ ] Set up logging/monitoring (Wazuh/ELK)
- [ ] Add vulnerability scanning in Kali VM
- [ ] Integrate Packet Tracer network with VirtualBox VMs

### Long Term
- [ ] Simulate attack scenarios
- [ ] Document security incidents and responses
- [ ] Create disaster recovery procedures
- [ ] Build multi-site network simulation

---

## 📞 Contact & Social

- **GitHub:** [github.com/LamprosTsokris](https://github.com/LamprosTsokris)
- **Portfolio:** [Your portfolio link when ready]
- **LinkedIn:** [Your LinkedIn when ready]

---

## 📄 License

This project is for educational purposes. All configurations and documentation are open for learning and improvement.

---

**Last Updated:** July 15, 2025  
**Status:** In Progress 🔄

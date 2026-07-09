# Home Lab Setup - Cybersecurity & Networking Project

## 📋 Project Overview

This project documents the complete setup of a home lab environment for learning cybersecurity and networking. The lab includes virtual machines running different operating systems, firewall configurations, and network topology documentation.

**Purpose:** Build hands-on skills in network administration, firewall configuration, and Linux/Windows server management.

---

## 🎯 Project Goals

- ✅ Set up virtualization environment (VirtualBox)
- ✅ Install and configure multiple virtual machines (Windows Server, Linux, pfSense)
- ✅ Create a functional network topology
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

---

## 📐 Network Topology

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

### Step-by-Step Setup

#### Phase 1: Firewall Setup
1. **Create pfSense VM**
   - Allocate: 2 cores, 2GB RAM
   - Network: 2 adapters (WAN & LAN)
   - [Detailed steps coming]

2. **Configure pfSense**
   - Set WAN interface to NAT
   - Set LAN interface to 10.0.0.0/24
   - [Configuration details coming]

#### Phase 2: Server Setup
1. **Windows Server VM**
   - Allocate: 2-4 cores, 4GB RAM
   - [Details coming]

2. **Ubuntu Linux VM**
   - Allocate: 2 cores, 3GB RAM
   - [Details coming]

#### Phase 3: Security Tools
1. **Kali Linux VM** (for testing)
   - Allocate: 2 cores, 3GB RAM
   - [Details coming]

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

---

## 📊 Current Progress

- [ ] VirtualBox installed
- [ ] pfSense VM created & configured
- [ ] Windows Server VM created & configured
- [ ] Ubuntu VM created & configured
- [ ] Kali Linux VM created & configured
- [ ] Network connectivity verified
- [ ] Firewall rules documented
- [ ] Screenshots & documentation complete

---

## 📚 Resources & Documentation

### Setup Guides
- [VirtualBox Installation Guide](https://www.virtualbox.org/manual/ch01.html)
- [pfSense Getting Started](https://docs.netgate.com/)
- [Ubuntu Server Installation](https://ubuntu.com/server/docs)

### Tools & Commands Used
```bash
# Example commands to be documented
# Linux network info
ip addr show
ip route show
netstat -an

# Network testing
ping 8.8.8.8
traceroute google.com
```

---

## 📸 Screenshots & Diagrams

*Screenshots of your setup will go here:*
- [ ] VirtualBox VM list
- [ ] Network topology diagram
- [ ] pfSense dashboard
- [ ] Network configuration screenshots

---

## 🔍 Testing & Validation

Document your testing process:
- [ ] Ping test between VMs
- [ ] Internet connectivity test
- [ ] DNS resolution test
- [ ] Firewall rule validation
- [ ] Performance baseline

### Test Results
```
Date: [When you run tests]
Host: [Your PC specs]

Ping test (Win Server to Ubuntu):
- Success: ✓
- RTT: X ms

[Add more tests...]
```

---

## 🚀 What I Learned

*Update this section as you progress:*
- [ ] How virtualization works
- [ ] Network fundamentals (IP addressing, routing)
- [ ] Firewall configuration basics
- [ ] Linux server setup
- [ ] Active Directory basics

### Key Takeaways
1. [Add your learnings here]
2. [What challenges you faced]
3. [How you overcame them]

---

## 🔗 Next Steps / Future Improvements

- [ ] Implement VPN between lab and external network
- [ ] Set up logging/monitoring (Wazuh/ELK)
- [ ] Add vulnerability scanning
- [ ] Simulate attack scenarios
- [ ] Document security incidents

---

## 📞 Contact & Social

- **GitHub:** [github.com/LamprosTsokris](https://github.com/LamprosTsokris)
- **Portfolio:** [Your portfolio link when ready]
- **LinkedIn:** [Your LinkedIn when ready]

---

## 📄 License

This project is for educational purposes. All configurations and documentation are open for learning and improvement.

---

**Last Updated:** July 9, 2025  
**Status:** In Progress 🔄

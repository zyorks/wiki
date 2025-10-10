# From Homelab Engineer to AI Infrastructure Architect

## 🧩 Overview

Starting in **Spring 2026**, I will begin my journey toward becoming a **Cybersecurity Architect** specializing in **AI infrastructure and enterprise networking**.  
This roadmap outlines how I will progress from my academic study at **UTSA’s BBA in Cybersecurity** to advanced Cisco certifications such as **CCIE Data Center**, leading toward a role in **AI-first companies** like NVIDIA or Cisco.

---

## 🎓 Current Certifications and Skills (as of 2025)

| Certification | Focus Area | Status |
|----------------|-------------|---------|
| **CompTIA A+** | IT hardware, troubleshooting, OS fundamentals | ✅ Completed |
| **RHCSA** | Linux system administration and automation | ✅ Completed |
| **Proxmox / pfSense / VLAN Lab** | Virtualization, routing, segmentation | 🧠 Active project |
| **TrueNAS Scale / Rocky Linux / Windows Server 2025** | Domain services, storage, and AD integration | 🧠 Active project |

---

## 📅 Career Roadmap Timeline (2026–2034)

| Year | Phase | Goals & Focus | Key Certifications | Career Milestones |
|------|--------|----------------|--------------------|-------------------|
| **2026–2028** | **Phase 1: Academic Foundation** | Begin UTSA Cybersecurity BBA, strengthen networking and Linux fundamentals, develop Proxmox enterprise lab | CCNA, Security+, AWS Cloud Practitioner | Entry-level IT or NOC Technician, Fiber Field Technician |
| **2028–2030** | **Phase 2: Network Engineering Growth** | Design enterprise VLANs, firewalling, automation (Ansible, Terraform), expand homelab | CCNP Enterprise, CyberOps Associate, Azure/AWS Associate | Network Engineer, Security Operations Engineer |
| **2030–2032** | **Phase 3: Architecture and Automation** | Study Cisco ACI, SDN, VXLAN/EVPN, hybrid cloud networking | CCNP Security, DevNet Professional | Senior Network Architect, Cybersecurity Engineer |
| **2032–2034** | **Phase 4: Cybersecurity & AI Infrastructure** | Focus on AI cluster networking, Zero Trust, and data center automation | CCIE Data Center, CISSP, DevNet Expert | Cybersecurity Architect, AI Infrastructure Architect |

---

## 🧱 Phase 1: Academic Foundation (2026–2028)

**Goal:** Build strong networking and cybersecurity fundamentals while completing UTSA’s BBA in Cybersecurity.

### Focus Areas
- Network architecture, subnetting, and VLANs  
- Virtualization with Proxmox and pfSense  
- Security fundamentals and risk management  
- Scripting with Bash and Python  

### Short-Term Certifications
- 🎯 **Cisco CCNA**
- ⚙️ **CompTIA Security+**
- ☁️ **AWS Cloud Practitioner**

### Experience Targets
- Part-time IT or NOC position  
- Expand Proxmox enterprise network simulation  
- Document homelab projects using **mdBook**

---

## 🚀 Phase 2: Network Engineering Growth (2028–2030)

**Goal:** Transition into full-time network or cybersecurity engineering roles.

### Focus Areas
- Enterprise Layer 2/3 design and VLAN segmentation  
- Automation via **Ansible** and **Terraform**  
- Network monitoring and observability (Prometheus, Grafana)  
- Cloud networking and security integration  

### Key Certifications
- 🧠 **CCNP Enterprise**
- 🔐 **Cisco CyberOps Associate**
- ☁️ **Azure Network Engineer Associate**

### Roles
- Network Engineer  
- Security Operations Engineer  
- Infrastructure Automation Specialist  

---

## 🧩 Phase 3: Advanced Architecture (2030–2032)

**Goal:** Develop advanced data center and security architecture skills.

### Focus Areas
- Cisco ACI (Application Centric Infrastructure)  
- VXLAN, EVPN, and SDN frameworks  
- Cloud-native network automation  
- Identity and Access Management across AD and Kubernetes  

### Certifications
- 📘 **CCNP Security**
- ⚙️ **Cisco DevNet Professional**
- 🧩 **CCIE Data Center (Written)**

### Career Path
- Senior Network Architect  
- Cybersecurity Engineer (Automation Focus)  

---

## 🧠 Phase 4: AI Infrastructure Leadership (2032–2034)

**Goal:** Design and secure high-performance AI networks.

### Focus Areas
- AI cluster networking (InfiniBand, NVLink, RoCEv2)  
- Zero Trust architectures and multi-tenant security  
- High-throughput data center automation pipelines  
- AI security compliance and monitoring  

### Certifications
- 🏅 **CCIE Data Center (Lab Complete)**
- 🔐 **CISSP or CCSP**
- 👨‍💻 **DevNet Expert (Optional)**

### Career Path
- **Cybersecurity Architect**
- **AI Infrastructure Architect**
- **Principal Network Engineer (AI Systems)**

---

## 🧰 Supporting Technologies in the Homelab

| Component | Function | Software Used |
|------------|-----------|----------------|
| **Proxmox VE 9** | Virtualization and orchestration | VLANs, ZFS/Btrfs, nested VMs |
| **pfSense** | Firewall and gateway | VLAN routing, DHCP/DNS services |
| **TrueNAS Scale** | Network-attached storage | iSCSI shares, NFS, SMB |
| **Rocky Linux 10** | K8s nodes and AD clients | Docker, Kubernetes, Realmd |
| **Windows Server 2025** | Domain Controller | AD DS, DNS, GPO, DHCP |
| **Terraform / Ansible** | Automation and infrastructure-as-code | IaC deployment of VMs and configs |

---

## 📚 Continuous Learning Resources

| Area | Recommended Resources |
|-------|-----------------------|
| Networking | “Network Warrior” by Gary Donahue, Jeremy’s IT Lab (YouTube) |
| Linux / Automation | RHCSA Study Guide, Ansible, Terraform Docs |
| Security | TryHackMe, HackTheBox, “Blue Team Field Manual” |
| Cisco | INE Labs, Boson ExSim, Cisco Learning Network |
| Fiber | FOA Online Certification, ETA Fiber Optics Training |

---

## 🏁 Final Vision

By combining formal education from **UTSA**, hands-on **homelab architecture**, and **progressive Cisco certifications**, my long-term mission is to design and secure scalable **AI-driven network infrastructures**.

Through this roadmap, I aim to evolve from a homelab engineer to an **AI Infrastructure Cybersecurity Architect** — capable of building and defending intelligent, data-driven networks for the next generation of computing.

---

## 🏗️ Homelab Topology Overview

My homelab environment is designed to simulate an **enterprise-grade network and cybersecurity infrastructure**, fully virtualized on **Proxmox VE 9** with **pfSense**, **TrueNAS Scale**, and multiple Linux and Windows VMs.  
This environment is used for hands-on practice in **Active Directory**, **network segmentation**, **Kubernetes**, and **infrastructure automation** using **Terraform** and **Ansible**.

---

### 🌐 Network Architecture

| VLAN ID | Subnet | Purpose | Gateway (pfSense) | Example Systems |
|----------|---------|----------|-------------------|-----------------|
| **10** | 10.0.1.0/24 | Management / Infrastructure | 10.0.1.1 | Proxmox, TrueNAS, pfSense LAN |
| **20** | 10.0.2.0/24 | Server / AD Network | 10.0.2.1 | Windows Server 2025 (DC), Rocky Linux AD Nodes |
| **30** | 10.0.3.0/24 | Kubernetes / DevOps | 10.0.3.1 | Rocky Linux K8s Master & Workers |
| **40** | 10.0.4.0/24 | Security / SIEM | 10.0.4.1 | Security Onion, Wazuh |
| **50** | 10.0.5.0/24 | Storage / Backup | 10.0.5.1 | TrueNAS Scale iSCSI, Backup nodes |
| **99** | 10.0.99.0/24 | Out-of-Band / Admin Access | 10.0.99.1 | Management terminals, monitoring tools |

All VLANs are trunked through **pfSense**, which acts as the default gateway, DHCP/DNS provider, and inter-VLAN router.  
Firewall rules and NAT policies are defined in pfSense to isolate or allow traffic between VLANs as needed for testing.

---

### 🧱 Virtual Machine Layout

| VM Name | OS | vCPUs | Memory | Storage | VLAN | Purpose |
|----------|----|-------|---------|----------|-------|----------|
| **pfsense-vm** | pfSense | 4 | 4 GB | 20 GB | VLAN 10 | Core firewall, DHCP/DNS, routing |
| **proxmox-ve** | Proxmox VE 9 | 50 | 95 GB | 680 GB (Btrfs RAID0) | VLAN 10 | Hypervisor hosting entire lab |
| **truenas-scale** | TrueNAS Scale | 4 | 16 GB | 100 GB | VLAN 50 | Centralized storage, NFS/iSCSI |
| **dc01-win2025** | Windows Server 2025 (Core) | 8 | 16 GB | 80 GB | VLAN 20 | Active Directory Domain Controller |
| **ad-node01** | Rocky Linux 10 | 4 | 8 GB | 40 GB | VLAN 20 | AD-joined Linux node |
| **ad-node02** | Rocky Linux 10 | 4 | 8 GB | 40 GB | VLAN 20 | Secondary AD Linux node |
| **k8s-master** | Rocky Linux 10 | 8 | 16 GB | 60 GB | VLAN 30 | Kubernetes control plane |
| **k8s-worker01** | Rocky Linux 10 | 8 | 16 GB | 60 GB | VLAN 30 | K8s worker node |
| **siem-node** | Rocky Linux 10 | 6 | 16 GB | 80 GB | VLAN 40 | Wazuh or Security Onion SIEM server |

---

### 🧩 Network Services Overview

| Service | Provided By | VLAN | Description |
|----------|--------------|------|-------------|
| **DHCP / DNS** | pfSense | 10, 20, 30, 40, 50 | Dynamic addressing and domain resolution |
| **Active Directory (AD DS)** | Windows Server 2025 | 20 | Domain Controller and central auth |
| **LDAP / Kerberos Integration** | AD DS + Rocky Linux | 20 | SSO for Linux nodes and K8s |
| **NFS / SMB / iSCSI** | TrueNAS Scale | 50 | Centralized storage and VM backups |
| **Kubernetes Cluster** | Rocky Linux nodes | 30 | Container orchestration for apps |
| **SIEM Stack** | Rocky Linux (Wazuh / Security Onion) | 40 | Security event monitoring and log analysis |
| **Automation / IaC** | Terraform, Ansible | 10 / 30 | Automates provisioning and configuration |

---

### 🔒 Security and Segmentation

- **pfSense** enforces inter-VLAN policies — for example, K8s nodes can reach AD for authentication but not directly access SIEM.
- VLAN 99 is isolated for **admin-only access** to pfSense, TrueNAS, and Proxmox GUIs.
- All traffic to the internet routes through pfSense’s **WAN** (bridged or passthrough NIC).
- Firewall rules simulate **Zero Trust segmentation**, testing lateral movement prevention and network hardening.

---

### ⚙️ Automation and Integration

- **Terraform** provisions VMs, network bridges, and VLANs inside Proxmox.
- **Ansible** configures systems post-deployment (networking, packages, K8s init).
- **LDAP / RealmD** connects Linux systems to AD for central authentication.
- **TrueNAS** shares storage via iSCSI/NFS for VM disks and backup volumes.
- **Kubernetes** runs lab microservices and containerized testing tools.

---

### 🧠 Lab Use Cases

- Practicing **Active Directory and LDAP integration** with Linux-based services  
- Simulating **enterprise segmentation and security policy enforcement**  
- Deploying **Kubernetes and Terraform** in realistic networked environments  
- Hosting **SIEM and log correlation tools** for threat monitoring practice  
- Running **TrueNAS-based storage networks** with VLAN-isolated traffic  

---

## 🧩 Summary

This homelab provides a self-contained **enterprise network ecosystem** designed for hands-on learning in:

- Network security architecture  
- Virtualization and infrastructure-as-code  
- Active Directory and domain management  
- Kubernetes and DevOps automation  
- Cybersecurity monitoring and analysis  

Together, these systems form the foundation for my path toward becoming an **AI Infrastructure Cybersecurity Architect** — blending networking, security, and automation into one cohesive platform for experimentation and professional growth.

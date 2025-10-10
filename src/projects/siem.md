# Building a Virtual Enterprise Infrastructure for DevOps, Security, and AI Research

## Introduction

I built this lab to demonstrate end-to-end enterprise infrastructure skills: network segmentation, identity management, orchestration, storage, and AI workloads.
It’s a reproducible, interview-ready project that showcases practical experience with modern systems engineering and DevOps tools.

---

## Overview

This project replicates a small enterprise network with domain services, Linux and Windows integration, DevOps automation, and a Kubernetes cluster — all virtualized under Proxmox VE 9.

---

## Host Hardware

* **CPU:** AMD Threadripper 9970X (32 cores / 64 threads)
* **Memory:** 128 GB DDR5-5600
* **GPU:** NVIDIA RTX 5090 (VFIO-ready)
* **Storage:** Samsung 9100 PRO 1 TB NVMe
* **Motherboard:** ASUS TRX50-SAGE Pro WS A
* **PSU:** Corsair RM1000e 1000 W Gold

---

## Virtualization Stack

* **Host OS:** Arch Linux
* **Hypervisor:** Proxmox VE 9
* **Filesystem:** Btrfs RAID0 with zstd compression
* **Network:** VLAN-aware bridges (vmbr0) with pfSense as the virtual router/firewall

---

## Network Design

The lab network is segmented into multiple VLANs for isolation and realism. Each VLAN maps to a distinct subnet in the 10.0.x.0/24 range.

| VLAN | Purpose             | Subnet      | Gateway  | DHCP Range           |
| ---- | ------------------- | ----------- | -------- | -------------------- |
| 10   | Management          | 10.0.1.0/24 | 10.0.1.1 | 10.0.1.100–10.0.1.200 |
| 20   | Servers / AD        | 10.0.2.0/24 | 10.0.2.1 | 10.0.2.100–10.0.2.200 |
| 30   | Kubernetes / DevOps | 10.0.3.0/24 | 10.0.3.1 | 10.0.3.100–10.0.3.200 |
| 40   | NAS / Storage       | 10.0.4.0/24 | 10.0.4.1 | 10.0.4.100–10.0.4.200 |
| 50   | SIEM / Cyber Range  | 10.0.5.0/24 | 10.0.5.1 | 10.0.5.100–10.0.5.200 |

---

## Virtual Machine Topology

| Hostname | OS / Role                   | VLAN  | IP        | vCPU | RAM  | Notes                                |
| -------- | --------------------------- | ----- | --------- | ---- | ---- | ------------------------------------ |
| FW01     | pfSense (Firewall/Router)   | trunk | 10.0.x.1  | 4    | 4 GB | Trunked for all VLANs                |
| DC01     | Windows Server 2025 Core    | 20    | 10.0.2.10 | 6    | 8 GB | AD DS + DNS                          |
| ADLIN01  | Rocky Linux 10 (Client)     | 20    | 10.0.2.20 | 4    | 4 GB | AD-joined                            |
| ADLIN02  | Rocky Linux 10 (Client)     | 20    | 10.0.2.21 | 4    | 4 GB | AD-joined                            |
| K8S-M1   | Rocky Linux 10 (K8s Master) | 30    | 10.0.3.10 | 8    | 8 GB | Control Plane                        |
| K8S-W1   | Rocky Linux 10 (K8s Worker) | 30    | 10.0.3.11 | 6    | 6 GB | Worker                               |
| K8S-W2   | Rocky Linux 10 (K8s Worker) | 30    | 10.0.3.12 | 6    | 6 GB | Optional Worker                      |
| NAS01    | TrueNAS SCALE               | 40    | 10.0.4.10 | 2    | 4 GB | NFS / SMB / Kubernetes-ready storage |
| SIEM01   | Rocky Linux 10 (Wazuh SIEM) | 50    | 10.0.5.10 | 4    | 8 GB | IDS + Log Aggregation                |

---

## Storage Integration

**TrueNAS SCALE** delivers:

* NFS + iSCSI for Kubernetes persistent volumes
* SMB shares for Windows and Linux clients
* AD integration for ACL management
* Built-in Docker and K3s support
* ZFS snapshots and replication

---

## Identity & Access

* **AD Domain:** `lab.local`
* **Domain Controller:** DC01 (10.0.2.10)
* Linux clients join AD via `realm join --user=Administrator lab.local`
* DNS points to the AD server to enable Kerberos authentication and group-based access.

---

## Kubernetes & DevOps

* Cluster setup with `kubeadm`, `containerd`, and Calico CNI
* Terraform manages VM provisioning and cluster resources
* AD integration planned through OIDC (Dex or Keycloak)
* Practice environment for IaC and GitOps (ArgoCD)

---

## AI & Cyber Range

* **Ollama + OpenWebUI** on host GPU for LLM use
* **Stable Diffusion** for image and video generation
* **SIEM01** collects telemetry and detects simulated attacks from Cyber Range VMs

---

## Technical Highlights

* Multi-VLAN design using Proxmox VE 9 and pfSense
* Hybrid Windows/Linux identity integration
* Kubernetes cluster automation with Terraform
* Enterprise-class storage with TrueNAS SCALE
* SIEM deployment and network security simulation

---

## Next Steps

* Integrate OIDC authentication for Kubernetes
* Expand Terraform automation and GitOps tooling
* Deploy centralized logging (OpenSearch / ELK)
* Extend cyber range and incident response testing

---

**Author:** Zach Yorks
**Date:** October 2025
**Technologies:** Proxmox VE 9 | pfSense | Windows Server 2025 | Rocky Linux 10 | TrueNAS SCALE | Kubernetes | Terraform
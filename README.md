# VMware Virtualization Lab (vSphere-Style on Workstation)

This lab simulates a small virtual infrastructure using VMware Workstation or ESXi.

## Objectives

- Build a virtualized environment with multiple networks (management + client).
- Deploy Windows Server and Windows 11 clients as VMs.
- Run AD/DNS/DHCP on a server VM.
- Practice snapshotting, resource allocation, and simple hardening.

## Example Topology

- **Hypervisor:** VMware Workstation / ESXi
- **VMs:**
  - `DC01` – Windows Server 2022 (AD DS, DNS, DHCP)
  - `WIN11-CL01` – Windows 11 client
  - (Optional) Linux server for testing

## Networks

- `VM-MGMT` – Management / Servers (host-only)
- `VM-CLIENTS` – Client access network

## High-Level Steps

1. Create two custom networks in VMware (or use NAT + Host-only).
2. Deploy `DC01`, configure static IP and domain services.
3. Deploy `WIN11-CL01`, join `corp.lab`.
4. Take snapshots before and after major changes.
5. Use the `CIS-Benchmark-Checklist.md` as a mini hardening guide.

This lab is meant to reflect how I work with virtual infrastructure and align it to security baselines.

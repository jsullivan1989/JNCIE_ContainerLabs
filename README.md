# 🧪 JNCIE ContainerLabs

> **Juniper Networks Certified Internet Expert — Service Provider**
> A growing collection of hands-on ContainerLab topologies designed to help you study, validate, and master the technologies tested on various **JNCIE** exams.  Initially a repo for the JNCIE-SP only but has grown to multiple JNCIE-level lab topics.

---

## 📖 About This Repository

This repository is a personal study lab environment built using [ContainerLab](https://containerlab.dev/), a powerful network emulation framework that spins up realistic topologies using containerized network operating systems — including **Juniper cRPD** and **vJunos**.

These are various labs that have been setup and torn down while initially studying for the JNCIE-SP exam and now the JNCIE-DC exam.

Labs will be added incrementally as they are built and validated. Each lab includes a topology file, relevant configuration snippets, and notes on expected behavior.

The majority of the labs were built using vJunos-router, vJunos-switch, and vSRX images with logical-systems, logical-tunnel interfaces, and routing-instances used to further segment logical devices within the virtual image to increase capacity.  

---

## 🗂️ Planned Lab Topics - JNCIE-SP

| Category | Lab |
|---|---|
| **IGP** | IS-IS Single/Multi-Level |
| **IGP** | OSPF / OSPFv3 Interoperability |
| **MPLS** | LDP Label Distribution |
| **MPLS** | RSVP-TE Signaled LSPs |
| **MPLS** | Segment Routing (MPLS & SRv6) |
| **L3VPN** | Hub-and-Spoke Layer 3 VPNs |
| **L3VPN** | Multicast VPNs (NG-MVPN) |
| **L2VPN** | Layer 2 VPNs (L2Circuit / Kompella) |
| **L2VPN** | VPLS (LDP & BGP Signaled) |
| **L2VPN** | EVPN (Type 2 / Type 5) |


## 🗂️ Planned Lab Topics - JNCIE-DC

| Category | Lab |
|---|---|
| **EVPN VXLAN L2VNI** | Intra-VLAN traffic same Tenant  |
| **EVPN VXLAN L3VNI** | Inter-VLAN traffic same Tenant|
| **EVPN VXLAN Security** | Inter-Tenant Traffic with SRX Hairpin|
| **Over the Top EVPN GW** | Over the Top Inter-POD VTEP Mesh
| **Inter POD DCI**| Datacenter Interconnect for Type 2 and Type 5 routing between Pods
| **Hub and Spoke Pod**| Designating a Pod Border Leaf as the Control Plane hub for OTT EVPN GW
|**WAN Access**| Underlay BGP peering between POD Border Leafs and a vMX router

> More labs will be added over time. Watch or star the repo to get notified of new additions.

---

## 🛠️ Prerequisites

- [ContainerLab](https://containerlab.dev/install/) installed on a Linux host
- Access to **Juniper cRPD** or **vJunos** images (requires a valid Juniper account / license)
- Basic familiarity with YAML topology files and Junos CLI
- Recommended: 32+ GB RAM for multi-node topologies

---

## To Clone 

Clone the repository and navigate to any lab directory:

```bash
git clone https://github.com/jsullivan1989/JNCIE_ContainerLabs
cd JNCIE_ContainerLabs/{{Lab_Directory}}/Topology/
```

Deploy a topology:

```bash
sudo containerlab deploy -t {{Topology_File}}.yml
```

Destroy when done:

```bash
sudo containerlab destroy -t topology.yml
```

Each lab folder contains its own `README.md` with a topology diagram, objectives, and configuration walkthrough.






# Homelab Hardware Projects

Open-source documentation and reference designs for building a compact, modular homelab using commercially available hardware, custom 3D-printed components, and repurposed equipment.

## Purpose

Sanitized public reference. Private network information, credentials, device identifiers, exact home infrastructure details, and other sensitive information are intentionally excluded.

## Projects

- **OptiPlex 7060 Custom Enclosure**
- **Micro-ATX Custom Server**
- **Compact Homelab Rack**
- **Future Permanent Rack**
- **Home Security & Automation**

## Documentation Philosophy

Projects are documented as they actually develop, including problems encountered, failed approaches, design mistakes, prototype revisions, testing results, decisions and their rationale, and final solutions.

The goal is to preserve the reasoning behind the build, not merely the final result.

## Planned DNS redundancy

**Future concept, not deployed:** evaluate a cold-standby backup Pi-hole Debian VM on an already-acquired Dell OptiPlex 7060 SFF, with Proxmox VE now installed on the host for resilient, filtered DNS on LAN and private VPN clients. Compare dual advertised Pi-hole resolvers with health-checked DNS proxy or virtual-IP approaches; only the latter can enforce a strict primary/standby selection when implemented correctly. Reported host specs: Intel Core i7-8700, 24 GB RAM, 512 GB storage of unverified type; subsequently inspected and deployed. Initial host inspection and Proxmox deployment have since been completed. Evaluate monitoring, VM startup, DNS handoff/virtual-IP ownership, split-brain prevention, synchronization, private VPN access, outage testing, and failback. Booting the VM alone does not redirect DNS. A second physical Pi-hole remains an alternative. No private addresses, hostnames, or identifying network details are included.


## Infrastructure status update (October 2026)

The repurposed OptiPlex has since been inspected and deployed as a live Proxmox virtualization host. It now runs Linux workloads including a dedicated containerized media-server VM. The earlier description of Proxmox as not yet installed is superseded. Additional drive bays, faster networking, custom enclosure/rack integration, NAS purchases and cold-standby DNS failover remain planned rather than deployed. This update concerns compute deployment, not a completed hardware modification.

## November 2026 project status

The OptiPlex Proxmox host remains deployed. Jellyfin 12.4 and the Homepage dashboard are operational, and What's Up Docker provides container update visibility. No new hardware purchases or rack builds are claimed. The compact rack and faster wired networking remain planned and subject to fit, cooling, and testing.

## November 2, 2026 — infrastructure monitoring milestone

The deployed Proxmox environment now includes a working Homepage What's Up Docker widget, showing monitored container and available-update counts. This is a software monitoring milestone; no new physical hardware or planned rack/network/NAS upgrades are claimed.

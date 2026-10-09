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

**Future concept, not deployed:** evaluate a cold-standby backup Pi-hole Debian VM on an already-acquired Dell OptiPlex 7060 SFF, with Proxmox VE recommended as its future host OS (not installed) for resilient, filtered DNS on LAN and private VPN clients. Compare dual advertised Pi-hole resolvers with health-checked DNS proxy or virtual-IP approaches; only the latter can enforce a strict primary/standby selection when implemented correctly. Reported host specs: Intel Core i7-8700, 24 GB RAM, 512 GB storage of unverified type; not yet booted or inspected. First verify existing Windows installation and hardware before reimaging. Evaluate monitoring, VM startup, DNS handoff/virtual-IP ownership, split-brain prevention, synchronization, private VPN access, outage testing, and failback. Booting the VM alone does not redirect DNS. A second physical Pi-hole remains an alternative. No private addresses, hostnames, or identifying network details are included.


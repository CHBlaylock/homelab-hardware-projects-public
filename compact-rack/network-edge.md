# Network Edge

**Status:** Planning

## Requirements

The homelab is being designed around a multi-gigabit Internet connection, with 2.5 GbE as the preferred minimum for new core network equipment and a future path toward 10 GbE.

## Planned Architecture

```
Internet
   |
ISP modem / ONT
   |
Router / firewall
   |
Managed core switch
   |
+-- Servers
+-- NAS
+-- Raspberry Pi appliances
+-- Security / PoE infrastructure
+-- Clients / access points
```

## Equipment Selection

Future modem/ONT and router/firewall choices should be verified against the Internet provider's current compatibility and service requirements at the time of purchase. Historical product recommendations are not treated as permanent compatibility guarantees.

## Rack Planning

The eventual infrastructure should provide for the Internet edge, managed switching, structured cabling, UPS/PDU, servers, storage, and PoE/security equipment.

Standalone Raspberry Pi appliances can remain outside the rack when their cases already provide the desired physical enclosure.

## Design Principles

- Prefer 2.5 GbE for new core equipment.
- Leave a path toward 10 GbE.
- Design for expansion rather than the smallest current configuration.
- Keep the temporary infrastructure portable so it can migrate to a future permanent rack.

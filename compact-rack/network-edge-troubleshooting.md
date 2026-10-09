# Internet Outlet Relocation Troubleshooting

**Status:** Completed

## Objective

Relocate the ISP gateway from one coax outlet to a second room so the network equipment could be positioned closer to the homelab and primary workstation.

## Problem

The second outlet initially failed to establish a stable Internet connection even though the original outlet worked normally.

## Investigation

The accessible coax distribution point and both ends of the room's coax run were inspected. A new attic termination initially produced an intermittent connection, but the gateway repeatedly lost synchronization.

The room-end wall-plate connection was then bypassed for testing. The legacy connector was found to be mechanically failed: it could be pulled directly off the coax cable.

## Fix

The failed room-end connector was replaced. The gateway was tested directly on the newly terminated cable and remained online. The router and downstream equipment were then reconnected.

## Verification

A wired speed test reached approximately 2.4 Gbps on a 2 Gbps service.

This confirmed that the complete path could support the multi-gigabit connection and that the in-wall coax run itself was usable.

## Lessons Learned

- Intermittent physical-layer problems are not necessarily caused by the cable inside the wall.
- Inspect and mechanically test accessible terminations before assuming a buried cable is damaged.
- Bypassing a wall plate is a useful diagnostic technique.
- Test the gateway by itself before reconnecting downstream equipment.
- Validate the final network path with a wired speed test.

## Infrastructure Takeaway

The experience reinforced the value of accessible, securely terminated, and well-documented structured cabling in a future homelab/network rack.

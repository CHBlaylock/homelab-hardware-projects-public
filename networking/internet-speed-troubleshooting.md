# Internet Speed Troubleshooting: Wi-Fi 7 vs ISP Throughput

## Scenario
A 2 Gbps cable Internet plan delivered only 208 Mbps down / 111 Mbps up to a desktop with a Wi-Fi 7 PCIe adapter connected through a dual-band Wi-Fi 7 router.

## Diagnostic observations
- Desktop wireless association: 5 GHz Wi-Fi 7, channel 36, 2882/2882 Mbps negotiated link rate.
- Router WAN Ethernet: 2.5 Gbps full duplex.
- Router configuration reviewed: dedicated 5 GHz network, Smart Connect off, 160 MHz-capable channel configuration; OFDMA + MU-MIMO enabled.
- Phone and desktop both produced approximately 320–430 Mbps down during the degraded period.
- Multiple test services produced broadly consistent results.

**Interpretation:** Fast local Wi-Fi and WAN Ethernet link rates did not establish actual ISP throughput. Similar slow results across multiple wireless clients made a desktop-only adapter issue less likely.

## What changed
The ISP reported neighborhood maintenance. After the maintenance window, the phone reached roughly 754 Mbps down and the desktop roughly 630–650 Mbps. Disconnecting and reconnecting desktop Wi-Fi later produced approximately 830 Mbps on Fast.com and 742 Mbps down / 114 Mbps up on Speedtest.

This is consistent with an ISP-side contribution to the initial speed problem. A wired benchmark was not performed, so the full 2 Gbps service rate was not independently validated.

## Separate problem: competing wireless adapters
The desktop also had onboard Wi-Fi 6E, which Windows repeatedly selected instead of the preferred PCIe Wi-Fi 7 adapter after power cycles.

Attempted without a lasting fix:
1. Disable onboard adapter in Device Manager.
2. Uninstall onboard adapter and driver.
3. Look for a firmware WLAN disable switch.
4. Disable motherboard vendor utilities download setting and uninstall the vendor management utility.

The onboard adapter continued to return. Physical removal of its wireless module was discussed but **not carried out**. The working compromise was manually disabling onboard Wi-Fi after startup and connecting with the PCIe card.

## Lessons learned
- Distinguish negotiated link rate from end-to-end Internet speed.
- Compare more than one client and test provider.
- Check ISP incidents before making disruptive local hardware changes.
- Document unsuccessful fixes and verify whether a setting persists across a cold boot.
- For definitive throughput isolation, use a wired device with an appropriately rated Ethernet interface.

This public case study deliberately omits SSIDs, addresses, account details, and identifiable screenshots.

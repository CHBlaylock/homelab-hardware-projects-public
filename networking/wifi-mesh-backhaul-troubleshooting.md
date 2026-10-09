# Wi-Fi Mesh Backhaul Troubleshooting

## Symptom
A desktop near an office mesh satellite experienced extremely slow or unusable Internet despite a strong wireless connection. The desktop sometimes associated with the distant main router rather than the nearby satellite.

## Diagnostic progression
1. Investigated desktop wireless adapter roaming and band preferences.
2. Inspected available BSSIDs and verified the actual connected access point with Windows wireless status commands.
3. Confirmed the office satellite's wireless signal to the desktop was strong, with a healthy local connection.
4. Tested connectivity across the network path rather than relying on the Wi-Fi signal indicator.
5. Found the client-to-satellite hop had low latency and no observed packet loss, while the satellite's onward path to the main router suffered severe latency and packet loss.

## Root cause identified
The office satellite was using a poor direct wireless backhaul to the main router instead of a hoped-for intermediate hallway satellite. A strong client-to-satellite signal therefore masked a broken onward path.

## Unsuccessful approaches and constraints
- Changing client roaming preferences did not fix the mesh backhaul.
- Attempting to force a particular BSSID with an unsupported Windows command was unsuccessful.
- The mesh interface exposed a manual preferred-parent access point setting but did not list an alternative parent for selection.
- Repositioning/restarting and exploring backhaul steering did not establish a documented permanent fix.

## Options considered
- Wired Ethernet backhaul between mesh nodes.
- Repositioning satellites to improve their uplink signal.
- Adjusting wireless radio power where supported.
- Changing the topology or adding a better backhaul path.

These were proposals, **not confirmed completed fixes**.

## Lessons learned
- Strong Wi-Fi signal on the client does not guarantee working Internet.
- Troubleshoot each hop: client → satellite → backhaul → main router → Internet.
- Packet loss and latency measurements can reveal failures hidden by high local link speeds.
- Verify the specific router firmware's supported controls rather than assuming features exist.

## Privacy
This public write-up omits SSIDs, IP and MAC addresses, device identifiers, and account details.

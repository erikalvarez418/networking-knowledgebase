# Routers vs Switches vs Hubs

Routers, switches, and hubs are foundational network devices — each plays a different role in how data is sent and received across a network.

Understanding their functions helps you troubleshoot traffic flow, design networks, and know which device is causing a problem.

---

## Why It Matters in Real Life

- Routers connect networks together (like LAN to WAN).
- Switches connect devices inside a network (PCs, printers, etc.).
- Hubs are outdated but may still appear in legacy environments.

---

## Quick Comparison

| Feature         | Hub                    | Switch                        | Router                             |
|-----------------|------------------------|-------------------------------|-------------------------------------|
| OSI Layer       | Layer 1 (Physical)     | Layer 2 (Data Link)           | Layer 3 (Network)                   |
| Traffic Type    | Broadcasts all traffic | Forwards to specific MAC      | Routes between networks/IPs         |
| Intelligence    | Dumb                   | Smart (uses MAC table)        | Very smart (uses routing tables)    |
| Common Use      | Rare/obsolete          | Connecting LAN devices        | Connecting LAN to WAN or internet   |
| Speed           | Shared bandwidth       | Dedicated per port            | Depends on uplink/ISP               |

---

## What Each Device Does

### Hub
- Repeats traffic to **all** ports
- No filtering or intelligence
- Causes collisions in busy networks
- Obsolete today

### Switch
- Learns MAC addresses of connected devices
- Sends data only to the correct port
- Supports VLANs and port security
- Used in nearly all LANs today

### Router
- Forwards data based on IP addresses
- Connects different networks (e.g., LAN to WAN)
- Assigns IPs via DHCP
- Performs NAT, routing, firewalling

---

## Real-World Use Cases

| Scenario                             | Device Needed |
|--------------------------------------|---------------|
| Connecting laptops and printers      | Switch        |
| Linking a home or office to the ISP  | Router        |
| Viewing all traffic for analysis     | Hub (for labs only) |

---

## Technician Tip

> If you're diagnosing internal LAN issues, you're likely dealing with a **switch**. If it's a problem with internet access or routing between networks, look at the **router**.

---

## Modern Network Example

Devices → Switch → Router → Modem/ISP

---

## Related Topics

- [MAC vs IP Addresses](../01-Networking-Fundamentals/MAC_vs_IP_Addresses.md)
- [Layer 2 Switching and MAC Tables](../04-Routing_and_Switching/Layer_2_Switching_and_MAC_Tables.md)
- [NAT and PAT](../06-Network_Services/NAT_and_PAT.md)

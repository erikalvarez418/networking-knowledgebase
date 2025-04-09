# Modems and Gateways

Modems and gateways connect your local network to the wider internet. While they’re often combined in consumer devices, they serve distinct purposes in enterprise environments.

---

## Why It Matters in Real Life

Whether you're setting up a school network or troubleshooting connectivity issues, understanding the role of a **modem** or **gateway** is key to identifying where the problem lies — especially when working with ISPs.

---

## What is a Modem?

A **modem** (modulator-demodulator) converts digital data from your network into a signal that can travel over ISP infrastructure (like cable or DSL) — and vice versa.

### Common Modem Types:
- **Cable Modem** (DOCSIS): Coax to Ethernet (e.g., Spectrum, Xfinity)
- **DSL Modem**: Phone line to Ethernet
- **Fiber ONT**: Converts fiber optic light to Ethernet

---

## What is a Gateway?

A **gateway** is a device that connects two different networks and handles protocol translation or routing. In many home setups, the router and modem are combined into a single gateway device.

### In Enterprise Settings:
- Gateway = Edge router that connects LAN to ISP
- Performs routing, NAT, and firewalling

---

## Modem vs Gateway

| Feature          | Modem                          | Gateway                            |
|------------------|--------------------------------|-------------------------------------|
| Purpose          | Signal conversion              | Network routing + translation      |
| Layer            | Layer 1 (Physical)             | Layer 3 (Network)                  |
| Common Location  | ISP handoff                    | Inside network or on edge router   |
| Example Device   | Cable modem                    | Router with NAT + firewall         |

---

## Real-World Use Cases

| Scenario                                    | Device      |
|---------------------------------------------|-------------|
| School with fiber internet                  | Fiber ONT (modem) + Firewall Gateway |
| Home user with bundled ISP equipment        | Modem/Router combo gateway           |
| Business connecting multiple ISPs           | Dual-WAN Gateway or Edge Router      |

---

## Technician Tip

> If you’re not getting a public IP, check the modem status. If the modem is fine but no LAN traffic is working, shift focus to the gateway/router.

---

## ISP vs Network Ownership

| Device Type | Typically Managed By |
|-------------|----------------------|
| Modem       | ISP (unless bridged) |
| Gateway     | You or your IT team  |

---

## Related Topics

- [Routers vs Switches vs Hubs](./Routers_vs_Switches_vs_Hubs.md)
- [NAT and PAT](../06-Network_Services/NAT_and_PAT.md)
- [Public vs Private IPs](../02-IP_Addressing_and_Subnetting/IP_Classes_and_Private_IPs.md)

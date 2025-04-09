# OSI Model

The OSI (Open Systems Interconnection) model is a conceptual framework used to understand and standardize how different networking protocols and devices interact. It's a 7-layer model that breaks down the complex process of communication into smaller, manageable parts.

> In practice, most networking tools and troubleshooting steps revolve around Layers 1–4.

---

## Why It Matters in Real Life

Understanding the OSI model helps technicians:
- Diagnose issues faster (e.g., “Is this a Layer 1 or Layer 3 problem?”)
- Communicate clearly with vendors or teammates
- Understand how firewalls, switches, and routers operate

---

## The 7 Layers of the OSI Model

| Layer | Name             | Description                              | Examples                              |
|-------|------------------|------------------------------------------|----------------------------------------|
| 7     | Application      | Interface for user applications          | HTTP, FTP, DNS, Outlook, Chrome        |
| 6     | Presentation     | Data translation, encryption, formatting | SSL/TLS, JPEG, ASCII                   |
| 5     | Session          | Manages sessions and connections         | NetBIOS, RPC, SSH sessions             |
| 4     | Transport        | Reliable delivery, flow control          | TCP, UDP                               |
| 3     | Network          | Routing and addressing                   | IP, ICMP, routers                      |
| 2     | Data Link        | MAC addressing, switching, framing       | Ethernet, VLANs, switches              |
| 1     | Physical         | Electrical signals, cabling              | Cables, NICs, Hubs, fiber optics       |

---

## Practical Examples

- **Can't access a website?** Start at Layer 1 and work up.
- **A laptop is not getting an IP address:** Check if the Ethernet cable (Layer 1) is connected, then look at the switch (Layer 2), then DHCP (Layer 7).
- **Ping fails to a known IP:** Troubleshoot Layers 1 through 3 — cable, switch, router.

---

## Real-World Layer Mapping

| Device/Protocol         | OSI Layer |
|-------------------------|-----------|
| Patch Cable             | 1         |
| Network Switch          | 2         |
| IP Addressing           | 3         |
| TCP/UDP Ports           | 4         |
| HTTP/HTTPS              | 7         |

---

## Technician Tip

> Always think: “Which OSI layer could be failing?” when troubleshooting. It brings order to chaos.

---

## Related Topics
- [IP Addressing](../02-IP_Addressing_and_Subnetting/IP_Classes_and_Private_IPs.md)
- [TCP vs UDP](../04-Routing_and_Switching/Routing_Protocols.md)


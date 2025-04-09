# IPv4 vs IPv6

IP addresses are used to identify devices on a network. IPv4 is the older, widely-used standard. IPv6 is the newer version created to solve address exhaustion and improve efficiency.

---

## Why It Matters in Real Life

As more devices connect to the internet, IPv4 addresses are running out. You'll see IPv6 more often in:
- Modern networks and data centers
- ISP deployments
- Cloud infrastructure (AWS, Azure, GCP)

Knowing how both versions work helps you configure systems and troubleshoot effectively.

---

## Quick Comparison

| Feature           | IPv4                          | IPv6                                     |
|-------------------|-------------------------------|-------------------------------------------|
| Address Length    | 32-bit                        | 128-bit                                   |
| Format            | Decimal (e.g. 192.168.1.1)    | Hexadecimal (e.g. 2001:0db8::1)           |
| Total Addresses   | ~4.3 billion                  | ~340 undecillion                          |
| Header Complexity | Simpler                       | More efficient with extension headers     |
| NAT Requirement   | Common                        | Not required (but still used sometimes)   |
| Configuration     | DHCP or static                | SLAAC, DHCPv6, or static                  |
| Security          | Add-on (IPSec optional)       | Built-in (IPSec mandatory)                |

---

## Real-World Use Cases

| Scenario                              | IPv4 or IPv6 | Reason                                     |
|---------------------------------------|--------------|--------------------------------------------|
| Internal office network               | IPv4         | Simpler and still widely supported         |
| Large-scale cloud deployment          | IPv6         | More scalable, native support              |
| IoT devices with global connectivity  | IPv6         | Direct access, no NAT required             |
| Older legacy software                 | IPv4         | Might not support IPv6                     |

---

## Address Format Examples

**IPv4 Addresses:**
- 192.168.1.100  
- 10.0.0.1  
- 172.16.5.250  

**IPv6 Addresses:**
- 2001:0db8:85a3:0000:0000:8a2e:0370:7334  
- fe80::1  
- ::1 (loopback)

> Note: IPv6 allows shorthand like `::` to replace consecutive zeros.

---

## Transition Technologies

Because most of the internet still relies on IPv4, several technologies bridge the gap:
- **Dual Stack:** Devices run IPv4 and IPv6 simultaneously
- **Tunneling:** IPv6 packets travel over IPv4 infrastructure
- **NAT64/DNS64:** Allows IPv6-only clients to communicate with IPv4 servers

---

## Technician Tip

> If you see an address starting with `fe80::`, that’s a **link-local** IPv6 address — it's only valid on that local network segment.

---

## Related Topics

- [MAC vs IP Addresses](./MAC_vs_IP_Addresses.md)
- [DHCP](../06-Network_Services/DHCP.md)
- [Routing Protocols](../04-Routing_and_Switching/Routing_Protocols.md)

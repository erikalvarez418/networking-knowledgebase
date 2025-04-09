# MAC vs IP Addresses

MAC and IP addresses are both unique identifiers used in networking, but they serve very different purposes. Understanding their roles is critical when configuring devices, troubleshooting network issues, or securing a network.

---

## Why It Matters in Real Life

When you're diagnosing issues like:
- A device not getting an IP address
- Duplicate IP conflicts
- Devices not showing up in DHCP logs

...you’ll need to understand **both** MAC and IP addresses to pinpoint the problem.

---

## What’s the Difference?

| Type         | MAC Address                          | IP Address                          |
|--------------|--------------------------------------|-------------------------------------|
| Stands For   | Media Access Control                 | Internet Protocol                   |
| Level        | Layer 2 (Data Link)                  | Layer 3 (Network)                   |
| Format       | 6-byte Hex (e.g., `00:1A:2B:3C:4D:5E`) | IPv4: `192.168.1.100`, IPv6: `fe80::1` |
| Assigned By  | Manufacturer (burned into NIC)       | Network (via DHCP or manual config) |
| Purpose      | Uniquely identify device on LAN      | Route packets across networks       |
| Changes?     | Rarely changes                       | Can change often (dynamic IPs)      |

---

## Real-World Analogy

- **MAC Address = Street Address** on your house — it doesn’t change and is unique on your block.
- **IP Address = Mailing Address** with ZIP code — it changes if you move but allows others to send you data.

---

## When Do You Use Each?

| Scenario                             | Use MAC or IP? | Why?                                          |
|--------------------------------------|----------------|-----------------------------------------------|
| Reserving a static IP in DHCP        | MAC            | DHCP uses the MAC to assign consistent IP     |
| Blocking a device from Wi-Fi         | MAC            | Access control lists (ACLs) use MAC filtering |
| Ping or Remote Desktop               | IP             | All traffic is routed using IP                |
| Switch forwarding decision           | MAC            | Switches use MAC tables to forward frames     |
| Router forwarding decision           | IP             | Routers use IP routing tables                 |

---

## Technician Tip

> When you're at the switch level, think **MAC**. When you're at the router or firewall level, think **IP**.

---

## How to Find Them

**On Windows (Command Prompt):**

ipconfig /all

**On macOS/Linux:**

ifconfig
# or
ip addr show

## Related Topics

- [IPv4 vs IPv6](./IPv4_vs_IPv6.md)
- [DHCP](../06-Network_Services/DHCP.md)
- [Layer 2 Switching and MAC Tables](../04-Routing_and_Switching/Layer_2_Switching_and_MAC_Tables.md)



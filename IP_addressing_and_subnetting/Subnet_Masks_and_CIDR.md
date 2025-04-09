# Subnet Masks and CIDR

Subnet masks and CIDR (Classless Inter-Domain Routing) notations define how IP addresses are split between the **network** and **host** portions. They are essential for routing, subnetting, and IP planning.

---

## Why It Matters in Real Life

You’ll run into subnet masks and CIDR notations when:
- Setting static IPs on devices
- Configuring firewalls and routers
- Breaking up large networks into smaller subnets
- Understanding how routing tables match traffic

---

## Subnet Mask Explained

A **subnet mask** is a 32-bit number that "masks" an IP address to show how many bits belong to the **network** and how many to the **host**.

Example:

- IP Address: `192.168.1.10`  
- Subnet Mask: `255.255.255.0`

This means:
- First 24 bits = network
- Last 8 bits = host

---

## CIDR Notation

CIDR simplifies subnet masks using a slash and number:

- `192.168.1.0/24`  
This means:
- 24 bits = network
- 8 bits = host
- Subnet mask: `255.255.255.0`

---

## Subnet Mask and CIDR Table

| CIDR | Subnet Mask       | Hosts | Network Blocks              |
|------|-------------------|-------|-----------------------------|
| /8   | 255.0.0.0         | ~16 million | 1.0.0.0, 2.0.0.0, etc. |
| /16  | 255.255.0.0       | ~65,000     | 192.168.0.0, 10.0.0.0     |
| /24  | 255.255.255.0     | 254         | 192.168.1.0, 192.168.2.0  |
| /25  | 255.255.255.128   | 126         | 192.168.1.0, 192.168.1.128|
| /30  | 255.255.255.252   | 2           | Point-to-point links      |

> Usable hosts = 2ⁿ - 2 (subtract network & broadcast)

---

## Binary Breakdown Example

- IP: `192.168.1.0`
- Subnet Mask: `255.255.255.0`
- Binary: `11111111.11111111.11111111.00000000`
- CIDR: `/24`

> The more 1s in the mask, the fewer hosts you can support.

---

## When to Use Which?

| CIDR  | Use Case                            |
|-------|-------------------------------------|
| /24   | Standard office subnet              |
| /30   | Router-to-router WAN link           |
| /16   | Large networks, large DHCP pools    |
| /28   | Isolated subnet for small devices   |

---

## Technician Tip

> CIDR gives you flexibility — you're not stuck with traditional A/B/C classes. That’s why it’s called *classless* routing.

---

## Related Topics

- [Subnetting 101](./Subnetting_101.md)
- [VLSM and Summarization](./VLSM_and_Summarization.md)
- [Routing and Switching](../04-Routing_and_Switching/Routing_Protocols.md)

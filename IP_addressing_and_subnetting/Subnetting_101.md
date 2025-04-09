# Subnetting 101

Subnetting is the process of dividing a larger network into smaller, more manageable segments (subnets). It improves performance, organization, and security by controlling how traffic flows across a network.

---

## Why It Matters in Real Life

You’ll use subnetting when:
- Splitting departments (like HR, Admin, IT) into separate networks
- Limiting broadcast traffic on a LAN
- Assigning IPs based on site or role (e.g., security cameras vs staff PCs)
- Working with VLANs and routing

---

## Key Terms

| Term           | Meaning                                                           |
|----------------|-------------------------------------------------------------------|
| Network ID     | Identifies the subnet                                            |
| Host ID        | Identifies devices within the subnet                             |
| Subnet Mask    | Defines which part of the IP is the network and which is the host|
| CIDR Notation  | Compact format to express subnet mask (e.g., /24)                |

---

## Subnet Mask Basics

| CIDR  | Subnet Mask       | # of Hosts | Notes                     |
|-------|-------------------|------------|----------------------------|
| /8    | 255.0.0.0         | ~16 million| Class A, large networks    |
| /16   | 255.255.0.0       | ~65,000    | Class B, medium networks   |
| /24   | 255.255.255.0     | 254        | Class C, typical LAN       |
| /30   | 255.255.255.252   | 2          | Point-to-point links       |

> Usable hosts = 2ⁿ - 2 (subtracting network and broadcast addresses)

---

## Example

If you have the IP address `192.168.1.0/24`, then:
- **Network ID:** 192.168.1.0  
- **Usable Host Range:** 192.168.1.1 – 192.168.1.254  
- **Broadcast Address:** 192.168.1.255  
- **Total Hosts:** 256 (254 usable)

---

## Real-World Use Cases

- Give printers a dedicated subnet like `192.168.10.0/24`
- Isolate security cameras on `10.0.50.0/24`
- Use `/30` for a link between two routers

---

## Subnetting Shortcut Table

| CIDR | Hosts | Subnet Mask       |
|------|-------|-------------------|
| /24  | 254   | 255.255.255.0     |
| /25  | 126   | 255.255.255.128   |
| /26  | 62    | 255.255.255.192   |
| /27  | 30    | 255.255.255.224   |
| /28  | 14    | 255.255.255.240   |
| /29  | 6     | 255.255.255.248   |
| /30  | 2     | 255.255.255.252   |

---

## Technician Tip

> Subnetting is just binary math. If you're preparing for certs or job interviews, memorize the CIDR table above — it's used constantly.

---

## Related Topics

- [Subnet Masks and CIDR](./Subnet_Masks_and_CIDR.md)
- [VLSM and Summarization](./VLSM_and_Summarization.md)
- [Routing Protocols](../04-Routing_and_Switching/Routing_Protocols.md)

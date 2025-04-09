# VLSM and Summarization

VLSM (Variable Length Subnet Masking) and route summarization are advanced subnetting techniques used to optimize IP space and routing efficiency.

---

## Why It Matters in Real Life

You’ll use VLSM and summarization when:
- Designing efficient IP addressing plans for multiple departments or buildings
- Avoiding wasted IPs in small subnets
- Reducing the size of routing tables across sites or routers

---

## What is VLSM?

**VLSM** allows you to use different subnet masks within the same network. Instead of using one fixed subnet size, you can create subnets that match the actual number of hosts needed.

### Example:

- You have `192.168.1.0/24` available.
- You need:
  - A subnet for 100 hosts → `/25` (126 usable)
  - A subnet for 30 hosts → `/27` (30 usable)
  - A subnet for 10 hosts → `/28` (14 usable)

With VLSM, you can assign each group only what they need — no wasted space.

---

## What is Route Summarization?

**Route summarization** combines multiple subnets into a single route to reduce routing table entries. It’s used primarily on routers to keep routing tables smaller and easier to manage.

### Example:

These routes:
- 192.168.10.0/24
- 192.168.11.0/24
- 192.168.12.0/24
- 192.168.13.0/24

Can be summarized as:
- `192.168.10.0/22`

This reduces four routes to one — faster lookups, fewer resources.

---

## Benefits of VLSM and Summarization

| Feature        | Benefit                                 |
|----------------|------------------------------------------|
| VLSM           | Efficient use of IP address space        |
| Summarization  | Smaller, faster routing tables           |
| Both           | Easier network management and scaling    |

---

## Technician Tip

> VLSM gives flexibility. Summarization gives simplicity. Use VLSM when designing networks and summarization when configuring routers.

---

## Real-World Use Case

In an enterprise:
- Use VLSM to assign only 10 IPs to the camera VLAN
- Use summarization at the edge router to advertise `10.0.0.0/16` instead of 50 smaller subnets

---

## Related Topics

- [Subnetting 101](./Subnetting_101.md)
- [Subnet Masks and CIDR](./Subnet_Masks_and_CIDR.md)
- [Routing Protocols](../04-Routing_and_Switching/Routing_Protocols.md)

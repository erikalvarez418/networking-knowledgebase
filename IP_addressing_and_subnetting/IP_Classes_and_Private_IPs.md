# IP Classes and Private IPs

IP addresses are divided into **classes** based on their range, and some of these are reserved as **private IPs** for use inside local networks.

Understanding IP classes helps when configuring static IPs, designing subnets, or troubleshooting network communication.

---

## Why It Matters in Real Life

You’ll often assign or recognize IPs in the following ways:
- 192.168.x.x → home or office networks
- 10.x.x.x → enterprise environments
- 172.16.x.x to 172.31.x.x → sometimes used by ISPs or schools

If you assign a **public IP** inside a LAN by mistake, it could cause serious routing issues.

---

## IP Address Classes (IPv4)

| Class | Range                | Default Subnet Mask | Used For              |
|-------|----------------------|----------------------|------------------------|
| A     | 1.0.0.0 – 126.255.255.255 | 255.0.0.0         | Very large networks    |
| B     | 128.0.0.0 – 191.255.255.255 | 255.255.0.0     | Medium networks        |
| C     | 192.0.0.0 – 223.255.255.255 | 255.255.255.0   | Small networks         |
| D     | 224.0.0.0 – 239.255.255.255 | N/A              | Multicast              |
| E     | 240.0.0.0 – 255.255.255.255 | N/A              | Research/reserved      |

> Note: Classful networking is mostly outdated but still useful for understanding address planning.

---

## Private IP Address Ranges

These IPs are not routable on the public internet — they are meant for internal network use.

| Class | Range                         | CIDR          |
|-------|-------------------------------|---------------|
| A     | 10.0.0.0 – 10.255.255.255     | 10.0.0.0/8    |
| B     | 172.16.0.0 – 172.31.255.255   | 172.16.0.0/12 |
| C     | 192.168.0.0 – 192.168.255.255 | 192.168.0.0/16|

---

## Public vs Private IPs

| Type    | Used In             | Can Access Internet? | NAT Required? |
|---------|---------------------|-----------------------|---------------|
| Private | Home/office networks| No (needs NAT)        | Yes           |
| Public  | ISP, cloud, servers | Yes                   | No            |

---

## Technician Tip

> If you're troubleshooting why a device can't reach the internet, double-check whether it has a private IP **and** if NAT is configured on the router.

---

## Real-World Examples

- **192.168.1.1** → Default gateway in most home routers
- **10.1.0.5** → Static IP for a server in a corporate environment
- **8.8.8.8** → Public DNS server (Google)

---

## Related Topics

- [Subnetting 101](./Subnetting_101.md)
- [NAT and PAT](../06-Network_Services/NAT_and_PAT.md)
- [DHCP](../06-Network_Services/DHCP.md)

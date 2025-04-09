# Firewalls and UTMs

Firewalls and Unified Threat Management (UTM) devices are key components in securing a network. They filter traffic based on rules and offer protection against external and internal threats.

---

## Why It Matters in Real Life

Firewalls control what enters and leaves your network. Whether you're:
- Allowing VPN access
- Blocking malicious IPs
- Isolating traffic between VLANs
...firewalls and UTMs are essential.

---

## What is a Firewall?

A **firewall** monitors and filters incoming and outgoing traffic based on predefined rules.

### Types of Firewalls:
| Type               | Description                                      | Example Use Case                      |
|--------------------|--------------------------------------------------|----------------------------------------|
| Packet Filtering   | Inspects packets based on IP, port, protocol     | Block all incoming traffic on port 23 |
| Stateful Inspection| Tracks active connections                        | Allow traffic only if part of session |
| Next-Gen (NGFW)    | Includes deep packet inspection, app control     | Block social media or P2P apps        |

---

## What is a UTM?

A **Unified Threat Management** (UTM) device is a multi-function firewall that combines several security features into one appliance.

### Typical UTM Features:
- Firewall + Intrusion Prevention (IPS)
- Antivirus scanning
- Web content filtering
- VPN support
- Application control

---

## Real-World Use Cases

| Scenario                                      | Device Needed |
|-----------------------------------------------|---------------|
| Block students from accessing gaming websites | UTM           |
| Allow internal traffic but block external SSH | Firewall      |
| Site-to-site VPN between campuses             | UTM or NGFW   |
| Log and monitor threat activity               | UTM           |

---

## Technician Tip

> When troubleshooting blocked traffic, always check firewall logs first. Look for denied connections by IP and port — it often tells you exactly what's happening.

---

## Where Firewalls Live

- **Edge Firewall**: Sits between the internal network and ISP
- **Internal Firewall**: Used between VLANs or sensitive systems
- **Host-Based Firewall**: Installed on endpoints (Windows Defender Firewall)

---

## Common Brands

- **UTM Vendors**: Sophos, Fortinet, SonicWall
- **NGFW Vendors**: Palo Alto, Cisco Firepower
- **Cloud Firewalls**: Azure NSG, AWS Security Groups

---

## Related Topics

- [NAT and PAT](../06-Network_Services/NAT_and_PAT.md)
- [IDS vs IPS](../09-Network_Security/IDS_vs_IPS.md)
- [Port Security and MAC Filtering](../09-Network_Security/Port_Security_and_MAC_Filtering.md)

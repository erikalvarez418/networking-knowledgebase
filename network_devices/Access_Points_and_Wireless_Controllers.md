# Access Points and Wireless Controllers

Access Points (APs) provide wireless access to a wired network. Wireless Controllers centrally manage multiple APs, especially in larger environments like schools, offices, and campuses.

---

## Why It Matters in Real Life

If you're troubleshooting wireless connectivity, signal issues, or roaming problems, you'll deal directly with:
- Individual Access Points (APs)
- Wireless LAN Controllers (WLCs)
- Management platforms like UniFi or Cisco Mobility Express

---

## What is an Access Point (AP)?

An Access Point connects wireless devices (phones, laptops, etc.) to the wired LAN.

### Key Functions:
- Broadcasts SSIDs
- Handles client connections via Wi-Fi
- Forwards data to the switch or router
- Can operate standalone or under a controller

---

## What is a Wireless Controller?

A wireless controller (or cloud-based manager) controls and monitors multiple APs from one interface.

### Key Functions:
- Centralized SSID and security settings
- Roaming and load balancing
- Automatic firmware updates
- Guest network and captive portal management

---

## Real-World Setup Example

- Small office: One standalone AP connected to a PoE switch
- School campus: 30+ APs managed by a UniFi Controller or Cisco WLC

---

## Access Point Modes

| Mode               | Description                                          |
|--------------------|------------------------------------------------------|
| Standalone         | Configured individually, no controller needed        |
| Controller-Based   | Managed centrally via hardware or software controller|
| Mesh               | Connects wirelessly to other APs to extend coverage  |
| Repeater/Extender  | Rebroadcasts another AP’s signal (not recommended)   |

---

## Troubleshooting Tips

| Symptom                        | Possible Cause                            |
|--------------------------------|--------------------------------------------|
| Slow wireless speeds           | AP overload, interference, channel conflict|
| Devices can't connect          | SSID broadcast disabled, security mismatch |
| Roaming issues between APs     | No controller, inconsistent settings       |
| AP not showing in controller   | Not adopted, wrong VLAN, firmware mismatch |

---

## Technician Tip

> Most enterprise Wi-Fi issues stem from poor channel planning, overloaded APs, or misconfigured controllers. Use controller logs and heatmaps to troubleshoot effectively.

---

## Related Topics

- [WiFi Standards and Frequencies](../05-Wireless_Networking/WiFi_Standards_and_Frequencies.md)
- [SSID and Channel Selection](../05-Wireless_Networking/SSID_Channel_Selection.md)
- [Wireless Security](../05-Wireless_Networking/Wireless_Security.md)

# Day 03 – Subnetting and CIDR

## 1. Introduction to Subnetting

Subnetting is the process of dividing a large network into smaller networks called subnets.

It helps network administrators manage IP addresses efficiently and organize devices into smaller network segments.

### Purpose of Subnetting

- Efficient utilization of IP addresses.
- Reduces unnecessary network traffic.
- Improves network performance.
- Provides better network security.
- Makes network management easier.
- Separates devices into different network segments.

### Example

A company has 100 computers. Instead of placing every computer in one large network, the administrator can divide them into smaller subnets for different departments.

---

## 2. Subnet Mask

A subnet mask is a 32-bit number used in IPv4 networking to distinguish the network portion from the host portion of an IP address.

It helps identify which part of an IP address represents the network and which part represents an individual device.

### Example

IP Address: `192.168.1.10`

Subnet Mask: `255.255.255.0`

In this example:
- Network portion: `192.168.1`
- Host portion: `10`

### Common Subnet Masks

| CIDR | Subnet Mask |
|---|---|
| /8 | 255.0.0.0 |
| /16 | 255.255.0.0 |
| /24 | 255.255.255.0 |
| /25 | 255.255.255.128 |
| /26 | 255.255.255.192 |
| /27 | 255.255.255.224 |
| /28 | 255.255.255.240 |

---

## 3. CIDR (Classless Inter-Domain Routing)

CIDR is a method of representing IP addresses using a slash followed by a number.

The number after the slash indicates how many bits are used for the network portion of an IP address.

### Example

`192.168.1.0/24`

Here:
- 192.168.1.0 is the network address.
- /24 means 24 bits are used for the network portion.
- The remaining 8 bits are used for hosts.

IPv4 addresses contain 32 bits.

Host bits = 32 - Prefix length

For /24:

32 - 24 = 8 host bits.

---

## 4. Network Address

A network address identifies a particular network.

It is the first address in a subnet and cannot normally be assigned to an individual host.

### Example

IP Network: `192.168.1.0/24`

Network Address: `192.168.1.0`

---

## 5. Broadcast Address

A broadcast address is used to send data to all devices within a particular IPv4 subnet.

It is the last address in a traditional IPv4 subnet and cannot normally be assigned to an individual host.

### Example

Network: `192.168.1.0/24`

Broadcast Address: `192.168.1.255`

---

## 6. Host Calculation

Host calculation helps determine how many devices can be assigned IP addresses within a subnet.

### Formula

Total addresses:

2^h

Usable host addresses (traditional IPv4 subnet):

2^h - 2

Where h represents the number of host bits.

We subtract two addresses because:
- One address is reserved for the network.
- One address is reserved for the broadcast.

### Example: /24

Number of host bits:

32 - 24 = 8

Total addresses:

2^8 = 256

Usable host addresses:

256 - 2 = 254

Therefore, a /24 network supports 254 usable host addresses.

---

## 7. Example of /24 Subnet

Network: `192.168.1.0/24`

- Subnet Mask: 255.255.255.0
- Network Address: 192.168.1.0
- First Usable IP: 192.168.1.1
- Last Usable IP: 192.168.1.254
- Broadcast Address: 192.168.1.255
- Total Addresses: 256
- Usable Hosts: 254

---

## 8. Example of /26 Subnet

Network: `192.168.1.0/26`

- Subnet Mask: 255.255.255.192
- Network Address: 192.168.1.0
- First Usable IP: 192.168.1.1
- Last Usable IP: 192.168.1.62
- Broadcast Address: 192.168.1.63
- Total Addresses: 64
- Usable Hosts: 62

The /26 network has fewer host addresses than the /24 network because more bits are allocated to the network portion.

---

## 9. Comparison Between /24 and /26

| Feature | /24 | /26 |
|---|---|---|
| Subnet Mask | 255.255.255.0 | 255.255.255.192 |
| Network Bits | 24 | 26 |
| Host Bits | 8 | 6 |
| Total Addresses | 256 | 64 |
| Usable Hosts | 254 | 62 |
| Network Size | Larger | Smaller |

A /24 network can be divided into four /26 subnets.

Example:

1. 192.168.1.0/26
2. 192.168.1.64/26
3. 192.168.1.128/26
4. 192.168.1.192/26

Each subnet contains 64 total addresses and 62 usable host addresses.

---

## 10. Practical Learning Using Kali Linux

During the practical session, I explored basic network information using Kali Linux.

### Commands Used

**1. Display IP address information**

```bash
ip addr
```

This command displays network interfaces and their assigned IP addresses.

**2. Display routing information**

```bash
ip route
```

This command displays the routing table and default gateway information.

**3. Display network interface information**

```bash
ip link
```

This command displays available network interfaces and their status.

**4. Check connectivity**

```bash
ping -c 4 127.0.0.1
```

This command checks local loopback connectivity.

### Non-sensitive Practical Observations

- Identified the available network interfaces.
- Observed IPv4 address information.
- Explored network interface status.
- Viewed routing information and the default gateway.
- Learned how command-line tools help troubleshoot basic networking problems.

Note: These are learning observations. Record your actual interface names and results separately if you want to document your own practical output. Do not publish public IP addresses, MAC addresses, passwords, or other private network details.

---

## 11. Key Learnings

After completing Day 03, I learned:

- What subnetting is and why it is important.
- How subnet masks work.
- How to understand CIDR notation.
- The difference between network and broadcast addresses.
- How to calculate total and usable host addresses.
- The difference between /24 and /26 networks.
- How to inspect network information using Kali Linux.

---

## 12. Conclusion

Subnetting and CIDR are important networking concepts in cybersecurity.

Understanding IP addressing and subnet calculations helps security professionals analyze networks, identify network segments, and understand how devices communicate.

These concepts are useful for network administration, SOC analysis, network troubleshooting, and defensive security.
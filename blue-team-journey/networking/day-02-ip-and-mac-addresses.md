# Day 2: IP and MAC Addresses

## 1. What is an IP Address?

An **IP (Internet Protocol) address** is a unique logical address assigned to a device connected to a network. It is used to identify devices and enable communication between them.

Every device communicating over an IP network uses an IP address.

### Purpose of an IP Address

- Identifies a device on an IP network.
- Helps deliver data to the correct destination.
- Enables communication between different networks.
- Helps routers forward packets.

### Example

`192.168.1.10`

This is an example of an IPv4 address.

---

## 2. IPv4 vs IPv6

IP addresses are mainly divided into two versions: IPv4 and IPv6.

### IPv4

IPv4 stands for Internet Protocol Version 4.

- Uses 32-bit addresses.
- Written in four decimal numbers separated by dots.
- Each number ranges from 0 to 255.
- Supports approximately 4.3 billion unique addresses.

Example:

`192.168.1.10`

### IPv6

IPv6 stands for Internet Protocol Version 6.

- Uses 128-bit addresses.
- Written using hexadecimal numbers.
- Uses colons to separate groups.
- Provides a much larger address space than IPv4.

Example:

`2001:db8:85a3::8a2e:370:7334`

### Differences Between IPv4 and IPv6

| Feature | IPv4 | IPv6 |
|---|---|---|
| Address size | 32 bits | 128 bits |
| Format | Decimal | Hexadecimal |
| Separator | Dot (.) | Colon (:) |
| Address space | Smaller | Extremely large |
| Example | 192.168.1.10 | 2001:db8::1 |

---

## 3. Public vs Private IP Addresses

### Public IP Address

A public IP address is an address used to identify a network or device on the public internet.

- Used for communication over the internet.
- Generally assigned by an Internet Service Provider (ISP).
- Must be globally unique.

### Private IP Address

A private IP address is used inside a local network, such as a home, college, or office network.

- Used for communication within private networks.
- Not directly routable over the public internet.
- The same private address ranges can be reused in different networks.

### Private IPv4 Address Ranges

There are three main private IPv4 ranges defined by RFC 1918.

| Class | Private IP Range |
|---|---|
| Class A | 10.0.0.0 – 10.255.255.255 |
| Class B | 172.16.0.0 – 172.31.255.255 |
| Class C | 192.168.0.0 – 192.168.255.255 |

Example:

`192.168.1.5` – Private IP address.

`8.8.8.8` – Public IP address.

---

## 4. Static vs Dynamic IP Addresses

### Static IP Address

A static IP address is an IP address that remains the same until it is manually changed or reconfigured.

Uses:
- Servers
- Network infrastructure
- Remote access systems
- Devices that need a consistent address

Advantages:
- Easy to locate consistently.
- Useful for hosting services.
- Suitable for network management.

### Dynamic IP Address

A dynamic IP address is automatically assigned to a device, usually through DHCP.

It may change over time.

Uses:
- Home networks
- College Wi-Fi
- Office networks
- Public Wi-Fi

Advantages:
- Automatic configuration.
- Reduces manual administration.
- Allows efficient reuse of IP addresses.

---

## 5. What is a MAC Address?

A **MAC (Media Access Control) address** is a hardware-level address associated with a network interface.

It is primarily used for communication within a local network at the Data Link Layer (Layer 2) of the OSI model.

### Features

- Usually 48 bits (6 bytes) for traditional Ethernet MAC addresses.
- Commonly written in hexadecimal.
- Contains six groups of two hexadecimal digits.
- Associated with a network interface.

Example:

`00:1A:2B:3C:4D:5E`

### Purpose of a MAC Address

- Identifies a network interface on a local network.
- Helps switches forward Ethernet frames.
- Supports local network communication.

Note: MAC addresses can be changed or spoofed in software, and devices may use randomized MAC addresses for privacy.

---

## 6. Difference Between IP Address and MAC Address

| IP Address | MAC Address |
|---|---|
| Logical address | Link-layer address |
| Used for network communication | Used for local link communication |
| Operates at Network Layer (Layer 3) | Operates at Data Link Layer (Layer 2) |
| Can be assigned dynamically or statically | Associated with a network interface |
| IPv4 and IPv6 formats | Usually 48-bit Ethernet address |
| Used by routers | Used by switches |

### Example

When a computer accesses a website:

1. It uses the destination IP address to identify the remote destination.
2. It uses a MAC address to deliver the Ethernet frame to the next hop on the local network.
3. Routers forward packets between networks.

---

## 7. DHCP and DORA Process

### What is DHCP?

DHCP stands for Dynamic Host Configuration Protocol.

It automatically provides network configuration to devices.

DHCP can assign:
- IP address
- Subnet mask
- Default gateway
- DNS server addresses

### DORA Process

DORA represents the four steps used in the DHCP address allocation process.

**1. Discover**

The client broadcasts a DHCP Discover message to find available DHCP servers.

**2. Offer**

The DHCP server responds with a DHCP Offer containing an available IP address and configuration information.

**3. Request**

The client sends a DHCP Request to indicate that it wants to use the offered address.

**4. Acknowledge**

The DHCP server sends a DHCP Acknowledgement (ACK) confirming the allocation.

### DORA Diagram

```text
Client                  DHCP Server
  |                          |
  |---- DHCP Discover ------>|
  |                          |
  |<----- DHCP Offer --------|
  |                          |
  |----- DHCP Request ------>|
  |                          |
  |<------ DHCP ACK ---------|
  |                          |
  IP address assigned
```

DHCP normally uses UDP port 67 on the server and UDP port 68 on the client.

---

## 8. What is NAT?

NAT stands for Network Address Translation.

It is a technique used by routers to translate IP addresses between different networks.

NAT commonly allows multiple devices using private IP addresses to access the internet through a public IP address.

### Example

Consider a home network:

| Device | Private IP |
|---|---|
| Laptop | 192.168.1.10 |
| Mobile | 192.168.1.11 |
| Desktop | 192.168.1.12 |

The router can translate their outgoing connections to use the network's public IP address.

### Types of NAT

1. Static NAT – Maps one private IP address to one public IP address.
2. Dynamic NAT – Maps private addresses to available public addresses from a pool.
3. PAT (Port Address Translation) – Allows multiple devices to share a public IP address using different port numbers.

### Importance of NAT

- Conserves public IPv4 addresses.
- Allows private networks to access the internet.
- Hides internal addressing from external networks.

Note: NAT is not a replacement for a firewall or a complete security solution.

---

## 9. Commands Practised

The following commands can be used to inspect network configuration.

### Windows Commands

**1. ipconfig**

Displays basic IP configuration.

```cmd
ipconfig
```

**2. ipconfig /all**

Displays detailed network configuration, including physical address, DHCP status, and DNS information.

```cmd
ipconfig /all
```

**3. getmac**

Displays MAC addresses of network interfaces.

```cmd
getmac
```

**4. arp -a**

Displays the ARP cache, which contains IP-to-MAC address mappings.

```cmd
arp -a
```

**5. ping**

Tests connectivity to another IP address or hostname.

```cmd
ping 8.8.8.8
```

**6. tracert**

Displays the route packets take towards a destination.

```cmd
tracert google.com
```

### Linux Commands

**1. ip addr**

Displays IP addresses assigned to network interfaces.

```bash
ip addr
```

**2. ip link**

Displays network interfaces and their link-layer information.

```bash
ip link
```

**3. ip route**

Displays the routing table.

```bash
ip route
```

**4. ip neigh**

Displays the neighbour table containing IP and link-layer address information.

```bash
ip neigh
```

**5. ping**

Tests network connectivity.

```bash
ping -c 4 8.8.8.8
```

### My Observations

Record your actual observations after running the commands.

- `ipconfig` displays the IPv4 configuration of my Windows system.
- `ipconfig /all` provides additional network details.
- `getmac` displays the MAC addresses of network interfaces.
- `arp -a` displays cached IP-to-MAC mappings.
- `ip addr` displays network interface information in Linux.
- `ip route` displays the routing table.

Do not publish your actual public IP address, MAC address, Wi-Fi details, or other sensitive network information on GitHub.

---

## 10. Practical Exercises

1. Open Command Prompt and execute `ipconfig`.
2. Identify the IPv4 address of your active network interface.
3. Execute `ipconfig /all` and locate the Physical Address field.
4. Execute `arp -a` and examine the available entries.
5. Open Kali Linux and execute `ip addr`.
6. Compare the IP and MAC address information in Windows and Kali.
7. Execute `ip route` in Kali and identify the default route.

### Questions for Self-Assessment

1. What is an IP address?
2. What is the main difference between IPv4 and IPv6?
3. What are private IP address ranges?
4. Differentiate static and dynamic IP addresses.
5. What is a MAC address?
6. Differentiate IP and MAC addresses.
7. Explain the four stages of DORA.
8. What is DHCP?
9. What is NAT?
10. Why is NAT important in home networks?

---

## Day 2 Summary

Today I learned:

- IP address fundamentals.
- IPv4 and IPv6.
- Public and private IP addresses.
- Static and dynamic IP addresses.
- MAC address fundamentals.
- IP address vs MAC address.
- DHCP and DORA.
- Network Address Translation (NAT).
- Basic Windows and Linux networking commands.

**Learning Goal:** Understand how devices are identified and communicate within local networks and across the internet.

**Next:** Day 3 – DNS, DHCP, ARP and Network Communication.

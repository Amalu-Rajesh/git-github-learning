# Day 01 – Networking Basics

**Learning Path:** Blue Team Cybersecurity  
**Subject:** Computer Networking  
**Day:** 01  
**Level:** Beginner

# 1. Learning Objectives

By the end of this session, I aim to understand:

- What a computer network is.
- Why computer networks are important.
- Different types of networks.
- Network architectures.
- Basic networking devices.
- Different network topologies.
- Basic Linux networking commands.
- The importance of networking in cybersecurity.

# 2. What is a Computer Network?

A computer network is a collection of two or more
computing devices connected together to communicate
and share information and resources.

Devices communicate through wired or wireless
connections using networking protocols.

   ### Example

Consider a college computer laboratory.

There are 20 computers connected to a network.
Students can access shared files, use a common
printer and connect to the internet.

All these computers form a computer network.

### Why is networking important in cybersecurity?

Cybersecurity professionals need to understand
how devices communicate.

Network knowledge helps security analysts:

- Identify suspicious network traffic.
- Detect unauthorized devices.
- Monitor communication between systems.
- Investigate network attacks.
- Identify suspicious connections.


# 3. Why Are Networks Used?

Computer networks are used for several purposes.
         Communication
         Resource Sharing
         Data Sharing
         Centralized Management
         Remote Access

# 4. Types of Computer Networks

Networks are classified according to their
geographical coverage and purpose.

## 4.1 PAN – Personal Area Network

PAN stands for Personal Area Network.

It is a small network that connects personal
devices within a short distance around an individual.

Examples:
- Bluetooth headphones connected to a smartphone.
- Smartwatch connected to a mobile phone.
- Phone sharing its internet connection.

## 4.2 LAN – Local Area Network

LAN stands for Local Area Network.

It connects devices within a limited geographical
area, such as a home, office, school or laboratory.

Characteristics:
- Covers a small geographical area.
- Usually provides high-speed communication.
- Can use wired Ethernet or wireless connections.
- Often managed by one organization or individual.

Example: Computers connected in a college laboratory.

## 4.3 MAN – Metropolitan Area Network

MAN stands for Metropolitan Area Network.

It connects multiple networks across a city
or a large metropolitan area.

Example: A network connecting different
branches of an organization within a city.

## 4.4 WAN – Wide Area Network

WAN stands for Wide Area Network.

It connects networks across large geographical
areas, such as countries and continents.

Characteristics:
- Covers large geographical areas.
- Connects multiple LANs and MANs.
- Uses telecommunications infrastructure.

Example: The Internet.

## 4.5 WLAN – Wireless Local Area Network

WLAN stands for Wireless Local Area Network.

It is a local network that connects devices
wirelessly using technologies such as Wi-Fi.

Example: A laptop and smartphone connected
to the same Wi-Fi router.

### Comparison of Network Types

| Type | Full Form | Coverage | Example |
| PAN | Personal Area Network | Personal space | Bluetooth |
| LAN | Local Area Network | Building | College lab |
| MAN | Metropolitan Area Network | City | City network |
| WAN | Wide Area Network | Countries/continents | Internet |
| WLAN | Wireless LAN | Local wireless area | Wi-Fi |

# 5. Network Architectures

Network architecture describes how devices
communicate and share resources within a network.

Two common architectures are Client-Server
and Peer-to-Peer.

## 5.1 Client-Server Architecture

Client-server is a network architecture in which
a central computer called a server provides
services or resources to other computers called clients.

The client sends a request, and the server
processes the request and returns a response.

Example:

When a user opens a website:

1. The browser acts as a client.
2. It sends a request to a web server.
3. The server processes the request.
4. The server sends the webpage.
5. The browser displays the webpage.

Advantages:
- Centralized management.
- Easier data backup.
- Better access control.
- Centralized security policies.

Disadvantages:
- Server failure can affect many clients.
- Requires server maintenance.
- Can be expensive to establish.

## 5.2 Peer-to-Peer Architecture

Peer-to-Peer (P2P) is a network architecture
in which devices communicate and share resources
directly with one another.

Each device can act as both a client and a server.

Example: Two computers directly sharing files.

Advantages:
- Easy to establish.
- Lower setup cost.
- No dedicated central server required.

Disadvantages:
- Difficult to manage centrally.
- Security management can be challenging.
- Backup and access control may be less organized.

### Difference Between Client-Server and P2P

| Client-Server | Peer-to-Peer |
| Uses a central server | No dedicated central server required |
| Centralized management | Distributed management |
| Easier centralized security | Security is managed across peers |
| Suitable for organizations | Suitable for small-scale sharing |

# 6. Basic Network Devices

Networking devices help computers communicate
and transfer data between networks.

## 6.1 Router

A router connects different networks and forwards
data packets between them using IP addresses.

Example: A home Wi-Fi router connects a home
network to the internet.

Main function:
- Connects different networks.
- Forwards packets.
- Maintains routing information.
- Can provide NAT and other network services.

Cybersecurity relevance:

Routers can be configured with firewall rules,
access controls and network security settings.

## 6.2 Switch

A switch connects multiple devices within a LAN.

It primarily uses MAC addresses to forward
Ethernet frames to the correct destination port.

Example: Connecting computers in an office.

Cybersecurity relevance:

Managed switches can support VLANs, port security
and network traffic monitoring.

## 6.3 Modem

A modem is a device that modulates and demodulates
signals to enable communication over a particular
transmission medium.

It connects a network to an internet service
provider through the provider's access technology.

Example: A cable modem used for internet access.

## 6.4 Access Point

An Access Point (AP) allows wireless devices
to connect to a wired network using Wi-Fi.

Example: A wireless access point in a college.

Cybersecurity relevance:

Weak Wi-Fi passwords and insecure wireless
configurations can expose networks to attacks.

## 6.5 Server

A server is a computer or software system that
provides services, resources or data to clients.

Examples:
- Web server
- File server
- Database server
- Mail server

Cybersecurity relevance:

Servers are important security targets because
they store data and provide essential services.

## 6.6 Client

A client is a device or software application
that requests services or resources from a server.

Examples:
- Web browser
- Email application
- Mobile application

# 7. Network Topologies

Network topology describes the physical or
logical arrangement of devices and connections
within a network.

## 7.1 Star Topology

In star topology, all devices connect to a
central networking device, usually a switch.

Advantages:
- Easy to install and manage.
- Failure of one device usually does not
  affect other devices.
- Easy to identify connection problems.

Disadvantages:
- Failure of the central device affects
  the connected network.
- Requires more cabling than some topologies.

## 7.2 Bus Topology

In bus topology, all devices connect to a
single main communication cable called the backbone.

Advantages:
- Simple design.
- Requires less cable in small installations.

Disadvantages:
- Backbone failure can affect the entire network.
- Performance can decrease with increased traffic.
- Troubleshooting can be difficult.

## 7.3 Ring Topology

In ring topology, devices are connected in
a circular arrangement.

Each device connects to its neighboring devices.

Advantages:
- Organized data transmission.
- Can provide predictable access in certain
  ring protocols.

Disadvantages:
- A single link or device failure can disrupt
  a basic single-ring network.
- Adding or removing devices can be difficult.

## 7.4 Mesh Topology

In mesh topology, devices are interconnected
through multiple communication links.

Advantages:
- High reliability.
- Multiple communication paths.
- Better fault tolerance.

Disadvantages:
- Expensive to implement.
- Requires more connections.
- Complex configuration.

# 8. Practical Work – Kali Linux

In this practical session, I will explore
basic networking commands in Kali Linux.

## Practical 1: Display Network Interfaces

Command:
```bash
ip addr
```

Purpose:

Displays information about network interfaces,
including IP addresses and interface details.

What to observe:

- Interface names.
- IPv4 addresses.
- IPv6 addresses, if present.
- MAC addresses.
- Interface state.

## Practical 2: Display Routing Information

Command:

```bash
ip route
```

Purpose:

Displays the IP routing table of the system.

What to observe:

- Default route.
- Gateway address.
- Destination networks.
- Network interface used for routing.

## Practical 3: Display Network Interfaces and Status

Command:

```bash
ip link
```

Purpose:

Displays network interface information
at the link layer.

What to observe:

- Interface names.
- MAC addresses.
- Interface status.
- MTU values.

## Practical 4: Test Network Connectivity

Command:

```bash
ping -c 4 1.1.1.1
```

Purpose:

Tests whether the system can communicate
with the specified IP address using ICMP.

What to observe:

- Successful replies.
- Packet loss.
- Response time.

Note: A failed ping does not always mean
the destination is offline. ICMP may be blocked.

## Practical 5: View Active Listening Ports

Command:

```bash
ss -tuln
```

Purpose:

Displays listening TCP and UDP sockets
without resolving service names.

What to observe:

- Local addresses.
- Listening ports.
- TCP and UDP protocols.

---

# 9. Practical Observations

I will record my actual observations below
after executing the commands in Kali Linux.

| Command | Observation |
| ip addr | To be updated |
| ip route | To be updated |
| ip link | To be updated |
| ping -c 4 1.1.1.1 | To be updated |
| ss -tuln | To be updated |


# 10. Networking and Blue Team Cybersecurity

Networking knowledge is essential for defensive
security and SOC operations.

A Blue Team analyst uses networking concepts
to understand and investigate suspicious activity.

Important applications:

1. Network Monitoring:
   Observing network traffic and identifying
   unusual communication patterns.

2. Intrusion Detection:
   Identifying suspicious activity using
   network intrusion detection systems.

3. Threat Detection:
   Recognizing suspicious IP addresses,
   unexpected ports and unusual connections.

4. Incident Investigation:
   Analysing network logs and communication
   patterns during security incidents.

5. Firewall Management:
   Understanding network traffic rules and
   controlling allowed and blocked connections.

Tools used in network security include:

- Wireshark
- tcpdump
- Snort
- Suricata
- Zeek


# 11. Important Terms to Remember

| Term | Meaning |
| Network | Connected devices communicating |
| IP Address | Logical network-layer address |
| MAC Address | Link-layer hardware address |
| Router | Connects different networks |
| Switch | Connects devices in a LAN |
| Server | Provides services |
| Client | Requests services |
| Packet | Network-layer data unit |
| Protocol | Rules for communication |
| Topology | Arrangement of network devices |
| Gateway | Device or system providing a path to another network |
| Bandwidth | Maximum data transfer capacity |

# 12. Revision Questions

## Short Answer Questions

1. What is a computer network?
2. Define LAN.
3. What is PAN?
4. Expand WAN and MAN.
5. What is a router?
6. What is a network switch?
7. Define client-server architecture.
8. What is peer-to-peer architecture?
9. What is network topology?
10. What is an access point?

## Descriptive Questions

1. Explain the different types of computer networks.
2. Explain client-server and peer-to-peer architectures.
3. Describe the functions of basic networking devices.
4. Explain different network topologies with advantages
   and disadvantages.
5. Explain the importance of networking in cybersecurity.

## Practical Questions

1. Which command displays IP addresses?
2. Which command displays the routing table?
3. Which command displays network interface information?
4. Which command tests connectivity using ICMP?
5. Which command displays listening TCP and UDP sockets?

# 13. What I Learned Today

After completing Day 1, I learned:

- The basic concept of computer networking.
- The importance and applications of networks.
- Different network types and architectures.
- Functions of routers, switches and other devices.
- Different network topologies.
- Basic Linux networking commands.
- How networking knowledge supports Blue Team security.

# 14. Questions to Revisit

- How does an IP address work?
- What is the difference between an IP address
  and a MAC address?
- How does a router forward packets?
- What happens when I access a website?
- How can network traffic reveal suspicious activity?

# Conclusion

Day 1 helped me establish a foundation in
computer networking.

I explored different network types, architectures,
network devices and topologies.

I also started practising basic networking
commands using Kali Linux.

My next step is to understand IP addresses
and MAC addresses in detail.

**Next: Day 02 – IP Address and MAC Address**

# secure-enterprise-network-packet-tracer

Cisco Packet Tracer-based enterprise networking project demonstrating **IP addressing, subnetting, routing protocols, network services, network protocols, and basic security controls** across multiple departments.

## Features

* Multi-Department LAN/WAN Network
* IPv4 Addressing and Subnetting
* Static Routing
* RIP v2 Routing
* OSPF Routing
* DHCP Configuration
* DNS Configuration
* HTTP/HTTPS Web Services
* FTP Service
* ARP Analysis
* TCP/UDP and Port Analysis
* Router Basic Security
* Access Control Lists (ACL)
* Windows Firewall Concepts
* VPN Concepts
* Network Connectivity Testing

## Technologies

* Cisco Packet Tracer
* IPv4
* TCP/IP
* OSI Model
* Static Routing
* RIP v2
* OSPF
* DHCP
* DNS
* HTTP/HTTPS
* FTP
* ARP
* TCP/UDP
* ACL

## Network Architecture

The project simulates a multi-department enterprise/college network containing:

* IT Department
* Computer Department
* Other/Examination Department
* Principal Room
* Internet Lab
* Server Room
* Multiple Routers and Switches
* DNS, Web and FTP Servers

### IP Addressing

| Network             | Subnet           |
| ------------------- | ---------------- |
| IT Department       | `192.168.1.0/24` |
| Computer Department | `192.168.2.0/24` |
| Other Department    | `192.168.3.0/24` |
| Principal Room      | `192.168.4.0/24` |
| Internet Lab        | `192.168.5.0/24` |
| Server Network      | `1.0.0.0/24`     |
| R0 ↔ R1             | `10.10.0.0/30`   |
| R1 ↔ R2             | `20.20.0.0/30`   |

## Routing

### Static Routing

Static routes are configured to provide manually defined paths between selected networks.

### RIP v2

RIPv2 is configured to demonstrate dynamic distance-vector routing.

```cisco
router rip
 version 2
 no auto-summary
```

### OSPF

OSPF is configured to demonstrate dynamic link-state routing.

```cisco
router ospf 1
 router-id 1.1.1.1
```

### Routing Verification

```cisco
show ip route
show ip protocols
show ip ospf neighbor
```

## Network Services

### DHCP

Provides automatic IP configuration to client devices, including:

* IP Address
* Subnet Mask
* Default Gateway
* DNS Server

### DNS

Provides domain-name resolution between hostnames and IP addresses.

Example:

```text
www.college.local → Web Server IP
```

### HTTP / HTTPS

The Web Server provides:

```text
HTTP  → TCP Port 80
HTTPS → TCP Port 443
```

### FTP

The FTP server provides file-transfer functionality:

```text
FTP → TCP Port 21
```

## Network Protocols

### ARP

ARP is used to resolve an IPv4 address to the corresponding MAC address.

```text
IP Address → ARP → MAC Address
```

### TCP / UDP

The project demonstrates the role of TCP and UDP in network communication and service delivery.

### ICMP

ICMP is used for connectivity testing with commands such as:

```text
ping <destination-ip>
```

## Ports & Services

| Service     | Protocol | Port |
| ----------- | -------- | ---: |
| FTP         | TCP      |   21 |
| SSH         | TCP      |   22 |
| DNS         | UDP/TCP  |   53 |
| DHCP Server | UDP      |   67 |
| DHCP Client | UDP      |   68 |
| HTTP        | TCP      |   80 |
| HTTPS       | TCP      |  443 |
| ICMP        | IP       |  N/A |

## Security

The project includes basic network security concepts such as:

* Router password protection
* Console and VTY authentication
* Password encryption
* Access Control Lists (ACL)
* HTTPS communication
* Windows Firewall concepts
* VPN concepts
* Port and service analysis

Example router security configuration:

```cisco
enable secret class123
service password-encryption
```

## OSI & TCP/IP Model

The project connects practical network communication with the **OSI** and **TCP/IP** models.

### OSI Model

```text
Application     → HTTP, HTTPS, DNS, FTP
Presentation    → Encryption / Data Formatting
Session         → Session Management
Transport       → TCP / UDP
Network         → IP / ICMP / Routing
Data Link       → Ethernet / MAC / ARP
Physical        → Cables / Interfaces
```

### TCP/IP Model

```text
Application     → HTTP, HTTPS, DNS, FTP, DHCP
Transport       → TCP, UDP
Internet        → IP, ICMP
Network Access  → Ethernet, ARP
```

## Testing

The network is tested using:

```cisco
show ip interface brief
show ip route
show ip protocols
show ip ospf neighbor
```

Client-side testing includes:

```text
ping <destination-ip>
arp -a
```

Additional tests include:

* DHCP IP assignment
* DNS name resolution
* HTTP/HTTPS access
* FTP connectivity
* Inter-department communication
* Routing table verification
* OSPF neighbor verification


## Skills Demonstrated

**Networking:**
IP Addressing | Subnetting | LAN | WAN | OSI Model | TCP/IP

**Routing:**
Static Routing | RIP v2 | OSPF

**Network Services:**
DHCP | DNS | HTTP | HTTPS | FTP

**Protocols:**
ARP | TCP | UDP | ICMP

**Security:**
ACL | Router Security | Windows Firewall | VPN | Port & Service Analysis

**Tools:**
Cisco Packet Tracer

## Disclaimer

This project is developed for **educational and authorized networking/security testing purposes**. All testing is performed within a controlled lab environment.

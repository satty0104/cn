
# **1️⃣ Physical Layer (Layer 1 – OSI)**

* **Purpose**: Transmission of raw bits over the physical medium.
* **Protocols/Standards**:

  * **Ethernet (IEEE 802.3)** → defines electrical signals, cables, connectors.
  * **Wi-Fi (IEEE 802.11 Physical layer)** → wireless transmission standards.
  * **DSL, ISDN** → wired digital transmission.
  * **Bluetooth (Physical layer part)** → short-range wireless communication.
* **Devices**: Hub, Repeater.

---

# **2️⃣ Data Link Layer (Layer 2 – OSI)**

* **Purpose**: Error detection, framing, MAC addressing, and reliable link communication.
* **Protocols**:

  * **Ethernet (Data link layer)** → framing, MAC addresses.
  * **PPP (Point-to-Point Protocol)** → framing for point-to-point links.
  * **HDLC** → serial communication framing.
  * **ARP (Address Resolution Protocol)** → maps IP → MAC.
  * **VLAN (IEEE 802.1Q)** → logical segmentation.
* **Devices**: Switch, Bridge, NIC.

---

# **3️⃣ Network Layer (Layer 3 – OSI)**

* **Purpose**: Logical addressing, routing, path selection.
* **Protocols**:

  * **IP (IPv4/IPv6)** → logical addressing.
  * **ICMP (Internet Control Message Protocol)** → error reporting & diagnostics (ping, traceroute).
  * **RIP (Routing Information Protocol)** → distance-vector routing.
  * **OSPF (Open Shortest Path First)** → link-state routing.
  * **BGP (Border Gateway Protocol)** → path-vector, inter-AS routing.
  * **NAT (Network Address Translation)** → IP translation.
  * **IGMP** → multicast group management.
* **Devices**: Router, Layer 3 switch.

---

# **4️⃣ Transport Layer (Layer 4 – OSI)**

* **Purpose**: End-to-end communication, reliability, flow control, multiplexing.
* **Protocols**:

  * **TCP (Transmission Control Protocol)** → reliable, connection-oriented.
  * **UDP (User Datagram Protocol)** → connectionless, faster.
  * **SCTP (Stream Control Transmission Protocol)** → combines features of TCP & UDP.
* **Key Functions**:

  * Port numbers for multiplexing (HTTP → 80, DNS → 53, SMTP → 25).

---

# **5️⃣ Session Layer (Layer 5 – OSI)**

* **Purpose**: Manage sessions between applications, connection establishment/termination.
* **Protocols**:

  * **NetBIOS** → sessions for Windows networking.
  * **RPC (Remote Procedure Call)** → application-level session communication.
  * **PPTP** → VPN session protocol.

---

# **6️⃣ Presentation Layer (Layer 6 – OSI)**

* **Purpose**: Data formatting, encryption/decryption, compression.
* **Protocols/Standards**:

  * **SSL/TLS** → encryption for secure communication.
  * **MIME** → email formatting.
  * **JPEG, GIF, MPEG** → media compression & encoding.

---

# **7️⃣ Application Layer (Layer 7 – OSI)**

* **Purpose**: Provides services directly to end-users and applications.
* **Protocols**:

  * **HTTP/HTTPS** → web browsing.
  * **FTP, SFTP, TFTP** → file transfer.
  * **SMTP, IMAP, POP3** → email.
  * **DNS** → name resolution.
  * **DHCP** → dynamic IP addressing.
  * **SNMP** → network management.

---

# **Mapping OSI → TCP/IP**

| OSI Layer                          | TCP/IP Layer   | Key Protocols                                 |
| ---------------------------------- | -------------- | --------------------------------------------- |
| Application, Presentation, Session | Application    | HTTP, HTTPS, FTP, DNS, SMTP, IMAP, SNMP, DHCP |
| Transport                          | Transport      | TCP, UDP, SCTP                                |
| Network                            | Internet       | IP, ICMP, ARP, RIP, OSPF, BGP, NAT            |
| Data Link + Physical               | Network Access | Ethernet, Wi-Fi, PPP, HDLC, VLAN              |

---

**Tip for Interviews**:

* Remember **layer → function → example protocol → device**.

  * *“Which layer does ARP operate on?” → Layer 2/Network*
  * *“Which protocol ensures reliable delivery?” → TCP*
  * *“Which protocol resolves domain names?” → DNS (Application Layer)*






| **Layer (OSI / TCP-IP)**           | **Purpose**                                    | **Key Protocols / Standards**                                        | **Port / Notes**                                                                              | **Devices**            |
| ---------------------------------- | ---------------------------------------------- | -------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | ---------------------- |
| **Physical (1 / Network Access)**  | Transmit raw bits                              | Ethernet (IEEE 802.3), Wi-Fi (IEEE 802.11 PHY), DSL, ISDN, Bluetooth | N/A                                                                                           | Hub, Repeater          |
| **Data Link (2 / Network Access)** | Framing, MAC addressing, error detection       | Ethernet (802.3), PPP, HDLC, ARP (IP→MAC), VLAN (802.1Q)             | N/A                                                                                           | Switch, Bridge, NIC    |
| **Network (3 / Internet)**         | Logical addressing, routing                    | IP (v4/v6), ICMP, RIP, OSPF, BGP, NAT, IGMP                          | N/A                                                                                           | Router, Layer 3 switch |
| **Transport (4 / Transport)**      | End-to-end delivery, reliability, flow control | TCP (reliable), UDP (unreliable), SCTP                               | TCP: HTTP→80, HTTPS→443, SMTP→25, DNS→53; UDP: DNS→53, DHCP→67/68                             | N/A                    |
| **Session (5 / Application)**      | Session establishment & termination            | RPC, NetBIOS, PPTP                                                   | N/A                                                                                           | N/A                    |
| **Presentation (6 / Application)** | Data formatting, encryption, compression       | SSL/TLS (HTTPS), MIME, JPEG, MPEG                                    | TLS/SSL → 443                                                                                 | N/A                    |
| **Application (7 / Application)**  | User services & applications                   | HTTP/HTTPS, FTP/SFTP/TFTP, SMTP, IMAP, POP3, DNS, DHCP, SNMP         | HTTP→80, HTTPS→443, FTP→21, SMTP→25, IMAP→143/993, POP3→110/995, DNS→53, DHCP→67/68, SNMP→161 | N/A                    |


RIP → Distance-vector routing, max 15 hops, simple.

OSPF → Link-state, uses LSAs, fast convergence.

BGP → Path-vector, inter-AS routing, backbone of the internet.

ICMP → Ping, traceroute, error reporting.

IMAP → Access emails from server without downloading.

ARP → Resolves IP → MAC, works at Data Link + Network.

TCP → Reliable, ordered, connection-oriented.

UDP → Fast, connectionless, for streaming/VoIP.

CSMA/CD → Ethernet collision detection (wired LAN).

CSMA/CA → Collision avoidance (Wi-Fi).

DHCP → Assigns IP automatically.

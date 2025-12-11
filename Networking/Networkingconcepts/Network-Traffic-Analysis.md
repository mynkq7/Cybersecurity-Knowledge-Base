# Network Traffic Analysis

## Network Traffic Analysis — Wireshark

### Overview
- **Wireshark:** Packet analyzer / traffic sniffer  
- **Type:** Open-source  
- **Platform:** Cross-platform  
- **Interface:** GUI-based  

---

## Data Packet Capturing Structure

### **Top Frame (Packet List)**

| Field       | Description                          |
|-------------|--------------------------------------|
| Number      | Packet sequence number               |
| Time        | Timestamp when packet was captured   |
| Source      | Source IP address                    |
| Destination | Destination IP address               |
| Protocol    | Communication protocol used          |
| Length      | Packet size in bytes                 |
| Info        | Summary of packet contents           |

---

### **Middle Frame (Packet Details)**

- **Frame** — General frame information  
- **Linux Cooked Capture** — Link-layer information  
- **Internet Protocol Version (IPv4/IPv6)** — Source & Destination IP addresses  
- **Transmission Control Protocol (TCP)** — Source port, Destination port, Sequence number, Length  

---

### **Bottom Frame (Packet Data)**
Displays raw data / payload in **hexadecimal** and **ASCII** formats.

---

## Wireshark Filters
tcp.port == 80
tcp.srcport == 443
tcp.port == 443 or tcp.port == 80
tcp.port in {80 443 8080}
tcp
udp

### Filter Types
- **Display Filter:** Filters packets displayed in the capture window  
- **Capture Filter:** Filters packets before they are captured  
- **GUI Filter Builder:** Create filters visually using the GUI  

---

## Common Filter Examples

### **TCP/UDP Filters**

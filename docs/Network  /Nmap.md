# Nmap (Network Mapper)

**Nmap** is a fast and flexible network scanning tool used for network discovery and security auditing.

It operates primarily at **Layer 3 (Network layer)** and is widely used in both offensive and defensive security.

---

## Key Features of Nmap

- Fast and flexible network scanner
- Works mainly at Layer 3
- Includes its own scripting engine (**NSE – Nmap Scripting Engine**)
- Supports service, version, and OS detection
- Helps identify misconfigurations

---

## Common Uses of Nmap

### Enumeration & Network Reconnaissance
Nmap is commonly used during:
- Network enumeration
- Asset discovery
- Port scanning
- Service identification

---

## Usage by Attackers

Attackers use Nmap to:
- Discover live hosts
- Identify open ports
- Detect running services
- Gather OS and version information

---

## Usage by Defenders

Defenders and SOC teams use Nmap to:
- Assess network inventory
- Audit exposed services
- Compare expected vs actual open ports
- Identify unauthorized systems
- Support incident investigation

---

## How Nmap Works

Nmap works by sending **probe packets** (commonly SYN packets) to target systems and analyzing the responses.

Based on how the target responds, Nmap determines:
- Port status
- Service behavior
- OS fingerprint

---

## Port States in Nmap

- **Open**  
  The target is actively listening on the port.

- **Closed**  
  The target is reachable, but no service is listening on the port.

- **Filtered**  
  A firewall or filtering device is blocking the traffic.

---

## Nmap Scripting Engine (NSE)

- Nmap includes a built-in scripting engine
- Scripts are used for:
  - Vulnerability detection
  - Service enumeration
  - Authentication checks
  - Configuration analysis

## NSE Script Location

```bash
/usr/share/nmap/scripts

Getting Help in Nmap

To view available options and usage:

nmap --help

This command provides:

Scan types

Timing options

Output formats

Script usage
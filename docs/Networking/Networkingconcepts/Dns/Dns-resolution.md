# DNS Resolution – Root → TLD → Authoritative (Live NSLOOKUP Demo)

This repository demonstrates how DNS resolution works by manually querying Root DNS servers, TLD servers, and authoritative DNS servers using `nslookup`.

We resolve the domain **shopify.com** without relying on the default DNS resolver.

---

## 1. DNS Lookup Flow

When a user types [**www.shopify.com**](http://www.shopify.com/)

in their browser:

1. Browser checks local DNS cache.
2. If not found, it queries the system resolver.
3. System resolver sends the query to a recursive DNS server.
4. Recursive DNS server queries a **Root DNS server** to locate the responsible TLD server for `.com`.
5. The Root server returns the `.com` TLD servers.
6. The recursive resolver queries the **TLD server** for the authoritative nameserver of `shopify.com`.
7. TLD server responds with Shopify’s authoritative DNS servers.
8. Resolver sends the query to the **authoritative nameserver**.
9. Authoritative server returns the final IP address.
10. Browser connects to the server using the resolved IP.

**Lookup Chain:**

**Root Server → TLD Server → Authoritative Server → Final IP**

---

## 2. Step-by-Step Commands and Screenshots

### Step 1: Query Root Server for `.com` TLD Information

```bash
nslookup -type=NS com. a.root-servers.net

```

This returns the list of `.com` TLD servers.

**Screenshot:**

`screenshots/1-root-server.png`

---

### Step 2: Query `.com` TLD Server for Shopify’s Authoritative Nameservers

```bash
nslookup -type=NS shopify.com a.gtld-servers.net

```

This returns Shopify’s authoritative DNS servers.

**Screenshot:**

`screenshots/2-tld-server.png`

---

### Step 3: Query Authoritative Server for Shopify’s Final IP Address

```bash
nslookup shopify.com gold.foundationdns.org

```

This returns the final IP address for `shopify.com`.

**Screenshot:**

`screenshots/3-authoritative-server.png`

---

## 3. DNS Server Roles Summary

### Root DNS Servers

- Know the locations of TLD servers (`.com`, `.net`, `.org`, etc.).
- Do not store IP addresses for domains.

### TLD Servers

- Know which authoritative nameserver handles each domain.
- Do not store IP information.

### Authoritative DNS Servers

- Store actual DNS records: **A, AAAA, CNAME, MX, TXT, etc.**
- Provide the final IP address for the domain.

---

## 4. Repository Structure

```
DNS-Resolution-Live-Demo/
│
├── Dns-resolution.md
│
├── screenshots/
│   ├── 1-root-server.png
│   ├── 2-tld-server.png
│   └── 3-authoritative-server.png
│
└── commands.txt

```

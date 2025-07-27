# 03 - Domain Name System (DNS)

## 🌐 What is DNS?

- DNS = **Domain Name System**.
- Translates **human-readable domains** (e.g., `google.com`) into **IP addresses** (e.g., `142.250.190.46`).
- It’s the **"phonebook"** of the internet.
- Essential for accessing websites, services, APIs, etc.

---

## 🧱 DNS Components

### 🔷 Nameservers
- Servers that store DNS records.
- Example: Google's DNS server → `8.8.8.8`.

### 🔷 Zone Files
- Configuration files on nameservers containing the DNS records for a domain.

### 🔷 DNS Records (Resource Records)
- Instructions stored in the zone file.

---

## 📄 Common DNS Record Types

| Record | Purpose                            | Example |
|--------|------------------------------------|---------|
| A      | Maps domain to IPv4 address        | `google.com → 142.250.190.46` |
| AAAA   | Maps domain to IPv6 address        | `example.com → 2606:4700::` |
| CNAME  | Alias for another domain           | `www → @ (root domain)` |
| MX     | Mail exchange server for domain    | Handles emails |
| TXT    | Freeform text data (e.g., SPF, DKIM) | Used in verification/security |
| NS     | Lists the authoritative name servers | `ns1.provider.com` |

---

## 🔁 DNS Resolution Process (Step-by-Step)

1. **User** types `example.com` in browser.
2. **Local cache** is checked first.
3. If not cached, query goes to **recursive resolver** (ISP or custom like `8.8.8.8`).
4. Resolver asks the **root nameserver**.
5. Root directs to **TLD server** (e.g., `.com`).
6. TLD directs to **authoritative nameserver**.
7. Authoritative server returns the **IP address**.
8. User’s browser connects to the server using that IP.

---

## DNS Debugging: dig & nslookup

dig – Detailed DNS lookup
Examples:
dig google.com            # Full DNS query for google.com, shows all details
dig +short google.com      # Shows only the IP address, no extra info
dig MX gmail.com           # Queries MX (mail) records for gmail.com
dig @8.8.8.8 google.com    # Queries google.com using Google’s public DNS server

nslookup – Quick domain check
Examples:
nslookup google.com                # Basic DNS lookup for google.com
nslookup -query=MX gmail.com       # Lookup MX (mail) records for gmail.com
nslookup google.com 8.8.8.8        # Use Google DNS server for lookup

Both tools help check DNS records and troubleshoot name resolution issues.

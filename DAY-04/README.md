## 🌐 Network Fundamentals

### What is a Network?
A **network** is a collection of interconnected devices (computers, servers, routers, etc.) that can communicate and share resources with each other. Networks can be as small as two computers connected directly or as large as the entire Internet.

### What is a Subnet?
A **subnet** (subnetwork) is a logical subdivision of an IP network. It allows network administrators to divide a large network into smaller, more manageable segments. Subnets help improve network performance, enhance security, and reduce broadcast traffic.

### What is Port Forwarding?
**Port forwarding** is a networking technique that redirects communication requests from one IP address and port number combination to another. It allows external devices to connect to services running on specific ports within a private network, typically used to make internal servers accessible from the internet.

### 🔐 Security Note: Antivirus Limitations
**Important Fact**: Antivirus software typically does **not have permission to access password-protected files** (such as encrypted ZIP files, password-protected documents, or encrypted containers). This means:
- Malware can potentially hide in encrypted/password-protected archives
- Antivirus scans may not detect threats within protected files
- Users should be cautious when opening password-protected files from unknown sources
- Additional security measures are needed for comprehensive protection

### 🛡️ User Account Control (UAC)
**User Account Control (UAC)** is a security feature in Windows that prevents unauthorized changes to the operating system. UAC works by:
- Requiring administrator approval for system-level changes
- Running applications with standard user privileges by default
- Prompting for credentials when administrative actions are attempted
- Helping prevent malware from making unauthorized system modifications

**UAC Levels:**
- **Always Notify**: Prompts for every system change
- **Notify me only when apps try to make changes**: Default setting
- **Notify me only when apps try to make changes (don't dim desktop)**: Same as above but without dimming
- **Never notify**: Disables UAC protection (not recommended)

### 🔍 Have I Been Pwned?
**Have I Been Pwned (HIBP)** is a free online service created by security expert Troy Hunt that allows users to check if their personal data has been compromised in data breaches. Features include:
- **Email breach checking**: See if your email address has appeared in known data breaches
- **Password checking**: Verify if your password has been exposed (using k-anonymity for privacy)
- **Paste search**: Check if your information appears in pasted content online
- **Domain search**: See breaches for specific domains
- **API access**: Developers can integrate HIBP into their applications

**Website**: https://haveibeenpwned.com

### 🕰️ Wayback Machine
**Wayback Machine** is a digital archive of the World Wide Web maintained by the Internet Archive. It allows users to:
- **View historical versions** of websites from the past
- **Recover lost content** from deleted or modified web pages
- **Research website evolution** over time
- **Verify information** by checking historical records
- **Access cached versions** when original sites are down

**Key Features:**
- Over 700 billion web pages archived
- Dating back to 1996
- Search by URL to see capture history
- Save pages to the archive
- API available for developers

**Website**: https://archive.org/web/

### 🔄 API (Application Programming Interface)
An **API** is a set of rules and protocols that allows different software applications to communicate with each other. APIs define:
- **Methods of communication** between applications
- **Data formats** for requests and responses
- **Authentication** mechanisms
- **Rate limits** and usage restrictions

**Types of APIs:**
- **REST APIs**: Use HTTP methods (GET, POST, PUT, DELETE)
- **GraphQL**: Query language for APIs
- **SOAP**: Protocol for exchanging structured information
- **WebSocket**: Full-duplex communication channels

**Common API Uses:**
- Integrating third-party services
- Building microservices
- Mobile app development
- Web service integration

### 🌐 .env (Environment Variables)
A **.env file** is a configuration file that stores environment variables, typically used to:
- **Store sensitive information** (API keys, passwords, secrets)
- **Configure application settings** without hardcoding
- **Separate configuration** from code
- **Manage different environments** (development, staging, production)

**Best Practices:**
- Never commit .env files to version control
- Add .env to .gitignore
- Use different .env files for different environments
- Validate required environment variables
- Use libraries like dotenv for loading variables

### 🗡️ Nmap Flags (Kali Linux)
**Nmap** is a powerful network discovery and security auditing tool. Common flags include:

| Flag | Description |
|------|-------------|
| **-Pn** | Treat all hosts as online (skip host discovery) |
| **-A** | Enable OS detection, version detection, script scanning, and traceroute |
| **-sV** | Service version detection |
| **-O** | Enable OS detection |
| **-oN** | Output scan results in normal format to specified file |
| **--script** | Run specified NSE (Nmap Scripting Engine) scripts |
| **-vv** | Increase verbosity level (very verbose) |
| **-p-** | Scan all 65535 ports |
| **-p** | Scan specified ports (e.g., -p 80,443 or -p 1-1000) |
| **-sS** | TCP SYN scan (default scan type) |
| **-sT** | TCP connect scan |

**Common Scan Examples:**
- `nmap -A -p- target.com` - Comprehensive scan of all ports
- `nmap -sS -p 80,443 target.com` - SYN scan on specific ports
- `nmap -O -sV target.com` - OS and service detection
- `nmap --script vuln target.com` - Run vulnerability scripts

---

## 📡 TCP vs UDP Comparison

| Feature | TCP | UDP |
|---------|-----|-----|
| **Connection** | Connection-oriented (3-way handshake) | Connectionless |
| **Reliability** | ✅ Guaranteed delivery | ❌ No delivery guarantee |
| **Ordering** | ✅ In-order delivery | ❌ May arrive out of order |
| **Error Handling** | ✅ Error detection & correction | ❌ Basic error detection only |
| **Speed** | ❌ Slower (more overhead) | ✅ Faster (minimal overhead) |
| **Header Size** | 20-60 bytes | 8 bytes |
| **Flow Control** | ✅ Yes (sliding window) | ❌ No |
| **Congestion Control** | ✅ Yes (adaptive) | ❌ No |
| **Use Cases** | Web, email, file transfer | Streaming, gaming, DNS |
| **Protocols** | HTTP, HTTPS, FTP, SMTP | DNS, DHCP, VoIP, RTP |

### 🎯 When to Use TCP vs UDP

**TCP** when you need: **Reliability** > Speed
- Web applications, file transfers, email, database operations

**UDP** when you need: **Speed** > Reliability  
- Video/audio streaming, online gaming, real-time systems, DNS queries

---

## 🌐 IPv4 vs IPv6 Comparison

| Feature | IPv4 | IPv6 |
|---------|------|------|
| **Address Length** | 32-bit | 128-bit |
| **Address Format** | Dotted decimal (e.g., 192.168.1.1) | Hexadecimal (e.g., 2001:0db8::1) |
| **Address Space** | ~4.3 billion addresses | ~340 undecillion addresses |
| **Header Size** | 20 bytes (minimum) | 40 bytes (fixed) |
| **Security** | Optional | Built-in IPsec support |
| **Configuration** | Manual or DHCP | Auto-configuration capabilities |
| **Mobility** | Limited support | Built-in mobility support |
| **Header Checksum** | Present | Removed (handled by higher layers) |
| **Broadcast** | Supported | Replaced with multicast |
| **Use Cases** | Legacy systems, current internet | Future internet, IoT devices |

### 🎯 When to Use IPv4 vs IPv6

**IPv4** for: Legacy systems, smaller networks, compatibility
**IPv6** for: Future-proofing, large networks, IoT devices

---

## 🖥️ MAC Address Information

| Feature | Description |
|---------|-------------|
| **Purpose** | Unique hardware identifier for network interfaces |
| **Format** | 6 bytes (48 bits) represented as 12 hexadecimal digits |
| **Example** | 00:1A:2B:3C:4D:5E |
| **Assignment** | Assigned by manufacturer |
| **Uniqueness** | Globally unique identifier |
| **Use Cases** | Network access control, device identification, ARP resolution |
| **Security** | Can be spoofed, limited built-in security features |
| **Validation** | CRC (Cyclic Redundancy Check) |

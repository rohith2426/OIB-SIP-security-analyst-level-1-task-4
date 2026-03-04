# Network Security Threats — Research Report

## 1. Introduction

Network security threats are malicious activities targeting computer networks with the intent to disrupt operations, steal data, or damage systems. These attacks exploit vulnerabilities in protocols, software, hardware, or human behaviour. Understanding common network threats—such as DoS/DDoS, Man-in-the-Middle, and spoofing—is critical for designing effective defence mechanisms.

## 2. Denial-of-Service (DoS) and Distributed DoS (DDoS) Attacks

### 2.1 Description & Mechanism

A Denial-of-Service (DoS) attack aims to make a system, network, or service unavailable to legitimate users by overwhelming it with excessive requests or exhausting its resources (e.g., bandwidth, CPU). In Distributed DoS (DDoS) attacks, many compromised systems (a *botnet*) send malicious traffic to the target simultaneously, amplifying the disruption.

Common types include:

- **Flood attack** (e.g., UDP flood, TCP SYN flood) where massive traffic saturates server capacity.
- **Application-layer DoS** targeting specific services (e.g., HTTP requests).
- **Hit-and-run DDoS**, short bursts of heavy traffic that evade detection systems.

### 2.2 Impact

DoS/DDoS attacks can cause:

- Service outages and loss of availability.
- Revenue loss and reputational damage for businesses.
- Distraction for further attacks (e.g., data breaches).

### 2.3 Real-World Examples

- The **GitHub DDoS attack (2018)** reached a historic 1.35 Tbps using memcached amplification, briefly taking the platform offline.
- The **Dyn DNS attack (2016)** crippled major websites like Netflix, Reddit, and Twitter by targeting a key DNS provider.
- Server infrastructure experienced record DDoS peaks exceeding **22 Tbps** in 2025 — underscoring rising attack volumes.

### 2.4 Mitigation and Prevention

- **Traffic filtering & rate limiting** — block suspicious traffic patterns.
- **DDoS mitigation services** (scrubbing centers) to absorb/deflect attacks.
- **Redundant infrastructure & CDNs** to distribute load.
- **Firewalls, IPS/IDS, and access control** to limit attack surfaces.

## 3. Man-in-the-Middle (MITM) Attacks

### 3.1 Description & How It Works

In a **Man-in-the-Middle (MITM)** attack, an adversary intercepts communication between two parties without their knowledge. The attacker can eavesdrop, alter, or inject data, impersonating one or both sides.

Common MITM techniques include:

- **ARP spoofing** — attackers poison ARP tables on LAN to reroute traffic via their device.
- **DNS spoofing** — forged DNS responses redirect users to malicious servers.
- **SSL/TLS stripping** — downgrading HTTPS to HTTP to access plaintext data.
- **Rogue Wi-Fi networks** — fake hotspots intercept user traffic.

### 3.2 Impact

MITM attacks can lead to:

- Credential theft and account compromise.
- Data alteration or financial fraud.
- Long-term unauthorized access to sensitive communications.

### 3.3 Real-World Examples

- **Equifax data breach (2017)** involved attackers exploiting vulnerable infrastructure, enabling MITM to steal information of ~145 million users.
- **Lenovo Superfish (2014)** shipped a pre-installed adware that enabled HTTPS interception, undermining trust in secure connections.

### 3.4 Mitigation and Prevention

- **Use HTTPS/TLS & certificate validation** to ensure secure channels.
- **Avoid unsecured public Wi-Fi** or use trusted VPNs.
- **Harden DNS with DNSSEC** to prevent DNS manipulation.
- **Network segmentation & endpoint security** to reduce exposure.

## 4. Spoofing Attacks

### 4.1 Definition & Mechanism

Spoofing attacks involve impersonating legitimate identities (IP address, email address, domain name, etc.) to deceive systems or users. The attacker falsifies information to gain access or redirect traffic.

Types include:

- **IP Spoofing** — forging source IP to conceal identity or bypass filters.
- **Email spoofing** — fake sender information used in scams and phishing.
- **Domain or URL spoofing** — attackers redirect users to look-alike malicious sites.

### 4.2 Impact

- Enables **DDoS amplification** via botnet coordination (IP spoofing).
- Leads to **phishing success**, fraud, and credential compromise.
- Weakens trust in digital communications.

### 4.3 Real-World Examples

- The **GitHub DDoS attack** used IP spoofing to generate massive traffic with memcached reflection.
- Email spoofing campaigns caused billions in losses reported by the US FBI in 2021.

### 4.4 Mitigation and Prevention

- **Ingress/egress filtering** (BCP 38) to block spoofed IP packets.
- **Email authentication standards** such as SPF, DKIM, and DMARC.
- **Multi-factor authentication (MFA)** to reduce the impact of credential compromise.

## 5. Conclusion

Network security threats such as DoS/DDoS, MITM, and spoofing continue to evolve in scale and sophistication. Real-world incidents demonstrate the disruptive impact these attacks can have on organizations and individuals alike. Effective defenses rely on a combination of secure protocols, traffic monitoring, infrastructure hardening, and ongoing cybersecurity vigilance.

## References

1. [Denial-of-service attack - Wikipedia](https://en.wikipedia.org/wiki/Denial-of-service_attack)
2. [UDP flood attack - Wikipedia](https://en.wikipedia.org/wiki/UDP_flood_attack)
3. [Hit-and-run DDoS - Wikipedia](https://en.wikipedia.org/wiki/Hit-and-run_DDoS)
4. [Five Most Famous DDoS Attacks and Then Some - A10 Networks](https://www.a10networks.com/blog/5-most-famous-ddos-attacks/)
5. [The Most Famous DDoS Attacks - Corero](https://www.corero.com/famous-ddos-attacks/)
6. [Cloudflare blocks largest DDoS attack in history - TechRadar](https://www.techradar.com/pro/security/cloudflare-says-it-has-once-again-blocked-the-largest-ever-ddos-attack-in-history)
7. [Man-in-the-Middle Attack (MITM) - Techopedia](https://www.techopedia.com/definition/4018/man-in-the-middle-attack-mitm)
8. [Man-in-the-Middle Attack - SSL Insights](https://sslinsights.com/man-in-the-middle-attack/)
9. [What Is a MITM Attack - DNSFilter](https://www.dnsfilter.com/glossary/mitm)
10. [Man-in-the-Middle Attacks - Netwrix](https://netwrix.com/en/cybersecurity-glossary/cyber-security-attacks/man-in-the-middle-attack-mitm/)
11. [Spoofing attack - Wikipedia](https://en.wikipedia.org/wiki/Spoofing_attack)
12. [IP Spoofing & Spoof Attacks - Kaspersky](https://www.kaspersky.com/resource-center/threats/ip-spoofing)
13. [What is Email Spoofing - SentinelOne](https://www.sentinelone.com/cybersecurity-101/threat-intelligence/email-spoofing/)
14. [What Is Spoofing - SOSAFE](https://sosafe-awareness.com/glossary/spoofing/)
15. [What is IP Spoofing - Twingate](https://www.twingate.com/blog/glossary/ip-spoofing)
